---
title: addTabStateChange (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 51b0dbf3-28bd-4eea-9ee9-50b322e9af9b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b069e0199f9dccd9a7613d9feada7b2b76b7bb1a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387744"
---
# <a name="addtabstatechange-client-api-reference"></a>addTabStateChange (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/addTabStateChange-description.md](./includes/addTabStateChange-description.md)].

## <a name="syntax"></a>Cú pháp

`tabObj.addTabStateChange(myFunction);` 

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|myFunction|function reference|Có|The function to be executed on the [TabStateChange](../events/tabstatechange.md) event. The function will be added to the bottom of the event handler pipeline. The execution context is automatically passed as the first parameter to the function. See [Execution context](../../clientapi-execution-context.md) for more information.|

### <a name="related-topics"></a>Chủ đề liên quan

[formContext.ui](../formContext-ui.md)

[formContext](../../clientapi-form-context.md)


