---
title: GridRowData (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 8139c622-e4d9-478f-9510-414d140e5556
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c038f8199f4ec6aac3da12f49ac9b5790d315668
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386659"
---
# <a name="gridrowdata-client-api-reference"></a>GridRowData (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

GridRowData is returned by the [GridRow](gridrow.md).[getData](gridrow/getData.md) method.

GridRowData also provides methods for retrieving information specific to a record displayed in an editable grid row, including a collection of all the attributes included in the row. Attribute data is limited to the columns presented by the editable grid. See [Collections (Client API reference)](../collections.md) for information on the methods available to access data in a collection.

```JavaScript
var myRows = gridContext.getGrid().getRows();
var myRow = myRows.get(arg);
var gridRowData = myRow.getData();
```

## <a name="properties"></a>Thuộc tính

|Tên|Mô tả|Có sẵn cho|
|--|--|--|
|thực thể|Returns the [GridEntity](gridentity.md) for the GridRowData.|Read-only and editable grids|


## <a name="methods"></a>Phương pháp

|                 Tên                  |                                               Mô tả                                                |        Có sẵn cho         |
|---------------------------------------|----------------------------------------------------------------------------------------------------------|------------------------------|
| [getEntity](gridrowdata/getEntity.md) | [!INCLUDE[gridrowdata/includes/getEntity-description.md](gridrowdata/includes/getEntity-description.md)] | Read-only and editable grids |

