---
title: GridRow (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 02fef0b4-b895-4277-b604-3f525c29dca3
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4158f171a06cfee463a1a1d7c52a692262370d17
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386993"
---
# <a name="gridrow-client-api-reference"></a>GridRow (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

A collection of GridRow is returned by [Grid](grid.md).[getRows](grid/getRows.md) and [Grid](grid.md).[getSelectedRows](grid/getSelectedRows.md) methods.

```JavaScript
var myRows = gridContext.getGrid().getRows();
var gridRow = myRows.get(arg);
```

## <a name="properties"></a>Thuộc tính

|Tên|Mô tả|Có sẵn cho|
|--|--|--|
|dữ liệu|A collection containing the [GridRowData](gridrowdata.md) for the GridRow. See [Collections (Client API reference)](../collections.md) for information on the methods available for accessing data in a collection.|Read-only and editable grids|


## <a name="methods"></a>Phương pháp

|             Tên              |                                         Mô tả                                          |        Có sẵn cho         |
|-------------------------------|----------------------------------------------------------------------------------------------|------------------------------|
| [getData](gridrow/getData.md) | [!INCLUDE[gridrow/includes/getData-description.md](gridrow/includes/getData-description.md)] | Read-only and editable grids |

### <a name="related-topics"></a>Chủ đề liên quan

[GridRowData](gridrowdata.md)

[Grids and subgrids in Customer Engagement](../grids.md)


