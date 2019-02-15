---
title: Install, deploy, and upgrade Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn how to install or upgrade Unified Service Desk for Dynamics 365 for Customer Engagement apps.
ms.custom:
- dyn365-USD, dyn365-admin
ms.date: 08/23/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: e0fd70b6-73a4-4426-92d7-bb300457597e
author: kabala123
ms.author: kabala
manager: shujoshi
tags:
- MigrationHO
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 103b8a0d4930405e07942459b9fe11d786f179b5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382441"
---
# <a name="install-deploy-and-upgrade-unified-service-desk"></a><span data-ttu-id="bf770-103">Install, deploy, and upgrade Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="bf770-103">Install, deploy, and upgrade Unified Service Desk</span></span>
<span data-ttu-id="bf770-104">Before you can install and deploy [!INCLUDE[pn_unified_service_desk_for_crm](../../includes/pn-unified-service-desk-for-crm.md)], you must identify the [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps instance that you want to build and deploy the configuration on.</span><span class="sxs-lookup"><span data-stu-id="bf770-104">Before you can install and deploy [!INCLUDE[pn_unified_service_desk_for_crm](../../includes/pn-unified-service-desk-for-crm.md)], you must identify the [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps instance that you want to build and deploy the configuration on.</span></span> <span data-ttu-id="bf770-105">While you can use a new [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] works best when the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] customization is mostly complete.</span><span class="sxs-lookup"><span data-stu-id="bf770-105">While you can use a new [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] works best when the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] customization is mostly complete.</span></span> [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="bf770-106">controls the call center agent’s view of [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] by manipulating windows, injecting [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)], and so on.</span><span class="sxs-lookup"><span data-stu-id="bf770-106">controls the call center agent’s view of [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] by manipulating windows, injecting [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)], and so on.</span></span> <span data-ttu-id="bf770-107">Nếu những thay đổi lớn xảy ra đối với môi trường [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] sau khi [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] được triển khai, nó có thể làm cho cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] của bạn không còn hoạt động theo yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="bf770-107">If major changes occur to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] environment after [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] is deployed, it might cause your [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration to no longer work as required.</span></span> <span data-ttu-id="bf770-108">While the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration often comes later in a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] implementation, having [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] in mind when designing your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] environment is beneficial.</span><span class="sxs-lookup"><span data-stu-id="bf770-108">While the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration often comes later in a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] implementation, having [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] in mind when designing your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] environment is beneficial.</span></span>  
  
 <span data-ttu-id="bf770-109">Cài đặt và triển khai [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] được thực hiện trong giai đoạn nơi ban đầu bạn thiết lập một môi trường phát triển để đặt cấu hình ứng dụng tổng đài viên bằng cách sử dụng một trong các ứng dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mẫu làm cơ sở.</span><span class="sxs-lookup"><span data-stu-id="bf770-109">[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] installation and deployment is done in phases where initially you set up a development environment to configure agent applications using one of the sample [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] applications as the base.</span></span> <span data-ttu-id="bf770-110">Next, you test how your configurations appear and work using the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application by connecting to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance where you configured [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="bf770-110">Next, you test how your configurations appear and work using the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application by connecting to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance where you configured [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="bf770-111">Next, you use the customized [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration on to a Production instance of [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], and the client application.</span><span class="sxs-lookup"><span data-stu-id="bf770-111">Next, you use the customized [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration on to a Production instance of [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], and the client application.</span></span> <span data-ttu-id="bf770-112">The configuration includes the Customization Files package used to distribute to your agent’s computers any files and assemblies that are required.</span><span class="sxs-lookup"><span data-stu-id="bf770-112">The configuration includes the Customization Files package used to distribute to your agent’s computers any files and assemblies that are required.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="bf770-113">Bạn có thể cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] để tích hợp với các ứng dụng ngành nghề kinh doanh của bên thứ ba (LOB).</span><span class="sxs-lookup"><span data-stu-id="bf770-113">You can configure [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to integrate with third-party line-of-business (LOB) applications.</span></span> <span data-ttu-id="bf770-114">However, before deploying an integrated solution (involving [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and LOB applications) in the production environment in your organization, you must thoroughly test your integrated solution to ensure that the performance results are aligned with your expectations.</span><span class="sxs-lookup"><span data-stu-id="bf770-114">However, before deploying an integrated solution (involving [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and LOB applications) in the production environment in your organization, you must thoroughly test your integrated solution to ensure that the performance results are aligned with your expectations.</span></span> [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="bf770-115">might not function appropriately if integrated with LOB applications that demonstrate user interface (UI) blocking, memory leak issues, and slow response times.</span><span class="sxs-lookup"><span data-stu-id="bf770-115">might not function appropriately if integrated with LOB applications that demonstrate user interface (UI) blocking, memory leak issues, and slow response times.</span></span>  
  
 <span data-ttu-id="bf770-116">Liệt kê dưới đây là trình tự mà chúng tôi khuyên bạn nên cài đặt và triển khai [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] trong tổ chức của bạn.</span><span class="sxs-lookup"><span data-stu-id="bf770-116">Listed below is the sequence that we recommend for installing and deploying [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] in your organization.</span></span> <span data-ttu-id="bf770-117">Before installing [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], ensure that you meet the system requirements: [Unified Service Desk system requirements](../../unified-service-desk/admin/unified-service-desk-system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bf770-117">Before installing [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], ensure that you meet the system requirements: [Unified Service Desk system requirements](../../unified-service-desk/admin/unified-service-desk-system-requirements.md).</span></span>  
  
## <a name="step-1-initial-installation-and-deployment"></a><span data-ttu-id="bf770-118">Bước 1: Cài đặt và triển khai đầu tiên</span><span class="sxs-lookup"><span data-stu-id="bf770-118">Step 1: Initial installation and deployment</span></span>  
 <span data-ttu-id="bf770-119">Xác định máy chủ [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] mà bạn muốn triển khai [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] và một máy tính phát triển sẽ được sử dụng cho triển khai gói [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] và sau đó kết nối với các gói bằng cách sử dụng ứng dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="bf770-119">Identify a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] server where you want to deploy [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and a development computer that will be used for deploying [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] packages and then connecting to the packages by using the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.</span></span>  
  
1. <span data-ttu-id="bf770-120">Cài đặt ứng dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] trên máy tính phát triển.</span><span class="sxs-lookup"><span data-stu-id="bf770-120">Install the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client on the development computer.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="bf770-121">[Install the Unified Service Desk Client](../../unified-service-desk/admin/install-upgrade-unified-service-desk-client.md)</span><span class="sxs-lookup"><span data-stu-id="bf770-121">[Install the Unified Service Desk Client](../../unified-service-desk/admin/install-upgrade-unified-service-desk-client.md)</span></span>  
  
2. <span data-ttu-id="bf770-122">Triển khai gói [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] cho phiên bản [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="bf770-122">Deploy [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] packages to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="bf770-123">[Deploy Unified Service Desk packages to Dynamics 365 for Customer Engagement server using Package Deployer](../../unified-service-desk/admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md)</span><span class="sxs-lookup"><span data-stu-id="bf770-123">[Deploy Unified Service Desk packages to Dynamics 365 for Customer Engagement server using Package Deployer](../../unified-service-desk/admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md)</span></span>  
  
3. <span data-ttu-id="bf770-124">Run the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client, and connect to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance where you deployed the packages to verify that everything is working correctly.</span><span class="sxs-lookup"><span data-stu-id="bf770-124">Run the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client, and connect to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance where you deployed the packages to verify that everything is working correctly.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="bf770-125">[Connect to Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)</span><span class="sxs-lookup"><span data-stu-id="bf770-125">[Connect to Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)</span></span>  
  
   <span data-ttu-id="bf770-126">**Thiết lập máy tính phát triển thêm**</span><span class="sxs-lookup"><span data-stu-id="bf770-126">**Set up additional development computers**</span></span>  
  
   <span data-ttu-id="bf770-127">To set up additional development computers for configuring your agent desktop applications using [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], install the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client on the computer.</span><span class="sxs-lookup"><span data-stu-id="bf770-127">To set up additional development computers for configuring your agent desktop applications using [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], install the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client on the computer.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="bf770-128">[Install Unified Service Desk Client](../../unified-service-desk/admin/install-upgrade-deploy-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="bf770-128">[Install Unified Service Desk Client](../../unified-service-desk/admin/install-upgrade-deploy-unified-service-desk.md)</span></span>  
  
## <a name="step-2-configure-and-test-your-agent-application"></a><span data-ttu-id="bf770-129">Bước 2: Đặt cấu hình và kiểm tra ứng dụng tổng đài viên của bạn</span><span class="sxs-lookup"><span data-stu-id="bf770-129">Step 2: Configure and test your agent application</span></span>  
 <span data-ttu-id="bf770-130">Use your development environment to configure your agent application by building on one of the available sample applications you deployed, and then test it by connecting to the customized package using the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application.</span><span class="sxs-lookup"><span data-stu-id="bf770-130">Use your development environment to configure your agent application by building on one of the available sample applications you deployed, and then test it by connecting to the customized package using the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="bf770-131">[Use Unified Service Desk to configure your agent application](../../unified-service-desk/configure-agent-application-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="bf770-131">[Use Unified Service Desk to configure your agent application](../../unified-service-desk/configure-agent-application-unified-service-desk.md)</span></span>  
  
## <a name="step-3-deploy-the-customized-agent-application"></a><span data-ttu-id="bf770-132">Bước 3: Triển khai ứng dụng đại lý tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="bf770-132">Step 3: Deploy the customized agent application</span></span>  
 <span data-ttu-id="bf770-133">Sau khi bạn đã tùy chỉnh ứng dụng đại lý của bạn thông qua các cấu hình hoặc mã tùy chỉnh, bạn phải cài đặt ứng dụng khách hàng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]cùng với bất kỳ tập tin cần thiết cho các chức năng tùy chỉnh trên máy tính của đại lý của bạn.</span><span class="sxs-lookup"><span data-stu-id="bf770-133">After you have customized your agent application through configuration or custom code, you must install the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application along with any files required for the custom functionality on your agent’s computers.</span></span> <span data-ttu-id="bf770-134">Consider creating a [!INCLUDE[pn_clickonce](../../includes/pn-clickonce.md)] application or an MSI package installer to bundle all the files together and deploy on the agent computers in your organization.</span><span class="sxs-lookup"><span data-stu-id="bf770-134">Consider creating a [!INCLUDE[pn_clickonce](../../includes/pn-clickonce.md)] application or an MSI package installer to bundle all the files together and deploy on the agent computers in your organization.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="bf770-135">see [MSDN: ClickOnce Security and Deployment](http://msdn.microsoft.com/library/t71a733d.aspx) or [MSDN: Windows Installer](http://msdn.microsoft.com/library/cc185688\(v=vs.85\).aspx)</span><span class="sxs-lookup"><span data-stu-id="bf770-135">see [MSDN: ClickOnce Security and Deployment](http://msdn.microsoft.com/library/t71a733d.aspx) or [MSDN: Windows Installer](http://msdn.microsoft.com/library/cc185688\(v=vs.85\).aspx)</span></span>  
  
 <span data-ttu-id="bf770-136">Bạn cũng có thể muốn di chuyển cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] của bạn từ một bài kiểm tra/phát triển đến một môi trường sản xuất.</span><span class="sxs-lookup"><span data-stu-id="bf770-136">You might also want to migrate your [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration from a development/test to a production environment.</span></span> <span data-ttu-id="bf770-137">Bạn có thể sử dụng [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)] mới để di chuyển dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] giữa phiên bản [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="bf770-137">You can use the new [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)] to migrate your [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration data across [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="bf770-138">[Migrate your Unified Service Desk configuration to another Dynamics 365 for Customer Engagement server](../../unified-service-desk/admin/migrate-unified-service-desk-configuration-dynamics-365-server.md)</span><span class="sxs-lookup"><span data-stu-id="bf770-138">[Migrate your Unified Service Desk configuration to another Dynamics 365 for Customer Engagement server](../../unified-service-desk/admin/migrate-unified-service-desk-configuration-dynamics-365-server.md)</span></span>  
    
  
## <a name="see-also"></a><span data-ttu-id="bf770-139">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="bf770-139">See also</span></span>  
 [<span data-ttu-id="bf770-140">Yêu cầu hệ thống Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="bf770-140">Unified Service Desk system requirements</span></span>](../../unified-service-desk/admin/unified-service-desk-system-requirements.md)  
  
 [<span data-ttu-id="bf770-141">Cài đặt ứng dụng Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="bf770-141">Install Unified Service Desk Client</span></span>](../../unified-service-desk/admin/install-upgrade-unified-service-desk-client.md)  
  
 [<span data-ttu-id="bf770-142">Deploy sample Unified Service Desk applications to Dynamics 365 for Customer Engagement server using Package Deployer</span><span class="sxs-lookup"><span data-stu-id="bf770-142">Deploy sample Unified Service Desk applications to Dynamics 365 for Customer Engagement server using Package Deployer</span></span>](../../unified-service-desk/admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md)  
  
 [<span data-ttu-id="bf770-143">Connect to Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client</span><span class="sxs-lookup"><span data-stu-id="bf770-143">Connect to Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client</span></span>](../../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)   
 