---
title: Update Unified Service Desk for Dynamics 365 for Customer Engagement apps solution | MicrosoftDocs
description: Learn how to update Unified Service Desk for Dynamics 365 for Customer Engagement apps.
keywords: ''
ms.date: 08/23/2017
ms.service:
- dynamics-365-customerservice
ms.custom:
- dyn365-USD, dyn365-admin
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: d3773029-8b2f-4aa3-9317-abc309b01960
author: kabala123
ms.author: kabala
manager: shujoshi
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 136d722b61b02fb3d550c62610f63bf987dd1894
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382435"
---
# <a name="updating-the-solution"></a><span data-ttu-id="d95cb-103">Updating the solution</span><span class="sxs-lookup"><span data-stu-id="d95cb-103">Updating the solution</span></span>
<span data-ttu-id="d95cb-104">Read this topic only if you have an existing installation of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] from the previous release of [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps, and want to update to the [!INCLUDE[pn_crm_2016](../../includes/pn-crm-2016.md)] release.</span><span class="sxs-lookup"><span data-stu-id="d95cb-104">Read this topic only if you have an existing installation of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] from the previous release of [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps, and want to update to the [!INCLUDE[pn_crm_2016](../../includes/pn-crm-2016.md)] release.</span></span>  
  
 <span data-ttu-id="d95cb-105">Nếu bạn đang cài đặt [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] lần đầu tiên, bạn có thể bỏ qua chủ đề này.</span><span class="sxs-lookup"><span data-stu-id="d95cb-105">If you’re installing [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] for the first time, you can skip this topic.</span></span>  
  
<a name="check"></a>   
## <a name="check-if-you-need-to-update-the-unified-service-desk-solution"></a><span data-ttu-id="d95cb-106">Check if you need to update the Unified Service Desk solution</span><span class="sxs-lookup"><span data-stu-id="d95cb-106">Check if you need to update the Unified Service Desk solution</span></span>  
 <span data-ttu-id="d95cb-107">Nếu bạn không chắc chắn cho dù bạn cần phải cập nhật cài đặt [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] của bạn, kiểm tra các phiên bản sau để chắc chắn.</span><span class="sxs-lookup"><span data-stu-id="d95cb-107">If you’re unsure whether you need to update your [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] installation, check the following versions to be sure.</span></span>  
  
### <a name="check-the-unified-service-desk-solution-version"></a><span data-ttu-id="d95cb-108">Kiểm tra phiên bản giải pháp Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="d95cb-108">Check the Unified Service Desk solution version</span></span>  
 <span data-ttu-id="d95cb-109">In your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance, navigate to **[!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps** > **Settings** > **Solutions**.</span><span class="sxs-lookup"><span data-stu-id="d95cb-109">In your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance, navigate to **[!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps** > **Settings** > **Solutions**.</span></span> <span data-ttu-id="d95cb-110">Nếu số phiên bản của các giải pháp phù hợp với những giải pháp trong bảng, bạn có phiên bản mới nhất của [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], và không cần phải Cập Nhật.</span><span class="sxs-lookup"><span data-stu-id="d95cb-110">If the version numbers of the solutions match those in the table, you have the latest version of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], and don’t need to update.</span></span>  
  
|<span data-ttu-id="d95cb-111">Tên Giải pháp</span><span class="sxs-lookup"><span data-stu-id="d95cb-111">Solution name</span></span>|<span data-ttu-id="d95cb-112">Phiên bản</span><span class="sxs-lookup"><span data-stu-id="d95cb-112">Version</span></span>|  
|-------------------|-------------|  
|<span data-ttu-id="d95cb-113">UiiForMicrosoftDynamicsCRM2011</span><span class="sxs-lookup"><span data-stu-id="d95cb-113">UiiForMicrosoftDynamicsCRM2011</span></span>|<span data-ttu-id="d95cb-114">4.0.0.xxx</span><span class="sxs-lookup"><span data-stu-id="d95cb-114">4.0.0.xxx</span></span>|  
|<span data-ttu-id="d95cb-115">DynamicsUnifiedServiceDesk</span><span class="sxs-lookup"><span data-stu-id="d95cb-115">DynamicsUnifiedServiceDesk</span></span>|<span data-ttu-id="d95cb-116">4.0.0.xxx</span><span class="sxs-lookup"><span data-stu-id="d95cb-116">4.0.0.xxx</span></span>|
  
<a name="UpdateSolutions"></a>   
## <a name="update-unified-service-desk-solutions"></a><span data-ttu-id="d95cb-117">Cập nhật giải pháp Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="d95cb-117">Update Unified Service Desk solutions</span></span>  
 <span data-ttu-id="d95cb-118">Before you update your [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] solutions, ensure that the version of your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] on-premises organization is [!INCLUDE[pn_crm_2016](../../includes/pn-crm-2016.md)], [!INCLUDE[pn_crm_2015_shortest](../../includes/pn-crm-2015-shortest.md)], or [!INCLUDE[pn_crm_2013_sp_shortest](../../includes/pn-crm-2013-sp-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="d95cb-118">Before you update your [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] solutions, ensure that the version of your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] on-premises organization is [!INCLUDE[pn_crm_2016](../../includes/pn-crm-2016.md)], [!INCLUDE[pn_crm_2015_shortest](../../includes/pn-crm-2015-shortest.md)], or [!INCLUDE[pn_crm_2013_sp_shortest](../../includes/pn-crm-2013-sp-shortest.md)].</span></span>  
  
1. <span data-ttu-id="d95cb-119">[Download the Unified Service Desk package file](http://go.microsoft.com/fwlink/p/?LinkID=2007340) (CRM2016-8.x.x-USD-PackageDeployer.exe), and save it on your computer.</span><span class="sxs-lookup"><span data-stu-id="d95cb-119">[Download the Unified Service Desk package file](http://go.microsoft.com/fwlink/p/?LinkID=2007340) (CRM2016-8.x.x-USD-PackageDeployer.exe), and save it on your computer.</span></span>  
  
2. <span data-ttu-id="d95cb-120">Chạy các tập tin đã tải về để trích xuất nội dung vào một thư mục.</span><span class="sxs-lookup"><span data-stu-id="d95cb-120">Run the downloaded file to extract the contents into a folder.</span></span>  
  
3. <span data-ttu-id="d95cb-121">Sau khi tệp được giải nén, nếu [!INCLUDE[pn_package_deployer_tool](../../includes/pn-package-deployer-tool.md)] bắt đầu tự động, hãy đóng lại.</span><span class="sxs-lookup"><span data-stu-id="d95cb-121">After the files are extracted, if the [!INCLUDE[pn_package_deployer_tool](../../includes/pn-package-deployer-tool.md)] starts automatically, close it.</span></span>  
  
4. <span data-ttu-id="d95cb-122">In the extracted folder, locate the following two solution files in the USDPackageDeployer\\*\<PackageName>* folder, where *\<PackageName>* is the name of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] package you currently have installed in your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance:</span><span class="sxs-lookup"><span data-stu-id="d95cb-122">In the extracted folder, locate the following two solution files in the USDPackageDeployer\\*\<PackageName>* folder, where *\<PackageName>* is the name of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] package you currently have installed in your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance:</span></span>  
  
   - <span data-ttu-id="d95cb-123">UiiForMicrosoftDynamicsCRM_3_0_managed.zip</span><span class="sxs-lookup"><span data-stu-id="d95cb-123">UiiForMicrosoftDynamicsCRM_3_0_managed.zip</span></span>  
  
   - <span data-ttu-id="d95cb-124">DynamicsUnifiedServiceDesk_1_0_managed.zip</span><span class="sxs-lookup"><span data-stu-id="d95cb-124">DynamicsUnifiedServiceDesk_1_0_managed.zip</span></span> 

   - <span data-ttu-id="d95cb-125">UnifiedInterfaceDemoCustomization_1_0_managed.zip</span><span class="sxs-lookup"><span data-stu-id="d95cb-125">UnifiedInterfaceDemoCustomization_1_0_managed.zip</span></span> 
  
     <span data-ttu-id="d95cb-126">Ví dụ, nếu bạn đã cài đặt gói cơ sở, bạn phải di chuyển vào thư mục USDPackageDeployer\BasePackage để tìm tập tin giải pháp cho việc Cập Nhật.</span><span class="sxs-lookup"><span data-stu-id="d95cb-126">For example, if you currently have Base package installed, you must navigate to the USDPackageDeployer\BasePackage folder to find the solution files for updating.</span></span> <span data-ttu-id="d95cb-127">Similarly, navigate to the USDPackageDeployer\CRM2013SP1Package folder if you have the [!INCLUDE[pn_crm_2013_sp_shortest](../../includes/pn-crm-2013-sp-shortest.md)] package, to the USDPackageDeployer\CRM2013SP1withProductUpdatesPackage folder if you have the [!INCLUDE[pn_crm_2013_sp_shortest](../../includes/pn-crm-2013-sp-shortest.md)] with Product Updates package, and USDPackageDeployer\ParatureKnowledgeManagementPackage folder if you have the Knowledge Management package.</span><span class="sxs-lookup"><span data-stu-id="d95cb-127">Similarly, navigate to the USDPackageDeployer\CRM2013SP1Package folder if you have the [!INCLUDE[pn_crm_2013_sp_shortest](../../includes/pn-crm-2013-sp-shortest.md)] package, to the USDPackageDeployer\CRM2013SP1withProductUpdatesPackage folder if you have the [!INCLUDE[pn_crm_2013_sp_shortest](../../includes/pn-crm-2013-sp-shortest.md)] with Product Updates package, and USDPackageDeployer\ParatureKnowledgeManagementPackage folder if you have the Knowledge Management package.</span></span>  
  
5. <span data-ttu-id="d95cb-128">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="d95cb-128">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
6. <span data-ttu-id="d95cb-129">Chuyển tới **Thiết đặt** > **Giải pháp**.</span><span class="sxs-lookup"><span data-stu-id="d95cb-129">Go to **Settings** > **Solutions**.</span></span>   
  
7. <span data-ttu-id="d95cb-130">Trên thanh công cụ **Hành động**, bấm **Nhập**.</span><span class="sxs-lookup"><span data-stu-id="d95cb-130">On the **Actions** toolbar, click **Import**.</span></span>  
  
8. <span data-ttu-id="d95cb-131">Browse to the UiiForMicrosoftDynamicsCRM_3_0_managed.zip file in the appropriate folder as explained in step 4, and select to import it to update the existing solution in your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance.</span><span class="sxs-lookup"><span data-stu-id="d95cb-131">Browse to the UiiForMicrosoftDynamicsCRM_3_0_managed.zip file in the appropriate folder as explained in step 4, and select to import it to update the existing solution in your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance.</span></span>  
  
9. <span data-ttu-id="d95cb-132">The next page will display a yellow bar saying **This solution package contains an update for a solution that is already installed**.</span><span class="sxs-lookup"><span data-stu-id="d95cb-132">The next page will display a yellow bar saying **This solution package contains an update for a solution that is already installed**.</span></span> <span data-ttu-id="d95cb-133">Review the information about the solution, and click **Next**.</span><span class="sxs-lookup"><span data-stu-id="d95cb-133">Review the information about the solution, and click **Next**.</span></span>  
  
10. <span data-ttu-id="d95cb-134">On the next page, select the **Maintain customizations (recommended)** option and ensure that the **Enable any SDK message processing steps included in the solution** check box is selected.</span><span class="sxs-lookup"><span data-stu-id="d95cb-134">On the next page, select the **Maintain customizations (recommended)** option and ensure that the **Enable any SDK message processing steps included in the solution** check box is selected.</span></span> <span data-ttu-id="d95cb-135">Bấm vào **tiếp theo**.</span><span class="sxs-lookup"><span data-stu-id="d95cb-135">Click **Next**.</span></span>  
  
     <span data-ttu-id="d95cb-136">After the solution import completes successfully, the **UiiForMicrosoftDynamicsCRM** solution is updated.</span><span class="sxs-lookup"><span data-stu-id="d95cb-136">After the solution import completes successfully, the **UiiForMicrosoftDynamicsCRM** solution is updated.</span></span>  
  
11. <span data-ttu-id="d95cb-137">Repeat steps 7-10 for the DynamicsUnifiedServiceDesk_1_0_managed.zip and UnifiedInterfaceDemoCustomization_1_0_managed.zip file to update the **DynamicsUnifiedServiceDesk** and solution in your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance.</span><span class="sxs-lookup"><span data-stu-id="d95cb-137">Repeat steps 7-10 for the DynamicsUnifiedServiceDesk_1_0_managed.zip and UnifiedInterfaceDemoCustomization_1_0_managed.zip file to update the **DynamicsUnifiedServiceDesk** and solution in your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance.</span></span>  
  
     <span data-ttu-id="d95cb-138">For detailed information about updating solutions in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], see [Import, update, and export solutions](/dynamics365/customer-engagement/customize/import-update-export-solutions).</span><span class="sxs-lookup"><span data-stu-id="d95cb-138">For detailed information about updating solutions in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], see [Import, update, and export solutions](/dynamics365/customer-engagement/customize/import-update-export-solutions).</span></span>  
  
