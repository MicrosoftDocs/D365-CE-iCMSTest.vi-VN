---
title: Support for Unified Interface apps in Unified Service Desk (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about the Unified Interface apps supportability in Unified Service Desk.
keywords: ''
ms.date: 05/07/2018
ms.service:
- usd
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 7ECEC924-5089-4D9C-88B3-50D1BD7B03A9
author: kabala123
ms.author: kabala
manager: shujoshi
ms.openlocfilehash: c08708881600c49e283bb80e9bf573b775178eb0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382402"
---
# <a name="preview-feature-support-for-unified-interface-apps-in-unified-service-desk"></a><span data-ttu-id="02b24-103">Preview feature: Support for Unified Interface Apps in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="02b24-103">Preview feature: Support for Unified Interface Apps in Unified Service Desk</span></span>

<span data-ttu-id="02b24-104">With the release [!INCLUDE[pn-unified-service-desk-3-3](../../includes/pn-unified-service-desk-3-3.md)], [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] supports the Apps built using Unified Interface framework.</span><span class="sxs-lookup"><span data-stu-id="02b24-104">With the release [!INCLUDE[pn-unified-service-desk-3-3](../../includes/pn-unified-service-desk-3-3.md)], [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] supports the Apps built using Unified Interface framework.</span></span>

## <a name="what-is-unified-interface"></a><span data-ttu-id="02b24-105">What is Unified Interface?</span><span class="sxs-lookup"><span data-stu-id="02b24-105">What is Unified Interface?</span></span>

<span data-ttu-id="02b24-106">With the release of Dynamics 365 for Customer Engagement apps version 9.0, we have introduced a new user experience - Unified Interface - which uses responsive web design principles to provide an optimal viewing and interaction experience for any screen size, device, or orientation.</span><span class="sxs-lookup"><span data-stu-id="02b24-106">With the release of Dynamics 365 for Customer Engagement apps version 9.0, we have introduced a new user experience - Unified Interface - which uses responsive web design principles to provide an optimal viewing and interaction experience for any screen size, device, or orientation.</span></span>

<span data-ttu-id="02b24-107">Giao diện Hợp nhất mới đem đến tất cả trải nghiệm phong phú dành cho mọi máy khách mà bạn đang sử dụng.</span><span class="sxs-lookup"><span data-stu-id="02b24-107">The new Unified Interface brings all the rich experiences to any client that you are using.</span></span> <span data-ttu-id="02b24-108">Cho dù đang sử dụng trình duyệt, máy tính bảng hay điện thoại, bạn đều có thể trải nghiệm những điều tương tự.</span><span class="sxs-lookup"><span data-stu-id="02b24-108">Whether you are on a browser, tablet, or phone, you will be able to consume similar experiences.</span></span> <span data-ttu-id="02b24-109">More Information: [About Unified Interface](/dynamics365/customer-engagement/admin/about-unified-interface)</span><span class="sxs-lookup"><span data-stu-id="02b24-109">More Information: [About Unified Interface](/dynamics365/customer-engagement/admin/about-unified-interface)</span></span>

## <a name="what-is-unified-interface-supportability-in-unified-service-desk"></a><span data-ttu-id="02b24-110">What is Unified Interface supportability in Unified Service Desk?</span><span class="sxs-lookup"><span data-stu-id="02b24-110">What is Unified Interface supportability in Unified Service Desk?</span></span>

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="02b24-111">supports the apps built using Unified Interface framework.</span><span class="sxs-lookup"><span data-stu-id="02b24-111">supports the apps built using Unified Interface framework.</span></span> <span data-ttu-id="02b24-112">That is, you can host a Unified Interface Page to load a URL or page from Dynamics 365 for Customer Engagement apps, which is built based on the Unified Interface framework.</span><span class="sxs-lookup"><span data-stu-id="02b24-112">That is, you can host a Unified Interface Page to load a URL or page from Dynamics 365 for Customer Engagement apps, which is built based on the Unified Interface framework.</span></span>

<span data-ttu-id="02b24-113">The experience of the supportability is that the Unified Interface Page hosted control type exposes number of predefined UII actions and events that are unique to handling of Dynamics 365 for Customer Engagement apps windows built using Unified Interface framework including list manipulation actions, and a find action for displaying a quick search or advanced search page.</span><span class="sxs-lookup"><span data-stu-id="02b24-113">The experience of the supportability is that the Unified Interface Page hosted control type exposes number of predefined UII actions and events that are unique to handling of Dynamics 365 for Customer Engagement apps windows built using Unified Interface framework including list manipulation actions, and a find action for displaying a quick search or advanced search page.</span></span>

## <a name="deploy-the-unified-interface-sample-application"></a><span data-ttu-id="02b24-114">Deploy the Unified Interface sample application</span><span class="sxs-lookup"><span data-stu-id="02b24-114">Deploy the Unified Interface sample application</span></span>

[!INCLUDE[pn_unified_service_desk_for_crm](../../includes/pn-unified-service-desk-for-crm.md)] <span data-ttu-id="02b24-115">comes with  sample applications that you can use as the base for starting with your configuration of your agent application.</span><span class="sxs-lookup"><span data-stu-id="02b24-115">comes with  sample applications that you can use as the base for starting with your configuration of your agent application.</span></span>  
  
 <span data-ttu-id="02b24-116">The Unified Interface sample application is bundled as a package that you need to deploy on a [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps instance before you can start working.</span><span class="sxs-lookup"><span data-stu-id="02b24-116">The Unified Interface sample application is bundled as a package that you need to deploy on a [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps instance before you can start working.</span></span> <span data-ttu-id="02b24-117">The deployment of the Unified Interface sample application package is performed using [!INCLUDE[pn_package_deployer_long](../../includes/pn-package-deployer-long.md)].</span><span class="sxs-lookup"><span data-stu-id="02b24-117">The deployment of the Unified Interface sample application package is performed using [!INCLUDE[pn_package_deployer_long](../../includes/pn-package-deployer-long.md)].</span></span> <span data-ttu-id="02b24-118">After the deployment, the entities and custom code specific to [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] become available in the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance.</span><span class="sxs-lookup"><span data-stu-id="02b24-118">After the deployment, the entities and custom code specific to [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] become available in the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance.</span></span>

<span data-ttu-id="02b24-119">To deploy the Unified Interface sample application package, refer [Deploy a sample Unified Service Desk package using Package Deployer](../admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md)</span><span class="sxs-lookup"><span data-stu-id="02b24-119">To deploy the Unified Interface sample application package, refer [Deploy a sample Unified Service Desk package using Package Deployer](../admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md)</span></span>

::: moniker range="dynamics-usd-3"
## <a name="configure-application-selection-window-in-unified-service-desk"></a><span data-ttu-id="02b24-120">Configure application selection window in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="02b24-120">Configure application selection window in Unified Service Desk</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02b24-121">This section is only applicable to Unified Service Desk 3.3.</span><span class="sxs-lookup"><span data-stu-id="02b24-121">This section is only applicable to Unified Service Desk 3.3.</span></span>

<span data-ttu-id="02b24-122">A application selection is introduced to ensure that you can select Web or Unified Interface app as per your business requirement.</span><span class="sxs-lookup"><span data-stu-id="02b24-122">A application selection is introduced to ensure that you can select Web or Unified Interface app as per your business requirement.</span></span>

<span data-ttu-id="02b24-123">The application selection window appears when you login to [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="02b24-123">The application selection window appears when you login to [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="02b24-124">To enable the application selection window, you must update a **SelectAppModule** key under the **\<appSettings>** section of the **UnifiedServiceDesk.exe.config** (application configuration) file and set it to **true**.</span><span class="sxs-lookup"><span data-stu-id="02b24-124">To enable the application selection window, you must update a **SelectAppModule** key under the **\<appSettings>** section of the **UnifiedServiceDesk.exe.config** (application configuration) file and set it to **true**.</span></span>

### <a name="add-the-application-selection-window-key"></a><span data-ttu-id="02b24-125">Add the application selection window key</span><span class="sxs-lookup"><span data-stu-id="02b24-125">Add the application selection window key</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02b24-126">This section is only applicable to Unified Service Desk 3.3.</span><span class="sxs-lookup"><span data-stu-id="02b24-126">This section is only applicable to Unified Service Desk 3.3.</span></span>

1. <span data-ttu-id="02b24-127">Truy cập `C:\Program Files\Microsoft Dynamics CRM USD\USD`.</span><span class="sxs-lookup"><span data-stu-id="02b24-127">Go to `C:\Program Files\Microsoft Dynamics CRM USD\USD`.</span></span>
2. <span data-ttu-id="02b24-128">Select **UnifiedServiceDesk.exe.config** file.</span><span class="sxs-lookup"><span data-stu-id="02b24-128">Select **UnifiedServiceDesk.exe.config** file.</span></span>
3. <span data-ttu-id="02b24-129">Under the **\<appSettings>** section, type the key.</span><span class="sxs-lookup"><span data-stu-id="02b24-129">Under the **\<appSettings>** section, type the key.</span></span><br>
`<add key="SelectAppModule" value="true"/>`<br>
  <span data-ttu-id="02b24-130">![Update SelectAppModule key in the UnifiedServiceDesk.exe.config file](../media/selectappmodule-app-config-file.PNG "Update SelectAppModule key in the UnifiedServiceDesk.exe.config file")</span><span class="sxs-lookup"><span data-stu-id="02b24-130">![Update SelectAppModule key in the UnifiedServiceDesk.exe.config file](../media/selectappmodule-app-config-file.PNG "Update SelectAppModule key in the UnifiedServiceDesk.exe.config file")</span></span>
4. <span data-ttu-id="02b24-131">Lưu tệp.</span><span class="sxs-lookup"><span data-stu-id="02b24-131">Save the file.</span></span>

### <a name="login-to-unified-service-desk-client-application"></a><span data-ttu-id="02b24-132">Login to Unified Service Desk client application</span><span class="sxs-lookup"><span data-stu-id="02b24-132">Login to Unified Service Desk client application</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02b24-133">This section is only applicable to Unified Service Desk 3.3.</span><span class="sxs-lookup"><span data-stu-id="02b24-133">This section is only applicable to Unified Service Desk 3.3.</span></span>

<span data-ttu-id="02b24-134">After you update the **SelectAppModule** key in the **UnifiedServiceDesk.exe.config** file, you need to login to [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to select an web or Unified Interface app.</span><span class="sxs-lookup"><span data-stu-id="02b24-134">After you update the **SelectAppModule** key in the **UnifiedServiceDesk.exe.config** file, you need to login to [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to select an web or Unified Interface app.</span></span>

<span data-ttu-id="02b24-135">![Select App Module](../media/select-app-module-new.PNG "Select App Module")</span><span class="sxs-lookup"><span data-stu-id="02b24-135">![Select App Module](../media/select-app-module-new.PNG "Select App Module")</span></span>

::: moniker-end

## <a name="see-also"></a><span data-ttu-id="02b24-136">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="02b24-136">See also</span></span>
 <span data-ttu-id="02b24-137">[Unified Interface Page (Hosted Control)](../../unified-service-desk/unified-interface-page-hosted-control.md) [Unified Service Desk and Unified Interface Configuration Walkthroughs](../../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md) [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md) [Walkthrough 2: Display an external webpage in your agent application](../../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="02b24-137">[Unified Interface Page (Hosted Control)](../../unified-service-desk/unified-interface-page-hosted-control.md) [Unified Service Desk and Unified Interface Configuration Walkthroughs](../../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md) [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md) [Walkthrough 2: Display an external webpage in your agent application](../../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md) </span></span>  
 <span data-ttu-id="02b24-138">[Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="02b24-138">[Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md) </span></span>  
 <span data-ttu-id="02b24-139">[Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="02b24-139">[Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md) </span></span>  
 <span data-ttu-id="02b24-140">[Cách 5: Hiển thị thông tin phiên bổ sung bằng cách hiển thị tên và dữ liệu tổng quan về phiên](../../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md) </span><span class="sxs-lookup"><span data-stu-id="02b24-140">[Walkthrough 5: Display enhanced session information by displaying session name and overview data](../../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md) </span></span>  
 <span data-ttu-id="02b24-141">[Walkthrough 6: Configure the Debugger hosted control in your agent application](../../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md) [Walkthrough 7: Configure agent scripting in your agent application](../../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md)</span><span class="sxs-lookup"><span data-stu-id="02b24-141">[Walkthrough 6: Configure the Debugger hosted control in your agent application](../../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md) [Walkthrough 7: Configure agent scripting in your agent application](../../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md)</span></span>
