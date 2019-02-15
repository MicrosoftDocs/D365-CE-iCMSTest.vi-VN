---
title: removeOnLoad (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4d025f92-db16-440c-9f82-e40d71e09862
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e0051881f4f97b4344a5c114efb0d764606bf3b1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387846"
---
# <a name="removeonload-client-api-reference"></a><span data-ttu-id="26a9b-102">removeOnLoad (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="26a9b-102">removeOnLoad (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/removeOnLoad-description.md](./includes/removeOnLoad-description.md)]

## <a name="grid-types-supported"></a><span data-ttu-id="26a9b-103">Grid types supported</span><span class="sxs-lookup"><span data-stu-id="26a9b-103">Grid types supported</span></span>

<span data-ttu-id="26a9b-104">Read-only grids</span><span class="sxs-lookup"><span data-stu-id="26a9b-104">Read-only grids</span></span>

## <a name="syntax"></a><span data-ttu-id="26a9b-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="26a9b-105">Syntax</span></span>

`gridContext.removeOnLoad(myFunction);`

## <a name="parameter"></a><span data-ttu-id="26a9b-106">Tham số</span><span class="sxs-lookup"><span data-stu-id="26a9b-106">Parameter</span></span>

|<span data-ttu-id="26a9b-107">Tên</span><span class="sxs-lookup"><span data-stu-id="26a9b-107">Name</span></span>|<span data-ttu-id="26a9b-108">Loại</span><span class="sxs-lookup"><span data-stu-id="26a9b-108">Type</span></span>|<span data-ttu-id="26a9b-109">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="26a9b-109">Required</span></span>|<span data-ttu-id="26a9b-110">Mô tả</span><span class="sxs-lookup"><span data-stu-id="26a9b-110">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="26a9b-111">myFunction</span><span class="sxs-lookup"><span data-stu-id="26a9b-111">myFunction</span></span>|<span data-ttu-id="26a9b-112">function reference</span><span class="sxs-lookup"><span data-stu-id="26a9b-112">function reference</span></span>|<span data-ttu-id="26a9b-113">Có</span><span class="sxs-lookup"><span data-stu-id="26a9b-113">Yes</span></span>|<span data-ttu-id="26a9b-114">The function to be removed from the **OnLoad** event.</span><span class="sxs-lookup"><span data-stu-id="26a9b-114">The function to be removed from the **OnLoad** event.</span></span>

## <a name="remarks"></a><span data-ttu-id="26a9b-115">Chú thích</span><span class="sxs-lookup"><span data-stu-id="26a9b-115">Remarks</span></span>

<span data-ttu-id="26a9b-116">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span><span class="sxs-lookup"><span data-stu-id="26a9b-116">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span></span>

### <a name="related-topics"></a><span data-ttu-id="26a9b-117">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="26a9b-117">Related topics</span></span>

[<span data-ttu-id="26a9b-118">addOnLoad</span><span class="sxs-lookup"><span data-stu-id="26a9b-118">addOnLoad</span></span>](addOnLoad.md) 


