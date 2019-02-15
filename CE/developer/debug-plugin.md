---
title: Debug a plug-In (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about debuggin a plug-in by logging and tracing.
keywords: ''
ms.date: 01/19/2018
ms.service: crm-online
ms.custom: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: b4bbe405-a56f-450b-acd9-0c063cf35990
author: JimDaly
ms.author: jdaly
manager: amyla
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 60
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9a0f324a161522c9ee02b2928157f6ca61d40401
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387550"
---
# <a name="debug-a-plug-in"></a><span data-ttu-id="d5b47-103">Debug a plug-In</span><span class="sxs-lookup"><span data-stu-id="d5b47-103">Debug a plug-In</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="d5b47-104">The following steps describe how to debug a plug-in executing on [!INCLUDE[pn_crm_op_edition](../includes/pn-crm-onprem.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="d5b47-104">The following steps describe how to debug a plug-in executing on [!INCLUDE[pn_crm_op_edition](../includes/pn-crm-onprem.md)] apps.</span></span> <span data-ttu-id="d5b47-105">To debug a plug-in that executes in the sandbox on [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps, you must be using tracing as described later in this topic.</span><span class="sxs-lookup"><span data-stu-id="d5b47-105">To debug a plug-in that executes in the sandbox on [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps, you must be using tracing as described later in this topic.</span></span>  
  
[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)]
<a name="bkmk_debugaplugin"></a>   
## <a name="debug-a-plug-in"></a><span data-ttu-id="d5b47-106">Gỡ lỗi phần bổ trợ</span><span class="sxs-lookup"><span data-stu-id="d5b47-106">Debug a plug-in</span></span>  
  
1. <span data-ttu-id="d5b47-107">Register and deploy the plug-in assembly.</span><span class="sxs-lookup"><span data-stu-id="d5b47-107">Register and deploy the plug-in assembly.</span></span>  
  
    <span data-ttu-id="d5b47-108">If there is another copy of the assembly at the same location and you cannot overwrite that copy because it is locked by [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps, you must restart the service process that was executing the plug-in.</span><span class="sxs-lookup"><span data-stu-id="d5b47-108">If there is another copy of the assembly at the same location and you cannot overwrite that copy because it is locked by [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps, you must restart the service process that was executing the plug-in.</span></span> <span data-ttu-id="d5b47-109">Refer to the table below for the correct service process.</span><span class="sxs-lookup"><span data-stu-id="d5b47-109">Refer to the table below for the correct service process.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="d5b47-110">[Register and Deploy Plug-ins](register-deploy-plugins.md)</span><span class="sxs-lookup"><span data-stu-id="d5b47-110">[Register and Deploy Plug-ins](register-deploy-plugins.md)</span></span>  
  
2. <span data-ttu-id="d5b47-111">Configure the debugger.</span><span class="sxs-lookup"><span data-stu-id="d5b47-111">Configure the debugger.</span></span>  
  
    <span data-ttu-id="d5b47-112">Attach the debugger to the process on the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps server that will run your plug-in.</span><span class="sxs-lookup"><span data-stu-id="d5b47-112">Attach the debugger to the process on the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps server that will run your plug-in.</span></span> <span data-ttu-id="d5b47-113">Refer to the following table to identify the process.</span><span class="sxs-lookup"><span data-stu-id="d5b47-113">Refer to the following table to identify the process.</span></span>  
  
   |<span data-ttu-id="d5b47-114">Plug-in Registration Configuration</span><span class="sxs-lookup"><span data-stu-id="d5b47-114">Plug-in Registration Configuration</span></span>|<span data-ttu-id="d5b47-115">Service Process</span><span class="sxs-lookup"><span data-stu-id="d5b47-115">Service Process</span></span>|  
   |-----------------------------------------|---------------------|  
   |<span data-ttu-id="d5b47-116">trực tuyến</span><span class="sxs-lookup"><span data-stu-id="d5b47-116">online</span></span>|<span data-ttu-id="d5b47-117">w3wp.exe</span><span class="sxs-lookup"><span data-stu-id="d5b47-117">w3wp.exe</span></span>|  
   |<span data-ttu-id="d5b47-118">offline</span><span class="sxs-lookup"><span data-stu-id="d5b47-118">offline</span></span>|<span data-ttu-id="d5b47-119">Microsoft.Crm.Application.Hoster.exe</span><span class="sxs-lookup"><span data-stu-id="d5b47-119">Microsoft.Crm.Application.Hoster.exe</span></span>|  
   |<span data-ttu-id="d5b47-120">asynchronous registered plug-ins (or custom workflow assemblies)</span><span class="sxs-lookup"><span data-stu-id="d5b47-120">asynchronous registered plug-ins (or custom workflow assemblies)</span></span>|<span data-ttu-id="d5b47-121">CrmAsyncService.exe</span><span class="sxs-lookup"><span data-stu-id="d5b47-121">CrmAsyncService.exe</span></span>|  
   |<span data-ttu-id="d5b47-122">sandbox (isolation mode)</span><span class="sxs-lookup"><span data-stu-id="d5b47-122">sandbox (isolation mode)</span></span>|<span data-ttu-id="d5b47-123">Microsoft.Crm.Sandbox.WorkerProcess.exe</span><span class="sxs-lookup"><span data-stu-id="d5b47-123">Microsoft.Crm.Sandbox.WorkerProcess.exe</span></span>|  
  
    <span data-ttu-id="d5b47-124">If there are multiple processes running the same executable file, for example multiple w3wp.exe processes, attach the debugger to all instances of the running executable process.</span><span class="sxs-lookup"><span data-stu-id="d5b47-124">If there are multiple processes running the same executable file, for example multiple w3wp.exe processes, attach the debugger to all instances of the running executable process.</span></span> <span data-ttu-id="d5b47-125">Next, set one or more breakpoints in your plug-in code.</span><span class="sxs-lookup"><span data-stu-id="d5b47-125">Next, set one or more breakpoints in your plug-in code.</span></span>  
  
3. <span data-ttu-id="d5b47-126">Test the plug-in.</span><span class="sxs-lookup"><span data-stu-id="d5b47-126">Test the plug-in.</span></span>  
  
    <span data-ttu-id="d5b47-127">Run the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] application, or other custom application that uses the SDK, and perform whatever action is required to cause the plug-in to execute.</span><span class="sxs-lookup"><span data-stu-id="d5b47-127">Run the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] application, or other custom application that uses the SDK, and perform whatever action is required to cause the plug-in to execute.</span></span> <span data-ttu-id="d5b47-128">For example, if a plug-in is registered for an account creation event, create a new account.</span><span class="sxs-lookup"><span data-stu-id="d5b47-128">For example, if a plug-in is registered for an account creation event, create a new account.</span></span>  
  
