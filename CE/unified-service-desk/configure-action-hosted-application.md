---
title: Configure an action for the hosted application | MicrosoftDocs
description: Learn about configuring the actions for the hosted application.
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
ms.assetid: e8a01fe6-df83-40e4-9b1e-faa4a3f46da5
caps.latest.revision: 5
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 9da8dd03175b2a4ea1c37f182910b50f7e14e7de
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386928"
---
# <a name="configure-an-action-for-the-hosted-application"></a><span data-ttu-id="01f7a-103">Configure an action for the hosted application</span><span class="sxs-lookup"><span data-stu-id="01f7a-103">Configure an action for the hosted application</span></span>
<span data-ttu-id="01f7a-104">After you have configured your application using the Hosted Application Toolkit (HAT), you must configure actions for the application.</span><span class="sxs-lookup"><span data-stu-id="01f7a-104">After you have configured your application using the Hosted Application Toolkit (HAT), you must configure actions for the application.</span></span> <span data-ttu-id="01f7a-105">The application along with the actions is deployed using the HAT Software Factory.</span><span class="sxs-lookup"><span data-stu-id="01f7a-105">The application along with the actions is deployed using the HAT Software Factory.</span></span>  
  
1. <span data-ttu-id="01f7a-106">Open the HAT application project in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)], if it’s not already open.</span><span class="sxs-lookup"><span data-stu-id="01f7a-106">Open the HAT application project in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)], if it’s not already open.</span></span> <span data-ttu-id="01f7a-107">For information about creating a HAT application, see [Use HAT Software Factory to create a hosted application](../unified-service-desk/use-hat-software-factory-create-hosted-application.md).</span><span class="sxs-lookup"><span data-stu-id="01f7a-107">For information about creating a HAT application, see [Use HAT Software Factory to create a hosted application](../unified-service-desk/use-hat-software-factory-create-hosted-application.md).</span></span>  
  
2. <span data-ttu-id="01f7a-108">In Solution Explorer, right-click the HAT application name, and then click **Action Configuration**.</span><span class="sxs-lookup"><span data-stu-id="01f7a-108">In Solution Explorer, right-click the HAT application name, and then click **Action Configuration**.</span></span>  
  
   <span data-ttu-id="01f7a-109">![Use the shortcut menu to configure](../unified-service-desk/media/usd-create-hat-control-11.png "Use the shortcut menu to configure")</span><span class="sxs-lookup"><span data-stu-id="01f7a-109">![Use the shortcut menu to configure](../unified-service-desk/media/usd-create-hat-control-11.png "Use the shortcut menu to configure")</span></span>  
  
3. <span data-ttu-id="01f7a-110">In the **Action Configuration** dialog box, select the **Default** check box if you want the action to be a default action.</span><span class="sxs-lookup"><span data-stu-id="01f7a-110">In the **Action Configuration** dialog box, select the **Default** check box if you want the action to be a default action.</span></span> <span data-ttu-id="01f7a-111">Otherwise, click **New** to create a new action.</span><span class="sxs-lookup"><span data-stu-id="01f7a-111">Otherwise, click **New** to create a new action.</span></span>  
  
4. <span data-ttu-id="01f7a-112">Select the **Focus** check box to return focus to the application after the action is completed.</span><span class="sxs-lookup"><span data-stu-id="01f7a-112">Select the **Focus** check box to return focus to the application after the action is completed.</span></span>  
  
5. <span data-ttu-id="01f7a-113">Under the **URL Navigation** area:</span><span class="sxs-lookup"><span data-stu-id="01f7a-113">Under the **URL Navigation** area:</span></span>  
  
   1.  <span data-ttu-id="01f7a-114">Enter the navigation URL and query string for the web application.</span><span class="sxs-lookup"><span data-stu-id="01f7a-114">Enter the navigation URL and query string for the web application.</span></span>  
  
   2.  <span data-ttu-id="01f7a-115">In the **Method** drop-down list, click **Get** or **Post**.</span><span class="sxs-lookup"><span data-stu-id="01f7a-115">In the **Method** drop-down list, click **Get** or **Post**.</span></span>  
  
   > [!NOTE]
   >  <span data-ttu-id="01f7a-116">For an external application, fields under the **URL Navigation** area are unavailable.</span><span class="sxs-lookup"><span data-stu-id="01f7a-116">For an external application, fields under the **URL Navigation** area are unavailable.</span></span>  
  
