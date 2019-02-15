---
title: Deploy the hosted application to Unified Service Desk | MicrosoftDocs
description: Learn about deploying the hosted application in Unified Service Desk.
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
ms.assetid: bd6242eb-5b59-4ceb-bc09-0f7b1e892cdc
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 61675ba5426efaf0455186c020b1ff19e18cd372
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387704"
---
# <a name="deploy-the-hosted-application-to-unified-service-desk"></a><span data-ttu-id="14512-103">Deploy the hosted application to Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="14512-103">Deploy the hosted application to Unified Service Desk</span></span>
<span data-ttu-id="14512-104">Once you have created a hosted application as described in [Create a HAT hosted application project](../unified-service-desk/use-hat-software-factory-create-hosted-application.md#Create), you can deploy it to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="14512-104">Once you have created a hosted application as described in [Create a HAT hosted application project](../unified-service-desk/use-hat-software-factory-create-hosted-application.md#Create), you can deploy it to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="14512-105">is configured on the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps server.</span><span class="sxs-lookup"><span data-stu-id="14512-105">is configured on the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps server.</span></span> <span data-ttu-id="14512-106">You must ensure that all workflow-dependent applications that contain a default workflow include the workflow assembly (.dll file).</span><span class="sxs-lookup"><span data-stu-id="14512-106">You must ensure that all workflow-dependent applications that contain a default workflow include the workflow assembly (.dll file).</span></span> <span data-ttu-id="14512-107">If the assembly file isn’t found or is deleted, the `Type` field in the Action XML is set to `NULL`.</span><span class="sxs-lookup"><span data-stu-id="14512-107">If the assembly file isn’t found or is deleted, the `Type` field in the Action XML is set to `NULL`.</span></span>  
  
<a name="deploy"></a>   
## <a name="deploy-your-hosted-application-to-unified-service-desk"></a><span data-ttu-id="14512-108">Deploy your hosted application to Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="14512-108">Deploy your hosted application to Unified Service Desk</span></span>  
  
1. <span data-ttu-id="14512-109">Right-click the application in **Solution Explorer** and select **Deploy**.</span><span class="sxs-lookup"><span data-stu-id="14512-109">Right-click the application in **Solution Explorer** and select **Deploy**.</span></span>  
  
   <span data-ttu-id="14512-110">![Use the shortcut menu to configure](../unified-service-desk/media/usd-create-hat-control-11.png "Use the shortcut menu to configure")</span><span class="sxs-lookup"><span data-stu-id="14512-110">![Use the shortcut menu to configure](../unified-service-desk/media/usd-create-hat-control-11.png "Use the shortcut menu to configure")</span></span>  
  
2. <span data-ttu-id="14512-111">In the **Publish to Dynamics 365 for Customer Engagement** dialog box, enter the Dynamics 365 for Customer Engagement server name and your credentials.</span><span class="sxs-lookup"><span data-stu-id="14512-111">In the **Publish to Dynamics 365 for Customer Engagement** dialog box, enter the Dynamics 365 for Customer Engagement server name and your credentials.</span></span>  
  
   <span data-ttu-id="14512-112">![Publish to Dynamics 365 for Customer Engagement apps dialog box](../unified-service-desk/media/usd-deploy.png "Publish to Dynamics 365 for Customer Engagement apps dialog box")</span><span class="sxs-lookup"><span data-stu-id="14512-112">![Publish to Dynamics 365 for Customer Engagement apps dialog box](../unified-service-desk/media/usd-deploy.png "Publish to Dynamics 365 for Customer Engagement apps dialog box")</span></span>  
  
3. <span data-ttu-id="14512-113">If there is more than one organization, check the **Display list of available organizations** check box and click **Login**.</span><span class="sxs-lookup"><span data-stu-id="14512-113">If there is more than one organization, check the **Display list of available organizations** check box and click **Login**.</span></span>  
  
4. <span data-ttu-id="14512-114">Select your organization from the list of organizations displayed and click **OK**.</span><span class="sxs-lookup"><span data-stu-id="14512-114">Select your organization from the list of organizations displayed and click **OK**.</span></span>  
  
<a name="verify"></a>   
## <a name="verify-that-the-application-is-successfully-deployed"></a><span data-ttu-id="14512-115">Verify that the application is successfully deployed</span><span class="sxs-lookup"><span data-stu-id="14512-115">Verify that the application is successfully deployed</span></span>  
  
1. <span data-ttu-id="14512-116">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="14512-116">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="14512-117">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement apps**, and then select **Settings**.</span><span class="sxs-lookup"><span data-stu-id="14512-117">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement apps**, and then select **Settings**.</span></span>  
  
3. <span data-ttu-id="14512-118">Choose **Settings** > **Unified Service Desk** > **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="14512-118">Choose **Settings** > **Unified Service Desk** > **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="14512-119">From the list of hosted controls, select the hosted application you just deployed.</span><span class="sxs-lookup"><span data-stu-id="14512-119">From the list of hosted controls, select the hosted application you just deployed.</span></span> <span data-ttu-id="14512-120">In this case, it’s [!INCLUDE[pn_bing](../includes/pn-bing.md)] Search.</span><span class="sxs-lookup"><span data-stu-id="14512-120">In this case, it’s [!INCLUDE[pn_bing](../includes/pn-bing.md)] Search.</span></span>  
  
   <span data-ttu-id="14512-121">![List of hosted controls showing Bing Search](../unified-service-desk/media/usd-hat-deploy-test.PNG "List of hosted controls showing Bing Search")</span><span class="sxs-lookup"><span data-stu-id="14512-121">![List of hosted controls showing Bing Search](../unified-service-desk/media/usd-hat-deploy-test.PNG "List of hosted controls showing Bing Search")</span></span>  
  
5. <span data-ttu-id="14512-122">The configuration information for the hosted application is displayed.</span><span class="sxs-lookup"><span data-stu-id="14512-122">The configuration information for the hosted application is displayed.</span></span>  
  
   <span data-ttu-id="14512-123">![Hosted control information dialog box](../unified-service-desk/media/usd-deploy-test-hosted-control-info.PNG "Hosted control information dialog box")</span><span class="sxs-lookup"><span data-stu-id="14512-123">![Hosted control information dialog box](../unified-service-desk/media/usd-deploy-test-hosted-control-info.PNG "Hosted control information dialog box")</span></span>  
  
6. <span data-ttu-id="14512-124">The bindings you created in [Use UII inspector to create bindings for the hosted application](../unified-service-desk/use-uii-inspector-create-bindings-hosted-application.md) are displayed in the Automation XML area.</span><span class="sxs-lookup"><span data-stu-id="14512-124">The bindings you created in [Use UII inspector to create bindings for the hosted application](../unified-service-desk/use-uii-inspector-create-bindings-hosted-application.md) are displayed in the Automation XML area.</span></span>  
  
   <span data-ttu-id="14512-125">![Automation bindings](../unified-service-desk/media/usd-automation-xml.PNG "Automation bindings")</span><span class="sxs-lookup"><span data-stu-id="14512-125">![Automation bindings](../unified-service-desk/media/usd-automation-xml.PNG "Automation bindings")</span></span>  
  
7. <span data-ttu-id="14512-126">Copy the assembly that you generated in [Create a HAT hosted application project](../unified-service-desk/use-hat-software-factory-create-hosted-application.md#Create) from your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project output folder (\<ProjectFolder>\bin\debug) to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application directory.</span><span class="sxs-lookup"><span data-stu-id="14512-126">Copy the assembly that you generated in [Create a HAT hosted application project](../unified-service-desk/use-hat-software-factory-create-hosted-application.md#Create) from your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project output folder (\<ProjectFolder>\bin\debug) to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application directory.</span></span> <span data-ttu-id="14512-127">In this case, we will copy the Bing Search.dll file to the c:\Program Files\Microsoft Dynamics CRM USD\USD directory.</span><span class="sxs-lookup"><span data-stu-id="14512-127">In this case, we will copy the Bing Search.dll file to the c:\Program Files\Microsoft Dynamics CRM USD\USD directory.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="14512-128">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="14512-128">See also</span></span>  
 <span data-ttu-id="14512-129">[Create a HAT hosted application project](../unified-service-desk/use-hat-software-factory-create-hosted-application.md#Create) </span><span class="sxs-lookup"><span data-stu-id="14512-129">[Create a HAT hosted application project](../unified-service-desk/use-hat-software-factory-create-hosted-application.md#Create) </span></span>  
 <span data-ttu-id="14512-130">[Using UII inspector to create bindings](../unified-service-desk/use-uii-inspector-create-bindings-hosted-application.md) </span><span class="sxs-lookup"><span data-stu-id="14512-130">[Using UII inspector to create bindings](../unified-service-desk/use-uii-inspector-create-bindings-hosted-application.md) </span></span>  
 <span data-ttu-id="14512-131">[Configure the HAT application](../unified-service-desk/configure-hosted-application.md) </span><span class="sxs-lookup"><span data-stu-id="14512-131">[Configure the HAT application](../unified-service-desk/configure-hosted-application.md) </span></span>  
 <span data-ttu-id="14512-132">[Configuring an action for the HAT application](../unified-service-desk/configure-action-hosted-application.md) </span><span class="sxs-lookup"><span data-stu-id="14512-132">[Configuring an action for the HAT application](../unified-service-desk/configure-action-hosted-application.md) </span></span>  
 [<span data-ttu-id="14512-133">Import the hosted application from Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="14512-133">Import the hosted application from Unified Service Desk</span></span>](../unified-service-desk/import-hosted-application-from-unified-service-desk.md)
