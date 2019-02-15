---
title: captureVideo| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9580d05a-a91f-4126-b94b-4d1068da35fa
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 184db5b218492ad8a80b68e1abae5685f4eae3a2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387021"
---
# <a name="capturevideo-client-api-reference"></a>captureVideo (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/captureVideo-description.md](./includes/captureVideo-description.md)]


## <a name="syntax"></a>Cú pháp

`Xrm.Device.captureVideo().then(successCallback, errorCallback)`

## <a name="parameters"></a>Tham số

| Parameter Name        | Loại           | Bắt buộc  |Mô tả  |
| ------------- |-------------| -----|-----|
|successCallback |Hàm | Có|A function to call when Video is returned. A base64 encoded Video object with the following attributes is passed to the function:<br/>- **fileContent**: Contents of the Video file. Chuỗi <br/>- **fileName**: Name of the Video file. String.<br/>- **fileSize**: Size of the Video file in KB. Số.<br/>- **mimeType**: Video file MIME type. String.|
|errorCallback |Hàm | Có|A function to call when the operation fails. |
 

## <a name="return-value"></a>Giá trị trả lại
On success, returns a base64 encoded Video object with the attributes specified earlier.

## <a name="remarks"></a>Chú thích
This method is supported only for the mobile clients.

### <a name="related-topics"></a>Chủ đề liên quan
[Xrm.Device](../xrm-device.md)

