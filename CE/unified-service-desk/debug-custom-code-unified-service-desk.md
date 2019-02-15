---
title: Debug your custom code for Unified Service Desk | MicrosoftDocs
description: Learn about debugging your custom code that you create for Unified Service Desk.
ms.custom:
- dyn365-USD
ms.date: 08/23/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: eabf5f09-b999-466b-8231-0d395f13c595
caps.latest.revision: 8
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 9f00d1e253456463384f2e3929c5c2f4499fb4d3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386132"
---
# <a name="debug-your-custom-code-for-unified-service-desk"></a><span data-ttu-id="d83f4-103">Debug your custom code for Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="d83f4-103">Debug your custom code for Unified Service Desk</span></span>
<span data-ttu-id="d83f4-104">Using custom code for extending [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] involves compiling your custom code into an assembly (DLL file), and then distributing the assembly to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client installation directory on each client computer.</span><span class="sxs-lookup"><span data-stu-id="d83f4-104">Using custom code for extending [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] involves compiling your custom code into an assembly (DLL file), and then distributing the assembly to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client installation directory on each client computer.</span></span>  
  
 <span data-ttu-id="d83f4-105">Debugging your custom code for [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] requires access to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application and a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps instance with [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] solutions deployed.</span><span class="sxs-lookup"><span data-stu-id="d83f4-105">Debugging your custom code for [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] requires access to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application and a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps instance with [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] solutions deployed.</span></span>  
  
 <span data-ttu-id="d83f4-106">To effectively debug your custom code, set your Visual Studio project properties to:</span><span class="sxs-lookup"><span data-stu-id="d83f4-106">To effectively debug your custom code, set your Visual Studio project properties to:</span></span>  
  
- <span data-ttu-id="d83f4-107">Ensure that the latest version of the assembly is copied to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client installation directory every time you build your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project so that you are testing the executable (the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application) using the latest code.</span><span class="sxs-lookup"><span data-stu-id="d83f4-107">Ensure that the latest version of the assembly is copied to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client installation directory every time you build your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project so that you are testing the executable (the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application) using the latest code.</span></span>  
  
- <span data-ttu-id="d83f4-108">Specify the executable or the calling application (the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application) for debugging your code.</span><span class="sxs-lookup"><span data-stu-id="d83f4-108">Specify the executable or the calling application (the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application) for debugging your code.</span></span>  
  
  <span data-ttu-id="d83f4-109">To do so:</span><span class="sxs-lookup"><span data-stu-id="d83f4-109">To do so:</span></span>  
  
1. <span data-ttu-id="d83f4-110">In your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project, from the **Project** menu, select **<Project_Name> Properties**.</span><span class="sxs-lookup"><span data-stu-id="d83f4-110">In your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project, from the **Project** menu, select **<Project_Name> Properties**.</span></span>  
  
2. <span data-ttu-id="d83f4-111">On the **Build** tab, under the **Output** area, set the **Output path** field value to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client installation directory, typically C:\Program Files\Microsoft Dynamics CRM USD\USD\\.</span><span class="sxs-lookup"><span data-stu-id="d83f4-111">On the **Build** tab, under the **Output** area, set the **Output path** field value to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client installation directory, typically C:\Program Files\Microsoft Dynamics CRM USD\USD\\.</span></span>  
  
   <span data-ttu-id="d83f4-112">![Set the output path of the assembly](../unified-service-desk/media/usd-project-build-tab.png "Set the output path of the assembly")</span><span class="sxs-lookup"><span data-stu-id="d83f4-112">![Set the output path of the assembly](../unified-service-desk/media/usd-project-build-tab.png "Set the output path of the assembly")</span></span>  
  
