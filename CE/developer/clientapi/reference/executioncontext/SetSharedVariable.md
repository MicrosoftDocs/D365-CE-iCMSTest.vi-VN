---
title: setSharedVariable (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Learn about the getEventSource method that returns a reference to the form or an item on the form depending on where the method was called.
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 702a13c1-f4ae-4de2-9e8b-95360ad9240c
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3a48c3169d57fb1febc97f76717943963418a8f2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385965"
---
# <a name="setsharedvariable-client-api-reference"></a><span data-ttu-id="095ae-103">setSharedVariable (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="095ae-103">setSharedVariable (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="095ae-104">Sets the value of a variable to be used by a handler after the current handler completes.</span><span class="sxs-lookup"><span data-stu-id="095ae-104">Sets the value of a variable to be used by a handler after the current handler completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="095ae-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="095ae-105">Syntax</span></span>

`ExecutionContextObj.setSharedVariable(key, value)`

## <a name="parameters"></a><span data-ttu-id="095ae-106">Tham số</span><span class="sxs-lookup"><span data-stu-id="095ae-106">Parameters</span></span>

- <span data-ttu-id="095ae-107">**key**: String: The name of the variable</span><span class="sxs-lookup"><span data-stu-id="095ae-107">**key**: String: The name of the variable</span></span>
- <span data-ttu-id="095ae-108">**Value**: Object.</span><span class="sxs-lookup"><span data-stu-id="095ae-108">**Value**: Object.</span></span> <span data-ttu-id="095ae-109">The values to set</span><span class="sxs-lookup"><span data-stu-id="095ae-109">The values to set</span></span>



## <a name="return-value"></a><span data-ttu-id="095ae-110">Return value</span><span class="sxs-lookup"><span data-stu-id="095ae-110">Return value</span></span>

<span data-ttu-id="095ae-111">**Type**: Object</span><span class="sxs-lookup"><span data-stu-id="095ae-111">**Type**: Object</span></span>

<span data-ttu-id="095ae-112">**Description**: The specific type depends on what the value object is.</span><span class="sxs-lookup"><span data-stu-id="095ae-112">**Description**: The specific type depends on what the value object is.</span></span>

### <a name="related-topics"></a><span data-ttu-id="095ae-113">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="095ae-113">Related topics</span></span>
[<span data-ttu-id="095ae-114">getSharedVariable</span><span class="sxs-lookup"><span data-stu-id="095ae-114">getSharedVariable</span></span>](getSharedVariable.md)

[<span data-ttu-id="095ae-115">Execution context</span><span class="sxs-lookup"><span data-stu-id="095ae-115">Execution context</span></span>](../execution-context.md)





