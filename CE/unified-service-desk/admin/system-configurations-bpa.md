---
title: System configurations (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about the system configurations that best practices outlines and against which Best Practices Analyzer performs analysis.
ms.custom: ''
ms.date: 04/24/2018
ms.service: usd
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 2ED0C60D-0C69-45C7-828A-8BB7D05A9180
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 2eeb8f4a910ae413bf4bea5add90f5fd90e36bdb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382484"
---
# <a name="system-configurations"></a><span data-ttu-id="20140-103">System configurations</span><span class="sxs-lookup"><span data-stu-id="20140-103">System configurations</span></span>

<span data-ttu-id="20140-104">In the context of [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application, system configurations are categorized as the hardware and software requirements for the computer and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="20140-104">In the context of [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application, system configurations are categorized as the hardware and software requirements for the computer and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span>

## <a name="memory-ram"></a><span data-ttu-id="20140-105">Memory (RAM)</span><span class="sxs-lookup"><span data-stu-id="20140-105">Memory (RAM)</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="20140-106">checks memory on your computer and displays an error or warning when the value is less than 4 GB.</span><span class="sxs-lookup"><span data-stu-id="20140-106">checks memory on your computer and displays an error or warning when the value is less than 4 GB.</span></span> [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="20140-107">works best when memory (RAM) is 4 GB or more.</span><span class="sxs-lookup"><span data-stu-id="20140-107">works best when memory (RAM) is 4 GB or more.</span></span>

|              | <span data-ttu-id="20140-108">Lỗi</span><span class="sxs-lookup"><span data-stu-id="20140-108">Error</span></span>         | <span data-ttu-id="20140-109">Cảnh báo</span><span class="sxs-lookup"><span data-stu-id="20140-109">Warning</span></span>       |
|--------------|---------------|---------------|
| <span data-ttu-id="20140-110">Memory (RAM)</span><span class="sxs-lookup"><span data-stu-id="20140-110">Memory (RAM)</span></span> | <span data-ttu-id="20140-111">Less than 2 GB</span><span class="sxs-lookup"><span data-stu-id="20140-111">Less than 2 GB</span></span> | <span data-ttu-id="20140-112">Less than 4 GB</span><span class="sxs-lookup"><span data-stu-id="20140-112">Less than 4 GB</span></span> |

### <a name="mitigation"></a><span data-ttu-id="20140-113">Mitigation</span><span class="sxs-lookup"><span data-stu-id="20140-113">Mitigation</span></span>

<span data-ttu-id="20140-114">Upgrade the memory (RAM) of your computer to 4 GB or more.</span><span class="sxs-lookup"><span data-stu-id="20140-114">Upgrade the memory (RAM) of your computer to 4 GB or more.</span></span>

## <a name="available-memory-ram"></a><span data-ttu-id="20140-115">Available Memory (RAM)</span><span class="sxs-lookup"><span data-stu-id="20140-115">Available Memory (RAM)</span></span>

<span data-ttu-id="20140-116">**Available Memory** is the remaining memory (RAM) on your computer after memory consumed by the existing processes.</span><span class="sxs-lookup"><span data-stu-id="20140-116">**Available Memory** is the remaining memory (RAM) on your computer after memory consumed by the existing processes.</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="20140-117">checks available memory (RAM) on your computer and displays the warning when the value is less than 1 GB.</span><span class="sxs-lookup"><span data-stu-id="20140-117">checks available memory (RAM) on your computer and displays the warning when the value is less than 1 GB.</span></span> [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="20140-118">works best when **Available Memory (RAM)** is 4 GB or more.</span><span class="sxs-lookup"><span data-stu-id="20140-118">works best when **Available Memory (RAM)** is 4 GB or more.</span></span>

|              | <span data-ttu-id="20140-119">Cảnh báo</span><span class="sxs-lookup"><span data-stu-id="20140-119">Warning</span></span>       |
|--------------|---------------|
| <span data-ttu-id="20140-120">Memory (RAM)</span><span class="sxs-lookup"><span data-stu-id="20140-120">Memory (RAM)</span></span> | <span data-ttu-id="20140-121">Less than 1 GB</span><span class="sxs-lookup"><span data-stu-id="20140-121">Less than 1 GB</span></span> |

### <a name="mitigation"></a><span data-ttu-id="20140-122">Mitigation</span><span class="sxs-lookup"><span data-stu-id="20140-122">Mitigation</span></span>

<span data-ttu-id="20140-123">Close other processes to help ensure that **Available Memory (RAM)** is 1 GB or more.</span><span class="sxs-lookup"><span data-stu-id="20140-123">Close other processes to help ensure that **Available Memory (RAM)** is 1 GB or more.</span></span>

## <a name="operating-system-version"></a><span data-ttu-id="20140-124">Operating system version</span><span class="sxs-lookup"><span data-stu-id="20140-124">Operating system version</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="20140-125">checks the [!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)] operating system version on your computer.</span><span class="sxs-lookup"><span data-stu-id="20140-125">checks the [!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)] operating system version on your computer.</span></span> <span data-ttu-id="20140-126">If you use any version earlier than [!include[pn-windows-7](../../includes/pn-windows-7.md)], the [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] displays a warning.</span><span class="sxs-lookup"><span data-stu-id="20140-126">If you use any version earlier than [!include[pn-windows-7](../../includes/pn-windows-7.md)], the [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] displays a warning.</span></span>

<span data-ttu-id="20140-127">The supported operating system version is [!include[pn-windows-10](../../includes/pn-windows-10.md)], [!include[pn-windows-8-1](../../includes/pn-windows-8-1.md)], [!include[pn-windows8](../../includes/pn-windows8.md)], or [!include[pn-windows-7](../../includes/pn-windows-7.md)].</span><span class="sxs-lookup"><span data-stu-id="20140-127">The supported operating system version is [!include[pn-windows-10](../../includes/pn-windows-10.md)], [!include[pn-windows-8-1](../../includes/pn-windows-8-1.md)], [!include[pn-windows8](../../includes/pn-windows8.md)], or [!include[pn-windows-7](../../includes/pn-windows-7.md)].</span></span> <span data-ttu-id="20140-128">However, the recommended operating system is [!include[pn-windows-10](../../includes/pn-windows-10.md)].</span><span class="sxs-lookup"><span data-stu-id="20140-128">However, the recommended operating system is [!include[pn-windows-10](../../includes/pn-windows-10.md)].</span></span>

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="20140-129">works best with latest version of operating system.</span><span class="sxs-lookup"><span data-stu-id="20140-129">works best with latest version of operating system.</span></span>

### <a name="mitigation"></a><span data-ttu-id="20140-130">Mitigation</span><span class="sxs-lookup"><span data-stu-id="20140-130">Mitigation</span></span>

<span data-ttu-id="20140-131">Upgrade your computer to latest operating system version.</span><span class="sxs-lookup"><span data-stu-id="20140-131">Upgrade your computer to latest operating system version.</span></span>

## <a name="hard-disk-space"></a><span data-ttu-id="20140-132">Hard Disk Space</span><span class="sxs-lookup"><span data-stu-id="20140-132">Hard Disk Space</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="20140-133">checks the free hard disk space on your computer and displays a warning when the value is less than 12 GB.</span><span class="sxs-lookup"><span data-stu-id="20140-133">checks the free hard disk space on your computer and displays a warning when the value is less than 12 GB.</span></span> [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="20140-134">works best when hard disk space is 12 GB or more.</span><span class="sxs-lookup"><span data-stu-id="20140-134">works best when hard disk space is 12 GB or more.</span></span>

### <a name="mitigation"></a><span data-ttu-id="20140-135">Mitigation</span><span class="sxs-lookup"><span data-stu-id="20140-135">Mitigation</span></span>

<span data-ttu-id="20140-136">Delete old or unnecessary files to free space for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="20140-136">Delete old or unnecessary files to free space for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span>

## <a name="includepnunifiedservicedeskincludespn-unified-service-deskmd-version"></a><span data-ttu-id="20140-137">Phiên bản [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]</span><span class="sxs-lookup"><span data-stu-id="20140-137">[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] version</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="20140-138">checks for the version of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and recommends upgrading to the latest version of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to experience performance, reliability, and stability.</span><span class="sxs-lookup"><span data-stu-id="20140-138">checks for the version of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and recommends upgrading to the latest version of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to experience performance, reliability, and stability.</span></span>

### <a name="mitigation"></a><span data-ttu-id="20140-139">Mitigation</span><span class="sxs-lookup"><span data-stu-id="20140-139">Mitigation</span></span>

<span data-ttu-id="20140-140">Download and upgrade to the latest version of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="20140-140">Download and upgrade to the latest version of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="20140-141">[Download Unified Service Desk](../download-unified-service-desk.md) and [Upgrade the Unified Service Desk](../admin/install-upgrade-unified-service-desk-client.md)</span><span class="sxs-lookup"><span data-stu-id="20140-141">[Download Unified Service Desk](../download-unified-service-desk.md) and [Upgrade the Unified Service Desk](../admin/install-upgrade-unified-service-desk-client.md)</span></span>

## <a name="includepnunifiedservicedeskincludespn-unified-service-deskmd-up-time"></a>[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="20140-142">Up time</span><span class="sxs-lookup"><span data-stu-id="20140-142">Up time</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="20140-143">checks the active operational time of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and displays a warning when [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] is active for more than eight hours.</span><span class="sxs-lookup"><span data-stu-id="20140-143">checks the active operational time of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and displays a warning when [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] is active for more than eight hours.</span></span>

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="20140-144">works best when the you restart the client application after an active operational time of eight hours.</span><span class="sxs-lookup"><span data-stu-id="20140-144">works best when the you restart the client application after an active operational time of eight hours.</span></span>

### <a name="mitigation"></a><span data-ttu-id="20140-145">Mitigation</span><span class="sxs-lookup"><span data-stu-id="20140-145">Mitigation</span></span>

<span data-ttu-id="20140-146">To experience uninterrupted performance, we recommended that you restart [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] after an active time of eight hours.</span><span class="sxs-lookup"><span data-stu-id="20140-146">To experience uninterrupted performance, we recommended that you restart [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] after an active time of eight hours.</span></span>

## <a name="memory-by-includepnunifiedservicedeskincludespn-unified-service-deskmd-process"></a><span data-ttu-id="20140-147">Memory by [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] process</span><span class="sxs-lookup"><span data-stu-id="20140-147">Memory by [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] process</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="20140-148">checks for memory consumption by [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] processes and displays a warning when the value is more than 500 MB.</span><span class="sxs-lookup"><span data-stu-id="20140-148">checks for memory consumption by [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] processes and displays a warning when the value is more than 500 MB.</span></span>
<!--Editing: In the following paragraph, I spelled out IE, but it should probabaly be a token.-->
<span data-ttu-id="20140-149">The memory consumption of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] process increases when you host browser hosted controls in **Internal WPF** mode.</span><span class="sxs-lookup"><span data-stu-id="20140-149">The memory consumption of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] process increases when you host browser hosted controls in **Internal WPF** mode.</span></span> <span data-ttu-id="20140-150">Hosting browser hosted controls in **IE process** significantly reduces the memory footprint of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] process.</span><span class="sxs-lookup"><span data-stu-id="20140-150">Hosting browser hosted controls in **IE process** significantly reduces the memory footprint of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] process.</span></span>

