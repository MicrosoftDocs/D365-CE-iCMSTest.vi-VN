---
title: Create and manage UII hosted applications | MicrosoftDocs
description: Learn about using the User Interface Integration (UII) hosted application to host your external application or a web application in Unified Service Desk. To host an external or web application in Unified Service Desk, you configure a hosted control of type CCA Hosted Application, and then select Web Hosted Application or External Hosted Application from the Hosted Application list.
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
ms.assetid: ba20bfa3-6a1d-4e87-9faa-40317c839be4
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: a704b2f64d7841b83a67aa77411de88cc4f6ea18
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386539"
---
# <a name="create-and-manage-uii-hosted-applications-in-unified-service-desk"></a><span data-ttu-id="0e72e-104">Create and manage UII hosted applications in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="0e72e-104">Create and manage UII hosted applications in Unified Service Desk</span></span>
<span data-ttu-id="0e72e-105">A [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] hosted application enables you to create and host a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control, Windows Forms or [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)] application, web application, or a remote (Citrix) application in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="0e72e-105">A [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] hosted application enables you to create and host a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control, Windows Forms or [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)] application, web application, or a remote (Citrix) application in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
 <span data-ttu-id="0e72e-106">In this topic, you’ll learn how to configure a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted application in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="0e72e-106">In this topic, you’ll learn how to configure a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted application in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
## <a name="create-a-hosted-application"></a><span data-ttu-id="0e72e-107">Create a hosted application</span><span class="sxs-lookup"><span data-stu-id="0e72e-107">Create a hosted application</span></span>  
  
1. <span data-ttu-id="0e72e-108">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="0e72e-108">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="0e72e-109">On the navigation bar, click or tap **Microsoft Dynamics 365 for Customer Engagement apps**, and then select **Settings**.</span><span class="sxs-lookup"><span data-stu-id="0e72e-109">On the navigation bar, click or tap **Microsoft Dynamics 365 for Customer Engagement apps**, and then select **Settings**.</span></span>  
  
3. <span data-ttu-id="0e72e-110">Choose **Settings** > **Unified Service Desk** > **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="0e72e-110">Choose **Settings** > **Unified Service Desk** > **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="0e72e-111">Chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="0e72e-111">Choose **New**.</span></span>  
  
5. <span data-ttu-id="0e72e-112">On the **New Hosted Control** page, under the **General** area, specify a name, sort order and display name for the hosted application.</span><span class="sxs-lookup"><span data-stu-id="0e72e-112">On the **New Hosted Control** page, under the **General** area, specify a name, sort order and display name for the hosted application.</span></span> <span data-ttu-id="0e72e-113">Each hosted application should have a unique name.</span><span class="sxs-lookup"><span data-stu-id="0e72e-113">Each hosted application should have a unique name.</span></span> <span data-ttu-id="0e72e-114">Sort order specifies the order in which the hosted applications are retrieved and displayed in **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="0e72e-114">Sort order specifies the order in which the hosted applications are retrieved and displayed in **Unified Service Desk**.</span></span> <span data-ttu-id="0e72e-115">Select the owner in the **Owner** box.</span><span class="sxs-lookup"><span data-stu-id="0e72e-115">Select the owner in the **Owner** box.</span></span>  
  
6. <span data-ttu-id="0e72e-116">Under the **Unified Service Desk** area, select **CCA Hosted Application** from the **USD Component Type** list.</span><span class="sxs-lookup"><span data-stu-id="0e72e-116">Under the **Unified Service Desk** area, select **CCA Hosted Application** from the **USD Component Type** list.</span></span> <span data-ttu-id="0e72e-117">The fields in the New Hosted Control page change based on the type of hosted control you choose.</span><span class="sxs-lookup"><span data-stu-id="0e72e-117">The fields in the New Hosted Control page change based on the type of hosted control you choose.</span></span> <span data-ttu-id="0e72e-118">For more information on the various hosted control types, see [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)</span><span class="sxs-lookup"><span data-stu-id="0e72e-118">For more information on the various hosted control types, see [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)</span></span>  
  
