---
title: 'Sample: Azure aware custom plug-in (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: The plug-in demonstrates how to obtain the execution context and the tracing service from the service provider parameter of the Execute method. The plug-in then posts the context to the Azure Service Bus endpoint and writes information to the trace log to facilitate debugging.
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
ms.assetid: 3a1fcf7e-1e86-4d55-b11f-38ee179b9f1d
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 37f9bf2bed61e77df8bef629401e1b85c25c65e2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386751"
---
# <a name="sample-azure-aware-custom-plug-in"></a><span data-ttu-id="47280-104">Sample: Azure aware custom plug-in</span><span class="sxs-lookup"><span data-stu-id="47280-104">Sample: Azure aware custom plug-in</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="47280-105">This is a sample custom plug-in that can post the pipeline execution context to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span><span class="sxs-lookup"><span data-stu-id="47280-105">This is a sample custom plug-in that can post the pipeline execution context to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span></span>  
  
 <span data-ttu-id="47280-106">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="47280-106">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="47280-107">Download the sample: [Work with Microsoft Dynamics 365 for Customer Engagement apps and Azure Integration](https://code.msdn.microsoft.com/Sample-Dynamics-365-and-6a95df2a)</span><span class="sxs-lookup"><span data-stu-id="47280-107">Download the sample: [Work with Microsoft Dynamics 365 for Customer Engagement apps and Azure Integration](https://code.msdn.microsoft.com/Sample-Dynamics-365-and-6a95df2a)</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="47280-108">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="47280-108">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="47280-109">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="47280-109">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="47280-110">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="47280-110">Demonstrates</span></span>  
 <span data-ttu-id="47280-111">The plug-in demonstrates how to obtain the execution context and the tracing service from the service provider parameter of the `Execute` method.</span><span class="sxs-lookup"><span data-stu-id="47280-111">The plug-in demonstrates how to obtain the execution context and the tracing service from the service provider parameter of the `Execute` method.</span></span> <span data-ttu-id="47280-112">The plug-in then posts the context to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] endpoint and writes information to the trace log to facilitate debugging.</span><span class="sxs-lookup"><span data-stu-id="47280-112">The plug-in then posts the context to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] endpoint and writes information to the trace log to facilitate debugging.</span></span>  
  
## <a name="example"></a><span data-ttu-id="47280-113">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="47280-113">Example</span></span>  
 [!code-csharp[WindowsAzure#SandboxPlugin](../snippets/csharp/CRMV8/windowsazure/cs/sandboxplugin.cs#sandboxplugin)]  
  
### <a name="see-also"></a><span data-ttu-id="47280-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="47280-114">See also</span></span>  
 <span data-ttu-id="47280-115">[Sample Code for Dynamics 365 for Customer Engagement apps and Microsoft Azure Integration](sample-code-azure-integration.md) </span><span class="sxs-lookup"><span data-stu-id="47280-115">[Sample Code for Dynamics 365 for Customer Engagement apps and Microsoft Azure Integration](sample-code-azure-integration.md) </span></span>  
 <span data-ttu-id="47280-116">[Sample: Azure Aware Custom Workflow Activity](sample-azure-aware-custom-workflow-activity.md) </span><span class="sxs-lookup"><span data-stu-id="47280-116">[Sample: Azure Aware Custom Workflow Activity](sample-azure-aware-custom-workflow-activity.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.IPlugin>   
 <xref:Microsoft.Xrm.Sdk.IPluginExecutionContext>   
 <xref:Microsoft.Xrm.Sdk.ITracingService>   
 [<span data-ttu-id="47280-117">Write a Plug-in</span><span class="sxs-lookup"><span data-stu-id="47280-117">Write a Plug-in</span></span>](write-plugin.md)
