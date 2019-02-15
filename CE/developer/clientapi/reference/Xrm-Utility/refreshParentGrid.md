---
title: refreshParentGrid (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 89123cde-7c66-4c7d-94e4-e287285019f8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 57d2bdf660937baa83d3bbc6a59ba2ddcef10732
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386430"
---
# <a name="refreshparentgrid-client-api-reference"></a><span data-ttu-id="c3e98-102">refreshParentGrid (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="c3e98-102">refreshParentGrid (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/refreshParentGrid-description.md](./includes/refreshParentGrid-description.md)] 

## <a name="syntax"></a><span data-ttu-id="c3e98-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="c3e98-103">Syntax</span></span>

`Xrm.Utility.refreshParentGrid(lookupOptions)`

## <a name="parameters"></a><span data-ttu-id="c3e98-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="c3e98-104">Parameters</span></span>

<span data-ttu-id="c3e98-105">**lookupOptions**: An object with the following properties to specify the record:</span><span class="sxs-lookup"><span data-stu-id="c3e98-105">**lookupOptions**: An object with the following properties to specify the record:</span></span>

|<span data-ttu-id="c3e98-106">Property Name</span><span class="sxs-lookup"><span data-stu-id="c3e98-106">Property Name</span></span> |<span data-ttu-id="c3e98-107">Loại</span><span class="sxs-lookup"><span data-stu-id="c3e98-107">Type</span></span> |<span data-ttu-id="c3e98-108">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="c3e98-108">Required</span></span>  |<span data-ttu-id="c3e98-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="c3e98-109">Description</span></span> |
|---|---|---|---|
|<span data-ttu-id="c3e98-110">entityType</span><span class="sxs-lookup"><span data-stu-id="c3e98-110">entityType</span></span>|<span data-ttu-id="c3e98-111">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="c3e98-111">String</span></span>|<span data-ttu-id="c3e98-112">Có</span><span class="sxs-lookup"><span data-stu-id="c3e98-112">Yes</span></span> |<span data-ttu-id="c3e98-113">Entity type of the record.</span><span class="sxs-lookup"><span data-stu-id="c3e98-113">Entity type of the record.</span></span>|
|<span data-ttu-id="c3e98-114">ID</span><span class="sxs-lookup"><span data-stu-id="c3e98-114">id</span></span>|<span data-ttu-id="c3e98-115">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="c3e98-115">String</span></span>|<span data-ttu-id="c3e98-116">Có</span><span class="sxs-lookup"><span data-stu-id="c3e98-116">Yes</span></span> |<span data-ttu-id="c3e98-117">ID of the record.</span><span class="sxs-lookup"><span data-stu-id="c3e98-117">ID of the record.</span></span>|
|<span data-ttu-id="c3e98-118">tên</span><span class="sxs-lookup"><span data-stu-id="c3e98-118">name</span></span>|<span data-ttu-id="c3e98-119">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="c3e98-119">String</span></span>|<span data-ttu-id="c3e98-120">Không</span><span class="sxs-lookup"><span data-stu-id="c3e98-120">No</span></span> |<span data-ttu-id="c3e98-121">Name of the record.</span><span class="sxs-lookup"><span data-stu-id="c3e98-121">Name of the record.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="c3e98-122">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="c3e98-122">Related topics</span></span>

[<span data-ttu-id="c3e98-123">Xrm.Utility</span><span class="sxs-lookup"><span data-stu-id="c3e98-123">Xrm.Utility</span></span>](../xrm-utility.md)



