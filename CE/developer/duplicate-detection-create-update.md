---
title: Manage duplicate detection for create and update operations (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Read how to detect duplicates during create and update operations using the Dynamics 365 for Customer Engagement Web API and Organization service.
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
- duplicate detection, Web API, Organization Service
ms.assetid: 5B84D5F0-CFB6-4212-ACCB-03AE81271F1E
caps.latest.revision: 25
author: SushantSikka
ms.author: susikka
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 535031698f07a75832e6ceb79d9a953d829b728c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386199"
---
# <a name="manage-duplicate-detection-for-create-and-update-operations"></a>Manage duplicate detection for create and update operations

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

Dynamics 365 for Customer Engagement Web API allows you to detect duplicate records of an existing record in order to maintain integrity of data. 

<a name="BKMK_webapi"></a>

## <a name="using-web-api"></a>Using Web API

Use Preference header `MSCRM.SuppressDuplicateDetection` and set its value to `false` to detect creation of a duplicate record during Create and Update operations.

> [!NOTE]
>  Make sure there are appropriate duplicate detection rules in place. Dynamics 365 for Customer Engagement apps includes default duplicate detection rules for accounts, contacts, and leads, but not for other types of records. If you want the system to detect duplicates for other record types, you’ll need to create a new rule. For information on how to create a duplicate detection rule, see [Duplicate detection rules](../admin/set-up-duplicate-detection-rules-keep-data-clean.md).

For more information and examples on how to prohibit creation of duplicate records during create and update operations, see [Manage duplicate detection for create and update operations using Web API](webapi/manage-duplicate-detection-create-update.md).

<a name="BKMK_orgservice"></a>

## <a name="using-organization-service"></a>Using Organization Service

Use `SuppressDuplicateDetection` parameter and set its value to `false` to activate duplicate detection and prohibit creation of a duplicate record during create and update operations.

For more information and example on how to prohibit creation of duplicate records during create and update operations, see [Manage duplicate detection for create and update operations using Organization Service](org-service/manage-duplicate-detection-create-update.md).

### <a name="see-also"></a>Xem thêm

[Manage duplicate detection during Create and Update operation using Web API](webapi/manage-duplicate-detection-create-update.md)  
[Manage duplicate detection during Create and Update operation using Organization Service](org-service/manage-duplicate-detection-create-update.md)  
[Sample: Use duplicate detection when creating and updating records](org-service/sample-use-duplicate-detection-when-creating-and-updating-records.md)  
[Sample: Detect multiple duplicate records](org-service/sample-detect-multiple-duplicate-records.md)  
[Run duplicate detection](run-duplicate-detection.md)
