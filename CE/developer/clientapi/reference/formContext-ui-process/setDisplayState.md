---
title: setDisplayState (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 21368fac-d4bc-4f75-8a9c-cce098fa0b45
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f90e065ff3b7cc54ed6bbf450c60290485a6e08c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387818"
---
# <a name="setdisplaystate-client-api-reference"></a>setDisplayState (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setDisplayState-description.md](./includes/setDisplayState-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.ui.process.setDisplayState(state);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|state|Chuỗi|Có|Specify "expanded", "collapsed", or "floating". The value "floating" is not supported on the web client.|

### <a name="related-topics"></a>Chủ đề liên quan

[getDisplayState](getDisplayState.md)

[formContext.ui.process](../formContext-ui-process.md)



