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
# <a name="gridentity-client-api-reference"></a><span data-ttu-id="a5b05-102">GridEntity (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="a5b05-102">GridEntity (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a5b05-103">GridEntity is returned by the [GridRowData](gridrowdata.md).[getEntity](gridrowdata/getEntity.md) method or by directly accessing the [GridRowData](gridrowdata.md).**entity** object.</span><span class="sxs-lookup"><span data-stu-id="a5b05-103">GridEntity is returned by the [GridRowData](gridrowdata.md).[getEntity](gridrowdata/getEntity.md) method or by directly accessing the [GridRowData](gridrowdata.md).**entity** object.</span></span> <span data-ttu-id="a5b05-104">Use the GridEntity methods to access data about the specific records in the rows.</span><span class="sxs-lookup"><span data-stu-id="a5b05-104">Use the GridEntity methods to access data about the specific records in the rows.</span></span>

```JavaScript
var myRows = gridContext.getGrid().getRows();
var myRow = myRows.get(arg);
var gridEntity = myRow.getData().getEntity();
```

<span data-ttu-id="a5b05-105">GridEntity also supports the **attributes** collection that provides methods of working with a collection of attributes for an entity in the editable grid.</span><span class="sxs-lookup"><span data-stu-id="a5b05-105">GridEntity also supports the **attributes** collection that provides methods of working with a collection of attributes for an entity in the editable grid.</span></span> <span data-ttu-id="a5b05-106">Each attribute ([GridAttribute](gridattribute.md)) represents the data in the cell of an editable grid, and contains a reference to all the cells associated with the attribute.</span><span class="sxs-lookup"><span data-stu-id="a5b05-106">Each attribute ([GridAttribute](gridattribute.md)) represents the data in the cell of an editable grid, and contains a reference to all the cells associated with the attribute.</span></span> <span data-ttu-id="a5b05-107">See [Collections (Client API reference)](../collections.md) for information on the methods available to access data in a collection.</span><span class="sxs-lookup"><span data-stu-id="a5b05-107">See [Collections (Client API reference)](../collections.md) for information on the methods available to access data in a collection.</span></span>

## <a name="methods"></a><span data-ttu-id="a5b05-108">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="a5b05-108">Methods</span></span>

|                                <span data-ttu-id="a5b05-109">Tên</span><span class="sxs-lookup"><span data-stu-id="a5b05-109">Name</span></span>                                |                                                             <span data-ttu-id="a5b05-110">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a5b05-110">Description</span></span>                                                              |        <span data-ttu-id="a5b05-111">Có sẵn cho</span><span class="sxs-lookup"><span data-stu-id="a5b05-111">Available for</span></span>         |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
|            [<span data-ttu-id="a5b05-112">getEntityName</span><span class="sxs-lookup"><span data-stu-id="a5b05-112">getEntityName</span></span>](gridentity/getEntityName.md)            |            [!INCLUDE[gridentity/includes/getEntityName-description.md](gridentity/includes/getEntityName-description.md)]            | <span data-ttu-id="a5b05-113">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="a5b05-113">Read-only and editable grids</span></span> |
|       [<span data-ttu-id="a5b05-114">getEntityReference</span><span class="sxs-lookup"><span data-stu-id="a5b05-114">getEntityReference</span></span>](gridentity/getEntityReference.md)       |       [!INCLUDE[gridentity/includes/getEntityReference-description.md](gridentity/includes/getEntityReference-description.md)]       | <span data-ttu-id="a5b05-115">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="a5b05-115">Read-only and editable grids</span></span> |
|                    [<span data-ttu-id="a5b05-116">getId</span><span class="sxs-lookup"><span data-stu-id="a5b05-116">getId</span></span>](gridentity/getId.md)                    |                    [!INCLUDE[gridentity/includes/getId-description.md](gridentity/includes/getId-description.md)]                    | <span data-ttu-id="a5b05-117">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="a5b05-117">Read-only and editable grids</span></span> |
| [<span data-ttu-id="a5b05-118">getPrimaryAttributeValue</span><span class="sxs-lookup"><span data-stu-id="a5b05-118">getPrimaryAttributeValue</span></span>](gridentity/getPrimaryAttributeValue.md) | [!INCLUDE[gridentity/includes/getPrimaryAttributeValue-description.md](gridentity/includes/getPrimaryAttributeValue-description.md)] |        <span data-ttu-id="a5b05-119">Read-only grid</span><span class="sxs-lookup"><span data-stu-id="a5b05-119">Read-only grid</span></span>        |

### <a name="related-topics"></a><span data-ttu-id="a5b05-120">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="a5b05-120">Related topics</span></span>

[<span data-ttu-id="a5b05-121">GridAttribute</span><span class="sxs-lookup"><span data-stu-id="a5b05-121">GridAttribute</span></span>](gridattribute.md)

[<span data-ttu-id="a5b05-122">Grids and subgrids in Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="a5b05-122">Grids and subgrids in Customer Engagement</span></span>](../grids.md)

[<span data-ttu-id="a5b05-123">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="a5b05-123">Attributes</span></span>](../attributes.md)


