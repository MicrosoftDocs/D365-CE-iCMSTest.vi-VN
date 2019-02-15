---
title: 'Sample: Create a global option set | MicrosoftDocs'
description: ''
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement (on-premises)
- Dynamics CRM 2016
- Dynamics CRM Online
ms.assetid: b312607a-d231-41fc-ba9d-259e0c76af4e
author: JimDaly
ms.author: jdaly
manager: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 1e14c9aef39b0713f42781e02c9ad6b04da5838d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386915"
---
# <a name="sample-create-a-global-option-set"></a>Sample: Create a global option set

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps. Download the sample: [Work with global option sets](https://code.msdn.microsoft.com/Samples-of-option-set-37c4b418).   

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to how to create a global option set.  It uses the <xref:Microsoft.Xrm.Sdk.Messages.CreateOptionSetRequest> message.
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Optionsets#CreateOptionSet](../../snippets/csharp/CRMV8/optionsets/cs/createoptionset.cs#createoptionset)]  
  
### <a name="see-also"></a>Xem thêm  
 [Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md)   
 [Customize Global Option Sets in Dynamics 365 for Customer Engagement apps](customize-global-option-sets.md)   
 [Sample: Work with Global Option Sets](sample-work-global-option-sets.md)   
 [Customize global option sets](customize-global-option-sets.md)
