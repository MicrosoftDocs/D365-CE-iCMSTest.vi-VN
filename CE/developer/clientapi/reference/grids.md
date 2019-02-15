---
title: Grids and subgrids in Customer Engagement for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9d35c036-637f-4580-8ba0-027a44c0fdee
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4ee8aa52937247860e34d3701fbc56abfad71a25
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388170"
---
# <a name="grids-and-subgrids-in-customer-engagement-client-api-reference"></a>Grids and subgrids in Customer Engagement (Client API reference)

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

Grids present data in a tabular format in Customer Engagement. Grids can span the entire form or can be one of the items on a form; the latter are called *subgrids*.

## <a name="types-of-grids"></a>Types of grids

There are two types of grids in Customer Engagement:
- **Read-only grids**: Display data in a tabular format. To edit the data displayed in a read-only grid, you have to click the record in the grid to open the form, edit the data, and then save.
-  **Editable grids**: In addition to displaying data in a tabular format, provides rich inline editing capabilities on web and mobile clients including the ability to group, sort, and filter data within the same grid so that you do not have to switch records or views. The editable grid is a custom control, and is supported in the main grid and subgrids on a form in the web client and in dashboards and on form grids on the mobile clients. Although the editable grid control provides editing capability, it honors the read-only grid metadata and field-level security settings.

<a name="bkmk_gridcontext"></a>
## <a name="getting-the-grid-context"></a>Getting the grid context

Grid context is the grid or subgrid instance on a form against which you want to run your code. For more information about getting the grid context to execute your JavaScript code, see [Client API grid context](../clientapi-grid-context.md)

## <a name="events"></a>Sự kiện

|Tên|Mô tả|Applicable for|
|--|--|--|
|[Subgrid OnLoad Event](events/subgrid-onload.md)|Occurs every time the subgrid refreshes. This includes when users sort values in subgrid by clicking the column headings.|Read-only grid|
|[Grid OnChange](events/grid-onchange.md)|Occurs when a value is changed in a cell in the editable grid and the cell loses focus|Editable grid|
|[Grid OnRecordSelect](events/grid-onrecordselect.md)|Occurs when a single row (record) is selected in the editable grid|Editable grid|
|[Grid OnSave](events/grid-onsave.md)|Occurs before sending the updated information to the server, and when any of the following occurs: there is a change in the record selection, the user explicitly triggers a save operation using the editable grid’s save button, or the user applies a sort, filter, group, pagination, or navigation operation from the editable grid while there are pending changes.|Editable grid|

>[!NOTE]
>You can register for the **OnChange**, **OnRecordSelect**, and **OnSave** events using the **Events** tab of the Dynamics 365 for Customer Engagement apps page that is used to enable editable grids for an entity or a read-only grid.

## <a name="methods"></a>Phương pháp

|Tên|Mô tả|Có sẵn cho|
|--|--|--|
|[GridControl](grids/gridcontrol.md)|Provides methods to work with the grid or subgrid control.|Read-only and editable grids|
|[Grid](grids/grid.md)|Provides methods to access information about data in the grid.|Read-only and editable grids|
|[GridRow](grids/gridrow.md)|Provides methods to work with rows or selected rows in the grid.|Read-only and editable grids|
|[GridRowData](grids/gridrowdata.md)|Provides methods to work with rows or selected rows in the grid.|Read-only and editable grids|
|[GridEntity](grids/gridentity.md)|Provides methods to access data about the specific records in the rows.|Read-only and editable grids|
|[GridAttribute](grids/gridattribute.md)|Provides methods to access the data in the cell of an editable grid.|Editable grid|
|[GridCell](grids/gridcell.md)|Provides methods to access the data related to control on a form that is tied to an attribute in an editable grid.|Editable grid|
|[ViewSelector](grids/viewselector.md)|Provides methods to get or set information about the view selector of the subgrid control.|Read-only grid|


### <a name="related-topics"></a>Chủ đề liên quan

[Client API grid context](../clientapi-grid-context.md)

[Use editable grids in Customer Engagement](../../customize-dev/use-editable-grids-dynamics-365.md)

[Client API Reference for Customer Engagement](../reference.md)

[Developer Guide for Dynamics 365 for Customer Engagement apps](../../developer-guide.md)
