---
title: Plug-in development (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: 'Learn more about how to develop plug-ins that can integrate with Dynamics 365 for Customer Engagement apps to modify or augment the standard behavior of the platform. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: aa037f4a-b5ae-485c-aac9-8a138a57c576
caps.latest.revision: 30
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ce9ebc7c9850b184a564d88e5160fbae2480d8ae
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385704"
---
# <a name="plug-in-development"></a><span data-ttu-id="1db1b-103">Plug-in development</span><span class="sxs-lookup"><span data-stu-id="1db1b-103">Plug-in development</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="1db1b-104">A plug-in is custom business logic (code) that you can integrate with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps to modify or augment the standard behavior of the platform.</span><span class="sxs-lookup"><span data-stu-id="1db1b-104">A plug-in is custom business logic (code) that you can integrate with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps to modify or augment the standard behavior of the platform.</span></span> <span data-ttu-id="1db1b-105">Another way to think about plug-ins is that they are handlers for events fired by [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="1db1b-105">Another way to think about plug-ins is that they are handlers for events fired by [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span></span> <span data-ttu-id="1db1b-106">You can subscribe, or register, a plug-in to a known set of events to have your code run when the event occurs.</span><span class="sxs-lookup"><span data-stu-id="1db1b-106">You can subscribe, or register, a plug-in to a known set of events to have your code run when the event occurs.</span></span>  
  
 <span data-ttu-id="1db1b-107">For more information about plug-in run-time execution, see [Event Execution Pipeline](event-execution-pipeline.md).</span><span class="sxs-lookup"><span data-stu-id="1db1b-107">For more information about plug-in run-time execution, see [Event Execution Pipeline](event-execution-pipeline.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="1db1b-108">In This Section</span><span class="sxs-lookup"><span data-stu-id="1db1b-108">In This Section</span></span>  
 [<span data-ttu-id="1db1b-109">Write a Plug-in</span><span class="sxs-lookup"><span data-stu-id="1db1b-109">Write a Plug-in</span></span>](write-plugin.md)  
  
 [<span data-ttu-id="1db1b-110">Understand the Data Context Passed to a Plug-in</span><span class="sxs-lookup"><span data-stu-id="1db1b-110">Understand the Data Context Passed to a Plug-in</span></span>](understand-data-context-passed-plugin.md)  
  
 [<span data-ttu-id="1db1b-111">Handle Exceptions in Plug-ins</span><span class="sxs-lookup"><span data-stu-id="1db1b-111">Handle Exceptions in Plug-ins</span></span>](handle-exceptions-plugins.md)  
  
 [<span data-ttu-id="1db1b-112">Passing Data Between Plug-ins</span><span class="sxs-lookup"><span data-stu-id="1db1b-112">Passing Data Between Plug-ins</span></span>](pass-data-between-plug-ins.md)  
  
 [<span data-ttu-id="1db1b-113">Impersonation in Plug-ins</span><span class="sxs-lookup"><span data-stu-id="1db1b-113">Impersonation in Plug-ins</span></span>](impersonation-plugins.md)  
  
 [<span data-ttu-id="1db1b-114">Register and Deploy Plug-ins</span><span class="sxs-lookup"><span data-stu-id="1db1b-114">Register and Deploy Plug-ins</span></span>](register-deploy-plugins.md)  
  
 [<span data-ttu-id="1db1b-115">Debug a Plug-in</span><span class="sxs-lookup"><span data-stu-id="1db1b-115">Debug a Plug-in</span></span>](debug-plugin.md)  
  
 [<span data-ttu-id="1db1b-116">Analyze Plug-in Performance</span><span class="sxs-lookup"><span data-stu-id="1db1b-116">Analyze Plug-in Performance</span></span>](analyze-plugin-performance.md)  
  
 [<span data-ttu-id="1db1b-117">Walkthrough: Register a Plug-in using the Plug-in Registration Tool</span><span class="sxs-lookup"><span data-stu-id="1db1b-117">Walkthrough: Register a Plug-in using the Plug-in Registration Tool</span></span>](walkthrough-register-plugin-using-plugin-registration-tool.md)  
  
 [<span data-ttu-id="1db1b-118">Walkthrough: Configure Assembly Security for an Offline Plug-in</span><span class="sxs-lookup"><span data-stu-id="1db1b-118">Walkthrough: Configure Assembly Security for an Offline Plug-in</span></span>](walkthrough-configure-assembly-security-offline-plugin.md)  
  
 [<span data-ttu-id="1db1b-119">Sample: Basic Plug-in</span><span class="sxs-lookup"><span data-stu-id="1db1b-119">Sample: Basic Plug-in</span></span>](sample-create-basic-plugin.md)  
  
 [<span data-ttu-id="1db1b-120">Sample: Web Access from a Sandboxed Plug-in</span><span class="sxs-lookup"><span data-stu-id="1db1b-120">Sample: Web Access from a Sandboxed Plug-in</span></span>](sample-web-access-sandboxed-plugin.md)  
  
## <a name="related-sections"></a><span data-ttu-id="1db1b-121">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="1db1b-121">Related Sections</span></span>  
 [<span data-ttu-id="1db1b-122">Write Plug-Ins to Extend Business Processes</span><span class="sxs-lookup"><span data-stu-id="1db1b-122">Write Plug-Ins to Extend Business Processes</span></span>](write-plugin-extend-business-processes.md)  
  
 [<span data-ttu-id="1db1b-123">Event Execution Pipeline</span><span class="sxs-lookup"><span data-stu-id="1db1b-123">Event Execution Pipeline</span></span>](event-execution-pipeline.md)  
  
 [<span data-ttu-id="1db1b-124">Web Service Authentication and Impersonation</span><span class="sxs-lookup"><span data-stu-id="1db1b-124">Web Service Authentication and Impersonation</span></span>](authenticate-users.md)
