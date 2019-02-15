---
title: Customize global option sets | MicrosoftDocs
ms.custom: ''
ms.date: 11/20/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 6786ff10-0e38-4f5c-b973-c682d1d60de5
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f71e64a19f907f8257d4adbf6aa0f821476ed12f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388234"
---
# <a name="customize-global-option-sets"></a>Customize global option sets

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

Typically, you use global option sets to set fields so that different fields can share the same set of options, which are maintained in one location. You can reuse global option sets. You will also see them used in request parameters in a manner similar to an enumeration.  
  
 When you define an option value by using <xref:Microsoft.Xrm.Sdk.Messages.CreateOptionSetRequest>, we recommend that you let the system assign a value. You do this by passing a **null** value when you create the new `OptionMetadata` instance. When you define an option, it will contain an option value prefix specific to the context of the publisher set for the solution that the option set is created in. This prefix helps reduce the chance of creating duplicate option sets for a managed solution, and in any option sets that are defined in organizations where your managed solution is installed. For more information, see [Merge option set options](../understand-managed-solutions-merged.md#merge-option-set-options).  
 
 ## <a name="messages"></a>Messages  
 The following table lists the messages that you can use with global option sets.  
  
|Thông báo|Web API Operation|SDK Assembly|  
|-------------|----------------------------|--------------------------------|  
|CreateOptionSet|Use `POST` request to create a new global option set.|<xref:Microsoft.Xrm.Sdk.Messages.CreateOptionSetRequest>|  
|DeleteOptionSet|Use `DELETE` request to delete a global optin set.|<xref:Microsoft.Xrm.Sdk.Messages.DeleteOptionSetRequest>|  
|DeleteOptionValue</br>Deletes one of the values in a global option set.|<xref href="Microsoft.Dynamics.CRM.DeleteOptionValue?text=DeleteOptionValue Action" />|<xref:Microsoft.Xrm.Sdk.Messages.DeleteOptionValueRequest>|    
|InsertOptionValue</br>Inserts a new option into a global option set.|<xref href="Microsoft.Dynamics.CRM.InsertOptionValue?text=InsertOptionValue Action" />|<xref:Microsoft.Xrm.Sdk.Messages.InsertOptionValueRequest>|  
|InsertStatusValue</br>Inserts a new option into the global option set used in the `Status` attribute.|<xref href="Microsoft.Dynamics.CRM.InsertOptionValue?text=InsertStatusValue Action" />|<xref:Microsoft.Xrm.Sdk.Messages.InsertStatusValueRequest>|  
|OrderOption</br>Changes the relative order of the options in an option set.|<xref href="Microsoft.Dynamics.CRM.OrderOption?text=OrderOption Action" />|<xref:Microsoft.Xrm.Sdk.Messages.OrderOptionRequest>|  
|RetrieveAllOptionSets|Use `GET` request to retrieve all the global option sets.|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllOptionSetsRequest>|  
|RetrieveOptionSet|Use `GET` request to retrieve a global option set.|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveOptionSetRequest>|    
|UpdateOptionSet|Use `PUT` request to update a global option set.|<xref:Microsoft.Xrm.Sdk.Messages.UpdateOptionSetRequest>|  
|UpdateOptionValue|</br>Updates an option in a global option set.|<xref:Microsoft.Xrm.Sdk.Messages.UpdateOptionValueRequest>|  
|UpdateStateValue</br>Inserts a new option into the option set used in the `Status` attribute.|<xref href="Microsoft.Dynamics.CRM.OrderOption?text=UpdateStateValue Action" />|<xref:Microsoft.Xrm.Sdk.Messages.UpdateStateValueRequest>|   

<a name="BKMK_RetrieveAGlobalOptionSet"></a>   
## <a name="retrieve-a-global-option-set"></a>Retrieve a global option set  
 The following sample shows how to retrieve a global option set by name using the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveOptionSetRequest> message:  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets6](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets6.cs#workwithglobaloptionsets6)]  
  
<a name="BKMK_CreateGlobalOptionSet"></a>   
## <a name="create-a-global-option-set"></a>Tạo bộ tùy chọn chung  
 Use the <xref:Microsoft.Xrm.Sdk.Messages.CreateOptionSetRequest> message to create a new global option set. Set the <xref:Microsoft.Xrm.Sdk.Metadata.OptionSetMetadataBase.IsGlobal> property to `true` to indicate that the option set is global. The following code example creates a global option set called “Example Option Set”:  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets2](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets2.cs#workwithglobaloptionsets2)]  
  
<a name="BKMK_CreatePicklistWithGlobalOptionSet"></a>   
## <a name="create-a-picklist-that-uses-a-global-option-set"></a>Create a picklist that uses a global option set  
 The following sample shows how to create a picklist attribute that uses a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest>:  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets3](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets3.cs#workwithglobaloptionsets3)]  
  
<a name="BKMK_UpdateGlobalOptionSet"></a>   
## <a name="update-a-global-option-set"></a>Update a global option set  
 The following sample shows how to update the label for a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.UpdateOptionSetRequest>:  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets4](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets4.cs#workwithglobaloptionsets4)]  
  
<a name="BKMK_OrderingOptions"></a>   
## <a name="ordering-options"></a>Ordering options  
 The following sample shows how the options in a global option set can be ordered by using <xref:Microsoft.Xrm.Sdk.Messages.OrderOptionRequest>:  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets8](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets8.cs#workwithglobaloptionsets8)]  
  
<a name="BKMK_RetrieveAllGlobalOptionSets"></a>   
## <a name="retrieve-all-global-option-sets"></a>Retrieve all global option sets  
 The following sample shows how to retrieve all global option sets by using <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllOptionSetsRequest>:  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets9](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets9.cs#workwithglobaloptionsets9)]  
  
<a name="BKMK_DeleteAGlobalOptionSet"></a>   
## <a name="delete-a-global-option-set"></a>Xóa bộ tùy chọn chung

 The following sample shows how to check whether a global option set is being used by another solution component by using `RetrieveDependentComponents` message (<xref href="Microsoft.Dynamics.CRM.RetrieveDependentComponents?text=RetrieveDependentComponents Function" /> or <xref:Microsoft.Crm.Sdk.Messages.RetrieveDependentComponentsRequest>), and then how to delete it by using `DeleteOptionSet` message (For Organization Service, use <xref:Microsoft.Xrm.Sdk.Messages.DeleteOptionSetRequest>):  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets12](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets12.cs#workwithglobaloptionsets12)]  
  
### <a name="see-also"></a>Xem thêm  
 [Customize Dynamics 365 for Customer Engagement applications](../customize-dev/customize-applications.md)   
 [Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md)   
 [Insert, update, delete, and order global option set options](insert-update-delete-order-global-option-set-options.md)   
 [Sample: Create Global Option Set](sample-create-global-option-set.md)   
 [Sample: Work with Global Option Sets](sample-work-global-option-sets.md)   
 [Sample: Dump Global Option Set Information to a File](sample-dump-global-option-set-information-file.md)
