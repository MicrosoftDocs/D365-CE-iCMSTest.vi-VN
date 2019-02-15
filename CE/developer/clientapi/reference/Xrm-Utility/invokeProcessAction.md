---
title: invokeProcessAction (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: e71012ba-249d-4ae7-8891-f7d3ae16a20a
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5091cc9650de3ea4a9ae739dc6fa2adff88877cd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387439"
---
# <a name="invokeprocessaction-client-api-reference"></a><span data-ttu-id="fd2c1-102">invokeProcessAction (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="fd2c1-102">invokeProcessAction (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/invokeProcessAction-description.md](./includes/invokeProcessAction-description.md)] 

<span data-ttu-id="fd2c1-103">For more information about actions, see [Actions overview](../../../../customize/actions.md)</span><span class="sxs-lookup"><span data-stu-id="fd2c1-103">For more information about actions, see [Actions overview](../../../../customize/actions.md)</span></span>

## <a name="syntax"></a><span data-ttu-id="fd2c1-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="fd2c1-104">Syntax</span></span>

`Xrm.Utility.invokeProcessAction(name,parameters).then(successCallback, errorCallback)`

## <a name="parameters"></a><span data-ttu-id="fd2c1-105">Tham số</span><span class="sxs-lookup"><span data-stu-id="fd2c1-105">Parameters</span></span>

|<span data-ttu-id="fd2c1-106">Tên</span><span class="sxs-lookup"><span data-stu-id="fd2c1-106">Name</span></span> |<span data-ttu-id="fd2c1-107">Loại</span><span class="sxs-lookup"><span data-stu-id="fd2c1-107">Type</span></span> |<span data-ttu-id="fd2c1-108">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="fd2c1-108">Required</span></span> |<span data-ttu-id="fd2c1-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="fd2c1-109">Description</span></span> |
|---|---|---|---|
|<span data-ttu-id="fd2c1-110">tên</span><span class="sxs-lookup"><span data-stu-id="fd2c1-110">name</span></span>|<span data-ttu-id="fd2c1-111">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="fd2c1-111">String</span></span>|<span data-ttu-id="fd2c1-112">Có</span><span class="sxs-lookup"><span data-stu-id="fd2c1-112">Yes</span></span>|<span data-ttu-id="fd2c1-113">Name of the process action to invoke.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-113">Name of the process action to invoke.</span></span>|
|<span data-ttu-id="fd2c1-114">parameters</span><span class="sxs-lookup"><span data-stu-id="fd2c1-114">parameters</span></span>|<span data-ttu-id="fd2c1-115">đối tượng</span><span class="sxs-lookup"><span data-stu-id="fd2c1-115">object</span></span>|<span data-ttu-id="fd2c1-116">Không</span><span class="sxs-lookup"><span data-stu-id="fd2c1-116">No</span></span>|<span data-ttu-id="fd2c1-117">An object containing input parameters for the action.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-117">An object containing input parameters for the action.</span></span> <span data-ttu-id="fd2c1-118">You define an object using `key:value` pairs of items, where `key` is of **String** type.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-118">You define an object using `key:value` pairs of items, where `key` is of **String** type.</span></span>|
|<span data-ttu-id="fd2c1-119">successCallback</span><span class="sxs-lookup"><span data-stu-id="fd2c1-119">successCallback</span></span> |<span data-ttu-id="fd2c1-120">Hàm</span><span class="sxs-lookup"><span data-stu-id="fd2c1-120">Function</span></span> |<span data-ttu-id="fd2c1-121">Có</span><span class="sxs-lookup"><span data-stu-id="fd2c1-121">Yes</span></span> |<span data-ttu-id="fd2c1-122">A function to call when the action is invoked.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-122">A function to call when the action is invoked.</span></span>  |
|<span data-ttu-id="fd2c1-123">errorCallback</span><span class="sxs-lookup"><span data-stu-id="fd2c1-123">errorCallback</span></span> |<span data-ttu-id="fd2c1-124">Hàm</span><span class="sxs-lookup"><span data-stu-id="fd2c1-124">Function</span></span> |<span data-ttu-id="fd2c1-125">Có</span><span class="sxs-lookup"><span data-stu-id="fd2c1-125">Yes</span></span> |<span data-ttu-id="fd2c1-126">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-126">A function to call when the operation fails.</span></span>  |

## <a name="returns"></a><span data-ttu-id="fd2c1-127">Returns</span><span class="sxs-lookup"><span data-stu-id="fd2c1-127">Returns</span></span>

<span data-ttu-id="fd2c1-128">On success, returns Web API result along with any action output.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-128">On success, returns Web API result along with any action output.</span></span>

### <a name="related-topics"></a><span data-ttu-id="fd2c1-129">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="fd2c1-129">Related topics</span></span>

[<span data-ttu-id="fd2c1-130">Tổng quan về các tác vụ</span><span class="sxs-lookup"><span data-stu-id="fd2c1-130">Actions overview</span></span>](../../../../customize/actions.md)

[<span data-ttu-id="fd2c1-131">Xrm.Utility</span><span class="sxs-lookup"><span data-stu-id="fd2c1-131">Xrm.Utility</span></span>](../xrm-utility.md)


