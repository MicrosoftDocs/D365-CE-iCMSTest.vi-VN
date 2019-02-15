---
title: 'Sample: Book an appointment (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: Sample demonstrates how to book or schedule an appointment by using the BookRequest message.
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
- sample for booking appointments
- schedule and appointment entities
- booking appointments sample, schedule and appointment entities samples
ms.assetid: 56e6a047-88dd-4f9b-b211-e5fc878595a9
caps.latest.revision: 17
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7ee60d1837bb54c6a0654deb2199c219ae8a7475
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387882"
---
# <a name="sample-book-an-appointment"></a><span data-ttu-id="3453e-103">Sample: Book an appointment</span><span class="sxs-lookup"><span data-stu-id="3453e-103">Sample: Book an appointment</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3453e-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="3453e-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="3453e-105">Download the complete sample from [Sample: Work with Schedule and Appointment](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).</span><span class="sxs-lookup"><span data-stu-id="3453e-105">Download the complete sample from [Sample: Work with Schedule and Appointment](https://code.msdn.microsoft.com/Schedule-and-Appointment-93ed80c0).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="3453e-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="3453e-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="3453e-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="3453e-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="3453e-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="3453e-108">Demonstrates</span></span>  
 <span data-ttu-id="3453e-109">This sample shows how to book or schedule an appointment by using the <xref:Microsoft.Crm.Sdk.Messages.BookRequest> message.</span><span class="sxs-lookup"><span data-stu-id="3453e-109">This sample shows how to book or schedule an appointment by using the <xref:Microsoft.Crm.Sdk.Messages.BookRequest> message.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3453e-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="3453e-110">Example</span></span>  
 [!code-csharp[ScheduleAndAppointment#BookAppointment](../snippets/csharp/CRMV8/scheduleandappointment/cs/bookappointment.cs#bookappointment)]  
  
### <a name="see-also"></a><span data-ttu-id="3453e-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3453e-111">See also</span></span>  
 <span data-ttu-id="3453e-112">[Sample Code for Schedule and Appointment Entities](sample-code-schedule-appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="3453e-112">[Sample Code for Schedule and Appointment Entities](sample-code-schedule-appointment-entities.md) </span></span>  
 <span data-ttu-id="3453e-113">[Appointment Entities](appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="3453e-113">[Appointment Entities](appointment-entities.md) </span></span>  
 <span data-ttu-id="3453e-114">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="3453e-114">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.BookRequest>   
 [<span data-ttu-id="3453e-115">Sample: Validate an Appointment</span><span class="sxs-lookup"><span data-stu-id="3453e-115">Sample: Validate an Appointment</span></span>](sample-validate-appointment.md)
