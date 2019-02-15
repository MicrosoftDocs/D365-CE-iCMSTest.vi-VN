---
title: Generate performance data log files Performance data collection using keyboard shortcuts | MicrosoftDocs
description: Learn about Unified Service Desk performance data collection to collect data about the operational events, errors, and performance in a client application and to create log files using keyboard shortcuts
keywords: ''
ms.date: 10/31/2018
ms.service:
- dynamics-365-customerservice
ms.custom:
- dyn365-a11y
- dyn365-USD, dyn365-admin
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: E838A9E7-4ED6-44DF-B2E9-0A3E3A82EA4B
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
monikerRange: '>= dynamics-usd-3'
ms.openlocfilehash: 0686c4e0fd646e3549fa336a57f247258ebbf24d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382413"
---
# <a name="generate-performance-data-logs-performance-data-collection"></a><span data-ttu-id="d7277-103">Generate performance data logs (Performance data collection)</span><span class="sxs-lookup"><span data-stu-id="d7277-103">Generate performance data logs (Performance data collection)</span></span>
<span data-ttu-id="d7277-104">Performance data collection enables you to collect data about operational events in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application to log files, which is used to identify and troubleshoot performance issues.</span><span class="sxs-lookup"><span data-stu-id="d7277-104">Performance data collection enables you to collect data about operational events in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application to log files, which is used to identify and troubleshoot performance issues.</span></span>

<span data-ttu-id="d7277-105">You can generate the performance data logs to:</span><span class="sxs-lookup"><span data-stu-id="d7277-105">You can generate the performance data logs to:</span></span>

- <span data-ttu-id="d7277-106">Analyze the end-to-end performance of Unified Service Desk from the time of client application booting.</span><span class="sxs-lookup"><span data-stu-id="d7277-106">Analyze the end-to-end performance of Unified Service Desk from the time of client application booting.</span></span> 
- <span data-ttu-id="d7277-107">Analyze the performance of operations that agents perform in the Unified Service Desk client application.</span><span class="sxs-lookup"><span data-stu-id="d7277-107">Analyze the performance of operations that agents perform in the Unified Service Desk client application.</span></span>

<span data-ttu-id="d7277-108">You can generate the performance data logs in two ways:</span><span class="sxs-lookup"><span data-stu-id="d7277-108">You can generate the performance data logs in two ways:</span></span>

- <span data-ttu-id="d7277-109">Using application configuration file (UnifiedServiceDesk.exe.config) to generate data log for the end-to-end client application, which includes booting through closing the client application.</span><span class="sxs-lookup"><span data-stu-id="d7277-109">Using application configuration file (UnifiedServiceDesk.exe.config) to generate data log for the end-to-end client application, which includes booting through closing the client application.</span></span>
- <span data-ttu-id="d7277-110">Using keyboard shortcuts to generate data log for operations.</span><span class="sxs-lookup"><span data-stu-id="d7277-110">Using keyboard shortcuts to generate data log for operations.</span></span>

> [!Note]
> <span data-ttu-id="d7277-111">If you encounter performance issues with [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], customer support may ask you to collect the performance data and send the log files to help troubleshoot the issue.</span><span class="sxs-lookup"><span data-stu-id="d7277-111">If you encounter performance issues with [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], customer support may ask you to collect the performance data and send the log files to help troubleshoot the issue.</span></span>

## <a name="use-application-configuration-file-unifiedservicedeskexeconfig-to-generate-performance-data-log"></a><span data-ttu-id="d7277-112">Use application configuration file (UnifiedServiceDesk.exe.config) to generate performance data log</span><span class="sxs-lookup"><span data-stu-id="d7277-112">Use application configuration file (UnifiedServiceDesk.exe.config) to generate performance data log</span></span>

<span data-ttu-id="d7277-113">Use the application configuration file (UnifiedServiceDesk.exe.config) to generate (collect) startup performance data log.</span><span class="sxs-lookup"><span data-stu-id="d7277-113">Use the application configuration file (UnifiedServiceDesk.exe.config) to generate (collect) startup performance data log.</span></span>

