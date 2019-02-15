---
title: Automate your business processes in Customer Engagement (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: 'Learn about automating your business processess. A business process can be of two types: automated processes that rely solely on communication among applications based on a set of rules, and interactive processes that also rely on people to initiate and run the process, and to make the appropriate decisions during the running of the process.'
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- process
- workflow
ms.assetid: 3ef415ed-d815-45de-8a7c-398b80d23cbd
caps.latest.revision: 51
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2703f9bf7cdd8a8919bd469564ba5cbada30f51b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386016"
---
# <a name="automate-your-business-processes-in-customer-engagement-apps"></a><span data-ttu-id="98128-104">Automate your business processes in Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="98128-104">Automate your business processes in Customer Engagement apps</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="98128-105">Business processes are an integral part of any enterprise software application.</span><span class="sxs-lookup"><span data-stu-id="98128-105">Business processes are an integral part of any enterprise software application.</span></span> <span data-ttu-id="98128-106">A business process can be of two types: *automated* processes that rely solely on communication among applications based on a set of rules, and *interactive* processes that also rely on people to initiate and run the process, and to make the appropriate decisions during the running of the process.</span><span class="sxs-lookup"><span data-stu-id="98128-106">A business process can be of two types: *automated* processes that rely solely on communication among applications based on a set of rules, and *interactive* processes that also rely on people to initiate and run the process, and to make the appropriate decisions during the running of the process.</span></span>  
<!-- TODO: Do you really mean online here?-->  
 <span data-ttu-id="98128-107">In [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps, a process enables you to create and manage your automated and interactive business processes.</span><span class="sxs-lookup"><span data-stu-id="98128-107">In [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps, a process enables you to create and manage your automated and interactive business processes.</span></span> <span data-ttu-id="98128-108">While the name has been changed from workflow to *process*, the entity that’s used to implement a process is still called *workflow*.</span><span class="sxs-lookup"><span data-stu-id="98128-108">While the name has been changed from workflow to *process*, the entity that’s used to implement a process is still called *workflow*.</span></span> <span data-ttu-id="98128-109">A [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps process provides many out-of-the-box components that business users and administrators can use to model their business processes.</span><span class="sxs-lookup"><span data-stu-id="98128-109">A [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps process provides many out-of-the-box components that business users and administrators can use to model their business processes.</span></span> [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="98128-110">apps also offers developers a mechanism to extend and customize the standard behavior of processes to achieve the functionality that their business applications require by allowing them to develop custom components.</span><span class="sxs-lookup"><span data-stu-id="98128-110">apps also offers developers a mechanism to extend and customize the standard behavior of processes to achieve the functionality that their business applications require by allowing them to develop custom components.</span></span>  
  
 <span data-ttu-id="98128-111">A [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps process is based on the [Windows Workflow Foundation](https://msdn.microsoft.com/netframework/aa663328.aspx) programming model.</span><span class="sxs-lookup"><span data-stu-id="98128-111">A [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps process is based on the [Windows Workflow Foundation](https://msdn.microsoft.com/netframework/aa663328.aspx) programming model.</span></span> 
[!INCLUDE[pn_Windows_Workflow_Foundation](../includes/pn-windows-workflow-foundation.md)] <span data-ttu-id="98128-112">provides a runtime engine, a framework, a base library of activities, and default implementations of the runtime services.</span><span class="sxs-lookup"><span data-stu-id="98128-112">provides a runtime engine, a framework, a base library of activities, and default implementations of the runtime services.</span></span> <span data-ttu-id="98128-113">The [!INCLUDE[pn_Windows_Workflow_Foundation](../includes/pn-windows-workflow-foundation.md)] runtime engine manages process execution, and supports processes that can remain active for extended periods of time.</span><span class="sxs-lookup"><span data-stu-id="98128-113">The [!INCLUDE[pn_Windows_Workflow_Foundation](../includes/pn-windows-workflow-foundation.md)] runtime engine manages process execution, and supports processes that can remain active for extended periods of time.</span></span> <span data-ttu-id="98128-114">It preserves the state of process execution during computer shutdown and restart.</span><span class="sxs-lookup"><span data-stu-id="98128-114">It preserves the state of process execution during computer shutdown and restart.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="98128-115">In This Section</span><span class="sxs-lookup"><span data-stu-id="98128-115">In This Section</span></span>  
 [<span data-ttu-id="98128-116">Choose a Process (Workflow) Type for Your Automation</span><span class="sxs-lookup"><span data-stu-id="98128-116">Choose a Process (Workflow) Type for Your Automation</span></span>](process-categories.md)  
  
 [<span data-ttu-id="98128-117">Process Architecture for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="98128-117">Process Architecture for Dynamics 365 for Customer Engagement apps</span></span>](process-architecture.md)  
  
 [<span data-ttu-id="98128-118">Workflow and Process Entities</span><span class="sxs-lookup"><span data-stu-id="98128-118">Workflow and Process Entities</span></span>](workflow-process-entities.md)  
  
 [<span data-ttu-id="98128-119">Supported Types, Triggers, and Entities for Process</span><span class="sxs-lookup"><span data-stu-id="98128-119">Supported Types, Triggers, and Entities for Process</span></span>](supported-types-triggers-entities-actions-processes.md)  
  
 [<span data-ttu-id="98128-120">Custom Workflow Activities (Workflow Assemblies)</span><span class="sxs-lookup"><span data-stu-id="98128-120">Custom Workflow Activities (Workflow Assemblies)</span></span>](custom-workflow-activities-workflow-assemblies.md) 
  
 [<span data-ttu-id="98128-121">Model the business process flow</span><span class="sxs-lookup"><span data-stu-id="98128-121">Model the business process flow</span></span>](model-business-process-flows.md)  
  
 [<span data-ttu-id="98128-122">Create real-time workflows</span><span class="sxs-lookup"><span data-stu-id="98128-122">Create real-time workflows</span></span>](create-real-time-workflows.md)  
  
 [<span data-ttu-id="98128-123">Create Your Own Custom Operations</span><span class="sxs-lookup"><span data-stu-id="98128-123">Create Your Own Custom Operations</span></span>](create-own-actions.md)  
  
 [<span data-ttu-id="98128-124">Use Dialogs in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="98128-124">Use Dialogs in Dynamics 365 for Customer Engagement apps</span></span>](use-dialogs-guided-processes.md)  
  
 [<span data-ttu-id="98128-125">Sample Code for Process and Workflow</span><span class="sxs-lookup"><span data-stu-id="98128-125">Sample Code for Process and Workflow</span></span>](sample-code-processes.md)  
  
## <a name="related-sections"></a><span data-ttu-id="98128-126">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="98128-126">Related Sections</span></span>  
 [<span data-ttu-id="98128-127">Software Development Kit for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="98128-127">Software Development Kit for Dynamics 365 for Customer Engagement apps</span></span>](developer-guide.md)  
  
 [<span data-ttu-id="98128-128">Write Plug-Ins for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="98128-128">Write Plug-Ins for Dynamics 365 for Customer Engagement apps</span></span>](write-plugin-extend-business-processes.md)  
  
 [<span data-ttu-id="98128-129">Understanding the Asynchronous Service</span><span class="sxs-lookup"><span data-stu-id="98128-129">Understanding the Asynchronous Service</span></span>](asynchronous-service.md)
