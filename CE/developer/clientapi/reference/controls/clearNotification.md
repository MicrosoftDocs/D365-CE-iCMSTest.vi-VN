---
title: clearNotification (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
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
ms.openlocfilehash: c12b39f383689e5f522f2e16e0ccfc95bb6b4961
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388309"
---
# <a name="clearnotification-client-api-reference"></a><span data-ttu-id="46c1e-102">clearNotification (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="46c1e-102">clearNotification (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="46c1e-103">Remove a message already displayed for a control.</span><span class="sxs-lookup"><span data-stu-id="46c1e-103">Remove a message already displayed for a control.</span></span>

## <a name="control-types-supported"></a><span data-ttu-id="46c1e-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="46c1e-104">Control types supported</span></span>

<span data-ttu-id="46c1e-105">Tất cả</span><span class="sxs-lookup"><span data-stu-id="46c1e-105">All</span></span>

## <a name="syntax"></a><span data-ttu-id="46c1e-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="46c1e-106">Syntax</span></span>

`formContext.getControl(arg).clearNotification(uniqueId);`

## <a name="parameters"></a><span data-ttu-id="46c1e-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="46c1e-107">Parameters</span></span>

|<span data-ttu-id="46c1e-108">Tên</span><span class="sxs-lookup"><span data-stu-id="46c1e-108">Name</span></span> | <span data-ttu-id="46c1e-109">Loại</span><span class="sxs-lookup"><span data-stu-id="46c1e-109">Type</span></span> | <span data-ttu-id="46c1e-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="46c1e-110">Required</span></span> | <span data-ttu-id="46c1e-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="46c1e-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="46c1e-112">uniqueId</span><span class="sxs-lookup"><span data-stu-id="46c1e-112">uniqueId</span></span> |<span data-ttu-id="46c1e-113">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="46c1e-113">String</span></span> |<span data-ttu-id="46c1e-114">Không</span><span class="sxs-lookup"><span data-stu-id="46c1e-114">No</span></span>|<span data-ttu-id="46c1e-115">The ID to use to clear a specific message that was set using **setNotification** or **addNotification**.</span><span class="sxs-lookup"><span data-stu-id="46c1e-115">The ID to use to clear a specific message that was set using **setNotification** or **addNotification**.</span></span> <span data-ttu-id="46c1e-116">If the **uniqueId** parameter isn’t specified, the currently displayed notification will be cleared.</span><span class="sxs-lookup"><span data-stu-id="46c1e-116">If the **uniqueId** parameter isn’t specified, the currently displayed notification will be cleared.</span></span>| 


## <a name="return-value"></a><span data-ttu-id="46c1e-117">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="46c1e-117">Return Value</span></span>

<span data-ttu-id="46c1e-118">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="46c1e-118">**Type**: Boolean</span></span> 

<span data-ttu-id="46c1e-119">**Description**: Indicates whether the method succeeded.</span><span class="sxs-lookup"><span data-stu-id="46c1e-119">**Description**: Indicates whether the method succeeded.</span></span> 

### <a name="related-topics"></a><span data-ttu-id="46c1e-120">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="46c1e-120">Related topics</span></span>

[<span data-ttu-id="46c1e-121">addNotification</span><span class="sxs-lookup"><span data-stu-id="46c1e-121">addNotification</span></span>](addNotification.md)

[<span data-ttu-id="46c1e-122">setNotification</span><span class="sxs-lookup"><span data-stu-id="46c1e-122">setNotification</span></span>](setNotification.md)
