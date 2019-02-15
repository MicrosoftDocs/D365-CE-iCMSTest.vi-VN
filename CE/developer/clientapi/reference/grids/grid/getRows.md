---
title: getRows (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4d025f92-db16-440c-9f82-e40d71e09862
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7536f18d002c18d3466f801807db5024f1636413
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388605"
---
# <a name="getrows-client-api-reference"></a>getRows (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getRows-description.md](./includes/getRows-description.md)]

## <a name="grid-types-supported"></a>Grid types supported

Read-only and editable grids

## <a name="syntax"></a>Cú pháp

`var allRows = gridContext.getGrid().getRows();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Collection

**Description**: A collection of rows in the grid.

## <a name="remarks"></a>Chú thích

To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).

See [Collections (Client API reference)](../../collections.md) for information on the methods available to access data in a collection.

