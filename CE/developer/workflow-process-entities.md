---
title: Workflow and process entities (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: The Dynamics 365 for Customer Engagement workflow object model is a set of classes that uses the Windows Workflow Foundation object model and exposes Dynamics 365 for Customer Engagement workflow activities. These classes are found in the Microsoft.Xrm.Sdk.Workflow assembly.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1b40f46a-31f1-4c2a-8e50-f3641b8d8973
caps.latest.revision: 20
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 95ac8160da45206cca50ef7ce302ae876b3f948b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385476"
---
# <a name="workflow-and-process-entities"></a><span data-ttu-id="59a3e-104">Workflow and process entities</span><span class="sxs-lookup"><span data-stu-id="59a3e-104">Workflow and process entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="59a3e-105">The [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps workflow object model is a set of classes that uses the [!INCLUDE[pn_Windows_Workflow_Foundation](../includes/pn-windows-workflow-foundation.md)] object model and exposes [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps workflow activities.</span><span class="sxs-lookup"><span data-stu-id="59a3e-105">The [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps workflow object model is a set of classes that uses the [!INCLUDE[pn_Windows_Workflow_Foundation](../includes/pn-windows-workflow-foundation.md)] object model and exposes [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps workflow activities.</span></span> <span data-ttu-id="59a3e-106">These classes are found in the `Microsoft.Xrm.Sdk.Workflow` assembly.</span><span class="sxs-lookup"><span data-stu-id="59a3e-106">These classes are found in the `Microsoft.Xrm.Sdk.Workflow` assembly.</span></span> <span data-ttu-id="59a3e-107">Để biết thêm thông tin, xem <xref:Microsoft.Xrm.Sdk.Workflow>.</span><span class="sxs-lookup"><span data-stu-id="59a3e-107">For more information, see <xref:Microsoft.Xrm.Sdk.Workflow>.</span></span>

 <span data-ttu-id="59a3e-108">Workflow activities are the elemental units of a workflow (process).</span><span class="sxs-lookup"><span data-stu-id="59a3e-108">Workflow activities are the elemental units of a workflow (process).</span></span> <span data-ttu-id="59a3e-109">They are added to a workflow (process) to form a hierarchical tree structure.</span><span class="sxs-lookup"><span data-stu-id="59a3e-109">They are added to a workflow (process) to form a hierarchical tree structure.</span></span> <span data-ttu-id="59a3e-110">When all activities in a given path are finished running, the workflow (process) instance is completed.</span><span class="sxs-lookup"><span data-stu-id="59a3e-110">When all activities in a given path are finished running, the workflow (process) instance is completed.</span></span>

 <span data-ttu-id="59a3e-111">The workflow entity stores the definition of a workflow (process).</span><span class="sxs-lookup"><span data-stu-id="59a3e-111">The workflow entity stores the definition of a workflow (process).</span></span> <span data-ttu-id="59a3e-112">This definition contains the XAML string that describes the workflow activity, and also the rules used in the process.</span><span class="sxs-lookup"><span data-stu-id="59a3e-112">This definition contains the XAML string that describes the workflow activity, and also the rules used in the process.</span></span>

 <span data-ttu-id="59a3e-113">The validity of a workflow definition may depend on external data.</span><span class="sxs-lookup"><span data-stu-id="59a3e-113">The validity of a workflow definition may depend on external data.</span></span> <span data-ttu-id="59a3e-114">There are several types of dependencies that are supported:</span><span class="sxs-lookup"><span data-stu-id="59a3e-114">There are several types of dependencies that are supported:</span></span>

 |<span data-ttu-id="59a3e-115">Dependency</span><span class="sxs-lookup"><span data-stu-id="59a3e-115">Dependency</span></span> |<span data-ttu-id="59a3e-116">Mô tả</span><span class="sxs-lookup"><span data-stu-id="59a3e-116">Description</span></span>|
 |-----------|-----------|
 |<span data-ttu-id="59a3e-117">SDK operation</span><span class="sxs-lookup"><span data-stu-id="59a3e-117">SDK operation</span></span>|<span data-ttu-id="59a3e-118">If a process is triggered on a specific SDK operation, it cannot be deleted.</span><span class="sxs-lookup"><span data-stu-id="59a3e-118">If a process is triggered on a specific SDK operation, it cannot be deleted.</span></span>|
 |<span data-ttu-id="59a3e-119">Input entity</span><span class="sxs-lookup"><span data-stu-id="59a3e-119">Input entity</span></span>|<span data-ttu-id="59a3e-120">A process depends on a snapshot of a record passed in to the workflow.</span><span class="sxs-lookup"><span data-stu-id="59a3e-120">A process depends on a snapshot of a record passed in to the workflow.</span></span>|
 |<span data-ttu-id="59a3e-121">Local parameter</span><span class="sxs-lookup"><span data-stu-id="59a3e-121">Local parameter</span></span>|<span data-ttu-id="59a3e-122">A formal description of a .NET property to be defined by the process type.</span><span class="sxs-lookup"><span data-stu-id="59a3e-122">A formal description of a .NET property to be defined by the process type.</span></span>|

<span data-ttu-id="59a3e-123">The workflow log entity contains detailed information about logical steps completed during the execution of a workflow.</span><span class="sxs-lookup"><span data-stu-id="59a3e-123">The workflow log entity contains detailed information about logical steps completed during the execution of a workflow.</span></span> <span data-ttu-id="59a3e-124">Similarly, the process session entity contains information about the running of a dialog.</span><span class="sxs-lookup"><span data-stu-id="59a3e-124">Similarly, the process session entity contains information about the running of a dialog.</span></span>

<span data-ttu-id="59a3e-125">If a workflow was created in the web application and the workflow definition has the `Workflow.AsyncAutoDelete` attribute set to true, and the workflow has a single step in it that is not a Stage/Wait/Condition step,  no `WorkflowLog` records will be created.</span><span class="sxs-lookup"><span data-stu-id="59a3e-125">If a workflow was created in the web application and the workflow definition has the `Workflow.AsyncAutoDelete` attribute set to true, and the workflow has a single step in it that is not a Stage/Wait/Condition step,  no `WorkflowLog` records will be created.</span></span> <span data-ttu-id="59a3e-126">This is an platform optimization  to improve performance and save disk space.</span><span class="sxs-lookup"><span data-stu-id="59a3e-126">This is an platform optimization  to improve performance and save disk space.</span></span>  

<span data-ttu-id="59a3e-127">There are two messages you can use to work with processes.</span><span class="sxs-lookup"><span data-stu-id="59a3e-127">There are two messages you can use to work with processes.</span></span> <span data-ttu-id="59a3e-128"><xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> is used to set the state of the process: draft or activated.</span><span class="sxs-lookup"><span data-stu-id="59a3e-128"><xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> is used to set the state of the process: draft or activated.</span></span> <span data-ttu-id="59a3e-129"><xref:Microsoft.Crm.Sdk.Messages.CreateWorkflowFromTemplateRequest> is used to create a process from a process template.</span><span class="sxs-lookup"><span data-stu-id="59a3e-129"><xref:Microsoft.Crm.Sdk.Messages.CreateWorkflowFromTemplateRequest> is used to create a process from a process template.</span></span>

### <a name="see-also"></a><span data-ttu-id="59a3e-130">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="59a3e-130">See also</span></span>

 [<span data-ttu-id="59a3e-131">Supported Types, Triggers, and Entities for Processes</span><span class="sxs-lookup"><span data-stu-id="59a3e-131">Supported Types, Triggers, and Entities for Processes</span></span>](supported-types-triggers-entities-actions-processes.md)<br />
 [<span data-ttu-id="59a3e-132">Processes in Dynamics 365 for Customer Engagement apps(formerly Workflows)</span><span class="sxs-lookup"><span data-stu-id="59a3e-132">Processes in Dynamics 365 for Customer Engagement apps(formerly Workflows)</span></span>](automate-business-processes-customer-engagement.md)<br />
 [<span data-ttu-id="59a3e-133">WorkFlow Entity</span><span class="sxs-lookup"><span data-stu-id="59a3e-133">WorkFlow Entity</span></span>](entities/workflow.md)<br />
 [<span data-ttu-id="59a3e-134">WorkFlowLog Entity</span><span class="sxs-lookup"><span data-stu-id="59a3e-134">WorkFlowLog Entity</span></span>](entities/workflowlog.md)<br />
  <!-- Bug 700905 
 [ProcessSession Entity](entities/processsession.md)
 -->