<span data-ttu-id="d7277-114">If you experience performance issues with boot of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], you can manually modify the application configuration file (UnifiedServiceDesk.exe.config) to start collecting the performance data to log files.</span><span class="sxs-lookup"><span data-stu-id="d7277-114">If you experience performance issues with boot of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], you can manually modify the application configuration file (UnifiedServiceDesk.exe.config) to start collecting the performance data to log files.</span></span>

<span data-ttu-id="d7277-115">To start collecting the startup performance data log, change the value in application configuration file from **Off** to **Verbose** in the XML node.</span><span class="sxs-lookup"><span data-stu-id="d7277-115">To start collecting the startup performance data log, change the value in application configuration file from **Off** to **Verbose** in the XML node.</span></span>

```<add name="Microsoft.Uii.Common.Performance" value="Verbose"/>```

[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="d7277-116">[Diagnostics Verbosity Level](../admin/configure-auditing-diagnostics-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="d7277-116">[Diagnostics Verbosity Level](../admin/configure-auditing-diagnostics-unified-service-desk.md)</span></span>

## <a name="use-keyboard-shortcut-to-generate-performance-data-log"></a><span data-ttu-id="d7277-117">Use keyboard shortcut to generate performance data log</span><span class="sxs-lookup"><span data-stu-id="d7277-117">Use keyboard shortcut to generate performance data log</span></span>

<span data-ttu-id="d7277-118">When you are working with the client application and want to analyze the performance of the operations that you execute, you need to generate the performance log from which you can generate a performance report specific those operations.</span><span class="sxs-lookup"><span data-stu-id="d7277-118">When you are working with the client application and want to analyze the performance of the operations that you execute, you need to generate the performance log from which you can generate a performance report specific those operations.</span></span>

### <a name="start-performance-data-collection-using-a-keyboard-shortcut"></a><span data-ttu-id="d7277-119">Start performance data collection using a keyboard shortcut</span><span class="sxs-lookup"><span data-stu-id="d7277-119">Start performance data collection using a keyboard shortcut</span></span>

1. <span data-ttu-id="d7277-120">Press **Ctrl+Alt+Q** or the configured keyboard shortcut to start collecting performance data.</span><span class="sxs-lookup"><span data-stu-id="d7277-120">Press **Ctrl+Alt+Q** or the configured keyboard shortcut to start collecting performance data.</span></span> 
   <span data-ttu-id="d7277-121">Unified Service Desk displays a window asking - **Do you want to start collecting performance data?**.</span><span class="sxs-lookup"><span data-stu-id="d7277-121">Unified Service Desk displays a window asking - **Do you want to start collecting performance data?**.</span></span>

   <span data-ttu-id="d7277-122">![Do you want to start collecting performance data](../../unified-service-desk/media/usd-keyboard-shortcut-start-collecting-perf-data.PNG "Do you want to start collecting performance data")</span><span class="sxs-lookup"><span data-stu-id="d7277-122">![Do you want to start collecting performance data](../../unified-service-desk/media/usd-keyboard-shortcut-start-collecting-perf-data.PNG "Do you want to start collecting performance data")</span></span>

   > [!Note]
   > <span data-ttu-id="d7277-123">When you press the keyboard shortcut and if [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] does not display the performance data collection starting window, then ensure the keyboard focus is not on the Internet Explorer Webpage.</span><span class="sxs-lookup"><span data-stu-id="d7277-123">When you press the keyboard shortcut and if [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] does not display the performance data collection starting window, then ensure the keyboard focus is not on the Internet Explorer Webpage.</span></span> <span data-ttu-id="d7277-124">Press **Alt+0** to bring the keyboard focus outside the Internet Explorer webpage, and then press the keyboard shortcut to start the performance data collection.</span><span class="sxs-lookup"><span data-stu-id="d7277-124">Press **Alt+0** to bring the keyboard focus outside the Internet Explorer webpage, and then press the keyboard shortcut to start the performance data collection.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="d7277-125">[Manage Options for Unified Service Desk](../../unified-service-desk/admin/manage-options-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="d7277-125">[Manage Options for Unified Service Desk](../../unified-service-desk/admin/manage-options-unified-service-desk.md)</span></span>

2. <span data-ttu-id="d7277-126">Click **Yes** to start collecting the performance data.</span><span class="sxs-lookup"><span data-stu-id="d7277-126">Click **Yes** to start collecting the performance data.</span></span>

> [!Note]
> <span data-ttu-id="d7277-127">If you press **Ctrl+Alt+Q** after you start collecting performance data for a session, Unified Service Desk displays a window with a message - **Performance data collection has already started. PerfSessionId - XXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="d7277-127">If you press **Ctrl+Alt+Q** after you start collecting performance data for a session, Unified Service Desk displays a window with a message - **Performance data collection has already started. PerfSessionId - XXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX**.</span></span>
> <span data-ttu-id="d7277-128">![Performance data collection already started](../../unified-service-desk/media/usd-keyboard-shortcut-already-started-collecting-perf-data.PNG "Performance data collection already started")</span><span class="sxs-lookup"><span data-stu-id="d7277-128">![Performance data collection already started](../../unified-service-desk/media/usd-keyboard-shortcut-already-started-collecting-perf-data.PNG "Performance data collection already started")</span></span>

### <a name="stop-performance-data-collection-using-keyboard-shortcut"></a><span data-ttu-id="d7277-129">Stop performance data collection using keyboard shortcut</span><span class="sxs-lookup"><span data-stu-id="d7277-129">Stop performance data collection using keyboard shortcut</span></span>

1. <span data-ttu-id="d7277-130">Press **Ctrl+Alt+P** or the configured keyboard shortcut to stop the collection of performance data.</span><span class="sxs-lookup"><span data-stu-id="d7277-130">Press **Ctrl+Alt+P** or the configured keyboard shortcut to stop the collection of performance data.</span></span></br>
   [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="d7277-131">displays a window with a message - **Do you want to stop collecting performance data? PerfSessionId - XXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="d7277-131">displays a window with a message - **Do you want to stop collecting performance data? PerfSessionId - XXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX**.</span></span>

   <span data-ttu-id="d7277-132">![Do you want to stop collecting performance data](../../unified-service-desk/media/usd-keyboard-shortcut-stop-collecting-perf-data.PNG "Do you want to stop collecting performance data")</span><span class="sxs-lookup"><span data-stu-id="d7277-132">![Do you want to stop collecting performance data](../../unified-service-desk/media/usd-keyboard-shortcut-stop-collecting-perf-data.PNG "Do you want to stop collecting performance data")</span></span>

2. <span data-ttu-id="d7277-133">Click **Yes** to stop collecting the performance data.</span><span class="sxs-lookup"><span data-stu-id="d7277-133">Click **Yes** to stop collecting the performance data.</span></span>

> [!Note]
> <span data-ttu-id="d7277-134">If you press **Ctrl+Alt+P** after you stop collecting performance data for a session, Unified Service Desk displays a window **Performance data collection has already stopped**.</span><span class="sxs-lookup"><span data-stu-id="d7277-134">If you press **Ctrl+Alt+P** after you stop collecting performance data for a session, Unified Service Desk displays a window **Performance data collection has already stopped**.</span></span>
> <span data-ttu-id="d7277-135">![Performance data collection already stopped](../../unified-service-desk/media/usd-keyboard-shortcut-already-stopped-collecting-perf-data.PNG "Performance data collection already stopped")</span><span class="sxs-lookup"><span data-stu-id="d7277-135">![Performance data collection already stopped](../../unified-service-desk/media/usd-keyboard-shortcut-already-stopped-collecting-perf-data.PNG "Performance data collection already stopped")</span></span>

## <a name="location-of-the-performance-data-file"></a><span data-ttu-id="d7277-136">Location of the performance data file</span><span class="sxs-lookup"><span data-stu-id="d7277-136">Location of the performance data file</span></span>

<span data-ttu-id="d7277-137">When you start collecting performance data, log files are generated with a unique performance session ID (GUID) on the client computer.</span><span class="sxs-lookup"><span data-stu-id="d7277-137">When you start collecting performance data, log files are generated with a unique performance session ID (GUID) on the client computer.</span></span>

<span data-ttu-id="d7277-138">The default path where the log files are maintained on the client computer:</span><span class="sxs-lookup"><span data-stu-id="d7277-138">The default path where the log files are maintained on the client computer:</span></span>

```%APPDATA%\Roaming\Microsoft\Microsoft Dynamics 365 for Customer Engagement Unified Service Desk\<version>\USDPerformanceData_<hhmmssfff>_<yyyy-mm-dd>```

<span data-ttu-id="d7277-139">You can change the default path of the log files from the application configuration file.</span><span class="sxs-lookup"><span data-stu-id="d7277-139">You can change the default path of the log files from the application configuration file.</span></span> <span data-ttu-id="d7277-140">In the XML node of the application configuration file, change the value of the following attributes.</span><span class="sxs-lookup"><span data-stu-id="d7277-140">In the XML node of the application configuration file, change the value of the following attributes.</span></span> 

|<span data-ttu-id="d7277-141">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="d7277-141">Attribute</span></span>|<span data-ttu-id="d7277-142">Giá trị Mặc định</span><span class="sxs-lookup"><span data-stu-id="d7277-142">Default Value</span></span>|<span data-ttu-id="d7277-143">New Value</span><span class="sxs-lookup"><span data-stu-id="d7277-143">New Value</span></span>|
|:------|:------|:------|
|<span data-ttu-id="d7277-144">**Location**</span><span class="sxs-lookup"><span data-stu-id="d7277-144">**Location**</span></span>|<span data-ttu-id="d7277-145">**LocalUserApplicationDirectory**</span><span class="sxs-lookup"><span data-stu-id="d7277-145">**LocalUserApplicationDirectory**</span></span>|<span data-ttu-id="d7277-146">**Tùy chỉnh**</span><span class="sxs-lookup"><span data-stu-id="d7277-146">**Custom**</span></span>|
|<span data-ttu-id="d7277-147">**CustomLocation**</span><span class="sxs-lookup"><span data-stu-id="d7277-147">**CustomLocation**</span></span>|**-**|<span data-ttu-id="d7277-148">**<\New folder path in client computer>**</span><span class="sxs-lookup"><span data-stu-id="d7277-148">**<\New folder path in client computer>**</span></span><br> <span data-ttu-id="d7277-149">Example: C:\UnifiedServiceDesk\Logs</span><span class="sxs-lookup"><span data-stu-id="d7277-149">Example: C:\UnifiedServiceDesk\Logs</span></span>|

<span data-ttu-id="d7277-150">Default XML node in the application configuration file:</span><span class="sxs-lookup"><span data-stu-id="d7277-150">Default XML node in the application configuration file:</span></span>

`<add name="RollingPerfTraceListener" type="Microsoft.Crm.UnifiedServiceDesk.Dynamics.Utilities.Performance.RollingPerfTraceListener, Microsoft.Crm.UnifiedServiceDesk.Dynamics" BaseFileName="USDPerformanceData" Location="LocalUserApplicationDirectory" MaxFileSize ="52428800" MaxFileCount="10"/>`

<span data-ttu-id="d7277-151">Example of setting new path in the application configuration file:</span><span class="sxs-lookup"><span data-stu-id="d7277-151">Example of setting new path in the application configuration file:</span></span>

`<add name="RollingPerfTraceListener" type="Microsoft.Uii.Common.Performance.RollingPerfTraceListener, Microsoft.Uii.Common" BaseFileName="USDPerformanceData" Location="Custom" CustomLocation="C:\UnifiedServiceDesk\Logs" MaxFileSize ="52428800" MaxFileCount="10"/>`

<span data-ttu-id="d7277-152">**MaxFileSize** is the maximum size (in bytes) of one performance log file that [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] maintains at the default or configured path in the client computer.</span><span class="sxs-lookup"><span data-stu-id="d7277-152">**MaxFileSize** is the maximum size (in bytes) of one performance log file that [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] maintains at the default or configured path in the client computer.</span></span> <span data-ttu-id="d7277-153">When the size of performance log file is equal to **MaxFileSize** value, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] generates a new file in the default or configured path and continues to collect the performance data.</span><span class="sxs-lookup"><span data-stu-id="d7277-153">When the size of performance log file is equal to **MaxFileSize** value, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] generates a new file in the default or configured path and continues to collect the performance data.</span></span>

<span data-ttu-id="d7277-154">Example: You configure **MaxFileSize="52000000"**.</span><span class="sxs-lookup"><span data-stu-id="d7277-154">Example: You configure **MaxFileSize="52000000"**.</span></span> <span data-ttu-id="d7277-155">When the size of performance log file is 52000000 bytes (52 MB), [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] generates a new performance log file in the default or configure path and continues to collect the performance data.</span><span class="sxs-lookup"><span data-stu-id="d7277-155">When the size of performance log file is 52000000 bytes (52 MB), [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] generates a new performance log file in the default or configure path and continues to collect the performance data.</span></span>

<span data-ttu-id="d7277-156">**MaxFileCount** is the count of files that [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] maintains at the default or configured path in client computer.</span><span class="sxs-lookup"><span data-stu-id="d7277-156">**MaxFileCount** is the count of files that [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] maintains at the default or configured path in client computer.</span></span> <span data-ttu-id="d7277-157">When the count of the performance log file is equal to **MaxFileCount** value, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] deletes the oldest performance log file to generate the new performance log file in the default or configured path.</span><span class="sxs-lookup"><span data-stu-id="d7277-157">When the count of the performance log file is equal to **MaxFileCount** value, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] deletes the oldest performance log file to generate the new performance log file in the default or configured path.</span></span>

