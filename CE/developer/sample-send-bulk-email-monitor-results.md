---
title: 'Sample: Send bulk email and monitor results (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to send bulk email using the SendBulkMailRequest and monitor the results by retrieving records from the AsyncOperation entity
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1caed83f-a80f-4abe-8f03-b1c79cc84051
caps.latest.revision: 14
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4f6a895e8c5d344918fdceadbf5cd0b46282006d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386019"
---
# <a name="sample-send-bulk-email-and-monitor-results"></a><span data-ttu-id="75dff-103">Sample: Send bulk email and monitor results</span><span class="sxs-lookup"><span data-stu-id="75dff-103">Sample: Send bulk email and monitor results</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="75dff-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="75dff-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="75dff-105">Download the complete sample from [Sample: Work with Activity entities](https://code.msdn.microsoft.com/Activities-Samples-61bf7504).</span><span class="sxs-lookup"><span data-stu-id="75dff-105">Download the complete sample from [Sample: Work with Activity entities](https://code.msdn.microsoft.com/Activities-Samples-61bf7504).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="75dff-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="75dff-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="75dff-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="75dff-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="75dff-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="75dff-108">Demonstrates</span></span>  
 <span data-ttu-id="75dff-109">This sample shows how to send bulk email using the <xref:Microsoft.Crm.Sdk.Messages.SendBulkMailRequest> and monitor the results by retrieving records from the `AsyncOperation` entity.</span><span class="sxs-lookup"><span data-stu-id="75dff-109">This sample shows how to send bulk email using the <xref:Microsoft.Crm.Sdk.Messages.SendBulkMailRequest> and monitor the results by retrieving records from the `AsyncOperation` entity.</span></span>  
  
## <a name="example"></a><span data-ttu-id="75dff-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="75dff-110">Example</span></span>  
 [!code-csharp[Activities#SendBulkEmailAndMonitor](../snippets/csharp/CRMV8/activities/cs/sendbulkemailandmonitor.cs#sendbulkemailandmonitor)]  
  
### <a name="see-also"></a><span data-ttu-id="75dff-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="75dff-111">See also</span></span>  
 <span data-ttu-id="75dff-112">[Email (E-mail) Activity Entities](email-activity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="75dff-112">[Email (E-mail) Activity Entities](email-activity-entities.md) </span></span>  
 <span data-ttu-id="75dff-113">[Sample Code for Activity Entities](sample-code-activity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="75dff-113">[Sample Code for Activity Entities](sample-code-activity-entities.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.SendBulkMailRequest>
