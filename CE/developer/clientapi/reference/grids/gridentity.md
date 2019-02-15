---
title: GridEntity (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: cc2b7eca-61f4-4949-8398-52c9fc36721c
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3e6eac3f4aa5659a89b89037c60eb5c42788313c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388201"
---
# <a name="gridentity-client-api-reference"></a>GridEntity (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

GridEntity is returned by the [GridRowData](gridrowdata.md).[getEntity](gridrowdata/getEntity.md) method or by directly accessing the [GridRowData](gridrowdata.md).**entity** object. Use the GridEntity methods to access data about the specific records in the rows.

```JavaScript
var myRows = gridContext.getGrid().getRows();
var myRow = myRows.get(arg);
var gridEntity = myRow.getData().getEntity();
```

GridEntity also supports the **attributes** collection that provides methods of working with a collection of attributes for an entity in the editable grid. Each attribute ([GridAttribute](gridattribute.md)) represents the data in the cell of an editable grid, and contains a reference to all the cells associated with the attribute. See [Collections (Client API reference)](../collections.md) for information on the methods available to access data in a collection.

## <a name="methods"></a>Phương pháp

|                                Tên                                |                                                             Mô tả                                                              |        Có sẵn cho         |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
|            [getEntityName](gridentity/getEntityName.md)            |            [!INCLUDE[gridentity/includes/getEntityName-description.md](gridentity/includes/getEntityName-description.md)]            | Read-only and editable grids |
|       [getEntityReference](gridentity/getEntityReference.md)       |       [!INCLUDE[gridentity/includes/getEntityReference-description.md](gridentity/includes/getEntityReference-description.md)]       | Read-only and editable grids |
|                    [getId](gridentity/getId.md)                    |                    [!INCLUDE[gridentity/includes/getId-description.md](gridentity/includes/getId-description.md)]                    | Read-only and editable grids |
| [getPrimaryAttributeValue](gridentity/getPrimaryAttributeValue.md) | [!INCLUDE[gridentity/includes/getPrimaryAttributeValue-description.md](gridentity/includes/getPrimaryAttributeValue-description.md)] |        Read-only grid        |

### <a name="related-topics"></a>Chủ đề liên quan

[GridAttribute](gridattribute.md)

[Grids and subgrids in Customer Engagement](../grids.md)

[Thuộc tính](../attributes.md)


