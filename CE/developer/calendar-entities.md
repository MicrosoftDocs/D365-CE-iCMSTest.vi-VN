---
title: Calendar entities (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
ms.custom: ''
ms.date: 10/10/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: aee14c98-38c7-4c47-850d-74ccc630735b
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d654bc1f6b852e7ebc46a3710f9af9f3b6eb97b9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386911"
---
# <a name="calendar-entities"></a><span data-ttu-id="312c1-102">Calendar entities</span><span class="sxs-lookup"><span data-stu-id="312c1-102">Calendar entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="312c1-103">The calendar entity stores data for customer service calendars and holiday schedules in addition to business.</span><span class="sxs-lookup"><span data-stu-id="312c1-103">The calendar entity stores data for customer service calendars and holiday schedules in addition to business.</span></span> <span data-ttu-id="312c1-104">Each calendar is set for a specific time zone.</span><span class="sxs-lookup"><span data-stu-id="312c1-104">Each calendar is set for a specific time zone.</span></span>  
  
 <span data-ttu-id="312c1-105">A calendar describes the availability of a service or a resource.</span><span class="sxs-lookup"><span data-stu-id="312c1-105">A calendar describes the availability of a service or a resource.</span></span> <span data-ttu-id="312c1-106">Calendars are related to `calendarrule` records, which include details about the duration, start and end times, and recurring patterns of events included in the calendar.</span><span class="sxs-lookup"><span data-stu-id="312c1-106">Calendars are related to `calendarrule` records, which include details about the duration, start and end times, and recurring patterns of events included in the calendar.</span></span>  
  
 <span data-ttu-id="312c1-107">There are two types of calendar rules in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)]:</span><span class="sxs-lookup"><span data-stu-id="312c1-107">There are two types of calendar rules in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)]:</span></span>  
  
- <span data-ttu-id="312c1-108">**Root**: A calendar rule that contains an inner calendar or that has nested (leaf) rules.</span><span class="sxs-lookup"><span data-stu-id="312c1-108">**Root**: A calendar rule that contains an inner calendar or that has nested (leaf) rules.</span></span> <span data-ttu-id="312c1-109">You can specify an inner calendar for a root calendar rule by using the `CalendarRule.InnerCalendarId` attribute.</span><span class="sxs-lookup"><span data-stu-id="312c1-109">You can specify an inner calendar for a root calendar rule by using the `CalendarRule.InnerCalendarId` attribute.</span></span> <span data-ttu-id="312c1-110">The attribute value of `CalendarRule.InnerCalendarId` of a root rule is the same as the attribute value of `CalendarRule.CalendarId` of its leaf rules.</span><span class="sxs-lookup"><span data-stu-id="312c1-110">The attribute value of `CalendarRule.InnerCalendarId` of a root rule is the same as the attribute value of `CalendarRule.CalendarId` of its leaf rules.</span></span>  
  
- <span data-ttu-id="312c1-111">**Leaf**: A calendar rule that doesn’t contain an inner calendar, and therefore, is the end of the "branch."</span><span class="sxs-lookup"><span data-stu-id="312c1-111">**Leaf**: A calendar rule that doesn’t contain an inner calendar, and therefore, is the end of the "branch."</span></span>  
  
  <span data-ttu-id="312c1-112">Calendar rules are ordered, or ranked, to describe their precedence, and rules can overlap.</span><span class="sxs-lookup"><span data-stu-id="312c1-112">Calendar rules are ordered, or ranked, to describe their precedence, and rules can overlap.</span></span> <span data-ttu-id="312c1-113">The nested rules expansion defines the time span, or extent, of a rule.</span><span class="sxs-lookup"><span data-stu-id="312c1-113">The nested rules expansion defines the time span, or extent, of a rule.</span></span> <span data-ttu-id="312c1-114">You can use the `CalendarRule.ExtentCode` attribute to define how rule expansion overlap is handled, for example, whether both time span or extent of a rule are shown or if only one is included.</span><span class="sxs-lookup"><span data-stu-id="312c1-114">You can use the `CalendarRule.ExtentCode` attribute to define how rule expansion overlap is handled, for example, whether both time span or extent of a rule are shown or if only one is included.</span></span> <span data-ttu-id="312c1-115">These features provide for recurrence patterns, for example, different shift schedules for winter and summer months in a single service calendar.</span><span class="sxs-lookup"><span data-stu-id="312c1-115">These features provide for recurrence patterns, for example, different shift schedules for winter and summer months in a single service calendar.</span></span>  
  
  <span data-ttu-id="312c1-116">A calendar can be a complex tree of rules and nested calendars that represent a high-level abstraction of the work schedule.</span><span class="sxs-lookup"><span data-stu-id="312c1-116">A calendar can be a complex tree of rules and nested calendars that represent a high-level abstraction of the work schedule.</span></span> <span data-ttu-id="312c1-117">The calendar entity supports the <xref:Microsoft.Crm.Sdk.Messages.ExpandCalendarRequest> message to convert to a simple view, which is an array of time blocks that determine availability over specific ranges.</span><span class="sxs-lookup"><span data-stu-id="312c1-117">The calendar entity supports the <xref:Microsoft.Crm.Sdk.Messages.ExpandCalendarRequest> message to convert to a simple view, which is an array of time blocks that determine availability over specific ranges.</span></span>  

> [!NOTE]
> <span data-ttu-id="312c1-118">It is not possible to perform GET, POST, PATCH and DELETE operations with `calendarrule` entity.</span><span class="sxs-lookup"><span data-stu-id="312c1-118">It is not possible to perform GET, POST, PATCH and DELETE operations with `calendarrule` entity.</span></span> <span data-ttu-id="312c1-119">Thông tin khác: <xref href="Microsoft.Dynamics.CRM.calendarrule?text=CalendarRule EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="312c1-119">More information: <xref href="Microsoft.Dynamics.CRM.calendarrule?text=CalendarRule EntityType" />.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="312c1-120">In This Section</span><span class="sxs-lookup"><span data-stu-id="312c1-120">In This Section</span></span>  
 [<span data-ttu-id="312c1-121">Types of Calendars</span><span class="sxs-lookup"><span data-stu-id="312c1-121">Types of Calendars</span></span>](types-calendars.md)  
  
 [<span data-ttu-id="312c1-122">Calendar Entity</span><span class="sxs-lookup"><span data-stu-id="312c1-122">Calendar Entity</span></span>](entities/calendar.md)  
  
## <a name="related-sections"></a><span data-ttu-id="312c1-123">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="312c1-123">Related Sections</span></span>  
 [<span data-ttu-id="312c1-124">Appointment Entities</span><span class="sxs-lookup"><span data-stu-id="312c1-124">Appointment Entities</span></span>](appointment-entities.md)  
  
 [<span data-ttu-id="312c1-125">Recurring Appointment Entities</span><span class="sxs-lookup"><span data-stu-id="312c1-125">Recurring Appointment Entities</span></span>](recurring-appointment-entities.md)  
  
 [<span data-ttu-id="312c1-126">Resource Entities</span><span class="sxs-lookup"><span data-stu-id="312c1-126">Resource Entities</span></span>](resource-entities.md)  
  
 [<span data-ttu-id="312c1-127">Service Entity</span><span class="sxs-lookup"><span data-stu-id="312c1-127">Service Entity</span></span>](service-entity.md)  
  
 [<span data-ttu-id="312c1-128">Sample Code for Schedule and Appointment Entities</span><span class="sxs-lookup"><span data-stu-id="312c1-128">Sample Code for Schedule and Appointment Entities</span></span>](sample-code-schedule-appointment-entities.md)
