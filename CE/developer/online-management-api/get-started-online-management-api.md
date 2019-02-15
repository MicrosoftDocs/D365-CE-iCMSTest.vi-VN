---
title: Get started with Online Management API for Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Provides basic information to help you get started with the Online Admin API for Customer Engagement.
ms.date: 11/16/2018
ms.service: crm-online
ms.topic: conceptual
ms.assetid: c292c148-01f0-41f6-a2fe-7ed05a01a733
author: KumarVivek
ms.author: kvivek
manager: annbe
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8f10d0d562b7ef11bc42f558e9c1a52eeb8c5159
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387893"
---
# <a name="get-started-with-online-management-api"></a><span data-ttu-id="3fdfa-103">Get started with Online Management API</span><span class="sxs-lookup"><span data-stu-id="3fdfa-103">Get started with Online Management API</span></span> 

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3fdfa-104">This topic provides basic information to help you get started with the Online Admin API for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="3fdfa-104">This topic provides basic information to help you get started with the Online Admin API for Customer Engagement.</span></span>

## <a name="office-365-admin-roles"></a><span data-ttu-id="3fdfa-105">Office 365 Admin roles</span><span class="sxs-lookup"><span data-stu-id="3fdfa-105">Office 365 Admin roles</span></span>

<span data-ttu-id="3fdfa-106">To use the Online Management API, you must have one of the following admin roles assigned to you in your Office 365 tenant:</span><span class="sxs-lookup"><span data-stu-id="3fdfa-106">To use the Online Management API, you must have one of the following admin roles assigned to you in your Office 365 tenant:</span></span>

- <span data-ttu-id="3fdfa-107">Global administrator</span><span class="sxs-lookup"><span data-stu-id="3fdfa-107">Global administrator</span></span>
- <span data-ttu-id="3fdfa-108">Service administrator</span><span class="sxs-lookup"><span data-stu-id="3fdfa-108">Service administrator</span></span>

