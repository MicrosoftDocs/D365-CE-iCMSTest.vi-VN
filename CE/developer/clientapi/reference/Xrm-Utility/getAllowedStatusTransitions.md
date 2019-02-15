---
title: getAllowedStatusTransitions (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 28c36741-0070-435c-a42f-49f4dda2ef7f
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 27d5582aecc1566ef588f0af0cb8a1b61b601b0d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387586"
---
# <a name="getallowedstatustransitions-client-api-reference"></a><span data-ttu-id="484b2-102">getAllowedStatusTransitions (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="484b2-102">getAllowedStatusTransitions (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getAllowedStatusTransitions-description.md](./includes/getAllowedStatusTransitions-description.md)] 

## <a name="syntax"></a><span data-ttu-id="484b2-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="484b2-103">Syntax</span></span>

`Xrm.Utility.getAllowedStatusTransitions(entityName,stateCode).then(successCallback, errorCallback)`

## <a name="parameters"></a><span data-ttu-id="484b2-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="484b2-104">Parameters</span></span>

|<span data-ttu-id="484b2-105">Tên</span><span class="sxs-lookup"><span data-stu-id="484b2-105">Name</span></span> |<span data-ttu-id="484b2-106">Loại</span><span class="sxs-lookup"><span data-stu-id="484b2-106">Type</span></span> |<span data-ttu-id="484b2-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="484b2-107">Required</span></span> |<span data-ttu-id="484b2-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="484b2-108">Description</span></span> |
|---|---|---|---|
|<span data-ttu-id="484b2-109">entityName</span><span class="sxs-lookup"><span data-stu-id="484b2-109">entityName</span></span>|<span data-ttu-id="484b2-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="484b2-110">String</span></span>|<span data-ttu-id="484b2-111">Có</span><span class="sxs-lookup"><span data-stu-id="484b2-111">Yes</span></span>|<span data-ttu-id="484b2-112">The logical name of the entity.</span><span class="sxs-lookup"><span data-stu-id="484b2-112">The logical name of the entity.</span></span>|
|<span data-ttu-id="484b2-113">stateCode</span><span class="sxs-lookup"><span data-stu-id="484b2-113">stateCode</span></span>|<span data-ttu-id="484b2-114">Số</span><span class="sxs-lookup"><span data-stu-id="484b2-114">Number</span></span>|<span data-ttu-id="484b2-115">Có</span><span class="sxs-lookup"><span data-stu-id="484b2-115">Yes</span></span>|<span data-ttu-id="484b2-116">The state code to find out the allowed status transition values.</span><span class="sxs-lookup"><span data-stu-id="484b2-116">The state code to find out the allowed status transition values.</span></span>|
|<span data-ttu-id="484b2-117">successCallback</span><span class="sxs-lookup"><span data-stu-id="484b2-117">successCallback</span></span>|<span data-ttu-id="484b2-118">Hàm</span><span class="sxs-lookup"><span data-stu-id="484b2-118">Function</span></span>|<span data-ttu-id="484b2-119">Không</span><span class="sxs-lookup"><span data-stu-id="484b2-119">No</span></span>|<span data-ttu-id="484b2-120">The function to execute when the operation succeeds.</span><span class="sxs-lookup"><span data-stu-id="484b2-120">The function to execute when the operation succeeds.</span></span>|
|<span data-ttu-id="484b2-121">errorCallback</span><span class="sxs-lookup"><span data-stu-id="484b2-121">errorCallback</span></span>|<span data-ttu-id="484b2-122">Hàm</span><span class="sxs-lookup"><span data-stu-id="484b2-122">Function</span></span>|<span data-ttu-id="484b2-123">Không</span><span class="sxs-lookup"><span data-stu-id="484b2-123">No</span></span>|<span data-ttu-id="484b2-124">The function to execute when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="484b2-124">The function to execute when the operation fails.</span></span>|


### <a name="related-topics"></a><span data-ttu-id="484b2-125">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="484b2-125">Related topics</span></span>

[<span data-ttu-id="484b2-126">Xrm.Utility</span><span class="sxs-lookup"><span data-stu-id="484b2-126">Xrm.Utility</span></span>](../xrm-utility.md)



