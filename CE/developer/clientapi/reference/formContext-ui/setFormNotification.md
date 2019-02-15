---
title: setFormNotification (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 48749e32-8490-4c8f-917c-3f1f8b9c028b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d7097f7ee2dd4557b4be9c9ba6d670c4151d31b5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388581"
---
# <a name="setformnotification-client-api-reference"></a><span data-ttu-id="a7603-102">setFormNotification (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="a7603-102">setFormNotification (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setFormNotification-description.md](./includes/setFormNotification-description.md)]

<span data-ttu-id="a7603-103">You can display any number of notifications and they will be displayed until they are removed using [clearFormNotification](clearFormNotification.md).</span><span class="sxs-lookup"><span data-stu-id="a7603-103">You can display any number of notifications and they will be displayed until they are removed using [clearFormNotification](clearFormNotification.md).</span></span> <span data-ttu-id="a7603-104">The height of the notification area is limited so each new message will be added to the top.</span><span class="sxs-lookup"><span data-stu-id="a7603-104">The height of the notification area is limited so each new message will be added to the top.</span></span> <span data-ttu-id="a7603-105">Users can scroll down to view older messages that have not yet been removed.</span><span class="sxs-lookup"><span data-stu-id="a7603-105">Users can scroll down to view older messages that have not yet been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7603-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="a7603-106">Syntax</span></span>

`formContext.ui.setFormNotification(message, level, uniqueId);`

## <a name="parameter"></a><span data-ttu-id="a7603-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="a7603-107">Parameter</span></span>

|<span data-ttu-id="a7603-108">Tên</span><span class="sxs-lookup"><span data-stu-id="a7603-108">Name</span></span>|<span data-ttu-id="a7603-109">Loại</span><span class="sxs-lookup"><span data-stu-id="a7603-109">Type</span></span>|<span data-ttu-id="a7603-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="a7603-110">Required</span></span>|<span data-ttu-id="a7603-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a7603-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="a7603-112">message</span><span class="sxs-lookup"><span data-stu-id="a7603-112">message</span></span>|<span data-ttu-id="a7603-113">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="a7603-113">String</span></span>|<span data-ttu-id="a7603-114">Có</span><span class="sxs-lookup"><span data-stu-id="a7603-114">Yes</span></span>|<span data-ttu-id="a7603-115">The text of the message.</span><span class="sxs-lookup"><span data-stu-id="a7603-115">The text of the message.</span></span>|
|<span data-ttu-id="a7603-116">level</span><span class="sxs-lookup"><span data-stu-id="a7603-116">level</span></span>|<span data-ttu-id="a7603-117">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="a7603-117">String</span></span>|<span data-ttu-id="a7603-118">Có</span><span class="sxs-lookup"><span data-stu-id="a7603-118">Yes</span></span>|<span data-ttu-id="a7603-119">The level of the message, which defines how the message will be displayed.</span><span class="sxs-lookup"><span data-stu-id="a7603-119">The level of the message, which defines how the message will be displayed.</span></span> <span data-ttu-id="a7603-120">Specify one of the following values:</span><span class="sxs-lookup"><span data-stu-id="a7603-120">Specify one of the following values:</span></span><br><span data-ttu-id="a7603-121">`ERROR` : Notification will use the system error icon.</span><span class="sxs-lookup"><span data-stu-id="a7603-121">`ERROR` : Notification will use the system error icon.</span></span><br/><span data-ttu-id="a7603-122">`WARNING` : Notification will use the system warning icon.</span><span class="sxs-lookup"><span data-stu-id="a7603-122">`WARNING` : Notification will use the system warning icon.</span></span><br/><span data-ttu-id="a7603-123">`INFO` : Notification will use the system info icon.</span><span class="sxs-lookup"><span data-stu-id="a7603-123">`INFO` : Notification will use the system info icon.</span></span>|
|<span data-ttu-id="a7603-124">uniqueId</span><span class="sxs-lookup"><span data-stu-id="a7603-124">uniqueId</span></span>|<span data-ttu-id="a7603-125">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="a7603-125">String</span></span>|<span data-ttu-id="a7603-126">Có</span><span class="sxs-lookup"><span data-stu-id="a7603-126">Yes</span></span>|<span data-ttu-id="a7603-127">A unique identifier for the message that can be used later with [clearFormNotification](clearFormNotification.md) to remove the notification.</span><span class="sxs-lookup"><span data-stu-id="a7603-127">A unique identifier for the message that can be used later with [clearFormNotification](clearFormNotification.md) to remove the notification.</span></span>|

## <a name="return-value"></a><span data-ttu-id="a7603-128">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="a7603-128">Return Value</span></span>

<span data-ttu-id="a7603-129">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="a7603-129">**Type**: Boolean</span></span>

<span data-ttu-id="a7603-130">**Description**: true if the method succeeded; false otherwise.</span><span class="sxs-lookup"><span data-stu-id="a7603-130">**Description**: true if the method succeeded; false otherwise.</span></span> 


### <a name="related-topics"></a><span data-ttu-id="a7603-131">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="a7603-131">Related topics</span></span>

[<span data-ttu-id="a7603-132">clearFormNotification</span><span class="sxs-lookup"><span data-stu-id="a7603-132">clearFormNotification</span></span>](clearFormNotification.md)

[<span data-ttu-id="a7603-133">formContext.ui</span><span class="sxs-lookup"><span data-stu-id="a7603-133">formContext.ui</span></span>](../formContext-ui.md)

[<span data-ttu-id="a7603-134">formContext</span><span class="sxs-lookup"><span data-stu-id="a7603-134">formContext</span></span>](../../clientapi-form-context.md)

