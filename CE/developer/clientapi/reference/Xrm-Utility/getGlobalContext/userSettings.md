---
title: getGlobalContext.userSettings (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 44296667-f1cd-49be-a300-7259bc3b41e0
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c5c897730b0247272335bec52eadacff1fe51787
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387237"
---
# <a name="getglobalcontextusersettings-client-api-reference"></a><span data-ttu-id="36d22-102">getGlobalContext.userSettings (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="36d22-102">getGlobalContext.userSettings (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="36d22-103">Returns information about the current user settings.</span><span class="sxs-lookup"><span data-stu-id="36d22-103">Returns information about the current user settings.</span></span>

`var userSettings = Xrm.Utility.getGlobalContext().userSettings`

<span data-ttu-id="36d22-104">The **userSettings** object provides following properties and a method.</span><span class="sxs-lookup"><span data-stu-id="36d22-104">The **userSettings** object provides following properties and a method.</span></span>

## <a name="dateformattinginfo"></a><span data-ttu-id="36d22-105">dateFormattingInfo</span><span class="sxs-lookup"><span data-stu-id="36d22-105">dateFormattingInfo</span></span> 

<span data-ttu-id="36d22-106">Returns the date formatting information for the current user.</span><span class="sxs-lookup"><span data-stu-id="36d22-106">Returns the date formatting information for the current user.</span></span>

### <a name="syntax"></a><span data-ttu-id="36d22-107">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="36d22-107">Syntax</span></span>

`userSettings.dateFormattingInfo`

### <a name="return-value"></a><span data-ttu-id="36d22-108">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="36d22-108">Return Value</span></span>

<span data-ttu-id="36d22-109">**Type**: Object</span><span class="sxs-lookup"><span data-stu-id="36d22-109">**Type**: Object</span></span>

<span data-ttu-id="36d22-110">**Description**: An object with information about date formatting such as **FirstDayOfWeek**, **LongDatePattern**, **MonthDayPattern**, **TimeSeparator**, and so on.</span><span class="sxs-lookup"><span data-stu-id="36d22-110">**Description**: An object with information about date formatting such as **FirstDayOfWeek**, **LongDatePattern**, **MonthDayPattern**, **TimeSeparator**, and so on.</span></span>

## <a name="defaultdashboardid"></a><span data-ttu-id="36d22-111">defaultDashboardId</span><span class="sxs-lookup"><span data-stu-id="36d22-111">defaultDashboardId</span></span> 

<span data-ttu-id="36d22-112">Returns the ID of the default dashboard for the current user.</span><span class="sxs-lookup"><span data-stu-id="36d22-112">Returns the ID of the default dashboard for the current user.</span></span>

### <a name="syntax"></a><span data-ttu-id="36d22-113">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="36d22-113">Syntax</span></span>

`userSettings.defaultDashboardId`

### <a name="return-value"></a><span data-ttu-id="36d22-114">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="36d22-114">Return Value</span></span>

<span data-ttu-id="36d22-115">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="36d22-115">**Type**: String</span></span>

<span data-ttu-id="36d22-116">**Description**: ID of the default dashboard.</span><span class="sxs-lookup"><span data-stu-id="36d22-116">**Description**: ID of the default dashboard.</span></span> 

## <a name="isguidedhelpenabled"></a><span data-ttu-id="36d22-117">isGuidedHelpEnabled</span><span class="sxs-lookup"><span data-stu-id="36d22-117">isGuidedHelpEnabled</span></span> 

<span data-ttu-id="36d22-118">Indicates whether guided help is enabled for the current user.</span><span class="sxs-lookup"><span data-stu-id="36d22-118">Indicates whether guided help is enabled for the current user.</span></span>

### <a name="syntax"></a><span data-ttu-id="36d22-119">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="36d22-119">Syntax</span></span>

`userSettings.isGuidedHelpEnabled`

### <a name="return-value"></a><span data-ttu-id="36d22-120">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="36d22-120">Return Value</span></span>

<span data-ttu-id="36d22-121">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="36d22-121">**Type**: Boolean</span></span>

<span data-ttu-id="36d22-122">**Description**: true if enabled; false otherwise.</span><span class="sxs-lookup"><span data-stu-id="36d22-122">**Description**: true if enabled; false otherwise.</span></span> 

## <a name="ishighcontrastenabled"></a><span data-ttu-id="36d22-123">isHighContrastEnabled</span><span class="sxs-lookup"><span data-stu-id="36d22-123">isHighContrastEnabled</span></span> 

<span data-ttu-id="36d22-124">Indicates whether high contrast is enabled for the current user.</span><span class="sxs-lookup"><span data-stu-id="36d22-124">Indicates whether high contrast is enabled for the current user.</span></span>

### <a name="syntax"></a><span data-ttu-id="36d22-125">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="36d22-125">Syntax</span></span>

`userSettings.isHighContrastEnabled`

### <a name="return-value"></a><span data-ttu-id="36d22-126">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="36d22-126">Return Value</span></span>

<span data-ttu-id="36d22-127">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="36d22-127">**Type**: Boolean</span></span>

<span data-ttu-id="36d22-128">**Description**: true if enabled; false otherwise.</span><span class="sxs-lookup"><span data-stu-id="36d22-128">**Description**: true if enabled; false otherwise.</span></span>

## <a name="isrtl"></a><span data-ttu-id="36d22-129">isRTL</span><span class="sxs-lookup"><span data-stu-id="36d22-129">isRTL</span></span> 

<span data-ttu-id="36d22-130">Indicates whether the language for the current user is a right-to-left (RTL) language.</span><span class="sxs-lookup"><span data-stu-id="36d22-130">Indicates whether the language for the current user is a right-to-left (RTL) language.</span></span>

### <a name="syntax"></a><span data-ttu-id="36d22-131">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="36d22-131">Syntax</span></span>

`userSettings.isRTL`

### <a name="return-value"></a><span data-ttu-id="36d22-132">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="36d22-132">Return Value</span></span>

<span data-ttu-id="36d22-133">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="36d22-133">**Type**: Boolean</span></span>

<span data-ttu-id="36d22-134">**Description**: true if it is RTL; false otherwise.</span><span class="sxs-lookup"><span data-stu-id="36d22-134">**Description**: true if it is RTL; false otherwise.</span></span>

## <a name="languageid"></a><span data-ttu-id="36d22-135">languageId</span><span class="sxs-lookup"><span data-stu-id="36d22-135">languageId</span></span> 

<span data-ttu-id="36d22-136">Returns the language ID for the current user.</span><span class="sxs-lookup"><span data-stu-id="36d22-136">Returns the language ID for the current user.</span></span>

### <a name="syntax"></a><span data-ttu-id="36d22-137">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="36d22-137">Syntax</span></span>

`userSettings.languageId`

### <a name="return-value"></a><span data-ttu-id="36d22-138">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="36d22-138">Return Value</span></span>

<span data-ttu-id="36d22-139">**Type**: Number</span><span class="sxs-lookup"><span data-stu-id="36d22-139">**Type**: Number</span></span>

<span data-ttu-id="36d22-140">**Description**: Language ID.</span><span class="sxs-lookup"><span data-stu-id="36d22-140">**Description**: Language ID.</span></span>

## <a name="securityroleprivileges"></a><span data-ttu-id="36d22-141">securityRolePrivileges</span><span class="sxs-lookup"><span data-stu-id="36d22-141">securityRolePrivileges</span></span> 

<span data-ttu-id="36d22-142">Returns an array of strings that represent the GUID values of each of the security role privilege that the user is associated with or any teams that the user is associated with.</span><span class="sxs-lookup"><span data-stu-id="36d22-142">Returns an array of strings that represent the GUID values of each of the security role privilege that the user is associated with or any teams that the user is associated with.</span></span>

### <a name="syntax"></a><span data-ttu-id="36d22-143">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="36d22-143">Syntax</span></span>

`userSettings.securityRolePrivileges`

### <a name="return-value"></a><span data-ttu-id="36d22-144">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="36d22-144">Return Value</span></span>

<span data-ttu-id="36d22-145">**Type**: Array</span><span class="sxs-lookup"><span data-stu-id="36d22-145">**Type**: Array</span></span>

<span data-ttu-id="36d22-146">**Description**: GUID values of each of the security role privilege.</span><span class="sxs-lookup"><span data-stu-id="36d22-146">**Description**: GUID values of each of the security role privilege.</span></span>

## <a name="securityroles"></a><span data-ttu-id="36d22-147">securityRoles</span><span class="sxs-lookup"><span data-stu-id="36d22-147">securityRoles</span></span> 

<span data-ttu-id="36d22-148">Returns an array of strings that represent the GUID values of each of the security role that the user is associated with or any teams that the user is associated with.</span><span class="sxs-lookup"><span data-stu-id="36d22-148">Returns an array of strings that represent the GUID values of each of the security role that the user is associated with or any teams that the user is associated with.</span></span>

### <a name="syntax"></a><span data-ttu-id="36d22-149">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="36d22-149">Syntax</span></span>

`userSettings.securityRoles`

### <a name="return-value"></a><span data-ttu-id="36d22-150">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="36d22-150">Return Value</span></span>

<span data-ttu-id="36d22-151">**Type**: Array</span><span class="sxs-lookup"><span data-stu-id="36d22-151">**Type**: Array</span></span>

<span data-ttu-id="36d22-152">**Description**: GUID values of each of the security role.</span><span class="sxs-lookup"><span data-stu-id="36d22-152">**Description**: GUID values of each of the security role.</span></span> <span data-ttu-id="36d22-153">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="36d22-153">For example:</span></span>

`["0d3dd20a-17a6-e711-a94e-000d3a1a7a9b", "ff42d20a-17a6-e711-a94e-000d3a1a7a9b"]`

## <a name="transactioncurrencyid"></a><span data-ttu-id="36d22-154">transactionCurrencyId</span><span class="sxs-lookup"><span data-stu-id="36d22-154">transactionCurrencyId</span></span> 

<span data-ttu-id="36d22-155">Returns the transaction currency ID for the current user.</span><span class="sxs-lookup"><span data-stu-id="36d22-155">Returns the transaction currency ID for the current user.</span></span>

### <a name="syntax"></a><span data-ttu-id="36d22-156">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="36d22-156">Syntax</span></span>

`userSettings.transactionCurrencyId`

### <a name="return-value"></a><span data-ttu-id="36d22-157">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="36d22-157">Return Value</span></span>

<span data-ttu-id="36d22-158">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="36d22-158">**Type**: String</span></span>

<span data-ttu-id="36d22-159">**Description**: Transaction currency ID.</span><span class="sxs-lookup"><span data-stu-id="36d22-159">**Description**: Transaction currency ID.</span></span>

## <a name="userid"></a><span data-ttu-id="36d22-160">userId</span><span class="sxs-lookup"><span data-stu-id="36d22-160">userId</span></span> 

<span data-ttu-id="36d22-161">Returns the GUID of the **SystemUser.Id** value for the current user.</span><span class="sxs-lookup"><span data-stu-id="36d22-161">Returns the GUID of the **SystemUser.Id** value for the current user.</span></span>

### <a name="syntax"></a><span data-ttu-id="36d22-162">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="36d22-162">Syntax</span></span>

`userSettings.userId`

### <a name="return-value"></a><span data-ttu-id="36d22-163">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="36d22-163">Return Value</span></span>

<span data-ttu-id="36d22-164">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="36d22-164">**Type**: String</span></span>

<span data-ttu-id="36d22-165">**Description**: The ID of the user.</span><span class="sxs-lookup"><span data-stu-id="36d22-165">**Description**: The ID of the user.</span></span> <span data-ttu-id="36d22-166">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="36d22-166">For example:</span></span>

`"{75B5BA27-FD41-4D45-8E3A-C8446C95F0CC}"`

## <a name="username"></a><span data-ttu-id="36d22-167">userName</span><span class="sxs-lookup"><span data-stu-id="36d22-167">userName</span></span> 

<span data-ttu-id="36d22-168">Returns the name of the current user.</span><span class="sxs-lookup"><span data-stu-id="36d22-168">Returns the name of the current user.</span></span>

### <a name="syntax"></a><span data-ttu-id="36d22-169">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="36d22-169">Syntax</span></span>

`userSettings.userName`

### <a name="return-value"></a><span data-ttu-id="36d22-170">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="36d22-170">Return Value</span></span>

<span data-ttu-id="36d22-171">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="36d22-171">**Type**: String</span></span>

<span data-ttu-id="36d22-172">**Description**: Name of the current user.</span><span class="sxs-lookup"><span data-stu-id="36d22-172">**Description**: Name of the current user.</span></span>

## <a name="gettimezoneoffsetminutes-method"></a><span data-ttu-id="36d22-173">getTimeZoneOffsetMinutes method</span><span class="sxs-lookup"><span data-stu-id="36d22-173">getTimeZoneOffsetMinutes method</span></span>

<span data-ttu-id="36d22-174">Returns the difference in minutes between the local time and Coordinated Universal Time (UTC).</span><span class="sxs-lookup"><span data-stu-id="36d22-174">Returns the difference in minutes between the local time and Coordinated Universal Time (UTC).</span></span>

### <a name="syntax"></a><span data-ttu-id="36d22-175">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="36d22-175">Syntax</span></span>

`userSettings.getTimeZoneOffsetMinutes()`

### <a name="return-value"></a><span data-ttu-id="36d22-176">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="36d22-176">Return Value</span></span>

<span data-ttu-id="36d22-177">**Type**: number</span><span class="sxs-lookup"><span data-stu-id="36d22-177">**Type**: number</span></span>

<span data-ttu-id="36d22-178">**Description**: Time zone offset in minutes.</span><span class="sxs-lookup"><span data-stu-id="36d22-178">**Description**: Time zone offset in minutes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36d22-179">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="36d22-179">Related topics</span></span>

[<span data-ttu-id="36d22-180">Client context</span><span class="sxs-lookup"><span data-stu-id="36d22-180">Client context</span></span>](client.md)

[<span data-ttu-id="36d22-181">Organization settings</span><span class="sxs-lookup"><span data-stu-id="36d22-181">Organization settings</span></span>](organizationSettings.md)

[<span data-ttu-id="36d22-182">Xrm.Utility.getGlobalContext</span><span class="sxs-lookup"><span data-stu-id="36d22-182">Xrm.Utility.getGlobalContext</span></span>](../getGlobalContext.md)

