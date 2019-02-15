---
title: 'Sample: Create, retrieve, update, and delete a recurring appointment (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: Sample demonstrates how to create, retrieve, update, and delete a recurring appointment series using four common methods.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- sample for creating, retrieving, updating, and deleting recurring appointments
- creating, retrieving, updating, and deleting recurring appointments sample, schedule and appointment entities samples
- schedule and appointment entities
ms.assetid: e8ec9b76-e219-4c2f-9816-c6fdf6ed8b0b
caps.latest.revision: 27
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ee51fa71667f4da90e1e0ae9dd89f919ca92e410
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388679"
---
# <a name="sample-create-retrieve-update-and-delete-a-recurring-appointment"></a><span data-ttu-id="c709d-103">Sample: Create, retrieve, update, and delete a recurring appointment</span><span class="sxs-lookup"><span data-stu-id="c709d-103">Sample: Create, retrieve, update, and delete a recurring appointment</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="c709d-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="c709d-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="c709d-105">Download the complete sample from [Sample: Work with Schedules and Appointments](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).</span><span class="sxs-lookup"><span data-stu-id="c709d-105">Download the complete sample from [Sample: Work with Schedules and Appointments](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c709d-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="c709d-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="c709d-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="c709d-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="c709d-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="c709d-108">Demonstrates</span></span>  
 <span data-ttu-id="c709d-109">This sample shows how to create, retrieve, update, and delete a recurring appointment series.</span><span class="sxs-lookup"><span data-stu-id="c709d-109">This sample shows how to create, retrieve, update, and delete a recurring appointment series.</span></span> <span data-ttu-id="c709d-110">This sample uses the following common methods:</span><span class="sxs-lookup"><span data-stu-id="c709d-110">This sample uses the following common methods:</span></span>  
  
-   <span data-ttu-id="c709d-111"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span><span class="sxs-lookup"><span data-stu-id="c709d-111"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span></span>  
  
-   <span data-ttu-id="c709d-112"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span><span class="sxs-lookup"><span data-stu-id="c709d-112"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span></span>  
  
-   <span data-ttu-id="c709d-113"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span><span class="sxs-lookup"><span data-stu-id="c709d-113"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span></span>  
  
-   <span data-ttu-id="c709d-114"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span><span class="sxs-lookup"><span data-stu-id="c709d-114"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span></span>  
  
## <a name="example"></a><span data-ttu-id="c709d-115">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="c709d-115">Example</span></span>  
 [!code-csharp[ScheduleAndAppointment#CRUDRecurringAppointment](../snippets/csharp/CRMV8/scheduleandappointment/cs/crudrecurringappointment.cs#crudrecurringappointment)]  
  
### <a name="see-also"></a><span data-ttu-id="c709d-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c709d-116">See also</span></span>  
 <span data-ttu-id="c709d-117">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="c709d-117">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
 <span data-ttu-id="c709d-118">[Create a Recurring Appointment](create-recurring-appointment-series-instance-exception.md) </span><span class="sxs-lookup"><span data-stu-id="c709d-118">[Create a Recurring Appointment](create-recurring-appointment-series-instance-exception.md) </span></span>  
 <span data-ttu-id="c709d-119">[Update a Recurring Appointment](update-recurring-appointment.md) </span><span class="sxs-lookup"><span data-stu-id="c709d-119">[Update a Recurring Appointment](update-recurring-appointment.md) </span></span>  
 <span data-ttu-id="c709d-120">[Delete a Recurring Appointment](delete-or-end-a-recurring-appointment-series-or-instance.md) </span><span class="sxs-lookup"><span data-stu-id="c709d-120">[Delete a Recurring Appointment](delete-or-end-a-recurring-appointment-series-or-instance.md) </span></span>  
 <span data-ttu-id="c709d-121">[Sample Code for Recurring Appointments](sample-code-schedule-appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="c709d-121">[Sample Code for Recurring Appointments](sample-code-schedule-appointment-entities.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*>
