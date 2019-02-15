---
title: 'Sample: Detect multiple duplicate records (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: Sample demonstrates how to detect and log multiple duplicate records for a specified entity type.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 5c83c1c2-25ef-480b-9195-6eabe9f6c4c7
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 13
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 99536dde5ea28cf9ff2da4962f57a89ca8616cda
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387493"
---
# <a name="sample-detect-multiple-duplicate-records"></a>Sample: Detect multiple duplicate records

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for Dynamics 365 for Customer Engagement. Download the sample: [With with duplicate detections](https://code.msdn.microsoft.com/Work-with-duplicate-9c7d6f59).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to detect and log multiple duplicate records for a specified entity type.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[DuplicateDetection#BulkDetectDuplicates](../snippets/csharp/CRMV8/duplicatedetection/cs/bulkdetectduplicates.cs#bulkdetectduplicates)]  
  
### <a name="see-also"></a>Xem thêm  
 [Detect Duplicate Data in Dynamics 365 for Customer Engagement apps](detect-duplicate-data-for-developers.md)   
 [Enable and disable duplicate detection](enable-disable-duplicate-detection.md)   
 [Run Duplicate Detection](run-duplicate-detection.md)   
 <xref:Microsoft.Crm.Sdk.Messages.BulkDetectDuplicatesRequest>  
 [Duplicate detection messages](duplicate-detection-messages.md)
