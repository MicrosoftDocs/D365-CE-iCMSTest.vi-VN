---
title: Introduction to the event framework (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Event framework enables your custom code to be developed and integrated into Dynamics 365 for Customer Engagement server
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 6116dde0-c6f5-4858-a4f9-93ccf495d39a
caps.latest.revision: 27
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f15e28e0c92ba026c0ea67a5a6748ce6eac2ef08
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385540"
---
# <a name="introduction-to-the-event-framework"></a><span data-ttu-id="2ad1a-103">Introduction to the event framework</span><span class="sxs-lookup"><span data-stu-id="2ad1a-103">Introduction to the event framework</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="2ad1a-104">With [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps you have the ability to extend or customize the functionality of the server through the integration of custom business logic (code).</span><span class="sxs-lookup"><span data-stu-id="2ad1a-104">With [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps you have the ability to extend or customize the functionality of the server through the integration of custom business logic (code).</span></span> <span data-ttu-id="2ad1a-105">You can customize the product to support the way your company does business, and you can add new features to the product.</span><span class="sxs-lookup"><span data-stu-id="2ad1a-105">You can customize the product to support the way your company does business, and you can add new features to the product.</span></span> <span data-ttu-id="2ad1a-106">The technology that enables your custom code to be developed and integrated into the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps server is called the *event framework*.</span><span class="sxs-lookup"><span data-stu-id="2ad1a-106">The technology that enables your custom code to be developed and integrated into the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps server is called the *event framework*.</span></span>  
  
 <span data-ttu-id="2ad1a-107">The event framework enables you to create rich vertical and horizontal solutions on top of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps by supporting the development and integration of custom business logic with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps in a reliable and portable way.</span><span class="sxs-lookup"><span data-stu-id="2ad1a-107">The event framework enables you to create rich vertical and horizontal solutions on top of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps by supporting the development and integration of custom business logic with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps in a reliable and portable way.</span></span> <span data-ttu-id="2ad1a-108">After your custom business logic has been integrated into [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps, it can be executed synchronously as part of the main [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps execution path, or asynchronously from a managed queue.</span><span class="sxs-lookup"><span data-stu-id="2ad1a-108">After your custom business logic has been integrated into [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps, it can be executed synchronously as part of the main [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps execution path, or asynchronously from a managed queue.</span></span> <span data-ttu-id="2ad1a-109">Business data can be passed to your custom code, which can then perform actions based on the nature of the information, or modify the information itself.</span><span class="sxs-lookup"><span data-stu-id="2ad1a-109">Business data can be passed to your custom code, which can then perform actions based on the nature of the information, or modify the information itself.</span></span>  
  
 <span data-ttu-id="2ad1a-110">The Event Framework provides the following key features:</span><span class="sxs-lookup"><span data-stu-id="2ad1a-110">The Event Framework provides the following key features:</span></span>  
  
- <span data-ttu-id="2ad1a-111">An **improved event processing subsystem**.</span><span class="sxs-lookup"><span data-stu-id="2ad1a-111">An **improved event processing subsystem**.</span></span> <span data-ttu-id="2ad1a-112">This subsystem provides a unified method of executing both plug-ins and workflow activities, which results in improved reliability, an enhanced feature set, and plug-in portability.</span><span class="sxs-lookup"><span data-stu-id="2ad1a-112">This subsystem provides a unified method of executing both plug-ins and workflow activities, which results in improved reliability, an enhanced feature set, and plug-in portability.</span></span>  
  
- <span data-ttu-id="2ad1a-113">An **event framework API** for extending the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps platform through the development of custom business logic in the form of plug-ins and workflow activities.</span><span class="sxs-lookup"><span data-stu-id="2ad1a-113">An **event framework API** for extending the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps platform through the development of custom business logic in the form of plug-ins and workflow activities.</span></span>  
  
- <span data-ttu-id="2ad1a-114">An API for the **deployment of plug-ins and custom workflow activities** to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps database.</span><span class="sxs-lookup"><span data-stu-id="2ad1a-114">An API for the **deployment of plug-ins and custom workflow activities** to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps database.</span></span> <span data-ttu-id="2ad1a-115">Deployment of plug-ins and workflow activities to the database enables automatic distribution of your plug-ins and custom workflow activities to servers running [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] services throughout a datacenter.</span><span class="sxs-lookup"><span data-stu-id="2ad1a-115">Deployment of plug-ins and workflow activities to the database enables automatic distribution of your plug-ins and custom workflow activities to servers running [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] services throughout a datacenter.</span></span>  
  
- <span data-ttu-id="2ad1a-116">**Synchronous and asynchronous execution of plug-ins**. Synchronous plug-ins are executed in a pre-defined order as part of the main [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps event processing.</span><span class="sxs-lookup"><span data-stu-id="2ad1a-116">**Synchronous and asynchronous execution of plug-ins**. Synchronous plug-ins are executed in a pre-defined order as part of the main [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps event processing.</span></span> <span data-ttu-id="2ad1a-117">Asynchronous plug-ins are queued and executed independently.</span><span class="sxs-lookup"><span data-stu-id="2ad1a-117">Asynchronous plug-ins are queued and executed independently.</span></span>  
  
  <span data-ttu-id="2ad1a-118">The Event Framework is only supported on the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server and the [!INCLUDE[pn_MS_Outlook_Short](../includes/pn-ms-outlook-short.md)] client.</span><span class="sxs-lookup"><span data-stu-id="2ad1a-118">The Event Framework is only supported on the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server and the [!INCLUDE[pn_MS_Outlook_Short](../includes/pn-ms-outlook-short.md)] client.</span></span> <span data-ttu-id="2ad1a-119">For more information about how to extend the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Web application, see [Customize Dynamics 365 for Customer Engagement](customize-dev/customize-applications.md).</span><span class="sxs-lookup"><span data-stu-id="2ad1a-119">For more information about how to extend the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Web application, see [Customize Dynamics 365 for Customer Engagement](customize-dev/customize-applications.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="2ad1a-120">In This Section</span><span class="sxs-lookup"><span data-stu-id="2ad1a-120">In This Section</span></span>  
 [<span data-ttu-id="2ad1a-121">Event Execution Pipeline</span><span class="sxs-lookup"><span data-stu-id="2ad1a-121">Event Execution Pipeline</span></span>](event-execution-pipeline.md)  
  
 [<span data-ttu-id="2ad1a-122">Plug-in Isolation, Trust, and the Disallowed List</span><span class="sxs-lookup"><span data-stu-id="2ad1a-122">Plug-in Isolation, Trust, and the Disallowed List</span></span>](plugin-isolation-trusts-statistics.md)  
  
## <a name="related-sections"></a><span data-ttu-id="2ad1a-123">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="2ad1a-123">Related Sections</span></span>  
 [<span data-ttu-id="2ad1a-124">Write Plug-Ins to Extend Business Processes</span><span class="sxs-lookup"><span data-stu-id="2ad1a-124">Write Plug-Ins to Extend Business Processes</span></span>](write-plugin-extend-business-processes.md)  
  
 [<span data-ttu-id="2ad1a-125">Supported Messages and Entities for Plugins for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="2ad1a-125">Supported Messages and Entities for Plugins for Dynamics 365 for Customer Engagement apps</span></span>](supported-messages-entities-plugin.md)  
  
 [<span data-ttu-id="2ad1a-126">Plug-in Development for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="2ad1a-126">Plug-in Development for Dynamics 365 for Customer Engagement apps</span></span>](plugin-development.md)  
  
 [<span data-ttu-id="2ad1a-127">Plug-in Entities for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="2ad1a-127">Plug-in Entities for Dynamics 365 for Customer Engagement apps</span></span>](plug-in-entities.md)  
  
 [<span data-ttu-id="2ad1a-128">Plug-in Registration Entities for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="2ad1a-128">Plug-in Registration Entities for Dynamics 365 for Customer Engagement apps</span></span>](plug-in-registration-entities.md)
