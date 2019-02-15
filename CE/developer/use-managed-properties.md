---
title: Use managed properties (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: Managed properties help you define which of the managed solution components can be customized
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
- using managed properties, setting the IsCustomizable property
- unmanaged solutions, applying managed properties
- using managed properties, applying managed properties to unmanaged solutions
- checking managed properties for solution components, using managed properties
- managed properties, using in unmanaged solutions
- solution components, list of managed properties for each solution component
- using managed properties, list of managed properties for each solution component
- solution components, using managed properties
- using managed properties, updating managed properties
- using managed properties, checking managed properties for solution components
ms.assetid: 749edaa4-e975-4e6a-925d-6ea77bfa9112
caps.latest.revision: 24
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3576c866ff52c75709366607cf0c45468de55be3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385888"
---
# <a name="use-managed-properties"></a>Use managed properties

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

You can control which of your managed solution components are customizable by using managed properties. You should allow as much customization as possible for those solution components that represent business entities. This lets organizations customize your           solution to their requirements. Limit or eliminate customization of critical solution components that provide the core functionality of your solution so that you can predictably support and maintain it.  
  
 Managed properties are intended to protect your solution from modifications that may cause it to break. Managed properties do not provide digital rights management (DRM), or capabilities to license your solution or control who may install it.  
  
## <a name="apply-managed-properties"></a>Apply managed properties  
 You apply managed properties when the solution is unmanaged. The managed properties will take effect after you package the managed solution and install it in a different organization. After the managed solution is installed, the managed properties cannot be              updated except by an update of the solution by the original publisher.  
  
 Most solution components have a **Managed Properties**button when viewing a list of solution components. You can view or update the managed properties for a solution component when you click this button. To access managed properties for solutions that do not display this button, select **Managed Properties**from the **More Actions**drop-down list.  
  
 By default, all custom solution components are customizable. To change the managed properties for a solution component, click the **Managed Properties**button in the toolbar for the solution component. Each solution component has a **Can be customized**(                 `IsCustomizable`) property. As long as this property is true, more properties specific to the type of solution component can be specified. If you set the              `IsCustomizable.Value`property to false, after the solution is installed as a managed solution the solution component will not be customizable. The following table lists the managed properties for each solution component.  
  
|Thành phần|Tên Hiển thị|Thuộc tính|  
|---------------|------------------|--------------|  
|Thực thể|Có thể tùy chỉnh|<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsCustomizable>.                                 `Value`|  
|Thực thể|Có thể sửa đổi tên hiển thị|<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsRenameable>.                              `Value`|  
|Thực thể|Can be related entity in relationship|<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanBeRelatedEntityInRelationship>.                                 `Value`(Read Only)|  
|Thực thể|Can be primary entity in relationship|<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanBePrimaryEntityInRelationship>.                                 `Value`(Read Only)|  
|Thực thể|Can be in many-to-many relationship|<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanBeInManyToMany>.                               `Value`(Read Only)|  
|Thực thể|Có thể tạo biểu mẫu mới|<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanCreateForms>.                              `Value`|  
|Thực thể|Có thể tạo biểu đồ mới|<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanCreateCharts>.                               `Value`|  
|Thực thể|Có thể tạo dạng xem mới|<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanCreateViews>.                              `Value`|  
|Thực thể|Can change any other entity properties not represented by a managed property|<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanModifyAdditionalSettings>.                                `Value`|  
|Field (Attribute)|Can be customized|<xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.IsCustomizable>.                                 `Value`|  
|Field (Attribute)|Display name can be modified|<xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.IsRenameable>.                              `Value`|  
|Field (Attribute)|Có thể thay đổi mức yêu cầu|<xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.RequiredLevel>.                                `CanBeChanged`<br /><br /> Note:<br /><br /> `RequiredLevel`is the only managed property to use the                                     `CanBeChanged`property.|  
|Field (Attribute)|Can change any other attribute properties not represented by a managed property|<xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.CanModifyAdditionalSettings>.                                 `Value`|  
|Mối quan hệ của thực thể|Can be customized|<xref:Microsoft.Xrm.Sdk.Metadata.RelationshipMetadataBase.IsCustomizable>.                              `Value`|  
|Biểu mẫu|Can be customized|`SystemForm.IsCustomizable.Value`|  
|Biểu đồ|Can be customized|`SavedQueryVisualization.IsCustomizable.Value`|  
|Dạng xem|Can be customized|`SavedQuery.IsCustomizable.Value`|  
|Bộ Tùy chọn|Can be customized|<xref:Microsoft.Xrm.Sdk.Metadata.OptionSetMetadataBase.IsCustomizable>.                              `Value`|  
|Tài nguyên Web|Can be customized|`WebResource.IsCustomizable.Value`|  
|Quy trình|Can be customized|`Workflow.IsCustomizable.Value`|  
|Bộ|Can be customized|`SdkMessageProcessingStep.IsCustomizable.Value`|  
|Assembly Registration|Can be customized|`ServiceEndpoint.IsCustomizable.Value`|  
|E-mail Template|Can be customized|`Template.IsCustomizable.Value`|  
|KB Article Template|Can be customized|`KbArticleTemplate.IsCustomizable.Value`|  
|Mẫu Hợp đồng|Can be customized|`ContractTemplate.IsCustomizable.Value`|  
|Mẫu Trộn Thư|Can be customized|`MailMergeTemplate.IsCustomizable.Value`|  
|Bảng thông tin|Can be customized|`SystemForm.IsCustomizable.Value`|  
|Vai trò Bảo mật|Can be customized|`Role.IsCustomizable.Value`|  
  
### <a name="update-managed-properties"></a>Update managed properties  
 After you release your managed solution, you may decide that you want to change the managed properties. You can only change managed properties to make them less restrictive. For example, after your initial release you can decide to allow customization of an                      entity.  
  
 You update managed properties for your solution by releasing an update to your solution with the changed managed properties. Your managed solution can only be updated by another managed solution associated with the same publisher record as the original managed                       solution. If your update includes a change in managed properties to make them more restrictive, those managed property changes will be ignored but other changes in the update will be applied.  
  
 Because the original publisher is a requirement to update managed properties for a managed solution, any unmanaged solution cannot be associated with a publisher that has been used to install a managed solution.  
  
> [!NOTE]
>  This means you will not be able to develop an update for your solution by using an organization where your managed solution is installed.  
  
## <a name="check-managed-properties"></a>Check managed properties  
 Use the                <xref:Microsoft.Crm.Sdk.Messages.IsComponentCustomizableRequest>to check whether a solution component is customizable. Alternatively, you can check the solution component properties but you must consider that the ultimate determination of                 the meaning depends on the values of several properties. Each solution component has an                 `IsCustomizable`property. When a solution component is installed as part of a managed solution, the                 `IsManaged`property will be true. Managed properties are only enforced for managed solutions. When checking managed properties to determine if an individual solution component is customizable, you must check both the                `IsCustomizable`and                 `IsManaged`properties. A solution component where               `IsCustomizable`is false and                `IsManaged`is false, is customizable.  
  
 Entity and attribute have more managed properties in addition to               `IsCustomizable`. These managed properties are not updated if               `IsCustomizable`is set to false. This means that in addition to checking the individual managed property, you must also check the               `IsCustomizable`property to see if the managed property is being enforced.  
  
### <a name="see-also"></a>Xem thêm  
 [Thuộc tính được quản lý](introduction-solutions.md#BKMK_ManagedProperties)   
 [Plan For Solution Development](plan-solution-development.md)   
 [Maintain Managed Solutions](maintain-managed-solutions.md)   
 [Package and Distribute Extensions with Dynamics 365 for Customer Engagement Solutions](package-distribute-extensions-use-solutions.md)   
 <xref:Microsoft.Crm.Sdk.Messages.IsComponentCustomizableRequest>
