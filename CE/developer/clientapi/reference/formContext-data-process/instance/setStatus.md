---
title: setStatus (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 649fe7b0-016d-409f-ba3c-b14e0f1953e0
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7f87ebcfb061391b879a0ba238ab60931b06a4d9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385652"
---
# <a name="setstatus-client-api-reference"></a>setStatus (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setStatus-description.md](./includes/setStatus-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.data.process.setStatus(status, callbackFunction);`

## <a name="parameters"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|status|Chuỗi|Có|The new status. The values can be **active**, **aborted**, or **finished**.|
|callbackFunction|Hàm|Không|A function to call when the operation is complete. This callback function is passed the new status as a string value.|

**Type**: String. 

**Description**:Returns one of the following values: **active**, **aborted**, or **finished**.

### <a name="related-topics"></a>Chủ đề liên quan

[formContext.data.process](../../formContext-data-process.md)
 