7. <span data-ttu-id="0e72e-119">Under the **Hosted App Type** area, select the type of the hosted application.</span><span class="sxs-lookup"><span data-stu-id="0e72e-119">Under the **Hosted App Type** area, select the type of the hosted application.</span></span> <span data-ttu-id="0e72e-120">The fields in the **Hosting** area change based on the type of hosted application type selected.</span><span class="sxs-lookup"><span data-stu-id="0e72e-120">The fields in the **Hosting** area change based on the type of hosted application type selected.</span></span>  
  
   <span data-ttu-id="0e72e-121">![Hosted application types](../unified-service-desk/media/usd-hostedapptypes.PNG "Hosted application types")</span><span class="sxs-lookup"><span data-stu-id="0e72e-121">![Hosted application types](../unified-service-desk/media/usd-hostedapptypes.PNG "Hosted application types")</span></span>  
  
   1.  <span data-ttu-id="0e72e-122">For a hosted control, select **Hosted Control** type.</span><span class="sxs-lookup"><span data-stu-id="0e72e-122">For a hosted control, select **Hosted Control** type.</span></span> <span data-ttu-id="0e72e-123">Under **Hosting** area, specify the assembly URI and Type.</span><span class="sxs-lookup"><span data-stu-id="0e72e-123">Under **Hosting** area, specify the assembly URI and Type.</span></span>  
  
   <span data-ttu-id="0e72e-124">**URI** là tên của cụm tổ hợp của bạn và **Loại** là tên của cụm tổ hợp của bạn (dll) theo sau bởi dấu chấm (.) sau đó là tên lớp trong dự án Visual Studio của bạn.</span><span class="sxs-lookup"><span data-stu-id="0e72e-124">**URI** is the name of your assembly and the **Type** is the name of your assembly (dll) followed by a dot (.) and then the class name in your Visual Studio project.</span></span>  
  
   <span data-ttu-id="0e72e-125">![Hosted control type assembly information](../unified-service-desk/media/usd-hostedcontroltype.PNG "Hosted control type assembly information")</span><span class="sxs-lookup"><span data-stu-id="0e72e-125">![Hosted control type assembly information](../unified-service-desk/media/usd-hostedcontroltype.PNG "Hosted control type assembly information")</span></span>  
  
   2.  <span data-ttu-id="0e72e-126">For hosting a web application, select **Web Hosted Application** type.</span><span class="sxs-lookup"><span data-stu-id="0e72e-126">For hosting a web application, select **Web Hosted Application** type.</span></span> <span data-ttu-id="0e72e-127">Under **Hosting** area,</span><span class="sxs-lookup"><span data-stu-id="0e72e-127">Under **Hosting** area,</span></span>  
  
       1. <span data-ttu-id="0e72e-128">**Application Hosting** is used to specify the mode of hosting the application.</span><span class="sxs-lookup"><span data-stu-id="0e72e-128">**Application Hosting** is used to specify the mode of hosting the application.</span></span> <span data-ttu-id="0e72e-129">There are three modes of hosting an application, namely,</span><span class="sxs-lookup"><span data-stu-id="0e72e-129">There are three modes of hosting an application, namely,</span></span>  
  
           1. <span data-ttu-id="0e72e-130">**Host Outside** – allows the application to be started outside of **Unified Service Desk**</span><span class="sxs-lookup"><span data-stu-id="0e72e-130">**Host Outside** – allows the application to be started outside of **Unified Service Desk**</span></span>  
  
           2. <span data-ttu-id="0e72e-131">**Use SetParent** – sets the application’s root window as the child window of **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="0e72e-131">**Use SetParent** – sets the application’s root window as the child window of **Unified Service Desk**.</span></span>  
  
           3. <span data-ttu-id="0e72e-132">**Use Dynamic Positioning** – monitors the size and position of the **Unified Service Desk** application and dynamically adjusts the size and position of the application.</span><span class="sxs-lookup"><span data-stu-id="0e72e-132">**Use Dynamic Positioning** – monitors the size and position of the **Unified Service Desk** application and dynamically adjusts the size and position of the application.</span></span>  
  
       1.  <span data-ttu-id="0e72e-133">Under **Web Application Home Page**,</span><span class="sxs-lookup"><span data-stu-id="0e72e-133">Under **Web Application Home Page**,</span></span>  
  
           1. <span data-ttu-id="0e72e-134">**URL** - specifies the URL where the application is running.</span><span class="sxs-lookup"><span data-stu-id="0e72e-134">**URL** - specifies the URL where the application is running.</span></span>  
  
           2. <span data-ttu-id="0e72e-135">**Use Toolbar** – when checked displays the Internet Explorer toolbar.</span><span class="sxs-lookup"><span data-stu-id="0e72e-135">**Use Toolbar** – when checked displays the Internet Explorer toolbar.</span></span>  
  
           3. <span data-ttu-id="0e72e-136">**Use New Browser Process** – when checked, initiates the application in a new Internet Explorer process.</span><span class="sxs-lookup"><span data-stu-id="0e72e-136">**Use New Browser Process** – when checked, initiates the application in a new Internet Explorer process.</span></span>  
  
           4. <span data-ttu-id="0e72e-137">**Manage Pop ups** – when checked, allows the pop-up windows to be managed in **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="0e72e-137">**Manage Pop ups** – when checked, allows the pop-up windows to be managed in **Unified Service Desk**.</span></span>  
  
   <span data-ttu-id="0e72e-138">![Web hosted application type](../unified-service-desk/media/usd-webhostedapp.PNG "Web hosted application type")</span><span class="sxs-lookup"><span data-stu-id="0e72e-138">![Web hosted application type](../unified-service-desk/media/usd-webhostedapp.PNG "Web hosted application type")</span></span>  
  
        For more information about how to build and host a web application in **Unified Service Desk**, see steps 1 to 3 of [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md)  
  
   3.  <span data-ttu-id="0e72e-139">For hosting an external application, select **External Hosted Application** type.</span><span class="sxs-lookup"><span data-stu-id="0e72e-139">For hosting an external application, select **External Hosted Application** type.</span></span> <span data-ttu-id="0e72e-140">Under **Hosting** area,</span><span class="sxs-lookup"><span data-stu-id="0e72e-140">Under **Hosting** area,</span></span>  
  
       1.  <span data-ttu-id="0e72e-141">Under the **External Application Settings** area,</span><span class="sxs-lookup"><span data-stu-id="0e72e-141">Under the **External Application Settings** area,</span></span>  
  
           1. <span data-ttu-id="0e72e-142">**External App URI** – Specifies the path of the executable.</span><span class="sxs-lookup"><span data-stu-id="0e72e-142">**External App URI** – Specifies the path of the executable.</span></span>  
  
           2. <span data-ttu-id="0e72e-143">**Arguments** – Specifies the arguments used during the application initiation.</span><span class="sxs-lookup"><span data-stu-id="0e72e-143">**Arguments** – Specifies the arguments used during the application initiation.</span></span>  
  
           3. <span data-ttu-id="0e72e-144">**Working Directory** – Specifies the working directory of the executable.</span><span class="sxs-lookup"><span data-stu-id="0e72e-144">**Working Directory** – Specifies the working directory of the executable.</span></span>  
  
           4. <span data-ttu-id="0e72e-145">**Manage Hosting** – Allows the hosting to be managed in **Unified Service Desk**</span><span class="sxs-lookup"><span data-stu-id="0e72e-145">**Manage Hosting** – Allows the hosting to be managed in **Unified Service Desk**</span></span>  
  
       2.  <span data-ttu-id="0e72e-146">Under **Application Hosting**,</span><span class="sxs-lookup"><span data-stu-id="0e72e-146">Under **Application Hosting**,</span></span>  
  
           1. <span data-ttu-id="0e72e-147">**Application Hosting** - same as 8a above.</span><span class="sxs-lookup"><span data-stu-id="0e72e-147">**Application Hosting** - same as 8a above.</span></span>  
  
           2. <span data-ttu-id="0e72e-148">**No Message Pump** – Specifies if the application has a Windows Messaging queue.</span><span class="sxs-lookup"><span data-stu-id="0e72e-148">**No Message Pump** – Specifies if the application has a Windows Messaging queue.</span></span>  
  
           3. <span data-ttu-id="0e72e-149">**Show Menu** – When checked, displays the system menu for the application.</span><span class="sxs-lookup"><span data-stu-id="0e72e-149">**Show Menu** – When checked, displays the system menu for the application.</span></span>  
  
           4. <span data-ttu-id="0e72e-150">**Main Window Acquisition Time out** – Specifies the timeout period for the top-level window handle to be found.</span><span class="sxs-lookup"><span data-stu-id="0e72e-150">**Main Window Acquisition Time out** – Specifies the timeout period for the top-level window handle to be found.</span></span>  
  
   <span data-ttu-id="0e72e-151">![External hosted appllication](../unified-service-desk/media/usd-exthostedapp.PNG "External hosted appllication")</span><span class="sxs-lookup"><span data-stu-id="0e72e-151">![External hosted appllication](../unified-service-desk/media/usd-exthostedapp.PNG "External hosted appllication")</span></span>  
  
        For more information about how to build and host an external application in **Unified Service Desk**, see steps 1 to 3 of [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md)  
  
   4. <span data-ttu-id="0e72e-152">For hosting a Citrix application, select **Remote Hosted Application** type.</span><span class="sxs-lookup"><span data-stu-id="0e72e-152">For hosting a Citrix application, select **Remote Hosted Application** type.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0e72e-153">[Integrate with Citrix applications](../unified-service-desk/integrate-citrix-applications.md)</span><span class="sxs-lookup"><span data-stu-id="0e72e-153">[Integrate with Citrix applications](../unified-service-desk/integrate-citrix-applications.md)</span></span>  
  
