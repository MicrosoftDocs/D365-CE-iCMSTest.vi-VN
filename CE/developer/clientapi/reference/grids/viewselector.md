---
title: ViewSelector methods (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 37fbabaf-e2ce-4e46-a54e-e46bd884197b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6084b514daec0bf11a7d4cd5f37b5e87985722a2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386716"
---
# <a name="viewselector-methods-client-api-reference"></a>ViewSelector methods (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Provides methods to get or set information about the view selector of the subgrid control. If the subgrid control is not configured to display the view selector, calling the **ViewSelector** methods will throw an error.

ViewSelector is available only for read-only grids. ViewSelector is returned by the **gridContext**.[getViewSelector](gridcontrol/getViewSelector.md) method.

```JavaScript
var viewSelector = gridContext.getViewSelector();
```

Phương pháp


|                       Tên                       |                                                     Mô tả                                                      | Có sẵn cho  |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|----------------|
| [getCurrentView](viewselector/getCurrentView.md) | [!INCLUDE[viewselector/includes/getCurrentView-description.md](viewselector/includes/getCurrentView-description.md)] | Read-only grid |
|      [isVisible](viewselector/isVisible.md)      |      [!INCLUDE[viewselector/includes/isVisible-description.md](viewselector/includes/isVisible-description.md)]      | Read-only grid |
| [setCurrentView](viewselector/setCurrentView.md) | [!INCLUDE[viewselector/includes/setCurrentView-description.md](viewselector/includes/setCurrentView-description.md)] | Read-only grid |

### <a name="related-topics"></a>Chủ đề liên quan

[gridContext](../grids.md#bkmk_gridcontext)

[Grids and subgrids in Customer Engagement](../grids.md)


