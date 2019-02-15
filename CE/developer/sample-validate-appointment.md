---
title: 'Sample: Validate an appointment (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: Sample demonstrates how to validate an appointment using the ValidateRequest message.
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
- sample for validating appointments
- validating appointments sample, schedule and appointment entities samples
ms.assetid: f88ba768-78f1-4fe8-9c72-59e72249f090
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9ff3244b4331decdf5d80eb46619ea528775a33e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386196"
---
# <a name="sample-validate-an-appointment"></a><span data-ttu-id="19065-103">Sample: Validate an appointment</span><span class="sxs-lookup"><span data-stu-id="19065-103">Sample: Validate an appointment</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="19065-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="19065-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="19065-105">Download the complete sample from [Sample: Work with Schedules and Appointments](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).</span><span class="sxs-lookup"><span data-stu-id="19065-105">Download the complete sample from [Sample: Work with Schedules and Appointments](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="19065-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="19065-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="19065-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="19065-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="19065-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="19065-108">Demonstrates</span></span>  
 <span data-ttu-id="19065-109">This sample shows how to validate an appointment using the <xref:Microsoft.Crm.Sdk.Messages.ValidateRequest> message.</span><span class="sxs-lookup"><span data-stu-id="19065-109">This sample shows how to validate an appointment using the <xref:Microsoft.Crm.Sdk.Messages.ValidateRequest> message.</span></span>  
  
## <a name="example"></a><span data-ttu-id="19065-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="19065-110">Example</span></span>  
 [!code-csharp[ScheduleAndAppointment#Validate](../snippets/csharp/CRMV8/scheduleandappointment/cs/validate.cs#validate)]  
  
### <a name="see-also"></a><span data-ttu-id="19065-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="19065-111">See also</span></span>  
 <span data-ttu-id="19065-112">[Sample Code for Schedule and Appointment Entities](sample-code-schedule-appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="19065-112">[Sample Code for Schedule and Appointment Entities](sample-code-schedule-appointment-entities.md) </span></span>  
 <span data-ttu-id="19065-113">[Sample: Create, Retrieve, Update, and Delete a Recurring Appointment](sample-create-retrieve-update-delete-recurring-appointment.md) </span><span class="sxs-lookup"><span data-stu-id="19065-113">[Sample: Create, Retrieve, Update, and Delete a Recurring Appointment](sample-create-retrieve-update-delete-recurring-appointment.md) </span></span>  
 <span data-ttu-id="19065-114">[Appointment Entities](appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="19065-114">[Appointment Entities](appointment-entities.md) </span></span>  
 <span data-ttu-id="19065-115">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="19065-115">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.ValidateRequest>
