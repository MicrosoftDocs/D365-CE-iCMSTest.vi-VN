---
title: setShowTime (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 77999c82-3d6a-4db9-af9c-7322491768d9
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: de36617554983334018cf87a0ad054508221085e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386342"
---
# <a name="setshowtime-client-api-reference"></a>setShowTime (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Specify whether a date control should show the time portion of the date. 

## <a name="control-types-supported"></a>Control types supported

standard control for **datetime** attributes.

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).setShowTime(bool);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|bool|Boolean|Có|Specify true to show the time portion of the date; false otherwise.|

## <a name="remarks"></a>Chú thích

This method will show or hide the time component of a date control where the attribute uses the **DateAndTime** format. This method will have no effect when the **DateOnly** format is used.

### <a name="related-topics"></a>Chủ đề liên quan

[getShowTime](getShowTime.md)

