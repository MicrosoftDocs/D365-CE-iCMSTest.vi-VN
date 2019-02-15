---
title: removeOnLoad (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/03/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 0b97afc4-1208-4c1b-8599-424d594ea69f
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e1e6924ba2651c04ce310fb9f09630746b736b6a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388665"
---
# <a name="removeonload-client-api-reference"></a>removeOnLoad (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/removeOnLoad-description.md](./includes/removeOnLoad-description.md)]

> [!NOTE]
> This method is supported only on Unified Interface.

## <a name="syntax"></a>Cú pháp

`formContext.ui.removeOnLoad(myFunction)`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|myFunction|function reference|Có|The function to be removed from the form [OnLoad](../events/form-onload.md) event.

### <a name="related-topics"></a>Chủ đề liên quan

[addOnLoad](addOnLoad.md)

[Form data OnLoad event](../events/form-onload.md)

[formContext.ui](../formContext-ui.md)

[formContext](../../clientapi-form-context.md)

