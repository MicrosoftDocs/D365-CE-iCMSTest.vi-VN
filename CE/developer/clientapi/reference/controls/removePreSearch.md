---
title: removePreSearch (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 2451c4ac-527c-4487-8f52-bde1690c5bde
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c96c3dbe2fcbfedcb5a24193b22657bd4313310d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385702"
---
# <a name="removepresearch-client-api-reference"></a><span data-ttu-id="491e3-102">removePreSearch (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="491e3-102">removePreSearch (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="491e3-103">Removes event handler functions that have previously been set for the [PreSearch](../events/PreSearch.md) event.</span><span class="sxs-lookup"><span data-stu-id="491e3-103">Removes event handler functions that have previously been set for the [PreSearch](../events/PreSearch.md) event.</span></span>

## <a name="control-types-supported"></a><span data-ttu-id="491e3-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="491e3-104">Control types supported</span></span>

<span data-ttu-id="491e3-105">Tra cứu</span><span class="sxs-lookup"><span data-stu-id="491e3-105">Lookup</span></span>

## <a name="syntax"></a><span data-ttu-id="491e3-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="491e3-106">Syntax</span></span>

`formContext.getControl(arg).removePreSearch(myFunction)`

## <a name="parameters"></a><span data-ttu-id="491e3-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="491e3-107">Parameters</span></span>

|<span data-ttu-id="491e3-108">Tên</span><span class="sxs-lookup"><span data-stu-id="491e3-108">Name</span></span> | <span data-ttu-id="491e3-109">Loại</span><span class="sxs-lookup"><span data-stu-id="491e3-109">Type</span></span> | <span data-ttu-id="491e3-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="491e3-110">Required</span></span> | <span data-ttu-id="491e3-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="491e3-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="491e3-112">myFunction</span><span class="sxs-lookup"><span data-stu-id="491e3-112">myFunction</span></span> |<span data-ttu-id="491e3-113">Hàm</span><span class="sxs-lookup"><span data-stu-id="491e3-113">Function</span></span> |<span data-ttu-id="491e3-114">Có</span><span class="sxs-lookup"><span data-stu-id="491e3-114">Yes</span></span>| <span data-ttu-id="491e3-115">The function to remove.</span><span class="sxs-lookup"><span data-stu-id="491e3-115">The function to remove.</span></span> <span data-ttu-id="491e3-116">The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.</span><span class="sxs-lookup"><span data-stu-id="491e3-116">The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="491e3-117">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="491e3-117">Related topics</span></span>

[<span data-ttu-id="491e3-118">PreSearch event</span><span class="sxs-lookup"><span data-stu-id="491e3-118">PreSearch event</span></span>](../events/PreSearch.md)

[<span data-ttu-id="491e3-119">addPreSearch</span><span class="sxs-lookup"><span data-stu-id="491e3-119">addPreSearch</span></span>](addPreSearch.md) 


