---
title: Internet Explorer settings (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about the Internet Explorer settings that best practices outlines and against which Best Practices Analyzer performs analysis.
keywords: ''
ms.date: 05/07/2018
ms.service:
- usd
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 104DE14D-F43E-4414-AC83-5C1157E79831
author: kabala123
ms.author: kabala
manager: shujoshi
ms.openlocfilehash: d0209d4252dd12a7c7bd57c63dfb807b6e3f3f17
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382384"
---
# <a name="includepn-internet-explorerincludespn-internet-explorermd-settings"></a>[!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)] <span data-ttu-id="b8959-103">settings</span><span class="sxs-lookup"><span data-stu-id="b8959-103">settings</span></span>

<span data-ttu-id="b8959-104">In the context of [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] and the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application, certain parameters of [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)] settings are important for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to work seamlessly.</span><span class="sxs-lookup"><span data-stu-id="b8959-104">In the context of [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] and the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application, certain parameters of [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)] settings are important for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to work seamlessly.</span></span>

## <a name="tab-process-growth-tabprocgrowth"></a><span data-ttu-id="b8959-105">Tab Process Growth (TabProcGrowth)</span><span class="sxs-lookup"><span data-stu-id="b8959-105">Tab Process Growth (TabProcGrowth)</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="b8959-106">checks for the **TabProcGrowth** registry key and displays an error message when the value isn't set to **16**.</span><span class="sxs-lookup"><span data-stu-id="b8959-106">checks for the **TabProcGrowth** registry key and displays an error message when the value isn't set to **16**.</span></span>

