---
title: Plug-in isolation, trusts, and statistics (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about collecting run-time statistics and monitors plug-ins and custom workflow activities that execute in the sandbox.
ms.custom: ''
ms.date: 12/03/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: fe83bfd4-7ac1-4b9c-8cea-dc32d3ed60b6
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f7ae3e33fecd41b4ba7a79beb12c9758662a561a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386152"
---
# <a name="plug-in-isolation-trusts-and-statistics"></a><span data-ttu-id="99bf5-103">Plug-in isolation, trusts, and statistics</span><span class="sxs-lookup"><span data-stu-id="99bf5-103">Plug-in isolation, trusts, and statistics</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] <span data-ttu-id="99bf5-104">apps supports the execution of plug-ins and custom workflow activities in an isolated environment.</span><span class="sxs-lookup"><span data-stu-id="99bf5-104">apps supports the execution of plug-ins and custom workflow activities in an isolated environment.</span></span> <span data-ttu-id="99bf5-105">In this isolated environment, known as a *sandbox*, a plug-in or custom activity can make use of the full power of the Organization Service.</span><span class="sxs-lookup"><span data-stu-id="99bf5-105">In this isolated environment, known as a *sandbox*, a plug-in or custom activity can make use of the full power of the Organization Service.</span></span> <span data-ttu-id="99bf5-106">Access to the file system, system event log, certain network protocols, registry, and more is prevented in the sandbox.</span><span class="sxs-lookup"><span data-stu-id="99bf5-106">Access to the file system, system event log, certain network protocols, registry, and more is prevented in the sandbox.</span></span> <span data-ttu-id="99bf5-107">However, sandbox plug-ins and custom activities do have access to external endpoints like [!INCLUDE[pn_azure_cloud_services](../includes/pn-azure-cloud-services.md)].</span><span class="sxs-lookup"><span data-stu-id="99bf5-107">However, sandbox plug-ins and custom activities do have access to external endpoints like [!INCLUDE[pn_azure_cloud_services](../includes/pn-azure-cloud-services.md)].</span></span>  
  
[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="99bf5-108">apps collects run-time statistics and monitors plug-ins and custom workflow activities that execute in the sandbox.</span><span class="sxs-lookup"><span data-stu-id="99bf5-108">apps collects run-time statistics and monitors plug-ins and custom workflow activities that execute in the sandbox.</span></span> <span data-ttu-id="99bf5-109">If the sandbox worker process that hosts this custom code exceeds threshold CPU, memory, or handle limits or is otherwise unresponsive, that process will be killed by the platform.</span><span class="sxs-lookup"><span data-stu-id="99bf5-109">If the sandbox worker process that hosts this custom code exceeds threshold CPU, memory, or handle limits or is otherwise unresponsive, that process will be killed by the platform.</span></span> <span data-ttu-id="99bf5-110">At that point any currently executing plug-in or custom workflow activity in that worker process will fail with exceptions.</span><span class="sxs-lookup"><span data-stu-id="99bf5-110">At that point any currently executing plug-in or custom workflow activity in that worker process will fail with exceptions.</span></span> <span data-ttu-id="99bf5-111">However, the next time that the plug-in or custom workflow activity is executed it will run normally.</span><span class="sxs-lookup"><span data-stu-id="99bf5-111">However, the next time that the plug-in or custom workflow activity is executed it will run normally.</span></span> <span data-ttu-id="99bf5-112">There is one worker process per organization so failures in one organization will not affect another organization.</span><span class="sxs-lookup"><span data-stu-id="99bf5-112">There is one worker process per organization so failures in one organization will not affect another organization.</span></span>  
  
<span data-ttu-id="99bf5-113">In summary, the sandbox is the recommended execution environment for plug-ins as it is more secure, supports run-time monitoring and statistics reporting, and is supported on all [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps deployments.</span><span class="sxs-lookup"><span data-stu-id="99bf5-113">In summary, the sandbox is the recommended execution environment for plug-ins as it is more secure, supports run-time monitoring and statistics reporting, and is supported on all [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps deployments.</span></span> <span data-ttu-id="99bf5-114">In addition, [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps only supports execution of custom workflow activities if they are registered in the sandbox.</span><span class="sxs-lookup"><span data-stu-id="99bf5-114">In addition, [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps only supports execution of custom workflow activities if they are registered in the sandbox.</span></span>  
  
## <a name="trusts"></a><span data-ttu-id="99bf5-115">Trusts</span><span class="sxs-lookup"><span data-stu-id="99bf5-115">Trusts</span></span>

 <span data-ttu-id="99bf5-116">Developers have the option of registering their plug-ins in the sandbox, known as partial trust, or outside the sandbox, known as full trust.</span><span class="sxs-lookup"><span data-stu-id="99bf5-116">Developers have the option of registering their plug-ins in the sandbox, known as partial trust, or outside the sandbox, known as full trust.</span></span> <span data-ttu-id="99bf5-117">Full trust is supported for on-premises and Internet-facing [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps deployments.</span><span class="sxs-lookup"><span data-stu-id="99bf5-117">Full trust is supported for on-premises and Internet-facing [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps deployments.</span></span> <span data-ttu-id="99bf5-118">For a [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps deployment, plug-ins or custom workflow activities must be registered in the sandbox (partial trust) where they are isolated as previously described.</span><span class="sxs-lookup"><span data-stu-id="99bf5-118">For a [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps deployment, plug-ins or custom workflow activities must be registered in the sandbox (partial trust) where they are isolated as previously described.</span></span>  
  
[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)]

## <a name="run-time-statistics"></a><span data-ttu-id="99bf5-119">Run-time statistics</span><span class="sxs-lookup"><span data-stu-id="99bf5-119">Run-time statistics</span></span>

<span data-ttu-id="99bf5-120">The [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] platform collects run-time information about plug-ins and custom workflow activities that execute in the sandbox.</span><span class="sxs-lookup"><span data-stu-id="99bf5-120">The [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] platform collects run-time information about plug-ins and custom workflow activities that execute in the sandbox.</span></span> <span data-ttu-id="99bf5-121">This information is stored in the database using [PluginTypeStatistic](entities/plugintypestatistic.md) entity records.</span><span class="sxs-lookup"><span data-stu-id="99bf5-121">This information is stored in the database using [PluginTypeStatistic](entities/plugintypestatistic.md) entity records.</span></span> <span data-ttu-id="99bf5-122">These records are populated within 30 minutes to one hour after the sandboxed custom code executes.</span><span class="sxs-lookup"><span data-stu-id="99bf5-122">These records are populated within 30 minutes to one hour after the sandboxed custom code executes.</span></span> <span data-ttu-id="99bf5-123">See the [PluginTypeStatistic](entities/plugintypestatistic.md) attributes to find out what information is collected.</span><span class="sxs-lookup"><span data-stu-id="99bf5-123">See the [PluginTypeStatistic](entities/plugintypestatistic.md) attributes to find out what information is collected.</span></span> <span data-ttu-id="99bf5-124">You can retrieve this information by using the retrieve message or method.</span><span class="sxs-lookup"><span data-stu-id="99bf5-124">You can retrieve this information by using the retrieve message or method.</span></span>  
  
## <a name="web-access"></a><span data-ttu-id="99bf5-125">Web access</span><span class="sxs-lookup"><span data-stu-id="99bf5-125">Web access</span></span>

<span data-ttu-id="99bf5-126">Sandboxed plug-ins and custom workflow activities can access the network through the HTTP and HTTPS protocols.</span><span class="sxs-lookup"><span data-stu-id="99bf5-126">Sandboxed plug-ins and custom workflow activities can access the network through the HTTP and HTTPS protocols.</span></span> <span data-ttu-id="99bf5-127">This capability provides support for accessing popular web resources like social sites, news feeds, web services, and more.</span><span class="sxs-lookup"><span data-stu-id="99bf5-127">This capability provides support for accessing popular web resources like social sites, news feeds, web services, and more.</span></span> <span data-ttu-id="99bf5-128">The following web access restrictions apply to this sandbox capability.</span><span class="sxs-lookup"><span data-stu-id="99bf5-128">The following web access restrictions apply to this sandbox capability.</span></span>  
  
- <span data-ttu-id="99bf5-129">Only the HTTP and HTTPS protocols are allowed.</span><span class="sxs-lookup"><span data-stu-id="99bf5-129">Only the HTTP and HTTPS protocols are allowed.</span></span>
- <span data-ttu-id="99bf5-130">Access to localhost (loopback) is not permitted.</span><span class="sxs-lookup"><span data-stu-id="99bf5-130">Access to localhost (loopback) is not permitted.</span></span>
- <span data-ttu-id="99bf5-131">IP addresses cannot be used.</span><span class="sxs-lookup"><span data-stu-id="99bf5-131">IP addresses cannot be used.</span></span> <span data-ttu-id="99bf5-132">You must use a named web address that requires DNS name resolution.</span><span class="sxs-lookup"><span data-stu-id="99bf5-132">You must use a named web address that requires DNS name resolution.</span></span>
- <span data-ttu-id="99bf5-133">Anonymous authentication is supported and recommended.</span><span class="sxs-lookup"><span data-stu-id="99bf5-133">Anonymous authentication is supported and recommended.</span></span> <span data-ttu-id="99bf5-134">There is no provision for prompting the logged on user for credentials or saving those credentials.</span><span class="sxs-lookup"><span data-stu-id="99bf5-134">There is no provision for prompting the logged on user for credentials or saving those credentials.</span></span>
  
### <a name="settings-for-on-premises-and-internet-facing-deployments"></a><span data-ttu-id="99bf5-135">Settings for on-premises and Internet Facing Deployments</span><span class="sxs-lookup"><span data-stu-id="99bf5-135">Settings for on-premises and Internet Facing Deployments</span></span>

[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)]

<span data-ttu-id="99bf5-136">Default web access restrictions are defined in a registry key on the server that is running the `Microsoft.Crm.Sandbox.HostService.exe` process.</span><span class="sxs-lookup"><span data-stu-id="99bf5-136">Default web access restrictions are defined in a registry key on the server that is running the `Microsoft.Crm.Sandbox.HostService.exe` process.</span></span> <span data-ttu-id="99bf5-137">For on-premises and IFD deployments the value of the registry key can be changed by the System Administrator according to business and security needs.</span><span class="sxs-lookup"><span data-stu-id="99bf5-137">For on-premises and IFD deployments the value of the registry key can be changed by the System Administrator according to business and security needs.</span></span> <span data-ttu-id="99bf5-138">The registry key path on the server is:</span><span class="sxs-lookup"><span data-stu-id="99bf5-138">The registry key path on the server is:</span></span>  
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSCRM\SandboxWorkerOutboundUriPattern`  
  
<span data-ttu-id="99bf5-139">The key value is a regular expression string that defines the web access restrictions.</span><span class="sxs-lookup"><span data-stu-id="99bf5-139">The key value is a regular expression string that defines the web access restrictions.</span></span> <span data-ttu-id="99bf5-140">The default key value is:</span><span class="sxs-lookup"><span data-stu-id="99bf5-140">The default key value is:</span></span>  
  
```
"^http[s]?://(?!((localhost[:/])|(\[.*\])|([0-9]+[:/])|(0x[0-9a-f]+[:/])|(((([0-9]+)|(0x[0-9A-F]+))\.){3}(([0-9]+)|(0x[0-9A-F]+))[:/]))).+";  
```  
  
<span data-ttu-id="99bf5-141">By changing this registry key value, you can change the web access for sandboxed plug-ins.</span><span class="sxs-lookup"><span data-stu-id="99bf5-141">By changing this registry key value, you can change the web access for sandboxed plug-ins.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="99bf5-142">The sandbox processing service role defaults to outbound calls being enabled.</span><span class="sxs-lookup"><span data-stu-id="99bf5-142">The sandbox processing service role defaults to outbound calls being enabled.</span></span> <span data-ttu-id="99bf5-143">If you do not want to permit outbound calls from custom code (plug-ins or custom workflow activities), you can disable outbound calls by setting the following registry key to 1 (DWORD) on the server that hosts the sandbox processing service role.</span><span class="sxs-lookup"><span data-stu-id="99bf5-143">If you do not want to permit outbound calls from custom code (plug-ins or custom workflow activities), you can disable outbound calls by setting the following registry key to 1 (DWORD) on the server that hosts the sandbox processing service role.</span></span> <span data-ttu-id="99bf5-144">Next, restart the Dynamics 365 for Customer Engagement apps Sandbox Processing Service.</span><span class="sxs-lookup"><span data-stu-id="99bf5-144">Next, restart the Dynamics 365 for Customer Engagement apps Sandbox Processing Service.</span></span>  
>   
>  `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSCRM\SandboxWorkerDisableOutboundCalls`  
  
### <a name="see-also"></a><span data-ttu-id="99bf5-145">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="99bf5-145">See also</span></span>
  
[<span data-ttu-id="99bf5-146">Introduction to the Event Framework</span><span class="sxs-lookup"><span data-stu-id="99bf5-146">Introduction to the Event Framework</span></span>](introduction-event-framework.md)<br />
[<span data-ttu-id="99bf5-147">Write a Plug-in</span><span class="sxs-lookup"><span data-stu-id="99bf5-147">Write a Plug-in</span></span>](write-plugin.md)<br />
[<span data-ttu-id="99bf5-148">Create a Custom Workflow Activity</span><span class="sxs-lookup"><span data-stu-id="99bf5-148">Create a Custom Workflow Activity</span></span>](workflow/create-custom-workflow-activity.md)<br />
[<span data-ttu-id="99bf5-149">Azure Extensions for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="99bf5-149">Azure Extensions for Dynamics 365 for Customer Engagement apps</span></span>](azure-extensions.md)<br />
[<span data-ttu-id="99bf5-150">PluginTypeStatistic Entity</span><span class="sxs-lookup"><span data-stu-id="99bf5-150">PluginTypeStatistic Entity</span></span>](entities/plugintypestatistic.md)<br />
[<span data-ttu-id="99bf5-151">Sample: Web Access from a Sandboxed Plug-in</span><span class="sxs-lookup"><span data-stu-id="99bf5-151">Sample: Web Access from a Sandboxed Plug-in</span></span>](sample-web-access-sandboxed-plugin.md)<br />