<span data-ttu-id="d7277-158">Example: You configure **MaxFileCount="10"**.</span><span class="sxs-lookup"><span data-stu-id="d7277-158">Example: You configure **MaxFileCount="10"**.</span></span> [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="d7277-159">generates 10 performance log files in the default or configured path.</span><span class="sxs-lookup"><span data-stu-id="d7277-159">generates 10 performance log files in the default or configured path.</span></span> <span data-ttu-id="d7277-160">To generate a new performance log file, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] deletes the oldest performance log file and generates the new performance log file.</span><span class="sxs-lookup"><span data-stu-id="d7277-160">To generate a new performance log file, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] deletes the oldest performance log file and generates the new performance log file.</span></span> <span data-ttu-id="d7277-161">At all times, the count of performance log files cannot exceed the **MaxFileCount**.</span><span class="sxs-lookup"><span data-stu-id="d7277-161">At all times, the count of performance log files cannot exceed the **MaxFileCount**.</span></span>

> [!Note]
> <span data-ttu-id="d7277-162">Each time you start collecting performance data, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] creates a new file with a performance session ID, which it maintains on the client computer.</span><span class="sxs-lookup"><span data-stu-id="d7277-162">Each time you start collecting performance data, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] creates a new file with a performance session ID, which it maintains on the client computer.</span></span><br><br>