8. <span data-ttu-id="0e72e-154">In the **Common Properties** area,</span><span class="sxs-lookup"><span data-stu-id="0e72e-154">In the **Common Properties** area,</span></span>  
  
   1.  <span data-ttu-id="0e72e-155">When **Application is Global** is checked, the application is run globally and is independent from the session context.</span><span class="sxs-lookup"><span data-stu-id="0e72e-155">When **Application is Global** is checked, the application is run globally and is independent from the session context.</span></span>  
  
   2.  <span data-ttu-id="0e72e-156">The **Display Group** specifies where the application will be hosted in **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="0e72e-156">The **Display Group** specifies where the application will be hosted in **Unified Service Desk**.</span></span> <span data-ttu-id="0e72e-157">For example, MainPanel or WorkflowPanel.</span><span class="sxs-lookup"><span data-stu-id="0e72e-157">For example, MainPanel or WorkflowPanel.</span></span>  
  
   3.  <span data-ttu-id="0e72e-158">When **Dependent on Workflow** is checked, the application is only loaded through a workflow step.</span><span class="sxs-lookup"><span data-stu-id="0e72e-158">When **Dependent on Workflow** is checked, the application is only loaded through a workflow step.</span></span>  
  
   4. <span data-ttu-id="0e72e-159">**Minimum Size X** specifies the minimum size of the application window in **Unified Service Desk** along the X axis.</span><span class="sxs-lookup"><span data-stu-id="0e72e-159">**Minimum Size X** specifies the minimum size of the application window in **Unified Service Desk** along the X axis.</span></span>  
  
   5. <span data-ttu-id="0e72e-160">**Minimum Size Y** specifies the minimum size of the application window in **Unified Service Desk** along the Y axis.</span><span class="sxs-lookup"><span data-stu-id="0e72e-160">**Minimum Size Y** specifies the minimum size of the application window in **Unified Service Desk** along the Y axis.</span></span>  
  
   6. <span data-ttu-id="0e72e-161">**Optimal Size X** specifies the display size of the application in **Unified Service Desk** along the X axis.</span><span class="sxs-lookup"><span data-stu-id="0e72e-161">**Optimal Size X** specifies the display size of the application in **Unified Service Desk** along the X axis.</span></span>  
  
   7. <span data-ttu-id="0e72e-162">**Optimal Size Y** specifies the display size of the application in **Unified Service Desk** along the Y axis.</span><span class="sxs-lookup"><span data-stu-id="0e72e-162">**Optimal Size Y** specifies the display size of the application in **Unified Service Desk** along the Y axis.</span></span>  
  
   <span data-ttu-id="0e72e-163">![Common Properties screen of hosted control](../unified-service-desk/media/usd-commonproperties.PNG "Common Properties screen of hosted control")</span><span class="sxs-lookup"><span data-stu-id="0e72e-163">![Common Properties screen of hosted control](../unified-service-desk/media/usd-commonproperties.PNG "Common Properties screen of hosted control")</span></span>  
  
