---
title: addOnPostSearch (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: c398dbca-0ead-487a-8a92-35b1f2953bf6
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: fd6e6f9426297f8424916a5a5020b6c787325cd1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388439"
---
# <a name="removeonpostsearch-client-api-reference"></a><span data-ttu-id="80093-102">removeOnPostSearch (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="80093-102">removeOnPostSearch (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="80093-103">Removes an event handler from the [PostSearch](../events/postsearch.md) event.</span><span class="sxs-lookup"><span data-stu-id="80093-103">Removes an event handler from the [PostSearch](../events/postsearch.md) event.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="80093-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="80093-104">Control types supported</span></span>

<span data-ttu-id="80093-105">knowledge base search control</span><span class="sxs-lookup"><span data-stu-id="80093-105">knowledge base search control</span></span>

## <a name="syntax"></a><span data-ttu-id="80093-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="80093-106">Syntax</span></span>

```
var kbSearchControl = formContext.getControl("<name>";
kbSearchControl.removeOnPostSearch(myFunction);
```

## <a name="parameters"></a><span data-ttu-id="80093-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="80093-107">Parameters</span></span>

|<span data-ttu-id="80093-108">Tên</span><span class="sxs-lookup"><span data-stu-id="80093-108">Name</span></span> | <span data-ttu-id="80093-109">Loại</span><span class="sxs-lookup"><span data-stu-id="80093-109">Type</span></span> | <span data-ttu-id="80093-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="80093-110">Required</span></span> | <span data-ttu-id="80093-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="80093-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="80093-112">myFunction</span><span class="sxs-lookup"><span data-stu-id="80093-112">myFunction</span></span> |<span data-ttu-id="80093-113">Hàm</span><span class="sxs-lookup"><span data-stu-id="80093-113">Function</span></span> |<span data-ttu-id="80093-114">Có</span><span class="sxs-lookup"><span data-stu-id="80093-114">Yes</span></span>|<span data-ttu-id="80093-115">The function to remove from the **PostSearch** event.</span><span class="sxs-lookup"><span data-stu-id="80093-115">The function to remove from the **PostSearch** event.</span></span>| 

### <a name="related-topics"></a><span data-ttu-id="80093-116">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="80093-116">Related topics</span></span>

[<span data-ttu-id="80093-117">PostSearch event</span><span class="sxs-lookup"><span data-stu-id="80093-117">PostSearch event</span></span>](../events/postsearch.md)

[<span data-ttu-id="80093-118">addOnPostSearch</span><span class="sxs-lookup"><span data-stu-id="80093-118">addOnPostSearch</span></span>](addOnPostSearch.md) 


