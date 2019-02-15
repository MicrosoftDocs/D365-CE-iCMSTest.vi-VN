---
title: getGlobalContext.client (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 89123cde-7c66-4c7d-94e4-e287285019f8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 697ab7190ff4e131e40c3a5a09803fd333cd0883
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388715"
---
# <a name="getglobalcontextclient-client-api-reference"></a><span data-ttu-id="6afdd-102">getGlobalContext.client (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="6afdd-102">getGlobalContext.client (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6afdd-103">Provides access to the methods to determine which client is being used, whether the client is connected to the server, and what kind of device is being used.</span><span class="sxs-lookup"><span data-stu-id="6afdd-103">Provides access to the methods to determine which client is being used, whether the client is connected to the server, and what kind of device is being used.</span></span>

`var clientContext = Xrm.Utility.getGlobalContext().client`

<span data-ttu-id="6afdd-104">The following methods are available for the client context.</span><span class="sxs-lookup"><span data-stu-id="6afdd-104">The following methods are available for the client context.</span></span>

## <a name="getclient"></a><span data-ttu-id="6afdd-105">getClient</span><span class="sxs-lookup"><span data-stu-id="6afdd-105">getClient</span></span>

<span data-ttu-id="6afdd-106">Returns a value to indicate which client the script is executing in.</span><span class="sxs-lookup"><span data-stu-id="6afdd-106">Returns a value to indicate which client the script is executing in.</span></span> 

### <a name="syntax"></a><span data-ttu-id="6afdd-107">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="6afdd-107">Syntax</span></span>

`clientContext.getClient()`

### <a name="return-value"></a><span data-ttu-id="6afdd-108">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="6afdd-108">Return Value</span></span>

<span data-ttu-id="6afdd-109">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="6afdd-109">**Type**: String</span></span>

<span data-ttu-id="6afdd-110">**Description**: The values returned are:</span><span class="sxs-lookup"><span data-stu-id="6afdd-110">**Description**: The values returned are:</span></span>

<span data-ttu-id="6afdd-111">Value</span><span class="sxs-lookup"><span data-stu-id="6afdd-111">Value</span></span> |<span data-ttu-id="6afdd-112">Máy khách</span><span class="sxs-lookup"><span data-stu-id="6afdd-112">Client</span></span> | 
|---|---|
|<span data-ttu-id="6afdd-113">Web</span><span class="sxs-lookup"><span data-stu-id="6afdd-113">Web</span></span> |<span data-ttu-id="6afdd-114">Web application</span><span class="sxs-lookup"><span data-stu-id="6afdd-114">Web application</span></span>|
|<span data-ttu-id="6afdd-115">Web</span><span class="sxs-lookup"><span data-stu-id="6afdd-115">Web</span></span> |<span data-ttu-id="6afdd-116">Giao diện Hợp nhất</span><span class="sxs-lookup"><span data-stu-id="6afdd-116">Unified Interface</span></span>|
|<span data-ttu-id="6afdd-117">Outlook</span><span class="sxs-lookup"><span data-stu-id="6afdd-117">Outlook</span></span> |<span data-ttu-id="6afdd-118">Outlook</span><span class="sxs-lookup"><span data-stu-id="6afdd-118">Outlook</span></span> |
|<span data-ttu-id="6afdd-119">Di động</span><span class="sxs-lookup"><span data-stu-id="6afdd-119">Mobile</span></span> |<span data-ttu-id="6afdd-120">Ứng dụng di động</span><span class="sxs-lookup"><span data-stu-id="6afdd-120">Mobile app</span></span> |

## <a name="getclientstate"></a><span data-ttu-id="6afdd-121">getClientState</span><span class="sxs-lookup"><span data-stu-id="6afdd-121">getClientState</span></span>

<span data-ttu-id="6afdd-122">Returns a value to indicate the state of the client.</span><span class="sxs-lookup"><span data-stu-id="6afdd-122">Returns a value to indicate the state of the client.</span></span>

### <a name="syntax"></a><span data-ttu-id="6afdd-123">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="6afdd-123">Syntax</span></span>

`clientContext.getClientState()`

### <a name="return-value"></a><span data-ttu-id="6afdd-124">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="6afdd-124">Return Value</span></span>

<span data-ttu-id="6afdd-125">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="6afdd-125">**Type**: String</span></span>

<span data-ttu-id="6afdd-126">**Description**: The values returned are:</span><span class="sxs-lookup"><span data-stu-id="6afdd-126">**Description**: The values returned are:</span></span>

<span data-ttu-id="6afdd-127">Value</span><span class="sxs-lookup"><span data-stu-id="6afdd-127">Value</span></span> |<span data-ttu-id="6afdd-128">Máy khách</span><span class="sxs-lookup"><span data-stu-id="6afdd-128">Client</span></span> | 
|---|---|
|<span data-ttu-id="6afdd-129">Trực tuyến</span><span class="sxs-lookup"><span data-stu-id="6afdd-129">Online</span></span> |<span data-ttu-id="6afdd-130">Web application, Outlook, Mobile app, Unified Interface</span><span class="sxs-lookup"><span data-stu-id="6afdd-130">Web application, Outlook, Mobile app, Unified Interface</span></span>|
|<span data-ttu-id="6afdd-131">Offline</span><span class="sxs-lookup"><span data-stu-id="6afdd-131">Offline</span></span> |<span data-ttu-id="6afdd-132">Outlook, Mobile app</span><span class="sxs-lookup"><span data-stu-id="6afdd-132">Outlook, Mobile app</span></span>|

## <a name="getformfactor"></a><span data-ttu-id="6afdd-133">getFormFactor</span><span class="sxs-lookup"><span data-stu-id="6afdd-133">getFormFactor</span></span>

<span data-ttu-id="6afdd-134">Returns information about the kind of device the user is using.</span><span class="sxs-lookup"><span data-stu-id="6afdd-134">Returns information about the kind of device the user is using.</span></span>

### <a name="syntax"></a><span data-ttu-id="6afdd-135">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="6afdd-135">Syntax</span></span>

`clientContext.getFormFactor()`

### <a name="return-value"></a><span data-ttu-id="6afdd-136">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="6afdd-136">Return Value</span></span>

<span data-ttu-id="6afdd-137">**Type**: Number</span><span class="sxs-lookup"><span data-stu-id="6afdd-137">**Type**: Number</span></span>

<span data-ttu-id="6afdd-138">**Description**: The values returned are:</span><span class="sxs-lookup"><span data-stu-id="6afdd-138">**Description**: The values returned are:</span></span>

<span data-ttu-id="6afdd-139">Value</span><span class="sxs-lookup"><span data-stu-id="6afdd-139">Value</span></span> |<span data-ttu-id="6afdd-140">Nhân tố biểu mẫu</span><span class="sxs-lookup"><span data-stu-id="6afdd-140">Form Factor</span></span> | 
|---|---|
|<span data-ttu-id="6afdd-141">0</span><span class="sxs-lookup"><span data-stu-id="6afdd-141">0</span></span> |<span data-ttu-id="6afdd-142">Unknown</span><span class="sxs-lookup"><span data-stu-id="6afdd-142">Unknown</span></span>|
|<span data-ttu-id="6afdd-143">1</span><span class="sxs-lookup"><span data-stu-id="6afdd-143">1</span></span> |<span data-ttu-id="6afdd-144">Desktop</span><span class="sxs-lookup"><span data-stu-id="6afdd-144">Desktop</span></span>|
|<span data-ttu-id="6afdd-145">2</span><span class="sxs-lookup"><span data-stu-id="6afdd-145">2</span></span> |<span data-ttu-id="6afdd-146">Máy tính bảng</span><span class="sxs-lookup"><span data-stu-id="6afdd-146">Tablet</span></span> |
|<span data-ttu-id="6afdd-147">3</span><span class="sxs-lookup"><span data-stu-id="6afdd-147">3</span></span> |<span data-ttu-id="6afdd-148">Số điện thoại</span><span class="sxs-lookup"><span data-stu-id="6afdd-148">Phone</span></span> |

## <a name="isoffline"></a><span data-ttu-id="6afdd-149">isOffline</span><span class="sxs-lookup"><span data-stu-id="6afdd-149">isOffline</span></span>

<span data-ttu-id="6afdd-150">Returns information whether the server is online or offline.</span><span class="sxs-lookup"><span data-stu-id="6afdd-150">Returns information whether the server is online or offline.</span></span>

### <a name="syntax"></a><span data-ttu-id="6afdd-151">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="6afdd-151">Syntax</span></span>

`clientContext.isOffline()`

### <a name="return-value"></a><span data-ttu-id="6afdd-152">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="6afdd-152">Return Value</span></span>

<span data-ttu-id="6afdd-153">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="6afdd-153">**Type**: Boolean</span></span>

<span data-ttu-id="6afdd-154">**Description**: **true** if the server is offline; **false** otherwise.</span><span class="sxs-lookup"><span data-stu-id="6afdd-154">**Description**: **true** if the server is offline; **false** otherwise.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6afdd-155">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="6afdd-155">Related topics</span></span>

[<span data-ttu-id="6afdd-156">Organization Settings</span><span class="sxs-lookup"><span data-stu-id="6afdd-156">Organization Settings</span></span>](organizationSettings.md)

[<span data-ttu-id="6afdd-157">Thiết đặt người dùng</span><span class="sxs-lookup"><span data-stu-id="6afdd-157">User Settings</span></span>](userSettings.md)

[<span data-ttu-id="6afdd-158">Xrm.Utility.getGlobalContext</span><span class="sxs-lookup"><span data-stu-id="6afdd-158">Xrm.Utility.getGlobalContext</span></span>](../getGlobalContext.md)

