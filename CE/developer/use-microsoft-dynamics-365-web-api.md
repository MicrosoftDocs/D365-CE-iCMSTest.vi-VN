---
title: Use the Dynamics 365 for Customer Engagement Web API (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: The Dynamics 365 for Customer Engagement Web API implements OData v4 and provides a development experience that can be used across a wide variety of programming languages, platforms, and devices
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 15c4039e-a3ca-4116-ba1d-3ac88cba3ae1
caps.latest.revision: 15
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d4289518a82a4e3a4316cd1c3252901bea3cf423
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386845"
---
# <a name="use-the-dynamics-365-for-customer-engagement-web-api"></a><span data-ttu-id="2d32a-103">Use the Dynamics 365 for Customer Engagement Web API</span><span class="sxs-lookup"><span data-stu-id="2d32a-103">Use the Dynamics 365 for Customer Engagement Web API</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="2d32a-104">The Customer Engagement Web API provides a development experience that can be used across a wide variety of programming languages, platforms, and devices.</span><span class="sxs-lookup"><span data-stu-id="2d32a-104">The Customer Engagement Web API provides a development experience that can be used across a wide variety of programming languages, platforms, and devices.</span></span> <span data-ttu-id="2d32a-105">The Web API implements the OData (Open Data Protocol), version 4.0, an OASIS standard for building and consuming RESTful APIs over rich data sources.</span><span class="sxs-lookup"><span data-stu-id="2d32a-105">The Web API implements the OData (Open Data Protocol), version 4.0, an OASIS standard for building and consuming RESTful APIs over rich data sources.</span></span> <span data-ttu-id="2d32a-106">You can learn more about this protocol at [http://www.odata.org/](http://www.odata.org/).</span><span class="sxs-lookup"><span data-stu-id="2d32a-106">You can learn more about this protocol at [http://www.odata.org/](http://www.odata.org/).</span></span> <span data-ttu-id="2d32a-107">Details about this standard are available at [https://www.oasis-open.org/standards#odatav4.0](https://www.oasis-open.org/standards#odatav4.0).</span><span class="sxs-lookup"><span data-stu-id="2d32a-107">Details about this standard are available at [https://www.oasis-open.org/standards#odatav4.0](https://www.oasis-open.org/standards#odatav4.0).</span></span>  
  
 <span data-ttu-id="2d32a-108">Because the Web API is built on open standards, we don’t provide assemblies for a specific developer experience.</span><span class="sxs-lookup"><span data-stu-id="2d32a-108">Because the Web API is built on open standards, we don’t provide assemblies for a specific developer experience.</span></span> <span data-ttu-id="2d32a-109">You can compose HTTP requests for specific operations or use third-party libraries to generate classes for whatever language or platform you want.</span><span class="sxs-lookup"><span data-stu-id="2d32a-109">You can compose HTTP requests for specific operations or use third-party libraries to generate classes for whatever language or platform you want.</span></span> <span data-ttu-id="2d32a-110">You can find a list of libraries that support OData version 4.0 at [http://www.odata.org/libraries/](http://www.odata.org/libraries/).</span><span class="sxs-lookup"><span data-stu-id="2d32a-110">You can find a list of libraries that support OData version 4.0 at [http://www.odata.org/libraries/](http://www.odata.org/libraries/).</span></span>  
  
 <span data-ttu-id="2d32a-111">To compare the Web API with other [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement web services, see [Use Dynamics 365 for Customer Engagement web services](use-microsoft-dynamics-365-web-services.md).</span><span class="sxs-lookup"><span data-stu-id="2d32a-111">To compare the Web API with other [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement web services, see [Use Dynamics 365 for Customer Engagement web services](use-microsoft-dynamics-365-web-services.md).</span></span> 

  
### <a name="related-sections"></a><span data-ttu-id="2d32a-112">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="2d32a-112">Related Sections</span></span>  
 [<span data-ttu-id="2d32a-113">Use Dynamics 365 for Customer Engagement web services</span><span class="sxs-lookup"><span data-stu-id="2d32a-113">Use Dynamics 365 for Customer Engagement web services</span></span>](use-microsoft-dynamics-365-web-services.md)  
  
 [<span data-ttu-id="2d32a-114">OData - the best way to REST</span><span class="sxs-lookup"><span data-stu-id="2d32a-114">OData - the best way to REST</span></span>](http://www.odata.org/)  
  
 [<span data-ttu-id="2d32a-115">OData Version 4.0 Part 1: Protocol Plus Errata 02</span><span class="sxs-lookup"><span data-stu-id="2d32a-115">OData Version 4.0 Part 1: Protocol Plus Errata 02</span></span>](http://docs.oasis-open.org/odata/odata/v4.0/odata-v4.0-part1-protocol.html)  
  
 [<span data-ttu-id="2d32a-116">OData Version 4.0 Part 2: URL Conventions Plus Errata 02</span><span class="sxs-lookup"><span data-stu-id="2d32a-116">OData Version 4.0 Part 2: URL Conventions Plus Errata 02</span></span>](http://docs.oasis-open.org/odata/odata/v4.0/odata-v4.0-part2-url-conventions.html)  
  
 [<span data-ttu-id="2d32a-117">OData Version 4.0 Part 3: Common Schema Definition Language (CSDL) Plus Errata 02</span><span class="sxs-lookup"><span data-stu-id="2d32a-117">OData Version 4.0 Part 3: Common Schema Definition Language (CSDL) Plus Errata 02</span></span>](http://docs.oasis-open.org/odata/odata/v4.0/odata-v4.0-part3-csdl.html)
