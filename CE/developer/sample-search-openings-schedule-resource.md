---
title: 'Sample: Search for openings to schedule a resource (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: Sample demonstrates how to find openings to schedule a resource by using the SearchRequest message.
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
- sample for scheduling resources
- scheduling resources sample, schedule and appointment entities samples
- schedule and appointment entities
ms.assetid: 4c6ac2c8-6765-4a65-b1e0-e05a8d335abe
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: bf2b5b3ab02a41774d7295ea0e11f7b9e5c47169
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388149"
---
# <a name="sample-search-for-openings-to-schedule-a-resource"></a>Sample: Search for openings to schedule a resource

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. [Download the Schedule and Appointment samples](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).  

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 The following code example shows how to find openings to schedule a resource by using the <xref:Microsoft.Crm.Sdk.Messages.SearchRequest> message.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[ScheduleAndAppointment#ScheduleResource](../snippets/csharp/CRMV8/scheduleandappointment/cs/scheduleresource.cs#scheduleresource)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample Code for Schedule and Appointment Entities](sample-code-schedule-appointment-entities.md)   
 [Sample: Query the Working Hours of a User](sample-query-working-hours-user.md)   
 [Resource Entities](resource-entities.md)   
 [Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.SearchRequest>
