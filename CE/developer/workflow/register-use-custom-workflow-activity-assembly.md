---
title: Register and use a custom workflow activity assembly (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about registering and using a custom workflow activity assembly
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 2dd2fe35-f681-4548-9b2b-5ad7c8470b8d
caps.latest.revision: 50
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f4b5c6535551e181001b61ea852333c5c17e8a3d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387454"
---
# <a name="register-and-use-a-custom-workflow-activity-assembly"></a><span data-ttu-id="e2820-103">Register and use a custom workflow activity assembly</span><span class="sxs-lookup"><span data-stu-id="e2820-103">Register and use a custom workflow activity assembly</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e2820-104">After you compile your custom workflow activity to create an assembly, you have to register the assembly with [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="e2820-104">After you compile your custom workflow activity to create an assembly, you have to register the assembly with [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement.</span></span> <span data-ttu-id="e2820-105">Your custom activity then appears in the process form of [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] or [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] (on-premises) depending on which deployment you registered the custom workflow activity with.</span><span class="sxs-lookup"><span data-stu-id="e2820-105">Your custom activity then appears in the process form of [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] or [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] (on-premises) depending on which deployment you registered the custom workflow activity with.</span></span>

<a name="enable_disable"></a>

## <a name="enable-or-disable-custom-code"></a><span data-ttu-id="e2820-106">Enable or disable custom code</span><span class="sxs-lookup"><span data-stu-id="e2820-106">Enable or disable custom code</span></span>

[!INCLUDE[cc_sdk_onpremises_note](../../includes/cc-sdk-onpremises-note.md)]
 <span data-ttu-id="e2820-107">You can use [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] to enable or disable custom workflow activities and plug-in execution for an on-premises server as described here.</span><span class="sxs-lookup"><span data-stu-id="e2820-107">You can use [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] to enable or disable custom workflow activities and plug-in execution for an on-premises server as described here.</span></span> <span data-ttu-id="e2820-108">Alternatively, you can use the Deployment web service.</span><span class="sxs-lookup"><span data-stu-id="e2820-108">Alternatively, you can use the Deployment web service.</span></span> <span data-ttu-id="e2820-109">For more information, see [Deployment Entities and Deployment Configuration Settings](https://msdn.microsoft.com/en-us/library/gg328063.aspx) to learn how to set the <xref:Microsoft.Xrm.Sdk.Deployment.CustomCodeSettings>.<xref:Microsoft.Xrm.Sdk.Deployment.CustomCodeSettings.AllowExternalCode></span><span class="sxs-lookup"><span data-stu-id="e2820-109">For more information, see [Deployment Entities and Deployment Configuration Settings](https://msdn.microsoft.com/en-us/library/gg328063.aspx) to learn how to set the <xref:Microsoft.Xrm.Sdk.Deployment.CustomCodeSettings>.<xref:Microsoft.Xrm.Sdk.Deployment.CustomCodeSettings.AllowExternalCode></span></span> <span data-ttu-id="e2820-110">property.</span><span class="sxs-lookup"><span data-stu-id="e2820-110">property.</span></span>  

### <a name="to-enable-custom-code"></a><span data-ttu-id="e2820-111">To enable custom code</span><span class="sxs-lookup"><span data-stu-id="e2820-111">To enable custom code</span></span>

1. <span data-ttu-id="e2820-112">Mở cửa sổ lệnh [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)].</span><span class="sxs-lookup"><span data-stu-id="e2820-112">Open a [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] command window.</span></span>
2. <span data-ttu-id="e2820-113">Thêm đính kèm PowerShell [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)]:</span><span class="sxs-lookup"><span data-stu-id="e2820-113">Add the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] PowerShell snap-in:</span></span>
    ```powershell
    Add-PSSnapin Microsoft.Crm.PowerShell
    ```
3. <span data-ttu-id="e2820-114">Retrieve the current setting:</span><span class="sxs-lookup"><span data-stu-id="e2820-114">Retrieve the current setting:</span></span>
    ```powershell
    $setting = get-crmsetting customcodesettings
    ```
4. <span data-ttu-id="e2820-115">Modify the current setting:</span><span class="sxs-lookup"><span data-stu-id="e2820-115">Modify the current setting:</span></span>
    ```powershell
    $setting.AllowExternalCode="True"
    set-crmsetting $setting
    ```
5. <span data-ttu-id="e2820-116">Verify the setting:</span><span class="sxs-lookup"><span data-stu-id="e2820-116">Verify the setting:</span></span>
    ```powershell
    get-crmsetting customcodesettings
    ```

### <a name="to-disable-custom-code"></a><span data-ttu-id="e2820-117">To disable custom code</span><span class="sxs-lookup"><span data-stu-id="e2820-117">To disable custom code</span></span>

1. <span data-ttu-id="e2820-118">Open a [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] command window.</span><span class="sxs-lookup"><span data-stu-id="e2820-118">Open a [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] command window.</span></span>
2. <span data-ttu-id="e2820-119">Add the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] PowerShell snap-in:</span><span class="sxs-lookup"><span data-stu-id="e2820-119">Add the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] PowerShell snap-in:</span></span>

    ```powershell
    Add-PSSnapin Microsoft.Crm.PowerShell
    ```

3. <span data-ttu-id="e2820-120">Retrieve the current setting:</span><span class="sxs-lookup"><span data-stu-id="e2820-120">Retrieve the current setting:</span></span>

    ```powershell
    $setting = get-crmsetting customcodesettings
    ```

