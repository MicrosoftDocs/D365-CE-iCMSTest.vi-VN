---
title: openUrl (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 29cb3685-21aa-42fc-8e84-0074dcc69197
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6b9436e9148bd815c77dafaafce6817e2310c8f0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387030"
---
# <a name="openurl-client-api-reference"></a>openUrl (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/openUrl-description.md](./includes/openUrl-description.md)]

## <a name="syntax"></a>Cú pháp

`Xrm.Navigation.openUrl(url,openUrlOptions)`

## <a name="parameters"></a>Tham số

|Tên |Loại |Bắt buộc |Mô tả |
|---|---|---|---|
|url|Chuỗi|Có|URL to open.|
|openUrlOptions|Đối tượng|Không|Options to open the URL.The object contains the following attributes:<br/>- **height**: (Optional) Number. Height of the window to display the resultant page in pixels.<br/>- **width**: (Optional) Number. Width of the window to display the resultant page in pixels.|

## <a name="remarks"></a>Chú thích

This method is especially helpful for mobile clients to open a URL in a browser outside of shim.

 ### <a name="related-topics"></a>Chủ đề liên quan

[Xrm.Navigation](../xrm-navigation.md)

