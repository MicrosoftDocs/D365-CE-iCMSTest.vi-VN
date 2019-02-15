---
title: getGlobalContext.organizationSettings (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: badf4f82-cb47-4864-aa43-bb777d04de4d
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 33e1eb7088e5c592b1824cab5275f8299c86bc96
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387530"
---
# <a name="getglobalcontextorganizationsettings-client-api-reference"></a><span data-ttu-id="16a87-102">getGlobalContext.organizationSettings (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="16a87-102">getGlobalContext.organizationSettings (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="16a87-103">Returns information about the current organization settings.</span><span class="sxs-lookup"><span data-stu-id="16a87-103">Returns information about the current organization settings.</span></span> 

`var organizationSettings = Xrm.Utility.getGlobalContext().organizationSettings`

<span data-ttu-id="16a87-104">The **organizationSettings** object provides following properties.</span><span class="sxs-lookup"><span data-stu-id="16a87-104">The **organizationSettings** object provides following properties.</span></span>

## <a name="attributes"></a><span data-ttu-id="16a87-105">attributes</span><span class="sxs-lookup"><span data-stu-id="16a87-105">attributes</span></span>

<span data-ttu-id="16a87-106">Returns attributes and their values as `key:value` pairs that are available for the organization entity.</span><span class="sxs-lookup"><span data-stu-id="16a87-106">Returns attributes and their values as `key:value` pairs that are available for the organization entity.</span></span> <span data-ttu-id="16a87-107">Additional values will be available as attributes if they are specified as attribute dependencies in the web resource dependency list.</span><span class="sxs-lookup"><span data-stu-id="16a87-107">Additional values will be available as attributes if they are specified as attribute dependencies in the web resource dependency list.</span></span> <span data-ttu-id="16a87-108">The `key` will be the attribute logical name.</span><span class="sxs-lookup"><span data-stu-id="16a87-108">The `key` will be the attribute logical name.</span></span>

### <a name="syntax"></a><span data-ttu-id="16a87-109">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="16a87-109">Syntax</span></span>

`organizationSettings.attributes`

### <a name="return-value"></a><span data-ttu-id="16a87-110">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="16a87-110">Return Value</span></span>

<span data-ttu-id="16a87-111">**Type**: Object</span><span class="sxs-lookup"><span data-stu-id="16a87-111">**Type**: Object</span></span>

<span data-ttu-id="16a87-112">**Description**: An object with attributes and their values.</span><span class="sxs-lookup"><span data-stu-id="16a87-112">**Description**: An object with attributes and their values.</span></span>

## <a name="basecurrencyid"></a><span data-ttu-id="16a87-113">baseCurrencyId</span><span class="sxs-lookup"><span data-stu-id="16a87-113">baseCurrencyId</span></span> 

<span data-ttu-id="16a87-114">Returns the ID of the base currency for the current organization.</span><span class="sxs-lookup"><span data-stu-id="16a87-114">Returns the ID of the base currency for the current organization.</span></span>

### <a name="syntax"></a><span data-ttu-id="16a87-115">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="16a87-115">Syntax</span></span>

`organizationSettings.baseCurrencyId`

### <a name="return-value"></a><span data-ttu-id="16a87-116">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="16a87-116">Return Value</span></span>

<span data-ttu-id="16a87-117">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="16a87-117">**Type**: String</span></span>

<span data-ttu-id="16a87-118">**Description**: ID of the base currency.</span><span class="sxs-lookup"><span data-stu-id="16a87-118">**Description**: ID of the base currency.</span></span>

## <a name="defaultcountrycode"></a><span data-ttu-id="16a87-119">defaultCountryCode</span><span class="sxs-lookup"><span data-stu-id="16a87-119">defaultCountryCode</span></span> 

<span data-ttu-id="16a87-120">Returns the default country/region code for phone numbers for the current organization.</span><span class="sxs-lookup"><span data-stu-id="16a87-120">Returns the default country/region code for phone numbers for the current organization.</span></span>

### <a name="syntax"></a><span data-ttu-id="16a87-121">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="16a87-121">Syntax</span></span>

`organizationSettings.defaultCountryCode`

### <a name="return-value"></a><span data-ttu-id="16a87-122">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="16a87-122">Return Value</span></span>

<span data-ttu-id="16a87-123">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="16a87-123">**Type**: String</span></span>

<span data-ttu-id="16a87-124">**Description**: Default country/region code for phone numbers.</span><span class="sxs-lookup"><span data-stu-id="16a87-124">**Description**: Default country/region code for phone numbers.</span></span>

## <a name="isautosaveenabled"></a><span data-ttu-id="16a87-125">isAutoSaveEnabled</span><span class="sxs-lookup"><span data-stu-id="16a87-125">isAutoSaveEnabled</span></span> 

<span data-ttu-id="16a87-126">Indicates whether the auto-save option is enabled for the current organization.</span><span class="sxs-lookup"><span data-stu-id="16a87-126">Indicates whether the auto-save option is enabled for the current organization.</span></span>

### <a name="syntax"></a><span data-ttu-id="16a87-127">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="16a87-127">Syntax</span></span>

`organizationSettings.isAutoSaveEnabled`

### <a name="return-value"></a><span data-ttu-id="16a87-128">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="16a87-128">Return Value</span></span>

<span data-ttu-id="16a87-129">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="16a87-129">**Type**: Boolean</span></span>

<span data-ttu-id="16a87-130">**Description**: **true** if enabled; **false** otherwise.</span><span class="sxs-lookup"><span data-stu-id="16a87-130">**Description**: **true** if enabled; **false** otherwise.</span></span>

## <a name="languageid"></a><span data-ttu-id="16a87-131">languageId</span><span class="sxs-lookup"><span data-stu-id="16a87-131">languageId</span></span> 

<span data-ttu-id="16a87-132">Returns the preferred language ID for the current organization.</span><span class="sxs-lookup"><span data-stu-id="16a87-132">Returns the preferred language ID for the current organization.</span></span>

### <a name="syntax"></a><span data-ttu-id="16a87-133">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="16a87-133">Syntax</span></span>

`organizationSettings.languageId`

### <a name="return-value"></a><span data-ttu-id="16a87-134">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="16a87-134">Return Value</span></span>

<span data-ttu-id="16a87-135">**Type**: Number</span><span class="sxs-lookup"><span data-stu-id="16a87-135">**Type**: Number</span></span>

<span data-ttu-id="16a87-136">**Description**: Preferred Language ID.</span><span class="sxs-lookup"><span data-stu-id="16a87-136">**Description**: Preferred Language ID.</span></span> <span data-ttu-id="16a87-137">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="16a87-137">For example:</span></span>

`1033`

## <a name="organizationid"></a><span data-ttu-id="16a87-138">organizationId</span><span class="sxs-lookup"><span data-stu-id="16a87-138">organizationId</span></span> 

<span data-ttu-id="16a87-139">Returns the ID of the current organization.</span><span class="sxs-lookup"><span data-stu-id="16a87-139">Returns the ID of the current organization.</span></span>

### <a name="syntax"></a><span data-ttu-id="16a87-140">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="16a87-140">Syntax</span></span>

`organizationSettings.organizationId`

### <a name="return-value"></a><span data-ttu-id="16a87-141">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="16a87-141">Return Value</span></span>

<span data-ttu-id="16a87-142">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="16a87-142">**Type**: String</span></span>

<span data-ttu-id="16a87-143">**Description**: Id of the current organization.</span><span class="sxs-lookup"><span data-stu-id="16a87-143">**Description**: Id of the current organization.</span></span>

## <a name="uniquename"></a><span data-ttu-id="16a87-144">uniqueName</span><span class="sxs-lookup"><span data-stu-id="16a87-144">uniqueName</span></span> 

<span data-ttu-id="16a87-145">Returns the unique name of the current organization.</span><span class="sxs-lookup"><span data-stu-id="16a87-145">Returns the unique name of the current organization.</span></span>

### <a name="syntax"></a><span data-ttu-id="16a87-146">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="16a87-146">Syntax</span></span>

`organizationSettings.uniqueName`

### <a name="return-value"></a><span data-ttu-id="16a87-147">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="16a87-147">Return Value</span></span>

<span data-ttu-id="16a87-148">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="16a87-148">**Type**: String</span></span>

<span data-ttu-id="16a87-149">**Description**: Unique name of the current organization.</span><span class="sxs-lookup"><span data-stu-id="16a87-149">**Description**: Unique name of the current organization.</span></span>

## <a name="useskypeprotocol"></a><span data-ttu-id="16a87-150">useSkypeProtocol</span><span class="sxs-lookup"><span data-stu-id="16a87-150">useSkypeProtocol</span></span> 

<span data-ttu-id="16a87-151">Indicates whether the Skype protocol is used for the current organization.</span><span class="sxs-lookup"><span data-stu-id="16a87-151">Indicates whether the Skype protocol is used for the current organization.</span></span>

### <a name="syntax"></a><span data-ttu-id="16a87-152">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="16a87-152">Syntax</span></span>

`organizationSettings.useSkypeProtocol`

### <a name="return-value"></a><span data-ttu-id="16a87-153">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="16a87-153">Return Value</span></span>

<span data-ttu-id="16a87-154">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="16a87-154">**Type**: Boolean</span></span>

<span data-ttu-id="16a87-155">**Description**: **true** if Skype protocol is used; **false** otherwise.</span><span class="sxs-lookup"><span data-stu-id="16a87-155">**Description**: **true** if Skype protocol is used; **false** otherwise.</span></span>


## <a name="related-topics"></a><span data-ttu-id="16a87-156">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="16a87-156">Related topics</span></span>

[<span data-ttu-id="16a87-157">Client context</span><span class="sxs-lookup"><span data-stu-id="16a87-157">Client context</span></span>](client.md)

[<span data-ttu-id="16a87-158">Cài đặt người dùng</span><span class="sxs-lookup"><span data-stu-id="16a87-158">User settings</span></span>](userSettings.md)

[<span data-ttu-id="16a87-159">Xrm.Utility.getGlobalContext</span><span class="sxs-lookup"><span data-stu-id="16a87-159">Xrm.Utility.getGlobalContext</span></span>](../getGlobalContext.md)