9. <span data-ttu-id="0e72e-164">In the **Dynamic** area, when the **Application is Dynamic** is checked, it means the application can be loaded dynamically and the **User Can Close** and the **Show in Toolbar Dropdown** check boxes become enabled.</span><span class="sxs-lookup"><span data-stu-id="0e72e-164">In the **Dynamic** area, when the **Application is Dynamic** is checked, it means the application can be loaded dynamically and the **User Can Close** and the **Show in Toolbar Dropdown** check boxes become enabled.</span></span>  
  
10. <span data-ttu-id="0e72e-165">In the **Adapter Configuration** section, there are three adapter configurations to choose from the **Adapter** drop-down list:</span><span class="sxs-lookup"><span data-stu-id="0e72e-165">In the **Adapter Configuration** section, there are three adapter configurations to choose from the **Adapter** drop-down list:</span></span>  
  
    1. <span data-ttu-id="0e72e-166">**Use No Adapter** – specifies that the hosted application does not require any automation.</span><span class="sxs-lookup"><span data-stu-id="0e72e-166">**Use No Adapter** – specifies that the hosted application does not require any automation.</span></span>  
  
    2. <span data-ttu-id="0e72e-167">**Use Automation Adapter (HAT)** – specifies the default configuration used for the Hosted Application Toolkit (HAT) Software Factory.</span><span class="sxs-lookup"><span data-stu-id="0e72e-167">**Use Automation Adapter (HAT)** – specifies the default configuration used for the Hosted Application Toolkit (HAT) Software Factory.</span></span>  
  
    3. <span data-ttu-id="0e72e-168">**Use Adapter** – Specifies that the hosted application uses a custom adapter.</span><span class="sxs-lookup"><span data-stu-id="0e72e-168">**Use Adapter** – Specifies that the hosted application uses a custom adapter.</span></span>  
  
         <span data-ttu-id="0e72e-169">To understand how to create and configure an external application adapter, see steps 4 to 6 of [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md).</span><span class="sxs-lookup"><span data-stu-id="0e72e-169">To understand how to create and configure an external application adapter, see steps 4 to 6 of [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md).</span></span>  
  
         <span data-ttu-id="0e72e-170">To understand how to create and configure a web application adapter, see steps 4 to 6 of [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md).</span><span class="sxs-lookup"><span data-stu-id="0e72e-170">To understand how to create and configure a web application adapter, see steps 4 to 6 of [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md).</span></span>  
  
