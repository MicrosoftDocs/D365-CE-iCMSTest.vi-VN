---
title: 'Sample: Azure aware custom workflow activity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample shows how to write a custom workflow activity that can post the data context from the current Dynamics 365 for Customer Engagement operation to the Azure Service Bus
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- azure
ms.assetid: 089bc521-c50e-4030-bcd1-7b71e0d34557
caps.latest.revision: 32
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c8611c0be08611ce5986e710b7fdf24cf68fc37a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386018"
---
# <a name="sample-azure-aware-custom-workflow-activity"></a>Sample: Azure aware custom workflow activity

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample obtains the data context from the current [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] for Customer Engagement apps operation and posts it to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].  
  
 This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the sample: [Work with Microsoft Dynamics 365 for Customer Engagement and Azure Integration](https://code.msdn.microsoft.com/Sample-Dynamics-365-and-6a95df2a)  

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
 You must configure [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to connect with [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] before registering and executing this sample custom workflow activity. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configure Microsoft Azure Integration with Dynamics 365 for Customer Engagement](configure-azure-integration.md).  
  
 Notice the “Input id” required argument in the code. When you add this activity to a workflow, you must provide the GUID of a [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] service endpoint.
  
 When registering this custom workflow activity with [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)], you must register it in the sandbox (partial trust).  
  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to write a custom workflow activity that can post the data context from the current [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] operation to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)]. The posting of the data context is done through the <xref:Microsoft.Xrm.Sdk.IServiceEndpointNotificationService.Execute(Microsoft.Xrm.Sdk.EntityReference,Microsoft.Xrm.Sdk.IExecutionContext)> method.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[WindowsAzure#AzureAwareWorkflowActivity](../snippets/csharp/CRMV8/windowsazure/cs/azureawareworkflowactivity.cs#azureawareworkflowactivity)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample Code for Dynamics 365 for Customer Engagement and Microsoft Azure Integration](sample-code-azure-integration.md)   
 [Sample: Persistent Queue Listener](sample-persistent-queue-listener.md)   
 [Custom Workflow Activities](custom-workflow-activities-workflow-assemblies.md)   
 <xref:Microsoft.Xrm.Sdk.IServiceEndpointNotificationService>
