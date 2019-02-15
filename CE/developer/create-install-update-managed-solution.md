---
title: Create, install, and update a managed solution (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- creating managed solutions
- updating managed solutions
- managed solutions, creating; installing; and updating
- creating; installing; and updating managed solutions, installing managed solutions
- creating; installing; and updating managed solutions, updating managed solutions
- installing managed solutions
- solutions, creating; installing; and updating managed solutions
- creating; installing; and updating managed solutions, creating managed solutions
ms.assetid: 78ec9f71-7845-46c7-be6d-7ac5ade85e28
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 15435d7c69620fa9d02e992436736bc4ed40d02d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386947"
---
# <a name="create-install-and-update-a-managed-solution"></a><span data-ttu-id="0641d-102">Create, install, and update a managed solution</span><span class="sxs-lookup"><span data-stu-id="0641d-102">Create, install, and update a managed solution</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="0641d-103">Bạn tạo giải pháp được quản lý bằng cách xuất giải pháp không được quản lý thành giải pháp được quản lý.</span><span class="sxs-lookup"><span data-stu-id="0641d-103">You create a managed solution by exporting an unmanaged solution as a managed solution.</span></span> <span data-ttu-id="0641d-104">Các tổ chức sử dụng giải pháp được quản lý của bạn sẽ cài đặt giải pháp này và bất kỳ bản cập nhật nào bạn tạo ra cho nó.</span><span class="sxs-lookup"><span data-stu-id="0641d-104">The organizations that use your managed solution will install it and any updates that you create for it.</span></span>  
  
 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0641d-105">[Use solutions for your customizations](../customize/use-solutions-for-your-customizations.md).</span><span class="sxs-lookup"><span data-stu-id="0641d-105">[Use solutions for your customizations](../customize/use-solutions-for-your-customizations.md).</span></span>  
  
<a name="BKMK_CreateManagedSolution"></a>   
## <a name="create-a-managed-solution"></a><span data-ttu-id="0641d-106">Tạo giải pháp được quản lý</span><span class="sxs-lookup"><span data-stu-id="0641d-106">Create a managed solution</span></span>  
 <span data-ttu-id="0641d-107">Before you can create a managed solution you must first create an unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="0641d-107">Before you can create a managed solution you must first create an unmanaged solution.</span></span> <span data-ttu-id="0641d-108">For more information about how to create an unmanaged solution, see [Create an unmanaged solution](create-export-import-unmanaged-solution.md#BKMK_CreateUnmanagedSolution).</span><span class="sxs-lookup"><span data-stu-id="0641d-108">For more information about how to create an unmanaged solution, see [Create an unmanaged solution](create-export-import-unmanaged-solution.md#BKMK_CreateUnmanagedSolution).</span></span>  
  
 <span data-ttu-id="0641d-109">You create a managed solution by selecting the **Managed** option in the **Package Type** dialog box when exporting the solution.</span><span class="sxs-lookup"><span data-stu-id="0641d-109">You create a managed solution by selecting the **Managed** option in the **Package Type** dialog box when exporting the solution.</span></span>  
  
 <span data-ttu-id="0641d-110">A managed solution only includes any customizable solution components that have been customized.</span><span class="sxs-lookup"><span data-stu-id="0641d-110">A managed solution only includes any customizable solution components that have been customized.</span></span> <span data-ttu-id="0641d-111">Not only does this prevent unintentionally changing existing solution components on the system where the solution is installed, it also keeps the size of the managed solution smaller.</span><span class="sxs-lookup"><span data-stu-id="0641d-111">Not only does this prevent unintentionally changing existing solution components on the system where the solution is installed, it also keeps the size of the managed solution smaller.</span></span>  
  
 <span data-ttu-id="0641d-112">Before the final step of creating a managed solution, you must decide whether there are any customization capabilities that you do not want to allow people who install your managed solution to perform.</span><span class="sxs-lookup"><span data-stu-id="0641d-112">Before the final step of creating a managed solution, you must decide whether there are any customization capabilities that you do not want to allow people who install your managed solution to perform.</span></span> <span data-ttu-id="0641d-113">Each solution component contains a set of managed properties that control which customization capabilities you want to allow.</span><span class="sxs-lookup"><span data-stu-id="0641d-113">Each solution component contains a set of managed properties that control which customization capabilities you want to allow.</span></span> <span data-ttu-id="0641d-114">The default settings allow all customization capabilities.</span><span class="sxs-lookup"><span data-stu-id="0641d-114">The default settings allow all customization capabilities.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0641d-115">[Using Managed Properties](use-managed-properties.md)</span><span class="sxs-lookup"><span data-stu-id="0641d-115">[Using Managed Properties](use-managed-properties.md)</span></span>  
  
 <span data-ttu-id="0641d-116">You can create a managed solution programmatically by using the <xref:Microsoft.Crm.Sdk.Messages.ExportSolutionRequest> message.</span><span class="sxs-lookup"><span data-stu-id="0641d-116">You can create a managed solution programmatically by using the <xref:Microsoft.Crm.Sdk.Messages.ExportSolutionRequest> message.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0641d-117">[Export or Package a Solution](work-solutions.md#BKMK_ExportPackageSolution)</span><span class="sxs-lookup"><span data-stu-id="0641d-117">[Export or Package a Solution](work-solutions.md#BKMK_ExportPackageSolution)</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="0641d-118">You should not import a managed solution back into the organization you used to create it.</span><span class="sxs-lookup"><span data-stu-id="0641d-118">You should not import a managed solution back into the organization you used to create it.</span></span>  
  
<a name="BKMK_InstallManagedSolution"></a>   
## <a name="install-a-managed-solution"></a><span data-ttu-id="0641d-119">Install a managed solution</span><span class="sxs-lookup"><span data-stu-id="0641d-119">Install a managed solution</span></span>  
 <span data-ttu-id="0641d-120">You install a managed solution in the same way you import an unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="0641d-120">You install a managed solution in the same way you import an unmanaged solution.</span></span> <span data-ttu-id="0641d-121">The difference is in how the solution has been packaged.</span><span class="sxs-lookup"><span data-stu-id="0641d-121">The difference is in how the solution has been packaged.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="0641d-122">Việc cài đặt một giải pháp hoặc phát hành các tùy chỉnh có thể can thiệp vào hoạt động bình thường của hệ thống.</span><span class="sxs-lookup"><span data-stu-id="0641d-122">Installing a solution or publishing customizations can interfere with normal system operation.</span></span> <span data-ttu-id="0641d-123">We recommend that you schedule solution imports when it’s least disruptive to users.</span><span class="sxs-lookup"><span data-stu-id="0641d-123">We recommend that you schedule solution imports when it’s least disruptive to users.</span></span>  
  
 <span data-ttu-id="0641d-124">If the solution did not import successfully, you can click **Download Log** in the dialog box to download a report that will provide information about errors that occurred that prevented successful import of the managed solution.</span><span class="sxs-lookup"><span data-stu-id="0641d-124">If the solution did not import successfully, you can click **Download Log** in the dialog box to download a report that will provide information about errors that occurred that prevented successful import of the managed solution.</span></span> <span data-ttu-id="0641d-125">This file is an XML document configured to be opened by using [!INCLUDE[pn_MS_Excel_Full](../includes/pn-ms-excel-full.md)].</span><span class="sxs-lookup"><span data-stu-id="0641d-125">This file is an XML document configured to be opened by using [!INCLUDE[pn_MS_Excel_Full](../includes/pn-ms-excel-full.md)].</span></span>  
  
 <span data-ttu-id="0641d-126">You can import or update a managed solution programmatically by using the <xref:Microsoft.Crm.Sdk.Messages.ImportSolutionRequest> message.</span><span class="sxs-lookup"><span data-stu-id="0641d-126">You can import or update a managed solution programmatically by using the <xref:Microsoft.Crm.Sdk.Messages.ImportSolutionRequest> message.</span></span> <span data-ttu-id="0641d-127">When using this message, you can request a reference to an `ImportJob`  entity record that will include details about the success of the import.</span><span class="sxs-lookup"><span data-stu-id="0641d-127">When using this message, you can request a reference to an `ImportJob`  entity record that will include details about the success of the import.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0641d-128">[Install or Upgrade a Solution](work-solutions.md#BKMK_InstallUpgradeSolution)</span><span class="sxs-lookup"><span data-stu-id="0641d-128">[Install or Upgrade a Solution](work-solutions.md#BKMK_InstallUpgradeSolution)</span></span>  
  
 <span data-ttu-id="0641d-129">The <xref:Microsoft.Crm.Sdk.Messages.ImportSolutionRequest> can be called using the <xref:Microsoft.Xrm.Sdk.Messages.ExecuteAsyncRequest>.</span><span class="sxs-lookup"><span data-stu-id="0641d-129">The <xref:Microsoft.Crm.Sdk.Messages.ImportSolutionRequest> can be called using the <xref:Microsoft.Xrm.Sdk.Messages.ExecuteAsyncRequest>.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0641d-130">[Execute messages in the background (asynchronously)](org-service/use-messages-request-response-classes-execute-method.md#bkmk_executeasync)</span><span class="sxs-lookup"><span data-stu-id="0641d-130">[Execute messages in the background (asynchronously)](org-service/use-messages-request-response-classes-execute-method.md#bkmk_executeasync)</span></span>  
  
 <span data-ttu-id="0641d-131">There are limits to the size of a solution you can install.</span><span class="sxs-lookup"><span data-stu-id="0641d-131">There are limits to the size of a solution you can install.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0641d-132">[Maximum size of solution to import](create-export-import-unmanaged-solution.md#BKMK_MaxSizeOfSolution)</span><span class="sxs-lookup"><span data-stu-id="0641d-132">[Maximum size of solution to import](create-export-import-unmanaged-solution.md#BKMK_MaxSizeOfSolution)</span></span>  
  
<a name="BKMK_UpdateManagedSolution"></a>   
### <a name="update-a-managed-solution"></a><span data-ttu-id="0641d-133">Update a managed solution</span><span class="sxs-lookup"><span data-stu-id="0641d-133">Update a managed solution</span></span>  
 <span data-ttu-id="0641d-134">When you install a managed solution that already exists in the organization, the import solution dialog will provide the following options:</span><span class="sxs-lookup"><span data-stu-id="0641d-134">When you install a managed solution that already exists in the organization, the import solution dialog will provide the following options:</span></span>  
  
 <span data-ttu-id="0641d-135">**Giữ tùy chỉnh (khuyến cáo)**</span><span class="sxs-lookup"><span data-stu-id="0641d-135">**Maintain customizations (recommended)**</span></span>  
 <span data-ttu-id="0641d-136">This option maintains any unmanaged customizations performed on components, but also implies that some of the updates included in this solution will not take effect.</span><span class="sxs-lookup"><span data-stu-id="0641d-136">This option maintains any unmanaged customizations performed on components, but also implies that some of the updates included in this solution will not take effect.</span></span>  
  
 <span data-ttu-id="0641d-137">**Overwrite customizations**</span><span class="sxs-lookup"><span data-stu-id="0641d-137">**Overwrite customizations**</span></span>  
 <span data-ttu-id="0641d-138">This option overwrites any unmanaged customizations previously performed on components included in this solution.</span><span class="sxs-lookup"><span data-stu-id="0641d-138">This option overwrites any unmanaged customizations previously performed on components included in this solution.</span></span> <span data-ttu-id="0641d-139">Tất cả các bản Cập Nhật được bao gồm trong giải pháp này sẽ có hiệu lực.</span><span class="sxs-lookup"><span data-stu-id="0641d-139">All updates included in this solution will take effect.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0641d-140">You may want to direct people who install your managed solution to use the **Overwrite customizations** option when investigating issues where the customizations conflict with the behavior of your solutions.</span><span class="sxs-lookup"><span data-stu-id="0641d-140">You may want to direct people who install your managed solution to use the **Overwrite customizations** option when investigating issues where the customizations conflict with the behavior of your solutions.</span></span> <span data-ttu-id="0641d-141">They should always export their unmanaged solutions first so that they can re-apply them if they need to.</span><span class="sxs-lookup"><span data-stu-id="0641d-141">They should always export their unmanaged solutions first so that they can re-apply them if they need to.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="0641d-142">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="0641d-142">See also</span></span>  
 <span data-ttu-id="0641d-143">[Package and Distribute Extensions with Dynamics 365 for Customer Engagement apps Solution](package-distribute-extensions-use-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="0641d-143">[Package and Distribute Extensions with Dynamics 365 for Customer Engagement apps Solution](package-distribute-extensions-use-solutions.md) </span></span>  
 <span data-ttu-id="0641d-144">[Introduction to Solutions](introduction-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="0641d-144">[Introduction to Solutions](introduction-solutions.md) </span></span>  
 <span data-ttu-id="0641d-145">[Planning for Solution Development](plan-solution-development.md) </span><span class="sxs-lookup"><span data-stu-id="0641d-145">[Planning for Solution Development](plan-solution-development.md) </span></span>  
 <span data-ttu-id="0641d-146">[Solution Components and Dependency Tracking](dependency-tracking-solution-components.md) </span><span class="sxs-lookup"><span data-stu-id="0641d-146">[Solution Components and Dependency Tracking](dependency-tracking-solution-components.md) </span></span>  
 <span data-ttu-id="0641d-147">[Create, Export, or Import an Unmanaged Solution](create-export-import-unmanaged-solution.md) </span><span class="sxs-lookup"><span data-stu-id="0641d-147">[Create, Export, or Import an Unmanaged Solution](create-export-import-unmanaged-solution.md) </span></span>  
 <span data-ttu-id="0641d-148">[Uninstall or Delete a solution](uninstall-delete-solution.md) </span><span class="sxs-lookup"><span data-stu-id="0641d-148">[Uninstall or Delete a solution](uninstall-delete-solution.md) </span></span>  
 [<span data-ttu-id="0641d-149">Customization Solutions File Schema</span><span class="sxs-lookup"><span data-stu-id="0641d-149">Customization Solutions File Schema</span></span>](customize-dev/customization-solutions-file-schema.md)
