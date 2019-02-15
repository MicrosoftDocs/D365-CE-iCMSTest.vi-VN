---
title: addOption (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9798f168-7b94-411d-9aed-6471042ff11a
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: af34fb6c2ac184b24dcdebc2975897fa76392229
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388465"
---
# <a name="addoption-client-api-reference"></a>addOption (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Adds an option to a control. 

## <a name="control-types-supported"></a>Control types supported

OptionSet, MultiSelectOptionSet

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).addOption(option, index);`

## <a name="parameters"></a>Tham số

|Tên | Loại | Bắt buộc | Mô tả|
|--|--|--|--|
|option |Đối tượng |Có|The option to add. The object contains the following attributes:<br/>**- text**: String. The label for the option.<br/>**- value**: Number. The value for the option.|
|chỉ mục |Số |Không|The index position to place the new option in. If not provided, the option will be added to the end.|

### <a name="related-topics"></a>Chủ đề liên quan

[clearOptions](clearOptions.md)

[removeOption](removeOption.md)
