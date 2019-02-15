---
title: clearFormNotification (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: d60ec5344717164aa87b49c6f552d442ff213d1c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387841"
---
# <a name="clearformnotification-client-api-reference"></a><span data-ttu-id="c8e85-102">clearFormNotification (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="c8e85-102">clearFormNotification (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/clearFormNotification-description.md](./includes/clearFormNotification-description.md)]

## <a name="syntax"></a><span data-ttu-id="c8e85-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="c8e85-103">Syntax</span></span>

`formContext.ui.clearFormNotification(uniqueId)`

## <a name="parameter"></a><span data-ttu-id="c8e85-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="c8e85-104">Parameter</span></span>

|<span data-ttu-id="c8e85-105">Tên</span><span class="sxs-lookup"><span data-stu-id="c8e85-105">Name</span></span>|<span data-ttu-id="c8e85-106">Loại</span><span class="sxs-lookup"><span data-stu-id="c8e85-106">Type</span></span>|<span data-ttu-id="c8e85-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="c8e85-107">Required</span></span>|<span data-ttu-id="c8e85-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="c8e85-108">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="c8e85-109">uniqueId</span><span class="sxs-lookup"><span data-stu-id="c8e85-109">uniqueId</span></span>|<span data-ttu-id="c8e85-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="c8e85-110">String</span></span>|<span data-ttu-id="c8e85-111">Có</span><span class="sxs-lookup"><span data-stu-id="c8e85-111">Yes</span></span>|<span data-ttu-id="c8e85-112">A unique identifier for the message to be cleared that was set using the [setFormNotification](setFormNotification.md) method.</span><span class="sxs-lookup"><span data-stu-id="c8e85-112">A unique identifier for the message to be cleared that was set using the [setFormNotification](setFormNotification.md) method.</span></span>|

## <a name="return-value"></a><span data-ttu-id="c8e85-113">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="c8e85-113">Return Value</span></span>

<span data-ttu-id="c8e85-114">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="c8e85-114">**Type**: Boolean</span></span>

<span data-ttu-id="c8e85-115">**Description**: true if the method succeeded, false otherwise.</span><span class="sxs-lookup"><span data-stu-id="c8e85-115">**Description**: true if the method succeeded, false otherwise.</span></span> 


### <a name="related-topics"></a><span data-ttu-id="c8e85-116">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="c8e85-116">Related topics</span></span>

[<span data-ttu-id="c8e85-117">setFormNotification</span><span class="sxs-lookup"><span data-stu-id="c8e85-117">setFormNotification</span></span>](setFormNotification.md)

[<span data-ttu-id="c8e85-118">formContext.ui</span><span class="sxs-lookup"><span data-stu-id="c8e85-118">formContext.ui</span></span>](../formContext-ui.md)

[<span data-ttu-id="c8e85-119">formContext</span><span class="sxs-lookup"><span data-stu-id="c8e85-119">formContext</span></span>](../../clientapi-form-context.md)

