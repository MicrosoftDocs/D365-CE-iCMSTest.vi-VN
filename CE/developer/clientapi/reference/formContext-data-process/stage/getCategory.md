---
title: getCategory (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 2849a9e1-b2fb-464c-8fc7-90b0df027c86
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0729f6861804036ca1abba59f3c20ec107ed3262
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385525"
---
# <a name="getcategory-client-api-reference"></a><span data-ttu-id="4bb7d-102">getCategory (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="4bb7d-102">getCategory (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getCategory-description.md](./includes/getCategory-description.md)]

## <a name="syntax"></a><span data-ttu-id="4bb7d-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="4bb7d-103">Syntax</span></span>

`var stageCategoryNumber = stageObj.getCategory().getValue();`

## <a name="return-value"></a><span data-ttu-id="4bb7d-104">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="4bb7d-104">Return Value</span></span>

<span data-ttu-id="4bb7d-105">**Type**: Number.</span><span class="sxs-lookup"><span data-stu-id="4bb7d-105">**Type**: Number.</span></span> 

<span data-ttu-id="4bb7d-106">**Description**: Here is the list of possible values.</span><span class="sxs-lookup"><span data-stu-id="4bb7d-106">**Description**: Here is the list of possible values.</span></span>

|<span data-ttu-id="4bb7d-107">Value</span><span class="sxs-lookup"><span data-stu-id="4bb7d-107">Value</span></span> |<span data-ttu-id="4bb7d-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="4bb7d-108">Description</span></span>|
|--|--|
|<span data-ttu-id="4bb7d-109">0</span><span class="sxs-lookup"><span data-stu-id="4bb7d-109">0</span></span>|<span data-ttu-id="4bb7d-110">Bao gồm</span><span class="sxs-lookup"><span data-stu-id="4bb7d-110">Qualify</span></span>|
|<span data-ttu-id="4bb7d-111">1</span><span class="sxs-lookup"><span data-stu-id="4bb7d-111">1</span></span>|<span data-ttu-id="4bb7d-112">Phát triển</span><span class="sxs-lookup"><span data-stu-id="4bb7d-112">Develop</span></span>|
|<span data-ttu-id="4bb7d-113">2</span><span class="sxs-lookup"><span data-stu-id="4bb7d-113">2</span></span>|<span data-ttu-id="4bb7d-114">Đề xuất</span><span class="sxs-lookup"><span data-stu-id="4bb7d-114">Propose</span></span>|
|<span data-ttu-id="4bb7d-115">3</span><span class="sxs-lookup"><span data-stu-id="4bb7d-115">3</span></span>|<span data-ttu-id="4bb7d-116">Đóng</span><span class="sxs-lookup"><span data-stu-id="4bb7d-116">Close</span></span>|
|<span data-ttu-id="4bb7d-117">4</span><span class="sxs-lookup"><span data-stu-id="4bb7d-117">4</span></span>|<span data-ttu-id="4bb7d-118">Identify</span><span class="sxs-lookup"><span data-stu-id="4bb7d-118">Identify</span></span>|
|<span data-ttu-id="4bb7d-119">5</span><span class="sxs-lookup"><span data-stu-id="4bb7d-119">5</span></span>|<span data-ttu-id="4bb7d-120">Research</span><span class="sxs-lookup"><span data-stu-id="4bb7d-120">Research</span></span>|
|<span data-ttu-id="4bb7d-121">6</span><span class="sxs-lookup"><span data-stu-id="4bb7d-121">6</span></span>|<span data-ttu-id="4bb7d-122">Resolve</span><span class="sxs-lookup"><span data-stu-id="4bb7d-122">Resolve</span></span>|

### <a name="related-topics"></a><span data-ttu-id="4bb7d-123">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="4bb7d-123">Related topics</span></span>

[<span data-ttu-id="4bb7d-124">formContext.data.process</span><span class="sxs-lookup"><span data-stu-id="4bb7d-124">formContext.data.process</span></span>](../../formContext-data-process.md)
 


