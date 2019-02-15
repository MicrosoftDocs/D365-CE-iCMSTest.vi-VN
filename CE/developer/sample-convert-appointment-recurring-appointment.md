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
# <a name="sample-convert-an-appointment-to-a-recurring-appointment"></a>Sample: Convert an appointment to a recurring appointment

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. [Download the Schedule and Appointment samples](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to convert an appointment to a recurring appointment series by using the <xref:Microsoft.Crm.Sdk.Messages.AddRecurrenceRequest> message.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[ScheduleAndAppointment#ConvertAnAppointmenttoRecurringAppointment](../snippets/csharp/CRMV8/scheduleandappointment/cs/convertanappointmenttorecurringappointment.cs#convertanappointmenttorecurringappointment)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md)   
 [Convert an Appointment to a Recurring Appointment](create-recurring-appointment-series-instance-exception.md#bkmk_convert)   
 [Sample Code for Recurring Appointments](sample-code-schedule-appointment-entities.md)   
 [Sample: Link Custom Attributes between Series and Instances](sample-link-custom-attributes-between-series-instances.md)   
 <xref:Microsoft.Crm.Sdk.Messages.AddRecurrenceRequest>
