---
title: getControlType (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
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
ms.openlocfilehash: 61ae1c58e11465fbec6b3d2a008474cfc284c95b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386719"
---
# <a name="getcontroltype-client-api-reference"></a><span data-ttu-id="8bb6d-102">getControlType (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="8bb6d-102">getControlType (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="8bb6d-103">Returns a value that categorizes controls.</span><span class="sxs-lookup"><span data-stu-id="8bb6d-103">Returns a value that categorizes controls.</span></span>

## <a name="control-types-supported"></a><span data-ttu-id="8bb6d-104">Control Types supported</span><span class="sxs-lookup"><span data-stu-id="8bb6d-104">Control Types supported</span></span>

<span data-ttu-id="8bb6d-105">Tất cả</span><span class="sxs-lookup"><span data-stu-id="8bb6d-105">All</span></span>

## <a name="syntax"></a><span data-ttu-id="8bb6d-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="8bb6d-106">Syntax</span></span>

`getControl(arg).getControlType();`

<span data-ttu-id="8bb6d-107">**Return Value**:</span><span class="sxs-lookup"><span data-stu-id="8bb6d-107">**Return Value**:</span></span>

<span data-ttu-id="8bb6d-108">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="8bb6d-108">**Type**: String</span></span>

|<span data-ttu-id="8bb6d-109">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="8bb6d-109">Return Value</span></span> |<span data-ttu-id="8bb6d-110">Decsription</span><span class="sxs-lookup"><span data-stu-id="8bb6d-110">Decsription</span></span>|
|--|--|
|<span data-ttu-id="8bb6d-111">standard</span><span class="sxs-lookup"><span data-stu-id="8bb6d-111">standard</span></span>|<span data-ttu-id="8bb6d-112">A standard control</span><span class="sxs-lookup"><span data-stu-id="8bb6d-112">A standard control</span></span>|
|<span data-ttu-id="8bb6d-113">iframe</span><span class="sxs-lookup"><span data-stu-id="8bb6d-113">iframe</span></span>|<span data-ttu-id="8bb6d-114">An IFRAME control</span><span class="sxs-lookup"><span data-stu-id="8bb6d-114">An IFRAME control</span></span>|
|<span data-ttu-id="8bb6d-115">kbsearch</span><span class="sxs-lookup"><span data-stu-id="8bb6d-115">kbsearch</span></span>|<span data-ttu-id="8bb6d-116">A knowledge base search control</span><span class="sxs-lookup"><span data-stu-id="8bb6d-116">A knowledge base search control</span></span>|
|<span data-ttu-id="8bb6d-117">lookup</span><span class="sxs-lookup"><span data-stu-id="8bb6d-117">lookup</span></span>|<span data-ttu-id="8bb6d-118">A lookup control</span><span class="sxs-lookup"><span data-stu-id="8bb6d-118">A lookup control</span></span>|
|<span data-ttu-id="8bb6d-119">multiselectoptionset</span><span class="sxs-lookup"><span data-stu-id="8bb6d-119">multiselectoptionset</span></span>|<span data-ttu-id="8bb6d-120">A multi-select option set control</span><span class="sxs-lookup"><span data-stu-id="8bb6d-120">A multi-select option set control</span></span>|
|<span data-ttu-id="8bb6d-121">notes</span><span class="sxs-lookup"><span data-stu-id="8bb6d-121">notes</span></span>|<span data-ttu-id="8bb6d-122">A notes control</span><span class="sxs-lookup"><span data-stu-id="8bb6d-122">A notes control</span></span>|
|<span data-ttu-id="8bb6d-123">optionset</span><span class="sxs-lookup"><span data-stu-id="8bb6d-123">optionset</span></span>|<span data-ttu-id="8bb6d-124">An option set control</span><span class="sxs-lookup"><span data-stu-id="8bb6d-124">An option set control</span></span>|
|<span data-ttu-id="8bb6d-125">quickform</span><span class="sxs-lookup"><span data-stu-id="8bb6d-125">quickform</span></span> | <span data-ttu-id="8bb6d-126">A [quick view](../formContext-ui-quickForms.md) control</span><span class="sxs-lookup"><span data-stu-id="8bb6d-126">A [quick view](../formContext-ui-quickForms.md) control</span></span>|
|<span data-ttu-id="8bb6d-127">subgrid</span><span class="sxs-lookup"><span data-stu-id="8bb6d-127">subgrid</span></span> | <span data-ttu-id="8bb6d-128">A [subgrid](../grids.md) control</span><span class="sxs-lookup"><span data-stu-id="8bb6d-128">A [subgrid](../grids.md) control</span></span>|
|<span data-ttu-id="8bb6d-129">timercontrol</span><span class="sxs-lookup"><span data-stu-id="8bb6d-129">timercontrol</span></span> | <span data-ttu-id="8bb6d-130">A timer control</span><span class="sxs-lookup"><span data-stu-id="8bb6d-130">A timer control</span></span>|
|<span data-ttu-id="8bb6d-131">timelinewall</span><span class="sxs-lookup"><span data-stu-id="8bb6d-131">timelinewall</span></span> | <span data-ttu-id="8bb6d-132">A timeline control (for Unified Interface)</span><span class="sxs-lookup"><span data-stu-id="8bb6d-132">A timeline control (for Unified Interface)</span></span>|
|<span data-ttu-id="8bb6d-133">webresource</span><span class="sxs-lookup"><span data-stu-id="8bb6d-133">webresource</span></span> | <span data-ttu-id="8bb6d-134">A web resource control</span><span class="sxs-lookup"><span data-stu-id="8bb6d-134">A web resource control</span></span>|
|<span data-ttu-id="8bb6d-135">customcontrol: \<*namespace*>.\<*name*></span><span class="sxs-lookup"><span data-stu-id="8bb6d-135">customcontrol: \<*namespace*>.\<*name*></span></span> | <span data-ttu-id="8bb6d-136">A custom control for Dynamics 365 for Customer Engagement apps mobile clients (phones and tablets)</span><span class="sxs-lookup"><span data-stu-id="8bb6d-136">A custom control for Dynamics 365 for Customer Engagement apps mobile clients (phones and tablets)</span></span>|
|<span data-ttu-id="8bb6d-137">customsubgrid:\<*namespace*>.\<*name*></span><span class="sxs-lookup"><span data-stu-id="8bb6d-137">customsubgrid:\<*namespace*>.\<*name*></span></span> | <span data-ttu-id="8bb6d-138">A custom dataset control for Dynamics 365 for Customer Engagement apps mobile clients (phones and tablets)</span><span class="sxs-lookup"><span data-stu-id="8bb6d-138">A custom dataset control for Dynamics 365 for Customer Engagement apps mobile clients (phones and tablets)</span></span>|

### <a name="related-topics"></a><span data-ttu-id="8bb6d-139">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="8bb6d-139">Related topics</span></span>

[<span data-ttu-id="8bb6d-140">Kiểm soát</span><span class="sxs-lookup"><span data-stu-id="8bb6d-140">Controls</span></span>](../controls.md)

[<span data-ttu-id="8bb6d-141">getControl</span><span class="sxs-lookup"><span data-stu-id="8bb6d-141">getControl</span></span>](getcontrol.md)