<span data-ttu-id="20140-151">Therefore, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] works best when you use an **IE process** for hosting browser hosted controls.</span><span class="sxs-lookup"><span data-stu-id="20140-151">Therefore, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] works best when you use an **IE process** for hosting browser hosted controls.</span></span>

### <a name="mitigation"></a><span data-ttu-id="20140-152">Mitigation</span><span class="sxs-lookup"><span data-stu-id="20140-152">Mitigation</span></span>
<span data-ttu-id="20140-153"><!--Editing: Below, if "IE" isn't used in the UI in this case, please spell it out. Also, if "Internal" isn't part of the mode name, please lowercase that. --> Review and move any browser hosted controls in **Internal WPF** mode or hybrid mode (IE process and Internal WPF) to **IE process** mode.</span><span class="sxs-lookup"><span data-stu-id="20140-153"><!--Editing: Below, if "IE" isn't used in the UI in this case, please spell it out. Also, if "Internal" isn't part of the mode name, please lowercase that. --> Review and move any browser hosted controls in **Internal WPF** mode or hybrid mode (IE process and Internal WPF) to **IE process** mode.</span></span>

## <a name="includepn-ms-windows-shortincludespn-ms-windows-shortmd-kb-updates"></a>[!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)] <span data-ttu-id="20140-154">KB updates</span><span class="sxs-lookup"><span data-stu-id="20140-154">KB updates</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="20140-155">checks for the [!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)] KB3092627 update if your operating system is [!include[pn-windows-7](../../includes/pn-windows-7.md)] and displays a warning when the KB3092627 is not installed on your computer.</span><span class="sxs-lookup"><span data-stu-id="20140-155">checks for the [!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)] KB3092627 update if your operating system is [!include[pn-windows-7](../../includes/pn-windows-7.md)] and displays a warning when the KB3092627 is not installed on your computer.</span></span>

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="20140-156">works best when the [!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)] KB3092627 update is installed on your [!include[pn-windows-7](../../includes/pn-windows-7.md)].</span><span class="sxs-lookup"><span data-stu-id="20140-156">works best when the [!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)] KB3092627 update is installed on your [!include[pn-windows-7](../../includes/pn-windows-7.md)].</span></span>

