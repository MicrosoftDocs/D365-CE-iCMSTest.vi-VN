---
title: 'Sample: Link custom attributes between series and instances (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: 'Sample demonstrates how to link a custom attribute that is created for a recurring appointment series (RecurringAppointmentMaster) with a custom attribute that is created for the Appointment instances. '
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
- linking custom attributes between series and instances sample, schedule and appointment entities samples
- sample for linking custom attributes between series and instances
- schedule and appointment entities
ms.assetid: 4a82ca6c-70eb-4587-9e5e-8d077e935c3d
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b7cd907d55b97c4ca602c999d17ee4d4b0d8e0b5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387002"
---
# <a name="sample-link-custom-attributes-between-series-and-instances"></a>Sample: Link custom attributes between series and instances

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample from [Sample: Work with Schedules and Appointments](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to link a custom attribute that is created for a recurring appointment series (`RecurringAppointmentMaster`) with a custom attribute that is created for the appointment instances (`Appointment`).  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[ScheduleAndAppointment#LinkCustomAttributesBetweenSeriesandInstances](../snippets/csharp/CRMV8/scheduleandappointment/cs/linkcustomattributesbetweenseriesandinstances.cs#linkcustomattributesbetweenseriesandinstances)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md)   
 [Link Custom Attributes between Series and Instances](link-custom-attributes-recurring-master-appointment-entities.md)   
 [Sample Code for Recurring Appointments](sample-code-schedule-appointment-entities.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>
