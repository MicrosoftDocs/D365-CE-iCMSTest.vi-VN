---
title: GridAttribute (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
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
ms.openlocfilehash: d1a96e1efeb5af95a4cab9625eec77f253d60409
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387844"
---
# <a name="gridattribute-client-api-reference"></a><span data-ttu-id="027be-102">GridAttribute (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="027be-102">GridAttribute (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="027be-103">GridAttribute is only supported for editable grids.</span><span class="sxs-lookup"><span data-stu-id="027be-103">GridAttribute is only supported for editable grids.</span></span>

<span data-ttu-id="027be-104">GridAttribute represents the data in the cell of an editable grid, and contains a reference to all the cells associated with the attribute.</span><span class="sxs-lookup"><span data-stu-id="027be-104">GridAttribute represents the data in the cell of an editable grid, and contains a reference to all the cells associated with the attribute.</span></span> <span data-ttu-id="027be-105">See [Collections (Client API reference)](../collections.md) for information on the methods available to access data in a collection.</span><span class="sxs-lookup"><span data-stu-id="027be-105">See [Collections (Client API reference)](../collections.md) for information on the methods available to access data in a collection.</span></span>

<span data-ttu-id="027be-106">GridAttribute also supports the **controls** collection for attributes of a selected grid row, which provides methods to work with a collection of cells associated with the attribute.</span><span class="sxs-lookup"><span data-stu-id="027be-106">GridAttribute also supports the **controls** collection for attributes of a selected grid row, which provides methods to work with a collection of cells associated with the attribute.</span></span> <span data-ttu-id="027be-107">Each cell ([GridCell](gridcell.md)) of a selected grid row is analogous to a control on a form that is tied to an attribute in an editable grid.</span><span class="sxs-lookup"><span data-stu-id="027be-107">Each cell ([GridCell](gridcell.md)) of a selected grid row is analogous to a control on a form that is tied to an attribute in an editable grid.</span></span> <span data-ttu-id="027be-108">See [Collections (Client API reference)](../collections.md) for information on the methods available to access data in a collection.</span><span class="sxs-lookup"><span data-stu-id="027be-108">See [Collections (Client API reference)](../collections.md) for information on the methods available to access data in a collection.</span></span>

> [!TIP]
> <span data-ttu-id="027be-109">For performance reasons, a row (record) in an editable grid is not editable until the record is selected.</span><span class="sxs-lookup"><span data-stu-id="027be-109">For performance reasons, a row (record) in an editable grid is not editable until the record is selected.</span></span> <span data-ttu-id="027be-110">Users must select a single record in a grid to edit it.</span><span class="sxs-lookup"><span data-stu-id="027be-110">Users must select a single record in a grid to edit it.</span></span> <span data-ttu-id="027be-111">Once a record is selected in an editable grid, Dynamics 365 for Customer Engagement internally evaluates a number of things including user access to the record, whether the record is active, and field validations to ensure that data security and validity are honored when you edit data.</span><span class="sxs-lookup"><span data-stu-id="027be-111">Once a record is selected in an editable grid, Dynamics 365 for Customer Engagement internally evaluates a number of things including user access to the record, whether the record is active, and field validations to ensure that data security and validity are honored when you edit data.</span></span> <span data-ttu-id="027be-112">Consider using the [OnRecordSelect](../events/grid-onrecordselect.md) event with the [getFormContext](../executioncontext/getFormContext.md) method to access records in the grid that are in the editable state.</span><span class="sxs-lookup"><span data-stu-id="027be-112">Consider using the [OnRecordSelect](../events/grid-onrecordselect.md) event with the [getFormContext](../executioncontext/getFormContext.md) method to access records in the grid that are in the editable state.</span></span>

## <a name="methods"></a><span data-ttu-id="027be-113">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="027be-113">Methods</span></span>

<span data-ttu-id="027be-114">GridAttribute supports the following methods for attributes of a selected grid row.</span><span class="sxs-lookup"><span data-stu-id="027be-114">GridAttribute supports the following methods for attributes of a selected grid row.</span></span>

|<span data-ttu-id="027be-115">Tên</span><span class="sxs-lookup"><span data-stu-id="027be-115">Name</span></span>|<span data-ttu-id="027be-116">Mô tả</span><span class="sxs-lookup"><span data-stu-id="027be-116">Description</span></span>|
|--|--|
|[<span data-ttu-id="027be-117">getName</span><span class="sxs-lookup"><span data-stu-id="027be-117">getName</span></span>](../attributes/getName.md)|<span data-ttu-id="027be-118">Returns the logical name of the attribute of a selected grid row.</span><span class="sxs-lookup"><span data-stu-id="027be-118">Returns the logical name of the attribute of a selected grid row.</span></span>|
|[<span data-ttu-id="027be-119">getRequiredLevel</span><span class="sxs-lookup"><span data-stu-id="027be-119">getRequiredLevel</span></span>](../attributes/getRequiredLevel.md)| <span data-ttu-id="027be-120">Returns a string value indicating whether a value for the attribute is required or recommended.</span><span class="sxs-lookup"><span data-stu-id="027be-120">Returns a string value indicating whether a value for the attribute is required or recommended.</span></span>|
|[<span data-ttu-id="027be-121">setRequiredLevel</span><span class="sxs-lookup"><span data-stu-id="027be-121">setRequiredLevel</span></span>](../attributes/setRequiredLevel.md)| <span data-ttu-id="027be-122">Sets whether data is required or recommended for the attribute of a selected grid row before the record can be saved.</span><span class="sxs-lookup"><span data-stu-id="027be-122">Sets whether data is required or recommended for the attribute of a selected grid row before the record can be saved.</span></span>|
|[<span data-ttu-id="027be-123">getValue</span><span class="sxs-lookup"><span data-stu-id="027be-123">getValue</span></span>](../attributes/getValue.md)| <span data-ttu-id="027be-124">Retrieves the data value for an attribute.</span><span class="sxs-lookup"><span data-stu-id="027be-124">Retrieves the data value for an attribute.</span></span>|
|[<span data-ttu-id="027be-125">setValue</span><span class="sxs-lookup"><span data-stu-id="027be-125">setValue</span></span>](../attributes/setValue.md)| <span data-ttu-id="027be-126">Sets the data value for an attribute.</span><span class="sxs-lookup"><span data-stu-id="027be-126">Sets the data value for an attribute.</span></span>|

>[!NOTE]
><span data-ttu-id="027be-127">To select a row in an editable grid, use the [Grid](grid.md).[getSelectedRows](grid/getSelectedRows.md)</span><span class="sxs-lookup"><span data-stu-id="027be-127">To select a row in an editable grid, use the [Grid](grid.md).[getSelectedRows](grid/getSelectedRows.md)</span></span>

### <a name="related-topics"></a><span data-ttu-id="027be-128">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="027be-128">Related topics</span></span>

[<span data-ttu-id="027be-129">GridCell</span><span class="sxs-lookup"><span data-stu-id="027be-129">GridCell</span></span>](gridcell.md)

[<span data-ttu-id="027be-130">Grids and subgrids in Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="027be-130">Grids and subgrids in Customer Engagement</span></span>](../grids.md)

[<span data-ttu-id="027be-131">Controls collection</span><span class="sxs-lookup"><span data-stu-id="027be-131">Controls collection</span></span>](../attributes/controls-collection.md)