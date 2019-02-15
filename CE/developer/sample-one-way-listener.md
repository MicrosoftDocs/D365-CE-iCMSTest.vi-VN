---
title: 'Sample: One-way listener (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: 'The sample shows how to write a Azure Service Bus listener for a one-way endpoint contract. '
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
ms.assetid: 643ea291-1830-4448-b9bf-26744077721a
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6d4bdc0c640d466d4d714c57a1d0c90e2d2eada3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387401"
---
# <a name="sample-one-way-listener"></a><span data-ttu-id="0e643-103">Sample: One-way listener</span><span class="sxs-lookup"><span data-stu-id="0e643-103">Sample: One-way listener</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="0e643-104">This sample listener application registers a remote service plug-in that executes whenever a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement message is posted to a one-way endpoint on the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span><span class="sxs-lookup"><span data-stu-id="0e643-104">This sample listener application registers a remote service plug-in that executes whenever a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement message is posted to a one-way endpoint on the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span></span> <span data-ttu-id="0e643-105">When the plug-in executes, it outputs to the console the contents of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] execution context contained in the message.</span><span class="sxs-lookup"><span data-stu-id="0e643-105">When the plug-in executes, it outputs to the console the contents of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] execution context contained in the message.</span></span> <span data-ttu-id="0e643-106">Download the sample: [Work with Microsoft Dynamics 365 for Customer Engagement and Azure Integration](https://code.msdn.microsoft.com/Sample-Dynamics-365-and-6a95df2a)</span><span class="sxs-lookup"><span data-stu-id="0e643-106">Download the sample: [Work with Microsoft Dynamics 365 for Customer Engagement and Azure Integration](https://code.msdn.microsoft.com/Sample-Dynamics-365-and-6a95df2a)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0e643-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="0e643-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="0e643-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="0e643-108">Requirements</span></span>  
 <span data-ttu-id="0e643-109">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] and [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="0e643-109">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] and [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)].</span></span> 
  
## <a name="demonstrates"></a><span data-ttu-id="0e643-110">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="0e643-110">Demonstrates</span></span>  
 <span data-ttu-id="0e643-111">This sample shows how to write a [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] listener for a one-way endpoint contract.</span><span class="sxs-lookup"><span data-stu-id="0e643-111">This sample shows how to write a [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] listener for a one-way endpoint contract.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0e643-112">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="0e643-112">Example</span></span>  
 [!code-csharp[WindowsAzure#OneWayListener](../snippets/csharp/CRMV8/windowsazure/cs/onewaylistener.cs#onewaylistener)]  
  
### <a name="see-also"></a><span data-ttu-id="0e643-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="0e643-113">See also</span></span>  
 <span data-ttu-id="0e643-114">[Sample Code for Dynamics 365 for Customer Engagement apps and Microsoft Azure Integration](sample-code-azure-integration.md) </span><span class="sxs-lookup"><span data-stu-id="0e643-114">[Sample Code for Dynamics 365 for Customer Engagement apps and Microsoft Azure Integration](sample-code-azure-integration.md) </span></span>  
 <span data-ttu-id="0e643-115">[Sample: Two-way Listener](sample-two-way-listener.md) </span><span class="sxs-lookup"><span data-stu-id="0e643-115">[Sample: Two-way Listener](sample-two-way-listener.md) </span></span>  
 <span data-ttu-id="0e643-116">[Write a One-way, Two-way, or REST Listener](write-listener-application-azure-solution.md#bkmk_writeoneway) </span><span class="sxs-lookup"><span data-stu-id="0e643-116">[Write a One-way, Two-way, or REST Listener](write-listener-application-azure-solution.md#bkmk_writeoneway) </span></span>  
 <xref:Microsoft.Xrm.Sdk.IServiceEndpointPlugin>