6. <span data-ttu-id="01f7a-117">Select one of the following from the **Automation Mode** drop-down list:</span><span class="sxs-lookup"><span data-stu-id="01f7a-117">Select one of the following from the **Automation Mode** drop-down list:</span></span>  
  
   - <span data-ttu-id="01f7a-118">**No Automation**: Select this option if you do not want the action to automate the hosted application.</span><span class="sxs-lookup"><span data-stu-id="01f7a-118">**No Automation**: Select this option if you do not want the action to automate the hosted application.</span></span>  
  
   - <span data-ttu-id="01f7a-119">**Use Workflow Assembly**: Select this option if want the action to use a workflow assembly to automate the hosted application.</span><span class="sxs-lookup"><span data-stu-id="01f7a-119">**Use Workflow Assembly**: Select this option if want the action to use a workflow assembly to automate the hosted application.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="01f7a-120">[Configure an action to run the automation](../unified-service-desk/create-hat-automation.md#action)</span><span class="sxs-lookup"><span data-stu-id="01f7a-120">[Configure an action to run the automation](../unified-service-desk/create-hat-automation.md#action)</span></span>  
  
   - <span data-ttu-id="01f7a-121">**Use Workflow XAML**: Select this option if want the action to use workflow XAML to automate the hosted application.</span><span class="sxs-lookup"><span data-stu-id="01f7a-121">**Use Workflow XAML**: Select this option if want the action to use workflow XAML to automate the hosted application.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="01f7a-122">[Configure an action to run the automation](../unified-service-desk/create-hat-automation.md#action)</span><span class="sxs-lookup"><span data-stu-id="01f7a-122">[Configure an action to run the automation](../unified-service-desk/create-hat-automation.md#action)</span></span>  
  
7. <span data-ttu-id="01f7a-123">Click **Save** to save the configurations.</span><span class="sxs-lookup"><span data-stu-id="01f7a-123">Click **Save** to save the configurations.</span></span>  
  
   <span data-ttu-id="01f7a-124">![Action configuration in HAT](../unified-service-desk/media/usd-action-config.png "Action configuration in HAT")</span><span class="sxs-lookup"><span data-stu-id="01f7a-124">![Action configuration in HAT](../unified-service-desk/media/usd-action-config.png "Action configuration in HAT")</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="01f7a-125">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="01f7a-125">See also</span></span>  
 <span data-ttu-id="01f7a-126">[Integrate with external applications and web applications](../unified-service-desk/integrate-external-applications-web-applications.md) </span><span class="sxs-lookup"><span data-stu-id="01f7a-126">[Integrate with external applications and web applications](../unified-service-desk/integrate-external-applications-web-applications.md) </span></span>  
 <span data-ttu-id="01f7a-127">[Tạo một dự án ứng dụng được lưu trữ bởi HAT](../unified-service-desk/use-hat-software-factory-create-hosted-application.md#Create) </span><span class="sxs-lookup"><span data-stu-id="01f7a-127">[Create a HAT hosted application project](../unified-service-desk/use-hat-software-factory-create-hosted-application.md#Create) </span></span>  
 <span data-ttu-id="01f7a-128">[Using UII inspector to create bindings](../unified-service-desk/use-uii-inspector-create-bindings-hosted-application.md) </span><span class="sxs-lookup"><span data-stu-id="01f7a-128">[Using UII inspector to create bindings](../unified-service-desk/use-uii-inspector-create-bindings-hosted-application.md) </span></span>  
 <span data-ttu-id="01f7a-129">[Configure the hosted application](../unified-service-desk/configure-hosted-application.md) </span><span class="sxs-lookup"><span data-stu-id="01f7a-129">[Configure the hosted application](../unified-service-desk/configure-hosted-application.md) </span></span>  
 <span data-ttu-id="01f7a-130">[Deploy your hosted application to Unified Service Desk](../unified-service-desk/deploy-hosted-application-unified-service-desk.md#deploy) </span><span class="sxs-lookup"><span data-stu-id="01f7a-130">[Deploy your hosted application to Unified Service Desk](../unified-service-desk/deploy-hosted-application-unified-service-desk.md#deploy) </span></span>  
 [<span data-ttu-id="01f7a-131">Import the hosted application from Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="01f7a-131">Import the hosted application from Unified Service Desk</span></span>](../unified-service-desk/import-hosted-application-from-unified-service-desk.md)
