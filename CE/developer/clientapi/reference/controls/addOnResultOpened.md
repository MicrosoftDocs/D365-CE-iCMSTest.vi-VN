---
title: addOnResultOpened (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 5f0eabe1-985a-4e89-b23a-72657208ae7e
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7cf70763e1f6e404eb9c278797949ef80ab0fdc8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388390"
---
# <a name="addonresultopened-client-api-reference"></a><span data-ttu-id="80e61-102">addOnResultOpened (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="80e61-102">addOnResultOpened (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="80e61-103">Adds an event handler to the [OnResultOpened](../events/onresultopened.md) event.</span><span class="sxs-lookup"><span data-stu-id="80e61-103">Adds an event handler to the [OnResultOpened](../events/onresultopened.md) event.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="80e61-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="80e61-104">Control types supported</span></span>

<span data-ttu-id="80e61-105">knowledge base search control</span><span class="sxs-lookup"><span data-stu-id="80e61-105">knowledge base search control</span></span>

## <a name="syntax"></a><span data-ttu-id="80e61-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="80e61-106">Syntax</span></span>

```
var kbSearchControl = formContext.getControl("<name>");
kbSearchControl.addOnResultOpened(myFunction);
```

## <a name="parameters"></a><span data-ttu-id="80e61-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="80e61-107">Parameters</span></span>

|<span data-ttu-id="80e61-108">Tên</span><span class="sxs-lookup"><span data-stu-id="80e61-108">Name</span></span> | <span data-ttu-id="80e61-109">Loại</span><span class="sxs-lookup"><span data-stu-id="80e61-109">Type</span></span> | <span data-ttu-id="80e61-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="80e61-110">Required</span></span> | <span data-ttu-id="80e61-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="80e61-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="80e61-112">myFunction</span><span class="sxs-lookup"><span data-stu-id="80e61-112">myFunction</span></span> |<span data-ttu-id="80e61-113">Hàm</span><span class="sxs-lookup"><span data-stu-id="80e61-113">Function</span></span> |<span data-ttu-id="80e61-114">Có</span><span class="sxs-lookup"><span data-stu-id="80e61-114">Yes</span></span>|<span data-ttu-id="80e61-115">The function to add to the **OnResultOpened** event.</span><span class="sxs-lookup"><span data-stu-id="80e61-115">The function to add to the **OnResultOpened** event.</span></span> <span data-ttu-id="80e61-116">The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.</span><span class="sxs-lookup"><span data-stu-id="80e61-116">The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="80e61-117">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="80e61-117">Related topics</span></span>

[<span data-ttu-id="80e61-118">OnResultOpened event</span><span class="sxs-lookup"><span data-stu-id="80e61-118">OnResultOpened event</span></span>](../events/onresultopened.md)

[<span data-ttu-id="80e61-119">removeOnResultOpened</span><span class="sxs-lookup"><span data-stu-id="80e61-119">removeOnResultOpened</span></span>](removeOnResultOpened.md)