4. <span data-ttu-id="d5b47-129">Debug your plug-in code.</span><span class="sxs-lookup"><span data-stu-id="d5b47-129">Debug your plug-in code.</span></span>  
  
    <span data-ttu-id="d5b47-130">Make any needed changes to your code so that it performs as you want.</span><span class="sxs-lookup"><span data-stu-id="d5b47-130">Make any needed changes to your code so that it performs as you want.</span></span> <span data-ttu-id="d5b47-131">If the code is changed, compile the code into an assembly and repeat steps 1 through 4 in this procedure as necessary.</span><span class="sxs-lookup"><span data-stu-id="d5b47-131">If the code is changed, compile the code into an assembly and repeat steps 1 through 4 in this procedure as necessary.</span></span> <span data-ttu-id="d5b47-132">However, if you change the plug-in assembly’s major or minor version numbers, you must unregister the earlier version of the assembly and register the new version.</span><span class="sxs-lookup"><span data-stu-id="d5b47-132">However, if you change the plug-in assembly’s major or minor version numbers, you must unregister the earlier version of the assembly and register the new version.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="d5b47-133">[Register and Deploy Plug-ins](register-deploy-plugins.md)</span><span class="sxs-lookup"><span data-stu-id="d5b47-133">[Register and Deploy Plug-ins](register-deploy-plugins.md)</span></span>  
  
5. <span data-ttu-id="d5b47-134">Register the plug-in in the database.</span><span class="sxs-lookup"><span data-stu-id="d5b47-134">Register the plug-in in the database.</span></span>  
  
    <span data-ttu-id="d5b47-135">After the edit/compile/deploy/test/debug cycle for your plug-in has been completed, unregister the (on-disk) plug-in assembly and then reregister the plug-in in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps database.</span><span class="sxs-lookup"><span data-stu-id="d5b47-135">After the edit/compile/deploy/test/debug cycle for your plug-in has been completed, unregister the (on-disk) plug-in assembly and then reregister the plug-in in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps database.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="d5b47-136">[Register and Deploy Plug-ins](register-deploy-plugins.md)</span><span class="sxs-lookup"><span data-stu-id="d5b47-136">[Register and Deploy Plug-ins](register-deploy-plugins.md)</span></span>  
  
