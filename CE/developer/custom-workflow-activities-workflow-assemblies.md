---
title: Custom workflow activities (workflow assemblies) (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about registration and execution of custom workflow activities in addition to the out-of-box activities provided by Windows Workflow Foundation. You can write custom workflow activities in Microsoft Visual C# or Visual Basic .NET code by creating an assembly that contains one or more classes derived from the Windows Workflow FoundationCodeActivity class.
ms.custom: ''
ms.date: 09/12/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d4e6e932-61cd-42fd-a280-ef63bbad45f0
author: JimDaly
ms.author: kvivek
manager: kvivek
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ac933bcd17f0d34f34e6fa670a8165a49d8a1bb4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388113"
---
# <a name="custom-workflow-activities-workflow-assemblies"></a><span data-ttu-id="6aa49-104">Custom workflow activities (workflow assemblies)</span><span class="sxs-lookup"><span data-stu-id="6aa49-104">Custom workflow activities (workflow assemblies)</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] <span data-ttu-id="6aa49-105">apps support the registration and execution of custom workflow activities in addition to the out-of-box activities provided by [Windows Workflow Foundation](https://msdn.microsoft.com/netframework/aa663328.aspx).</span><span class="sxs-lookup"><span data-stu-id="6aa49-105">apps support the registration and execution of custom workflow activities in addition to the out-of-box activities provided by [Windows Workflow Foundation](https://msdn.microsoft.com/netframework/aa663328.aspx).</span></span> [!INCLUDE[pn_Windows_Workflow_Foundation](../includes/pn-windows-workflow-foundation.md)] <span data-ttu-id="6aa49-106">includes an [activity library](https://msdn.microsoft.com/library/dd489459.aspx) that provides activities for control flow, sending and receiving messages, doing work in parallel, and more.</span><span class="sxs-lookup"><span data-stu-id="6aa49-106">includes an [activity library](https://msdn.microsoft.com/library/dd489459.aspx) that provides activities for control flow, sending and receiving messages, doing work in parallel, and more.</span></span> <span data-ttu-id="6aa49-107">However, to build applications that satisfy your business needs, you may need activities that perform tasks specific to that application.</span><span class="sxs-lookup"><span data-stu-id="6aa49-107">However, to build applications that satisfy your business needs, you may need activities that perform tasks specific to that application.</span></span> <span data-ttu-id="6aa49-108">To make this possible, [!INCLUDE[pn_Windows_Workflow_Foundation](../includes/pn-windows-workflow-foundation.md)] supports the creation of custom workflow activities.</span><span class="sxs-lookup"><span data-stu-id="6aa49-108">To make this possible, [!INCLUDE[pn_Windows_Workflow_Foundation](../includes/pn-windows-workflow-foundation.md)] supports the creation of custom workflow activities.</span></span>  
  
 <span data-ttu-id="6aa49-109">You can write custom workflow activities in [!INCLUDE[pn_MS_Visual_C#](../includes/pn-ms-visual-csharp.md)] or [!INCLUDE[pn_Visual_Basic](../includes/pn-visual-basic.md)] code by creating an assembly that contains one or more classes derived from the [!INCLUDE[pn_Windows_Workflow_Foundation](../includes/pn-windows-workflow-foundation.md)] <xref:System.Activities.CodeActivity> class.</span><span class="sxs-lookup"><span data-stu-id="6aa49-109">You can write custom workflow activities in [!INCLUDE[pn_MS_Visual_C#](../includes/pn-ms-visual-csharp.md)] or [!INCLUDE[pn_Visual_Basic](../includes/pn-visual-basic.md)] code by creating an assembly that contains one or more classes derived from the [!INCLUDE[pn_Windows_Workflow_Foundation](../includes/pn-windows-workflow-foundation.md)] <xref:System.Activities.CodeActivity> class.</span></span> <span data-ttu-id="6aa49-110">This assembly is annotated with .NET attributes to provide the metadata that [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps uses at runtime to link your code to the workflow engine.</span><span class="sxs-lookup"><span data-stu-id="6aa49-110">This assembly is annotated with .NET attributes to provide the metadata that [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps uses at runtime to link your code to the workflow engine.</span></span>  
  
 <span data-ttu-id="6aa49-111">After you have created an assembly that contains one or more custom workflow activities, you register this assembly with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="6aa49-111">After you have created an assembly that contains one or more custom workflow activities, you register this assembly with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span></span> <span data-ttu-id="6aa49-112">This process is similar to registering a plug-in.</span><span class="sxs-lookup"><span data-stu-id="6aa49-112">This process is similar to registering a plug-in.</span></span> <span data-ttu-id="6aa49-113">The custom workflow activity can then be incorporated into a workflow or dialog in the `Process` form in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="6aa49-113">The custom workflow activity can then be incorporated into a workflow or dialog in the `Process` form in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span></span>  
  
> [!NOTE]
> [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] <span data-ttu-id="6aa49-114">only supports sandbox (partial trust) execution of custom workflow activities.</span><span class="sxs-lookup"><span data-stu-id="6aa49-114">only supports sandbox (partial trust) execution of custom workflow activities.</span></span> <span data-ttu-id="6aa49-115">On-premises [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps support execution of custom workflow activities in partial or full trust.</span><span class="sxs-lookup"><span data-stu-id="6aa49-115">On-premises [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps support execution of custom workflow activities in partial or full trust.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="6aa49-116">In This Section</span><span class="sxs-lookup"><span data-stu-id="6aa49-116">In This Section</span></span>  
 [<span data-ttu-id="6aa49-117">Creating a Custom Workflow Activity</span><span class="sxs-lookup"><span data-stu-id="6aa49-117">Creating a Custom Workflow Activity</span></span>](workflow/create-custom-workflow-activity.md)  
  
 [<span data-ttu-id="6aa49-118">Adding Metadata to the Custom Workflow Activity</span><span class="sxs-lookup"><span data-stu-id="6aa49-118">Adding Metadata to the Custom Workflow Activity</span></span>](workflow/add-metadata-custom-workflow-activity.md)  
  
 [<span data-ttu-id="6aa49-119">Using the Web Services within a Custom Workflow Activity</span><span class="sxs-lookup"><span data-stu-id="6aa49-119">Using the Web Services within a Custom Workflow Activity</span></span>](workflow/use-iorganization-web-service-custom-workflow-activity.md)  
  
 [<span data-ttu-id="6aa49-120">Registering the Workflow Assembly</span><span class="sxs-lookup"><span data-stu-id="6aa49-120">Registering the Workflow Assembly</span></span>](workflow/register-use-custom-workflow-activity-assembly.md)  
  
 [<span data-ttu-id="6aa49-121">Debugging a Custom Workflow Activity</span><span class="sxs-lookup"><span data-stu-id="6aa49-121">Debugging a Custom Workflow Activity</span></span>](workflow/debug-custom-workflow-activity.md)  
  
 [<span data-ttu-id="6aa49-122">Updating or Upgrading Custom Workflow Activity: Assembly Versioning</span><span class="sxs-lookup"><span data-stu-id="6aa49-122">Updating or Upgrading Custom Workflow Activity: Assembly Versioning</span></span>](workflow/update-custom-workflow-activity-using-assembly-versioning.md)  
  
 [<span data-ttu-id="6aa49-123">Process Classes, Attributes, and Dynamics 365 for Customer Engagement apps Type</span><span class="sxs-lookup"><span data-stu-id="6aa49-123">Process Classes, Attributes, and Dynamics 365 for Customer Engagement apps Type</span></span>](workflow/process-classes-attributes-and-types.md)  
  
 [<span data-ttu-id="6aa49-124">Sample: Create a custom workflow activity</span><span class="sxs-lookup"><span data-stu-id="6aa49-124">Sample: Create a custom workflow activity</span></span>](workflow/sample-create-custom-workflow-activity.md)  
  
 [<span data-ttu-id="6aa49-125">Sample: Update Next Birthday Using a Custom Workflow Activity</span><span class="sxs-lookup"><span data-stu-id="6aa49-125">Sample: Update Next Birthday Using a Custom Workflow Activity</span></span>](workflow/sample-update-next-birthday-using-custom-workflow-activity.md)  
  
 [<span data-ttu-id="6aa49-126">Sample: Calculate a Credit Score with a Custom Workflow Activity</span><span class="sxs-lookup"><span data-stu-id="6aa49-126">Sample: Calculate a Credit Score with a Custom Workflow Activity</span></span>](workflow/sample-calculate-credit-score-custom-workflow-activity.md)  
  
## <a name="related-sections"></a><span data-ttu-id="6aa49-127">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="6aa49-127">Related Sections</span></span>  
 [<span data-ttu-id="6aa49-128">Write Workflows to Automate Business Processes</span><span class="sxs-lookup"><span data-stu-id="6aa49-128">Write Workflows to Automate Business Processes</span></span>](automate-business-processes-customer-engagement.md)  
  
 [<span data-ttu-id="6aa49-129">Write Plug-Ins for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="6aa49-129">Write Plug-Ins for Dynamics 365 for Customer Engagement apps</span></span>](write-plugin-extend-business-processes.md)  
  
 [<span data-ttu-id="6aa49-130">Plug-in Isolation, Trusts, and Statistics</span><span class="sxs-lookup"><span data-stu-id="6aa49-130">Plug-in Isolation, Trusts, and Statistics</span></span>](plugin-isolation-trusts-statistics.md)
