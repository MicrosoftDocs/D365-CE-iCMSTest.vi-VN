---
title: getUrl (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: f2023d7d-5877-4436-abe6-e81ca68b8ec0
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 952e8bb90d2e81988657e980217d6f97a8a2e903
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386370"
---
# <a name="geturl-client-api-reference"></a><span data-ttu-id="51eaa-102">getUrl (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="51eaa-102">getUrl (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getUrl-description.md](./includes/getUrl-description.md)]

## <a name="grid-types-supported"></a><span data-ttu-id="51eaa-103">Grid types supported</span><span class="sxs-lookup"><span data-stu-id="51eaa-103">Grid types supported</span></span>

<span data-ttu-id="51eaa-104">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="51eaa-104">Read-only and editable grids</span></span>

## <a name="syntax"></a><span data-ttu-id="51eaa-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="51eaa-105">Syntax</span></span>

`gridContext.getUrl(client);`

## <a name="parameter"></a><span data-ttu-id="51eaa-106">Tham số</span><span class="sxs-lookup"><span data-stu-id="51eaa-106">Parameter</span></span>

|<span data-ttu-id="51eaa-107">Tên</span><span class="sxs-lookup"><span data-stu-id="51eaa-107">Name</span></span>|<span data-ttu-id="51eaa-108">Loại</span><span class="sxs-lookup"><span data-stu-id="51eaa-108">Type</span></span>|<span data-ttu-id="51eaa-109">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="51eaa-109">Required</span></span>|<span data-ttu-id="51eaa-110">Mô tả</span><span class="sxs-lookup"><span data-stu-id="51eaa-110">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="51eaa-111">client</span><span class="sxs-lookup"><span data-stu-id="51eaa-111">client</span></span>|<span data-ttu-id="51eaa-112">Số</span><span class="sxs-lookup"><span data-stu-id="51eaa-112">Number</span></span>|<span data-ttu-id="51eaa-113">Không</span><span class="sxs-lookup"><span data-stu-id="51eaa-113">No</span></span>|<span data-ttu-id="51eaa-114">Indicates the client type.</span><span class="sxs-lookup"><span data-stu-id="51eaa-114">Indicates the client type.</span></span> <span data-ttu-id="51eaa-115">Bạn có thể chỉ định một trong các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="51eaa-115">You can specify one of the following values:</span></span><br/><span data-ttu-id="51eaa-116">0: Browser</span><span class="sxs-lookup"><span data-stu-id="51eaa-116">0: Browser</span></span><br/><span data-ttu-id="51eaa-117">1: MobileApplication</span><span class="sxs-lookup"><span data-stu-id="51eaa-117">1: MobileApplication</span></span>|

## <a name="return-value"></a><span data-ttu-id="51eaa-118">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="51eaa-118">Return Value</span></span>

<span data-ttu-id="51eaa-119">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="51eaa-119">**Type**: String</span></span>

<span data-ttu-id="51eaa-120">**Description**: The Url of the current grid control.</span><span class="sxs-lookup"><span data-stu-id="51eaa-120">**Description**: The Url of the current grid control.</span></span>

## <a name="remarks"></a><span data-ttu-id="51eaa-121">Chú thích</span><span class="sxs-lookup"><span data-stu-id="51eaa-121">Remarks</span></span>

<span data-ttu-id="51eaa-122">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span><span class="sxs-lookup"><span data-stu-id="51eaa-122">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span></span>



