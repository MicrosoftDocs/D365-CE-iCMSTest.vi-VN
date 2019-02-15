---
title: getSubmitMode (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: a3231438-3821-4dce-b118-d63e6ce85e01
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 05805855194ce259d855c06cf05a695ea5ad818e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388768"
---
# <a name="getsubmitmode-client-api-reference"></a><span data-ttu-id="9d6a0-102">getSubmitMode (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="9d6a0-102">getSubmitMode (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="9d6a0-103">Returns a string indicating when data from the attribute will be submitted when the record is saved.</span><span class="sxs-lookup"><span data-stu-id="9d6a0-103">Returns a string indicating when data from the attribute will be submitted when the record is saved.</span></span> 

## <a name="attribute-types-supported"></a><span data-ttu-id="9d6a0-104">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="9d6a0-104">Attribute types supported</span></span>

<span data-ttu-id="9d6a0-105">Tất cả</span><span class="sxs-lookup"><span data-stu-id="9d6a0-105">All</span></span>

## <a name="syntax"></a><span data-ttu-id="9d6a0-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="9d6a0-106">Syntax</span></span>

`formContext.getAttribute(arg).getSubmitMode()`

## <a name="return-value"></a><span data-ttu-id="9d6a0-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="9d6a0-107">Return Value</span></span>

<span data-ttu-id="9d6a0-108">**Type**: String.</span><span class="sxs-lookup"><span data-stu-id="9d6a0-108">**Type**: String.</span></span> 

<span data-ttu-id="9d6a0-109">**Description**: Returns one of the following values:</span><span class="sxs-lookup"><span data-stu-id="9d6a0-109">**Description**: Returns one of the following values:</span></span>
- <span data-ttu-id="9d6a0-110">always</span><span class="sxs-lookup"><span data-stu-id="9d6a0-110">always</span></span>
- <span data-ttu-id="9d6a0-111">never</span><span class="sxs-lookup"><span data-stu-id="9d6a0-111">never</span></span>
- <span data-ttu-id="9d6a0-112">dirty</span><span class="sxs-lookup"><span data-stu-id="9d6a0-112">dirty</span></span>

### <a name="related-topic"></a><span data-ttu-id="9d6a0-113">Related topic</span><span class="sxs-lookup"><span data-stu-id="9d6a0-113">Related topic</span></span>
[<span data-ttu-id="9d6a0-114">setSubmitMode (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="9d6a0-114">setSubmitMode (Client API reference)</span></span>](setSubmitMode.md)

