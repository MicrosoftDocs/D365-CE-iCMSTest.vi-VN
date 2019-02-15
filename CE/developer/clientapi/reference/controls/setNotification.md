---
title: setNotification (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
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
ms.openlocfilehash: 3ebf8e1351bb3ca55934c884c1bada69d055c4fd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385803"
---
# <a name="setnotification-client-api-reference"></a><span data-ttu-id="7c50c-102">setNotification (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="7c50c-102">setNotification (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="7c50c-103">Displays an error message for the control to indicate that data isn’t valid.</span><span class="sxs-lookup"><span data-stu-id="7c50c-103">Displays an error message for the control to indicate that data isn’t valid.</span></span> <span data-ttu-id="7c50c-104">When this method is used,  a red "X" icon appears next to the control.</span><span class="sxs-lookup"><span data-stu-id="7c50c-104">When this method is used,  a red "X" icon appears next to the control.</span></span> <span data-ttu-id="7c50c-105">On Dynamics 365 for Customer Engagement apps mobile clients, tapping on the icon will display the message.</span><span class="sxs-lookup"><span data-stu-id="7c50c-105">On Dynamics 365 for Customer Engagement apps mobile clients, tapping on the icon will display the message.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="7c50c-106">Control types supported</span><span class="sxs-lookup"><span data-stu-id="7c50c-106">Control types supported</span></span>

<span data-ttu-id="7c50c-107">Tất cả</span><span class="sxs-lookup"><span data-stu-id="7c50c-107">All</span></span>

## <a name="syntax"></a><span data-ttu-id="7c50c-108">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="7c50c-108">Syntax</span></span>

`formContext.getControl(arg).setNotification(message,uniqueId);`

## <a name="parameters"></a><span data-ttu-id="7c50c-109">Tham số</span><span class="sxs-lookup"><span data-stu-id="7c50c-109">Parameters</span></span>

|<span data-ttu-id="7c50c-110">Tên</span><span class="sxs-lookup"><span data-stu-id="7c50c-110">Name</span></span> | <span data-ttu-id="7c50c-111">Loại</span><span class="sxs-lookup"><span data-stu-id="7c50c-111">Type</span></span> | <span data-ttu-id="7c50c-112">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="7c50c-112">Required</span></span> | <span data-ttu-id="7c50c-113">Mô tả</span><span class="sxs-lookup"><span data-stu-id="7c50c-113">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="7c50c-114">message</span><span class="sxs-lookup"><span data-stu-id="7c50c-114">message</span></span> |<span data-ttu-id="7c50c-115">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="7c50c-115">String</span></span> |<span data-ttu-id="7c50c-116">Có</span><span class="sxs-lookup"><span data-stu-id="7c50c-116">Yes</span></span>|<span data-ttu-id="7c50c-117">The message to display.</span><span class="sxs-lookup"><span data-stu-id="7c50c-117">The message to display.</span></span>| 
|<span data-ttu-id="7c50c-118">uniqueId</span><span class="sxs-lookup"><span data-stu-id="7c50c-118">uniqueId</span></span> |<span data-ttu-id="7c50c-119">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="7c50c-119">String</span></span> |<span data-ttu-id="7c50c-120">Không</span><span class="sxs-lookup"><span data-stu-id="7c50c-120">No</span></span>|<span data-ttu-id="7c50c-121">The ID to use to clear this message when using the **clearNotification** method.</span><span class="sxs-lookup"><span data-stu-id="7c50c-121">The ID to use to clear this message when using the **clearNotification** method.</span></span>
| | |

## <a name="return-value"></a><span data-ttu-id="7c50c-122">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="7c50c-122">Return Value</span></span>
<span data-ttu-id="7c50c-123">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="7c50c-123">**Type**: Boolean</span></span> 

<span data-ttu-id="7c50c-124">**Description**: Indicates whether the method succeeded.</span><span class="sxs-lookup"><span data-stu-id="7c50c-124">**Description**: Indicates whether the method succeeded.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c50c-125">Chú thích</span><span class="sxs-lookup"><span data-stu-id="7c50c-125">Remarks</span></span>

<span data-ttu-id="7c50c-126">Setting an error notification on a control will block the form from saving.</span><span class="sxs-lookup"><span data-stu-id="7c50c-126">Setting an error notification on a control will block the form from saving.</span></span>

### <a name="related-topics"></a><span data-ttu-id="7c50c-127">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="7c50c-127">Related topics</span></span>

[<span data-ttu-id="7c50c-128">addNotification</span><span class="sxs-lookup"><span data-stu-id="7c50c-128">addNotification</span></span>](addNotification.md)

[<span data-ttu-id="7c50c-129">clearNotification</span><span class="sxs-lookup"><span data-stu-id="7c50c-129">clearNotification</span></span>](clearNotification.md)
