---
title: Use UII inspector to create bindings for the hosted application in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn how to use UII inspector to create bindings for the hosted application in Unified Service Desk.
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
ms.assetid: bd17bf36-73d1-4f0e-9d8a-df832ae66bfa
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
ms.openlocfilehash: 14d60a76f7007429b990b0997fe3531f2e50ed69
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388426"
---
# <a name="use-uii-inspector-to-create-bindings-for-the-hosted-application-in-unified-service-desk"></a><span data-ttu-id="4ecb4-103">Use UII inspector to create bindings for the hosted application in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="4ecb4-103">Use UII inspector to create bindings for the hosted application in Unified Service Desk</span></span>
<span data-ttu-id="4ecb4-104">After you create a hosted application, you can inspect it to create bindings.</span><span class="sxs-lookup"><span data-stu-id="4ecb4-104">After you create a hosted application, you can inspect it to create bindings.</span></span> <span data-ttu-id="4ecb4-105">Inspecting an application means that you can select user interface (UI) controls for automating the hosted application.</span><span class="sxs-lookup"><span data-stu-id="4ecb4-105">Inspecting an application means that you can select user interface (UI) controls for automating the hosted application.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="4ecb4-106">[Automate hosted applications using HAT automation activities](../unified-service-desk/automate-hosted-applications-using-hat-automation-activities.md)</span><span class="sxs-lookup"><span data-stu-id="4ecb4-106">[Automate hosted applications using HAT automation activities](../unified-service-desk/automate-hosted-applications-using-hat-automation-activities.md)</span></span>  
  
1. <span data-ttu-id="4ecb4-107">Right-click the application to view the **Application Context** menu, and then choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="4ecb4-107">Right-click the application to view the **Application Context** menu, and then choose **Inspect**.</span></span>  
  
   <span data-ttu-id="4ecb4-108">![Use the shortcut menu to configure](../unified-service-desk/media/usd-create-hat-control-11.png "Use the shortcut menu to configure")</span><span class="sxs-lookup"><span data-stu-id="4ecb4-108">![Use the shortcut menu to configure](../unified-service-desk/media/usd-create-hat-control-11.png "Use the shortcut menu to configure")</span></span>  
  
2. <span data-ttu-id="4ecb4-109">The application selected is displayed and is ready to be inspected.</span><span class="sxs-lookup"><span data-stu-id="4ecb4-109">The application selected is displayed and is ready to be inspected.</span></span> <span data-ttu-id="4ecb4-110">This example uses the web application created in the previous section.</span><span class="sxs-lookup"><span data-stu-id="4ecb4-110">This example uses the web application created in the previous section.</span></span>  
  
   <span data-ttu-id="4ecb4-111">![Screenshot of bindings](../unified-service-desk/media/usd-bindings.PNG "Screenshot of bindings")</span><span class="sxs-lookup"><span data-stu-id="4ecb4-111">![Screenshot of bindings](../unified-service-desk/media/usd-bindings.PNG "Screenshot of bindings")</span></span>  
  
3. <span data-ttu-id="4ecb4-112">Choose **UII Inspector** on the toolbar to display the **UII Inspector** dialog box.</span><span class="sxs-lookup"><span data-stu-id="4ecb4-112">Choose **UII Inspector** on the toolbar to display the **UII Inspector** dialog box.</span></span> <span data-ttu-id="4ecb4-113">Make sure that the **Visual Studio Toolbox** is not in focus when you choose the **UII Inspector** button.</span><span class="sxs-lookup"><span data-stu-id="4ecb4-113">Make sure that the **Visual Studio Toolbox** is not in focus when you choose the **UII Inspector** button.</span></span> <span data-ttu-id="4ecb4-114">If it is, the UII Inspector displays the following error message: "Active Window is not the UII Inspector."</span><span class="sxs-lookup"><span data-stu-id="4ecb4-114">If it is, the UII Inspector displays the following error message: "Active Window is not the UII Inspector."</span></span>  
  
