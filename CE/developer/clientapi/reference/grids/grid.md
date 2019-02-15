---
title: Grid (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: eac932a598997ecc2f4654defdad2f90776e9b51
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387626"
---
# <a name="grid-client-api-reference"></a>Grid (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Grid is returned by the **gridContext**.[getGrid](gridcontrol/getGrid.md) method. Use Grid methods to access information about data in the grid.

`var myGrid = gridContext.getGrid();`

## <a name="methods"></a>Phương pháp

|                        Tên                        |                                                  Mô tả                                                   |        Có sẵn cho         |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|------------------------------|
|             [getRows](grid/getRows.md)             |             [!INCLUDE[grid/includes/getRows-description.md](grid/includes/getRows-description.md)]             | Read-only and editable grids |
|     [getSelectedRows](grid/getSelectedRows.md)     |     [!INCLUDE[grid/includes/getSelectedRows-description.md](grid/includes/getSelectedRows-description.md)]     | Read-only and editable grids |
| [getTotalRecordCount](grid/getTotalRecordCount.md) | [!INCLUDE[grid/includes/getTotalRecordCount-description.md](grid/includes/getTotalRecordCount-description.md)] | Read-only and editable grids |

### <a name="related-topics"></a>Chủ đề liên quan

[GridRow](gridrow.md)

[Grids and subgrids in Customer Engagement](../grids.md)
