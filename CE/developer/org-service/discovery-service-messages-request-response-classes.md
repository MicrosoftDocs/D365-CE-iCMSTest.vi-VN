---
title: Discovery service messages (request and response classes) (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: ''
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
- IDiscoveryService web service, request and response classes
- 'IDiscoveryService web service, base classes: DiscoveryRequest and DiscoveryResponse'
- request and response classes, discovery service messages
- discovery service messages (request and response classes)
ms.assetid: 053f259e-40c9-46ba-8c47-39e29e228590
caps.latest.revision: 8
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9d59b51506911796f1c26bb5773ac61d60213f24
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385707"
---
# <a name="discovery-service-messages-request-and-response-classes"></a><span data-ttu-id="b4acf-102">Discovery service messages (request and response classes)</span><span class="sxs-lookup"><span data-stu-id="b4acf-102">Discovery service messages (request and response classes)</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b4acf-103">The <xref:Microsoft.Xrm.Sdk.Discovery.IDiscoveryService> provides an <xref:Microsoft.Xrm.Sdk.Discovery.IDiscoveryService.Execute*> method to perform supported operations.</span><span class="sxs-lookup"><span data-stu-id="b4acf-103">The <xref:Microsoft.Xrm.Sdk.Discovery.IDiscoveryService> provides an <xref:Microsoft.Xrm.Sdk.Discovery.IDiscoveryService.Execute*> method to perform supported operations.</span></span> <span data-ttu-id="b4acf-104">This method takes a message request class as a parameter and returns a message response class.</span><span class="sxs-lookup"><span data-stu-id="b4acf-104">This method takes a message request class as a parameter and returns a message response class.</span></span> <span data-ttu-id="b4acf-105">Request message class names end with "Request" and response message class names end with "Response”.</span><span class="sxs-lookup"><span data-stu-id="b4acf-105">Request message class names end with "Request" and response message class names end with "Response”.</span></span>  
  
 ![Execute message flow](../media/crm-v5s-executemessage.png)  
  
 <span data-ttu-id="b4acf-107"><xref:Microsoft.Xrm.Sdk.Discovery.DiscoveryRequest> is the base class for all discovery message requests and <xref:Microsoft.Xrm.Sdk.Discovery.DiscoveryResponse> is the base class for all discovery message responses.</span><span class="sxs-lookup"><span data-stu-id="b4acf-107"><xref:Microsoft.Xrm.Sdk.Discovery.DiscoveryRequest> is the base class for all discovery message requests and <xref:Microsoft.Xrm.Sdk.Discovery.DiscoveryResponse> is the base class for all discovery message responses.</span></span> <span data-ttu-id="b4acf-108">Typically, you use one of the derived request and response class pairs in your application, for example: <xref:Microsoft.Xrm.Sdk.Discovery.RetrieveOrganizationRequest> and  <xref:Microsoft.Xrm.Sdk.Discovery.RetrieveOrganizationResponse>.</span><span class="sxs-lookup"><span data-stu-id="b4acf-108">Typically, you use one of the derived request and response class pairs in your application, for example: <xref:Microsoft.Xrm.Sdk.Discovery.RetrieveOrganizationRequest> and  <xref:Microsoft.Xrm.Sdk.Discovery.RetrieveOrganizationResponse>.</span></span>  
  
 <span data-ttu-id="b4acf-109">For a list of the messages supported by the `Execute` method, see [Messages in the Discovery Service](messages-discovery-service.md).</span><span class="sxs-lookup"><span data-stu-id="b4acf-109">For a list of the messages supported by the `Execute` method, see [Messages in the Discovery Service](messages-discovery-service.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b4acf-110">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b4acf-110">See also</span></span>  
 <span data-ttu-id="b4acf-111">[Discover the URL for Your Organization With IDiscoveryService Web Service](discover-url-organization-organization-service.md) </span><span class="sxs-lookup"><span data-stu-id="b4acf-111">[Discover the URL for Your Organization With IDiscoveryService Web Service](discover-url-organization-organization-service.md) </span></span>  
 <span data-ttu-id="b4acf-112">[Messages in the Discovery Service](messages-discovery-service.md) </span><span class="sxs-lookup"><span data-stu-id="b4acf-112">[Messages in the Discovery Service](messages-discovery-service.md) </span></span>  
 [<span data-ttu-id="b4acf-113">Sample: Accessing the Discovery Service</span><span class="sxs-lookup"><span data-stu-id="b4acf-113">Sample: Accessing the Discovery Service</span></span>](sample-access-discovery-service.md)
