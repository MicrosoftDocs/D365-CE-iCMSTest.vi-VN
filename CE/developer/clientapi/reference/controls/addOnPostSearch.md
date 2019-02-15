---
title: addOnPostSearch (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/04/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9d000628-5dbe-45bd-9c47-e19187ffdae7
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: bbed161a94b47159aa4e47003f1ad153fbc623dd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388393"
---
# <a name="addonpostsearch-client-api-reference"></a><span data-ttu-id="b5ea9-102">addOnPostSearch (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="b5ea9-102">addOnPostSearch (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b5ea9-103">Adds an event handler to the [PostSearch](../events/postsearch.md) event.</span><span class="sxs-lookup"><span data-stu-id="b5ea9-103">Adds an event handler to the [PostSearch](../events/postsearch.md) event.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="b5ea9-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="b5ea9-104">Control types supported</span></span>

<span data-ttu-id="b5ea9-105">knowledge base search control</span><span class="sxs-lookup"><span data-stu-id="b5ea9-105">knowledge base search control</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ea9-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="b5ea9-106">Syntax</span></span>

```
var kbSearchControl = formContext.getControl("<name>");
kbSearchControl.addOnPostSearch(myFunction);
```

## <a name="parameters"></a><span data-ttu-id="b5ea9-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="b5ea9-107">Parameters</span></span>

|<span data-ttu-id="b5ea9-108">Tên</span><span class="sxs-lookup"><span data-stu-id="b5ea9-108">Name</span></span> | <span data-ttu-id="b5ea9-109">Loại</span><span class="sxs-lookup"><span data-stu-id="b5ea9-109">Type</span></span> | <span data-ttu-id="b5ea9-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="b5ea9-110">Required</span></span> | <span data-ttu-id="b5ea9-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="b5ea9-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="b5ea9-112">myFunction</span><span class="sxs-lookup"><span data-stu-id="b5ea9-112">myFunction</span></span> |<span data-ttu-id="b5ea9-113">Hàm</span><span class="sxs-lookup"><span data-stu-id="b5ea9-113">Function</span></span> |<span data-ttu-id="b5ea9-114">Có</span><span class="sxs-lookup"><span data-stu-id="b5ea9-114">Yes</span></span>|<span data-ttu-id="b5ea9-115">The function to add to the **PostSearch** event.</span><span class="sxs-lookup"><span data-stu-id="b5ea9-115">The function to add to the **PostSearch** event.</span></span> <span data-ttu-id="b5ea9-116">The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.</span><span class="sxs-lookup"><span data-stu-id="b5ea9-116">The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.</span></span>| 

### <a name="related-topics"></a><span data-ttu-id="b5ea9-117">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="b5ea9-117">Related topics</span></span>

[<span data-ttu-id="b5ea9-118">PostSearch event</span><span class="sxs-lookup"><span data-stu-id="b5ea9-118">PostSearch event</span></span>](../events/postsearch.md)

[<span data-ttu-id="b5ea9-119">removeOnPostSearch</span><span class="sxs-lookup"><span data-stu-id="b5ea9-119">removeOnPostSearch</span></span>](removeOnPostSearch.md)
