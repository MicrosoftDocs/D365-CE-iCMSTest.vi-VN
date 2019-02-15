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
# <a name="sample-send-bulk-email-and-monitor-results"></a>Sample: Send bulk email and monitor results

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample from [Sample: Work with Activity entities](https://code.msdn.microsoft.com/Activities-Samples-61bf7504).  

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to send bulk email using the <xref:Microsoft.Crm.Sdk.Messages.SendBulkMailRequest> and monitor the results by retrieving records from the `AsyncOperation` entity.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Activities#SendBulkEmailAndMonitor](../snippets/csharp/CRMV8/activities/cs/sendbulkemailandmonitor.cs#sendbulkemailandmonitor)]  
  
### <a name="see-also"></a>Xem thêm  
 [Email (E-mail) Activity Entities](email-activity-entities.md)   
 [Sample Code for Activity Entities](sample-code-activity-entities.md)   
 <xref:Microsoft.Crm.Sdk.Messages.SendBulkMailRequest>
