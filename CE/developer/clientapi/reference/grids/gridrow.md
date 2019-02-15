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
# <a name="gridrow-client-api-reference"></a><span data-ttu-id="94e07-102">GridRow (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="94e07-102">GridRow (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="94e07-103">A collection of GridRow is returned by [Grid](grid.md).[getRows](grid/getRows.md) and [Grid](grid.md).[getSelectedRows](grid/getSelectedRows.md) methods.</span><span class="sxs-lookup"><span data-stu-id="94e07-103">A collection of GridRow is returned by [Grid](grid.md).[getRows](grid/getRows.md) and [Grid](grid.md).[getSelectedRows](grid/getSelectedRows.md) methods.</span></span>

```JavaScript
var myRows = gridContext.getGrid().getRows();
var gridRow = myRows.get(arg);
```

## <a name="properties"></a><span data-ttu-id="94e07-104">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="94e07-104">Properties</span></span>

|<span data-ttu-id="94e07-105">Tên</span><span class="sxs-lookup"><span data-stu-id="94e07-105">Name</span></span>|<span data-ttu-id="94e07-106">Mô tả</span><span class="sxs-lookup"><span data-stu-id="94e07-106">Description</span></span>|<span data-ttu-id="94e07-107">Có sẵn cho</span><span class="sxs-lookup"><span data-stu-id="94e07-107">Available for</span></span>|
|--|--|--|
|<span data-ttu-id="94e07-108">dữ liệu</span><span class="sxs-lookup"><span data-stu-id="94e07-108">data</span></span>|<span data-ttu-id="94e07-109">A collection containing the [GridRowData](gridrowdata.md) for the GridRow.</span><span class="sxs-lookup"><span data-stu-id="94e07-109">A collection containing the [GridRowData](gridrowdata.md) for the GridRow.</span></span> <span data-ttu-id="94e07-110">See [Collections (Client API reference)](../collections.md) for information on the methods available for accessing data in a collection.</span><span class="sxs-lookup"><span data-stu-id="94e07-110">See [Collections (Client API reference)](../collections.md) for information on the methods available for accessing data in a collection.</span></span>|<span data-ttu-id="94e07-111">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="94e07-111">Read-only and editable grids</span></span>|


## <a name="methods"></a><span data-ttu-id="94e07-112">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="94e07-112">Methods</span></span>

|             <span data-ttu-id="94e07-113">Tên</span><span class="sxs-lookup"><span data-stu-id="94e07-113">Name</span></span>              |                                         <span data-ttu-id="94e07-114">Mô tả</span><span class="sxs-lookup"><span data-stu-id="94e07-114">Description</span></span>                                          |        <span data-ttu-id="94e07-115">Có sẵn cho</span><span class="sxs-lookup"><span data-stu-id="94e07-115">Available for</span></span>         |
|-------------------------------|----------------------------------------------------------------------------------------------|------------------------------|
| [<span data-ttu-id="94e07-116">getData</span><span class="sxs-lookup"><span data-stu-id="94e07-116">getData</span></span>](gridrow/getData.md) | [!INCLUDE[gridrow/includes/getData-description.md](gridrow/includes/getData-description.md)] | <span data-ttu-id="94e07-117">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="94e07-117">Read-only and editable grids</span></span> |

### <a name="related-topics"></a><span data-ttu-id="94e07-118">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="94e07-118">Related topics</span></span>

[<span data-ttu-id="94e07-119">GridRowData</span><span class="sxs-lookup"><span data-stu-id="94e07-119">GridRowData</span></span>](gridrowdata.md)

[<span data-ttu-id="94e07-120">Grids and subgrids in Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="94e07-120">Grids and subgrids in Customer Engagement</span></span>](../grids.md)


