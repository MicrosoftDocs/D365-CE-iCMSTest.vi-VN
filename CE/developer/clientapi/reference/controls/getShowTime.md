---
title: getShowTime (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 43341b96-ca2c-4c7e-b6d5-fe7a5fd3c8b2
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2765f2391e25a5735a5ccd9b276e9122adfc6146
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385521"
---
# <a name="getshowtime-client-api-reference"></a>getShowTime (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Get whether a date control shows the time portion of the date. 

## <a name="control-types-supported"></a>Control types supported

standard control for **datetime** attributes.

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).getShowTime();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean

**Description**: true if shows the time portion of the date; false otherwise.

### <a name="related-topics"></a>Chủ đề liên quan

[setShowTime](setShowTime.md)