> [!TIP]
>  <span data-ttu-id="d5b47-137">It is possible to debug a database deployed plug-in.</span><span class="sxs-lookup"><span data-stu-id="d5b47-137">It is possible to debug a database deployed plug-in.</span></span> <span data-ttu-id="d5b47-138">The compiled plug-in assembly's symbol file (.pdb) must be copied to the server's \<*crm-root*>\Server\bin\assembly folder and [!INCLUDE[pn_Internet_Information_Services](../includes/pn-internet-information-services.md)] must then be restarted.</span><span class="sxs-lookup"><span data-stu-id="d5b47-138">The compiled plug-in assembly's symbol file (.pdb) must be copied to the server's \<*crm-root*>\Server\bin\assembly folder and [!INCLUDE[pn_Internet_Information_Services](../includes/pn-internet-information-services.md)] must then be restarted.</span></span> <span data-ttu-id="d5b47-139">After debugging has been completed, you must remove the symbol file and reset IIS to prevent the process that was executing the plug-in from consuming additional memory.</span><span class="sxs-lookup"><span data-stu-id="d5b47-139">After debugging has been completed, you must remove the symbol file and reset IIS to prevent the process that was executing the plug-in from consuming additional memory.</span></span>  
  
 <span data-ttu-id="d5b47-140">For more information about debugging a plug-in using the Plug-in Profiler tool, see [Analyze Plug-in Performance](analyze-plugin-performance.md).</span><span class="sxs-lookup"><span data-stu-id="d5b47-140">For more information about debugging a plug-in using the Plug-in Profiler tool, see [Analyze Plug-in Performance](analyze-plugin-performance.md).</span></span>  
  
<a name="bkmk_sandboxplugin"></a>   
## <a name="debug-a-sandboxed-plug-in"></a><span data-ttu-id="d5b47-141">Debug a sandboxed plug-in</span><span class="sxs-lookup"><span data-stu-id="d5b47-141">Debug a sandboxed plug-in</span></span>  
 <span data-ttu-id="d5b47-142">It is important to perform these steps before the first execution of a sandboxed plug-in.</span><span class="sxs-lookup"><span data-stu-id="d5b47-142">It is important to perform these steps before the first execution of a sandboxed plug-in.</span></span> <span data-ttu-id="d5b47-143">If the plug-in has already been executed, either change the code of the assembly, causing the hash of the assembly to change on the server, or restart the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps Sandbox Processing Service on the sandbox server.</span><span class="sxs-lookup"><span data-stu-id="d5b47-143">If the plug-in has already been executed, either change the code of the assembly, causing the hash of the assembly to change on the server, or restart the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps Sandbox Processing Service on the sandbox server.</span></span>  
  
 <span data-ttu-id="d5b47-144">**Configure the Server**</span><span class="sxs-lookup"><span data-stu-id="d5b47-144">**Configure the Server**</span></span>  
  
 <span data-ttu-id="d5b47-145">The sandbox host process monitors the sandbox worker process which is executing the plug-in.</span><span class="sxs-lookup"><span data-stu-id="d5b47-145">The sandbox host process monitors the sandbox worker process which is executing the plug-in.</span></span> <span data-ttu-id="d5b47-146">The host process checks if the plug-in stops responding, if it is exceeding memory thresholds, and more.</span><span class="sxs-lookup"><span data-stu-id="d5b47-146">The host process checks if the plug-in stops responding, if it is exceeding memory thresholds, and more.</span></span> <span data-ttu-id="d5b47-147">If the worker process doesn't respond for than 30 seconds, it will be shutdown.</span><span class="sxs-lookup"><span data-stu-id="d5b47-147">If the worker process doesn't respond for than 30 seconds, it will be shutdown.</span></span> <span data-ttu-id="d5b47-148">In order to debug a sandbox plug-in, you must disable this shutdown feature.</span><span class="sxs-lookup"><span data-stu-id="d5b47-148">In order to debug a sandbox plug-in, you must disable this shutdown feature.</span></span> <span data-ttu-id="d5b47-149">To disable the shutdown feature, set the following registry key to 1 (`DWORD`):</span><span class="sxs-lookup"><span data-stu-id="d5b47-149">To disable the shutdown feature, set the following registry key to 1 (`DWORD`):</span></span>  
  
