---
title: 'Sample: REST listener (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: 'The sample shows how to write a Azure Service Bus Listener for a REST endpoint contract. '
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
ms.assetid: db6a8899-9003-4ae0-b249-9fc31854583e
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8076d6f70d22d8789446edff6cbaaa6f86ce35fa
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387837"
---
# <a name="sample-rest-listener"></a>Sample: REST listener

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement. Download the sample: [Work with Microsoft Dynamics 365 for Customer Engagement apps and Azure Integration](https://code.msdn.microsoft.com/Sample-Dynamics-365-and-6a95df2a)
  
## <a name="requirements"></a>Yêu cầu  
 You must configure [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] integration with [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] prior to registering and executing this sample activity.  
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to write a [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] Listener for a REST endpoint contract.  
  
 This sample registers a remote service plug-in that executes whenever a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] message is posted to a REST endpoint on the service bus. When the plug-in executes, it prints to the console the contents of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] execution context contained in the message.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[WindowsAzure#RestListener](../snippets/csharp/CRMV8/windowsazure/cs/restlistener.cs#restlistener)]  
  
### <a name="see-also"></a>Xem thêm  
 [Configure Microsoft Azure Integration with Dynamics 365 for Customer Engagement apps](configure-azure-integration.md)   
 [Sample Code for Dynamics 365 for Customer Engagement and Microsoft Azure Integration](sample-code-azure-integration.md)   
 [Sample: Persistent Queue Listener](sample-persistent-queue-listener.md)   
 <xref:Microsoft.Xrm.Sdk.IWebHttpServiceEndpointPlugin>
