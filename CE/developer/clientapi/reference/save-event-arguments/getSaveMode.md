---
title: getSaveMode (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: 7a4a46d1257d42803801412ee832b4faa40d0867
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387365"
---
# <a name="getsavemode-client-api-reference"></a>getSaveMode (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getSaveMode-description.md](./includes/getSaveMode-description.md)]

## <a name="syntax"></a>Cú pháp

`executionContext.getEventArgs().getSaveMode()`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Number

**Description**: The following table describes the supported values returned to detect different ways entity records may be saved by the user.

|Value |Save mode |Thực thể|
|---|---|---|
|1|Lưu|Tất cả|
|2|Lưu và Đóng|Tất cả|
|5|Dừng kích hoạt|Tất cả|
|6|Reactivate|Tất cả|
|7|Gửi|Email|
|15|Disqualify|Khách hàng tiềm năng|
|16|Bao gồm|Khách hàng tiềm năng|
|47|Chỉ định|User or Team owned entities|
|58|Save as Completed|Hoạt động|
|59|Save and New|Tất cả|
|70|Auto Save|Tất cả|

## <a name="remarks"></a>Chú thích

This method is essential if you want to enable auto-save for most forms in an organization but disable it for specific forms.  

## <a name="example"></a>Ví dụ

The following code registered for the **OnSave** event with the execution context passed to it will prevent any saves that initiate from an auto-save but allow all others. With auto-save enabled, navigating away is equivalent to **Save and Close**. This code will prevent any saves that are initiated by the 30 second timer or when people navigate away from a form with unsaved data.

```JavaScript
function preventAutoSave(executionContext) {
    var eventArgs = executionContext.getEventArgs();
    if (eventArgs.getSaveMode() == 70 || eventArgs.getSaveMode() == 2) {
        eventArgs.preventDefault();
    }
}
```

To save a record the user must click the **Save** icon at the bottom of the form or a custom **Save** command needs to be added to the command bar.

### <a name="related-topics"></a>Chủ đề liên quan

[isDefaultPrevented](isDefaultPrevented.md)

[preventDefault](preventDefault.md)

