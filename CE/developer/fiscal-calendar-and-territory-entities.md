---
title: Fiscal calendar and territory entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: 'Learn about fiscal calendar and territory entities. Depending on the fiscal year settings that are defined by the Organization entity, you can use one of the following fiscal calendar entities to set the sales quotas: AnnualFiscalCalendar, FixedMonthlyFiscalCalendar, MonthlyFiscalCalendar, QuarterlyFiscalCalendar, and SemiAnnualFiscalCalendar.'
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
- quotas, definition
- salepersons, definition
- setting sales quotas, goal management entities
- goal management entities, using for setting sales quotas
- goal management entities, more versatile than the fiscal calendar entities
- fiscal calendar; fiscal year; and fiscal periods entities, definition
- territory entity, definition
ms.assetid: 1a695f80-f042-4a56-a698-72fd1055f01e
caps.latest.revision: 22
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7acb022f6380c1663ba9c14f0d01cd1fea5ef124
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385832"
---
# <a name="fiscal-calendar-and-territory-entities"></a><span data-ttu-id="f2d5f-104">Fiscal calendar and territory entities</span><span class="sxs-lookup"><span data-stu-id="f2d5f-104">Fiscal calendar and territory entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="f2d5f-105">You can use the *fiscal calendar* entities and the *territory* entity to track sales information for a salesperson.</span><span class="sxs-lookup"><span data-stu-id="f2d5f-105">You can use the *fiscal calendar* entities and the *territory* entity to track sales information for a salesperson.</span></span> <span data-ttu-id="f2d5f-106">A salesperson is a user in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] who has to meet sales objectives, such as sales quotas.</span><span class="sxs-lookup"><span data-stu-id="f2d5f-106">A salesperson is a user in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] who has to meet sales objectives, such as sales quotas.</span></span> <span data-ttu-id="f2d5f-107">A territory is a geographical area that is assigned to a salesperson.</span><span class="sxs-lookup"><span data-stu-id="f2d5f-107">A territory is a geographical area that is assigned to a salesperson.</span></span> <span data-ttu-id="f2d5f-108">The fiscal calendar entities define sales quotas for a salesperson.</span><span class="sxs-lookup"><span data-stu-id="f2d5f-108">The fiscal calendar entities define sales quotas for a salesperson.</span></span> <span data-ttu-id="f2d5f-109">A quota is a revenue objective for a salesperson.</span><span class="sxs-lookup"><span data-stu-id="f2d5f-109">A quota is a revenue objective for a salesperson.</span></span> <span data-ttu-id="f2d5f-110">A quota is defined as a specific currency amount for a particular fiscal period.</span><span class="sxs-lookup"><span data-stu-id="f2d5f-110">A quota is defined as a specific currency amount for a particular fiscal period.</span></span> <span data-ttu-id="f2d5f-111">A fiscal calendar is a span of time during which the financial activities of an organization are calculated.</span><span class="sxs-lookup"><span data-stu-id="f2d5f-111">A fiscal calendar is a span of time during which the financial activities of an organization are calculated.</span></span> <span data-ttu-id="f2d5f-112">A fiscal year is divided into fiscal periods, typically defined as semesters, quarters, or months.</span><span class="sxs-lookup"><span data-stu-id="f2d5f-112">A fiscal year is divided into fiscal periods, typically defined as semesters, quarters, or months.</span></span> <span data-ttu-id="f2d5f-113">Depending on the fiscal year settings that are defined by the `Organization` entity, you can use one of the following fiscal calendar entities to set the sales quotas:  `AnnualFiscalCalendar`, `FixedMonthlyFiscalCalendar`,  `MonthlyFiscalCalendar`,  `QuarterlyFiscalCalendar`, and `SemiAnnualFiscalCalendar`.</span><span class="sxs-lookup"><span data-stu-id="f2d5f-113">Depending on the fiscal year settings that are defined by the `Organization` entity, you can use one of the following fiscal calendar entities to set the sales quotas:  `AnnualFiscalCalendar`, `FixedMonthlyFiscalCalendar`,  `MonthlyFiscalCalendar`,  `QuarterlyFiscalCalendar`, and `SemiAnnualFiscalCalendar`.</span></span> <span data-ttu-id="f2d5f-114">Each of these entities has one or more money type attributes that you can use to specify a quota for a particular time period.</span><span class="sxs-lookup"><span data-stu-id="f2d5f-114">Each of these entities has one or more money type attributes that you can use to specify a quota for a particular time period.</span></span> <span data-ttu-id="f2d5f-115">For example, to set a quota for a full fiscal year period, use the `AnnualFiscalCalendar.Period1` attribute.</span><span class="sxs-lookup"><span data-stu-id="f2d5f-115">For example, to set a quota for a full fiscal year period, use the `AnnualFiscalCalendar.Period1` attribute.</span></span> <span data-ttu-id="f2d5f-116">To set monthly quotas, use the `MonthlyFiscalCalendar` entity that contains twelve periods.</span><span class="sxs-lookup"><span data-stu-id="f2d5f-116">To set monthly quotas, use the `MonthlyFiscalCalendar` entity that contains twelve periods.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="f2d5f-117">The create action (<xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span><span class="sxs-lookup"><span data-stu-id="f2d5f-117">The create action (<xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span></span> <span data-ttu-id="f2d5f-118">method and <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message) for fiscal calendar entities is deprecated in [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="f2d5f-118">method and <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message) for fiscal calendar entities is deprecated in [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="f2d5f-119">We encourage you to use new *goal management* entities for setting sales quotas.</span><span class="sxs-lookup"><span data-stu-id="f2d5f-119">We encourage you to use new *goal management* entities for setting sales quotas.</span></span> <span data-ttu-id="f2d5f-120">The goal management entities are much more versatile and offer many more capabilities than the fiscal calendar entities.</span><span class="sxs-lookup"><span data-stu-id="f2d5f-120">The goal management entities are much more versatile and offer many more capabilities than the fiscal calendar entities.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f2d5f-121">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="f2d5f-121">See also</span></span>  
 <span data-ttu-id="f2d5f-122">[Business Management Entities](business-management-entities.md) </span><span class="sxs-lookup"><span data-stu-id="f2d5f-122">[Business Management Entities](business-management-entities.md) </span></span>  
 <span data-ttu-id="f2d5f-123">[Territory Entity](entities/territory.md) </span><span class="sxs-lookup"><span data-stu-id="f2d5f-123">[Territory Entity](entities/territory.md) </span></span>  
 <span data-ttu-id="f2d5f-124">[AnnualFiscalCalendar Entity](entities/annualfiscalcalendar.md) </span><span class="sxs-lookup"><span data-stu-id="f2d5f-124">[AnnualFiscalCalendar Entity](entities/annualfiscalcalendar.md) </span></span>  
 <span data-ttu-id="f2d5f-125">[FixedMonthlyFiscalCalendar Entity](entities/fixedmonthlyfiscalcalendar.md) </span><span class="sxs-lookup"><span data-stu-id="f2d5f-125">[FixedMonthlyFiscalCalendar Entity](entities/fixedmonthlyfiscalcalendar.md) </span></span>  
 <span data-ttu-id="f2d5f-126">[MonthlyFiscalCalendar Entity](entities/monthlyfiscalcalendar.md) </span><span class="sxs-lookup"><span data-stu-id="f2d5f-126">[MonthlyFiscalCalendar Entity](entities/monthlyfiscalcalendar.md) </span></span>  
 <span data-ttu-id="f2d5f-127">[QuarterlyFiscalCalendar Entity](entities/quarterlyfiscalcalendar.md) </span><span class="sxs-lookup"><span data-stu-id="f2d5f-127">[QuarterlyFiscalCalendar Entity](entities/quarterlyfiscalcalendar.md) </span></span>  
 <span data-ttu-id="f2d5f-128">[SemiAnnualFiscalCalendar Entity](entities/semiannualfiscalcalendar.md) </span><span class="sxs-lookup"><span data-stu-id="f2d5f-128">[SemiAnnualFiscalCalendar Entity](entities/semiannualfiscalcalendar.md) </span></span>  
 <span data-ttu-id="f2d5f-129">[Goal Management Entities](goal-management-entities.md) </span><span class="sxs-lookup"><span data-stu-id="f2d5f-129">[Goal Management Entities](goal-management-entities.md) </span></span>  
 <span data-ttu-id="f2d5f-130">[Organization Entities](organization-entities.md) </span><span class="sxs-lookup"><span data-stu-id="f2d5f-130">[Organization Entities](organization-entities.md) </span></span>  
 [<span data-ttu-id="f2d5f-131">Queue Entities</span><span class="sxs-lookup"><span data-stu-id="f2d5f-131">Queue Entities</span></span>](queue-entities.md)
