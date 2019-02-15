---
title: refresh (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 03e970ee-7ed3-4df2-9670-222d76a479fd
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3ea5a6aaf3f4f317d2a345e99538ce14b8e6b99c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385484"
---
# <a name="refresh-client-api-reference"></a>refresh (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/refresh-description.md](./includes/refresh-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.data.refresh(save).then(successCallback, errorCallback);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|save|Boolean|Không|true if the data should be saved after it is refreshed, otherwise false.|
|successCallback|Hàm|Không|A function to call when the operation succeeds.|
|errorCallback|Hàm|Không|A function to call when the operation fails.|

### <a name="related-topics"></a>Chủ đề liên quan

[formContext](../../clientapi-form-context.md)

