---
title: Use UII adapters to interact with external and web applications in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn how to use UII adapters to interact with your external and web applications without having access to the application’s source code in Unified Service Desk.
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
ms.assetid: 8716818e-8f18-4c29-9cab-0f3ab7416055
caps.latest.revision: 6
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: a6f648928e4c55bed8922c76247012b490b5fe53
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386470"
---
# <a name="use-uii-adapters-to-interact-with-external-and-web-applications-in-unified-service-desk"></a><span data-ttu-id="1630b-103">Use UII adapters to interact with external and web applications in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="1630b-103">Use UII adapters to interact with external and web applications in Unified Service Desk</span></span>
<span data-ttu-id="1630b-104">You can use [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] adapters to interact with your external and web applications without having access to the application’s source code.</span><span class="sxs-lookup"><span data-stu-id="1630b-104">You can use [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] adapters to interact with your external and web applications without having access to the application’s source code.</span></span>  
  
<a name="AppAdapter"></a>   
## <a name="use-the-uii-application-adapter"></a><span data-ttu-id="1630b-105">Use the UII application adapter</span><span class="sxs-lookup"><span data-stu-id="1630b-105">Use the UII application adapter</span></span>  
 <span data-ttu-id="1630b-106">External applications are executable (.exe) files that weren’t written specifically for [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)].</span><span class="sxs-lookup"><span data-stu-id="1630b-106">External applications are executable (.exe) files that weren’t written specifically for [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)].</span></span> <span data-ttu-id="1630b-107">External applications have their own processes.</span><span class="sxs-lookup"><span data-stu-id="1630b-107">External applications have their own processes.</span></span> <span data-ttu-id="1630b-108">Typically, they’re written using Win32 APIs, Microsoft Foundation Classes (MFC), or Visual Basic 6.0.</span><span class="sxs-lookup"><span data-stu-id="1630b-108">Typically, they’re written using Win32 APIs, Microsoft Foundation Classes (MFC), or Visual Basic 6.0.</span></span> <span data-ttu-id="1630b-109">A UII application adapter ([HostedApplicationAdapter](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.hostedapplicationadapter)) allows you to modify the behavior of the application without access to its source code.</span><span class="sxs-lookup"><span data-stu-id="1630b-109">A UII application adapter ([HostedApplicationAdapter](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.hostedapplicationadapter)) allows you to modify the behavior of the application without access to its source code.</span></span>  
  
 [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="1630b-110">provides you a [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] project template for creating a [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] application adapter that contains pre-wired events and methods that you should implement to create your application adapter.</span><span class="sxs-lookup"><span data-stu-id="1630b-110">provides you a [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] project template for creating a [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] application adapter that contains pre-wired events and methods that you should implement to create your application adapter.</span></span> <span data-ttu-id="1630b-111">For information about how you can create a UII application adapter to integrate with an external application, see [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md).</span><span class="sxs-lookup"><span data-stu-id="1630b-111">For information about how you can create a UII application adapter to integrate with an external application, see [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md).</span></span>  
  
<a name="WebAppAdapter"></a>   
## <a name="use-the-uii-web-application-adapter"></a><span data-ttu-id="1630b-112">Use the UII web application adapter</span><span class="sxs-lookup"><span data-stu-id="1630b-112">Use the UII web application adapter</span></span>  
 <span data-ttu-id="1630b-113">You can host any browser-based site, webpage, or web application in **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="1630b-113">You can host any browser-based site, webpage, or web application in **Unified Service Desk**.</span></span> <span data-ttu-id="1630b-114">A UII web application adapter ([WebApplicationAdapter](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.webapplicationadapter)) acts as an interface between the hosted web application and **Unified Service Desk**, allowing you to modify the behavior of the application without accessing its source code.</span><span class="sxs-lookup"><span data-stu-id="1630b-114">A UII web application adapter ([WebApplicationAdapter](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.webapplicationadapter)) acts as an interface between the hosted web application and **Unified Service Desk**, allowing you to modify the behavior of the application without accessing its source code.</span></span>  
  
 [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="1630b-115">provides you a [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] project template for creating a UII web application adapter that contains pre-wired events and methods that you should implement to create your web application adapter.</span><span class="sxs-lookup"><span data-stu-id="1630b-115">provides you a [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] project template for creating a UII web application adapter that contains pre-wired events and methods that you should implement to create your web application adapter.</span></span> <span data-ttu-id="1630b-116">For information about how you can create a UII web application adapter to integrate with an external application, see [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md).</span><span class="sxs-lookup"><span data-stu-id="1630b-116">For information about how you can create a UII web application adapter to integrate with an external application, see [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md).</span></span>  
  
### <a name="uii-action-protocols"></a><span data-ttu-id="1630b-117">UII action protocols</span><span class="sxs-lookup"><span data-stu-id="1630b-117">UII action protocols</span></span>  
 <span data-ttu-id="1630b-118">Under most conditions, [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] hosted applications aren’t modified to work with the agent desktop.</span><span class="sxs-lookup"><span data-stu-id="1630b-118">Under most conditions, [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] hosted applications aren’t modified to work with the agent desktop.</span></span> <span data-ttu-id="1630b-119">Occasionally, though, application modifications are the most expedient way to handle required automations.</span><span class="sxs-lookup"><span data-stu-id="1630b-119">Occasionally, though, application modifications are the most expedient way to handle required automations.</span></span> <span data-ttu-id="1630b-120">If the situation allows, a webpage can leverage HTTP-oriented UII protocols to make calls into Application Integration Framework (AIF).In a hosted application, you can customize the webpage content by implementing additional action protocols.</span><span class="sxs-lookup"><span data-stu-id="1630b-120">If the situation allows, a webpage can leverage HTTP-oriented UII protocols to make calls into Application Integration Framework (AIF).In a hosted application, you can customize the webpage content by implementing additional action protocols.</span></span> <span data-ttu-id="1630b-121">The following table describes the action protocols [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] provides.</span><span class="sxs-lookup"><span data-stu-id="1630b-121">The following table describes the action protocols [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] provides.</span></span>  
  
|<span data-ttu-id="1630b-122">Giao thức</span><span class="sxs-lookup"><span data-stu-id="1630b-122">Protocol</span></span>|<span data-ttu-id="1630b-123">Requested URL</span><span class="sxs-lookup"><span data-stu-id="1630b-123">Requested URL</span></span>|<span data-ttu-id="1630b-124">Mô tả</span><span class="sxs-lookup"><span data-stu-id="1630b-124">Description</span></span>|  
|--------------|-------------------|-----------------|  
|<span data-ttu-id="1630b-125">UII</span><span class="sxs-lookup"><span data-stu-id="1630b-125">UII</span></span>|<span data-ttu-id="1630b-126">UII://\<Target App>/Action?\<ActionData>\<ActionData></span><span class="sxs-lookup"><span data-stu-id="1630b-126">UII://\<Target App>/Action?\<ActionData>\<ActionData></span></span>|<span data-ttu-id="1630b-127">The protocol triggers a `RequestAction` event to the target web application.</span><span class="sxs-lookup"><span data-stu-id="1630b-127">The protocol triggers a `RequestAction` event to the target web application.</span></span>|  
|<span data-ttu-id="1630b-128">UIICTX</span><span class="sxs-lookup"><span data-stu-id="1630b-128">UIICTX</span></span>|<span data-ttu-id="1630b-129">UIICTX://update/Name1=Value1&Name2=Value2</span><span class="sxs-lookup"><span data-stu-id="1630b-129">UIICTX://update/Name1=Value1&Name2=Value2</span></span>|<span data-ttu-id="1630b-130">The protocol adds a name-value pair to the current context and triggers a **ChangeContext** event.</span><span class="sxs-lookup"><span data-stu-id="1630b-130">The protocol adds a name-value pair to the current context and triggers a **ChangeContext** event.</span></span>|  
  
 <span data-ttu-id="1630b-131">The following is an example of a UII protocol call from an HTML page.</span><span class="sxs-lookup"><span data-stu-id="1630b-131">The following is an example of a UII protocol call from an HTML page.</span></span>  
  
```  
<HTML>  
  <HEAD>  
    <TITLE>Sample UII Protocol Call</TITLE>  
  </HEAD>  
  <BODY  
    <A href="UII://MyApp/MyAction?<GetFocus>true</GetFocus>">Click to execute an action</A></FONT></P>  
  </BODY>  
</HTML>  
  
```  
  
 <span data-ttu-id="1630b-132">In the preceding example, clicking the link initiates the `WebApplicationAdapter` for the `MyApp` web application and adapter.</span><span class="sxs-lookup"><span data-stu-id="1630b-132">In the preceding example, clicking the link initiates the `WebApplicationAdapter` for the `MyApp` web application and adapter.</span></span> <span data-ttu-id="1630b-133">The adapter calls the action specified [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] protocol to update the [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] context.</span><span class="sxs-lookup"><span data-stu-id="1630b-133">The adapter calls the action specified [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] protocol to update the [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] context.</span></span> <span data-ttu-id="1630b-134">You can replace the [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] protocol with the UIICTX protocol to execute context update action.</span><span class="sxs-lookup"><span data-stu-id="1630b-134">You can replace the [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] protocol with the UIICTX protocol to execute context update action.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="1630b-135">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1630b-135">See also</span></span>  
 <span data-ttu-id="1630b-136">[Use HAT adapters](../unified-service-desk/use-uii-automation-adapter-interact-external-web-applications.md) </span><span class="sxs-lookup"><span data-stu-id="1630b-136">[Use HAT adapters](../unified-service-desk/use-uii-automation-adapter-interact-external-web-applications.md) </span></span>  
 <span data-ttu-id="1630b-137">[UII adapters](../unified-service-desk/uii-adapters.md) </span><span class="sxs-lookup"><span data-stu-id="1630b-137">[UII adapters](../unified-service-desk/uii-adapters.md) </span></span>  
 <span data-ttu-id="1630b-138">[Cách: Tạo Bộ chuyển đổi Ứng dụng UII](../unified-service-desk/walkthrough-create-uii-application-adapter.md) </span><span class="sxs-lookup"><span data-stu-id="1630b-138">[Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) </span></span>  
 [<span data-ttu-id="1630b-139">Walkthrough: Create a UII Web Application Adapter</span><span class="sxs-lookup"><span data-stu-id="1630b-139">Walkthrough: Create a UII Web Application Adapter</span></span>](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md)
