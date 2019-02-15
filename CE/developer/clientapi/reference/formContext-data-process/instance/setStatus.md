---
title: setStatus (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 649fe7b0-016d-409f-ba3c-b14e0f1953e0
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7f87ebcfb061391b879a0ba238ab60931b06a4d9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385652"
---
# <a name="setstatus-client-api-reference"></a><span data-ttu-id="2f97a-102">setStatus (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="2f97a-102">setStatus (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setStatus-description.md](./includes/setStatus-description.md)]

## <a name="syntax"></a><span data-ttu-id="2f97a-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="2f97a-103">Syntax</span></span>

`formContext.data.process.setStatus(status, callbackFunction);`

## <a name="parameters"></a><span data-ttu-id="2f97a-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="2f97a-104">Parameters</span></span>

|<span data-ttu-id="2f97a-105">Tên</span><span class="sxs-lookup"><span data-stu-id="2f97a-105">Name</span></span>|<span data-ttu-id="2f97a-106">Loại</span><span class="sxs-lookup"><span data-stu-id="2f97a-106">Type</span></span>|<span data-ttu-id="2f97a-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="2f97a-107">Required</span></span>|<span data-ttu-id="2f97a-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="2f97a-108">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="2f97a-109">status</span><span class="sxs-lookup"><span data-stu-id="2f97a-109">status</span></span>|<span data-ttu-id="2f97a-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="2f97a-110">String</span></span>|<span data-ttu-id="2f97a-111">Có</span><span class="sxs-lookup"><span data-stu-id="2f97a-111">Yes</span></span>|<span data-ttu-id="2f97a-112">The new status.</span><span class="sxs-lookup"><span data-stu-id="2f97a-112">The new status.</span></span> <span data-ttu-id="2f97a-113">The values can be **active**, **aborted**, or **finished**.</span><span class="sxs-lookup"><span data-stu-id="2f97a-113">The values can be **active**, **aborted**, or **finished**.</span></span>|
|<span data-ttu-id="2f97a-114">callbackFunction</span><span class="sxs-lookup"><span data-stu-id="2f97a-114">callbackFunction</span></span>|<span data-ttu-id="2f97a-115">Hàm</span><span class="sxs-lookup"><span data-stu-id="2f97a-115">Function</span></span>|<span data-ttu-id="2f97a-116">Không</span><span class="sxs-lookup"><span data-stu-id="2f97a-116">No</span></span>|<span data-ttu-id="2f97a-117">A function to call when the operation is complete.</span><span class="sxs-lookup"><span data-stu-id="2f97a-117">A function to call when the operation is complete.</span></span> <span data-ttu-id="2f97a-118">This callback function is passed the new status as a string value.</span><span class="sxs-lookup"><span data-stu-id="2f97a-118">This callback function is passed the new status as a string value.</span></span>|

<span data-ttu-id="2f97a-119">**Type**: String.</span><span class="sxs-lookup"><span data-stu-id="2f97a-119">**Type**: String.</span></span> 

<span data-ttu-id="2f97a-120">**Description**:Returns one of the following values: **active**, **aborted**, or **finished**.</span><span class="sxs-lookup"><span data-stu-id="2f97a-120">**Description**:Returns one of the following values: **active**, **aborted**, or **finished**.</span></span>

### <a name="related-topics"></a><span data-ttu-id="2f97a-121">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="2f97a-121">Related topics</span></span>

[<span data-ttu-id="2f97a-122">formContext.data.process</span><span class="sxs-lookup"><span data-stu-id="2f97a-122">formContext.data.process</span></span>](../../formContext-data-process.md)
 


