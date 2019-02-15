---
title: Discover the URL for your organization using the Discovery Service (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: For a multi-tenant environment like Dynamics 365 for Customer Engagement, you can use Discovery Service to determine the organizations that a user is member of
ms.custom: ''
ms.date: 11/14/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 29b0777c-f28d-4301-ae5c-a25064bfbcc9
caps.latest.revision: 46
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ddec3aabdbdc25a5a066805f89689b03c730b76a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385884"
---
# <a name="discover-the-url-for-your-organization-using-the-discovery-service"></a><span data-ttu-id="046d8-103">Discover the URL for your organization using the Discovery Service</span><span class="sxs-lookup"><span data-stu-id="046d8-103">Discover the URL for your organization using the Discovery Service</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="046d8-104">Use the discovery service to determine the organizations that a user is a member of, and the endpoint address URL to access the organization service for each of those organizations.</span><span class="sxs-lookup"><span data-stu-id="046d8-104">Use the discovery service to determine the organizations that a user is a member of, and the endpoint address URL to access the organization service for each of those organizations.</span></span> <span data-ttu-id="046d8-105">This discovery service is necessary because [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps is a multi-tenant environment—a single [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps server can host multiple business organizations.</span><span class="sxs-lookup"><span data-stu-id="046d8-105">This discovery service is necessary because [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps is a multi-tenant environment—a single [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps server can host multiple business organizations.</span></span> <span data-ttu-id="046d8-106">By using the discovery service, your application can determine the endpoint address URL to access the target organization’s business data.</span><span class="sxs-lookup"><span data-stu-id="046d8-106">By using the discovery service, your application can determine the endpoint address URL to access the target organization’s business data.</span></span>  
  
 <span data-ttu-id="046d8-107">For [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps installations, server and organization allocation may change as part of datacenter management and load balancing.</span><span class="sxs-lookup"><span data-stu-id="046d8-107">For [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps installations, server and organization allocation may change as part of datacenter management and load balancing.</span></span> <span data-ttu-id="046d8-108">Therefore, the discovery service provides a way to discover which [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps server is serving your organization at a given time.</span><span class="sxs-lookup"><span data-stu-id="046d8-108">Therefore, the discovery service provides a way to discover which [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps server is serving your organization at a given time.</span></span>  
  
 <span data-ttu-id="046d8-109">The following table lists the Web service URLs for the worldwide [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md) apps data centers.</span><span class="sxs-lookup"><span data-stu-id="046d8-109">The following table lists the Web service URLs for the worldwide [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md) apps data centers.</span></span>  

[!INCLUDE [regional-discovery-services](../../includes/regional-discovery-services.md)]
  
 <span data-ttu-id="046d8-110">For an Internet-facing deployment (IFD) installation, the Web service URL has the following form:</span><span class="sxs-lookup"><span data-stu-id="046d8-110">For an Internet-facing deployment (IFD) installation, the Web service URL has the following form:</span></span>  
  
```  
https://dev.<hostname[:port]>/XRMServices/2011/Discovery.svc  
```  
  
 <span data-ttu-id="046d8-111">For an on-premises installation, the web service URL has the following form:</span><span class="sxs-lookup"><span data-stu-id="046d8-111">For an on-premises installation, the web service URL has the following form:</span></span>  
  
[!INCLUDE[cc_sdk_onpremises_note](../../includes/cc-sdk-onpremises-note.md)]
```  
http[s]://<hostname[:port]>/XRMServices/2011/Discovery.svc  
```  
  
 <span data-ttu-id="046d8-112">Consult the **Developer Resources** page in the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Web application for the correct URL of your installation.</span><span class="sxs-lookup"><span data-stu-id="046d8-112">Consult the **Developer Resources** page in the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Web application for the correct URL of your installation.</span></span>  
  
 <span data-ttu-id="046d8-113">To use the discovery service, add a reference to the `Microsoft.Xrm.Sdk.dll` assembly to your [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] project, and then add a `using` or `imports` statement to access the <xref:Microsoft.Xrm.Sdk.Discovery> namespace.</span><span class="sxs-lookup"><span data-stu-id="046d8-113">To use the discovery service, add a reference to the `Microsoft.Xrm.Sdk.dll` assembly to your [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] project, and then add a `using` or `imports` statement to access the <xref:Microsoft.Xrm.Sdk.Discovery> namespace.</span></span> <span data-ttu-id="046d8-114">The <xref:Microsoft.Xrm.Sdk.Discovery.IDiscoveryService> interface provides <xref:Microsoft.Xrm.Sdk.Discovery.IDiscoveryService.Execute*> method you will use to pass a instance of the <xref:Microsoft.Xrm.Sdk.Discovery.DiscoveryRequest> class.</span><span class="sxs-lookup"><span data-stu-id="046d8-114">The <xref:Microsoft.Xrm.Sdk.Discovery.IDiscoveryService> interface provides <xref:Microsoft.Xrm.Sdk.Discovery.IDiscoveryService.Execute*> method you will use to pass a instance of the <xref:Microsoft.Xrm.Sdk.Discovery.DiscoveryRequest> class.</span></span>
 
<span data-ttu-id="046d8-115">Alternatively, you can add the service references for the URLs described previously to your project.</span><span class="sxs-lookup"><span data-stu-id="046d8-115">Alternatively, you can add the service references for the URLs described previously to your project.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="046d8-116">In This Section</span><span class="sxs-lookup"><span data-stu-id="046d8-116">In This Section</span></span>  
 [<span data-ttu-id="046d8-117">Discovery Service Methods</span><span class="sxs-lookup"><span data-stu-id="046d8-117">Discovery Service Methods</span></span>](discovery-service-methods.md)<br />
 [<span data-ttu-id="046d8-118">Discovery Service Messages (Request and Response Classes)</span><span class="sxs-lookup"><span data-stu-id="046d8-118">Discovery Service Messages (Request and Response Classes)</span></span>](discovery-service-messages-request-response-classes.md)<br />
 [<span data-ttu-id="046d8-119">Messages in the Discovery Service</span><span class="sxs-lookup"><span data-stu-id="046d8-119">Messages in the Discovery Service</span></span>](messages-discovery-service.md)<br />
 [<span data-ttu-id="046d8-120">Sample: Accessing the DiscoveryService</span><span class="sxs-lookup"><span data-stu-id="046d8-120">Sample: Accessing the DiscoveryService</span></span>](sample-access-discovery-service.md)<br />
  
## <a name="related-sections"></a><span data-ttu-id="046d8-121">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="046d8-121">Related Sections</span></span>  
 [<span data-ttu-id="046d8-122">Write Applications and Server Extensions</span><span class="sxs-lookup"><span data-stu-id="046d8-122">Write Applications and Server Extensions</span></span>](../extend-dynamics-365-server.md)<br />
 [<span data-ttu-id="046d8-123">Use Dynamics 365 for Customer Engagement apps Services</span><span class="sxs-lookup"><span data-stu-id="046d8-123">Use Dynamics 365 for Customer Engagement apps Services</span></span>](use-services-in-code.md)<br />
 [<span data-ttu-id="046d8-124">Download endpoints using Developer resources page</span><span class="sxs-lookup"><span data-stu-id="046d8-124">Download endpoints using Developer resources page</span></span>](../developer-resources-page.md)<br />
 [<span data-ttu-id="046d8-125">Access the Web Services in Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="046d8-125">Access the Web Services in Dynamics 365 for Customer Engagement</span></span>](../authenticate-users.md)<br />
 [<span data-ttu-id="046d8-126">Quick Start: A Simple Program</span><span class="sxs-lookup"><span data-stu-id="046d8-126">Quick Start: A Simple Program</span></span>](../simple-program-web-services.md)<br />