<span data-ttu-id="3fdfa-109">For information about these roles, see [About Office 365 admin roles](https://support.office.com/en-us/article/About-Office-365-admin-roles-da585eea-f576-4f55-a1e0-87090b6aaa9d)</span><span class="sxs-lookup"><span data-stu-id="3fdfa-109">For information about these roles, see [About Office 365 admin roles](https://support.office.com/en-us/article/About-Office-365-admin-roles-da585eea-f576-4f55-a1e0-87090b6aaa9d)</span></span>

## <a name="service-url"></a><span data-ttu-id="3fdfa-110">Service URL</span><span class="sxs-lookup"><span data-stu-id="3fdfa-110">Service URL</span></span>

<span data-ttu-id="3fdfa-111">The service URL defines the endpoint address for accessing REST API.</span><span class="sxs-lookup"><span data-stu-id="3fdfa-111">The service URL defines the endpoint address for accessing REST API.</span></span> <span data-ttu-id="3fdfa-112">To perform any operation using the Online Management API, you need to specify the request URL in the following format:</span><span class="sxs-lookup"><span data-stu-id="3fdfa-112">To perform any operation using the Online Management API, you need to specify the request URL in the following format:</span></span>

`{ServiceUrl}/api/v1.1/{resource}`

<span data-ttu-id="3fdfa-113">For example, you can pass in the following URL with a **GET** request to retrieve the instances in your Office 365 tenant in North America:</span><span class="sxs-lookup"><span data-stu-id="3fdfa-113">For example, you can pass in the following URL with a **GET** request to retrieve the instances in your Office 365 tenant in North America:</span></span>

`https://admin.services.crm.dynamics.com/api/v1.1/instances`


<span data-ttu-id="3fdfa-114">The following table lists the service URL of Online Management API for worldwide Office 365 data centers.</span><span class="sxs-lookup"><span data-stu-id="3fdfa-114">The following table lists the service URL of Online Management API for worldwide Office 365 data centers.</span></span>

|<span data-ttu-id="3fdfa-115">Location</span><span class="sxs-lookup"><span data-stu-id="3fdfa-115">Location</span></span> | <span data-ttu-id="3fdfa-116">Service URL</span><span class="sxs-lookup"><span data-stu-id="3fdfa-116">Service URL</span></span> |
|---------|-------------|
|<span data-ttu-id="3fdfa-117">Bắc Mỹ</span><span class="sxs-lookup"><span data-stu-id="3fdfa-117">North America</span></span> | https://admin.services.crm.dynamics.com |
|<span data-ttu-id="3fdfa-118">Bắc Mỹ 2</span><span class="sxs-lookup"><span data-stu-id="3fdfa-118">North America 2</span></span> | https://admin.services.crm9.dynamics.com |
|<span data-ttu-id="3fdfa-119">Châu Âu, Trung Đông và Châu Phi (EMEA)</span><span class="sxs-lookup"><span data-stu-id="3fdfa-119">Europe, Middle East and Africa (EMEA)</span></span> | https://admin.services.crm4.dynamics.com |
|<span data-ttu-id="3fdfa-120">Asia Pacific (APAC)</span><span class="sxs-lookup"><span data-stu-id="3fdfa-120">Asia Pacific (APAC)</span></span> | https://admin.services.crm5.dynamics.com |
|<span data-ttu-id="3fdfa-121">Châu Đại Dương</span><span class="sxs-lookup"><span data-stu-id="3fdfa-121">Oceania</span></span> | https://admin.services.crm6.dynamics.com |
|<span data-ttu-id="3fdfa-122">Nhật Bản (JPN)</span><span class="sxs-lookup"><span data-stu-id="3fdfa-122">Japan (JPN)</span></span> | https://admin.services.crm7.dynamics.com |
|<span data-ttu-id="3fdfa-123">Nam Mỹ</span><span class="sxs-lookup"><span data-stu-id="3fdfa-123">South America</span></span> | https://admin.services.crm2.dynamics.com |
|<span data-ttu-id="3fdfa-124">Ấn Độ (IND)</span><span class="sxs-lookup"><span data-stu-id="3fdfa-124">India (IND)</span></span> | https://admin.services.crm8.dynamics.com |
|<span data-ttu-id="3fdfa-125">Canada</span><span class="sxs-lookup"><span data-stu-id="3fdfa-125">Canada</span></span> | https://admin.services.crm3.dynamics.com |
|<span data-ttu-id="3fdfa-126">Vương quốc Anh (UK)</span><span class="sxs-lookup"><span data-stu-id="3fdfa-126">United Kingdom (UK)</span></span> | https://admin.services.crm11.dynamics.com |


## <a name="standard-headers"></a><span data-ttu-id="3fdfa-127">Standard headers</span><span class="sxs-lookup"><span data-stu-id="3fdfa-127">Standard headers</span></span>

<span data-ttu-id="3fdfa-128">The Online Management API has following standard request and response headers.</span><span class="sxs-lookup"><span data-stu-id="3fdfa-128">The Online Management API has following standard request and response headers.</span></span>   

### <a name="request-headers"></a><span data-ttu-id="3fdfa-129">Request headers</span><span class="sxs-lookup"><span data-stu-id="3fdfa-129">Request headers</span></span>

| <span data-ttu-id="3fdfa-130">Dòng đầu trang</span><span class="sxs-lookup"><span data-stu-id="3fdfa-130">Header</span></span> | <span data-ttu-id="3fdfa-131">Loại</span><span class="sxs-lookup"><span data-stu-id="3fdfa-131">Type</span></span> | <span data-ttu-id="3fdfa-132">Mô tả</span><span class="sxs-lookup"><span data-stu-id="3fdfa-132">Description</span></span>  |
|--------|------|--------------|
|<span data-ttu-id="3fdfa-133">**Accept-Language**</span><span class="sxs-lookup"><span data-stu-id="3fdfa-133">**Accept-Language**</span></span>|<span data-ttu-id="3fdfa-134">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="3fdfa-134">String</span></span>|<span data-ttu-id="3fdfa-135">Specifies the preferred language for the response.</span><span class="sxs-lookup"><span data-stu-id="3fdfa-135">Specifies the preferred language for the response.</span></span> <span data-ttu-id="3fdfa-136">More information about the header: [Accept-Language (MDN web docs)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Accept-Language)</span><span class="sxs-lookup"><span data-stu-id="3fdfa-136">More information about the header: [Accept-Language (MDN web docs)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Accept-Language)</span></span>|
|<span data-ttu-id="3fdfa-137">**Authorization**</span><span class="sxs-lookup"><span data-stu-id="3fdfa-137">**Authorization**</span></span>|<span data-ttu-id="3fdfa-138">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="3fdfa-138">String</span></span>|<span data-ttu-id="3fdfa-139">Specifies the credentials to authenticate a user with the Online Management API service.</span><span class="sxs-lookup"><span data-stu-id="3fdfa-139">Specifies the credentials to authenticate a user with the Online Management API service.</span></span> <span data-ttu-id="3fdfa-140">More information about the header: [Authorization (MDN web docs)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Authorization)</span><span class="sxs-lookup"><span data-stu-id="3fdfa-140">More information about the header: [Authorization (MDN web docs)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Authorization)</span></span>|

<span data-ttu-id="3fdfa-141">See [Authenticate to use the Online Management API](authentication.md) to know about setting these headers in your request.</span><span class="sxs-lookup"><span data-stu-id="3fdfa-141">See [Authenticate to use the Online Management API](authentication.md) to know about setting these headers in your request.</span></span>

### <a name="response-headers"></a><span data-ttu-id="3fdfa-142">Response headers</span><span class="sxs-lookup"><span data-stu-id="3fdfa-142">Response headers</span></span>

| <span data-ttu-id="3fdfa-143">Dòng đầu trang</span><span class="sxs-lookup"><span data-stu-id="3fdfa-143">Header</span></span> | <span data-ttu-id="3fdfa-144">Mô tả</span><span class="sxs-lookup"><span data-stu-id="3fdfa-144">Description</span></span>  |
|--------|--------------|
|<span data-ttu-id="3fdfa-145">**Operation-Location**</span><span class="sxs-lookup"><span data-stu-id="3fdfa-145">**Operation-Location**</span></span>|<span data-ttu-id="3fdfa-146">For long-running operations, specifies the location of the operation query to check its status.</span><span class="sxs-lookup"><span data-stu-id="3fdfa-146">For long-running operations, specifies the location of the operation query to check its status.</span></span> <span data-ttu-id="3fdfa-147">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="3fdfa-147">For example:</span></span><br />`https://admin.services.crm.dynamics.com/operations/{operationid}`|
|<span data-ttu-id="3fdfa-148">**Retry-After**</span><span class="sxs-lookup"><span data-stu-id="3fdfa-148">**Retry-After**</span></span>|<span data-ttu-id="3fdfa-149">For long-running operations, specifies the recommended period in seconds after which to query the operation status again.</span><span class="sxs-lookup"><span data-stu-id="3fdfa-149">For long-running operations, specifies the recommended period in seconds after which to query the operation status again.</span></span> <span data-ttu-id="3fdfa-150">For example: **30**</span><span class="sxs-lookup"><span data-stu-id="3fdfa-150">For example: **30**</span></span>|
    
### <a name="related-topics"></a><span data-ttu-id="3fdfa-151">Related Topics</span><span class="sxs-lookup"><span data-stu-id="3fdfa-151">Related Topics</span></span>  

[<span data-ttu-id="3fdfa-152">Authenticate to use Online Management API</span><span class="sxs-lookup"><span data-stu-id="3fdfa-152">Authenticate to use Online Management API</span></span>](authentication.md)

[<span data-ttu-id="3fdfa-153">Operations supported by Online Management API</span><span class="sxs-lookup"><span data-stu-id="3fdfa-153">Operations supported by Online Management API</span></span>](operations-supported.md)

[<span data-ttu-id="3fdfa-154">Online Management API Reference</span><span class="sxs-lookup"><span data-stu-id="3fdfa-154">Online Management API Reference</span></span>](/rest/api/admin.services.crm.dynamics.com)
