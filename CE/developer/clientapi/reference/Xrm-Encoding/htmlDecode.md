---
title: htmlDecode| MicrosoftDocs
description: The Client API method converts a string that has been HTML-encoded into a decoded string.
ms.date: 05/09/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4ef7160b-ac01-4d08-8a98-f8e3012ef20b
author: KumarVivek
ms.author: kvivek
manager: kvivek
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a757e3ca5caec7c90e3c69a2060d103956de25d0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388627"
---
# <a name="htmldecode-client-api-reference"></a>htmlDecode (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/htmlDecode-description.md](./includes/htmlDecode-description.md)] 

## <a name="syntax"></a>Cú pháp

`Xrm.Encoding.htmlDecode(arg)`

## <a name="parameters"></a>Tham số

|Parameter Name        | Loại           | Bắt buộc  |Mô tả  |
| ------------- |-------------| -----|-----|
|arg        | Chuỗi           | Bắt buộc  |HTML-encoded string to be decoded.  |


## <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: Decoded string.

## <a name="related-topics"></a>Chủ đề liên quan

[htmlEncode](htmlEncode.md)

[htmlAttributeEncode](htmlAttributeEncode.md)
