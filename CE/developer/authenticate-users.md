---
title: Authenticate users in Dynamics 365 for Customer Engagement (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: Learn about the various security models for authentication that Dynamics 365 for Customer Engagement apps support
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: a9cbe79f-6f3b-44a7-aac4-f6f982bee2e5
caps.latest.revision: 55
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4d7b4cf954b8d6aca2a0fb500f1241b01aae7e5a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388203"
---
# <a name="authenticate-users-in-dynamics-365-for-customer-engagement-apps"></a><span data-ttu-id="71f7d-103">Authenticate users in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="71f7d-103">Authenticate users in Dynamics 365 for Customer Engagement apps</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="71f7d-104">apps support three security models for authentication: claims-based authentication, [!INCLUDE[pn_Active_Directory](../includes/pn-active-directory.md)] authentication, and OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="71f7d-104">apps support three security models for authentication: claims-based authentication, [!INCLUDE[pn_Active_Directory](../includes/pn-active-directory.md)] authentication, and OAuth 2.0.</span></span> <span data-ttu-id="71f7d-105">The type of authentication used depends on the type of deployment your application is accessing (Online, on-premises, or internet facing deployment) and if your application is using the Web API or the Organization Service.</span><span class="sxs-lookup"><span data-stu-id="71f7d-105">The type of authentication used depends on the type of deployment your application is accessing (Online, on-premises, or internet facing deployment) and if your application is using the Web API or the Organization Service.</span></span>  
  
 <span data-ttu-id="71f7d-106">In addition to using the correct security model, applications must establish a communication channel with the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web services on the target deployment.</span><span class="sxs-lookup"><span data-stu-id="71f7d-106">In addition to using the correct security model, applications must establish a communication channel with the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web services on the target deployment.</span></span> <span data-ttu-id="71f7d-107">The SDK run-time assemblies use [Windows Communication Foundation](https://msdn.microsoft.com/netframework/aa663324.aspx) ([!INCLUDE[pn_WCF_short](../includes/pn-wcf-short.md)]) technology to establish this communication channel.</span><span class="sxs-lookup"><span data-stu-id="71f7d-107">The SDK run-time assemblies use [Windows Communication Foundation](https://msdn.microsoft.com/netframework/aa663324.aspx) ([!INCLUDE[pn_WCF_short](../includes/pn-wcf-short.md)]) technology to establish this communication channel.</span></span>  
  
 <span data-ttu-id="71f7d-108">The SDK assemblies simplify use of [!INCLUDE[pn_WCF_short](../includes/pn-wcf-short.md)] technology and claims-based authentication by providing helper proxy classes that make it easy to write applications that connect to and authenticate with the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web services.</span><span class="sxs-lookup"><span data-stu-id="71f7d-108">The SDK assemblies simplify use of [!INCLUDE[pn_WCF_short](../includes/pn-wcf-short.md)] technology and claims-based authentication by providing helper proxy classes that make it easy to write applications that connect to and authenticate with the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web services.</span></span> <span data-ttu-id="71f7d-109">By using these helper classes in your application, you can access any [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps deployment using the same code and you don’t have to become an expert in claims-based security or [!INCLUDE[pn_WCF_short](../includes/pn-wcf-short.md)] programming.</span><span class="sxs-lookup"><span data-stu-id="71f7d-109">By using these helper classes in your application, you can access any [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps deployment using the same code and you don’t have to become an expert in claims-based security or [!INCLUDE[pn_WCF_short](../includes/pn-wcf-short.md)] programming.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="71f7d-110">In This Section</span><span class="sxs-lookup"><span data-stu-id="71f7d-110">In This Section</span></span>  
 [<span data-ttu-id="71f7d-111">Use OAuth to connect to Dynamics 365 for Customer Engagement web Services</span><span class="sxs-lookup"><span data-stu-id="71f7d-111">Use OAuth to connect to Dynamics 365 for Customer Engagement web Services</span></span>](connect-customer-engagement-web-services-using-oauth.md)  
  
 [<span data-ttu-id="71f7d-112">Use OAuth with Cross-Origin Resource Sharing  to connect a Single Page Application  to Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="71f7d-112">Use OAuth with Cross-Origin Resource Sharing  to connect a Single Page Application  to Dynamics 365 for Customer Engagement apps</span></span>](oauth-cross-origin-resource-sharing-connect-single-page-application.md)  
  
 [<span data-ttu-id="71f7d-113">Active Directory and Claims-Based Authentication</span><span class="sxs-lookup"><span data-stu-id="71f7d-113">Active Directory and Claims-Based Authentication</span></span>](active-directory-claims-based-authentication.md)  
  
## <a name="related-sections"></a><span data-ttu-id="71f7d-114">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="71f7d-114">Related Sections</span></span>  
 [<span data-ttu-id="71f7d-115">Connect to Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="71f7d-115">Connect to Dynamics 365 for Customer Engagement apps</span></span>](connect-customer-engagement.md)  
  
 [<span data-ttu-id="71f7d-116">OAuth 2.0</span><span class="sxs-lookup"><span data-stu-id="71f7d-116">OAuth 2.0</span></span>](http://oauth.net/2/)  
  
 [<span data-ttu-id="71f7d-117">Authorization Code Grant Flow</span><span class="sxs-lookup"><span data-stu-id="71f7d-117">Authorization Code Grant Flow</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn645542.aspx)  
  
 [<span data-ttu-id="71f7d-118">Use the Dynamics 365 for Customer Engagement Web API</span><span class="sxs-lookup"><span data-stu-id="71f7d-118">Use the Dynamics 365 for Customer Engagement Web API</span></span>](use-microsoft-dynamics-365-web-api.md)  
  
 [<span data-ttu-id="71f7d-119">Use the Dynamics 365 for Customer Engagement Organization Service</span><span class="sxs-lookup"><span data-stu-id="71f7d-119">Use the Dynamics 365 for Customer Engagement Organization Service</span></span>](use-microsoft-dynamics-365-organization-service.md)
