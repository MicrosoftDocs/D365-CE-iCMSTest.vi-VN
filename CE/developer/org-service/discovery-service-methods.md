---
title: Discovery Service methods (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: The IDiscoveryService Web service provides a single method which can be used to determine the correct organization and URL to use to interact with the Dynamics 365 for Customer Engagement Server
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 8ad9ac57-55f6-4951-9266-672b60ef4aed
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c7ac6e474a9d5a9bac2b643b746cd6e6a7164091
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385479"
---
# <a name="discovery-service-methods"></a><span data-ttu-id="9811c-103">Discovery Service methods</span><span class="sxs-lookup"><span data-stu-id="9811c-103">Discovery Service methods</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="9811c-104">The <xref:Microsoft.Xrm.Sdk.Discovery.IDiscoveryService> Web service provides a single method you can use to determine the correct organization and URL to use to interact with the [!INCLUDE[pn_microsoftcrm_server](../../includes/pn-microsoftcrm-server.md)].</span><span class="sxs-lookup"><span data-stu-id="9811c-104">The <xref:Microsoft.Xrm.Sdk.Discovery.IDiscoveryService> Web service provides a single method you can use to determine the correct organization and URL to use to interact with the [!INCLUDE[pn_microsoftcrm_server](../../includes/pn-microsoftcrm-server.md)].</span></span>  
  
 <span data-ttu-id="9811c-105">To access the `IDiscoveryService` Web service, you add a reference to Microsoft.Xrm.Sdk.dll assembly to your [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] project, and then add a `using` or `imports` statement for the Microsoft.Xrm.Sdk.Discovery namespace.</span><span class="sxs-lookup"><span data-stu-id="9811c-105">To access the `IDiscoveryService` Web service, you add a reference to Microsoft.Xrm.Sdk.dll assembly to your [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] project, and then add a `using` or `imports` statement for the Microsoft.Xrm.Sdk.Discovery namespace.</span></span>  
  
## <a name="execute"></a><span data-ttu-id="9811c-106">Thực thi</span><span class="sxs-lookup"><span data-stu-id="9811c-106">Execute</span></span>  
 <span data-ttu-id="9811c-107">Use the <xref:Microsoft.Xrm.Sdk.Discovery.IDiscoveryService.Execute(Microsoft.Xrm.Sdk.Discovery.DiscoveryRequest)> method to execute a discovery service message.</span><span class="sxs-lookup"><span data-stu-id="9811c-107">Use the <xref:Microsoft.Xrm.Sdk.Discovery.IDiscoveryService.Execute(Microsoft.Xrm.Sdk.Discovery.DiscoveryRequest)> method to execute a discovery service message.</span></span> <span data-ttu-id="9811c-108">For a list of the messages you can use with this method, see [Microsoft.Xrm.Sdk.Discovery Messages](messages-discovery-service.md).</span><span class="sxs-lookup"><span data-stu-id="9811c-108">For a list of the messages you can use with this method, see [Microsoft.Xrm.Sdk.Discovery Messages](messages-discovery-service.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="9811c-109">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="9811c-109">See also</span></span>  
 <span data-ttu-id="9811c-110">[Discover the URL for Your Organization With IDiscoveryService Web Service](discover-url-organization-organization-service.md) </span><span class="sxs-lookup"><span data-stu-id="9811c-110">[Discover the URL for Your Organization With IDiscoveryService Web Service](discover-url-organization-organization-service.md) </span></span>  
 <span data-ttu-id="9811c-111">[Discovery Service Messages (Request and Response Classes)](discovery-service-messages-request-response-classes.md) </span><span class="sxs-lookup"><span data-stu-id="9811c-111">[Discovery Service Messages (Request and Response Classes)](discovery-service-messages-request-response-classes.md) </span></span>  
 <span data-ttu-id="9811c-112">[Access the Web Services in Dynamics 365 for Customer Engagement](../authenticate-users.md) [Messages in the discovery service](messages-discovery-service.md)</span><span class="sxs-lookup"><span data-stu-id="9811c-112">[Access the Web Services in Dynamics 365 for Customer Engagement](../authenticate-users.md) [Messages in the discovery service](messages-discovery-service.md)</span></span>
