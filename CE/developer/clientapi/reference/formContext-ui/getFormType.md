---
title: getFormType (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 6c57db71-a76d-404c-852e-9c36a1c549ee
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 549107d174a59d394c43727c6e26e0e9024a4fad
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387331"
---
# <a name="getformtype-client-api-reference"></a><span data-ttu-id="d4829-102">getFormType (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="d4829-102">getFormType (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getFormType-description.md](./includes/getFormType-description.md)]

## <a name="syntax"></a><span data-ttu-id="d4829-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="d4829-103">Syntax</span></span>

`formContext.ui.getFormType();`

## <a name="return-value"></a><span data-ttu-id="d4829-104">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="d4829-104">Return Value</span></span>

<span data-ttu-id="d4829-105">**Type**: Number</span><span class="sxs-lookup"><span data-stu-id="d4829-105">**Type**: Number</span></span>

<span data-ttu-id="d4829-106">**Description**: Form type.</span><span class="sxs-lookup"><span data-stu-id="d4829-106">**Description**: Form type.</span></span> <span data-ttu-id="d4829-107">Returns one of the following values</span><span class="sxs-lookup"><span data-stu-id="d4829-107">Returns one of the following values</span></span> 

|<span data-ttu-id="d4829-108">Value</span><span class="sxs-lookup"><span data-stu-id="d4829-108">Value</span></span> |<span data-ttu-id="d4829-109">Loại biểu mẫu</span><span class="sxs-lookup"><span data-stu-id="d4829-109">Form type</span></span> |
|---|---|
|<span data-ttu-id="d4829-110">0</span><span class="sxs-lookup"><span data-stu-id="d4829-110">0</span></span>|<span data-ttu-id="d4829-111">Undefined</span><span class="sxs-lookup"><span data-stu-id="d4829-111">Undefined</span></span>|
|<span data-ttu-id="d4829-112">1</span><span class="sxs-lookup"><span data-stu-id="d4829-112">1</span></span>|<span data-ttu-id="d4829-113">Tạo</span><span class="sxs-lookup"><span data-stu-id="d4829-113">Create</span></span>|
|<span data-ttu-id="d4829-114">2</span><span class="sxs-lookup"><span data-stu-id="d4829-114">2</span></span>|<span data-ttu-id="d4829-115">Update</span><span class="sxs-lookup"><span data-stu-id="d4829-115">Update</span></span>|
|<span data-ttu-id="d4829-116">3</span><span class="sxs-lookup"><span data-stu-id="d4829-116">3</span></span>|<span data-ttu-id="d4829-117">Read Only</span><span class="sxs-lookup"><span data-stu-id="d4829-117">Read Only</span></span>|
|<span data-ttu-id="d4829-118">4</span><span class="sxs-lookup"><span data-stu-id="d4829-118">4</span></span>|<span data-ttu-id="d4829-119">Đã vô hiệu hóa</span><span class="sxs-lookup"><span data-stu-id="d4829-119">Disabled</span></span>|
|<span data-ttu-id="d4829-120">6</span><span class="sxs-lookup"><span data-stu-id="d4829-120">6</span></span>|<span data-ttu-id="d4829-121">Bulk Edit</span><span class="sxs-lookup"><span data-stu-id="d4829-121">Bulk Edit</span></span>|

>[!NOTE]
><span data-ttu-id="d4829-122">Quick Create forms return 1.</span><span class="sxs-lookup"><span data-stu-id="d4829-122">Quick Create forms return 1.</span></span>


### <a name="related-topics"></a><span data-ttu-id="d4829-123">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="d4829-123">Related topics</span></span>

[<span data-ttu-id="d4829-124">formContext.ui</span><span class="sxs-lookup"><span data-stu-id="d4829-124">formContext.ui</span></span>](../formContext-ui.md)

[<span data-ttu-id="d4829-125">formContext</span><span class="sxs-lookup"><span data-stu-id="d4829-125">formContext</span></span>](../../clientapi-form-context.md)

