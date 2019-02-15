---
title: Insert, update, delete, and order global option set options (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement (on-premises)
- Dynamics CRM 2016
- Dynamics CRM Online
ms.assetid: dfcafa54-d368-46c8-8760-19bcbc4c6797
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5556d55cc343fc2f86bc4c1226767d1155b51b10
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387462"
---
# <a name="insert-update-delete-and-order-global-option-set-options"></a>Insert, update, delete, and order global option set options

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

These code samples show you how to insert, update, delete, and order options in a global option set.  
  
<a name="BKMK_InsertNewOption"></a>   
## <a name="insert-a-new-option"></a>Insert a new option  
 The following sample shows how to add a new option to a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.InsertOptionValueRequest>:  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets5](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets5.cs#workwithglobaloptionsets5)]  

  
<a name="BKMK_UpdateAnOption"></a>   
## <a name="update-an-option"></a>Update an option  
 The following sample shows how to update an option in a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.UpdateOptionValueRequest>:  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets7](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets7.cs#workwithglobaloptionsets7)]  
  
<a name="BKMK_DeleteAnOption"></a>   
## <a name="delete-an-option"></a>Xóa một tùy chọn  
 The following sample shows how to deletes an option in a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.DeleteOptionValueRequest>:  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets11](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets11.cs#workwithglobaloptionsets11)]  
  
<a name="BKMK_OrderOptions"></a>   
## <a name="order-options"></a>Order options  
 The following sample shows how to set the order of options in a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.OrderOptionRequest>:  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets8](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets8.cs#workwithglobaloptionsets8)] 
  
### <a name="see-also"></a>Xem thêm  
 [Customize Global Options Sets](../org-service/customize-global-option-sets.md)   
