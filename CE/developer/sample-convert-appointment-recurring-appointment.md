---
title: 'Sample: Convert an appointment to a recurring appointment (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: Sample demonstrates how to convert an appointment to a recurring appointment series by using the AddRecurrenceRequest message.
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
- schedule and appointment entities
- sample for converting appointments to recurring appointments
- converting appointments to recurring appointments sample, schedule and appointment entities samples
ms.assetid: 0b2a00b8-f970-4201-b10f-9ec13fa32afe
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0e6cef84d4e53312154b2d5c899525baa7e9ddf8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387562"
---
# <a name="sample-convert-an-appointment-to-a-recurring-appointment"></a><span data-ttu-id="e5c9d-103">Sample: Convert an appointment to a recurring appointment</span><span class="sxs-lookup"><span data-stu-id="e5c9d-103">Sample: Convert an appointment to a recurring appointment</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e5c9d-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="e5c9d-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="e5c9d-105">[Download the Schedule and Appointment samples](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).</span><span class="sxs-lookup"><span data-stu-id="e5c9d-105">[Download the Schedule and Appointment samples](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e5c9d-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="e5c9d-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="e5c9d-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="e5c9d-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="e5c9d-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="e5c9d-108">Demonstrates</span></span>  
 <span data-ttu-id="e5c9d-109">This sample shows how to convert an appointment to a recurring appointment series by using the <xref:Microsoft.Crm.Sdk.Messages.AddRecurrenceRequest> message.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-109">This sample shows how to convert an appointment to a recurring appointment series by using the <xref:Microsoft.Crm.Sdk.Messages.AddRecurrenceRequest> message.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e5c9d-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="e5c9d-110">Example</span></span>  
 [!code-csharp[ScheduleAndAppointment#ConvertAnAppointmenttoRecurringAppointment](../snippets/csharp/CRMV8/scheduleandappointment/cs/convertanappointmenttorecurringappointment.cs#convertanappointmenttorecurringappointment)]  
  
### <a name="see-also"></a><span data-ttu-id="e5c9d-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e5c9d-111">See also</span></span>  
 <span data-ttu-id="e5c9d-112">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="e5c9d-112">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
 <span data-ttu-id="e5c9d-113">[Convert an Appointment to a Recurring Appointment](create-recurring-appointment-series-instance-exception.md#bkmk_convert) </span><span class="sxs-lookup"><span data-stu-id="e5c9d-113">[Convert an Appointment to a Recurring Appointment](create-recurring-appointment-series-instance-exception.md#bkmk_convert) </span></span>  
 <span data-ttu-id="e5c9d-114">[Sample Code for Recurring Appointments](sample-code-schedule-appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="e5c9d-114">[Sample Code for Recurring Appointments](sample-code-schedule-appointment-entities.md) </span></span>  
 <span data-ttu-id="e5c9d-115">[Sample: Link Custom Attributes between Series and Instances](sample-link-custom-attributes-between-series-instances.md) </span><span class="sxs-lookup"><span data-stu-id="e5c9d-115">[Sample: Link Custom Attributes between Series and Instances](sample-link-custom-attributes-between-series-instances.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.AddRecurrenceRequest>
