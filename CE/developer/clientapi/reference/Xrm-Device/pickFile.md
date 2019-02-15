---
title: pickFile| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: c777a0b8-2b07-458b-8a4f-8938f7a2e696
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7fec32127ec14b1ba2e74122ac252627e9b9f025
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385925"
---
# <a name="pickfile-client-api-reference"></a>pickFile (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/pickFile-description.md](./includes/pickFile-description.md)]


## <a name="syntax"></a>Cú pháp

`Xrm.Device.pickFile(pickFileOptions).then(successCallback, errorCallback)`

## <a name="parameters"></a>Tham số

| Parameter Name        | Loại           | Bắt buộc  |Mô tả  |
| ------------- |-------------| -----|-----|
|pickFileOptions |Đối tượng | Không|An object with the following attributes:<br/>- **accept**: Image file types to select. Valid values are "audio", "video", or "image". String.<br/>- **allowMultipleFiles**: Indicates whether to allow selecting multiple files. Boolean.<br/>- **maximumAllowedFileSize**: Maximum size of the files(s) to be selected. Số.|
|successCallback |Hàm | Có|A function to call when selected files are returned. An array of objects with *each* object having the following attributes is passed to the function:<br/>- **fileContent**: Contents of the file. Chuỗi <br/>- **fileName**: Name of the file. String.<br/>- **fileSize**: Size of the file in KB. Số.<br/>- **mimeType**: File MIME type. String.|
|errorCallback |Hàm | Có|A function to call when the operation fails. |
 

## <a name="return-value"></a>Giá trị trả lại
On success, returns a promise with array of objects as specified earlier for the **successCallback** function.

### <a name="related-topics"></a>Chủ đề liên quan
[Xrm.Device](../xrm-device.md)

