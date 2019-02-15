---
title: Authenticate to Dynamics 365 for Customer Engagement with the Web API (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Learn about the different ways to manage authentication when using the Web API
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 767f39d4-6a8e-48f0-bf7d-69ea1191acef
caps.latest.revision: 8
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2e7236f4507cfe197d1ad3803a98b52f78212f46
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388468"
---
# <a name="authenticate-to-dynamics-365-for-customer-engagement-with-the-web-api"></a><span data-ttu-id="f548d-103">Authenticate to Dynamics 365 for Customer Engagement with the Web API</span><span class="sxs-lookup"><span data-stu-id="f548d-103">Authenticate to Dynamics 365 for Customer Engagement with the Web API</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="f548d-104">The code you write to manage authentication when using the Web API depends on the type of deployment and where your code is.</span><span class="sxs-lookup"><span data-stu-id="f548d-104">The code you write to manage authentication when using the Web API depends on the type of deployment and where your code is.</span></span>  
  
## <a name="web-api-authentication-patterns"></a><span data-ttu-id="f548d-105">Web API authentication patterns</span><span class="sxs-lookup"><span data-stu-id="f548d-105">Web API authentication patterns</span></span>  
 <span data-ttu-id="f548d-106">There are three different ways to manage authentication when using the Web API.</span><span class="sxs-lookup"><span data-stu-id="f548d-106">There are three different ways to manage authentication when using the Web API.</span></span>  
  
### <a name="with-javascript-in-web-resources"></a><span data-ttu-id="f548d-107">With JavaScript in web resources</span><span class="sxs-lookup"><span data-stu-id="f548d-107">With JavaScript in web resources</span></span>  
 <span data-ttu-id="f548d-108">When you use the Web API with [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] within HTML web resources, form scripts, or ribbon commands you don’t need to include any code for authentication.</span><span class="sxs-lookup"><span data-stu-id="f548d-108">When you use the Web API with [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] within HTML web resources, form scripts, or ribbon commands you don’t need to include any code for authentication.</span></span> <span data-ttu-id="f548d-109">In each of these cases the user is already authenticated by the application and authentication is managed by the application.</span><span class="sxs-lookup"><span data-stu-id="f548d-109">In each of these cases the user is already authenticated by the application and authentication is managed by the application.</span></span>  
  
### <a name="with-on-premises-deployments"></a><span data-ttu-id="f548d-110">With on-premises deployments</span><span class="sxs-lookup"><span data-stu-id="f548d-110">With on-premises deployments</span></span>  

[!INCLUDE[cc_sdk_onpremises_note](../../includes/cc-sdk-onpremises-note.md)] 

<span data-ttu-id="f548d-111">When you use the Web API for on-premises deployments you must include the user’s network credentials.</span><span class="sxs-lookup"><span data-stu-id="f548d-111">When you use the Web API for on-premises deployments you must include the user’s network credentials.</span></span> <span data-ttu-id="f548d-112">The following example is a C# function that will return an [HttpClient](https://msdn.microsoft.com/library/system.net.http.httpclient\(v=vs.110\).aspx) configured for a given user’s network credentials:</span><span class="sxs-lookup"><span data-stu-id="f548d-112">The following example is a C# function that will return an [HttpClient](https://msdn.microsoft.com/library/system.net.http.httpclient\(v=vs.110\).aspx) configured for a given user’s network credentials:</span></span>  
  
```csharp  
private HttpClient getNewHttpClient(string userName,string password,string domainName, string webAPIBaseAddress)  
{  
    HttpClient client = new HttpClient(new HttpClientHandler() { Credentials = new NetworkCredential(userName, password, domainName) });  
    client.BaseAddress = new Uri(webAPIBaseAddress);  
    client.Timeout = new TimeSpan(0, 2, 0);  
    return client;  
}  
```  
  
### <a name="with-includepndynamicscrmonlineincludespn-dynamics-crm-onlinemd-or-internet-facing-deployments"></a><span data-ttu-id="f548d-113">With [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] or Internet-facing deployments</span><span class="sxs-lookup"><span data-stu-id="f548d-113">With [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] or Internet-facing deployments</span></span>  
 <span data-ttu-id="f548d-114">When you use the Web API for [!INCLUDE[pn_crm_online_shortest](../../includes/pn-crm-online-shortest.md)] Customer Engagement or an on-premises Internet-facing deployment (IFD) you must use OAuth as described in [Use OAuth to connect to Dynamics 365 for Customer Engagement web Services](../connect-customer-engagement-web-services-using-oauth.md).</span><span class="sxs-lookup"><span data-stu-id="f548d-114">When you use the Web API for [!INCLUDE[pn_crm_online_shortest](../../includes/pn-crm-online-shortest.md)] Customer Engagement or an on-premises Internet-facing deployment (IFD) you must use OAuth as described in [Use OAuth to connect to Dynamics 365 for Customer Engagement web Services](../connect-customer-engagement-web-services-using-oauth.md).</span></span>  
  
 <span data-ttu-id="f548d-115">If you’re creating a single page application (SPA) using [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] you can use the adal.js library as described in [Use OAuth with Cross-Origin Resource Sharing  to connect a Single Page Application  to Dynamics 365 for Customer Engagement](../oauth-cross-origin-resource-sharing-connect-single-page-application.md).</span><span class="sxs-lookup"><span data-stu-id="f548d-115">If you’re creating a single page application (SPA) using [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] you can use the adal.js library as described in [Use OAuth with Cross-Origin Resource Sharing  to connect a Single Page Application  to Dynamics 365 for Customer Engagement](../oauth-cross-origin-resource-sharing-connect-single-page-application.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f548d-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="f548d-116">See also</span></span>  
 <span data-ttu-id="f548d-117">[Use the Dynamics 365 for Customer Engagement Web API](../use-microsoft-dynamics-365-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="f548d-117">[Use the Dynamics 365 for Customer Engagement Web API](../use-microsoft-dynamics-365-web-api.md) </span></span>  
 <span data-ttu-id="f548d-118">[Web API types and operations](web-api-types-operations.md) </span><span class="sxs-lookup"><span data-stu-id="f548d-118">[Web API types and operations](web-api-types-operations.md) </span></span>  
 <span data-ttu-id="f548d-119">[Perform operations using the Web API](perform-operations-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="f548d-119">[Perform operations using the Web API](perform-operations-web-api.md) </span></span>  
 <span data-ttu-id="f548d-120">[Use OAuth to connect to Dynamics 365 for Customer Engagement web Services](../connect-customer-engagement-web-services-using-oauth.md) </span><span class="sxs-lookup"><span data-stu-id="f548d-120">[Use OAuth to connect to Dynamics 365 for Customer Engagement web Services](../connect-customer-engagement-web-services-using-oauth.md) </span></span>  
 [<span data-ttu-id="f548d-121">Use OAuth with Cross-Origin Resource Sharing  to connect a Single Page Application  to Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="f548d-121">Use OAuth with Cross-Origin Resource Sharing  to connect a Single Page Application  to Dynamics 365 for Customer Engagement</span></span>](../oauth-cross-origin-resource-sharing-connect-single-page-application.md)
