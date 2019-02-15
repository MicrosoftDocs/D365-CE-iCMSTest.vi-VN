---
title: addOnRecordSelect (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4bfd7f48-5db8-45ea-816f-9d590fbdf60d
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4fa8c0f1c61615c0cbed7cfda37a6c8104cf085a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387242"
---
# <a name="addonrecordselect-client-api-reference"></a>addOnRecordSelect (Client API reference)

[!INCLUDE[./includes/addOnRecordSelect-description.md](./includes/addOnRecordSelect-description.md)]

## <a name="grid-types-supported"></a>Grid types supported

Read-only and editable grids

## <a name="syntax"></a>Cú pháp

`gridContext.getGrid().addOnRecordSelect(myFunction);`

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|myFunction|function reference|Có|The function to be executed when you select record (row) in a grid. The function will be added to the bottom of the event handler pipeline. The execution context is automatically passed as the first parameter to the function. See [execution context](../../../clientapi-execution-context.md) for more information.

## <a name="remarks"></a>Chú thích

To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).

