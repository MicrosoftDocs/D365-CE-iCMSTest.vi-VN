---
title: Use OAuth with Cross-Origin Resource Sharing to connect a Single Page Application (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: Learn how to use OAuth with Cross-Origin Resource Sharing to connect a Single Page Application to Dynamics 365 for Customer Engagement apps
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: oauth-cross-origin-resource-sharing-connect-single-page-application
caps.latest.revision: 11
author: JimDaly
ms.author: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f8746045ec707b0c8791463584ae78452e355d1c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388143"
---
# <a name="use-oauth-with-cross-origin-resource-sharing--to-connect-a-single-page-application--to-dynamics-365-for-customer-engagement-apps"></a>Use OAuth with Cross-Origin Resource Sharing  to connect a Single Page Application  to Dynamics 365 for Customer Engagement apps

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

You can create a Single Page Apps (SPAs) which uses [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] to work with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps data. To provide this, Cross-Origin Resource Sharing (CORS) is enabled so that your SPAs can bypass browser restrictions that normally prevent requests that cross domain boundaries.  
  
> [!NOTE]
>  CORS support is only provided when using the Web API. You cannot use the organization service or the deprecated organization data service.  
  
<a name="bkmk_Spas_and_same_origin_policy"></a>   
## <a name="spas-and-same-origin-policy"></a>SPAs and Same-Origin policy  
 SPAs depend on extensive use of client-side [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] to create a single dynamic page which doesn't need to load new pages. Instead they use XMLHTTPRequests to retrieve data and other resources from the server. SPAs work well when the data and resources exist in the same domain as the application. But to protect access to data and resources on other domains, all modern browsers enforce a Same-Origin policy to prevent sites from using data and resources from sites on a different domain. CORS provides a way to gain access to resources on another domain. Creating a SPA to access [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps data without CORS is not a viable option.  
  
<a name="bkmk_use_cors"></a>   
## <a name="use-cors-with-includepndynamicscrmonlineincludespn-dynamics-crm-onlinemd-apps"></a>Use CORS with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps
 The [Cross-Origin Resource Sharing specification](http://www.w3.org/TR/cors/) provides a detailed description of how to implement and use CORS. It explains all about the various headers and preflight requests that you need to apply to make CORS work. The good news is that you don't need to become an expert in CORS to use it with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps. The server-side part has been done for you and all you need is to know how to consume it.  You don't need to understand all the inner workings of CORS to use it with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps. Instead you can use the [Azure Active Directory Authentication Library for JavaScript](https://github.com/AzureAD/azure-activedirectory-library-for-js) (adal.js) and it will take care of much of the CORS complexity for you. Since [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] and Internet-facing deployment (IFD) users are authenticated using Azure Active Directory, ADAL.js is the supported way to authenticate SPA users.  
  
<a name="bkmk_how_adaljs_works"></a>   
## <a name="how-adaljs-works"></a>How adal.js works  
 The core library is `adal.js`. You can access the minimized version of this library at [https://secure.aadcdn.microsoftonline-p.com/lib/1.0.0/js/adal.min.js](https://secure.aadcdn.microsoftonline-p.com/lib/1.0.0/js/adal.min.js). The Github project and documentation is at [https://github.com/AzureAD/azure-activedirectory-library-for-js](https://github.com/AzureAD/azure-activedirectory-library-for-js).  
  
 The adal.js library contains the low-level capabilities to authenticate using OAuth2. Adal.js is designed so that it can be used with other frameworks, for example there is an `adal-angular.js` library that is designed to be used with the Angular framework.The way you work with this library is to set certain configuration properties and then it will wait until events occur that trigger the interaction flow. This could be simply calling the `login` function or if your application has routing behaviors, the authentication can be initiated by how the controller for that route is configured.  
  
 When authentication is required, the user is taken to the sign-in page where they can enter their credentials. After they successfully authenticate, they are re-directed back to the calling page with the token information attached as a fragment (using #) to the URL. This allows the SPA to acquire the token and cache it in local or session storage in the browser. This means that the entire page is re-loaded after authentication, but this time the information about the authorized user is available and the application can proceed to make calls the Dynamics 365 for Customer Engagement Web API or other resources.  
  
 When calling the Dynamics 365 for Customer Engagement Web API, you must include the token value in an Authorization header with your XMLHTPPRequest. However, because tokens have an expiration you want to be sure that it doesn't expire while people are using your SPA. Remember, entering new credentials requires that the entire content of your SPA page is transferred to the sign-in page. This would cause a very bad user experience if it were to happen while people are in the middle of doing something. In order to ensure this doesn't happen, you wrap your Web API calls within an `acquireToken` function so that the validity of the token can be checked and refreshed if necessary without taking the user to a sign-in page.  
  
<a name="bkmk_preparing_to_use_adaljs"></a>   
## <a name="preparing-to-use-adaljs-with-a-spa"></a>Preparing to use ADAL.js with a SPA  
 In order to configure your SPA to work with adal.js you will need to :  
  
1. Register your application with the Azure Active Directory tenant  
  
2. Export your registered application manifest and edit it to allow OAuth2 Implicit Flow, and then import the JSON file back to your application registration.  
  
3. Set configuration variables in your SPA with information from that registration.  
  
    You will need to include the following:  
  
   - The URL to your [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps organization  
  
   - The name of the Active Directory tenant your organization uses to authenticate  
  
   - The client ID you get when you register your application  
  
   - The URL to where the SPA will be deployed or debugged during development  
  
   The set of steps required are described in [Walkthrough: Registering and configuring SimpleSPA application with adal.js](walkthrough-registering-configuring-simplespa-application-adal-js.md).  
  
### <a name="see-also"></a>Xem thêm  
 [Authenticate users in Dynamics 365 for Customer Engagement apps](authenticate-users.md)   
 [Use OAuth to connect to Dynamics 365 for Customer Engagement web Services](connect-customer-engagement-web-services-using-oauth.md)   
 [Active Directory and Claims-Based Authentication](active-directory-claims-based-authentication.md)
