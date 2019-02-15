---
title: setShowTime (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 77999c82-3d6a-4db9-af9c-7322491768d9
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: de36617554983334018cf87a0ad054508221085e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386342"
---
# <a name="setshowtime-client-api-reference"></a><span data-ttu-id="5132e-102">setShowTime (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="5132e-102">setShowTime (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5132e-103">Specify whether a date control should show the time portion of the date.</span><span class="sxs-lookup"><span data-stu-id="5132e-103">Specify whether a date control should show the time portion of the date.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="5132e-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="5132e-104">Control types supported</span></span>

<span data-ttu-id="5132e-105">standard control for **datetime** attributes.</span><span class="sxs-lookup"><span data-stu-id="5132e-105">standard control for **datetime** attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5132e-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="5132e-106">Syntax</span></span>

`formContext.getControl(arg).setShowTime(bool);`

## <a name="parameter"></a><span data-ttu-id="5132e-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="5132e-107">Parameter</span></span>

|<span data-ttu-id="5132e-108">Tên</span><span class="sxs-lookup"><span data-stu-id="5132e-108">Name</span></span>|<span data-ttu-id="5132e-109">Loại</span><span class="sxs-lookup"><span data-stu-id="5132e-109">Type</span></span>|<span data-ttu-id="5132e-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="5132e-110">Required</span></span>|<span data-ttu-id="5132e-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5132e-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="5132e-112">bool</span><span class="sxs-lookup"><span data-stu-id="5132e-112">bool</span></span>|<span data-ttu-id="5132e-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="5132e-113">Boolean</span></span>|<span data-ttu-id="5132e-114">Có</span><span class="sxs-lookup"><span data-stu-id="5132e-114">Yes</span></span>|<span data-ttu-id="5132e-115">Specify true to show the time portion of the date; false otherwise.</span><span class="sxs-lookup"><span data-stu-id="5132e-115">Specify true to show the time portion of the date; false otherwise.</span></span>|

## <a name="remarks"></a><span data-ttu-id="5132e-116">Chú thích</span><span class="sxs-lookup"><span data-stu-id="5132e-116">Remarks</span></span>

<span data-ttu-id="5132e-117">This method will show or hide the time component of a date control where the attribute uses the **DateAndTime** format.</span><span class="sxs-lookup"><span data-stu-id="5132e-117">This method will show or hide the time component of a date control where the attribute uses the **DateAndTime** format.</span></span> <span data-ttu-id="5132e-118">This method will have no effect when the **DateOnly** format is used.</span><span class="sxs-lookup"><span data-stu-id="5132e-118">This method will have no effect when the **DateOnly** format is used.</span></span>

### <a name="related-topics"></a><span data-ttu-id="5132e-119">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="5132e-119">Related topics</span></span>

[<span data-ttu-id="5132e-120">getShowTime</span><span class="sxs-lookup"><span data-stu-id="5132e-120">getShowTime</span></span>](getShowTime.md)

