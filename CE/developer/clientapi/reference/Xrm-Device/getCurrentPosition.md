---
title: getCurrentPosition | MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 062a52d8-170c-4e98-b48a-ac99ec759f83
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 512823952503699089c81c428cdea9c1adae0df1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388632"
---
# <a name="getcurrentposition-client-api-reference"></a>getCurrentPosition (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getCurrentPosition-description.md](./includes/getCurrentPosition-description.md)]


## <a name="syntax"></a>Cú pháp

`Xrm.Device.getCurrentPosition().then(successCallback, errorCallback)`

## <a name="parameters"></a>Tham số

| Parameter Name        | Loại           | Bắt buộc  |Mô tả  |
| ------------- |-------------| -----|-----|
|successCallback |Hàm | Có|A function to call when the current geolocation information is returned. A geolocation object with the following attributes is passed to the function.:<br/>- **coords**: Contains a set of geographic coordinates along with associated accuracy as well as a set of other optional attributes such as altitude and speed. <br/>- **timestamp**: Represents the time when the object was acquired and is represented as DOMTimeStamp.|
|errorCallback |Hàm | Có|A function to call when the operation fails. An object with the following properties will be passed: <br/>- **code**: The error code. Số. <br/>- **message**: RLocalized message describing the error details. String.<br/><br/>If the user location setting is not enabled on your mobile device, the error message indicates the same. If you are using an earlier version of the Dynamics 365 for Customer Engagement mobile client or if geolocation capability is not available on your mobile device, null is passed to the error callback.|
 

## <a name="return-value"></a>Giá trị trả lại
On success, returns a geolocation object with the attributes specified earlier in the **successCallback** function.

## <a name="remarks"></a>Chú thích
For the **getCurrentPosition** method to work, the geolocation capability must be enabled on your mobile device, and the Dynamics 365 for Customer Engagement mobile clients must have permissions to access the device location, which isn't enabled by default.

This method is supported only for the mobile clients.

## <a name="example"></a>Ví dụ

```JavaScript
Xrm.Device.getCurrentPosition().then(
    function success(location) {
        Xrm.Navigation.openAlertDialog({
            text: "Latitude: " + location.coords.latitude +
            ", Longitude: " + location.coords.longitude
        });
    },
    function (error) {
        Xrm.Navigation.openAlertDialog({ text: error.message });
    }
);
```

### <a name="related-topics"></a>Chủ đề liên quan
[Xrm.Device](../xrm-device.md)