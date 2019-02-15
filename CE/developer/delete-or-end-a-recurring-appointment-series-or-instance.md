---
title: Delete or end a recurring appointment series or instance | MicrosoftDocs
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
- deleting a recurring appointment series or instance
- schedule and appointment entities, recurring appointment instances or series
- ending a recurring appointment series after a specified date
- recurring appointment instances, deleting or ending
- schedule and appointment entities, deleting or ending a recurring appointment series or instance
ms.assetid: c07ed908-effe-404b-9925-467b31a29766
caps.latest.revision: 18
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 22602f3537174969b9fc451811b37f4712c162c9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388310"
---
# <a name="delete-or-end-a-recurring-appointment-series-or-instance"></a><span data-ttu-id="13cca-102">Delete or end a recurring appointment series or instance</span><span class="sxs-lookup"><span data-stu-id="13cca-102">Delete or end a recurring appointment series or instance</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="13cca-103">You can delete a recurring appointment series, delete an instance in the series, or end a recurring appointment series after a specified date and time.</span><span class="sxs-lookup"><span data-stu-id="13cca-103">You can delete a recurring appointment series, delete an instance in the series, or end a recurring appointment series after a specified date and time.</span></span>  
  
<a name="bkmk_deleteinstance"></a>   
## <a name="delete-a-recurring-appointment-instance"></a><span data-ttu-id="13cca-104">Delete a recurring appointment instance</span><span class="sxs-lookup"><span data-stu-id="13cca-104">Delete a recurring appointment instance</span></span>  
 <span data-ttu-id="13cca-105">Because recurring appointment instances are stored as appointment objects, you can use the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest></span><span class="sxs-lookup"><span data-stu-id="13cca-105">Because recurring appointment instances are stored as appointment objects, you can use the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest></span></span> <span data-ttu-id="13cca-106">on an appointment record to delete a recurring appointment instance.</span><span class="sxs-lookup"><span data-stu-id="13cca-106">on an appointment record to delete a recurring appointment instance.</span></span> <span data-ttu-id="13cca-107">Deleting an appointment instance marks it as an exception by creating an entry for the instance in the `RecurringAppointmentMaster.DeletedExceptionsList` attribute for the parent appointment series object.</span><span class="sxs-lookup"><span data-stu-id="13cca-107">Deleting an appointment instance marks it as an exception by creating an entry for the instance in the `RecurringAppointmentMaster.DeletedExceptionsList` attribute for the parent appointment series object.</span></span> <span data-ttu-id="13cca-108">This is done to track the deleted instance for later synchronization with [!INCLUDE[pn_crm_for_outlook_full](../includes/pn-crm-for-outlook-full.md)].</span><span class="sxs-lookup"><span data-stu-id="13cca-108">This is done to track the deleted instance for later synchronization with [!INCLUDE[pn_crm_for_outlook_full](../includes/pn-crm-for-outlook-full.md)].</span></span>  
  
<a name="bkmk_deleteseries"></a>   
## <a name="delete-a-recurring-appointment-series"></a><span data-ttu-id="13cca-109">Delete a recurring appointment series</span><span class="sxs-lookup"><span data-stu-id="13cca-109">Delete a recurring appointment series</span></span>  
 <span data-ttu-id="13cca-110">You can use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span><span class="sxs-lookup"><span data-stu-id="13cca-110">You can use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span></span> <span data-ttu-id="13cca-111">method or the <xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest> on a `RecurringAppointmentMaster` record to delete a recurring appointment series.</span><span class="sxs-lookup"><span data-stu-id="13cca-111">method or the <xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest> on a `RecurringAppointmentMaster` record to delete a recurring appointment series.</span></span> <span data-ttu-id="13cca-112">Deleting a series deletes the record and all of the associated recurring appointment instances.</span><span class="sxs-lookup"><span data-stu-id="13cca-112">Deleting a series deletes the record and all of the associated recurring appointment instances.</span></span>  
  
<a name="bkmk_endseries"></a>   
## <a name="end-a-recurring-appointment-series"></a><span data-ttu-id="13cca-113">End a recurring appointment series</span><span class="sxs-lookup"><span data-stu-id="13cca-113">End a recurring appointment series</span></span>  
 <span data-ttu-id="13cca-114">If you want to end a series before the original end date specified during the creation of the series, you can use the <xref:Microsoft.Crm.Sdk.Messages.DeleteOpenInstancesRequest> class.</span><span class="sxs-lookup"><span data-stu-id="13cca-114">If you want to end a series before the original end date specified during the creation of the series, you can use the <xref:Microsoft.Crm.Sdk.Messages.DeleteOpenInstancesRequest> class.</span></span> <span data-ttu-id="13cca-115">Using this message does the following:</span><span class="sxs-lookup"><span data-stu-id="13cca-115">Using this message does the following:</span></span>  
  