## <a name="configure-a-performance-data-collection-keyboard-shortcut"></a><span data-ttu-id="d7277-163">Configure a performance data collection keyboard shortcut</span><span class="sxs-lookup"><span data-stu-id="d7277-163">Configure a performance data collection keyboard shortcut</span></span>

<span data-ttu-id="d7277-164">An agent working on a client computer can start and stop collecting the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] performance data using keyboard shortcuts.</span><span class="sxs-lookup"><span data-stu-id="d7277-164">An agent working on a client computer can start and stop collecting the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] performance data using keyboard shortcuts.</span></span> <span data-ttu-id="d7277-165">By default, the keyboard shortcut to start performance data collection is **Ctrl+Alt+Q** and to stop performance data collection is **Ctrl+Alt+P**.</span><span class="sxs-lookup"><span data-stu-id="d7277-165">By default, the keyboard shortcut to start performance data collection is **Ctrl+Alt+Q** and to stop performance data collection is **Ctrl+Alt+P**.</span></span>

<span data-ttu-id="d7277-166">To change the default keyboard shortcut, a System Administrator needs to configure new keyboard shortcuts to start and stop collection of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] performance data.</span><span class="sxs-lookup"><span data-stu-id="d7277-166">To change the default keyboard shortcut, a System Administrator needs to configure new keyboard shortcuts to start and stop collection of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] performance data.</span></span>

