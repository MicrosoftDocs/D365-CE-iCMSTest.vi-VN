---
title: getRequiredLevel (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: c0b6ea26-2a11-4a49-8ecf-fe700e782bf3
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6b6ee7539e0a0849856ed59e641ef5f0eb53fede
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387872"
---
# <a name="getrequiredlevel-client-api-reference"></a><span data-ttu-id="2c17c-102">getRequiredLevel (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="2c17c-102">getRequiredLevel (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="2c17c-103">Returns a string value indicating whether a value for the attribute is required or recommended.</span><span class="sxs-lookup"><span data-stu-id="2c17c-103">Returns a string value indicating whether a value for the attribute is required or recommended.</span></span> 

## <a name="attribute-types-supported"></a><span data-ttu-id="2c17c-104">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="2c17c-104">Attribute types supported</span></span>

<span data-ttu-id="2c17c-105">Tất cả</span><span class="sxs-lookup"><span data-stu-id="2c17c-105">All</span></span>

## <a name="syntax"></a><span data-ttu-id="2c17c-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="2c17c-106">Syntax</span></span>

`formContext.getAttribute(arg).getRequiredLevel()`

## <a name="return-value"></a><span data-ttu-id="2c17c-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="2c17c-107">Return Value</span></span>

<span data-ttu-id="2c17c-108">**Type**: String.</span><span class="sxs-lookup"><span data-stu-id="2c17c-108">**Type**: String.</span></span> 

<span data-ttu-id="2c17c-109">**Description**: Returns one of the following values:</span><span class="sxs-lookup"><span data-stu-id="2c17c-109">**Description**: Returns one of the following values:</span></span>
- <span data-ttu-id="2c17c-110">không</span><span class="sxs-lookup"><span data-stu-id="2c17c-110">none</span></span>
- <span data-ttu-id="2c17c-111">required</span><span class="sxs-lookup"><span data-stu-id="2c17c-111">required</span></span>
- <span data-ttu-id="2c17c-112">recommended</span><span class="sxs-lookup"><span data-stu-id="2c17c-112">recommended</span></span>

### <a name="related-topic"></a><span data-ttu-id="2c17c-113">Related topic</span><span class="sxs-lookup"><span data-stu-id="2c17c-113">Related topic</span></span>
[<span data-ttu-id="2c17c-114">setRequiredLevel (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="2c17c-114">setRequiredLevel (Client API reference)</span></span>](setRequiredLevel.md)
