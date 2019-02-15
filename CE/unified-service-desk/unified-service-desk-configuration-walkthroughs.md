---
title: Unified Service Desk for Dynamics 365 for Customer Engagement apps configuration walkthroughs | MicrosoftDocs
description: Unified Service Desk walkthroughs provide you a step-by-step tutorial on configuring an agent application from scratch and progressively add features.
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
ms.assetid: 8bf9991c-4809-489f-b478-0d86666c2299
caps.latest.revision: 7
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 2e5cfade392fe28cf8c9c48e4e31af4a6961dcd0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388704"
---
# <a name="unified-service-desk-configuration-walkthroughs"></a><span data-ttu-id="2386a-103">Unified Service Desk configuration walkthroughs</span><span class="sxs-lookup"><span data-stu-id="2386a-103">Unified Service Desk configuration walkthroughs</span></span>
<span data-ttu-id="2386a-104">Each walkthrough in this section covers an area or a combination of areas in [!INCLUDE[pn_unified_service_desk_for_crm](../includes/pn-unified-service-desk-for-crm.md)].</span><span class="sxs-lookup"><span data-stu-id="2386a-104">Each walkthrough in this section covers an area or a combination of areas in [!INCLUDE[pn_unified_service_desk_for_crm](../includes/pn-unified-service-desk-for-crm.md)].</span></span> <span data-ttu-id="2386a-105">These walkthroughs are arranged in increasing order of complexity so it may benefit you to do them in sequence.</span><span class="sxs-lookup"><span data-stu-id="2386a-105">These walkthroughs are arranged in increasing order of complexity so it may benefit you to do them in sequence.</span></span> <span data-ttu-id="2386a-106">Also, you must complete [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md) first because it sets up the base application that the other walkthroughs, except walkthrough 8, are built on.</span><span class="sxs-lookup"><span data-stu-id="2386a-106">Also, you must complete [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md) first because it sets up the base application that the other walkthroughs, except walkthrough 8, are built on.</span></span> <span data-ttu-id="2386a-107">Cách 8 là cách độc lập và không yêu cầu hoàn thành bất kỳ cách nào khác trước khi sử dụng.</span><span class="sxs-lookup"><span data-stu-id="2386a-107">Walkthrough 8 is a standalone walkthrough, and does not require any other walkthroughs to be completed before using it.</span></span>  
  
 <span data-ttu-id="2386a-108">These walkthroughs are created using the “New Environment” sample application package deployed on an on-premises instance of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="2386a-108">These walkthroughs are created using the “New Environment” sample application package deployed on an on-premises instance of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span> <span data-ttu-id="2386a-109">Before you begin these walkthroughs, ensure that you have deployed one of the sample [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] applications, have installed the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and have appropriate security access in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps to configure [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] entities.</span><span class="sxs-lookup"><span data-stu-id="2386a-109">Before you begin these walkthroughs, ensure that you have deployed one of the sample [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] applications, have installed the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and have appropriate security access in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps to configure [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] entities.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="2386a-110">[Deploy sample Unified Service Desk applications using Package Deployer](/dynamics365/customer-engagement/admin/deploy-packages-using-package-deployer-windows-powershell)</span><span class="sxs-lookup"><span data-stu-id="2386a-110">[Deploy sample Unified Service Desk applications using Package Deployer](/dynamics365/customer-engagement/admin/deploy-packages-using-package-deployer-windows-powershell)</span></span>  
  
## <a name="related-topics"></a><span data-ttu-id="2386a-111">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="2386a-111">Related topics</span></span>  
 [<span data-ttu-id="2386a-112">Install, upgrade and deploy Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="2386a-112">Install, upgrade and deploy Unified Service Desk</span></span>](../unified-service-desk/admin/install-upgrade-deploy-unified-service-desk.md)  
  
 [<span data-ttu-id="2386a-113">Sample Unified Service Desk applications</span><span class="sxs-lookup"><span data-stu-id="2386a-113">Sample Unified Service Desk applications</span></span>](../unified-service-desk/admin/sample-unified-service-desk-applications.md )  
  
 [<span data-ttu-id="2386a-114">Learn to use Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="2386a-114">Learn to use Unified Service Desk</span></span>](../unified-service-desk/learn-to-use-unified-service-desk.md)  
  
 [<span data-ttu-id="2386a-115">Customize themes in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="2386a-115">Customize themes in Unified Service Desk</span></span>](../unified-service-desk/customize-themes-in-unified-service-desk.md)  
  
 [<span data-ttu-id="2386a-116">Create a custom Unified Service Desk hosted control</span><span class="sxs-lookup"><span data-stu-id="2386a-116">Create a custom Unified Service Desk hosted control</span></span>](../unified-service-desk/walkthrough-create-custom-hosted-control-for-unified-service-desk.md)  
  
 [<span data-ttu-id="2386a-117">Create a custom panel layout in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="2386a-117">Create a custom panel layout in Unified Service Desk</span></span>](../unified-service-desk/create-custom-panel-layout.md)  
    
 [<span data-ttu-id="2386a-118">Walkthrough: Create a UII Application Adapter</span><span class="sxs-lookup"><span data-stu-id="2386a-118">Walkthrough: Create a UII Application Adapter</span></span>](../unified-service-desk/walkthrough-create-uii-application-adapter.md)  
  
 [<span data-ttu-id="2386a-119">Walkthrough: Create a UII Web Application Adapter</span><span class="sxs-lookup"><span data-stu-id="2386a-119">Walkthrough: Create a UII Web Application Adapter</span></span>](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md)  
  
 [<span data-ttu-id="2386a-120">Walkthrough: Create a UII Windows Forms Hosted Control</span><span class="sxs-lookup"><span data-stu-id="2386a-120">Walkthrough: Create a UII Windows Forms Hosted Control</span></span>](../unified-service-desk/walkthrough-create-uii-windows-forms-hosted-control.md)  
  
 [<span data-ttu-id="2386a-121">Walkthrough: Create a UII WPF Hosted Control</span><span class="sxs-lookup"><span data-stu-id="2386a-121">Walkthrough: Create a UII WPF Hosted Control</span></span>](../unified-service-desk/walkthrough-create-uii-wpf-hosted-control.md)  
  
 [<span data-ttu-id="2386a-122">Walkthrough: Use the generic listener adapter for CTI event routing</span><span class="sxs-lookup"><span data-stu-id="2386a-122">Walkthrough: Use the generic listener adapter for CTI event routing</span></span>](../unified-service-desk/walkthrough-use-the-generic-listener-adapter-for-cti-event-routing.md)
