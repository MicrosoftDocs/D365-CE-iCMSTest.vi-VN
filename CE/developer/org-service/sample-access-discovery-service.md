---
title: 'Sample: Access the Discovery service (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: The sample demonstrates how to obtain organization information, including the organization’s URL, from the DiscoveryService Web service.
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 34249eb1-378e-4dd2-9c02-f14bcd470b64
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 09dc7e5678a398cf0c476d2c3b44bf15a2a235ad
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388437"
---
# <a name="sample-access-the-discovery-service"></a><span data-ttu-id="01d56-103">Sample: Access the Discovery service</span><span class="sxs-lookup"><span data-stu-id="01d56-103">Sample: Access the Discovery service</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="01d56-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="01d56-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="01d56-105">Download the complete: [Access the discovery service](https://code.msdn.microsoft.com/Sample-Access-the-6dea28f1).</span><span class="sxs-lookup"><span data-stu-id="01d56-105">Download the complete: [Access the discovery service](https://code.msdn.microsoft.com/Sample-Access-the-6dea28f1).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="01d56-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="01d56-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="01d56-107">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="01d56-107">Demonstrates</span></span>  
 <span data-ttu-id="01d56-108">How to obtain organization information, including the organization’s URL, from the DiscoveryService Web service.</span><span class="sxs-lookup"><span data-stu-id="01d56-108">How to obtain organization information, including the organization’s URL, from the DiscoveryService Web service.</span></span>  
  
## <a name="example"></a><span data-ttu-id="01d56-109">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="01d56-109">Example</span></span>  
 [!code-csharp[DiscoveryService#DiscoveryService](../../snippets/csharp/CRMV8/discoveryservice/cs/discoveryservice.cs#discoveryservice)]  
  
### <a name="see-also"></a><span data-ttu-id="01d56-110">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="01d56-110">See also</span></span>  
 <span data-ttu-id="01d56-111">[Use IDiscoveryService to Discover the URL for Your Organization](discover-url-organization-organization-service.md) </span><span class="sxs-lookup"><span data-stu-id="01d56-111">[Use IDiscoveryService to Discover the URL for Your Organization](discover-url-organization-organization-service.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Client.DiscoveryServiceProxy>   
 <xref:Microsoft.Xrm.Sdk.Discovery.RetrieveOrganizationsRequest>   
 <xref:Microsoft.Xrm.Sdk.Discovery.OrganizationDetail>