```ms-dos  
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSCRM\SandboxDebugPlugins  
```  
  
 <span data-ttu-id="d5b47-150">**Debug the Plug-in**</span><span class="sxs-lookup"><span data-stu-id="d5b47-150">**Debug the Plug-in**</span></span>  
  
 <span data-ttu-id="d5b47-151">Follow these steps to debug a sandboxed plug-in.</span><span class="sxs-lookup"><span data-stu-id="d5b47-151">Follow these steps to debug a sandboxed plug-in.</span></span>  
  
1. <span data-ttu-id="d5b47-152">Register the plug-in in the sandbox (isolation mode) and deploy it to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server database.</span><span class="sxs-lookup"><span data-stu-id="d5b47-152">Register the plug-in in the sandbox (isolation mode) and deploy it to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server database.</span></span>  
  
2. <span data-ttu-id="d5b47-153">Copy the symbol file (.pdb) of the compiled plug-in assembly to the server\bin\assembly folder on the server running the sandbox worker process named Microsoft.Crm.Sandbox.WorkerProcess.exe.</span><span class="sxs-lookup"><span data-stu-id="d5b47-153">Copy the symbol file (.pdb) of the compiled plug-in assembly to the server\bin\assembly folder on the server running the sandbox worker process named Microsoft.Crm.Sandbox.WorkerProcess.exe.</span></span> <span data-ttu-id="d5b47-154">This is the server hosting the Sandbox Processing Service role.</span><span class="sxs-lookup"><span data-stu-id="d5b47-154">This is the server hosting the Sandbox Processing Service role.</span></span>  
  
3. <span data-ttu-id="d5b47-155">Follow the instructions in steps 2 through 4 presented at the beginning of this topic.</span><span class="sxs-lookup"><span data-stu-id="d5b47-155">Follow the instructions in steps 2 through 4 presented at the beginning of this topic.</span></span>  
  
   <span data-ttu-id="d5b47-156">For more information about debugging a plug-in using the Plug-in Profiler tool, see [Analyze Plug-in Performance](analyze-plugin-performance.md).</span><span class="sxs-lookup"><span data-stu-id="d5b47-156">For more information about debugging a plug-in using the Plug-in Profiler tool, see [Analyze Plug-in Performance](analyze-plugin-performance.md).</span></span>  
  
<a name="loggingandtracing"></a>   
## <a name="logging-and-tracing"></a><span data-ttu-id="d5b47-157">Logging and tracing</span><span class="sxs-lookup"><span data-stu-id="d5b47-157">Logging and tracing</span></span>  
 <span data-ttu-id="d5b47-158">An alternative method to troubleshoot a plug-in or custom workflow activity (custom code), compared to debugging in [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)], is to use tracing.</span><span class="sxs-lookup"><span data-stu-id="d5b47-158">An alternative method to troubleshoot a plug-in or custom workflow activity (custom code), compared to debugging in [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)], is to use tracing.</span></span> <span data-ttu-id="d5b47-159">Tracing assists developers by recording run-time custom information as an aid in diagnosing the cause of code failures.</span><span class="sxs-lookup"><span data-stu-id="d5b47-159">Tracing assists developers by recording run-time custom information as an aid in diagnosing the cause of code failures.</span></span> <span data-ttu-id="d5b47-160">Tracing is especially useful to troubleshoot [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] registered custom code as it is the only supported troubleshooting method for that scenario.</span><span class="sxs-lookup"><span data-stu-id="d5b47-160">Tracing is especially useful to troubleshoot [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] registered custom code as it is the only supported troubleshooting method for that scenario.</span></span> <span data-ttu-id="d5b47-161">Tracing is supported for sandboxed (partial trust) and full trust registered custom code and during synchronous or asynchronous execution.</span><span class="sxs-lookup"><span data-stu-id="d5b47-161">Tracing is supported for sandboxed (partial trust) and full trust registered custom code and during synchronous or asynchronous execution.</span></span> <span data-ttu-id="d5b47-162">Tracing isn’t supported for custom code that executes in [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)] or other mobile client.</span><span class="sxs-lookup"><span data-stu-id="d5b47-162">Tracing isn’t supported for custom code that executes in [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)] or other mobile client.</span></span>  
  
 <span data-ttu-id="d5b47-163">Recording of run-time tracing information for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps is provided by a service named <xref:Microsoft.Xrm.Sdk.ITracingService>.</span><span class="sxs-lookup"><span data-stu-id="d5b47-163">Recording of run-time tracing information for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps is provided by a service named <xref:Microsoft.Xrm.Sdk.ITracingService>.</span></span> <span data-ttu-id="d5b47-164">Information provided to this service by custom code can be recorded in three different places as identified here.</span><span class="sxs-lookup"><span data-stu-id="d5b47-164">Information provided to this service by custom code can be recorded in three different places as identified here.</span></span>  

