---
title: getSelectedRows (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 49f39f0f-33ef-41d1-9ab3-14966ae075b5
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4df882571226b3b09aa53bcfb6bf505661e969b7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388147"
---
# <a name="getselectedrows-client-api-reference"></a><span data-ttu-id="27f40-102">getSelectedRows (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="27f40-102">getSelectedRows (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getSelectedRows-description.md](./includes/getSelectedRows-description.md)]

## <a name="grid-types-supported"></a><span data-ttu-id="27f40-103">Grid types supported</span><span class="sxs-lookup"><span data-stu-id="27f40-103">Grid types supported</span></span>

<span data-ttu-id="27f40-104">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="27f40-104">Read-only and editable grids</span></span>

## <a name="syntax"></a><span data-ttu-id="27f40-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="27f40-105">Syntax</span></span>

`var allSelectedRows = gridContext.getGrid().getSelectedRows();`

## <a name="return-value"></a><span data-ttu-id="27f40-106">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="27f40-106">Return Value</span></span>

<span data-ttu-id="27f40-107">**Type**: Collection</span><span class="sxs-lookup"><span data-stu-id="27f40-107">**Type**: Collection</span></span>

<span data-ttu-id="27f40-108">**Description**: A collection of selected rows in the grid.</span><span class="sxs-lookup"><span data-stu-id="27f40-108">**Description**: A collection of selected rows in the grid.</span></span>

## <a name="remarks"></a><span data-ttu-id="27f40-109">Chú thích</span><span class="sxs-lookup"><span data-stu-id="27f40-109">Remarks</span></span>

<span data-ttu-id="27f40-110">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span><span class="sxs-lookup"><span data-stu-id="27f40-110">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span></span>

<span data-ttu-id="27f40-111">See [Collections (Client API reference)](../../collections.md) for information on the methods available to access data in a collection.</span><span class="sxs-lookup"><span data-stu-id="27f40-111">See [Collections (Client API reference)](../../collections.md) for information on the methods available to access data in a collection.</span></span>

