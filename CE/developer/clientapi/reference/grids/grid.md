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
# <a name="grid-client-api-reference"></a><span data-ttu-id="e424b-102">Grid (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="e424b-102">Grid (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e424b-103">Grid is returned by the **gridContext**.[getGrid](gridcontrol/getGrid.md) method.</span><span class="sxs-lookup"><span data-stu-id="e424b-103">Grid is returned by the **gridContext**.[getGrid](gridcontrol/getGrid.md) method.</span></span> <span data-ttu-id="e424b-104">Use Grid methods to access information about data in the grid.</span><span class="sxs-lookup"><span data-stu-id="e424b-104">Use Grid methods to access information about data in the grid.</span></span>

`var myGrid = gridContext.getGrid();`

## <a name="methods"></a><span data-ttu-id="e424b-105">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="e424b-105">Methods</span></span>

|                        <span data-ttu-id="e424b-106">Tên</span><span class="sxs-lookup"><span data-stu-id="e424b-106">Name</span></span>                        |                                                  <span data-ttu-id="e424b-107">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e424b-107">Description</span></span>                                                   |        <span data-ttu-id="e424b-108">Có sẵn cho</span><span class="sxs-lookup"><span data-stu-id="e424b-108">Available for</span></span>         |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|------------------------------|
|             [<span data-ttu-id="e424b-109">getRows</span><span class="sxs-lookup"><span data-stu-id="e424b-109">getRows</span></span>](grid/getRows.md)             |             [!INCLUDE[grid/includes/getRows-description.md](grid/includes/getRows-description.md)]             | <span data-ttu-id="e424b-110">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="e424b-110">Read-only and editable grids</span></span> |
|     [<span data-ttu-id="e424b-111">getSelectedRows</span><span class="sxs-lookup"><span data-stu-id="e424b-111">getSelectedRows</span></span>](grid/getSelectedRows.md)     |     [!INCLUDE[grid/includes/getSelectedRows-description.md](grid/includes/getSelectedRows-description.md)]     | <span data-ttu-id="e424b-112">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="e424b-112">Read-only and editable grids</span></span> |
| [<span data-ttu-id="e424b-113">getTotalRecordCount</span><span class="sxs-lookup"><span data-stu-id="e424b-113">getTotalRecordCount</span></span>](grid/getTotalRecordCount.md) | [!INCLUDE[grid/includes/getTotalRecordCount-description.md](grid/includes/getTotalRecordCount-description.md)] | <span data-ttu-id="e424b-114">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="e424b-114">Read-only and editable grids</span></span> |

### <a name="related-topics"></a><span data-ttu-id="e424b-115">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="e424b-115">Related topics</span></span>

[<span data-ttu-id="e424b-116">GridRow</span><span class="sxs-lookup"><span data-stu-id="e424b-116">GridRow</span></span>](gridrow.md)

[<span data-ttu-id="e424b-117">Grids and subgrids in Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="e424b-117">Grids and subgrids in Customer Engagement</span></span>](../grids.md)
