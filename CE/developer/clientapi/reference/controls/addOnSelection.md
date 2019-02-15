---
title: addOnSelection (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 66cfb2ff-4d78-4bb9-8dc0-e214ae1d2880
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0af1072cfee4d775d683a2bb8ff6ebdeaeb9ffd1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386563"
---
# <a name="addonselection-client-api-reference"></a><span data-ttu-id="ddb29-102">addOnSelection (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="ddb29-102">addOnSelection (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ddb29-103">Adds an event handler to the [OnSelection](../events/onselection.md) event.</span><span class="sxs-lookup"><span data-stu-id="ddb29-103">Adds an event handler to the [OnSelection](../events/onselection.md) event.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="ddb29-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="ddb29-104">Control types supported</span></span>

<span data-ttu-id="ddb29-105">Knowledge base search control</span><span class="sxs-lookup"><span data-stu-id="ddb29-105">Knowledge base search control</span></span>

## <a name="syntax"></a><span data-ttu-id="ddb29-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="ddb29-106">Syntax</span></span>

```
var kbSearchControl = formContext.getControl("<name>");
kbSearchControl.addOnSelection(myFunction);
```

## <a name="parameters"></a><span data-ttu-id="ddb29-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="ddb29-107">Parameters</span></span>

|<span data-ttu-id="ddb29-108">Tên</span><span class="sxs-lookup"><span data-stu-id="ddb29-108">Name</span></span> | <span data-ttu-id="ddb29-109">Loại</span><span class="sxs-lookup"><span data-stu-id="ddb29-109">Type</span></span> | <span data-ttu-id="ddb29-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="ddb29-110">Required</span></span> | <span data-ttu-id="ddb29-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="ddb29-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="ddb29-112">myFunction</span><span class="sxs-lookup"><span data-stu-id="ddb29-112">myFunction</span></span> |<span data-ttu-id="ddb29-113">Hàm</span><span class="sxs-lookup"><span data-stu-id="ddb29-113">Function</span></span> |<span data-ttu-id="ddb29-114">Có</span><span class="sxs-lookup"><span data-stu-id="ddb29-114">Yes</span></span>|<span data-ttu-id="ddb29-115">The function to add to the **OnSelection** event.</span><span class="sxs-lookup"><span data-stu-id="ddb29-115">The function to add to the **OnSelection** event.</span></span> <span data-ttu-id="ddb29-116">The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.</span><span class="sxs-lookup"><span data-stu-id="ddb29-116">The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="ddb29-117">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="ddb29-117">Related topics</span></span>

[<span data-ttu-id="ddb29-118">OnSelection event</span><span class="sxs-lookup"><span data-stu-id="ddb29-118">OnSelection event</span></span>](../events/onselection.md)

[<span data-ttu-id="ddb29-119">removeOnSelection</span><span class="sxs-lookup"><span data-stu-id="ddb29-119">removeOnSelection</span></span>](removeOnSelection.md)
