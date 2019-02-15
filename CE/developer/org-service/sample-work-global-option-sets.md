---
title: 'Sample: Work with global option sets (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement (on-premises)
- Dynamics CRM 2016
- Dynamics CRM Online
ms.assetid: 348e0bc9-ddde-4bbe-a0aa-968d0d6b0ac2
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a0b911448eda17d4a8ccefa75496cd4d7e80d098
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385625"
---
# <a name="sample-work-with-global-option-sets"></a>Sample: Work with global option sets

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps. Download the sample: [Work with global option sets](https://code.msdn.microsoft.com/Samples-of-option-set-37c4b418). 

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to perform the following actions with global option sets:  
  
-   Create, retrieve, or update a global option set.  
  
-   Create a <xref:Microsoft.Xrm.Sdk.Metadata.PicklistAttributeMetadata> attribute using a global option set.  
  
-   Insert or update an option item.  
  
-   Re-order option items.  
  
-   Retrieve all global option sets.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[optionsets#WorkwithGlobalOptionSets](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets.cs#workwithglobaloptionsets)]  
  
### <a name="see-also"></a>Xem thêm  
 [Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md)   
 [Customize Global Option Sets in Dynamics 365 for Customer Engagement apps](customize-global-option-sets.md)   
 [Sample: Dump global option set information to a file](sample-dump-global-option-set-information-file.md)   
 [Global Option Set Messages](customize-global-option-sets.md#messages)
