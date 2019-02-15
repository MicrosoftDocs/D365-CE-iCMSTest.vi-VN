---
title: Write plug-ins to extend business processes (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: A plug-in is custom business logic that you can integrate with Dynamics 365 for Customer Engagement (online) Customer Engagement to modify or augment the standard behavior of the platform. Plug-ins are event handlers since they are registered to execute in response to a particular event being fired by the platform.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
f1_keywords:
- plugins
- plugin
helpviewer_keywords:
- plug-in
ms.assetid: f5a0690c-1783-4b36-96cd-cd34ae41eb41
caps.latest.revision: 34
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 62c0beb9439ef6d79559d7a7b74a3c86cdb2cfae
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388747"
---
# <a name="write-plug-ins-to-extend-business-processes"></a><span data-ttu-id="9cf6c-104">Write plug-ins to extend business processes</span><span class="sxs-lookup"><span data-stu-id="9cf6c-104">Write plug-ins to extend business processes</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="9cf6c-105">A plug-in is custom business logic that you can integrate with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement to modify or augment the standard behavior of the platform.</span><span class="sxs-lookup"><span data-stu-id="9cf6c-105">A plug-in is custom business logic that you can integrate with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement to modify or augment the standard behavior of the platform.</span></span> <span data-ttu-id="9cf6c-106">Plug-ins are event handlers since they are registered to execute in response to a particular event being fired by the platform.</span><span class="sxs-lookup"><span data-stu-id="9cf6c-106">Plug-ins are event handlers since they are registered to execute in response to a particular event being fired by the platform.</span></span>  
  
 <span data-ttu-id="9cf6c-107">The following topics describe how to add custom business logic to [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] through the development and registration of plug-ins. For more information about the run-time execution of plug-ins and the plug-in development framework, see [Introduction to the Event Framework](introduction-event-framework.md).</span><span class="sxs-lookup"><span data-stu-id="9cf6c-107">The following topics describe how to add custom business logic to [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] through the development and registration of plug-ins. For more information about the run-time execution of plug-ins and the plug-in development framework, see [Introduction to the Event Framework](introduction-event-framework.md).</span></span>  
  
 <span data-ttu-id="9cf6c-108">You can also extend the functionality of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] by using processes.</span><span class="sxs-lookup"><span data-stu-id="9cf6c-108">You can also extend the functionality of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] by using processes.</span></span> <span data-ttu-id="9cf6c-109">For more information, see the related link below.</span><span class="sxs-lookup"><span data-stu-id="9cf6c-109">For more information, see the related link below.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="9cf6c-110">In This Section</span><span class="sxs-lookup"><span data-stu-id="9cf6c-110">In This Section</span></span>  
 [<span data-ttu-id="9cf6c-111">Introduction to the Event Framework</span><span class="sxs-lookup"><span data-stu-id="9cf6c-111">Introduction to the Event Framework</span></span>](introduction-event-framework.md)<br />  
 [<span data-ttu-id="9cf6c-112">Supported Messages and Entities for Plug-ins</span><span class="sxs-lookup"><span data-stu-id="9cf6c-112">Supported Messages and Entities for Plug-ins</span></span>](supported-messages-entities-plugin.md)<br />    
 [<span data-ttu-id="9cf6c-113">Plug-in Development</span><span class="sxs-lookup"><span data-stu-id="9cf6c-113">Plug-in Development</span></span>](plugin-development.md)<br />    
 [<span data-ttu-id="9cf6c-114">Plug-in Entities</span><span class="sxs-lookup"><span data-stu-id="9cf6c-114">Plug-in Entities</span></span>](plug-in-entities.md)<br />    
 [<span data-ttu-id="9cf6c-115">Plug-in Registration Entities</span><span class="sxs-lookup"><span data-stu-id="9cf6c-115">Plug-in Registration Entities</span></span>](plug-in-registration-entities.md) 
  
## <a name="related-sections"></a><span data-ttu-id="9cf6c-116">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="9cf6c-116">Related Sections</span></span>  
 [<span data-ttu-id="9cf6c-117">Developer Guide for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="9cf6c-117">Developer Guide for Dynamics 365 for Customer Engagement apps</span></span>](developer-guide.md)<br />     
 [<span data-ttu-id="9cf6c-118">Write Workflows to Automate Business Processes in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="9cf6c-118">Write Workflows to Automate Business Processes in Dynamics 365 for Customer Engagement apps</span></span>](automate-business-processes-customer-engagement.md)<br />     
 [<span data-ttu-id="9cf6c-119">Package and Distribute Extensions with Dynamics 365 for Customer Engagement apps Solutions</span><span class="sxs-lookup"><span data-stu-id="9cf6c-119">Package and Distribute Extensions with Dynamics 365 for Customer Engagement apps Solutions</span></span>](package-distribute-extensions-use-solutions.md)<br /> 
