---
title: Azure extensions for Dynamics 365 for Customer Engagement (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: Dynamics 365 for Customer Engagement apps can be integrated with Microsoft Azure. Developers can register plug-ins with Dynamics 365 for Customer Engagement apps that can pass run-time message data, to one or more Microsoft Azure solutions in the cloud.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- azure
- appfabric
ms.assetid: 70140156-f6b5-4cae-846c-23009ed755b2
caps.latest.revision: 56
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8fe713eee66d402bb5aaf6cf6fdf69eb6fdb78eb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386373"
---
# <a name="azure-extensions-for-dynamics-365-for-customer-engagement-apps"></a><span data-ttu-id="f9f28-104">Azure extensions for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="f9f28-104">Azure extensions for Dynamics 365 for Customer Engagement apps</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] <span data-ttu-id="f9f28-105">apps supports integration with [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)].</span><span class="sxs-lookup"><span data-stu-id="f9f28-105">apps supports integration with [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)].</span></span> <span data-ttu-id="f9f28-106">Developers can register plug-ins with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps that can pass run-time message data, known as the execution context, to one or more [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] solutions in the cloud.</span><span class="sxs-lookup"><span data-stu-id="f9f28-106">Developers can register plug-ins with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps that can pass run-time message data, known as the execution context, to one or more [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] solutions in the cloud.</span></span> <span data-ttu-id="f9f28-107">This is especially important for [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps because [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] is one of two supported solutions for communicating run-time context obtained in a plug-in to external line-of-business (LOB) applications.</span><span class="sxs-lookup"><span data-stu-id="f9f28-107">This is especially important for [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps because [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] is one of two supported solutions for communicating run-time context obtained in a plug-in to external line-of-business (LOB) applications.</span></span> <span data-ttu-id="f9f28-108">The other solution is the external custom endpoint access capability from a plug-in registered in the sandbox.</span><span class="sxs-lookup"><span data-stu-id="f9f28-108">The other solution is the external custom endpoint access capability from a plug-in registered in the sandbox.</span></span>  
  
 <span data-ttu-id="f9f28-109">The [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] provides a secure communication channel for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps run-time data to external line of business applications.</span><span class="sxs-lookup"><span data-stu-id="f9f28-109">The [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] provides a secure communication channel for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps run-time data to external line of business applications.</span></span> <span data-ttu-id="f9f28-110">This capability is especially useful in keeping disparate [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps system or other [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server synchronized with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] business data changes.</span><span class="sxs-lookup"><span data-stu-id="f9f28-110">This capability is especially useful in keeping disparate [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps system or other [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server synchronized with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] business data changes.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f9f28-111">In This Section</span><span class="sxs-lookup"><span data-stu-id="f9f28-111">In This Section</span></span>  
 [<span data-ttu-id="f9f28-112">Azure integration with Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="f9f28-112">Azure integration with Dynamics 365 for Customer Engagement apps</span></span>](azure-integration.md)  
  
 [<span data-ttu-id="f9f28-113">Configure Microsoft Azure Integration with Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="f9f28-113">Configure Microsoft Azure Integration with Dynamics 365 for Customer Engagement apps</span></span>](configure-azure-integration.md)  
  
 [<span data-ttu-id="f9f28-114">Work with Dynamics 365 for Customer Engagement apps data in your Azure solution</span><span class="sxs-lookup"><span data-stu-id="f9f28-114">Work with Dynamics 365 for Customer Engagement apps data in your Azure solution</span></span>](work-data-azure-solution.md)  
  
 [<span data-ttu-id="f9f28-115">Work with Dynamics 365 for Customer Engagement apps event data in your Azure Event Hub solution</span><span class="sxs-lookup"><span data-stu-id="f9f28-115">Work with Dynamics 365 for Customer Engagement apps event data in your Azure Event Hub solution</span></span>](work-event-data-azure-event-hub-solution.md)  
  
 [<span data-ttu-id="f9f28-116">Write a Custom Azure-aware Plug-in</span><span class="sxs-lookup"><span data-stu-id="f9f28-116">Write a Custom Azure-aware Plug-in</span></span>](write-custom-azure-aware-plugin.md)  
  
 [<span data-ttu-id="f9f28-117">Write a Listener for a Microsoft Azure Solution</span><span class="sxs-lookup"><span data-stu-id="f9f28-117">Write a Listener for a Microsoft Azure Solution</span></span>](write-listener-application-azure-solution.md)  
  
 [<span data-ttu-id="f9f28-118">Walkthrough: Configure Microsoft Azure (SAS) for integration with Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="f9f28-118">Walkthrough: Configure Microsoft Azure (SAS) for integration with Dynamics 365 for Customer Engagement apps</span></span>](walkthrough-configure-azure-sas-integration.md)  
  
 [<span data-ttu-id="f9f28-119">Walkthrough: Register an Azure-aware Plug-in with Plug-in Registration Tool</span><span class="sxs-lookup"><span data-stu-id="f9f28-119">Walkthrough: Register an Azure-aware Plug-in with Plug-in Registration Tool</span></span>](walkthrough-register-azure-aware-plug-in-using-plug-in-registration-tool.md)  
 [<span data-ttu-id="f9f28-120">Walkthrough: Update a service endpoint from ACS to SAS authorization</span><span class="sxs-lookup"><span data-stu-id="f9f28-120">Walkthrough: Update a service endpoint from ACS to SAS authorization</span></span>](walkthrough-update-service-endpoint-acs-sas-authorization.md)  
  
 [<span data-ttu-id="f9f28-121">Walkthrough: Update a service endpoint imported from a solution</span><span class="sxs-lookup"><span data-stu-id="f9f28-121">Walkthrough: Update a service endpoint imported from a solution</span></span>](walkthrough-update-service-endpoint-imported-solution.md)  
  
 [<span data-ttu-id="f9f28-122">Sample Code for Dynamics 365 for Customer Engagement apps-Azure Integration</span><span class="sxs-lookup"><span data-stu-id="f9f28-122">Sample Code for Dynamics 365 for Customer Engagement apps-Azure Integration</span></span>](sample-code-azure-integration.md)  
  
## <a name="related-sections"></a><span data-ttu-id="f9f28-123">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="f9f28-123">Related Sections</span></span>  
 [<span data-ttu-id="f9f28-124">Plug-ins for Extending Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="f9f28-124">Plug-ins for Extending Dynamics 365 for Customer Engagement apps</span></span>](write-plugin-extend-business-processes.md)  
  
 [<span data-ttu-id="f9f28-125">Microsoft Azure Platform Developer Center</span><span class="sxs-lookup"><span data-stu-id="f9f28-125">Microsoft Azure Platform Developer Center</span></span>](https://msdn.microsoft.com/azure/default.aspx)  
  
 [<span data-ttu-id="f9f28-126">Microsoft Azure Service Bus</span><span class="sxs-lookup"><span data-stu-id="f9f28-126">Microsoft Azure Service Bus</span></span>](http://www.windowsazure.com/develop/net/fundamentals/hybrid-solutions/)
