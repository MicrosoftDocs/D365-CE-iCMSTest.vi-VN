---
title: Use the Dynamics 365 for Customer Engagement Discovery services (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: In a multi-tenant environment like Dynamics 365 for Customer Engagement, the Discovery web service helps determine which organizations a user is a member of.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 0b95ebbd-49f5-4e09-8f18-7708dbef65d0
caps.latest.revision: 9
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7f4afd98a2bf1315362c2487b08ed2b55dc2a4d8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387197"
---
# <a name="use-the-dynamics-365-for-customer-engagement-discovery-services"></a><span data-ttu-id="37e8b-103">Use the Dynamics 365 for Customer Engagement Discovery services</span><span class="sxs-lookup"><span data-stu-id="37e8b-103">Use the Dynamics 365 for Customer Engagement Discovery services</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="37e8b-104">The Discovery web services are used to determine the organizations that a user is a member of, and the endpoint address URL to access the Organization service or Web API for each of those organizations.</span><span class="sxs-lookup"><span data-stu-id="37e8b-104">The Discovery web services are used to determine the organizations that a user is a member of, and the endpoint address URL to access the Organization service or Web API for each of those organizations.</span></span> <span data-ttu-id="37e8b-105">This Discovery service is necessary because [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] is a multi-tenant environment.</span><span class="sxs-lookup"><span data-stu-id="37e8b-105">This Discovery service is necessary because [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] is a multi-tenant environment.</span></span> <span data-ttu-id="37e8b-106">A single [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server can host multiple business organizations.</span><span class="sxs-lookup"><span data-stu-id="37e8b-106">A single [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server can host multiple business organizations.</span></span> <span data-ttu-id="37e8b-107">By using the Discovery web service, your application can determine the endpoint address URL to access the target organization’s business data.</span><span class="sxs-lookup"><span data-stu-id="37e8b-107">By using the Discovery web service, your application can determine the endpoint address URL to access the target organization’s business data.</span></span>  
  
<span data-ttu-id="37e8b-108">A Discovery service is accessed through either the Web API or the Organization Service.</span><span class="sxs-lookup"><span data-stu-id="37e8b-108">A Discovery service is accessed through either the Web API or the Organization Service.</span></span>  

- <span data-ttu-id="37e8b-109">For the Web API see: [Discover the URL for your organization using the Web API](webapi/discover-url-organization-web-api.md)</span><span class="sxs-lookup"><span data-stu-id="37e8b-109">For the Web API see: [Discover the URL for your organization using the Web API](webapi/discover-url-organization-web-api.md)</span></span> 
- <span data-ttu-id="37e8b-110">For the Organization Service see: [Discover the URL for your organization using the Organization Service API](org-service/discover-url-organization-organization-service.md)</span><span class="sxs-lookup"><span data-stu-id="37e8b-110">For the Organization Service see: [Discover the URL for your organization using the Organization Service API](org-service/discover-url-organization-organization-service.md)</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="37e8b-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="37e8b-111">See also</span></span>  
 [<span data-ttu-id="37e8b-112">Use Dynamics 365 for Customer Engagement web services</span><span class="sxs-lookup"><span data-stu-id="37e8b-112">Use Dynamics 365 for Customer Engagement web services</span></span>](use-microsoft-dynamics-365-web-services.md)<br />
 [<span data-ttu-id="37e8b-113">Use Dynamics 365 for Customer Engagement Web API</span><span class="sxs-lookup"><span data-stu-id="37e8b-113">Use Dynamics 365 for Customer Engagement Web API</span></span>](webapi/index.md)<br />
 [<span data-ttu-id="37e8b-114">Use Dynamics 365 for Customer Engagement Organization Service</span><span class="sxs-lookup"><span data-stu-id="37e8b-114">Use Dynamics 365 for Customer Engagement Organization Service</span></span>](org-service/index.md)<br />
