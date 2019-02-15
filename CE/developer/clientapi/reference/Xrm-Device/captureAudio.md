---
title: captureAudio| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: fa39d18e-4b82-423a-84a0-e54450b7964e
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b709b90159c7108946f788c54bf5bb0dfee10a3f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388193"
---
# <a name="captureaudio-client-api-reference"></a>captureAudio (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/captureAudio-description.md](./includes/captureAudio-description.md)]


## <a name="syntax"></a>Cú pháp

`Xrm.Device.captureAudio().then(successCallback, errorCallback)`

## <a name="parameters"></a>Tham số

| Parameter Name        | Loại           | Bắt buộc  |Mô tả  |
| ------------- |-------------| -----|-----|
|successCallback |Hàm | Có|A function to call when audio is returned. A base64 encoded audio object with the following attributes is passed to the function:<br/>- **fileContent**: Contents of the audio file. Chuỗi <br/>- **fileName**: Name of the audio file. String.<br/>- **fileSize**: Size of the audio file in KB. Số.<br/>- **mimeType**: Audio file MIME type. String.|
|errorCallback |Hàm | Có|A function to call when the operation fails. |
 

## <a name="return-value"></a>Giá trị trả lại
On success, returns a base64 encoded audio object with the attributes specified earlier.

## <a name="remarks"></a>Chú thích
This method is supported only for the mobile clients.

### <a name="related-topics"></a>Chủ đề liên quan
[Xrm.Device](../xrm-device.md)

