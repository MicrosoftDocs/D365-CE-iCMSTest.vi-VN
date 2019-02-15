---
title: Update a recurring appointment (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Update a recurring appointment series by using the IOrganizationService.Entity method or the UpdateRequest message on the RecurringAppointmentMaster entity.
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
- updating recurring appointments and recurring appointment series
- updating basic information in a recurring appointment series
- schedule and appointment entities, updating recurring appointments and recurring appointment series
ms.assetid: 8b4e75d1-4d3e-4d93-b4c1-6223269c4d4b
caps.latest.revision: 24
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 56a0f028b881d5093d72f97f73944b38c1f322ee
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388021"
---
# <a name="update-a-recurring-appointment"></a><span data-ttu-id="cc8d8-103">Update a recurring appointment</span><span class="sxs-lookup"><span data-stu-id="cc8d8-103">Update a recurring appointment</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="cc8d8-104">You can either update the whole series or update an instance of a recurring appointment.</span><span class="sxs-lookup"><span data-stu-id="cc8d8-104">You can either update the whole series or update an instance of a recurring appointment.</span></span>  
  
## <a name="update-a-recurring-appointment-series"></a><span data-ttu-id="cc8d8-105">Update a recurring appointment series</span><span class="sxs-lookup"><span data-stu-id="cc8d8-105">Update a recurring appointment series</span></span>  
 <span data-ttu-id="cc8d8-106">You can update a recurring appointment series by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span><span class="sxs-lookup"><span data-stu-id="cc8d8-106">You can update a recurring appointment series by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span></span> <span data-ttu-id="cc8d8-107">method or the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message on the `RecurringAppointmentMaster` entity.</span><span class="sxs-lookup"><span data-stu-id="cc8d8-107">method or the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message on the `RecurringAppointmentMaster` entity.</span></span> <span data-ttu-id="cc8d8-108">You can update the *basic* or *recurrence* information.</span><span class="sxs-lookup"><span data-stu-id="cc8d8-108">You can update the *basic* or *recurrence* information.</span></span>  
  
### <a name="update-basic-information"></a><span data-ttu-id="cc8d8-109">Update basic information</span><span class="sxs-lookup"><span data-stu-id="cc8d8-109">Update basic information</span></span>  
 <span data-ttu-id="cc8d8-110">When you update the basic information of a recurring appointment series, such as subject, location, or attendees, all instances in the recurring appointment series are updated except those that have exceptions on the same attribute.</span><span class="sxs-lookup"><span data-stu-id="cc8d8-110">When you update the basic information of a recurring appointment series, such as subject, location, or attendees, all instances in the recurring appointment series are updated except those that have exceptions on the same attribute.</span></span>  
  
### <a name="update-recurrence-information"></a><span data-ttu-id="cc8d8-111">Update recurrence information</span><span class="sxs-lookup"><span data-stu-id="cc8d8-111">Update recurrence information</span></span>  
 <span data-ttu-id="cc8d8-112">When you update the recurring information of a recurring appointment series, such as pattern and range, the following things occur:</span><span class="sxs-lookup"><span data-stu-id="cc8d8-112">When you update the recurring information of a recurring appointment series, such as pattern and range, the following things occur:</span></span>  
  
1. <span data-ttu-id="cc8d8-113">A new series with a new `RecurringAppointmentMaster.ActivityId` is created that has the same information as the original series, and the date in the `RecurringAppointmentMaster.EffectiveEndDate` attribute of the new series is set to the last occurring past instance of the original series.</span><span class="sxs-lookup"><span data-stu-id="cc8d8-113">A new series with a new `RecurringAppointmentMaster.ActivityId` is created that has the same information as the original series, and the date in the `RecurringAppointmentMaster.EffectiveEndDate` attribute of the new series is set to the last occurring past instance of the original series.</span></span> <span data-ttu-id="cc8d8-114">All the future instances of the original series are deleted.</span><span class="sxs-lookup"><span data-stu-id="cc8d8-114">All the future instances of the original series are deleted.</span></span> <span data-ttu-id="cc8d8-115">In this manner, the original series is ended, and the history of the past instances is preserved in the system by storing it in a new series.</span><span class="sxs-lookup"><span data-stu-id="cc8d8-115">In this manner, the original series is ended, and the history of the past instances is preserved in the system by storing it in a new series.</span></span>  
  
2. <span data-ttu-id="cc8d8-116">The new information is used to create the future instances of the new series from the effective start date (`RecurringAppointmentMaster.EffectiveStartDate`).</span><span class="sxs-lookup"><span data-stu-id="cc8d8-116">The new information is used to create the future instances of the new series from the effective start date (`RecurringAppointmentMaster.EffectiveStartDate`).</span></span>  
  
   <span data-ttu-id="cc8d8-117">Also, the `RecurringAppointmentMaster.GroupId` attribute for both the original and the new series  is populated with the same value.</span><span class="sxs-lookup"><span data-stu-id="cc8d8-117">Also, the `RecurringAppointmentMaster.GroupId` attribute for both the original and the new series  is populated with the same value.</span></span> <span data-ttu-id="cc8d8-118">This implies that whenever you update the recurrence information in a recurring appointment series, all the new series’ that are created have the same value for the `RecurringAppointmentMaster.GroupId` attribute as the recurring appointment series that is updated, although each series has a unique series ID.</span><span class="sxs-lookup"><span data-stu-id="cc8d8-118">This implies that whenever you update the recurrence information in a recurring appointment series, all the new series’ that are created have the same value for the `RecurringAppointmentMaster.GroupId` attribute as the recurring appointment series that is updated, although each series has a unique series ID.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cc8d8-119">When you update the recurrence information of a recurring appointment series that has all the instances slated to occur in future, all instances are deleted and new recurrence information is used to create or expand new instances.</span><span class="sxs-lookup"><span data-stu-id="cc8d8-119">When you update the recurrence information of a recurring appointment series that has all the instances slated to occur in future, all instances are deleted and new recurrence information is used to create or expand new instances.</span></span>  
  
 <span data-ttu-id="cc8d8-120">To see the sample code for updating a recurring appointment series, see [Sample: Update a Recurring Appointment](sample-reschedule-cancel-recurring-appointment.md).</span><span class="sxs-lookup"><span data-stu-id="cc8d8-120">To see the sample code for updating a recurring appointment series, see [Sample: Update a Recurring Appointment](sample-reschedule-cancel-recurring-appointment.md).</span></span>  
  
## <a name="update-a-recurring-appointment-instance"></a><span data-ttu-id="cc8d8-121">Update a recurring appointment instance</span><span class="sxs-lookup"><span data-stu-id="cc8d8-121">Update a recurring appointment instance</span></span>  
 <span data-ttu-id="cc8d8-122">Because the recurring appointment records are stored as appointment objects, you can use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span><span class="sxs-lookup"><span data-stu-id="cc8d8-122">Because the recurring appointment records are stored as appointment objects, you can use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span></span> <span data-ttu-id="cc8d8-123">method on the `Appointment` entity to update a recurring appointment instance.</span><span class="sxs-lookup"><span data-stu-id="cc8d8-123">method on the `Appointment` entity to update a recurring appointment instance.</span></span> <span data-ttu-id="cc8d8-124">When you update a recurring appointment instance, the instance is marked as an exception to the recurring appointment series.</span><span class="sxs-lookup"><span data-stu-id="cc8d8-124">When you update a recurring appointment instance, the instance is marked as an exception to the recurring appointment series.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="cc8d8-125">[Create a Recurring Appointment Exception](create-recurring-appointment-series-instance-exception.md#bkmk_createexception)</span><span class="sxs-lookup"><span data-stu-id="cc8d8-125">[Create a Recurring Appointment Exception](create-recurring-appointment-series-instance-exception.md#bkmk_createexception)</span></span>  
  
 <span data-ttu-id="cc8d8-126">You can also use the <xref:Microsoft.Crm.Sdk.Messages.CreateExceptionRequest> class on the `Appointment` entity to update a recurring appointment instance.</span><span class="sxs-lookup"><span data-stu-id="cc8d8-126">You can also use the <xref:Microsoft.Crm.Sdk.Messages.CreateExceptionRequest> class on the `Appointment` entity to update a recurring appointment instance.</span></span>  
  
> [!TIP]
>  <span data-ttu-id="cc8d8-127">Recurring appointment instances can be identified using the `Appointment.InstanceTypeCode` attribute, which will have a value of “2” (Recurring Instance).</span><span class="sxs-lookup"><span data-stu-id="cc8d8-127">Recurring appointment instances can be identified using the `Appointment.InstanceTypeCode` attribute, which will have a value of “2” (Recurring Instance).</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)]<span data-ttu-id="cc8d8-128">[Appointment Entity](entities/appointment.md)</span><span class="sxs-lookup"><span data-stu-id="cc8d8-128">[Appointment Entity](entities/appointment.md)</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="cc8d8-129">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="cc8d8-129">See also</span></span>  
 <span data-ttu-id="cc8d8-130">[Recurring Appointment Entities](recurring-appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="cc8d8-130">[Recurring Appointment Entities](recurring-appointment-entities.md) </span></span>  
 <span data-ttu-id="cc8d8-131">[Delete or end a recurring appointment series or instance](delete-or-end-a-recurring-appointment-series-or-instance.md) </span><span class="sxs-lookup"><span data-stu-id="cc8d8-131">[Delete or end a recurring appointment series or instance](delete-or-end-a-recurring-appointment-series-or-instance.md) </span></span>  
 <span data-ttu-id="cc8d8-132">[Sample: Create, Retrieve, Update, and Delete (CRUD) a Recurring Appointment](sample-create-retrieve-update-delete-recurring-appointment.md) </span><span class="sxs-lookup"><span data-stu-id="cc8d8-132">[Sample: Create, Retrieve, Update, and Delete (CRUD) a Recurring Appointment](sample-create-retrieve-update-delete-recurring-appointment.md) </span></span>  
 [<span data-ttu-id="cc8d8-133">Sample: Reschedule and Cancel Recurring Appointment</span><span class="sxs-lookup"><span data-stu-id="cc8d8-133">Sample: Reschedule and Cancel Recurring Appointment</span></span>](sample-reschedule-cancel-recurring-appointment.md)