> [!NOTE]
> <span data-ttu-id="d5b47-165">Trace logging using `ITracingService` interface works only when the Plug-in is registered in Sandbox mode.</span><span class="sxs-lookup"><span data-stu-id="d5b47-165">Trace logging using `ITracingService` interface works only when the Plug-in is registered in Sandbox mode.</span></span>

- <span data-ttu-id="d5b47-166">**Trace log**</span><span class="sxs-lookup"><span data-stu-id="d5b47-166">**Trace log**</span></span>  
  
     <span data-ttu-id="d5b47-167">Trace log records of type **PluginTraceLog** can be found in the web application by navigating to **Settings** and choosing the **Plug-in Trace Log** tile.</span><span class="sxs-lookup"><span data-stu-id="d5b47-167">Trace log records of type **PluginTraceLog** can be found in the web application by navigating to **Settings** and choosing the **Plug-in Trace Log** tile.</span></span> <span data-ttu-id="d5b47-168">The tile is only visible if you have access to the trace log entity records in your assigned security role.</span><span class="sxs-lookup"><span data-stu-id="d5b47-168">The tile is only visible if you have access to the trace log entity records in your assigned security role.</span></span> <span data-ttu-id="d5b47-169">Writing of these records is controlled by the trace settings mentioned in the next section.</span><span class="sxs-lookup"><span data-stu-id="d5b47-169">Writing of these records is controlled by the trace settings mentioned in the next section.</span></span>
  
    > [!NOTE]
    >  <span data-ttu-id="d5b47-170">Trace logging takes up organization storage space especially when many traces and exceptions are generated.</span><span class="sxs-lookup"><span data-stu-id="d5b47-170">Trace logging takes up organization storage space especially when many traces and exceptions are generated.</span></span> <span data-ttu-id="d5b47-171">You should only turn trace logging on for debugging and troubleshooting, and turn it off after your investigation is completed.</span><span class="sxs-lookup"><span data-stu-id="d5b47-171">You should only turn trace logging on for debugging and troubleshooting, and turn it off after your investigation is completed.</span></span>  
  
- <span data-ttu-id="d5b47-172">**Error dialog**</span><span class="sxs-lookup"><span data-stu-id="d5b47-172">**Error dialog**</span></span>  
  
     <span data-ttu-id="d5b47-173">A synchronous registered plug-in or custom workflow activity that returns an exception back to the platform results in an error dialog box in the web application presented to the logged on user.</span><span class="sxs-lookup"><span data-stu-id="d5b47-173">A synchronous registered plug-in or custom workflow activity that returns an exception back to the platform results in an error dialog box in the web application presented to the logged on user.</span></span> <span data-ttu-id="d5b47-174">The user may select the **Download Log File** button in the dialog to view the log containing exception and trace output.</span><span class="sxs-lookup"><span data-stu-id="d5b47-174">The user may select the **Download Log File** button in the dialog to view the log containing exception and trace output.</span></span>  
  
- <span data-ttu-id="d5b47-175">**System job**</span><span class="sxs-lookup"><span data-stu-id="d5b47-175">**System job**</span></span>  
  
     <span data-ttu-id="d5b47-176">For asynchronous registered plug-in or custom workflow activities that returns an exception, the tracing information is shown in the **Details** area of the **System Job** form in the web application.</span><span class="sxs-lookup"><span data-stu-id="d5b47-176">For asynchronous registered plug-in or custom workflow activities that returns an exception, the tracing information is shown in the **Details** area of the **System Job** form in the web application.</span></span>  
  