### <a name="mitigation"></a><span data-ttu-id="20140-157">Mitigation</span><span class="sxs-lookup"><span data-stu-id="20140-157">Mitigation</span></span>

<span data-ttu-id="20140-158">Install the [!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)] KB3092627 update on your computer.</span><span class="sxs-lookup"><span data-stu-id="20140-158">Install the [!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)] KB3092627 update on your computer.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)]
<span data-ttu-id="20140-159">[KB3092627](https://support.microsoft.com/en-us/help/3092627/september-2015-update-to-fix-windows-or-application-freezes-after-you)</span><span class="sxs-lookup"><span data-stu-id="20140-159">[KB3092627](https://support.microsoft.com/en-us/help/3092627/september-2015-update-to-fix-windows-or-application-freezes-after-you)</span></span>

## <a name="see-also"></a><span data-ttu-id="20140-160">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="20140-160">See also</span></span>

[<span data-ttu-id="20140-161">Analyze best practices in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="20140-161">Analyze best practices in Unified Service Desk</span></span>](../admin/analyze-best-practices-unified-service-desk.md)

[<span data-ttu-id="20140-162">Download and install Best Practices Analyzer</span><span class="sxs-lookup"><span data-stu-id="20140-162">Download and install Best Practices Analyzer</span></span>](../admin/download-install-best-practices-analyzer.md)

[<span data-ttu-id="20140-163">Read Best Practices Analyzer report</span><span class="sxs-lookup"><span data-stu-id="20140-163">Read Best Practices Analyzer report</span></span>](../admin/read-best-practices-analyzer-report.md)

[<span data-ttu-id="20140-164">Best practice rule categories and parameters</span><span class="sxs-lookup"><span data-stu-id="20140-164">Best practice rule categories and parameters</span></span>](../admin/compliance-categories-parameters-bpa.md)

[<span data-ttu-id="20140-165">Internet Explorer settings</span><span class="sxs-lookup"><span data-stu-id="20140-165">Internet Explorer settings</span></span>](../admin/internet-explorer-settings-bpa.md)

[<span data-ttu-id="20140-166">Unified Service Desk configurations</span><span class="sxs-lookup"><span data-stu-id="20140-166">Unified Service Desk configurations</span></span>](../admin/unified-service-desk-configurations-bpa.md)