3. <span data-ttu-id="d83f4-113">On the **Debug** tab, select **Start external program**, and specify the full path to the `UnifiedServiceDesk.exe` file in the field, typically C:\Program Files\Microsoft Dynamics CRM USD\USD\ UnifiedServiceDesk.exe</span><span class="sxs-lookup"><span data-stu-id="d83f4-113">On the **Debug** tab, select **Start external program**, and specify the full path to the `UnifiedServiceDesk.exe` file in the field, typically C:\Program Files\Microsoft Dynamics CRM USD\USD\ UnifiedServiceDesk.exe</span></span>  
  
   <span data-ttu-id="d83f4-114">![Set the external application name](../unified-service-desk/media/usd-project-debug-tab.png "Set the external application name")</span><span class="sxs-lookup"><span data-stu-id="d83f4-114">![Set the external application name](../unified-service-desk/media/usd-project-debug-tab.png "Set the external application name")</span></span>  
  
4. <span data-ttu-id="d83f4-115">Save your project.</span><span class="sxs-lookup"><span data-stu-id="d83f4-115">Save your project.</span></span>  
  
    <span data-ttu-id="d83f4-116">This ensures that the latest version of the assembly is copied to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client installation directory every time you build your project, and the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application is automatically started when you debug your project.</span><span class="sxs-lookup"><span data-stu-id="d83f4-116">This ensures that the latest version of the assembly is copied to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client installation directory every time you build your project, and the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application is automatically started when you debug your project.</span></span>  
  
5. <span data-ttu-id="d83f4-117">Set breakpoints in your Visual Studio project as required, and then build/debug your project.</span><span class="sxs-lookup"><span data-stu-id="d83f4-117">Set breakpoints in your Visual Studio project as required, and then build/debug your project.</span></span>  
  
    <span data-ttu-id="d83f4-118">When the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application starts automatically on debugging the project, specify the credentials to connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance to continue with the debugging session until you hit a breakpoint or issue in your code.</span><span class="sxs-lookup"><span data-stu-id="d83f4-118">When the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application starts automatically on debugging the project, specify the credentials to connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance to continue with the debugging session until you hit a breakpoint or issue in your code.</span></span>  
  
   <span data-ttu-id="d83f4-119">Additionally, the **Debug Output** tab of the Debugger hosted control in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application provides real time trace information of the underlying execution, which can be also used to debug your custom code.</span><span class="sxs-lookup"><span data-stu-id="d83f4-119">Additionally, the **Debug Output** tab of the Debugger hosted control in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application provides real time trace information of the underlying execution, which can be also used to debug your custom code.</span></span> <span data-ttu-id="d83f4-120">For more information, see [Debug issues in Unified Service Desk](debug-issues-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="d83f4-120">For more information, see [Debug issues in Unified Service Desk](debug-issues-unified-service-desk.md)</span></span>  
  
   <span data-ttu-id="d83f4-121">The Debugger hosted control comes pre-configured if you have deployed one of the sample [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] packages.</span><span class="sxs-lookup"><span data-stu-id="d83f4-121">The Debugger hosted control comes pre-configured if you have deployed one of the sample [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] packages.</span></span> <span data-ttu-id="d83f4-122">Alternatively, you can easily set up the Debugger hosted control in your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] deployment.</span><span class="sxs-lookup"><span data-stu-id="d83f4-122">Alternatively, you can easily set up the Debugger hosted control in your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] deployment.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="d83f4-123">[Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md)</span><span class="sxs-lookup"><span data-stu-id="d83f4-123">[Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md)</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="d83f4-124">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d83f4-124">See also</span></span>  
 <span data-ttu-id="d83f4-125">[Extend Unified Service Desk](../unified-service-desk/extend-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="d83f4-125">[Extend Unified Service Desk](../unified-service-desk/extend-unified-service-desk.md) </span></span>  
 [<span data-ttu-id="d83f4-126">Unified Service Desk and the UII framework</span><span class="sxs-lookup"><span data-stu-id="d83f4-126">Unified Service Desk and the UII framework</span></span>](../unified-service-desk/unified-service-desk-uii-framework.md)