4. <span data-ttu-id="e2820-121">Modify the current setting:</span><span class="sxs-lookup"><span data-stu-id="e2820-121">Modify the current setting:</span></span>

    ```powershell
    $setting.AllowExternalCode=0
    set-crmsetting $setting
    ```
5. <span data-ttu-id="e2820-122">Verify the setting:</span><span class="sxs-lookup"><span data-stu-id="e2820-122">Verify the setting:</span></span>
    ```powershell
    get-crmsetting customcodesettings
    ```

<a name="register"></a>

## <a name="register-a-custom-workflow-activity"></a><span data-ttu-id="e2820-123">Register a custom workflow activity</span><span class="sxs-lookup"><span data-stu-id="e2820-123">Register a custom workflow activity</span></span>

 <span data-ttu-id="e2820-124">Custom workflow activity assemblies are registered using the Plug-in Registration tool.</span><span class="sxs-lookup"><span data-stu-id="e2820-124">Custom workflow activity assemblies are registered using the Plug-in Registration tool.</span></span> <span data-ttu-id="e2820-125">The tool provides a graphical user interface and supports registering assemblies that contain plug-ins or custom workflow activities.</span><span class="sxs-lookup"><span data-stu-id="e2820-125">The tool provides a graphical user interface and supports registering assemblies that contain plug-ins or custom workflow activities.</span></span> <span data-ttu-id="e2820-126">When registering an assembly that contains custom workflow activities with [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)], you must register the assembly in the sandbox (partial trust).</span><span class="sxs-lookup"><span data-stu-id="e2820-126">When registering an assembly that contains custom workflow activities with [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)], you must register the assembly in the sandbox (partial trust).</span></span>

 <span data-ttu-id="e2820-127">For more information about how to register and deploy a custom activity assembly by using the tool, see [Specify the Name and Group Name for a Custom Workflow Activity](create-custom-workflow-activity.md#NameandGroupName).</span><span class="sxs-lookup"><span data-stu-id="e2820-127">For more information about how to register and deploy a custom activity assembly by using the tool, see [Specify the Name and Group Name for a Custom Workflow Activity](create-custom-workflow-activity.md#NameandGroupName).</span></span>

> [!NOTE]
> [!INCLUDE[proc-download-plugin-registration-tool](../../includes/proc-download-plugin-registration-tool.md)] <span data-ttu-id="e2820-128">The `PluginRegistration.exe` can be added to the [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] **Tools** menu as an external tool to speed up the development process.</span><span class="sxs-lookup"><span data-stu-id="e2820-128">The `PluginRegistration.exe` can be added to the [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] **Tools** menu as an external tool to speed up the development process.</span></span>

<a name="use"></a>

## <a name="use-a-custom-workflow-activity-in-a-process"></a><span data-ttu-id="e2820-129">Use a custom workflow activity in a process</span><span class="sxs-lookup"><span data-stu-id="e2820-129">Use a custom workflow activity in a process</span></span>

<span data-ttu-id="e2820-130">After you have registered your custom workflow activity assembly, you can use it in the process designer in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)].</span><span class="sxs-lookup"><span data-stu-id="e2820-130">After you have registered your custom workflow activity assembly, you can use it in the process designer in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)].</span></span>

<span data-ttu-id="e2820-131">To use your custom workflow activity in a process:</span><span class="sxs-lookup"><span data-stu-id="e2820-131">To use your custom workflow activity in a process:</span></span>

1. <span data-ttu-id="e2820-132">Đăng nhập vào [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)].</span><span class="sxs-lookup"><span data-stu-id="e2820-132">Sign in to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)].</span></span>
2. [!INCLUDE[proc_settings_processes](../../includes/proc-settings-processes.md)]<span data-ttu-id="e2820-133">.</span><span class="sxs-lookup"><span data-stu-id="e2820-133">.</span></span>
3. <span data-ttu-id="e2820-134">Create or open an existing process.</span><span class="sxs-lookup"><span data-stu-id="e2820-134">Create or open an existing process.</span></span>
4. <span data-ttu-id="e2820-135">In the process designer, click or tap **Add Step**.</span><span class="sxs-lookup"><span data-stu-id="e2820-135">In the process designer, click or tap **Add Step**.</span></span> <span data-ttu-id="e2820-136">Your custom workflow activity name will appear in the drop-down list.</span><span class="sxs-lookup"><span data-stu-id="e2820-136">Your custom workflow activity name will appear in the drop-down list.</span></span>

### <a name="see-also"></a><span data-ttu-id="e2820-137">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e2820-137">See also</span></span>

 [<span data-ttu-id="e2820-138">Custom workflow activities (workflow assemblies)</span><span class="sxs-lookup"><span data-stu-id="e2820-138">Custom workflow activities (workflow assemblies)</span></span>](../custom-workflow-activities-workflow-assemblies.md)<br />
 [<span data-ttu-id="e2820-139">Debug a custom workflow activity</span><span class="sxs-lookup"><span data-stu-id="e2820-139">Debug a custom workflow activity</span></span>](debug-custom-workflow-activity.md)<br />
 [<span data-ttu-id="e2820-140">Plug-in isolation, trusts, and statistics</span><span class="sxs-lookup"><span data-stu-id="e2820-140">Plug-in isolation, trusts, and statistics</span></span>](../plugin-isolation-trusts-statistics.md)<br />
 [<span data-ttu-id="e2820-141">Register and Deploy Plug-Ins</span><span class="sxs-lookup"><span data-stu-id="e2820-141">Register and Deploy Plug-Ins</span></span>](../register-deploy-plugins.md)
