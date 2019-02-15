---
title: addPreSearch (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: d69a432a-1d74-4782-bedd-f9f30d3d7d9c
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 81094aa272839b4dbf7b4778f80a4f4062bc6f66
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388130"
---
# <a name="addpresearch-client-api-reference"></a><span data-ttu-id="b7516-102">addPreSearch (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="b7516-102">addPreSearch (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b7516-103">Applies changes to lookups based on values current just as the user is about to view results for the lookup.</span><span class="sxs-lookup"><span data-stu-id="b7516-103">Applies changes to lookups based on values current just as the user is about to view results for the lookup.</span></span>

## <a name="control-types-supported"></a><span data-ttu-id="b7516-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="b7516-104">Control types supported</span></span>

<span data-ttu-id="b7516-105">Tra cứu</span><span class="sxs-lookup"><span data-stu-id="b7516-105">Lookup</span></span>

## <a name="syntax"></a><span data-ttu-id="b7516-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="b7516-106">Syntax</span></span>

`formContext.getControl(arg).addPreSearch(myFunction)`

## <a name="parameters"></a><span data-ttu-id="b7516-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="b7516-107">Parameters</span></span>

|<span data-ttu-id="b7516-108">Tên</span><span class="sxs-lookup"><span data-stu-id="b7516-108">Name</span></span> | <span data-ttu-id="b7516-109">Loại</span><span class="sxs-lookup"><span data-stu-id="b7516-109">Type</span></span> | <span data-ttu-id="b7516-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="b7516-110">Required</span></span> | <span data-ttu-id="b7516-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="b7516-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="b7516-112">myFunction</span><span class="sxs-lookup"><span data-stu-id="b7516-112">myFunction</span></span> |<span data-ttu-id="b7516-113">Hàm</span><span class="sxs-lookup"><span data-stu-id="b7516-113">Function</span></span> |<span data-ttu-id="b7516-114">Có</span><span class="sxs-lookup"><span data-stu-id="b7516-114">Yes</span></span>| <span data-ttu-id="b7516-115">The function that will be run just before the search to provide results for a lookup occurs.</span><span class="sxs-lookup"><span data-stu-id="b7516-115">The function that will be run just before the search to provide results for a lookup occurs.</span></span> <span data-ttu-id="b7516-116">You can use this function to call one of the other lookup control functions and improve the results to be displayed in the lookup.</span><span class="sxs-lookup"><span data-stu-id="b7516-116">You can use this function to call one of the other lookup control functions and improve the results to be displayed in the lookup.</span></span> <span data-ttu-id="b7516-117">The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.</span><span class="sxs-lookup"><span data-stu-id="b7516-117">The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="b7516-118">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="b7516-118">Related topics</span></span>

[<span data-ttu-id="b7516-119">PreSearch event</span><span class="sxs-lookup"><span data-stu-id="b7516-119">PreSearch event</span></span>](../events/PreSearch.md)

[<span data-ttu-id="b7516-120">removePreSearch</span><span class="sxs-lookup"><span data-stu-id="b7516-120">removePreSearch</span></span>](removePreSearch.md) 


