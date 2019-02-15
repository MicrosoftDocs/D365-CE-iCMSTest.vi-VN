---
title: Work with Dynamics 365 for Customer Engagement data in your Azure solution (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: The ServiceBusPlugin plug-in contains the business logic to post the Dynamics 365 for Customer Engagement message execution context to the Azure Service Bus. To use this plug-in, you need to register a Azure Service Bus solution endpoint and a step for the plug-in. The step defines what message and entity combination being processed by the core Dynamics 365 for Customer Engagement operation should trigger the plug-in to execute. The ServiceBusPlugin can only be registered to run asynchronously.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: ccc4abde-9e4b-427a-a98c-c2b6bfce1195
caps.latest.revision: 30
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c6c040766e5d57d6d17d3e507c04de1a2847f80b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386558"
---
# <a name="work-with-customer-engagement-data-in-your-azure-solution"></a><span data-ttu-id="49093-106">Work with Customer Engagement data in your Azure solution</span><span class="sxs-lookup"><span data-stu-id="49093-106">Work with Customer Engagement data in your Azure solution</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="49093-107">An internal plug-in named ServiceBusPlugin is provided with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="49093-107">An internal plug-in named ServiceBusPlugin is provided with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="49093-108">The plug-in contains the business logic to post the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] message execution context to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span><span class="sxs-lookup"><span data-stu-id="49093-108">The plug-in contains the business logic to post the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] message execution context to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span></span> <span data-ttu-id="49093-109">To use this plug-in, you need to register a [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] solution endpoint and a step for the plug-in.</span><span class="sxs-lookup"><span data-stu-id="49093-109">To use this plug-in, you need to register a [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] solution endpoint and a step for the plug-in.</span></span> <span data-ttu-id="49093-110">The step defines what message and entity combination being processed by the core [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] operation should trigger the plug-in to execute.</span><span class="sxs-lookup"><span data-stu-id="49093-110">The step defines what message and entity combination being processed by the core [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] operation should trigger the plug-in to execute.</span></span> <span data-ttu-id="49093-111">The ServiceBusPlugin can only be registered to run asynchronously.</span><span class="sxs-lookup"><span data-stu-id="49093-111">The ServiceBusPlugin can only be registered to run asynchronously.</span></span> <span data-ttu-id="49093-112">For more information, see [Walkthrough: Register an Azure-aware Plug-in using the Plug-in Registration Tool](walkthrough-register-azure-aware-plug-in-using-plug-in-registration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="49093-112">For more information, see [Walkthrough: Register an Azure-aware Plug-in using the Plug-in Registration Tool](walkthrough-register-azure-aware-plug-in-using-plug-in-registration-tool.md).</span></span>  
  
 <span data-ttu-id="49093-113">In addition, you can write a custom plug-in that includes the required lines of code to post to the service bus.</span><span class="sxs-lookup"><span data-stu-id="49093-113">In addition, you can write a custom plug-in that includes the required lines of code to post to the service bus.</span></span> <span data-ttu-id="49093-114">The plug-in is registered in a similar way, except that it must be registered in the sandbox and run under partial trust.</span><span class="sxs-lookup"><span data-stu-id="49093-114">The plug-in is registered in a similar way, except that it must be registered in the sandbox and run under partial trust.</span></span> <span data-ttu-id="49093-115">For more information on writing a custom plug-in that can post to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)], see [Write a Custom Azure-aware Plug-in](write-custom-azure-aware-plugin.md).</span><span class="sxs-lookup"><span data-stu-id="49093-115">For more information on writing a custom plug-in that can post to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)], see [Write a Custom Azure-aware Plug-in](write-custom-azure-aware-plugin.md).</span></span>  
  
 <span data-ttu-id="49093-116">You can also write a custom workflow activity that can post the execution context to the service bus and include this activity in your workflows.</span><span class="sxs-lookup"><span data-stu-id="49093-116">You can also write a custom workflow activity that can post the execution context to the service bus and include this activity in your workflows.</span></span> <span data-ttu-id="49093-117">Sample code for a custom [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)]-aware workflow activity is provided in the topic [Sample: Azure Aware Custom Workflow Activity](sample-azure-aware-custom-workflow-activity.md).</span><span class="sxs-lookup"><span data-stu-id="49093-117">Sample code for a custom [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)]-aware workflow activity is provided in the topic [Sample: Azure Aware Custom Workflow Activity](sample-azure-aware-custom-workflow-activity.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="49093-118">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="49093-118">See also</span></span>  
 <span data-ttu-id="49093-119">[Walkthrough: Register a Plug-in using the Plug-in Registration Tool](walkthrough-register-plugin-using-plugin-registration-tool.md) </span><span class="sxs-lookup"><span data-stu-id="49093-119">[Walkthrough: Register a Plug-in using the Plug-in Registration Tool](walkthrough-register-plugin-using-plugin-registration-tool.md) </span></span>  
 <span data-ttu-id="49093-120">[Writing a Plug-in](write-plugin.md) </span><span class="sxs-lookup"><span data-stu-id="49093-120">[Writing a Plug-in](write-plugin.md) </span></span>  
 <span data-ttu-id="49093-121">[Plug-in Isolation, Trust, and Statistics](plugin-isolation-trusts-statistics.md) </span><span class="sxs-lookup"><span data-stu-id="49093-121">[Plug-in Isolation, Trust, and Statistics](plugin-isolation-trusts-statistics.md) </span></span>  
 <span data-ttu-id="49093-122">[Understand the Data Context Passed to a Plug-in](understand-data-context-passed-plugin.md) </span><span class="sxs-lookup"><span data-stu-id="49093-122">[Understand the Data Context Passed to a Plug-in](understand-data-context-passed-plugin.md) </span></span>  
 <span data-ttu-id="49093-123">[Registering Plug-ins](register-deploy-plugins.md) </span><span class="sxs-lookup"><span data-stu-id="49093-123">[Registering Plug-ins](register-deploy-plugins.md) </span></span>  
 <span data-ttu-id="49093-124">[Event Execution Pipeline](event-execution-pipeline.md) </span><span class="sxs-lookup"><span data-stu-id="49093-124">[Event Execution Pipeline](event-execution-pipeline.md) </span></span>  
 <span data-ttu-id="49093-125">[Azure Extensions for Dynamics 365 for Customer Engagement apps](azure-extensions.md) </span><span class="sxs-lookup"><span data-stu-id="49093-125">[Azure Extensions for Dynamics 365 for Customer Engagement apps](azure-extensions.md) </span></span>  
 [<span data-ttu-id="49093-126">ServiceEndPoint Entity</span><span class="sxs-lookup"><span data-stu-id="49093-126">ServiceEndPoint Entity</span></span>](entities/serviceendpoint.md)
