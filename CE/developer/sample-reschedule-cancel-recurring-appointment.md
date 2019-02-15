---
title: 'Sample: Reschedule and  cancel a recurring appointment (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: Sample demonstrates how to reschedule and cancel appointment instances in a recurring appointment series using the RescheduleRequest message.
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
- rescheduling or canceling recurring appointments sample, schedule and appointment entities samples
- sample for rescheduling or canceling recurring appointments
- schedule and appointment entities
ms.assetid: cc070cb3-f1c0-4390-8d23-ba2b60101d59
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 20017e4873c7be43a7b7b0b32d6bfe472d266a0c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388559"
---
# <a name="sample-reschedule-and--cancel-a-recurring-appointment"></a><span data-ttu-id="f16a6-103">Sample: Reschedule and  cancel a recurring appointment</span><span class="sxs-lookup"><span data-stu-id="f16a6-103">Sample: Reschedule and  cancel a recurring appointment</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="f16a6-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="f16a6-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="f16a6-105">Download the complete sample from [Sample: Work with Schedules and Appointments](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).</span><span class="sxs-lookup"><span data-stu-id="f16a6-105">Download the complete sample from [Sample: Work with Schedules and Appointments](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f16a6-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="f16a6-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="f16a6-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="f16a6-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="f16a6-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="f16a6-108">Demonstrates</span></span>  
 <span data-ttu-id="f16a6-109">The following code example demonstrates how to reschedule and cancel appointment instances in a recurring appointment series using the <xref:Microsoft.Crm.Sdk.Messages.RescheduleRequest> message.</span><span class="sxs-lookup"><span data-stu-id="f16a6-109">The following code example demonstrates how to reschedule and cancel appointment instances in a recurring appointment series using the <xref:Microsoft.Crm.Sdk.Messages.RescheduleRequest> message.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f16a6-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="f16a6-110">Example</span></span>  
 [!code-csharp[ScheduleAndAppointment#RescheduleandCancelRecurringAppointmentInstance](../snippets/csharp/CRMV8/scheduleandappointment/cs/rescheduleandcancelrecurringappointmentinstance.cs#rescheduleandcancelrecurringappointmentinstance)]  
  
### <a name="see-also"></a><span data-ttu-id="f16a6-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="f16a6-111">See also</span></span>  
 <span data-ttu-id="f16a6-112">[Recurring Appointment Entities](recurring-appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="f16a6-112">[Recurring Appointment Entities](recurring-appointment-entities.md) </span></span>  
 <span data-ttu-id="f16a6-113">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="f16a6-113">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
 <span data-ttu-id="f16a6-114">[Sample Code for Recurring Appointments](sample-code-schedule-appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="f16a6-114">[Sample Code for Recurring Appointments](sample-code-schedule-appointment-entities.md) </span></span>  
 <span data-ttu-id="f16a6-115">[Sample: End a Recurring Appointment Series](sample-end-recurring-appointment-series.md) </span><span class="sxs-lookup"><span data-stu-id="f16a6-115">[Sample: End a Recurring Appointment Series](sample-end-recurring-appointment-series.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.RescheduleRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest>