<a name="bkmk_trace-settings"></a>   
### <a name="enable-trace-logging"></a><span data-ttu-id="d5b47-177">Enable trace logging</span><span class="sxs-lookup"><span data-stu-id="d5b47-177">Enable trace logging</span></span>  
 <span data-ttu-id="d5b47-178">To enable trace logging in an organization that supports this feature, in the web application navigate to **Settings** > **Administration** > **System Settings**.</span><span class="sxs-lookup"><span data-stu-id="d5b47-178">To enable trace logging in an organization that supports this feature, in the web application navigate to **Settings** > **Administration** > **System Settings**.</span></span> <span data-ttu-id="d5b47-179">In the **Customization** tab, locate the drop-down menu labeled **Enable logging to plug-in trace log** and select one of the available options.</span><span class="sxs-lookup"><span data-stu-id="d5b47-179">In the **Customization** tab, locate the drop-down menu labeled **Enable logging to plug-in trace log** and select one of the available options.</span></span>  
  
|<span data-ttu-id="d5b47-180">Tùy chọn</span><span class="sxs-lookup"><span data-stu-id="d5b47-180">Option</span></span>|<span data-ttu-id="d5b47-181">Mô tả</span><span class="sxs-lookup"><span data-stu-id="d5b47-181">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="d5b47-182">Tắt</span><span class="sxs-lookup"><span data-stu-id="d5b47-182">Off</span></span>|<span data-ttu-id="d5b47-183">Writing to the trace log is disabled.</span><span class="sxs-lookup"><span data-stu-id="d5b47-183">Writing to the trace log is disabled.</span></span> <span data-ttu-id="d5b47-184">No **PluginTraceLog** records will be created.</span><span class="sxs-lookup"><span data-stu-id="d5b47-184">No **PluginTraceLog** records will be created.</span></span> <span data-ttu-id="d5b47-185">However, custom code can still call the <xref:Microsoft.Xrm.Sdk.ITracingService.Trace(System.String,System.Object[])> method even though no log is written.</span><span class="sxs-lookup"><span data-stu-id="d5b47-185">However, custom code can still call the <xref:Microsoft.Xrm.Sdk.ITracingService.Trace(System.String,System.Object[])> method even though no log is written.</span></span>|  
|<span data-ttu-id="d5b47-186">Ngoại lệ</span><span class="sxs-lookup"><span data-stu-id="d5b47-186">Exceptions</span></span>|<span data-ttu-id="d5b47-187">Trace information is written to the log if an exception is passed back to the platform from custom code.</span><span class="sxs-lookup"><span data-stu-id="d5b47-187">Trace information is written to the log if an exception is passed back to the platform from custom code.</span></span>|  
|<span data-ttu-id="d5b47-188">Tất cả</span><span class="sxs-lookup"><span data-stu-id="d5b47-188">All</span></span>|<span data-ttu-id="d5b47-189">Trace information is written to the log upon code completion or an exception is passed back to the platform from the custom code.</span><span class="sxs-lookup"><span data-stu-id="d5b47-189">Trace information is written to the log upon code completion or an exception is passed back to the platform from the custom code.</span></span>|  
  
 <span data-ttu-id="d5b47-190">If the trace logging setting is set to **Exception** and your custom code returns an exception back to the platform, a trace log record is created and tracing information is also written to one other location.</span><span class="sxs-lookup"><span data-stu-id="d5b47-190">If the trace logging setting is set to **Exception** and your custom code returns an exception back to the platform, a trace log record is created and tracing information is also written to one other location.</span></span> <span data-ttu-id="d5b47-191">For custom code that executes synchronously, the information is presented to the user in an error dialog box, otherwise, for asynchronous code, the information is written to the related system job.</span><span class="sxs-lookup"><span data-stu-id="d5b47-191">For custom code that executes synchronously, the information is presented to the user in an error dialog box, otherwise, for asynchronous code, the information is written to the related system job.</span></span>  
  
 <span data-ttu-id="d5b47-192">By default, the System Administrator and System Customizer roles have the required privileges to change the trace logging setting, which is stored in a <xref:Microsoft.Xrm.Sdk.Deployment.TraceSettings> entity record.</span><span class="sxs-lookup"><span data-stu-id="d5b47-192">By default, the System Administrator and System Customizer roles have the required privileges to change the trace logging setting, which is stored in a <xref:Microsoft.Xrm.Sdk.Deployment.TraceSettings> entity record.</span></span> <span data-ttu-id="d5b47-193">Trace settings have an organization scope.</span><span class="sxs-lookup"><span data-stu-id="d5b47-193">Trace settings have an organization scope.</span></span>  
  
