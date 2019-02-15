---
title: openAlertDialog (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 8615a284-41b4-479c-81bd-577b3b7c79ad
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 338b064b8a046d13a1c84ef6eeff8e0bf2d88083
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385565"
---
# <a name="openalertdialog-client-api-reference"></a>openAlertDialog (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/openAlertDialog-description.md](./includes/openAlertDialog-description.md)]

## <a name="syntax"></a>Cú pháp

`Xrm.Navigation.openAlertDialog(alertStrings,alertOptions).then(closeCallback,errorCallback);`

## <a name="parameters"></a>Tham số

|Tên |Loại |Bắt buộc |Mô tả |
|---|---|---|---|
|alertStrings|Đối tượng|Có|The strings to be used in the alert dialog. The object contains the following attributes:<br/>- **confirmButtonLabel**: (Optional) String. The confirm button label. If you do not specify the button label, **OK** is used as the button label.<br/>- **text**: String. The message to be displyed in the alert dialog.|
|alertOptions|Đối tượng|Không|The height and width options for alert dialog. The object contains the following attributes:<br/>- **height**: (Optional) Number. Height of the alert dialog in pixels.<br/>- **width**: (Optional) Number. Width of the alert dialog pixels.|
|successCallback|function|Không|A function to execute when the alert dialog is closed by either clicking the confirm button or canceled by pressing ESC.|
|errorCallback|function|Không|A function to execute when the operation fails.|


## <a name="example"></a>Ví dụ

The following sample code displays an alert dialog. Clicking **Yes** button in the alert dialog or canceling the alert dialog by pressing ESC calls the `close` function::

```JavaScript
var alertStrings = { confirmButtonLabel: "Yes", text: "This is an alert." };
var alertOptions = { height: 120, width: 260 };
Xrm.Navigation.openAlertDialog(alertStrings, alertOptions).then(
    function success(result) {
        console.log("Alert dialog closed");
    },
    function (error) {
        console.log(error.message);
    }
);
```

### <a name="related-topics"></a>Chủ đề liên quan

[Xrm.navigation](../xrm-navigation.md)

