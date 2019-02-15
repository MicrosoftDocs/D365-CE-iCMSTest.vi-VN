---
title: Messages in the discovery service (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: This article discusses the messages that are used with the discovery service DiscoveryRequest) method. Some supported messages are RetrieveUserIdByExternalIdRequest, RetrieveOrganizationRequest and RetrieveOrganizationsRequest.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- discovery service web service, messages in
- messages in the discovery service, about
- discovery service web service, supported messages for the Execute method
- discovery service web service, deployment types
ms.assetid: d6ecf6b2-6d20-4d7f-8577-ef5d42637a1a
caps.latest.revision: 32
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9c078fea58f00aba1a93862ebd490642601e5d0c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385870"
---
# <a name="messages-in-the-discovery-service"></a><span data-ttu-id="283b7-104">Messages in the discovery service</span><span class="sxs-lookup"><span data-stu-id="283b7-104">Messages in the discovery service</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="283b7-105">Messages are used with the discovery service <xref:Microsoft.Xrm.Sdk.Discovery.IDiscoveryService.Execute(Microsoft.Xrm.Sdk.Discovery.DiscoveryRequest)> method.</span><span class="sxs-lookup"><span data-stu-id="283b7-105">Messages are used with the discovery service <xref:Microsoft.Xrm.Sdk.Discovery.IDiscoveryService.Execute(Microsoft.Xrm.Sdk.Discovery.DiscoveryRequest)> method.</span></span> <span data-ttu-id="283b7-106">All messages available in the discovery web service for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps apply to all deployment types.</span><span class="sxs-lookup"><span data-stu-id="283b7-106">All messages available in the discovery web service for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps apply to all deployment types.</span></span>  

 <span data-ttu-id="283b7-107">The following table lists the messages that are supported with <xref:Microsoft.Xrm.Sdk.Discovery.IDiscoveryService.Execute(Microsoft.Xrm.Sdk.Discovery.DiscoveryRequest)> method.</span><span class="sxs-lookup"><span data-stu-id="283b7-107">The following table lists the messages that are supported with <xref:Microsoft.Xrm.Sdk.Discovery.IDiscoveryService.Execute(Microsoft.Xrm.Sdk.Discovery.DiscoveryRequest)> method.</span></span> <span data-ttu-id="283b7-108">Each message derives from the abstract base class <xref:Microsoft.Xrm.Sdk.Discovery.DiscoveryRequest>.</span><span class="sxs-lookup"><span data-stu-id="283b7-108">Each message derives from the abstract base class <xref:Microsoft.Xrm.Sdk.Discovery.DiscoveryRequest>.</span></span>  


|                               <span data-ttu-id="283b7-109">Thông báo</span><span class="sxs-lookup"><span data-stu-id="283b7-109">Message</span></span>                                |                                                                                          <span data-ttu-id="283b7-110">Mô tả</span><span class="sxs-lookup"><span data-stu-id="283b7-110">Description</span></span>                                                                                           |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <xref:Microsoft.Xrm.Sdk.Discovery.RetrieveUserIdByExternalIdRequest> | <span data-ttu-id="283b7-111">Retrieves the logged-on user's ID in [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="283b7-111">Retrieves the logged-on user's ID in [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps.</span></span> <span data-ttu-id="283b7-112">This message is available in [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps only.</span><span class="sxs-lookup"><span data-stu-id="283b7-112">This message is available in [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps only.</span></span> |
|    <xref:Microsoft.Xrm.Sdk.Discovery.RetrieveOrganizationRequest>    |                                                                       <span data-ttu-id="283b7-113">Retrieves information about a single organization.</span><span class="sxs-lookup"><span data-stu-id="283b7-113">Retrieves information about a single organization.</span></span>                                                                       |
|   <xref:Microsoft.Xrm.Sdk.Discovery.RetrieveOrganizationsRequest>    |                                                            <span data-ttu-id="283b7-114">Retrieves information about all organizations to which the user belongs.</span><span class="sxs-lookup"><span data-stu-id="283b7-114">Retrieves information about all organizations to which the user belongs.</span></span>                                                            |

### <a name="see-also"></a><span data-ttu-id="283b7-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="283b7-115">See also</span></span>  
 <span data-ttu-id="283b7-116">[Discover the URL for Your Organization With IDiscoveryService Web Service](discover-url-organization-organization-service.md) </span><span class="sxs-lookup"><span data-stu-id="283b7-116">[Discover the URL for Your Organization With IDiscoveryService Web Service](discover-url-organization-organization-service.md) </span></span>  
 <span data-ttu-id="283b7-117">[Sample: Access the Discovery Service](sample-access-discovery-service.md) </span><span class="sxs-lookup"><span data-stu-id="283b7-117">[Sample: Access the Discovery Service](sample-access-discovery-service.md) </span></span>  
 [<span data-ttu-id="283b7-118">Use Messages (Request and Response Classes)</span><span class="sxs-lookup"><span data-stu-id="283b7-118">Use Messages (Request and Response Classes)</span></span>](discovery-service-messages-request-response-classes.md)
