---
title: addOnChange (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Learn about the attribute addOnchange method to set a function to be called when the attribute value is changed.
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9f3b2fed-fde5-46e4-8c59-43aa51aa82df
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 618f353e679cf0f6f220b0eaec77fb961f86c735
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385792"
---
# <a name="addonchange-client-api-reference"></a><span data-ttu-id="19f7b-103">addOnChange (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="19f7b-103">addOnChange (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="19f7b-104">Sets a function to be called when the **OnChange** event occurs.</span><span class="sxs-lookup"><span data-stu-id="19f7b-104">Sets a function to be called when the **OnChange** event occurs.</span></span>

## <a name="attribute-types-supported"></a><span data-ttu-id="19f7b-105">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="19f7b-105">Attribute types supported</span></span>

<span data-ttu-id="19f7b-106">Tất cả</span><span class="sxs-lookup"><span data-stu-id="19f7b-106">All</span></span>

## <a name="syntax"></a><span data-ttu-id="19f7b-107">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="19f7b-107">Syntax</span></span>

`formContext.getAttribute(arg).addOnChange(myFunction)`

## <a name="parameters"></a><span data-ttu-id="19f7b-108">Tham số</span><span class="sxs-lookup"><span data-stu-id="19f7b-108">Parameters</span></span>

| <span data-ttu-id="19f7b-109">Parameter Name</span><span class="sxs-lookup"><span data-stu-id="19f7b-109">Parameter Name</span></span>| <span data-ttu-id="19f7b-110">Loại</span><span class="sxs-lookup"><span data-stu-id="19f7b-110">Type</span></span>| <span data-ttu-id="19f7b-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="19f7b-111">Description</span></span>  |
| --------|-----------| -----|
|<span data-ttu-id="19f7b-112">myFunction</span><span class="sxs-lookup"><span data-stu-id="19f7b-112">myFunction</span></span>| <span data-ttu-id="19f7b-113">Function reference</span><span class="sxs-lookup"><span data-stu-id="19f7b-113">Function reference</span></span>| <span data-ttu-id="19f7b-114">Specifies the function to be executed on the attribute **OnChange** event.</span><span class="sxs-lookup"><span data-stu-id="19f7b-114">Specifies the function to be executed on the attribute **OnChange** event.</span></span> <span data-ttu-id="19f7b-115">The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.</span><span class="sxs-lookup"><span data-stu-id="19f7b-115">The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.</span></span>|


### <a name="related-topics"></a><span data-ttu-id="19f7b-116">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="19f7b-116">Related topics</span></span>

[<span data-ttu-id="19f7b-117">removeOnChange</span><span class="sxs-lookup"><span data-stu-id="19f7b-117">removeOnChange</span></span>](removeOnChange.md)

[<span data-ttu-id="19f7b-118">Attribute OnChange Event</span><span class="sxs-lookup"><span data-stu-id="19f7b-118">Attribute OnChange Event</span></span>](../events/attribute-onchange.md)





