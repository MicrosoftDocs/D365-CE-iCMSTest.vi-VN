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
# <a name="work-with-customer-engagement-data-in-your-azure-solution"></a>Work with Customer Engagement data in your Azure solution

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

An internal plug-in named ServiceBusPlugin is provided with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement. The plug-in contains the business logic to post the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] message execution context to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)]. To use this plug-in, you need to register a [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] solution endpoint and a step for the plug-in. The step defines what message and entity combination being processed by the core [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] operation should trigger the plug-in to execute. The ServiceBusPlugin can only be registered to run asynchronously. For more information, see [Walkthrough: Register an Azure-aware Plug-in using the Plug-in Registration Tool](walkthrough-register-azure-aware-plug-in-using-plug-in-registration-tool.md).  
  
 In addition, you can write a custom plug-in that includes the required lines of code to post to the service bus. The plug-in is registered in a similar way, except that it must be registered in the sandbox and run under partial trust. For more information on writing a custom plug-in that can post to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)], see [Write a Custom Azure-aware Plug-in](write-custom-azure-aware-plugin.md).  
  
 You can also write a custom workflow activity that can post the execution context to the service bus and include this activity in your workflows. Sample code for a custom [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)]-aware workflow activity is provided in the topic [Sample: Azure Aware Custom Workflow Activity](sample-azure-aware-custom-workflow-activity.md).  
  
### <a name="see-also"></a>Xem thêm  
 [Walkthrough: Register a Plug-in using the Plug-in Registration Tool](walkthrough-register-plugin-using-plugin-registration-tool.md)   
 [Writing a Plug-in](write-plugin.md)   
 [Plug-in Isolation, Trust, and Statistics](plugin-isolation-trusts-statistics.md)   
 [Understand the Data Context Passed to a Plug-in](understand-data-context-passed-plugin.md)   
 [Registering Plug-ins](register-deploy-plugins.md)   
 [Event Execution Pipeline](event-execution-pipeline.md)   
 [Azure Extensions for Dynamics 365 for Customer Engagement apps](azure-extensions.md)   
 [ServiceEndPoint Entity](entities/serviceendpoint.md)
