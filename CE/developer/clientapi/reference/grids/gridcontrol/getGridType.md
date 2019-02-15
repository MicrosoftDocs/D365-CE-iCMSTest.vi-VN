---
title: getGridType (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: a441c08c-df32-433e-b666-4253f2cf878c
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4fd2e200b5b48456e3c89b058b480ec91710c479
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386773"
---
# <a name="getgridtype-client-api-reference"></a><span data-ttu-id="9a3d8-102">getGridType (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="9a3d8-102">getGridType (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getGridType-description.md](./includes/getGridType-description.md)]

## <a name="grid-types-supported"></a><span data-ttu-id="9a3d8-103">Grid types supported</span><span class="sxs-lookup"><span data-stu-id="9a3d8-103">Grid types supported</span></span>

<span data-ttu-id="9a3d8-104">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="9a3d8-104">Read-only and editable grids</span></span>

## <a name="syntax"></a><span data-ttu-id="9a3d8-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="9a3d8-105">Syntax</span></span>

`var gridType = gridContext.getGridType();`

## <a name="return-value"></a><span data-ttu-id="9a3d8-106">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="9a3d8-106">Return Value</span></span>

<span data-ttu-id="9a3d8-107">**Type**: Number</span><span class="sxs-lookup"><span data-stu-id="9a3d8-107">**Type**: Number</span></span>

<span data-ttu-id="9a3d8-108">**Description**: Returns one of the following values:</span><span class="sxs-lookup"><span data-stu-id="9a3d8-108">**Description**: Returns one of the following values:</span></span>

|<span data-ttu-id="9a3d8-109">Value</span><span class="sxs-lookup"><span data-stu-id="9a3d8-109">Value</span></span> |<span data-ttu-id="9a3d8-110">Mô tả</span><span class="sxs-lookup"><span data-stu-id="9a3d8-110">Description</span></span> |
|--|--|
|<span data-ttu-id="9a3d8-111">1</span><span class="sxs-lookup"><span data-stu-id="9a3d8-111">1</span></span>|<span data-ttu-id="9a3d8-112">HomePageGrid</span><span class="sxs-lookup"><span data-stu-id="9a3d8-112">HomePageGrid</span></span>|
|<span data-ttu-id="9a3d8-113">2</span><span class="sxs-lookup"><span data-stu-id="9a3d8-113">2</span></span>|<span data-ttu-id="9a3d8-114">Subgrid</span><span class="sxs-lookup"><span data-stu-id="9a3d8-114">Subgrid</span></span>|

## <a name="remarks"></a><span data-ttu-id="9a3d8-115">Chú thích</span><span class="sxs-lookup"><span data-stu-id="9a3d8-115">Remarks</span></span>

<span data-ttu-id="9a3d8-116">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span><span class="sxs-lookup"><span data-stu-id="9a3d8-116">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span></span> 


