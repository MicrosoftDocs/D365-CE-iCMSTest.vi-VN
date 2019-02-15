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
# <a name="gridcontrol-client-api-reference"></a><span data-ttu-id="3328a-102">GridControl (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="3328a-102">GridControl (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3328a-103">GridControl or the gridContext is the instance of grid or subgrid on a form against which you want to execute your script.</span><span class="sxs-lookup"><span data-stu-id="3328a-103">GridControl or the gridContext is the instance of grid or subgrid on a form against which you want to execute your script.</span></span> <span data-ttu-id="3328a-104">Use the form context to get GridControl [(gridContext)](../grids.md#bkmk_gridcontext) on a form.</span><span class="sxs-lookup"><span data-stu-id="3328a-104">Use the form context to get GridControl [(gridContext)](../grids.md#bkmk_gridcontext) on a form.</span></span>

## <a name="methods"></a><span data-ttu-id="3328a-105">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="3328a-105">Methods</span></span>

|                       <span data-ttu-id="3328a-106">Tên</span><span class="sxs-lookup"><span data-stu-id="3328a-106">Name</span></span>                        |                                                     <span data-ttu-id="3328a-107">Mô tả</span><span class="sxs-lookup"><span data-stu-id="3328a-107">Description</span></span>                                                      |        <span data-ttu-id="3328a-108">Có sẵn cho</span><span class="sxs-lookup"><span data-stu-id="3328a-108">Available for</span></span>         |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|------------------------------|
|       [<span data-ttu-id="3328a-109">addOnLoad</span><span class="sxs-lookup"><span data-stu-id="3328a-109">addOnLoad</span></span>](gridcontrol/addOnLoad.md)       |       [!INCLUDE[gridcontrol/includes/addOnLoad-description.md](gridcontrol/includes/addOnLoad-description.md)]       |        <span data-ttu-id="3328a-110">Read-only grid</span><span class="sxs-lookup"><span data-stu-id="3328a-110">Read-only grid</span></span>        |
|   [<span data-ttu-id="3328a-111">getEntityName</span><span class="sxs-lookup"><span data-stu-id="3328a-111">getEntityName</span></span>](gridcontrol/getEntityName.md)   |   [!INCLUDE[gridcontrol/includes/getEntityName-description.md](gridcontrol/includes/getEntityName-description.md)]   | <span data-ttu-id="3328a-112">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="3328a-112">Read-only and editable grids</span></span> |
|     [<span data-ttu-id="3328a-113">getFetchXml</span><span class="sxs-lookup"><span data-stu-id="3328a-113">getFetchXml</span></span>](gridcontrol/getFetchXml.md)     |     [!INCLUDE[gridcontrol/includes/getFetchXml-description.md](gridcontrol/includes/getFetchXml-description.md)]     | <span data-ttu-id="3328a-114">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="3328a-114">Read-only and editable grids</span></span> |
|         [<span data-ttu-id="3328a-115">getGrid</span><span class="sxs-lookup"><span data-stu-id="3328a-115">getGrid</span></span>](gridcontrol/getGrid.md)         |         [!INCLUDE[gridcontrol/includes/getGrid-description.md](gridcontrol/includes/getGrid-description.md)]         | <span data-ttu-id="3328a-116">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="3328a-116">Read-only and editable grids</span></span> |
|     [<span data-ttu-id="3328a-117">getGridType</span><span class="sxs-lookup"><span data-stu-id="3328a-117">getGridType</span></span>](gridcontrol/getGridType.md)     |     [!INCLUDE[gridcontrol/includes/getGridType-description.md](gridcontrol/includes/getGridType-description.md)]     | <span data-ttu-id="3328a-118">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="3328a-118">Read-only and editable grids</span></span> |
| [<span data-ttu-id="3328a-119">getRelationship</span><span class="sxs-lookup"><span data-stu-id="3328a-119">getRelationship</span></span>](gridcontrol/getRelationship.md) | [!INCLUDE[gridcontrol/includes/getRelationship-description.md](gridcontrol/includes/getRelationship-description.md)] | <span data-ttu-id="3328a-120">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="3328a-120">Read-only and editable grids</span></span> |
|          [<span data-ttu-id="3328a-121">getUrl</span><span class="sxs-lookup"><span data-stu-id="3328a-121">getUrl</span></span>](gridcontrol/getUrl.md)          |          [!INCLUDE[gridcontrol/includes/getUrl-description.md](gridcontrol/includes/getUrl-description.md)]          | <span data-ttu-id="3328a-122">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="3328a-122">Read-only and editable grids</span></span> |
| [<span data-ttu-id="3328a-123">getViewSelector</span><span class="sxs-lookup"><span data-stu-id="3328a-123">getViewSelector</span></span>](gridcontrol/getViewSelector.md) | [!INCLUDE[gridcontrol/includes/getViewSelector-description.md](gridcontrol/includes/getViewSelector-description.md)] |        <span data-ttu-id="3328a-124">Read-only grid</span><span class="sxs-lookup"><span data-stu-id="3328a-124">Read-only grid</span></span>        |
| [<span data-ttu-id="3328a-125">openRelatedGrid</span><span class="sxs-lookup"><span data-stu-id="3328a-125">openRelatedGrid</span></span>](gridcontrol/openRelatedGrid.md) | [!INCLUDE[gridcontrol/includes/openRelatedGrid-description.md](gridcontrol/includes/openRelatedGrid-description.md)] | <span data-ttu-id="3328a-126">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="3328a-126">Read-only and editable grids</span></span> |
|         [<span data-ttu-id="3328a-127">refresh</span><span class="sxs-lookup"><span data-stu-id="3328a-127">refresh</span></span>](gridcontrol/refresh.md)         |         [!INCLUDE[gridcontrol/includes/refresh-description.md](gridcontrol/includes/refresh-description.md)]         | <span data-ttu-id="3328a-128">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="3328a-128">Read-only and editable grids</span></span> |
|   [<span data-ttu-id="3328a-129">refreshRibbon</span><span class="sxs-lookup"><span data-stu-id="3328a-129">refreshRibbon</span></span>](gridcontrol/refreshRibbon.md)   |   [!INCLUDE[gridcontrol/includes/refreshRibbon-description.md](gridcontrol/includes/refreshRibbon-description.md)]   | <span data-ttu-id="3328a-130">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="3328a-130">Read-only and editable grids</span></span> |
|    [<span data-ttu-id="3328a-131">removeOnLoad</span><span class="sxs-lookup"><span data-stu-id="3328a-131">removeOnLoad</span></span>](gridcontrol/removeOnLoad.md)    |    [!INCLUDE[gridcontrol/includes/removeOnLoad-description.md](gridcontrol/includes/removeOnLoad-description.md)]    |        <span data-ttu-id="3328a-132">Read-only grid</span><span class="sxs-lookup"><span data-stu-id="3328a-132">Read-only grid</span></span>        |

### <a name="related-topics"></a><span data-ttu-id="3328a-133">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="3328a-133">Related topics</span></span>

[<span data-ttu-id="3328a-134">Grid</span><span class="sxs-lookup"><span data-stu-id="3328a-134">Grid</span></span>](grid.md)

[<span data-ttu-id="3328a-135">Grids and subgrids in Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="3328a-135">Grids and subgrids in Customer Engagement</span></span>](../grids.md)


