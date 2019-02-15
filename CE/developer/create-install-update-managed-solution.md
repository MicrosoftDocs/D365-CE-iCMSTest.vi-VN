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
# <a name="create-install-and-update-a-managed-solution"></a>Create, install, and update a managed solution

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

Bạn tạo giải pháp được quản lý bằng cách xuất giải pháp không được quản lý thành giải pháp được quản lý. Các tổ chức sử dụng giải pháp được quản lý của bạn sẽ cài đặt giải pháp này và bất kỳ bản cập nhật nào bạn tạo ra cho nó.  
  
 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Use solutions for your customizations](../customize/use-solutions-for-your-customizations.md).  
  
<a name="BKMK_CreateManagedSolution"></a>   
## <a name="create-a-managed-solution"></a>Tạo giải pháp được quản lý  
 Before you can create a managed solution you must first create an unmanaged solution. For more information about how to create an unmanaged solution, see [Create an unmanaged solution](create-export-import-unmanaged-solution.md#BKMK_CreateUnmanagedSolution).  
  
 You create a managed solution by selecting the **Managed** option in the **Package Type** dialog box when exporting the solution.  
  
 A managed solution only includes any customizable solution components that have been customized. Not only does this prevent unintentionally changing existing solution components on the system where the solution is installed, it also keeps the size of the managed solution smaller.  
  
 Before the final step of creating a managed solution, you must decide whether there are any customization capabilities that you do not want to allow people who install your managed solution to perform. Each solution component contains a set of managed properties that control which customization capabilities you want to allow. The default settings allow all customization capabilities. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Using Managed Properties](use-managed-properties.md)  
  
 You can create a managed solution programmatically by using the <xref:Microsoft.Crm.Sdk.Messages.ExportSolutionRequest> message. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Export or Package a Solution](work-solutions.md#BKMK_ExportPackageSolution)  
  
> [!IMPORTANT]
>  You should not import a managed solution back into the organization you used to create it.  
  
<a name="BKMK_InstallManagedSolution"></a>   
## <a name="install-a-managed-solution"></a>Install a managed solution  
 You install a managed solution in the same way you import an unmanaged solution. The difference is in how the solution has been packaged.  
  
> [!IMPORTANT]
>  Việc cài đặt một giải pháp hoặc phát hành các tùy chỉnh có thể can thiệp vào hoạt động bình thường của hệ thống. We recommend that you schedule solution imports when it’s least disruptive to users.  
  
 If the solution did not import successfully, you can click **Download Log** in the dialog box to download a report that will provide information about errors that occurred that prevented successful import of the managed solution. This file is an XML document configured to be opened by using [!INCLUDE[pn_MS_Excel_Full](../includes/pn-ms-excel-full.md)].  
  
 You can import or update a managed solution programmatically by using the <xref:Microsoft.Crm.Sdk.Messages.ImportSolutionRequest> message. When using this message, you can request a reference to an `ImportJob`  entity record that will include details about the success of the import. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Install or Upgrade a Solution](work-solutions.md#BKMK_InstallUpgradeSolution)  
  
 The <xref:Microsoft.Crm.Sdk.Messages.ImportSolutionRequest> can be called using the <xref:Microsoft.Xrm.Sdk.Messages.ExecuteAsyncRequest>. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Execute messages in the background (asynchronously)](org-service/use-messages-request-response-classes-execute-method.md#bkmk_executeasync)  
  
 There are limits to the size of a solution you can install. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Maximum size of solution to import](create-export-import-unmanaged-solution.md#BKMK_MaxSizeOfSolution)  
  
<a name="BKMK_UpdateManagedSolution"></a>   
### <a name="update-a-managed-solution"></a>Update a managed solution  
 When you install a managed solution that already exists in the organization, the import solution dialog will provide the following options:  
  
 **Giữ tùy chỉnh (khuyến cáo)**  
 This option maintains any unmanaged customizations performed on components, but also implies that some of the updates included in this solution will not take effect.  
  
 **Overwrite customizations**  
 This option overwrites any unmanaged customizations previously performed on components included in this solution. Tất cả các bản Cập Nhật được bao gồm trong giải pháp này sẽ có hiệu lực.  
  
> [!NOTE]
>  You may want to direct people who install your managed solution to use the **Overwrite customizations** option when investigating issues where the customizations conflict with the behavior of your solutions. They should always export their unmanaged solutions first so that they can re-apply them if they need to.  
  
### <a name="see-also"></a>Xem thêm  
 [Package and Distribute Extensions with Dynamics 365 for Customer Engagement apps Solution](package-distribute-extensions-use-solutions.md)   
 [Introduction to Solutions](introduction-solutions.md)   
 [Planning for Solution Development](plan-solution-development.md)   
 [Solution Components and Dependency Tracking](dependency-tracking-solution-components.md)   
 [Create, Export, or Import an Unmanaged Solution](create-export-import-unmanaged-solution.md)   
 [Uninstall or Delete a solution](uninstall-delete-solution.md)   
 [Customization Solutions File Schema](customize-dev/customization-solutions-file-schema.md)
