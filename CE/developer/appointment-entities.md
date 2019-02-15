---
title: Appointment entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Overview of the appointment entity, which represents a commitment over a time interval with start and end times and a duration.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 0e1254fa-d7a1-42a5-840c-cd26162c1f48
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 26f3d4b8e1099375da6b78ae52212a5a1a5213f1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386424"
---
# <a name="appointment-entities"></a><span data-ttu-id="99381-103">Appointment entities</span><span class="sxs-lookup"><span data-stu-id="99381-103">Appointment entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="99381-104">An *appointment* is a commitment that represents a time interval with start and end times and duration.</span><span class="sxs-lookup"><span data-stu-id="99381-104">An *appointment* is a commitment that represents a time interval with start and end times and duration.</span></span> <span data-ttu-id="99381-105">The schema name for this entity is `Appointment`.</span><span class="sxs-lookup"><span data-stu-id="99381-105">The schema name for this entity is `Appointment`.</span></span>
<span data-ttu-id="99381-106">A *service appointment* represents an appointment for service.</span><span class="sxs-lookup"><span data-stu-id="99381-106">A *service appointment* represents an appointment for service.</span></span> <span data-ttu-id="99381-107">The schema name for this entity is `ServiceAppointment`.</span><span class="sxs-lookup"><span data-stu-id="99381-107">The schema name for this entity is `ServiceAppointment`.</span></span> <span data-ttu-id="99381-108">A service appointment can be customized independently from other activities to accommodate the customer's business requirements for service delivery.</span><span class="sxs-lookup"><span data-stu-id="99381-108">A service appointment can be customized independently from other activities to accommodate the customer's business requirements for service delivery.</span></span> <span data-ttu-id="99381-109">Service appointments can block the availability of required resources and participate in resource availability searches and scheduling.</span><span class="sxs-lookup"><span data-stu-id="99381-109">Service appointments can block the availability of required resources and participate in resource availability searches and scheduling.</span></span> <span data-ttu-id="99381-110">A service appointment must have a corresponding service.</span><span class="sxs-lookup"><span data-stu-id="99381-110">A service appointment must have a corresponding service.</span></span> <span data-ttu-id="99381-111">It can be already bound with a set of resources specified by an activity party (`ActivityParty`) list.</span><span class="sxs-lookup"><span data-stu-id="99381-111">It can be already bound with a set of resources specified by an activity party (`ActivityParty`) list.</span></span>  
  
<span data-ttu-id="99381-112">To create an appointment by making sure that the constraints are met, use the <xref:Microsoft.Crm.Sdk.Messages.BookRequest> message or the <xref:Microsoft.Crm.Sdk.Messages.RescheduleRequest> message.</span><span class="sxs-lookup"><span data-stu-id="99381-112">To create an appointment by making sure that the constraints are met, use the <xref:Microsoft.Crm.Sdk.Messages.BookRequest> message or the <xref:Microsoft.Crm.Sdk.Messages.RescheduleRequest> message.</span></span> <span data-ttu-id="99381-113">The scheduling engine stores the booked appointment and adjusts the free/busy information for the resource.</span><span class="sxs-lookup"><span data-stu-id="99381-113">The scheduling engine stores the booked appointment and adjusts the free/busy information for the resource.</span></span> <span data-ttu-id="99381-114">You can create an appointment at a specific time for a specific service that uses a specific set of resources, ignoring all constraints, by using the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span><span class="sxs-lookup"><span data-stu-id="99381-114">You can create an appointment at a specific time for a specific service that uses a specific set of resources, ignoring all constraints, by using the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span></span> <span data-ttu-id="99381-115">method or <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message.</span><span class="sxs-lookup"><span data-stu-id="99381-115">method or <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message.</span></span>  
  
<span data-ttu-id="99381-116">Appointments can block the availability of the required resources.</span><span class="sxs-lookup"><span data-stu-id="99381-116">Appointments can block the availability of the required resources.</span></span> <span data-ttu-id="99381-117">Appointments can be blocking, specified as part of the service definition or per appointment instance, for other appointments at the same interval.</span><span class="sxs-lookup"><span data-stu-id="99381-117">Appointments can be blocking, specified as part of the service definition or per appointment instance, for other appointments at the same interval.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="99381-118">In This Section</span><span class="sxs-lookup"><span data-stu-id="99381-118">In This Section</span></span>  
 [<span data-ttu-id="99381-119">Schedule and appointment entities</span><span class="sxs-lookup"><span data-stu-id="99381-119">Schedule and appointment entities</span></span>](schedule-appointment-entities.md)  
  
 [<span data-ttu-id="99381-120">Schedules in Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="99381-120">Schedules in Dynamics 365 for Customer Engagement</span></span>](schedule-collections.md)  
  
 [<span data-ttu-id="99381-121">Appointment Entity</span><span class="sxs-lookup"><span data-stu-id="99381-121">Appointment Entity</span></span>](entities/appointment.md)  
  
 [<span data-ttu-id="99381-122">ServiceAppointment Entity</span><span class="sxs-lookup"><span data-stu-id="99381-122">ServiceAppointment Entity</span></span>](entities/serviceappointment.md)
