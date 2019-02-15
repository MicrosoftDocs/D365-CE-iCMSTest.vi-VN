---
title: getSelectedRows (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 49f39f0f-33ef-41d1-9ab3-14966ae075b5
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4df882571226b3b09aa53bcfb6bf505661e969b7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388147"
---
# <a name="getselectedrows-client-api-reference"></a>getSelectedRows (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getSelectedRows-description.md](./includes/getSelectedRows-description.md)]

## <a name="grid-types-supported"></a>Grid types supported

Read-only and editable grids

## <a name="syntax"></a>Cú pháp

`var allSelectedRows = gridContext.getGrid().getSelectedRows();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Collection

**Description**: A collection of selected rows in the grid.

## <a name="remarks"></a>Chú thích

To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).

See [Collections (Client API reference)](../../collections.md) for information on the methods available to access data in a collection.

