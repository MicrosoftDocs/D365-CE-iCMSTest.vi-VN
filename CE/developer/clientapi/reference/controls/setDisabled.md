---
title: setDisabled (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 86383cb1-c4c8-4e82-9f60-1dc4588b519d
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9b4f7d8a23631211d4bb08ffd80799d0b3df61c9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388440"
---
# <a name="setdisabled-client-api-reference"></a>setDisabled (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Sets whether the control is disabled.

## <a name="control-types-supported"></a>Control types supported

All except **kbsearch** control type

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).setDisabled(bool);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|bool|Boolean|Có|Specify **true** or **false** to disable or enable the control.|

### <a name="related-topics"></a>Chủ đề liên quan

[getDisabled](getDisabled.md)



