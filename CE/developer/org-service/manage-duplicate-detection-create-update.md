---
title: Manage duplicate detection for create and update operations using Organization Service (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Read how to detect duplicates during create and update operations using the Dynamics 365 for Customer Engagement Organization service.
ms.custom: ''
ms.date: 11/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- duplicate detection, organization service
ms.assetid: A69EDF59-3E81-4C6E-A5C9-EF8DCCF6F936
caps.latest.revision: 25
author: SushantSikka
ms.author: susikka
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: de04767889d605e7fea7c62685aeb11ed5ebd527
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387031"
---
# <a name="manage-duplicate-detection-for-create-and-update-operations-using-organization-service"></a>Manage duplicate detection for create and update operations using Organization Service

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

Dynamics 365 for Customer Engagement Web API allows you to detect duplicate records of an existing record in order to maintain integrity of data. 

Use `SuppressDuplicateDetection` parameter and set its value to `false` to activate duplicate detection and prohibit creation of a duplicate record during create and update operations.

The example shown below illustrates how to create a duplicate record by suppressing duplicate detection. Change the value of `SuppressDuplicateDetection` parameter to `false` to prohibit creation of a duplicate record.

[!code-csharp[DuplicateDetection#DuplicateDetectionCreate](../../snippets/csharp/CRMV8/duplicatedetection/cs/duplicatedetectioncreate.cs#duplicatedetectioncreate)]

Find the complete code sample, see [Sample: Use duplicate detection when creating and updating records](sample-use-duplicate-detection-when-creating-and-updating-records.md).

### <a name="see-also"></a>Xem thêm

[Detect duplicate data for developers](../detect-duplicate-data-for-developers.md)  
[Run duplicate detection](../run-duplicate-detection.md)  
[Sample: Use duplicate detection when creating and updating records](sample-use-duplicate-detection-when-creating-and-updating-records.md)  
[Sample: Enable duplicate detection and retrieve duplicates](sample-enable-duplicate-detection-and-retrieve-duplicates.md)
