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
# <a name="sample-end-a-recurring-appointment-series"></a>Sample: End a recurring appointment series

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample from [Sample: Work with Schedules and Appointments](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0). 

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 The following sample shows how to end a recurring appointment series by using the <xref:Microsoft.Crm.Sdk.Messages.DeleteOpenInstancesRequest> message.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[ScheduleAndAppointment#EndRecurringAppointmentSeries](../snippets/csharp/CRMV8/scheduleandappointment/cs/endrecurringappointmentseries.cs#endrecurringappointmentseries)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md)   
 [Delete or End a Recurring Appointment Series or Instance](delete-or-end-a-recurring-appointment-series-or-instance.md)   
 <xref:Microsoft.Crm.Sdk.Messages.DeleteOpenInstancesRequest>   
 [Sample Code for Recurring Appointments](sample-code-schedule-appointment-entities.md)   
 [Sample: Convert an Appointment to a Recurring Appointment](sample-convert-appointment-recurring-appointment.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>
