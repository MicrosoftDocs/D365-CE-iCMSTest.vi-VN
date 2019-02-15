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
# <a name="sample-rest-listener"></a><span data-ttu-id="3e101-103">Sample: REST listener</span><span class="sxs-lookup"><span data-stu-id="3e101-103">Sample: REST listener</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3e101-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="3e101-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="3e101-105">Download the sample: [Work with Microsoft Dynamics 365 for Customer Engagement apps and Azure Integration](https://code.msdn.microsoft.com/Sample-Dynamics-365-and-6a95df2a)</span><span class="sxs-lookup"><span data-stu-id="3e101-105">Download the sample: [Work with Microsoft Dynamics 365 for Customer Engagement apps and Azure Integration](https://code.msdn.microsoft.com/Sample-Dynamics-365-and-6a95df2a)</span></span>
  
## <a name="requirements"></a><span data-ttu-id="3e101-106">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="3e101-106">Requirements</span></span>  
 <span data-ttu-id="3e101-107">You must configure [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] integration with [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] prior to registering and executing this sample activity.</span><span class="sxs-lookup"><span data-stu-id="3e101-107">You must configure [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] integration with [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] prior to registering and executing this sample activity.</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="3e101-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="3e101-108">Demonstrates</span></span>  
 <span data-ttu-id="3e101-109">This sample shows how to write a [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] Listener for a REST endpoint contract.</span><span class="sxs-lookup"><span data-stu-id="3e101-109">This sample shows how to write a [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] Listener for a REST endpoint contract.</span></span>  
  
 <span data-ttu-id="3e101-110">This sample registers a remote service plug-in that executes whenever a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] message is posted to a REST endpoint on the service bus.</span><span class="sxs-lookup"><span data-stu-id="3e101-110">This sample registers a remote service plug-in that executes whenever a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] message is posted to a REST endpoint on the service bus.</span></span> <span data-ttu-id="3e101-111">When the plug-in executes, it prints to the console the contents of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] execution context contained in the message.</span><span class="sxs-lookup"><span data-stu-id="3e101-111">When the plug-in executes, it prints to the console the contents of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] execution context contained in the message.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3e101-112">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="3e101-112">Example</span></span>  
 [!code-csharp[WindowsAzure#RestListener](../snippets/csharp/CRMV8/windowsazure/cs/restlistener.cs#restlistener)]  
  
### <a name="see-also"></a><span data-ttu-id="3e101-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3e101-113">See also</span></span>  
 <span data-ttu-id="3e101-114">[Configure Microsoft Azure Integration with Dynamics 365 for Customer Engagement apps](configure-azure-integration.md) </span><span class="sxs-lookup"><span data-stu-id="3e101-114">[Configure Microsoft Azure Integration with Dynamics 365 for Customer Engagement apps](configure-azure-integration.md) </span></span>  
 <span data-ttu-id="3e101-115">[Sample Code for Dynamics 365 for Customer Engagement and Microsoft Azure Integration](sample-code-azure-integration.md) </span><span class="sxs-lookup"><span data-stu-id="3e101-115">[Sample Code for Dynamics 365 for Customer Engagement and Microsoft Azure Integration](sample-code-azure-integration.md) </span></span>  
 <span data-ttu-id="3e101-116">[Sample: Persistent Queue Listener](sample-persistent-queue-listener.md) </span><span class="sxs-lookup"><span data-stu-id="3e101-116">[Sample: Persistent Queue Listener](sample-persistent-queue-listener.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.IWebHttpServiceEndpointPlugin>