- <span data-ttu-id="13cca-116">Deletes all the “open” and “scheduled” future instances of the specified series from the date specified in the <xref:Microsoft.Crm.Sdk.Messages.DeleteOpenInstancesRequest.SeriesEndDate> property.</span><span class="sxs-lookup"><span data-stu-id="13cca-116">Deletes all the “open” and “scheduled” future instances of the specified series from the date specified in the <xref:Microsoft.Crm.Sdk.Messages.DeleteOpenInstancesRequest.SeriesEndDate> property.</span></span> <span data-ttu-id="13cca-117">However, if the state of the future instances is changed to “completed” or “canceled”, they are not deleted.</span><span class="sxs-lookup"><span data-stu-id="13cca-117">However, if the state of the future instances is changed to “completed” or “canceled”, they are not deleted.</span></span>  
  
- <span data-ttu-id="13cca-118">Sets the status of the past instances to the specified value in the <xref:Microsoft.Crm.Sdk.Messages.DeleteOpenInstancesRequest.StateOfPastInstances> property.</span><span class="sxs-lookup"><span data-stu-id="13cca-118">Sets the status of the past instances to the specified value in the <xref:Microsoft.Crm.Sdk.Messages.DeleteOpenInstancesRequest.StateOfPastInstances> property.</span></span> <span data-ttu-id="13cca-119">However, the past instances are not deleted.</span><span class="sxs-lookup"><span data-stu-id="13cca-119">However, the past instances are not deleted.</span></span>  
  
- <span data-ttu-id="13cca-120">Terminates the series to the last occurring past instance date with respect to the date specified in the <xref:Microsoft.Crm.Sdk.Messages.DeleteOpenInstancesRequest.SeriesEndDate> property, and sets the state of the series to “canceled”.</span><span class="sxs-lookup"><span data-stu-id="13cca-120">Terminates the series to the last occurring past instance date with respect to the date specified in the <xref:Microsoft.Crm.Sdk.Messages.DeleteOpenInstancesRequest.SeriesEndDate> property, and sets the state of the series to “canceled”.</span></span>  
  
  <span data-ttu-id="13cca-121">This allows you to preserve the instances of a recurring appointment series even if you have decided to end it prematurely.</span><span class="sxs-lookup"><span data-stu-id="13cca-121">This allows you to preserve the instances of a recurring appointment series even if you have decided to end it prematurely.</span></span> <span data-ttu-id="13cca-122">This is useful if you have attached notes or attachments to past instances of a recurring appointment series that contain important information about the customer or business.</span><span class="sxs-lookup"><span data-stu-id="13cca-122">This is useful if you have attached notes or attachments to past instances of a recurring appointment series that contain important information about the customer or business.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="13cca-123">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="13cca-123">See also</span></span>  
 <span data-ttu-id="13cca-124">[Recurring Appointment Entities](recurring-appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="13cca-124">[Recurring Appointment Entities](recurring-appointment-entities.md) </span></span>  
 <span data-ttu-id="13cca-125">[Link custom attributes of the recurring appointment master and appointment entities](link-custom-attributes-recurring-master-appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="13cca-125">[Link custom attributes of the recurring appointment master and appointment entities](link-custom-attributes-recurring-master-appointment-entities.md) </span></span>  
 <span data-ttu-id="13cca-126">[Sample: Create, Retrieve, Update, and Delete (CRUD) a Recurring Appointment](sample-create-retrieve-update-delete-recurring-appointment.md) </span><span class="sxs-lookup"><span data-stu-id="13cca-126">[Sample: Create, Retrieve, Update, and Delete (CRUD) a Recurring Appointment](sample-create-retrieve-update-delete-recurring-appointment.md) </span></span>  
 [<span data-ttu-id="13cca-127">Sample: End a Recurring Appointment</span><span class="sxs-lookup"><span data-stu-id="13cca-127">Sample: End a Recurring Appointment</span></span>](sample-end-recurring-appointment-series.md)
