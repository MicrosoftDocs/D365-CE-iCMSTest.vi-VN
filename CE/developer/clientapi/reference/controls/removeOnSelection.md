---
title: removeOnSelection (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 3ca41e3e-af2b-4aa8-8233-64a8c276d0ef
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2bd8b1034dba9659b388ae9b0954966633a763a7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386526"
---
# <a name="removeonselection-client-api-reference"></a><span data-ttu-id="4f3ec-102">removeOnSelection (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="4f3ec-102">removeOnSelection (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="4f3ec-103">Removes an event handler from the [OnSelection](../events/onselection.md) event.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-103">Removes an event handler from the [OnSelection](../events/onselection.md) event.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="4f3ec-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="4f3ec-104">Control types supported</span></span>

<span data-ttu-id="4f3ec-105">Điều khiển tìm kiếm cơ sở Kiến thức</span><span class="sxs-lookup"><span data-stu-id="4f3ec-105">Knowledge base search control</span></span>

## <a name="syntax"></a><span data-ttu-id="4f3ec-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="4f3ec-106">Syntax</span></span>

```
var kbSearchControl = formContext.getControl("<name>");
kbSearchControl.removeOnSelection(myFunction);
```

## <a name="parameters"></a><span data-ttu-id="4f3ec-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="4f3ec-107">Parameters</span></span>

|<span data-ttu-id="4f3ec-108">Tên</span><span class="sxs-lookup"><span data-stu-id="4f3ec-108">Name</span></span> | <span data-ttu-id="4f3ec-109">Loại</span><span class="sxs-lookup"><span data-stu-id="4f3ec-109">Type</span></span> | <span data-ttu-id="4f3ec-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="4f3ec-110">Required</span></span> | <span data-ttu-id="4f3ec-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="4f3ec-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="4f3ec-112">myFunction</span><span class="sxs-lookup"><span data-stu-id="4f3ec-112">myFunction</span></span> |<span data-ttu-id="4f3ec-113">Hàm</span><span class="sxs-lookup"><span data-stu-id="4f3ec-113">Function</span></span> |<span data-ttu-id="4f3ec-114">Có</span><span class="sxs-lookup"><span data-stu-id="4f3ec-114">Yes</span></span>|<span data-ttu-id="4f3ec-115">The function to remove from the **OnSelection** event.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-115">The function to remove from the **OnSelection** event.</span></span>| 

### <a name="related-topics"></a><span data-ttu-id="4f3ec-116">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="4f3ec-116">Related topics</span></span>

[<span data-ttu-id="4f3ec-117">addOnSelection</span><span class="sxs-lookup"><span data-stu-id="4f3ec-117">addOnSelection</span></span>](addOnSelection.md)