<span data-ttu-id="d7277-167">To configure a new performance data collection keyboard shortcut:</span><span class="sxs-lookup"><span data-stu-id="d7277-167">To configure a new performance data collection keyboard shortcut:</span></span>

1. <span data-ttu-id="d7277-168">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="d7277-168">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]
 
3. <span data-ttu-id="d7277-169">Open the Audit & Diagnostics Setting record in the **Audit & Diagnostics Settings** section.</span><span class="sxs-lookup"><span data-stu-id="d7277-169">Open the Audit & Diagnostics Setting record in the **Audit & Diagnostics Settings** section.</span></span>
   > [!Note]
   > <span data-ttu-id="d7277-170">If there is no existing record, create a new Audit & Diagnostics Setting record.</span><span class="sxs-lookup"><span data-stu-id="d7277-170">If there is no existing record, create a new Audit & Diagnostics Setting record.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="d7277-171">[Create an Audit & Diagnostics record to use for diagnostics](../admin/configure-auditing-diagnostics-unified-service-desk.md).</span><span class="sxs-lookup"><span data-stu-id="d7277-171">[Create an Audit & Diagnostics record to use for diagnostics](../admin/configure-auditing-diagnostics-unified-service-desk.md).</span></span>

4. <span data-ttu-id="d7277-172">Expand the **Diagnostics Settings** area to see **Performance Data Collection**.</span><span class="sxs-lookup"><span data-stu-id="d7277-172">Expand the **Diagnostics Settings** area to see **Performance Data Collection**.</span></span>

