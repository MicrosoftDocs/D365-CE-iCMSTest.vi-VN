---
title: 'Helper code: Enumerations for option sets (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: The SDK download package includes an extension to the CrmSvcUtil code generation tool that you can use to generate enumerations for all option set values including global option sets, picklist, state, and status values.
ms.custom: ''
ms.date: 08/21/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 9ca7cb42-2b16-4429-8205-04f27e7eeb54
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 013986fc06cec16e24097c40f9ea0c127031d774
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385757"
---
# <a name="helper-code-enumerations-for-option-sets"></a>Helper code: Enumerations for option sets

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

The [Sample: Extension to Generate Enumerations for Option Sets](extend-code-generation-tool.md#Generate_Enums) includes an extension to the CrmSvcUtil code generation tool that you can use to generate enumerations for all option set values including global option sets, picklist, state, and status values. In addition, it includes a helper code file that contains the enumerations generated for all out-of-the-box values. These enumerations can be used in your code by adding the file `OptionSets.cs` or `OptionSets.vb` file to your project.  
  
 Each enumeration can be used to test or set the value for a property. Typically this property is an entity attribute but there are a few that are used for other properties.  
  
## <a name="usage-example"></a>Usage Example  
 The following example shows how to use one of these enumerations to set a value in the `Account` entity.  
  
 [!code-csharp[QuickStartCS#CRUDOperations2](../../snippets/csharp/CRMV8/quickstartcs/cs/crudoperations2.cs#crudoperations2)]  
  
### <a name="see-also"></a>Xem thêm  
 [Use the Sample and Helper Code](use-sample-helper-code.md)   
 [Helper code: ServerConnectionclass](helper-code-serverconnection-class.md)   
 [Helper code: SystemUserProviderclass](helper-code-systemuserprovider-class.md)   
 [Sample Extension to Generate Enumerations for Option Sets](extend-code-generation-tool.md#Generate_Enums)   
 [Run a simple program using Customer Engagement web services](../simple-program-web-services.md)
