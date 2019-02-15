---
title: openSearchResult (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 1f9169ce-cba3-4bb6-af20-f86140139cfe
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 42e6eda39ba74aadefcb0480d07acd175891f42c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385672"
---
# <a name="opensearchresult-client-api-reference"></a><span data-ttu-id="570ac-102">openSearchResult (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="570ac-102">openSearchResult (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="570ac-103">Opens a search result in the search control by specifying the result number..</span><span class="sxs-lookup"><span data-stu-id="570ac-103">Opens a search result in the search control by specifying the result number..</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="570ac-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="570ac-104">Control types supported</span></span>

<span data-ttu-id="570ac-105">knowledge base search control</span><span class="sxs-lookup"><span data-stu-id="570ac-105">knowledge base search control</span></span>

## <a name="syntax"></a><span data-ttu-id="570ac-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="570ac-106">Syntax</span></span>

```
var kbSearchControl = formContext.getControl("<name>");
var openResultStatus = kbSearchControl.openSearchResult(resultNumber, mode);
```

## <a name="parameter"></a><span data-ttu-id="570ac-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="570ac-107">Parameter</span></span>

|<span data-ttu-id="570ac-108">Tên</span><span class="sxs-lookup"><span data-stu-id="570ac-108">Name</span></span>|<span data-ttu-id="570ac-109">Loại</span><span class="sxs-lookup"><span data-stu-id="570ac-109">Type</span></span>|<span data-ttu-id="570ac-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="570ac-110">Required</span></span>|<span data-ttu-id="570ac-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="570ac-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="570ac-112">resultNumber</span><span class="sxs-lookup"><span data-stu-id="570ac-112">resultNumber</span></span>|<span data-ttu-id="570ac-113">Số</span><span class="sxs-lookup"><span data-stu-id="570ac-113">Number</span></span>|<span data-ttu-id="570ac-114">Có</span><span class="sxs-lookup"><span data-stu-id="570ac-114">Yes</span></span>|<span data-ttu-id="570ac-115">Numerical value specifying the result number to be opened.</span><span class="sxs-lookup"><span data-stu-id="570ac-115">Numerical value specifying the result number to be opened.</span></span> <span data-ttu-id="570ac-116">Result number starts from 1.</span><span class="sxs-lookup"><span data-stu-id="570ac-116">Result number starts from 1.</span></span>|
|<span data-ttu-id="570ac-117">mode</span><span class="sxs-lookup"><span data-stu-id="570ac-117">mode</span></span>|<span data-ttu-id="570ac-118">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="570ac-118">String</span></span>|<span data-ttu-id="570ac-119">Không</span><span class="sxs-lookup"><span data-stu-id="570ac-119">No</span></span>|<span data-ttu-id="570ac-120">Specify "Inline" or "Popout".</span><span class="sxs-lookup"><span data-stu-id="570ac-120">Specify "Inline" or "Popout".</span></span> <span data-ttu-id="570ac-121">If you do not specify a value for the argument, the default ("Inline") option is used.</span><span class="sxs-lookup"><span data-stu-id="570ac-121">If you do not specify a value for the argument, the default ("Inline") option is used.</span></span><br/><br/><span data-ttu-id="570ac-122">The "Inline" mode opens the result inline either in the reading pane of the control or in a reference panel tab in case of reference panel.</span><span class="sxs-lookup"><span data-stu-id="570ac-122">The "Inline" mode opens the result inline either in the reading pane of the control or in a reference panel tab in case of reference panel.</span></span> <span data-ttu-id="570ac-123">The "Popout" mode opens the result in a pop-out window.</span><span class="sxs-lookup"><span data-stu-id="570ac-123">The "Popout" mode opens the result in a pop-out window.</span></span>|

## <a name="return-value"></a><span data-ttu-id="570ac-124">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="570ac-124">Return Value</span></span>

<span data-ttu-id="570ac-125">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="570ac-125">**Type**: Boolean</span></span>

<span data-ttu-id="570ac-126">**Description**:  Status of opening the specified search result.</span><span class="sxs-lookup"><span data-stu-id="570ac-126">**Description**:  Status of opening the specified search result.</span></span> <span data-ttu-id="570ac-127">Returns 1 if successful; 0 if unsuccessful.</span><span class="sxs-lookup"><span data-stu-id="570ac-127">Returns 1 if successful; 0 if unsuccessful.</span></span> <span data-ttu-id="570ac-128">The method will return -1 if the specified resultNumber value is not present, or if the specified mode value is invalid.</span><span class="sxs-lookup"><span data-stu-id="570ac-128">The method will return -1 if the specified resultNumber value is not present, or if the specified mode value is invalid.</span></span>
