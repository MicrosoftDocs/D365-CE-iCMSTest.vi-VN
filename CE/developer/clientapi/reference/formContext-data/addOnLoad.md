---
title: addOnLoad (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 03e970ee-7ed3-4df2-9670-222d76a479fd
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9c2a808237f8bb826e012911bcbbbbbe136b7941
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387681"
---
# <a name="addonload-client-api-reference"></a>addOnLoad (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/addOnLoad-description.md](./includes/addOnLoad-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.data.addOnLoad(myFunction)`

## <a name="parameter"></a>Tham số

|    Tên    |        Loại        | Bắt buộc |                                                                                                                                               Mô tả                                                                                                                                               |
|------------|--------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| myFunction | function reference |   Có    | The function to be executed when the form data loads. The function will be added to the bottom of the event handler pipeline. The execution context is automatically passed as the first parameter to the function. See [Execution context](../../clientapi-execution-context.md) for more information. |

### <a name="related-topics"></a>Chủ đề liên quan

[removeOnLoad](removeOnLoad.md)

[Form data OnLoad event](../events/form-data-onload.md)

