---
title: captureImage | MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 1b24e8b2-20af-4e75-8c00-1aa393c07aef
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 98596bf2bd62820b45b7f005a3ab230c04eaff07
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388276"
---
# <a name="captureimage-client-api-reference"></a>captureImage (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/captureImage-description.md](./includes/captureImage-description.md)]


## <a name="syntax"></a>Cú pháp

`Xrm.Device.captureImage(imageOptions).then(successCallback, errorCallback)`

## <a name="parameters"></a>Tham số

| Parameter Name        | Loại           | Bắt buộc  |Mô tả  |
| ------------- |-------------| -----|-----|
|imageOptions |Đối tượng | Không|An object with the following attributes:<br/>- **allowEdit**: Indicates whether to edit the image before saving. Boolean.<br/>- **height**: Height of the image to capture. Số.<br/>- **preferFrontCamera**: Indicates whether to capture image using the front camera of the device. Boolean.<br/>- **quality**: Quality of the image file in percentage. Số.<br/>- **width**: Width of the image to capture. Number..|
|successCallback |Hàm | Có|A function to call when image is returned. A base64 encoded image object with the following attributes is passed to the function:<br/>- **fileContent**: Contents of the image file. Chuỗi <br/>- **fileName**: Name of the image file. String.<br/>- **fileSize**: Size of the image file in KB. Số.<br/>- **mimeType**: Image file MIME type. String.|
|errorCallback |Hàm | Có|A function to call when the operation fails. |
 

## <a name="return-value"></a>Giá trị trả lại
On success, returns a base64 encoded image object with the attributes specified earlier.

## <a name="remarks"></a>Chú thích
This method is supported only for the mobile clients.

### <a name="related-topics"></a>Chủ đề liên quan
[Xrm.Device](../xrm-device.md)

