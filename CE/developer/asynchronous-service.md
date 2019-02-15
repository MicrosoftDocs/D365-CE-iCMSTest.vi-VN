---
title: Asynchronous service in Dynamics 365 for Customer Engagement (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: Learn about the asynchronous service that executes long-running operations independent of the main Dynamics 365 for Customer Engagement (online) Customer Engagement core operation. The asynchronous service features a managed queue for the execution of asynchronous registered plug-ins, workflows, and operations such as bulk mail, bulk import, and campaign activity propagation.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1a668103-29aa-40d1-877a-263487ba3be1
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8e73c9612b2cd0566f074d91389e5aad0d46980a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387026"
---
# <a name="asynchronous-service-in-dynamics-365-for-customer-engagement"></a><span data-ttu-id="a0e5f-104">Asynchronous service in Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="a0e5f-104">Asynchronous service in Dynamics 365 for Customer Engagement</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a0e5f-105">The asynchronous service executes long-running operations independent of the main [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps core operation.</span><span class="sxs-lookup"><span data-stu-id="a0e5f-105">The asynchronous service executes long-running operations independent of the main [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps core operation.</span></span> <span data-ttu-id="a0e5f-106">This results in improved overall system performance and improved scalability.</span><span class="sxs-lookup"><span data-stu-id="a0e5f-106">This results in improved overall system performance and improved scalability.</span></span> <span data-ttu-id="a0e5f-107">The asynchronous service features a managed queue for the execution of asynchronous registered plug-ins, workflows, and operations such as bulk mail, bulk import, and campaign activity propagation.</span><span class="sxs-lookup"><span data-stu-id="a0e5f-107">The asynchronous service features a managed queue for the execution of asynchronous registered plug-ins, workflows, and operations such as bulk mail, bulk import, and campaign activity propagation.</span></span> <span data-ttu-id="a0e5f-108">These operations are registered with the asynchronous service and executed periodically when the service processes its queue.</span><span class="sxs-lookup"><span data-stu-id="a0e5f-108">These operations are registered with the asynchronous service and executed periodically when the service processes its queue.</span></span> <span data-ttu-id="a0e5f-109">The asynchronous service can be hosted on a server other that the server running [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="a0e5f-109">The asynchronous service can be hosted on a server other that the server running [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="a0e5f-110">In This Section</span><span class="sxs-lookup"><span data-stu-id="a0e5f-110">In This Section</span></span>  
 [<span data-ttu-id="a0e5f-111">Asynchronous Service Architecture</span><span class="sxs-lookup"><span data-stu-id="a0e5f-111">Asynchronous Service Architecture</span></span>](asynchronous-service-architecture.md)  
  
 [<span data-ttu-id="a0e5f-112">Asynchronous Operation (system job) Entity</span><span class="sxs-lookup"><span data-stu-id="a0e5f-112">Asynchronous Operation (system job) Entity</span></span>](asyncoperation-system-job-entity.md)  
  
 [<span data-ttu-id="a0e5f-113">Asynchronous Operation States</span><span class="sxs-lookup"><span data-stu-id="a0e5f-113">Asynchronous Operation States</span></span>](asynchronous-operation-states.md)  
  
 [<span data-ttu-id="a0e5f-114">Dependency and Execution Order in Asynchronous Operations</span><span class="sxs-lookup"><span data-stu-id="a0e5f-114">Dependency and Execution Order in Asynchronous Operations</span></span>](dependency-execution-order-asynchronous-operations.md)  
  
 [<span data-ttu-id="a0e5f-115">Recurrence Pattern in Asynchronous Job Execution</span><span class="sxs-lookup"><span data-stu-id="a0e5f-115">Recurrence Pattern in Asynchronous Job Execution</span></span>](recurrence-pattern-asynchronous-job-execution.md)  
  
 [<span data-ttu-id="a0e5f-116">Supported Entities for Asynchronous Operations</span><span class="sxs-lookup"><span data-stu-id="a0e5f-116">Supported Entities for Asynchronous Operations</span></span>](supported-entities-asynchronous-operations.md)  
  
 [<span data-ttu-id="a0e5f-117">Walkthrough: Stop and Start the Asynchronous Service</span><span class="sxs-lookup"><span data-stu-id="a0e5f-117">Walkthrough: Stop and Start the Asynchronous Service</span></span>](stop-start-asynchronous-service.md)  
  
## <a name="related-sections"></a><span data-ttu-id="a0e5f-118">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="a0e5f-118">Related Sections</span></span>  
 [<span data-ttu-id="a0e5f-119">AsyncOperation EntityType</span><span class="sxs-lookup"><span data-stu-id="a0e5f-119">AsyncOperation EntityType</span></span>](entities/asyncoperation.md) 

 [<span data-ttu-id="a0e5f-120">Event Execution Pipeline</span><span class="sxs-lookup"><span data-stu-id="a0e5f-120">Event Execution Pipeline</span></span>](event-execution-pipeline.md)  
  
 [<span data-ttu-id="a0e5f-121">Processes in Dynamics 365 for Customer Engagement apps (formerly Workflows)</span><span class="sxs-lookup"><span data-stu-id="a0e5f-121">Processes in Dynamics 365 for Customer Engagement apps (formerly Workflows)</span></span>](automate-business-processes-customer-engagement.md)  
  
 [<span data-ttu-id="a0e5f-122">Data Management in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="a0e5f-122">Data Management in Dynamics 365 for Customer Engagement apps</span></span>](manage-data.md)
