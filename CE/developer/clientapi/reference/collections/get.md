---
title: get method for collections (Client API reference) in Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
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
ms.openlocfilehash: edef3ef6934fecb254295f900b82590ae5d5f8f7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387786"
---
# <a name="get-method-for-collections-client-api-reference"></a><span data-ttu-id="d83b4-102">get method for collections (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="d83b4-102">get method for collections (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/get-description.md](./includes/get-description.md)]

## <a name="syntax"></a><span data-ttu-id="d83b4-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="d83b4-103">Syntax</span></span>

`collection.get([String][Number][delegate function(attribute, index)])`

## <a name="parameters"></a><span data-ttu-id="d83b4-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="d83b4-104">Parameters</span></span>

|<span data-ttu-id="d83b4-105">Tham số</span><span class="sxs-lookup"><span data-stu-id="d83b4-105">Parameter</span></span>  |<span data-ttu-id="d83b4-106">Return value</span><span class="sxs-lookup"><span data-stu-id="d83b4-106">Return value</span></span> |<span data-ttu-id="d83b4-107">Loại trả về</span><span class="sxs-lookup"><span data-stu-id="d83b4-107">Return type</span></span>  |
|---------|------|-------|
|<span data-ttu-id="d83b4-108">Không có</span><span class="sxs-lookup"><span data-stu-id="d83b4-108">None</span></span>  |<span data-ttu-id="d83b4-109">All the objects in the collection</span><span class="sxs-lookup"><span data-stu-id="d83b4-109">All the objects in the collection</span></span>  |<span data-ttu-id="d83b4-110">Mảng</span><span class="sxs-lookup"><span data-stu-id="d83b4-110">Array</span></span>|
|<span data-ttu-id="d83b4-111">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="d83b4-111">String</span></span>  |<span data-ttu-id="d83b4-112">The object where the name matches the argument</span><span class="sxs-lookup"><span data-stu-id="d83b4-112">The object where the name matches the argument</span></span><br/><br/><span data-ttu-id="d83b4-113">The objects returned in the **formContext.data.process** namespace don’t contain names.</span><span class="sxs-lookup"><span data-stu-id="d83b4-113">The objects returned in the **formContext.data.process** namespace don’t contain names.</span></span> <span data-ttu-id="d83b4-114">So, using the string parameter for this method returns no objects.</span><span class="sxs-lookup"><span data-stu-id="d83b4-114">So, using the string parameter for this method returns no objects.</span></span>  |<span data-ttu-id="d83b4-115">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="d83b4-115">Object</span></span>|
|<span data-ttu-id="d83b4-116">Số</span><span class="sxs-lookup"><span data-stu-id="d83b4-116">Number</span></span>  |<span data-ttu-id="d83b4-117">The object where the index matches the number</span><span class="sxs-lookup"><span data-stu-id="d83b4-117">The object where the index matches the number</span></span>  |<span data-ttu-id="d83b4-118">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="d83b4-118">Object</span></span>|
|<span data-ttu-id="d83b4-119">delegate function(attribute, index)</span><span class="sxs-lookup"><span data-stu-id="d83b4-119">delegate function(attribute, index)</span></span>  |<span data-ttu-id="d83b4-120">Any objects that cause the delegate function to return **true**.</span><span class="sxs-lookup"><span data-stu-id="d83b4-120">Any objects that cause the delegate function to return **true**.</span></span>  |<span data-ttu-id="d83b4-121">Mảng</span><span class="sxs-lookup"><span data-stu-id="d83b4-121">Array</span></span>|


### <a name="related-topics"></a><span data-ttu-id="d83b4-122">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="d83b4-122">Related topics</span></span>
[<span data-ttu-id="d83b4-123">Collections in Client API</span><span class="sxs-lookup"><span data-stu-id="d83b4-123">Collections in Client API</span></span>](../collections.md)

[<span data-ttu-id="d83b4-124">forEach</span><span class="sxs-lookup"><span data-stu-id="d83b4-124">forEach</span></span>](forEach.md)

[<span data-ttu-id="d83b4-125">getLength</span><span class="sxs-lookup"><span data-stu-id="d83b4-125">getLength</span></span>](getLength.md)

