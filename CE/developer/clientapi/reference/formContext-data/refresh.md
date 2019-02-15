---
title: refresh (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 03e970ee-7ed3-4df2-9670-222d76a479fd
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3ea5a6aaf3f4f317d2a345e99538ce14b8e6b99c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385484"
---
# <a name="refresh-client-api-reference"></a><span data-ttu-id="eb952-102">refresh (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="eb952-102">refresh (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/refresh-description.md](./includes/refresh-description.md)]

## <a name="syntax"></a><span data-ttu-id="eb952-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="eb952-103">Syntax</span></span>

`formContext.data.refresh(save).then(successCallback, errorCallback);`

## <a name="parameter"></a><span data-ttu-id="eb952-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="eb952-104">Parameter</span></span>

|<span data-ttu-id="eb952-105">Tên</span><span class="sxs-lookup"><span data-stu-id="eb952-105">Name</span></span>|<span data-ttu-id="eb952-106">Loại</span><span class="sxs-lookup"><span data-stu-id="eb952-106">Type</span></span>|<span data-ttu-id="eb952-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="eb952-107">Required</span></span>|<span data-ttu-id="eb952-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="eb952-108">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="eb952-109">save</span><span class="sxs-lookup"><span data-stu-id="eb952-109">save</span></span>|<span data-ttu-id="eb952-110">Boolean</span><span class="sxs-lookup"><span data-stu-id="eb952-110">Boolean</span></span>|<span data-ttu-id="eb952-111">Không</span><span class="sxs-lookup"><span data-stu-id="eb952-111">No</span></span>|<span data-ttu-id="eb952-112">true if the data should be saved after it is refreshed, otherwise false.</span><span class="sxs-lookup"><span data-stu-id="eb952-112">true if the data should be saved after it is refreshed, otherwise false.</span></span>|
|<span data-ttu-id="eb952-113">successCallback</span><span class="sxs-lookup"><span data-stu-id="eb952-113">successCallback</span></span>|<span data-ttu-id="eb952-114">Hàm</span><span class="sxs-lookup"><span data-stu-id="eb952-114">Function</span></span>|<span data-ttu-id="eb952-115">Không</span><span class="sxs-lookup"><span data-stu-id="eb952-115">No</span></span>|<span data-ttu-id="eb952-116">A function to call when the operation succeeds.</span><span class="sxs-lookup"><span data-stu-id="eb952-116">A function to call when the operation succeeds.</span></span>|
|<span data-ttu-id="eb952-117">errorCallback</span><span class="sxs-lookup"><span data-stu-id="eb952-117">errorCallback</span></span>|<span data-ttu-id="eb952-118">Hàm</span><span class="sxs-lookup"><span data-stu-id="eb952-118">Function</span></span>|<span data-ttu-id="eb952-119">Không</span><span class="sxs-lookup"><span data-stu-id="eb952-119">No</span></span>|<span data-ttu-id="eb952-120">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="eb952-120">A function to call when the operation fails.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="eb952-121">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="eb952-121">Related topics</span></span>

[<span data-ttu-id="eb952-122">formContext</span><span class="sxs-lookup"><span data-stu-id="eb952-122">formContext</span></span>](../../clientapi-form-context.md)