11. <span data-ttu-id="0e72e-171">If the hosted application uses an Automation Adapter (HAT), the **Automation XML** in the **Automation** section contains the hosted application’s binding information.</span><span class="sxs-lookup"><span data-stu-id="0e72e-171">If the hosted application uses an Automation Adapter (HAT), the **Automation XML** in the **Automation** section contains the hosted application’s binding information.</span></span> <span data-ttu-id="0e72e-172">For more information about bindings, see [Use UII inspector to create bindings for the hosted application](../unified-service-desk/use-uii-inspector-create-bindings-hosted-application.md).</span><span class="sxs-lookup"><span data-stu-id="0e72e-172">For more information about bindings, see [Use UII inspector to create bindings for the hosted application](../unified-service-desk/use-uii-inspector-create-bindings-hosted-application.md).</span></span>  
  
12. <span data-ttu-id="0e72e-173">In the **Extensions** section, specify additional configuration information for your hosted control.</span><span class="sxs-lookup"><span data-stu-id="0e72e-173">In the **Extensions** section, specify additional configuration information for your hosted control.</span></span> <span data-ttu-id="0e72e-174">For an example of the Extentions XML configuration, see the definition of the Kpi hosted control.</span><span class="sxs-lookup"><span data-stu-id="0e72e-174">For an example of the Extentions XML configuration, see the definition of the Kpi hosted control.</span></span> <span data-ttu-id="0e72e-175">Kpi hosted control is one of the sample applications that is shipped with **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="0e72e-175">Kpi hosted control is one of the sample applications that is shipped with **Unified Service Desk**.</span></span>  
  
13. <span data-ttu-id="0e72e-176">Click **Save** to create the hosted application.</span><span class="sxs-lookup"><span data-stu-id="0e72e-176">Click **Save** to create the hosted application.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="0e72e-177">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="0e72e-177">See also</span></span>  
 <span data-ttu-id="0e72e-178">[Integrate with external applications and web applications](../unified-service-desk/integrate-external-applications-web-applications.md) </span><span class="sxs-lookup"><span data-stu-id="0e72e-178">[Integrate with external applications and web applications](../unified-service-desk/integrate-external-applications-web-applications.md) </span></span>  
 [<span data-ttu-id="0e72e-179">Integrate with Citrix applications</span><span class="sxs-lookup"><span data-stu-id="0e72e-179">Integrate with Citrix applications</span></span>](../unified-service-desk/integrate-citrix-applications.md)
