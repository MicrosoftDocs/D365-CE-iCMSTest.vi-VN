---
title: Create a recurring appointment series, instance, or exception (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: programmatically create a recurring appointment master (series),  individual recurring appointment instances, exceptions to those instances, or convert an appointment to a recurring appointment.
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
- schedule and appointment entities, converting appointments to recurring appointments
- identifying recurring appointment instances
- recurring appointment series; instance; or exception, schedule and appointment entities
- recurring appointment instances stored as appointment records, schedule and appointment entities
- appointments
- recurring appointment instances, updating; deleting; or identifying
- appointments, converting to recurring appointments
- converting appointments to recurring appointments
- deleting recurring appointment instances
- updating recurring appointment instances
- creating a recurring appointment series; instance; or exception
- schedule and appointment entities, creating a recurring appointment series; instance; or exception
ms.assetid: bb2eadf8-058e-43c2-9fda-c56ac501bc1c
caps.latest.revision: 29
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 19cf97203cd900b6707fbd5f906779d67171eaf5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385749"
---
# <a name="create-a-recurring-appointment-series-instance-or-exception"></a><span data-ttu-id="acdce-103">Create a recurring appointment series, instance, or exception</span><span class="sxs-lookup"><span data-stu-id="acdce-103">Create a recurring appointment series, instance, or exception</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="acdce-104">When you create a recurring appointment master (series), [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] creates individual appointment instances based on the specified recurrence information.</span><span class="sxs-lookup"><span data-stu-id="acdce-104">When you create a recurring appointment master (series), [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] creates individual appointment instances based on the specified recurrence information.</span></span> <span data-ttu-id="acdce-105">You can also create individual recurring appointment instances and exceptions to those instances, and you can convert an appointment to a recurring appointment.</span><span class="sxs-lookup"><span data-stu-id="acdce-105">You can also create individual recurring appointment instances and exceptions to those instances, and you can convert an appointment to a recurring appointment.</span></span>  
  
<a name="bkmk_createseries"></a>   
## <a name="create-a-recurring-appointment-series"></a><span data-ttu-id="acdce-106">Create a recurring appointment series</span><span class="sxs-lookup"><span data-stu-id="acdce-106">Create a recurring appointment series</span></span>  
 <span data-ttu-id="acdce-107">To create a recurring appointment series (a `RecurringAppointmentMaster` record), you can use the <xref:Microsoft.Crm.Sdk.Messages.BookRequest> message, the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message, or the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span><span class="sxs-lookup"><span data-stu-id="acdce-107">To create a recurring appointment series (a `RecurringAppointmentMaster` record), you can use the <xref:Microsoft.Crm.Sdk.Messages.BookRequest> message, the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message, or the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span></span> <span data-ttu-id="acdce-108">method.</span><span class="sxs-lookup"><span data-stu-id="acdce-108">method.</span></span>  
  
 <span data-ttu-id="acdce-109">When you create a recurring appointment series, the following things occur:</span><span class="sxs-lookup"><span data-stu-id="acdce-109">When you create a recurring appointment series, the following things occur:</span></span>  
  
1. <span data-ttu-id="acdce-110">A `RecurringAppointmentMaster` record (recurring appointment series) is created that contains the basic and recurrence information about the recurring appointment series.</span><span class="sxs-lookup"><span data-stu-id="acdce-110">A `RecurringAppointmentMaster` record (recurring appointment series) is created that contains the basic and recurrence information about the recurring appointment series.</span></span> <span data-ttu-id="acdce-111">Each record can be uniquely identified using the `RecurringAppointmentMaster.ActivityId` property.</span><span class="sxs-lookup"><span data-stu-id="acdce-111">Each record can be uniquely identified using the `RecurringAppointmentMaster.ActivityId` property.</span></span> <span data-ttu-id="acdce-112">Further, this recurring appointment series is also created and stored as an activity (`ActivityPointer`) record.</span><span class="sxs-lookup"><span data-stu-id="acdce-112">Further, this recurring appointment series is also created and stored as an activity (`ActivityPointer`) record.</span></span> <span data-ttu-id="acdce-113">The activity record can be uniquely identified using the `ActivityPointer.ActivityId` property.</span><span class="sxs-lookup"><span data-stu-id="acdce-113">The activity record can be uniquely identified using the `ActivityPointer.ActivityId` property.</span></span>  
  
2. <span data-ttu-id="acdce-114">Individual recurring appointment instances are created based on the recurrence information and stored as `Appointment` records.</span><span class="sxs-lookup"><span data-stu-id="acdce-114">Individual recurring appointment instances are created based on the recurrence information and stored as `Appointment` records.</span></span> <span data-ttu-id="acdce-115">These appointment objects are associated with the parent recurring appointment series using the `Appointment.SeriesId` property and have the same value as the parent recurring appointment series ID (`ActivityPointer.SeriesId`).</span><span class="sxs-lookup"><span data-stu-id="acdce-115">These appointment objects are associated with the parent recurring appointment series using the `Appointment.SeriesId` property and have the same value as the parent recurring appointment series ID (`ActivityPointer.SeriesId`).</span></span>  
  
    <span data-ttu-id="acdce-116">The value of the `Appointment.InstanceTypeCode` property is set to **Recurring Instance** (picklist value 2) for these appointment objects.</span><span class="sxs-lookup"><span data-stu-id="acdce-116">The value of the `Appointment.InstanceTypeCode` property is set to **Recurring Instance** (picklist value 2) for these appointment objects.</span></span>  
  
   > [!NOTE]
   >  <span data-ttu-id="acdce-117">Recurring appointment instances are created based on the expansion model and the parameters that define it.</span><span class="sxs-lookup"><span data-stu-id="acdce-117">Recurring appointment instances are created based on the expansion model and the parameters that define it.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="acdce-118">[Recurring Appointment Partial Expansion Model](recurring-appointment-partial-expansion-model.md).</span><span class="sxs-lookup"><span data-stu-id="acdce-118">[Recurring Appointment Partial Expansion Model](recurring-appointment-partial-expansion-model.md).</span></span>  
  
   <span data-ttu-id="acdce-119">For sample code that demonstrates how to create a recurring appointment series, see [Sample: Create a Recurring Appointment](sample-create-retrieve-update-delete-recurring-appointment.md).</span><span class="sxs-lookup"><span data-stu-id="acdce-119">For sample code that demonstrates how to create a recurring appointment series, see [Sample: Create a Recurring Appointment](sample-create-retrieve-update-delete-recurring-appointment.md).</span></span>  
  
<a name="bkmk_createinstance"></a>   
## <a name="create-a-recurring-appointment-instance"></a><span data-ttu-id="acdce-120">Create a recurring appointment instance</span><span class="sxs-lookup"><span data-stu-id="acdce-120">Create a recurring appointment instance</span></span>  
 <span data-ttu-id="acdce-121">To create a recurring appointment instance (a `RecurringAppointmentMaster` record), you can use the <xref:Microsoft.Crm.Sdk.Messages.CreateInstanceRequest>.</span><span class="sxs-lookup"><span data-stu-id="acdce-121">To create a recurring appointment instance (a `RecurringAppointmentMaster` record), you can use the <xref:Microsoft.Crm.Sdk.Messages.CreateInstanceRequest>.</span></span> <span data-ttu-id="acdce-122">This message takes two parameters: the number of instances to be created and the recurring appointment series for which the instances have to be created.</span><span class="sxs-lookup"><span data-stu-id="acdce-122">This message takes two parameters: the number of instances to be created and the recurring appointment series for which the instances have to be created.</span></span>  
  
 <span data-ttu-id="acdce-123">The instances are created after the last instance in the recurring appointment series.</span><span class="sxs-lookup"><span data-stu-id="acdce-123">The instances are created after the last instance in the recurring appointment series.</span></span> <span data-ttu-id="acdce-124">Also, the instances are only created up until the future instance cutoff date, regardless of the number of instances you have specified for creation.</span><span class="sxs-lookup"><span data-stu-id="acdce-124">Also, the instances are only created up until the future instance cutoff date, regardless of the number of instances you have specified for creation.</span></span>  
  
<a name="bkmk_createexception"></a>   
## <a name="create-a-recurring-appointment-exception"></a><span data-ttu-id="acdce-125">Create a recurring appointment exception</span><span class="sxs-lookup"><span data-stu-id="acdce-125">Create a recurring appointment exception</span></span>  
 <span data-ttu-id="acdce-126">An exception is created when you either update or delete an instance of the recurring appointment.</span><span class="sxs-lookup"><span data-stu-id="acdce-126">An exception is created when you either update or delete an instance of the recurring appointment.</span></span> <span data-ttu-id="acdce-127">Recurring appointment instances are stored as an appointment record along like other appointments, and you can identify a recurring appointment instance using the `Appointment.InstanceTypeCode` attribute of an appointment record, which will have a value of **Recurring Instance** (picklist value 2).</span><span class="sxs-lookup"><span data-stu-id="acdce-127">Recurring appointment instances are stored as an appointment record along like other appointments, and you can identify a recurring appointment instance using the `Appointment.InstanceTypeCode` attribute of an appointment record, which will have a value of **Recurring Instance** (picklist value 2).</span></span>  
  
 <span data-ttu-id="acdce-128">You can create exceptions in the following ways:</span><span class="sxs-lookup"><span data-stu-id="acdce-128">You can create exceptions in the following ways:</span></span>  
  
-   <span data-ttu-id="acdce-129">Use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> class on the `Appointment` entity to update a recurring appointment instance, and set the value of the `Appointment.InstanceTypeCode` attribute to **Recurring Exception** (picklist value 3).</span><span class="sxs-lookup"><span data-stu-id="acdce-129">Use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> class on the `Appointment` entity to update a recurring appointment instance, and set the value of the `Appointment.InstanceTypeCode` attribute to **Recurring Exception** (picklist value 3).</span></span>  
  
-   <span data-ttu-id="acdce-130">Use the <xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest> class on the `Appointment` entity to delete a recurring appointment instance.</span><span class="sxs-lookup"><span data-stu-id="acdce-130">Use the <xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest> class on the `Appointment` entity to delete a recurring appointment instance.</span></span> <span data-ttu-id="acdce-131">Deleting an appointment instance marks it an exception by creating an entry for the instance in the `RecurringAppointmentMaster.DeletedExceptionsList` attribute for the parent appointment series object.</span><span class="sxs-lookup"><span data-stu-id="acdce-131">Deleting an appointment instance marks it an exception by creating an entry for the instance in the `RecurringAppointmentMaster.DeletedExceptionsList` attribute for the parent appointment series object.</span></span>  
  
-   <span data-ttu-id="acdce-132">Use the <xref:Microsoft.Crm.Sdk.Messages.CreateExceptionRequest> class on the `Appointment` entity.</span><span class="sxs-lookup"><span data-stu-id="acdce-132">Use the <xref:Microsoft.Crm.Sdk.Messages.CreateExceptionRequest> class on the `Appointment` entity.</span></span>  
  
<a name="bkmk_convert"></a>   
## <a name="convert-an-appointment-to-a-recurring-appointment"></a><span data-ttu-id="acdce-133">Convert an appointment to a recurring appointment</span><span class="sxs-lookup"><span data-stu-id="acdce-133">Convert an appointment to a recurring appointment</span></span>  
 <span data-ttu-id="acdce-134">A recurring appointment is an appointment with recurrence information.</span><span class="sxs-lookup"><span data-stu-id="acdce-134">A recurring appointment is an appointment with recurrence information.</span></span> <span data-ttu-id="acdce-135">You can convert an existing appointment in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] to a recurring appointment by using <xref:Microsoft.Crm.Sdk.Messages.AddRecurrenceRequest>.</span><span class="sxs-lookup"><span data-stu-id="acdce-135">You can convert an existing appointment in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] to a recurring appointment by using <xref:Microsoft.Crm.Sdk.Messages.AddRecurrenceRequest>.</span></span> <span data-ttu-id="acdce-136">When you convert an existing appointment to a recurring appointment, the data from the existing appointment is copied to a new recurring appointment master instance and the existing appointment is deleted.</span><span class="sxs-lookup"><span data-stu-id="acdce-136">When you convert an existing appointment to a recurring appointment, the data from the existing appointment is copied to a new recurring appointment master instance and the existing appointment is deleted.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="acdce-137">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="acdce-137">See also</span></span>  
 <span data-ttu-id="acdce-138">[Recurring Appointment Entities](recurring-appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="acdce-138">[Recurring Appointment Entities](recurring-appointment-entities.md) </span></span>  
 <span data-ttu-id="acdce-139">[Update a recurring appointment](update-recurring-appointment.md) </span><span class="sxs-lookup"><span data-stu-id="acdce-139">[Update a recurring appointment](update-recurring-appointment.md) </span></span>  
 <span data-ttu-id="acdce-140">[Sample: Create a Recurring Appointment](sample-create-retrieve-update-delete-recurring-appointment.md) </span><span class="sxs-lookup"><span data-stu-id="acdce-140">[Sample: Create a Recurring Appointment](sample-create-retrieve-update-delete-recurring-appointment.md) </span></span>  
 [<span data-ttu-id="acdce-141">Sample: Convert an Appointment to a Recurring Appointment</span><span class="sxs-lookup"><span data-stu-id="acdce-141">Sample: Convert an Appointment to a Recurring Appointment</span></span>](sample-convert-appointment-recurring-appointment.md)
