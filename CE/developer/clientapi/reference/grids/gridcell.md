---
title: GridCell (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: d82ebf3bf0a705bcb684bea1ad07d2ee454f0d0f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386772"
---
# <a name="gridcell-client-api-reference"></a>GridCell (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

GridCell is only supported for editable grids.

GridCell of a selected grid row is analogous to a control on a form that is tied to an attribute in an editable grid. See [Collections (Client API reference)](../collections.md) for information on the methods available to access data in a collection.

## <a name="methods"></a>Phương pháp

GridCell supports the following methods.

|Tên |Mô tả |
|--|--|
|[clearNotification](../controls/clearNotification.md)| Clears notification for a cell.|
|[getDisabled](../controls/getDisabled.md)| Returns whether the cell is disabled (read-only).|
|[setDisabled](../controls/setDisabled.md)| Sets whether the cell is disabled.<br/><br/>**NOTE**: Enabling a read-only cell for editing can cause an error when the record is saved. If the field is considered read-only by the server, an error may occur if the value is modified. This may happen in scenarios where the user doesn't have write privileges to the record, the record is disabled, or the user doesn't have the necessary field-level security privileges.| 
|[setNotification](../controls/setNotification.md)|Displays an error message for a cell to indicate that data isn’t valid.|
|[getLabel](../controls/getLabel.md)|Returns the label of the column that contains the cell.|


### <a name="related-topics"></a>Chủ đề liên quan

[Grids and subgrids in Customer Engagement](../grids.md)

[Kiểm soát](../controls.md)


