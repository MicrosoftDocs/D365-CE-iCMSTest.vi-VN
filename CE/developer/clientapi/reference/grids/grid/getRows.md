---
title: getRows (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
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
ms.openlocfilehash: 7536f18d002c18d3466f801807db5024f1636413
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388605"
---
# <a name="getrows-client-api-reference"></a><span data-ttu-id="a8fa7-102">getRows (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="a8fa7-102">getRows (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getRows-description.md](./includes/getRows-description.md)]

## <a name="grid-types-supported"></a><span data-ttu-id="a8fa7-103">Grid types supported</span><span class="sxs-lookup"><span data-stu-id="a8fa7-103">Grid types supported</span></span>

<span data-ttu-id="a8fa7-104">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="a8fa7-104">Read-only and editable grids</span></span>

## <a name="syntax"></a><span data-ttu-id="a8fa7-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="a8fa7-105">Syntax</span></span>

`var allRows = gridContext.getGrid().getRows();`

## <a name="return-value"></a><span data-ttu-id="a8fa7-106">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="a8fa7-106">Return Value</span></span>

<span data-ttu-id="a8fa7-107">**Type**: Collection</span><span class="sxs-lookup"><span data-stu-id="a8fa7-107">**Type**: Collection</span></span>

<span data-ttu-id="a8fa7-108">**Description**: A collection of rows in the grid.</span><span class="sxs-lookup"><span data-stu-id="a8fa7-108">**Description**: A collection of rows in the grid.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8fa7-109">Chú thích</span><span class="sxs-lookup"><span data-stu-id="a8fa7-109">Remarks</span></span>

<span data-ttu-id="a8fa7-110">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span><span class="sxs-lookup"><span data-stu-id="a8fa7-110">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span></span>

<span data-ttu-id="a8fa7-111">See [Collections (Client API reference)](../../collections.md) for information on the methods available to access data in a collection.</span><span class="sxs-lookup"><span data-stu-id="a8fa7-111">See [Collections (Client API reference)](../../collections.md) for information on the methods available to access data in a collection.</span></span>

