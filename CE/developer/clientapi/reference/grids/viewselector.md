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
# <a name="viewselector-methods-client-api-reference"></a><span data-ttu-id="ffdad-102">ViewSelector methods (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="ffdad-102">ViewSelector methods (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ffdad-103">Provides methods to get or set information about the view selector of the subgrid control.</span><span class="sxs-lookup"><span data-stu-id="ffdad-103">Provides methods to get or set information about the view selector of the subgrid control.</span></span> <span data-ttu-id="ffdad-104">If the subgrid control is not configured to display the view selector, calling the **ViewSelector** methods will throw an error.</span><span class="sxs-lookup"><span data-stu-id="ffdad-104">If the subgrid control is not configured to display the view selector, calling the **ViewSelector** methods will throw an error.</span></span>

<span data-ttu-id="ffdad-105">ViewSelector is available only for read-only grids.</span><span class="sxs-lookup"><span data-stu-id="ffdad-105">ViewSelector is available only for read-only grids.</span></span> <span data-ttu-id="ffdad-106">ViewSelector is returned by the **gridContext**.[getViewSelector](gridcontrol/getViewSelector.md) method.</span><span class="sxs-lookup"><span data-stu-id="ffdad-106">ViewSelector is returned by the **gridContext**.[getViewSelector](gridcontrol/getViewSelector.md) method.</span></span>

```JavaScript
var viewSelector = gridContext.getViewSelector();
```

<span data-ttu-id="ffdad-107">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="ffdad-107">Methods</span></span>


|                       <span data-ttu-id="ffdad-108">Tên</span><span class="sxs-lookup"><span data-stu-id="ffdad-108">Name</span></span>                       |                                                     <span data-ttu-id="ffdad-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="ffdad-109">Description</span></span>                                                      | <span data-ttu-id="ffdad-110">Có sẵn cho</span><span class="sxs-lookup"><span data-stu-id="ffdad-110">Available for</span></span>  |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="ffdad-111">getCurrentView</span><span class="sxs-lookup"><span data-stu-id="ffdad-111">getCurrentView</span></span>](viewselector/getCurrentView.md) | [!INCLUDE[viewselector/includes/getCurrentView-description.md](viewselector/includes/getCurrentView-description.md)] | <span data-ttu-id="ffdad-112">Read-only grid</span><span class="sxs-lookup"><span data-stu-id="ffdad-112">Read-only grid</span></span> |
|      [<span data-ttu-id="ffdad-113">isVisible</span><span class="sxs-lookup"><span data-stu-id="ffdad-113">isVisible</span></span>](viewselector/isVisible.md)      |      [!INCLUDE[viewselector/includes/isVisible-description.md](viewselector/includes/isVisible-description.md)]      | <span data-ttu-id="ffdad-114">Read-only grid</span><span class="sxs-lookup"><span data-stu-id="ffdad-114">Read-only grid</span></span> |
| [<span data-ttu-id="ffdad-115">setCurrentView</span><span class="sxs-lookup"><span data-stu-id="ffdad-115">setCurrentView</span></span>](viewselector/setCurrentView.md) | [!INCLUDE[viewselector/includes/setCurrentView-description.md](viewselector/includes/setCurrentView-description.md)] | <span data-ttu-id="ffdad-116">Read-only grid</span><span class="sxs-lookup"><span data-stu-id="ffdad-116">Read-only grid</span></span> |

### <a name="related-topics"></a><span data-ttu-id="ffdad-117">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="ffdad-117">Related topics</span></span>

[<span data-ttu-id="ffdad-118">gridContext</span><span class="sxs-lookup"><span data-stu-id="ffdad-118">gridContext</span></span>](../grids.md#bkmk_gridcontext)

[<span data-ttu-id="ffdad-119">Grids and subgrids in Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="ffdad-119">Grids and subgrids in Customer Engagement</span></span>](../grids.md)


