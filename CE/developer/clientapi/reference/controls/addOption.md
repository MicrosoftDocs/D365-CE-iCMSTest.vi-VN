---
title: addOption (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9798f168-7b94-411d-9aed-6471042ff11a
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: af34fb6c2ac184b24dcdebc2975897fa76392229
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388465"
---
# <a name="addoption-client-api-reference"></a><span data-ttu-id="d20e5-102">addOption (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="d20e5-102">addOption (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="d20e5-103">Adds an option to a control.</span><span class="sxs-lookup"><span data-stu-id="d20e5-103">Adds an option to a control.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="d20e5-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="d20e5-104">Control types supported</span></span>

<span data-ttu-id="d20e5-105">OptionSet, MultiSelectOptionSet</span><span class="sxs-lookup"><span data-stu-id="d20e5-105">OptionSet, MultiSelectOptionSet</span></span>

## <a name="syntax"></a><span data-ttu-id="d20e5-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="d20e5-106">Syntax</span></span>

`formContext.getControl(arg).addOption(option, index);`

## <a name="parameters"></a><span data-ttu-id="d20e5-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="d20e5-107">Parameters</span></span>

|<span data-ttu-id="d20e5-108">Tên</span><span class="sxs-lookup"><span data-stu-id="d20e5-108">Name</span></span> | <span data-ttu-id="d20e5-109">Loại</span><span class="sxs-lookup"><span data-stu-id="d20e5-109">Type</span></span> | <span data-ttu-id="d20e5-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="d20e5-110">Required</span></span> | <span data-ttu-id="d20e5-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="d20e5-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="d20e5-112">option</span><span class="sxs-lookup"><span data-stu-id="d20e5-112">option</span></span> |<span data-ttu-id="d20e5-113">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="d20e5-113">Object</span></span> |<span data-ttu-id="d20e5-114">Có</span><span class="sxs-lookup"><span data-stu-id="d20e5-114">Yes</span></span>|<span data-ttu-id="d20e5-115">The option to add.</span><span class="sxs-lookup"><span data-stu-id="d20e5-115">The option to add.</span></span> <span data-ttu-id="d20e5-116">The object contains the following attributes:</span><span class="sxs-lookup"><span data-stu-id="d20e5-116">The object contains the following attributes:</span></span><br/><span data-ttu-id="d20e5-117">**- text**: String.</span><span class="sxs-lookup"><span data-stu-id="d20e5-117">**- text**: String.</span></span> <span data-ttu-id="d20e5-118">The label for the option.</span><span class="sxs-lookup"><span data-stu-id="d20e5-118">The label for the option.</span></span><br/><span data-ttu-id="d20e5-119">**- value**: Number.</span><span class="sxs-lookup"><span data-stu-id="d20e5-119">**- value**: Number.</span></span> <span data-ttu-id="d20e5-120">The value for the option.</span><span class="sxs-lookup"><span data-stu-id="d20e5-120">The value for the option.</span></span>|
|<span data-ttu-id="d20e5-121">chỉ mục</span><span class="sxs-lookup"><span data-stu-id="d20e5-121">index</span></span> |<span data-ttu-id="d20e5-122">Số</span><span class="sxs-lookup"><span data-stu-id="d20e5-122">Number</span></span> |<span data-ttu-id="d20e5-123">Không</span><span class="sxs-lookup"><span data-stu-id="d20e5-123">No</span></span>|<span data-ttu-id="d20e5-124">The index position to place the new option in.</span><span class="sxs-lookup"><span data-stu-id="d20e5-124">The index position to place the new option in.</span></span> <span data-ttu-id="d20e5-125">If not provided, the option will be added to the end.</span><span class="sxs-lookup"><span data-stu-id="d20e5-125">If not provided, the option will be added to the end.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="d20e5-126">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="d20e5-126">Related topics</span></span>

[<span data-ttu-id="d20e5-127">clearOptions</span><span class="sxs-lookup"><span data-stu-id="d20e5-127">clearOptions</span></span>](clearOptions.md)

[<span data-ttu-id="d20e5-128">removeOption</span><span class="sxs-lookup"><span data-stu-id="d20e5-128">removeOption</span></span>](removeOption.md)