<span data-ttu-id="b8959-107">Tab Process Growth is the rate at which [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)] creates new tab processes.</span><span class="sxs-lookup"><span data-stu-id="b8959-107">Tab Process Growth is the rate at which [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)] creates new tab processes.</span></span> [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="b8959-108">works best when the value is **16**.</span><span class="sxs-lookup"><span data-stu-id="b8959-108">works best when the value is **16**.</span></span>

### <a name="mitigation"></a><span data-ttu-id="b8959-109">Mitigation</span><span class="sxs-lookup"><span data-stu-id="b8959-109">Mitigation</span></span>

<span data-ttu-id="b8959-110">Set **TabProcGrowth** value to **16**:</span><span class="sxs-lookup"><span data-stu-id="b8959-110">Set **TabProcGrowth** value to **16**:</span></span>

1. <span data-ttu-id="b8959-111">Open **C:/** > **[!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)]** > **regedit**.</span><span class="sxs-lookup"><span data-stu-id="b8959-111">Open **C:/** > **[!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)]** > **regedit**.</span></span>
2. <span data-ttu-id="b8959-112">Go to **Computer**\\**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Internet Explorer**\\**Main**.</span><span class="sxs-lookup"><span data-stu-id="b8959-112">Go to **Computer**\\**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Internet Explorer**\\**Main**.</span></span>
3. <span data-ttu-id="b8959-113">Right-click **TabProcGrowth**, and then select **Modify**.</span><span class="sxs-lookup"><span data-stu-id="b8959-113">Right-click **TabProcGrowth**, and then select **Modify**.</span></span>
   > [!Note]
   > <span data-ttu-id="b8959-114">If the registry key isn't present, create it:</span><span class="sxs-lookup"><span data-stu-id="b8959-114">If the registry key isn't present, create it:</span></span><br>
   >      1. <span data-ttu-id="b8959-115">Right-click the blank area, and then select **New** > **DWORD (32-bit) Value**.</span><span class="sxs-lookup"><span data-stu-id="b8959-115">Right-click the blank area, and then select **New** > **DWORD (32-bit) Value**.</span></span> <span data-ttu-id="b8959-116">You can see new file.</span><span class="sxs-lookup"><span data-stu-id="b8959-116">You can see new file.</span></span><br>
   >      2. <span data-ttu-id="b8959-117">Type **TabProcGrowth** as the file name, and then select **Modify**.</span><span class="sxs-lookup"><span data-stu-id="b8959-117">Type **TabProcGrowth** as the file name, and then select **Modify**.</span></span>

4. <span data-ttu-id="b8959-118">In the **Value data** field, type **16**.</span><span class="sxs-lookup"><span data-stu-id="b8959-118">In the **Value data** field, type **16**.</span></span>
5. <span data-ttu-id="b8959-119">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8959-119">Select **OK**.</span></span>

## <a name="tab-shutdown-delay-tabshutdowndelay"></a><span data-ttu-id="b8959-120">Tab Shutdown Delay (TabShutdownDelay)</span><span class="sxs-lookup"><span data-stu-id="b8959-120">Tab Shutdown Delay (TabShutdownDelay)</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="b8959-121">checks for the **TabShutdownDelay** registry key and displays an error message when the key is enabled (value set to **0**).</span><span class="sxs-lookup"><span data-stu-id="b8959-121">checks for the **TabShutdownDelay** registry key and displays an error message when the key is enabled (value set to **0**).</span></span>

<span data-ttu-id="b8959-122">Tab Shutdown Delay causes the [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)] processes to terminate on demand.</span><span class="sxs-lookup"><span data-stu-id="b8959-122">Tab Shutdown Delay causes the [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)] processes to terminate on demand.</span></span> <span data-ttu-id="b8959-123">If the value isn't set to zero, Tab Shutdown Delay is enabled.</span><span class="sxs-lookup"><span data-stu-id="b8959-123">If the value isn't set to zero, Tab Shutdown Delay is enabled.</span></span> [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="b8959-124">works best when Tab Shutdown Delay is disabled (value set to **0**).</span><span class="sxs-lookup"><span data-stu-id="b8959-124">works best when Tab Shutdown Delay is disabled (value set to **0**).</span></span>

### <a name="mitigation"></a><span data-ttu-id="b8959-125">Mitigation</span><span class="sxs-lookup"><span data-stu-id="b8959-125">Mitigation</span></span>

<span data-ttu-id="b8959-126">Set **TabShutdownDelay** value to **0**:</span><span class="sxs-lookup"><span data-stu-id="b8959-126">Set **TabShutdownDelay** value to **0**:</span></span>

1. <span data-ttu-id="b8959-127">Open **C:/** > **[!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)]** > **regedit**.</span><span class="sxs-lookup"><span data-stu-id="b8959-127">Open **C:/** > **[!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)]** > **regedit**.</span></span>
2. <span data-ttu-id="b8959-128">Truy cập `Computer\HKEY\CURRENT\USER\Software\Microsoft\Internet Explorer\Main`.</span><span class="sxs-lookup"><span data-stu-id="b8959-128">Go to `Computer\HKEY\CURRENT\USER\Software\Microsoft\Internet Explorer\Main`.</span></span>
3. <span data-ttu-id="b8959-129">Right-click **TabShutdownDelay**, and then select **Modify**.</span><span class="sxs-lookup"><span data-stu-id="b8959-129">Right-click **TabShutdownDelay**, and then select **Modify**.</span></span>
   > [!NOTE]
   > <span data-ttu-id="b8959-130">If the registry key isn't present, create it:</span><span class="sxs-lookup"><span data-stu-id="b8959-130">If the registry key isn't present, create it:</span></span><br>
   >     1.  <span data-ttu-id="b8959-131">Right-click the blank area, and then select **New** > **DWORD (32-bit) Value**.</span><span class="sxs-lookup"><span data-stu-id="b8959-131">Right-click the blank area, and then select **New** > **DWORD (32-bit) Value**.</span></span> <span data-ttu-id="b8959-132">You can see new file.</span><span class="sxs-lookup"><span data-stu-id="b8959-132">You can see new file.</span></span><br>
   >     2.  <span data-ttu-id="b8959-133">Type **TabShutdownDelay** as the file name, and then select **Modify**.</span><span class="sxs-lookup"><span data-stu-id="b8959-133">Type **TabShutdownDelay** as the file name, and then select **Modify**.</span></span>

4. <span data-ttu-id="b8959-134">In the **Value data** field, type **0**.</span><span class="sxs-lookup"><span data-stu-id="b8959-134">In the **Value data** field, type **0**.</span></span>
5. <span data-ttu-id="b8959-135">In the **Base** group box, select **Decimal**.</span><span class="sxs-lookup"><span data-stu-id="b8959-135">In the **Base** group box, select **Decimal**.</span></span>
6. <span data-ttu-id="b8959-136">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8959-136">Select **OK**.</span></span>

## <a name="enable-enhanced-protected-mode"></a><span data-ttu-id="b8959-137">Enable Enhanced Protected Mode</span><span class="sxs-lookup"><span data-stu-id="b8959-137">Enable Enhanced Protected Mode</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="b8959-138">checks for Enable Enhanced Protected Mode by checking for the **Isolation** registry key and displays an error message when the key is enabled (value set to **PMEM**).</span><span class="sxs-lookup"><span data-stu-id="b8959-138">checks for Enable Enhanced Protected Mode by checking for the **Isolation** registry key and displays an error message when the key is enabled (value set to **PMEM**).</span></span>

<span data-ttu-id="b8959-139">Enable Enhanced Protected Mode is a security feature.</span><span class="sxs-lookup"><span data-stu-id="b8959-139">Enable Enhanced Protected Mode is a security feature.</span></span> <span data-ttu-id="b8959-140">When this feature is enabled, add-ons such as toolbars and extensions are loaded only if they're compatible with Enhanced Protected Mode.</span><span class="sxs-lookup"><span data-stu-id="b8959-140">When this feature is enabled, add-ons such as toolbars and extensions are loaded only if they're compatible with Enhanced Protected Mode.</span></span>

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="b8959-141">works best when Enable Enhanced Protected Mode is disabled (value set to **PMIL**).</span><span class="sxs-lookup"><span data-stu-id="b8959-141">works best when Enable Enhanced Protected Mode is disabled (value set to **PMIL**).</span></span>

### <a name="mitigation"></a><span data-ttu-id="b8959-142">Mitigation</span><span class="sxs-lookup"><span data-stu-id="b8959-142">Mitigation</span></span>

<span data-ttu-id="b8959-143">Disable **Enable Enhanced Protected Mode**.</span><span class="sxs-lookup"><span data-stu-id="b8959-143">Disable **Enable Enhanced Protected Mode**.</span></span>

<span data-ttu-id="b8959-144">You can disable the option using the Registry Editor or Internet options.</span><span class="sxs-lookup"><span data-stu-id="b8959-144">You can disable the option using the Registry Editor or Internet options.</span></span>

<span data-ttu-id="b8959-145">To disable **Enable Enhanced Protected Mode** using the Registry Editor:</span><span class="sxs-lookup"><span data-stu-id="b8959-145">To disable **Enable Enhanced Protected Mode** using the Registry Editor:</span></span>

1. <span data-ttu-id="b8959-146">Open **C:/** > **[!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)]** > **regedit**.</span><span class="sxs-lookup"><span data-stu-id="b8959-146">Open **C:/** > **[!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)]** > **regedit**.</span></span>
2. <span data-ttu-id="b8959-147">Go to `Computer\HKEY\CURRENT\USER\Software\Microsoft\Internet Explorer\Main`.</span><span class="sxs-lookup"><span data-stu-id="b8959-147">Go to `Computer\HKEY\CURRENT\USER\Software\Microsoft\Internet Explorer\Main`.</span></span>
3. <span data-ttu-id="b8959-148">Right-click **Isolation**, and then select **Modify**.</span><span class="sxs-lookup"><span data-stu-id="b8959-148">Right-click **Isolation**, and then select **Modify**.</span></span>
   > [!Note]
   > <span data-ttu-id="b8959-149">If the registry key isn't present, create it:</span><span class="sxs-lookup"><span data-stu-id="b8959-149">If the registry key isn't present, create it:</span></span><br>
   >     1.  <span data-ttu-id="b8959-150">Right-click the blank area, and then select **New** > **String Value**.</span><span class="sxs-lookup"><span data-stu-id="b8959-150">Right-click the blank area, and then select **New** > **String Value**.</span></span> <span data-ttu-id="b8959-151">You can a see new file.</span><span class="sxs-lookup"><span data-stu-id="b8959-151">You can a see new file.</span></span><br>
   >     2.  <span data-ttu-id="b8959-152">Type **Isolation** as the file name, and then select **Modify**.</span><span class="sxs-lookup"><span data-stu-id="b8959-152">Type **Isolation** as the file name, and then select **Modify**.</span></span>

4. <span data-ttu-id="b8959-153">In the **Value data** field, type **PMIL**.</span><span class="sxs-lookup"><span data-stu-id="b8959-153">In the **Value data** field, type **PMIL**.</span></span> 
5. <span data-ttu-id="b8959-154">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8959-154">Select **OK**.</span></span>

<span data-ttu-id="b8959-155">To disable the option using Internet options:</span><span class="sxs-lookup"><span data-stu-id="b8959-155">To disable the option using Internet options:</span></span>

1. <span data-ttu-id="b8959-156">Open **[!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)]**.</span><span class="sxs-lookup"><span data-stu-id="b8959-156">Open **[!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)]**.</span></span>
2. <span data-ttu-id="b8959-157">Select **Tools** > **Internet Options** > **Advanced** tab.</span><span class="sxs-lookup"><span data-stu-id="b8959-157">Select **Tools** > **Internet Options** > **Advanced** tab.</span></span>
3. <span data-ttu-id="b8959-158">In the **Security** section, clear the **Enable Enhanced Protected Mode** check box.</span><span class="sxs-lookup"><span data-stu-id="b8959-158">In the **Security** section, clear the **Enable Enhanced Protected Mode** check box.</span></span>
4. <span data-ttu-id="b8959-159">Select **Apply**, and then select **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8959-159">Select **Apply**, and then select **OK**.</span></span>

## <a name="enable-automatic-crash-recovery"></a><span data-ttu-id="b8959-160">Enable Automatic Crash Recovery</span><span class="sxs-lookup"><span data-stu-id="b8959-160">Enable Automatic Crash Recovery</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="b8959-161">checks for Enable Automatic Crash Recovery by checking for the **AutoRecover** registry key and displays an error message when the key is enabled (value set to 0).</span><span class="sxs-lookup"><span data-stu-id="b8959-161">checks for Enable Automatic Crash Recovery by checking for the **AutoRecover** registry key and displays an error message when the key is enabled (value set to 0).</span></span>

<span data-ttu-id="b8959-162">Enable Automatic Crash Recovery is a feature that allows you to restore your previous browsing session in the event of crash.</span><span class="sxs-lookup"><span data-stu-id="b8959-162">Enable Automatic Crash Recovery is a feature that allows you to restore your previous browsing session in the event of crash.</span></span>

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="b8959-163">works best when Enable Automatic Crash Recovery is disabled (value is set to **2**).</span><span class="sxs-lookup"><span data-stu-id="b8959-163">works best when Enable Automatic Crash Recovery is disabled (value is set to **2**).</span></span>

### <a name="mitigation"></a><span data-ttu-id="b8959-164">Mitigation</span><span class="sxs-lookup"><span data-stu-id="b8959-164">Mitigation</span></span>

<span data-ttu-id="b8959-165">Disable the **Enable Automatic Crash Recovery** option.</span><span class="sxs-lookup"><span data-stu-id="b8959-165">Disable the **Enable Automatic Crash Recovery** option.</span></span>

<span data-ttu-id="b8959-166">You can disable the option using the Registry Editor or Internet options.</span><span class="sxs-lookup"><span data-stu-id="b8959-166">You can disable the option using the Registry Editor or Internet options.</span></span>

<span data-ttu-id="b8959-167">To disable the option using the Registry Editor:</span><span class="sxs-lookup"><span data-stu-id="b8959-167">To disable the option using the Registry Editor:</span></span>

1. <span data-ttu-id="b8959-168">Open **C:/** > **[!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)]** > **regedit**.</span><span class="sxs-lookup"><span data-stu-id="b8959-168">Open **C:/** > **[!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)]** > **regedit**.</span></span>
2. <span data-ttu-id="b8959-169">Truy cập `Computer\HKEY\CURRENT\USER\Software\Microsoft\Internet Explorer\Recovery`.</span><span class="sxs-lookup"><span data-stu-id="b8959-169">Go to `Computer\HKEY\CURRENT\USER\Software\Microsoft\Internet Explorer\Recovery`.</span></span>
3. <span data-ttu-id="b8959-170">Right-click **AutoRecover**, and then select **Modify**.</span><span class="sxs-lookup"><span data-stu-id="b8959-170">Right-click **AutoRecover**, and then select **Modify**.</span></span>
   > [!Note]
   > <span data-ttu-id="b8959-171">If the registry key isn't present, create it:</span><span class="sxs-lookup"><span data-stu-id="b8959-171">If the registry key isn't present, create it:</span></span><br>
   >     1.  <span data-ttu-id="b8959-172">Right-click the blank area, and then select **New** > **String Value**.</span><span class="sxs-lookup"><span data-stu-id="b8959-172">Right-click the blank area, and then select **New** > **String Value**.</span></span> <span data-ttu-id="b8959-173">You can a see new file.</span><span class="sxs-lookup"><span data-stu-id="b8959-173">You can a see new file.</span></span><br>
   >     2.  <span data-ttu-id="b8959-174">Type **Isolation** as the file name, and then select **Modify**.</span><span class="sxs-lookup"><span data-stu-id="b8959-174">Type **Isolation** as the file name, and then select **Modify**.</span></span>

4. <span data-ttu-id="b8959-175">In the **Value data** field, type **2**.</span><span class="sxs-lookup"><span data-stu-id="b8959-175">In the **Value data** field, type **2**.</span></span>
5. <span data-ttu-id="b8959-176">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8959-176">Select **OK**.</span></span>

<span data-ttu-id="b8959-177">To disable the option using Internet options:</span><span class="sxs-lookup"><span data-stu-id="b8959-177">To disable the option using Internet options:</span></span>

1. <span data-ttu-id="b8959-178">Open [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)].</span><span class="sxs-lookup"><span data-stu-id="b8959-178">Open [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)].</span></span>
2. <span data-ttu-id="b8959-179">Select **Tools** > **Internet Options** > **Advanced** tab.</span><span class="sxs-lookup"><span data-stu-id="b8959-179">Select **Tools** > **Internet Options** > **Advanced** tab.</span></span>
3. <span data-ttu-id="b8959-180">In the **Browsing** section, clear the **Enable automatic crash recovery** check box.</span><span class="sxs-lookup"><span data-stu-id="b8959-180">In the **Browsing** section, clear the **Enable automatic crash recovery** check box.</span></span>
4. <span data-ttu-id="b8959-181">Select **Apply**, and then select **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8959-181">Select **Apply**, and then select **OK**.</span></span>

## <a name="enable-protected-mode"></a><span data-ttu-id="b8959-182">Enable Protected Mode</span><span class="sxs-lookup"><span data-stu-id="b8959-182">Enable Protected Mode</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="b8959-183">checks for Enable Protected Mode by checking for the **2500** registry key and displays an error message when the key is disabled (value set to **3**).</span><span class="sxs-lookup"><span data-stu-id="b8959-183">checks for Enable Protected Mode by checking for the **2500** registry key and displays an error message when the key is disabled (value set to **3**).</span></span>

<span data-ttu-id="b8959-184">Enable Protected Mode is a security feature where [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)] provides multiple layers of defense from untrustworthy access to the [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)] process.</span><span class="sxs-lookup"><span data-stu-id="b8959-184">Enable Protected Mode is a security feature where [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)] provides multiple layers of defense from untrustworthy access to the [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)] process.</span></span> [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="b8959-185">works best when Enable Protected Mode is enabled (value is set to **0**).</span><span class="sxs-lookup"><span data-stu-id="b8959-185">works best when Enable Protected Mode is enabled (value is set to **0**).</span></span>

### <a name="mitigation"></a><span data-ttu-id="b8959-186">Mitigation</span><span class="sxs-lookup"><span data-stu-id="b8959-186">Mitigation</span></span>

<span data-ttu-id="b8959-187">Enable the **Enable Protected Mode** option.</span><span class="sxs-lookup"><span data-stu-id="b8959-187">Enable the **Enable Protected Mode** option.</span></span>

<span data-ttu-id="b8959-188">You can enable the option using the Registry Editor or Internet options.</span><span class="sxs-lookup"><span data-stu-id="b8959-188">You can enable the option using the Registry Editor or Internet options.</span></span>

<span data-ttu-id="b8959-189">To enable the option using the Registry Editor:</span><span class="sxs-lookup"><span data-stu-id="b8959-189">To enable the option using the Registry Editor:</span></span>

1. <span data-ttu-id="b8959-190">Open **C:/** > **[!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)]** > **regedit**.</span><span class="sxs-lookup"><span data-stu-id="b8959-190">Open **C:/** > **[!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)]** > **regedit**.</span></span>
2. <span data-ttu-id="b8959-191">Truy cập `Computer\HKEY\CURRENT\USER\Software\Microsoft\Windows\CurrentVersion\Internet Settings\Zones\\\<numerically named key folder>`.</span><span class="sxs-lookup"><span data-stu-id="b8959-191">Go to `Computer\HKEY\CURRENT\USER\Software\Microsoft\Windows\CurrentVersion\Internet Settings\Zones\\\<numerically named key folder>`.</span></span> <br>
   <span data-ttu-id="b8959-192">Numerically named folders are as follows:</span><span class="sxs-lookup"><span data-stu-id="b8959-192">Numerically named folders are as follows:</span></span><br>
   - <span data-ttu-id="b8959-193">1 (Intranet zone)</span><span class="sxs-lookup"><span data-stu-id="b8959-193">1 (Intranet zone)</span></span>
   - <span data-ttu-id="b8959-194">2 (Trusted Sites zone)</span><span class="sxs-lookup"><span data-stu-id="b8959-194">2 (Trusted Sites zone)</span></span>
   - <span data-ttu-id="b8959-195">3 (Internet zone)</span><span class="sxs-lookup"><span data-stu-id="b8959-195">3 (Internet zone)</span></span>
   - <span data-ttu-id="b8959-196">4 (Restricted Sites zone)</span><span class="sxs-lookup"><span data-stu-id="b8959-196">4 (Restricted Sites zone)</span></span>
3. <span data-ttu-id="b8959-197">Right-click the **2500** file, and then select **Modify**.</span><span class="sxs-lookup"><span data-stu-id="b8959-197">Right-click the **2500** file, and then select **Modify**.</span></span>
   > [!Note]
   > <span data-ttu-id="b8959-198">If the registry key isn't present, create it:</span><span class="sxs-lookup"><span data-stu-id="b8959-198">If the registry key isn't present, create it:</span></span><br>
   >     1. <span data-ttu-id="b8959-199">Right-click the blank area, and then select **New** > **DWORD (32-bit) Value**.</span><span class="sxs-lookup"><span data-stu-id="b8959-199">Right-click the blank area, and then select **New** > **DWORD (32-bit) Value**.</span></span> <span data-ttu-id="b8959-200">You can a see new file.</span><span class="sxs-lookup"><span data-stu-id="b8959-200">You can a see new file.</span></span> <br>
   >     2. <span data-ttu-id="b8959-201">Type **2500** as the file name, and then select **Modify**.</span><span class="sxs-lookup"><span data-stu-id="b8959-201">Type **2500** as the file name, and then select **Modify**.</span></span>

4. <span data-ttu-id="b8959-202">In the **Value data** field, type **0**.</span><span class="sxs-lookup"><span data-stu-id="b8959-202">In the **Value data** field, type **0**.</span></span>
5. <span data-ttu-id="b8959-203">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8959-203">Select **OK**.</span></span>

<span data-ttu-id="b8959-204">To enable the option using Internet options:</span><span class="sxs-lookup"><span data-stu-id="b8959-204">To enable the option using Internet options:</span></span>

1. <span data-ttu-id="b8959-205">Open **[!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)]**.</span><span class="sxs-lookup"><span data-stu-id="b8959-205">Open **[!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)]**.</span></span>
2. <span data-ttu-id="b8959-206">Select **Tools** > **Internet Options** > **Security** tab.</span><span class="sxs-lookup"><span data-stu-id="b8959-206">Select **Tools** > **Internet Options** > **Security** tab.</span></span>
3. <span data-ttu-id="b8959-207">Select a zone to change the security settings.</span><span class="sxs-lookup"><span data-stu-id="b8959-207">Select a zone to change the security settings.</span></span> <br><span data-ttu-id="b8959-208">Following are the zones:</span><span class="sxs-lookup"><span data-stu-id="b8959-208">Following are the zones:</span></span><br>
    -   <span data-ttu-id="b8959-209">Internet</span><span class="sxs-lookup"><span data-stu-id="b8959-209">Internet</span></span>
    -   <span data-ttu-id="b8959-210">Local intranet</span><span class="sxs-lookup"><span data-stu-id="b8959-210">Local intranet</span></span>
    -   <span data-ttu-id="b8959-211">Trusted sites</span><span class="sxs-lookup"><span data-stu-id="b8959-211">Trusted sites</span></span>
    -   <span data-ttu-id="b8959-212">Restricted sites</span><span class="sxs-lookup"><span data-stu-id="b8959-212">Restricted sites</span></span>
4. <span data-ttu-id="b8959-213">Select the **Enable Protected Mode** check box for the all the zones.</span><span class="sxs-lookup"><span data-stu-id="b8959-213">Select the **Enable Protected Mode** check box for the all the zones.</span></span>
5. <span data-ttu-id="b8959-214">Select **Apply**, and then select **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8959-214">Select **Apply**, and then select **OK**.</span></span>

> [!TIP]
> <span data-ttu-id="b8959-215">An alternative mitigation is retaining the default settings in the **Security** zones, and adding the Dynamics 365 for Customer Engagement apps instance and authentication URLs to the **Trusted sites**.</span><span class="sxs-lookup"><span data-stu-id="b8959-215">An alternative mitigation is retaining the default settings in the **Security** zones, and adding the Dynamics 365 for Customer Engagement apps instance and authentication URLs to the **Trusted sites**.</span></span> <span data-ttu-id="b8959-216">For more information, see the [blog](https://blogs.msdn.microsoft.com/usd/2016/01/26/ie-process-mode-gives-httpevent-popup/).</span><span class="sxs-lookup"><span data-stu-id="b8959-216">For more information, see the [blog](https://blogs.msdn.microsoft.com/usd/2016/01/26/ie-process-mode-gives-httpevent-popup/).</span></span>

## <a name="cleanup-htcs"></a><span data-ttu-id="b8959-217">Cleanup HTCs</span><span class="sxs-lookup"><span data-stu-id="b8959-217">Cleanup HTCs</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="b8959-218">checks for the **Cleanup HTCs** registry key and displays an error message when the key is disabled (value set to **No**).</span><span class="sxs-lookup"><span data-stu-id="b8959-218">checks for the **Cleanup HTCs** registry key and displays an error message when the key is disabled (value set to **No**).</span></span>

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="b8959-219">works best when the **Cleanup HTCs** option is set to **Yes**.</span><span class="sxs-lookup"><span data-stu-id="b8959-219">works best when the **Cleanup HTCs** option is set to **Yes**.</span></span>

### <a name="mitigation"></a><span data-ttu-id="b8959-220">Mitigation</span><span class="sxs-lookup"><span data-stu-id="b8959-220">Mitigation</span></span>

<span data-ttu-id="b8959-221">Set the **Cleanup HTCs** option to **Yes**:</span><span class="sxs-lookup"><span data-stu-id="b8959-221">Set the **Cleanup HTCs** option to **Yes**:</span></span>

1. <span data-ttu-id="b8959-222">Go to **C:/** > **[!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)]** > **regedit**</span><span class="sxs-lookup"><span data-stu-id="b8959-222">Go to **C:/** > **[!include[pn-ms-windows-short](../../includes/pn-ms-windows-short.md)]** > **regedit**</span></span>
2. <span data-ttu-id="b8959-223">Double-click to open **regedit**.</span><span class="sxs-lookup"><span data-stu-id="b8959-223">Double-click to open **regedit**.</span></span>
3. <span data-ttu-id="b8959-224">Truy cập `Computer\HKEY\CURRENT\USER\Software\Microsoft\Internet Explorer`.</span><span class="sxs-lookup"><span data-stu-id="b8959-224">Go to `Computer\HKEY\CURRENT\USER\Software\Microsoft\Internet Explorer`.</span></span>
4. <span data-ttu-id="b8959-225">Right-click **Cleanup HTCs**, and then select **Modify**.</span><span class="sxs-lookup"><span data-stu-id="b8959-225">Right-click **Cleanup HTCs**, and then select **Modify**.</span></span>
5. <span data-ttu-id="b8959-226">In the **Value data** field, select **Yes**.</span><span class="sxs-lookup"><span data-stu-id="b8959-226">In the **Value data** field, select **Yes**.</span></span>
6. <span data-ttu-id="b8959-227">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8959-227">Select **OK**.</span></span>

## <a name="includepn-internet-explorerincludespn-internet-explorermd-version"></a><span data-ttu-id="b8959-228">Phiên bản [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)]</span><span class="sxs-lookup"><span data-stu-id="b8959-228">[!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)] version</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="b8959-229">checks for the [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)] version and recommends using the latest version of [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)].</span><span class="sxs-lookup"><span data-stu-id="b8959-229">checks for the [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)] version and recommends using the latest version of [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)].</span></span>

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="b8959-230">works best with the latest version of [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)] 11.</span><span class="sxs-lookup"><span data-stu-id="b8959-230">works best with the latest version of [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)] 11.</span></span> <span data-ttu-id="b8959-231">If you are running [!include[pn-windows-8-1](../../includes/pn-windows-8-1.md)] or [!include[pn-windows-10](../../includes/pn-windows-10.md)], you already have [!include[pn-ie-11](../../includes/pn-ie-11.md)].</span><span class="sxs-lookup"><span data-stu-id="b8959-231">If you are running [!include[pn-windows-8-1](../../includes/pn-windows-8-1.md)] or [!include[pn-windows-10](../../includes/pn-windows-10.md)], you already have [!include[pn-ie-11](../../includes/pn-ie-11.md)].</span></span>

### <a name="mitigation"></a><span data-ttu-id="b8959-232">Mitigation</span><span class="sxs-lookup"><span data-stu-id="b8959-232">Mitigation</span></span>

<span data-ttu-id="b8959-233">Use the latest version of [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)].</span><span class="sxs-lookup"><span data-stu-id="b8959-233">Use the latest version of [!include[pn-internet-explorer](../../includes/pn-internet-explorer.md)].</span></span>

<span data-ttu-id="b8959-234">If you're running [!include[pn-windows-7](../../includes/pn-windows-7.md)] or earlier, download [!include[pn-ie-11](../../includes/pn-ie-11.md)].</span><span class="sxs-lookup"><span data-stu-id="b8959-234">If you're running [!include[pn-windows-7](../../includes/pn-windows-7.md)] or earlier, download [!include[pn-ie-11](../../includes/pn-ie-11.md)].</span></span>

[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="b8959-235">[Internet Explorer Downloads](https://support.microsoft.com/en-us/help/17621/internet-explorer-downloads)</span><span class="sxs-lookup"><span data-stu-id="b8959-235">[Internet Explorer Downloads](https://support.microsoft.com/en-us/help/17621/internet-explorer-downloads)</span></span>

## <a name="see-also"></a><span data-ttu-id="b8959-236">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b8959-236">See also</span></span>

[<span data-ttu-id="b8959-237">Analyze best practices in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="b8959-237">Analyze best practices in Unified Service Desk</span></span>](../admin/analyze-best-practices-unified-service-desk.md)

[<span data-ttu-id="b8959-238">Download and install Best Practices Analyzer</span><span class="sxs-lookup"><span data-stu-id="b8959-238">Download and install Best Practices Analyzer</span></span>](../admin/download-install-best-practices-analyzer.md)

[<span data-ttu-id="b8959-239">Read Best Practices Analyzer report</span><span class="sxs-lookup"><span data-stu-id="b8959-239">Read Best Practices Analyzer report</span></span>](../admin/read-best-practices-analyzer-report.md)

[<span data-ttu-id="b8959-240">Best practice rule categories and parameters</span><span class="sxs-lookup"><span data-stu-id="b8959-240">Best practice rule categories and parameters</span></span>](../admin/compliance-categories-parameters-bpa.md)

[<span data-ttu-id="b8959-241">System configurations</span><span class="sxs-lookup"><span data-stu-id="b8959-241">System configurations</span></span>](../admin/system-configurations-bpa.md)

[<span data-ttu-id="b8959-242">Unified Service Desk configurations</span><span class="sxs-lookup"><span data-stu-id="b8959-242">Unified Service Desk configurations</span></span>](../admin/unified-service-desk-configurations-bpa.md)
