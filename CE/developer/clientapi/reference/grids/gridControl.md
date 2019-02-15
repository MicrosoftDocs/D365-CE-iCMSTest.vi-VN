---
title: GridControl (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: d54eb190-9a97-4004-8771-637c413626c1
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 04ea7c6d333006dec17af56354fcc8394aabbc58
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388835"
---
# <a name="gridcontrol-client-api-reference"></a>GridControl (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

GridControl or the gridContext is the instance of grid or subgrid on a form against which you want to execute your script. Use the form context to get GridControl [(gridContext)](../grids.md#bkmk_gridcontext) on a form.

## <a name="methods"></a>Phương pháp

|                       Tên                        |                                                     Mô tả                                                      |        Có sẵn cho         |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|------------------------------|
|       [addOnLoad](gridcontrol/addOnLoad.md)       |       [!INCLUDE[gridcontrol/includes/addOnLoad-description.md](gridcontrol/includes/addOnLoad-description.md)]       |        Read-only grid        |
|   [getEntityName](gridcontrol/getEntityName.md)   |   [!INCLUDE[gridcontrol/includes/getEntityName-description.md](gridcontrol/includes/getEntityName-description.md)]   | Read-only and editable grids |
|     [getFetchXml](gridcontrol/getFetchXml.md)     |     [!INCLUDE[gridcontrol/includes/getFetchXml-description.md](gridcontrol/includes/getFetchXml-description.md)]     | Read-only and editable grids |
|         [getGrid](gridcontrol/getGrid.md)         |         [!INCLUDE[gridcontrol/includes/getGrid-description.md](gridcontrol/includes/getGrid-description.md)]         | Read-only and editable grids |
|     [getGridType](gridcontrol/getGridType.md)     |     [!INCLUDE[gridcontrol/includes/getGridType-description.md](gridcontrol/includes/getGridType-description.md)]     | Read-only and editable grids |
| [getRelationship](gridcontrol/getRelationship.md) | [!INCLUDE[gridcontrol/includes/getRelationship-description.md](gridcontrol/includes/getRelationship-description.md)] | Read-only and editable grids |
|          [getUrl](gridcontrol/getUrl.md)          |          [!INCLUDE[gridcontrol/includes/getUrl-description.md](gridcontrol/includes/getUrl-description.md)]          | Read-only and editable grids |
| [getViewSelector](gridcontrol/getViewSelector.md) | [!INCLUDE[gridcontrol/includes/getViewSelector-description.md](gridcontrol/includes/getViewSelector-description.md)] |        Read-only grid        |
| [openRelatedGrid](gridcontrol/openRelatedGrid.md) | [!INCLUDE[gridcontrol/includes/openRelatedGrid-description.md](gridcontrol/includes/openRelatedGrid-description.md)] | Read-only and editable grids |
|         [refresh](gridcontrol/refresh.md)         |         [!INCLUDE[gridcontrol/includes/refresh-description.md](gridcontrol/includes/refresh-description.md)]         | Read-only and editable grids |
|   [refreshRibbon](gridcontrol/refreshRibbon.md)   |   [!INCLUDE[gridcontrol/includes/refreshRibbon-description.md](gridcontrol/includes/refreshRibbon-description.md)]   | Read-only and editable grids |
|    [removeOnLoad](gridcontrol/removeOnLoad.md)    |    [!INCLUDE[gridcontrol/includes/removeOnLoad-description.md](gridcontrol/includes/removeOnLoad-description.md)]    |        Read-only grid        |

### <a name="related-topics"></a>Chủ đề liên quan

[Grid](grid.md)

[Grids and subgrids in Customer Engagement](../grids.md)


