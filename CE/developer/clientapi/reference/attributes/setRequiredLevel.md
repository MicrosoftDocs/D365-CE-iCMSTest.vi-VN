---
title: setRequiredLevel (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 67a96fc4-4d65-4858-90da-f41eeba0365a
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3ec91975dbd973b1ae630bc9e4c68e1be2b8de6a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388185"
---
# <a name="setrequiredlevel-client-api-reference"></a><span data-ttu-id="bd762-102">setRequiredLevel (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="bd762-102">setRequiredLevel (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="bd762-103">Sets whether data is required or recommended for the attribute before the record can be saved.</span><span class="sxs-lookup"><span data-stu-id="bd762-103">Sets whether data is required or recommended for the attribute before the record can be saved.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bd762-104">Reducing the required level of an attribute can cause an error when the page is saved.</span><span class="sxs-lookup"><span data-stu-id="bd762-104">Reducing the required level of an attribute can cause an error when the page is saved.</span></span> <span data-ttu-id="bd762-105">If the attribute is required by the server, an error will occur if there is no value for the attribute.</span><span class="sxs-lookup"><span data-stu-id="bd762-105">If the attribute is required by the server, an error will occur if there is no value for the attribute.</span></span> 

## <a name="attribute-types-supported"></a><span data-ttu-id="bd762-106">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="bd762-106">Attribute types supported</span></span>

<span data-ttu-id="bd762-107">Tất cả</span><span class="sxs-lookup"><span data-stu-id="bd762-107">All</span></span>

## <a name="syntax"></a><span data-ttu-id="bd762-108">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="bd762-108">Syntax</span></span>

`formContext.getAttribute(arg).setRequiredLevel(requirementLevel)`

## <a name="parameters"></a><span data-ttu-id="bd762-109">Tham số</span><span class="sxs-lookup"><span data-stu-id="bd762-109">Parameters</span></span>

<span data-ttu-id="bd762-110">**Type**: String.</span><span class="sxs-lookup"><span data-stu-id="bd762-110">**Type**: String.</span></span> 

<span data-ttu-id="bd762-111">**Description**: Set the level to one of the following values:</span><span class="sxs-lookup"><span data-stu-id="bd762-111">**Description**: Set the level to one of the following values:</span></span>
- <span data-ttu-id="bd762-112">không</span><span class="sxs-lookup"><span data-stu-id="bd762-112">none</span></span>
- <span data-ttu-id="bd762-113">required</span><span class="sxs-lookup"><span data-stu-id="bd762-113">required</span></span>
- <span data-ttu-id="bd762-114">recommended</span><span class="sxs-lookup"><span data-stu-id="bd762-114">recommended</span></span>

### <a name="related-topic"></a><span data-ttu-id="bd762-115">Related topic</span><span class="sxs-lookup"><span data-stu-id="bd762-115">Related topic</span></span>
[<span data-ttu-id="bd762-116">getRequiredLevel (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="bd762-116">getRequiredLevel (Client API reference)</span></span>](getRequiredLevel.md)


