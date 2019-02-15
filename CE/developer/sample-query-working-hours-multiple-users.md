---
title: 'Sample: Query the working hours of multiple users (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: Sample demonstrates how to retrieve the working hours of multiple users by using the QueryMultipleSchedulesRequest message.
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
- sample for querying the schedules of multiple users
- schedule and appointment entities
- querying the schedules of multiple users sample, schedule and appointment entities samples
ms.assetid: 68c9d5d9-ab69-4b6f-9f84-a1d5919d549e
caps.latest.revision: 26
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e11f43aa1deaacb30af192c12c51ce4e1afff433
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388777"
---
# <a name="sample-query-the-working-hours-of-multiple-users"></a><span data-ttu-id="1a44a-103">Sample: Query the working hours of multiple users</span><span class="sxs-lookup"><span data-stu-id="1a44a-103">Sample: Query the working hours of multiple users</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="1a44a-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="1a44a-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="1a44a-105">Download the complete sample from [Sample: Work with Schedules and Appointments](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).</span><span class="sxs-lookup"><span data-stu-id="1a44a-105">Download the complete sample from [Sample: Work with Schedules and Appointments](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="1a44a-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="1a44a-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="1a44a-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="1a44a-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="1a44a-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="1a44a-108">Demonstrates</span></span>  
 <span data-ttu-id="1a44a-109">This sample shows how to retrieve the working hours of multiple users by using the <xref:Microsoft.Crm.Sdk.Messages.QueryMultipleSchedulesRequest> message.</span><span class="sxs-lookup"><span data-stu-id="1a44a-109">This sample shows how to retrieve the working hours of multiple users by using the <xref:Microsoft.Crm.Sdk.Messages.QueryMultipleSchedulesRequest> message.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1a44a-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="1a44a-110">Example</span></span>  
 [!code-csharp[ScheduleAndAppointment#QueryWorkingHoursOfMultipleUsers](../snippets/csharp/CRMV8/scheduleandappointment/cs/queryworkinghoursofmultipleusers.cs#queryworkinghoursofmultipleusers)]  
  
### <a name="see-also"></a><span data-ttu-id="1a44a-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1a44a-111">See also</span></span>  
 <span data-ttu-id="1a44a-112">[Schedules in Dynamics 365 for Customer Engagement apps](schedule-collections.md) </span><span class="sxs-lookup"><span data-stu-id="1a44a-112">[Schedules in Dynamics 365 for Customer Engagement apps](schedule-collections.md) </span></span>  
 <span data-ttu-id="1a44a-113">[Sample Code for Schedule and Appointment Entities](sample-code-schedule-appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="1a44a-113">[Sample Code for Schedule and Appointment Entities](sample-code-schedule-appointment-entities.md) </span></span>  
 <span data-ttu-id="1a44a-114">[Sample: Book an Appointment](sample-book-appointment.md) </span><span class="sxs-lookup"><span data-stu-id="1a44a-114">[Sample: Book an Appointment](sample-book-appointment.md) </span></span>  
 <span data-ttu-id="1a44a-115">[Resource Entities](resource-entities.md) </span><span class="sxs-lookup"><span data-stu-id="1a44a-115">[Resource Entities](resource-entities.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.QueryMultipleSchedulesRequest>   
 [<span data-ttu-id="1a44a-116">Sample: CrmServiceHelper Class</span><span class="sxs-lookup"><span data-stu-id="1a44a-116">Sample: CrmServiceHelper Class</span></span>](org-service/helper-code-serverconnection-class.md)
