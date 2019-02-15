---
title: 'Sample: Two-way listener (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: 'The sample shows how to write a Azure Service Bus Listener for a two-way endpoint contract. '
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
ms.assetid: 6acfffff-0045-4a1c-a3d2-9906dd93845d
caps.latest.revision: 26
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 15c537f19472b7a483a2fd9559948db7b7e7007c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385923"
---
# <a name="sample-two-way-listener"></a><span data-ttu-id="3c2cd-103">Sample: Two-way listener</span><span class="sxs-lookup"><span data-stu-id="3c2cd-103">Sample: Two-way listener</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3c2cd-104">This sample registers a remote service plug-in that executes whenever a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement message is posted to a two-way endpoint on the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span><span class="sxs-lookup"><span data-stu-id="3c2cd-104">This sample registers a remote service plug-in that executes whenever a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement message is posted to a two-way endpoint on the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span></span> <span data-ttu-id="3c2cd-105">When the plug-in executes, it prints to the console the contents of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] execution context contained in the message.</span><span class="sxs-lookup"><span data-stu-id="3c2cd-105">When the plug-in executes, it prints to the console the contents of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] execution context contained in the message.</span></span> <span data-ttu-id="3c2cd-106">Download the sample: [Work with Microsoft Dynamics 365 for Customer Engagement apps and Azure Integration](https://code.msdn.microsoft.com/Sample-Dynamics-365-and-6a95df2a)</span><span class="sxs-lookup"><span data-stu-id="3c2cd-106">Download the sample: [Work with Microsoft Dynamics 365 for Customer Engagement apps and Azure Integration](https://code.msdn.microsoft.com/Sample-Dynamics-365-and-6a95df2a)</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="3c2cd-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="3c2cd-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="3c2cd-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="3c2cd-108">Requirements</span></span>  
 <span data-ttu-id="3c2cd-109">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="3c2cd-109">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> 
  
## <a name="demonstrates"></a><span data-ttu-id="3c2cd-110">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="3c2cd-110">Demonstrates</span></span>  
 <span data-ttu-id="3c2cd-111">This sample shows how to write a [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] Listener for a two-way endpoint contract.</span><span class="sxs-lookup"><span data-stu-id="3c2cd-111">This sample shows how to write a [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] Listener for a two-way endpoint contract.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3c2cd-112">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="3c2cd-112">Example</span></span>  
 [!code-csharp[WindowsAzure#TwoWayListener](../snippets/csharp/CRMV8/windowsazure/cs/twowaylistener.cs#twowaylistener)]  
  
### <a name="see-also"></a><span data-ttu-id="3c2cd-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3c2cd-113">See also</span></span>  
 <span data-ttu-id="3c2cd-114">[Azure Extentions for Dynamics 365 for Customer Engagement apps](azure-extensions.md) </span><span class="sxs-lookup"><span data-stu-id="3c2cd-114">[Azure Extentions for Dynamics 365 for Customer Engagement apps](azure-extensions.md) </span></span>  
 <span data-ttu-id="3c2cd-115">[Sample Code for Dynamics 365 for Customer Engagement apps and Microsoft Azure Integration](sample-code-azure-integration.md) </span><span class="sxs-lookup"><span data-stu-id="3c2cd-115">[Sample Code for Dynamics 365 for Customer Engagement apps and Microsoft Azure Integration](sample-code-azure-integration.md) </span></span>  
 <span data-ttu-id="3c2cd-116">[Sample: REST Listener](sample-rest-listener.md) </span><span class="sxs-lookup"><span data-stu-id="3c2cd-116">[Sample: REST Listener](sample-rest-listener.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.ITwoWayServiceEndpointPlugin>
