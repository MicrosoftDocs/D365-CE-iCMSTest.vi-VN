---
title: getBarcodeValue| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 0218b96c-2809-4f2d-9f9f-d8ee8f8e3b7b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 17ec172e7aa3ba3ac5ef897c49375581d3dbcefa
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386218"
---
# <a name="getbarcodevalue-client-api-reference"></a>getBarcodeValue (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getBarcodeValue-description.md](./includes/getBarcodeValue-description.md)]


## <a name="syntax"></a>Cú pháp

`Xrm.Device.getBarcodeValue().then(successCallback, errorCallback)`

## <a name="parameters"></a>Tham số

| Parameter Name        | Loại           | Bắt buộc  |Mô tả  |
| ------------- |-------------| -----|-----|
|successCallback |Hàm | Có|A function to call when the barcode value is returned as a String.|
|errorCallback |Hàm | Có|A function to call when the operation fails. An error object with the **message** property (String) will be passed that describes the error details.|
 

## <a name="return-value"></a>Giá trị trả lại
On success, returns a string containing the scanned barcode value.

## <a name="remarks"></a>Chú thích
This method is supported only for the mobile clients.

## <a name="example"></a>Ví dụ

```JavaScript
Xrm.Device.getBarcodeValue().then(
    function success(result) {
        Xrm.Navigation.openAlertDialog({ text: "Barcode value: " + result });
    },
    function (error) {
        Xrm.Navigation.openAlertDialog( {text: error.message} );
    }
);
``` 

### <a name="related-topics"></a>Chủ đề liên quan
[Xrm.Device](../xrm-device.md)