12. <span data-ttu-id="d95cb-139">Trong [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], xác minh số phiên bản của giải pháp đã cập nhật với các giải pháp được liệt kê trong bảng trước đây để đảm bảo chúng là phiên bản mới nhất.</span><span class="sxs-lookup"><span data-stu-id="d95cb-139">In [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], verify the version numbers of the updated solutions with those listed in the table shown earlier to ensure they’re the latest versions.</span></span>  
  
13. <span data-ttu-id="d95cb-140">Đóng phiên bản trình duyệt và đăng nhập một lần nữa vào [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] để xem các tính năng mới trong [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="d95cb-140">Close the browser instance, and sign in again to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] to see the new features in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="d95cb-141">[What's new in Unified Service Desk for administrators](../../unified-service-desk/admin/whats-new-unified-service-desk-administrators.md).</span><span class="sxs-lookup"><span data-stu-id="d95cb-141">[What's new in Unified Service Desk for administrators](../../unified-service-desk/admin/whats-new-unified-service-desk-administrators.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d95cb-142">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d95cb-142">See also</span></span>  
 <span data-ttu-id="d95cb-143">[Connect to Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md) </span><span class="sxs-lookup"><span data-stu-id="d95cb-143">[Connect to Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md) </span></span>  
 [<span data-ttu-id="d95cb-144">Install and Deploy Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="d95cb-144">Install and Deploy Unified Service Desk</span></span>](../../unified-service-desk/admin/install-upgrade-deploy-unified-service-desk.md)   