4. <span data-ttu-id="4ecb4-115">With the **UII Inspector** dialog box open, move the mouse over the control you want to capture, and then press the Ctrl key.</span><span class="sxs-lookup"><span data-stu-id="4ecb4-115">With the **UII Inspector** dialog box open, move the mouse over the control you want to capture, and then press the Ctrl key.</span></span> <span data-ttu-id="4ecb4-116">The Inspector will provide a default control name and retrieve the component's binding information.</span><span class="sxs-lookup"><span data-stu-id="4ecb4-116">The Inspector will provide a default control name and retrieve the component's binding information.</span></span>  
  
   <span data-ttu-id="4ecb4-117">![Screenshot of inspector](../unified-service-desk/media/usd-inspector.png "Screenshot of inspector")</span><span class="sxs-lookup"><span data-stu-id="4ecb4-117">![Screenshot of inspector](../unified-service-desk/media/usd-inspector.png "Screenshot of inspector")</span></span>  
  
   <span data-ttu-id="4ecb4-118">For the purpose of this example, add the following controls to the current project:</span><span class="sxs-lookup"><span data-stu-id="4ecb4-118">For the purpose of this example, add the following controls to the current project:</span></span>  
  
-   <span data-ttu-id="4ecb4-119">`SearchText` – The text field on the home page.</span><span class="sxs-lookup"><span data-stu-id="4ecb4-119">`SearchText` – The text field on the home page.</span></span>  
  
-   <span data-ttu-id="4ecb4-120">`Search` – The search button in the home page.</span><span class="sxs-lookup"><span data-stu-id="4ecb4-120">`Search` – The search button in the home page.</span></span>  
  
-   <span data-ttu-id="4ecb4-121">`SearchText2` – The text field on the results page.</span><span class="sxs-lookup"><span data-stu-id="4ecb4-121">`SearchText2` – The text field on the results page.</span></span>  
  
-   <span data-ttu-id="4ecb4-122">`Search2` – The search button in the results page.</span><span class="sxs-lookup"><span data-stu-id="4ecb4-122">`Search2` – The search button in the results page.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="4ecb4-123">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="4ecb4-123">See also</span></span>  
 <span data-ttu-id="4ecb4-124">[Create a HAT hosted application project](../unified-service-desk/use-hat-software-factory-create-hosted-application.md#Create) </span><span class="sxs-lookup"><span data-stu-id="4ecb4-124">[Create a HAT hosted application project](../unified-service-desk/use-hat-software-factory-create-hosted-application.md#Create) </span></span>  
 <span data-ttu-id="4ecb4-125">[Using UII inspector to create bindings](../unified-service-desk/use-uii-inspector-create-bindings-hosted-application.md) </span><span class="sxs-lookup"><span data-stu-id="4ecb4-125">[Using UII inspector to create bindings](../unified-service-desk/use-uii-inspector-create-bindings-hosted-application.md) </span></span>  
 <span data-ttu-id="4ecb4-126">[Configure the hosted application](../unified-service-desk/configure-hosted-application.md) </span><span class="sxs-lookup"><span data-stu-id="4ecb4-126">[Configure the hosted application](../unified-service-desk/configure-hosted-application.md) </span></span>  
 <span data-ttu-id="4ecb4-127">[Configure an action for the hosted application](../unified-service-desk/configure-action-hosted-application.md) </span><span class="sxs-lookup"><span data-stu-id="4ecb4-127">[Configure an action for the hosted application](../unified-service-desk/configure-action-hosted-application.md) </span></span>  
 <span data-ttu-id="4ecb4-128">[Deploy your hosted application to Unified Service Desk](../unified-service-desk/deploy-hosted-application-unified-service-desk.md#deploy) </span><span class="sxs-lookup"><span data-stu-id="4ecb4-128">[Deploy your hosted application to Unified Service Desk](../unified-service-desk/deploy-hosted-application-unified-service-desk.md#deploy) </span></span>  
 [<span data-ttu-id="4ecb4-129">Import the hosted application from Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="4ecb4-129">Import the hosted application from Unified Service Desk</span></span>](../unified-service-desk/import-hosted-application-from-unified-service-desk.md)