5. <span data-ttu-id="d7277-173">Type the keyboard shortcut in the format _key1+key2+key3_ for the **On-Demand Begin Shortcut** field.</span><span class="sxs-lookup"><span data-stu-id="d7277-173">Type the keyboard shortcut in the format _key1+key2+key3_ for the **On-Demand Begin Shortcut** field.</span></span>

6. <span data-ttu-id="d7277-174">Type the keyboard shortcut in the format _key1+key2+key3_ for the **On-Demand End Shortcut** field.</span><span class="sxs-lookup"><span data-stu-id="d7277-174">Type the keyboard shortcut in the format _key1+key2+key3_ for the **On-Demand End Shortcut** field.</span></span>

7. <span data-ttu-id="d7277-175">Click **Save & Close**.</span><span class="sxs-lookup"><span data-stu-id="d7277-175">Click **Save & Close**.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="d7277-176">Generate performance report</span><span class="sxs-lookup"><span data-stu-id="d7277-176">Generate performance report</span></span>](generate-performance-report.md)

## <a name="see-also"></a><span data-ttu-id="d7277-177">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d7277-177">See also</span></span>

[<span data-ttu-id="d7277-178">Overview of Unified Service Desk Performance Analyzer</span><span class="sxs-lookup"><span data-stu-id="d7277-178">Overview of Unified Service Desk Performance Analyzer</span></span>](overview-performance-analyzer.md)

[<span data-ttu-id="d7277-179">Download Unified Service Desk Performance Analyzer</span><span class="sxs-lookup"><span data-stu-id="d7277-179">Download Unified Service Desk Performance Analyzer</span></span>](download-performance-analyzer.md)

[<span data-ttu-id="d7277-180">Overview of performance report user interface</span><span class="sxs-lookup"><span data-stu-id="d7277-180">Overview of performance report user interface</span></span>](overview-performance-report-user-interface.md)

[<span data-ttu-id="d7277-181">Configure auditing and diagnostics in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="d7277-181">Configure auditing and diagnostics in Unified Service Desk</span></span>](../admin/configure-auditing-diagnostics-unified-service-desk.md)

[<span data-ttu-id="d7277-182">Manage Options for Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="d7277-182">Manage Options for Unified Service Desk</span></span>](../../unified-service-desk/admin/manage-options-unified-service-desk.md)