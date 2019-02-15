---
title: 'Sample: Query the working hours of a user (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: Sample demonstrates how to retrieve the working hours of a user by using the QueryScheduleRequest message.
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
- sample for querying user schedules
- schedule and appointment entities
- querying user schedules sample, schedule and appointment entities samples
ms.assetid: 06211393-b9aa-4c4d-9730-7ec51ec1bd3f
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ea3d09dc7a4577dbcd2e5610e9511624219cbef7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388678"
---
# <a name="sample-query-the-working-hours-of-a-user"></a><span data-ttu-id="456cd-103">Sample: Query the working hours of a user</span><span class="sxs-lookup"><span data-stu-id="456cd-103">Sample: Query the working hours of a user</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="456cd-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="456cd-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="456cd-105">Download the complete sample from [Sample: Work with Schedules and Appointments](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).</span><span class="sxs-lookup"><span data-stu-id="456cd-105">Download the complete sample from [Sample: Work with Schedules and Appointments](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="456cd-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="456cd-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="456cd-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="456cd-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="456cd-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="456cd-108">Demonstrates</span></span>  
 <span data-ttu-id="456cd-109">This sample shows how to retrieve the working hours of a user by using the <xref:Microsoft.Crm.Sdk.Messages.QueryScheduleRequest> message.</span><span class="sxs-lookup"><span data-stu-id="456cd-109">This sample shows how to retrieve the working hours of a user by using the <xref:Microsoft.Crm.Sdk.Messages.QueryScheduleRequest> message.</span></span>  
  
## <a name="example"></a><span data-ttu-id="456cd-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="456cd-110">Example</span></span>  
 [!code-csharp[ScheduleAndAppointment#QueryWorkingHoursOfUser](../snippets/csharp/CRMV8/scheduleandappointment/cs/queryworkinghoursofuser.cs#queryworkinghoursofuser)]  
  
### <a name="see-also"></a><span data-ttu-id="456cd-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="456cd-111">See also</span></span>  
 <span data-ttu-id="456cd-112">[Schedules in Dynamics 365 for Customer Engagement](schedule-collections.md) </span><span class="sxs-lookup"><span data-stu-id="456cd-112">[Schedules in Dynamics 365 for Customer Engagement](schedule-collections.md) </span></span>  
 <span data-ttu-id="456cd-113">[Sample Code for Schedule and Appointment Entities](sample-code-schedule-appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="456cd-113">[Sample Code for Schedule and Appointment Entities](sample-code-schedule-appointment-entities.md) </span></span>  
 <span data-ttu-id="456cd-114">[Sample: Query the Working Hours of Multiple Users](sample-query-working-hours-multiple-users.md) </span><span class="sxs-lookup"><span data-stu-id="456cd-114">[Sample: Query the Working Hours of Multiple Users](sample-query-working-hours-multiple-users.md) </span></span>  
 <span data-ttu-id="456cd-115">[Resource Entities](resource-entities.md) </span><span class="sxs-lookup"><span data-stu-id="456cd-115">[Resource Entities](resource-entities.md) </span></span>  
 <span data-ttu-id="456cd-116">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="456cd-116">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.QueryScheduleRequest>