### <a name="write-to-the-tracing-service"></a><span data-ttu-id="d5b47-194">Write to the tracing service</span><span class="sxs-lookup"><span data-stu-id="d5b47-194">Write to the tracing service</span></span>  
 <span data-ttu-id="d5b47-195">Before writing to the tracing service, you must first extract the tracing service object from the passed execution context.</span><span class="sxs-lookup"><span data-stu-id="d5b47-195">Before writing to the tracing service, you must first extract the tracing service object from the passed execution context.</span></span> <span data-ttu-id="d5b47-196">Afterwards, simply add <xref:Microsoft.Xrm.Sdk.ITracingService.Trace(System.String,System.Object[])> calls to your custom code where appropriate passing any relevant diagnostic information in that method call.</span><span class="sxs-lookup"><span data-stu-id="d5b47-196">Afterwards, simply add <xref:Microsoft.Xrm.Sdk.ITracingService.Trace(System.String,System.Object[])> calls to your custom code where appropriate passing any relevant diagnostic information in that method call.</span></span>  

 <span data-ttu-id="d5b47-197">Download the sample: [Work with plug-ins](https://code.msdn.microsoft.com/Sample-Create-a-basic-plug-64d86ade).</span><span class="sxs-lookup"><span data-stu-id="d5b47-197">Download the sample: [Work with plug-ins](https://code.msdn.microsoft.com/Sample-Create-a-basic-plug-64d86ade).</span></span>
  
 [!code-csharp[Plug-ins#AdvancedPlugin2](../snippets/csharp/CRMV8/plug-ins/cs/advancedplugin2.cs#advancedplugin2)]  
  
 <span data-ttu-id="d5b47-198">Next, build and deploy the plug-in or custom workflow activity.</span><span class="sxs-lookup"><span data-stu-id="d5b47-198">Next, build and deploy the plug-in or custom workflow activity.</span></span> <span data-ttu-id="d5b47-199">During execution of the custom code, the information provided in the **Trace** method calls is written to a trace log entity record by <xref:Microsoft.Xrm.Sdk.ITracingService>, if supported by your organization and enabled, and may also be made available to the user in a Web dialog or system job as described in the previous section.</span><span class="sxs-lookup"><span data-stu-id="d5b47-199">During execution of the custom code, the information provided in the **Trace** method calls is written to a trace log entity record by <xref:Microsoft.Xrm.Sdk.ITracingService>, if supported by your organization and enabled, and may also be made available to the user in a Web dialog or system job as described in the previous section.</span></span> <span data-ttu-id="d5b47-200">Tracing information written to the trace log is configured in the trace settings.</span><span class="sxs-lookup"><span data-stu-id="d5b47-200">Tracing information written to the trace log is configured in the trace settings.</span></span> <span data-ttu-id="d5b47-201">For more information see [Enable the trace logging feature](debug-plugin.md#bkmk_trace-settings).</span><span class="sxs-lookup"><span data-stu-id="d5b47-201">For more information see [Enable the trace logging feature](debug-plugin.md#bkmk_trace-settings).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d5b47-202">If your custom code executes within a database transaction, and an exception occurs that causes a transaction rollback, all entity data changes by your code will be undone.</span><span class="sxs-lookup"><span data-stu-id="d5b47-202">If your custom code executes within a database transaction, and an exception occurs that causes a transaction rollback, all entity data changes by your code will be undone.</span></span> <span data-ttu-id="d5b47-203">However, the **PluginTraceLog** records will remain after the rollback completes.</span><span class="sxs-lookup"><span data-stu-id="d5b47-203">However, the **PluginTraceLog** records will remain after the rollback completes.</span></span>  
  
### <a name="about-the-tracing-service"></a><span data-ttu-id="d5b47-204">About the tracing service</span><span class="sxs-lookup"><span data-stu-id="d5b47-204">About the tracing service</span></span>  
 <span data-ttu-id="d5b47-205">The <xref:Microsoft.Xrm.Sdk.ITracingService> batches the information provided to it through the **Trace** method.</span><span class="sxs-lookup"><span data-stu-id="d5b47-205">The <xref:Microsoft.Xrm.Sdk.ITracingService> batches the information provided to it through the **Trace** method.</span></span> <span data-ttu-id="d5b47-206">The information is written to a new **PluginTraceLog** record after the custom code successfully runs to completion or an exception is thrown.</span><span class="sxs-lookup"><span data-stu-id="d5b47-206">The information is written to a new **PluginTraceLog** record after the custom code successfully runs to completion or an exception is thrown.</span></span>  
  
 <span data-ttu-id="d5b47-207">PluginTraceLog records have a finite lifetime.</span><span class="sxs-lookup"><span data-stu-id="d5b47-207">PluginTraceLog records have a finite lifetime.</span></span> <span data-ttu-id="d5b47-208">A bulk deletion background job runs once per day to delete records that are older than 24 hours from creation.</span><span class="sxs-lookup"><span data-stu-id="d5b47-208">A bulk deletion background job runs once per day to delete records that are older than 24 hours from creation.</span></span> <span data-ttu-id="d5b47-209">This job can be disabled when needed.</span><span class="sxs-lookup"><span data-stu-id="d5b47-209">This job can be disabled when needed.</span></span>  

 ## <a name="community-tools"></a><span data-ttu-id="d5b47-210">Các công cụ dành cho cộng đồng</span><span class="sxs-lookup"><span data-stu-id="d5b47-210">Community tools</span></span>

 ### <a name="plugin-trace-viewer"></a><span data-ttu-id="d5b47-211">Plugin trace viewer</span><span class="sxs-lookup"><span data-stu-id="d5b47-211">Plugin trace viewer</span></span>

<span data-ttu-id="d5b47-212">**Plugin Trace Viewer** is a tool that XrmToolbox community developed for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="d5b47-212">**Plugin Trace Viewer** is a tool that XrmToolbox community developed for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span></span> <span data-ttu-id="d5b47-213">Vui lòng xem chủ đề [Công cụ dành cho nhà phát triển](developer-tools.md) về các công cụ được cộng đồng phát triển.</span><span class="sxs-lookup"><span data-stu-id="d5b47-213">Please see the [Developer tools](developer-tools.md) topic for community developed tools.</span></span>

> [!NOTE]
> <span data-ttu-id="d5b47-214">The community tools are not a product of [!include[pn_microsoft_dynamics](../includes/pn-microsoft-dynamics.md)] apps and does not extend support to the community tools.</span><span class="sxs-lookup"><span data-stu-id="d5b47-214">The community tools are not a product of [!include[pn_microsoft_dynamics](../includes/pn-microsoft-dynamics.md)] apps and does not extend support to the community tools.</span></span> <span data-ttu-id="d5b47-215">If you have questions pertaining to the tool, please contact the publisher.</span><span class="sxs-lookup"><span data-stu-id="d5b47-215">If you have questions pertaining to the tool, please contact the publisher.</span></span> <span data-ttu-id="d5b47-216">More Information: [XrmToolBox](https://www.xrmtoolbox.com).</span><span class="sxs-lookup"><span data-stu-id="d5b47-216">More Information: [XrmToolBox](https://www.xrmtoolbox.com).</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="d5b47-217">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d5b47-217">See also</span></span>  
 <span data-ttu-id="d5b47-218">[Plug-in Development](plugin-development.md) </span><span class="sxs-lookup"><span data-stu-id="d5b47-218">[Plug-in Development](plugin-development.md) </span></span>  
 <span data-ttu-id="d5b47-219">[Analyze Plug-in Performance](analyze-plugin-performance.md) </span><span class="sxs-lookup"><span data-stu-id="d5b47-219">[Analyze Plug-in Performance](analyze-plugin-performance.md) </span></span>  
 <span data-ttu-id="d5b47-220">[Register and Deploy Plug-ins](register-deploy-plugins.md) </span><span class="sxs-lookup"><span data-stu-id="d5b47-220">[Register and Deploy Plug-ins](register-deploy-plugins.md) </span></span>  
 <span data-ttu-id="d5b47-221">[Event Execution Pipeline](event-execution-pipeline.md) </span><span class="sxs-lookup"><span data-stu-id="d5b47-221">[Event Execution Pipeline](event-execution-pipeline.md) </span></span>  
 <span data-ttu-id="d5b47-222">[Write a Plug-in](write-plugin.md) </span><span class="sxs-lookup"><span data-stu-id="d5b47-222">[Write a Plug-in](write-plugin.md) </span></span>  
 <span data-ttu-id="d5b47-223">[Plug-in Isolation, Trust, and the Disallowed List](plugin-isolation-trusts-statistics.md) </span><span class="sxs-lookup"><span data-stu-id="d5b47-223">[Plug-in Isolation, Trust, and the Disallowed List](plugin-isolation-trusts-statistics.md) </span></span>  
 [<span data-ttu-id="d5b47-224">PluginTraceLog Entity</span><span class="sxs-lookup"><span data-stu-id="d5b47-224">PluginTraceLog Entity</span></span>](entities/plugintracelog.md)