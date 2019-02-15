---
title: 'Sample: End a recurring appointment series (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: Sample demonstrates how to end a recurring appointment series by using the DeleteOpenInstancesRequest message.
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
- sample for ending a recurring appointment series
- schedule and appointment entities
- ending a recurring appointment series sample, schedule and appointment entities samples
ms.assetid: 914a0fde-42ad-4a56-8d2d-7d0166bb2d3f
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 221a1eceb4ede22458380607118d74ae70f169b3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385695"
---
# <a name="sample-end-a-recurring-appointment-series"></a><span data-ttu-id="34a4a-103">Sample: End a recurring appointment series</span><span class="sxs-lookup"><span data-stu-id="34a4a-103">Sample: End a recurring appointment series</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="34a4a-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="34a4a-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="34a4a-105">Download the complete sample from [Sample: Work with Schedules and Appointments](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).</span><span class="sxs-lookup"><span data-stu-id="34a4a-105">Download the complete sample from [Sample: Work with Schedules and Appointments](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="34a4a-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="34a4a-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="34a4a-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="34a4a-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="34a4a-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="34a4a-108">Demonstrates</span></span>  
 <span data-ttu-id="34a4a-109">The following sample shows how to end a recurring appointment series by using the <xref:Microsoft.Crm.Sdk.Messages.DeleteOpenInstancesRequest> message.</span><span class="sxs-lookup"><span data-stu-id="34a4a-109">The following sample shows how to end a recurring appointment series by using the <xref:Microsoft.Crm.Sdk.Messages.DeleteOpenInstancesRequest> message.</span></span>  
  
## <a name="example"></a><span data-ttu-id="34a4a-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="34a4a-110">Example</span></span>  
 [!code-csharp[ScheduleAndAppointment#EndRecurringAppointmentSeries](../snippets/csharp/CRMV8/scheduleandappointment/cs/endrecurringappointmentseries.cs#endrecurringappointmentseries)]  
  
### <a name="see-also"></a><span data-ttu-id="34a4a-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="34a4a-111">See also</span></span>  
 <span data-ttu-id="34a4a-112">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="34a4a-112">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
 <span data-ttu-id="34a4a-113">[Delete or End a Recurring Appointment Series or Instance](delete-or-end-a-recurring-appointment-series-or-instance.md) </span><span class="sxs-lookup"><span data-stu-id="34a4a-113">[Delete or End a Recurring Appointment Series or Instance](delete-or-end-a-recurring-appointment-series-or-instance.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.DeleteOpenInstancesRequest>   
 <span data-ttu-id="34a4a-114">[Sample Code for Recurring Appointments](sample-code-schedule-appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="34a4a-114">[Sample Code for Recurring Appointments](sample-code-schedule-appointment-entities.md) </span></span>  
 <span data-ttu-id="34a4a-115">[Sample: Convert an Appointment to a Recurring Appointment](sample-convert-appointment-recurring-appointment.md) </span><span class="sxs-lookup"><span data-stu-id="34a4a-115">[Sample: Convert an Appointment to a Recurring Appointment](sample-convert-appointment-recurring-appointment.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>
