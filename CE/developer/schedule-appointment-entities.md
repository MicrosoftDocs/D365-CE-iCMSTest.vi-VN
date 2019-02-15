---
title: Schedule and appointment entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Overview of appointment-based service scheduling, including defining services, resources and work schedules, and service locations.
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
- schedule and appointment entities, scheduling engines
- optimizing scheduling, see 'schedule and appointment entities'
- schedule and appointment entities, introduction
- appointment entities, see 'schedule and appointment entities'
- managing appointment-based services, see 'schedule and appointment entities'
- schedule and appointment entities, managing appointment-based services
- scheduling engines, see 'schedule and appointment entities'
- schedule and appointment entities, message classes for appointments
- schedule and appointment entities, optimizing scheduling
ms.assetid: 676e9f3f-e5a0-4251-aaea-27f396da8bf1
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9e751ade5384b9a9a590b7c558855d1a0ca33565
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386178"
---
# <a name="schedule-and-appointment-entities"></a><span data-ttu-id="49a60-103">Schedule and appointment entities</span><span class="sxs-lookup"><span data-stu-id="49a60-103">Schedule and appointment entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] <span data-ttu-id="49a60-104">provides capabilities to address appointment-based service scheduling.</span><span class="sxs-lookup"><span data-stu-id="49a60-104">provides capabilities to address appointment-based service scheduling.</span></span> <span data-ttu-id="49a60-105">You can define services, resources and work schedules, and service locations.</span><span class="sxs-lookup"><span data-stu-id="49a60-105">You can define services, resources and work schedules, and service locations.</span></span> <span data-ttu-id="49a60-106">A scheduling engine manages booked appointments and service availability, and can be tuned to optimize scheduling to reduce costs and required resources.</span><span class="sxs-lookup"><span data-stu-id="49a60-106">A scheduling engine manages booked appointments and service availability, and can be tuned to optimize scheduling to reduce costs and required resources.</span></span>  
  
 <span data-ttu-id="49a60-107">The entity model for the scheduling engine includes a core set of entities: `Service`, `Resource`, `Calendar` and `Site`.</span><span class="sxs-lookup"><span data-stu-id="49a60-107">The entity model for the scheduling engine includes a core set of entities: `Service`, `Resource`, `Calendar` and `Site`.</span></span> <span data-ttu-id="49a60-108">Other entities describe resource requirements, constraints, calendar rules, and a schedule.</span><span class="sxs-lookup"><span data-stu-id="49a60-108">Other entities describe resource requirements, constraints, calendar rules, and a schedule.</span></span>  
  
 <span data-ttu-id="49a60-109">The following messages can be used for scheduling appointments, recurring appointments, and service appointments (service activity).</span><span class="sxs-lookup"><span data-stu-id="49a60-109">The following messages can be used for scheduling appointments, recurring appointments, and service appointments (service activity).</span></span>  
  
|<span data-ttu-id="49a60-110">Thông báo</span><span class="sxs-lookup"><span data-stu-id="49a60-110">Message</span></span>|<span data-ttu-id="49a60-111">Web API Operation</span><span class="sxs-lookup"><span data-stu-id="49a60-111">Web API Operation</span></span>|<span data-ttu-id="49a60-112">SDK Assembly</span><span class="sxs-lookup"><span data-stu-id="49a60-112">SDK Assembly</span></span>|  
|-------------|-----------------|-----------------|  
|<span data-ttu-id="49a60-113">Creates an appointment, recurring appointment, or service appointment (service activity), and calls the scheduling engine to make sure that it is valid for all constraints without any scheduling conflicts.</span><span class="sxs-lookup"><span data-stu-id="49a60-113">Creates an appointment, recurring appointment, or service appointment (service activity), and calls the scheduling engine to make sure that it is valid for all constraints without any scheduling conflicts.</span></span>|<xref href="Microsoft.Dynamics.CRM.Book?text=Book Action" />|<xref:Microsoft.Crm.Sdk.Messages.BookRequest>|  
|<span data-ttu-id="49a60-114">Reschedules an appointment, recurring appointment, or service appointment (service activity), and calls the scheduling engine to make sure that it is valid for all constraints without any scheduling conflicts.</span><span class="sxs-lookup"><span data-stu-id="49a60-114">Reschedules an appointment, recurring appointment, or service appointment (service activity), and calls the scheduling engine to make sure that it is valid for all constraints without any scheduling conflicts.</span></span>|<xref href="Microsoft.Dynamics.CRM.Reschedule?text=Reschedule Action" />|<xref:Microsoft.Crm.Sdk.Messages.RescheduleRequest>|  
  
## <a name="in-this-section"></a><span data-ttu-id="49a60-115">In This Section</span><span class="sxs-lookup"><span data-stu-id="49a60-115">In This Section</span></span>  
 [<span data-ttu-id="49a60-116">Appointment Entities</span><span class="sxs-lookup"><span data-stu-id="49a60-116">Appointment Entities</span></span>](appointment-entities.md)  
  
 [<span data-ttu-id="49a60-117">Recurring Appointment Entities</span><span class="sxs-lookup"><span data-stu-id="49a60-117">Recurring Appointment Entities</span></span>](recurring-appointment-entities.md)  
  
 [<span data-ttu-id="49a60-118">Calendar Entities</span><span class="sxs-lookup"><span data-stu-id="49a60-118">Calendar Entities</span></span>](calendar-entities.md)  
  
 [<span data-ttu-id="49a60-119">Resource Entities</span><span class="sxs-lookup"><span data-stu-id="49a60-119">Resource Entities</span></span>](resource-entities.md)  
  
 [<span data-ttu-id="49a60-120">Service Entity</span><span class="sxs-lookup"><span data-stu-id="49a60-120">Service Entity</span></span>](service-entity.md)  
  
 [<span data-ttu-id="49a60-121">Sample Code for Recurring Appointments</span><span class="sxs-lookup"><span data-stu-id="49a60-121">Sample Code for Recurring Appointments</span></span>](sample-code-schedule-appointment-entities.md)
