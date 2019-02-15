---
title: addOnRecordSelect (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4bfd7f48-5db8-45ea-816f-9d590fbdf60d
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4fa8c0f1c61615c0cbed7cfda37a6c8104cf085a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387242"
---
# <a name="addonrecordselect-client-api-reference"></a><span data-ttu-id="dab93-102">addOnRecordSelect (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="dab93-102">addOnRecordSelect (Client API reference)</span></span>

[!INCLUDE[./includes/addOnRecordSelect-description.md](./includes/addOnRecordSelect-description.md)]

## <a name="grid-types-supported"></a><span data-ttu-id="dab93-103">Grid types supported</span><span class="sxs-lookup"><span data-stu-id="dab93-103">Grid types supported</span></span>

<span data-ttu-id="dab93-104">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="dab93-104">Read-only and editable grids</span></span>

## <a name="syntax"></a><span data-ttu-id="dab93-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="dab93-105">Syntax</span></span>

`gridContext.getGrid().addOnRecordSelect(myFunction);`

|<span data-ttu-id="dab93-106">Tên</span><span class="sxs-lookup"><span data-stu-id="dab93-106">Name</span></span>|<span data-ttu-id="dab93-107">Loại</span><span class="sxs-lookup"><span data-stu-id="dab93-107">Type</span></span>|<span data-ttu-id="dab93-108">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="dab93-108">Required</span></span>|<span data-ttu-id="dab93-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="dab93-109">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="dab93-110">myFunction</span><span class="sxs-lookup"><span data-stu-id="dab93-110">myFunction</span></span>|<span data-ttu-id="dab93-111">function reference</span><span class="sxs-lookup"><span data-stu-id="dab93-111">function reference</span></span>|<span data-ttu-id="dab93-112">Có</span><span class="sxs-lookup"><span data-stu-id="dab93-112">Yes</span></span>|<span data-ttu-id="dab93-113">The function to be executed when you select record (row) in a grid.</span><span class="sxs-lookup"><span data-stu-id="dab93-113">The function to be executed when you select record (row) in a grid.</span></span> <span data-ttu-id="dab93-114">The function will be added to the bottom of the event handler pipeline.</span><span class="sxs-lookup"><span data-stu-id="dab93-114">The function will be added to the bottom of the event handler pipeline.</span></span> <span data-ttu-id="dab93-115">The execution context is automatically passed as the first parameter to the function.</span><span class="sxs-lookup"><span data-stu-id="dab93-115">The execution context is automatically passed as the first parameter to the function.</span></span> <span data-ttu-id="dab93-116">See [execution context](../../../clientapi-execution-context.md) for more information.</span><span class="sxs-lookup"><span data-stu-id="dab93-116">See [execution context](../../../clientapi-execution-context.md) for more information.</span></span>

## <a name="remarks"></a><span data-ttu-id="dab93-117">Chú thích</span><span class="sxs-lookup"><span data-stu-id="dab93-117">Remarks</span></span>

<span data-ttu-id="dab93-118">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span><span class="sxs-lookup"><span data-stu-id="dab93-118">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span></span>

