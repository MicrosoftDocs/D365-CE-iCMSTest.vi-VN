---
title: formContext.ui.tabs (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Learn about working with processes in Customer Engagement using client API.
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 1888a882-7dfc-41a8-9bb4-d693d6046666
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 117512b080f9b36e8f4e84f2ca8e65443144fd90
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385558"
---
# <a name="formcontextuitabs-client-api-reference"></a><span data-ttu-id="54d26-103">formContext.ui.tabs (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="54d26-103">formContext.ui.tabs (Client API reference)</span></span>

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="54d26-104">Thẻ là nhóm các phần trên một trang.</span><span class="sxs-lookup"><span data-stu-id="54d26-104">A tab is a group of sections on a page.</span></span> <span data-ttu-id="54d26-105">It contains properties and methods to manipulate tabs as well as access to sections within the tab through the sections collection.</span><span class="sxs-lookup"><span data-stu-id="54d26-105">It contains properties and methods to manipulate tabs as well as access to sections within the tab through the sections collection.</span></span>

<span data-ttu-id="54d26-106">You can retrieve a tab object (say **tabObj**) by using the following example code:</span><span class="sxs-lookup"><span data-stu-id="54d26-106">You can retrieve a tab object (say **tabObj**) by using the following example code:</span></span>

```JavaScript
var tabObj = formContext.ui.tabs.get(arg);
```

## <a name="properties"></a><span data-ttu-id="54d26-107">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="54d26-107">Properties</span></span>

- <span data-ttu-id="54d26-108">**Sections**: The sections collection provides access to sections within the tab. See [Collections (Client API reference)](collections.md) for information about methods to access the sections in the collection.</span><span class="sxs-lookup"><span data-stu-id="54d26-108">**Sections**: The sections collection provides access to sections within the tab. See [Collections (Client API reference)](collections.md) for information about methods to access the sections in the collection.</span></span> <span data-ttu-id="54d26-109">See [formContext.ui section](formContext-ui-sections.md) for information about the properties and methods of the section objects in the collection.</span><span class="sxs-lookup"><span data-stu-id="54d26-109">See [formContext.ui section](formContext-ui-sections.md) for information about the properties and methods of the section objects in the collection.</span></span>

## <a name="methods"></a><span data-ttu-id="54d26-110">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="54d26-110">Methods</span></span>

|                                <span data-ttu-id="54d26-111">Tên</span><span class="sxs-lookup"><span data-stu-id="54d26-111">Name</span></span>                                 |                                                                  <span data-ttu-id="54d26-112">Mô tả</span><span class="sxs-lookup"><span data-stu-id="54d26-112">Description</span></span>                                                                   |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
|    [<span data-ttu-id="54d26-113">addTabStateChange</span><span class="sxs-lookup"><span data-stu-id="54d26-113">addTabStateChange</span></span>](formcontext-ui-tabs/addTabStateChange.md)    |    [!INCLUDE[formcontext-ui-tabs/includes/addTabStateChange-description.md](formcontext-ui-tabs/includes/addTabStateChange-description.md)]    |
|      [<span data-ttu-id="54d26-114">getDisplayState</span><span class="sxs-lookup"><span data-stu-id="54d26-114">getDisplayState</span></span>](formcontext-ui-tabs/getDisplayState.md)      |      [!INCLUDE[formcontext-ui-tabs/includes/getDisplayState-description.md](formcontext-ui-tabs/includes/getDisplayState-description.md)]      |
|             [<span data-ttu-id="54d26-115">getLabel</span><span class="sxs-lookup"><span data-stu-id="54d26-115">getLabel</span></span>](formcontext-ui-tabs/getLabel.md)             |             [!INCLUDE[formcontext-ui-tabs/includes/getLabel-description.md](formcontext-ui-tabs/includes/getLabel-description.md)]             |
|              [<span data-ttu-id="54d26-116">getName</span><span class="sxs-lookup"><span data-stu-id="54d26-116">getName</span></span>](formcontext-ui-tabs/getName.md)              |              [!INCLUDE[formcontext-ui-tabs/includes/getName-description.md](formcontext-ui-tabs/includes/getName-description.md)]              |
|            [<span data-ttu-id="54d26-117">getParent</span><span class="sxs-lookup"><span data-stu-id="54d26-117">getParent</span></span>](formcontext-ui-tabs/getParent.md)            |            [!INCLUDE[formcontext-ui-tabs/includes/getParent-description.md](formcontext-ui-tabs/includes/getParent-description.md)]            |
|           [<span data-ttu-id="54d26-118">getVisible</span><span class="sxs-lookup"><span data-stu-id="54d26-118">getVisible</span></span>](formcontext-ui-tabs/getVisible.md)           |           [!INCLUDE[formcontext-ui-tabs/includes/getVisible-description.md](formcontext-ui-tabs/includes/getVisible-description.md)]           |
| [<span data-ttu-id="54d26-119">removeTabStateChange</span><span class="sxs-lookup"><span data-stu-id="54d26-119">removeTabStateChange</span></span>](formcontext-ui-tabs/removeTabStateChange.md) | [!INCLUDE[formcontext-ui-tabs/includes/removeTabStateChange-description.md](formcontext-ui-tabs/includes/removeTabStateChange-description.md)] |
|      [<span data-ttu-id="54d26-120">setDisplayState</span><span class="sxs-lookup"><span data-stu-id="54d26-120">setDisplayState</span></span>](formcontext-ui-tabs/setDisplayState.md)      |      [!INCLUDE[formcontext-ui-tabs/includes/setDisplayState-description.md](formcontext-ui-tabs/includes/setDisplayState-description.md)]      |
|             [<span data-ttu-id="54d26-121">setFocus</span><span class="sxs-lookup"><span data-stu-id="54d26-121">setFocus</span></span>](formcontext-ui-tabs/setFocus.md)             |             [!INCLUDE[formcontext-ui-tabs/includes/setFocus-description.md](formcontext-ui-tabs/includes/setFocus-description.md)]             |
|             [<span data-ttu-id="54d26-122">setLabel</span><span class="sxs-lookup"><span data-stu-id="54d26-122">setLabel</span></span>](formcontext-ui-tabs/setLabel.md)             |             [!INCLUDE[formcontext-ui-tabs/includes/setLabel-description.md](formcontext-ui-tabs/includes/setLabel-description.md)]             |
|           [<span data-ttu-id="54d26-123">setVisible</span><span class="sxs-lookup"><span data-stu-id="54d26-123">setVisible</span></span>](formcontext-ui-tabs/setVisible.md)           |           [!INCLUDE[formcontext-ui-tabs/includes/setVisible-description.md](formcontext-ui-tabs/includes/setVisible-description.md)]           |

### <a name="related-topics"></a><span data-ttu-id="54d26-124">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="54d26-124">Related topics</span></span>

[<span data-ttu-id="54d26-125">formcontext.ui.tabs</span><span class="sxs-lookup"><span data-stu-id="54d26-125">formcontext.ui.tabs</span></span>](formcontext-ui-tabs.md)

[<span data-ttu-id="54d26-126">formContext</span><span class="sxs-lookup"><span data-stu-id="54d26-126">formContext</span></span>](../clientapi-form-context.md)

