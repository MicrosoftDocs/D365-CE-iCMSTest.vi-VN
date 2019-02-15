---
title: 'Sample: Create and update an emailable entity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: 'The sample demonstrates how to create an entity that can be used in the To field of an email activity. It uses the CreateEntityRequest message. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: a3954fc9-6b40-4b7d-ba6e-51c50e004723
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6f91fe5ac7a7c8be98b42565e1f482bb00ac6366
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386725"
---
# <a name="sample-create-and-update-an-emailable-entity"></a>Sample: Create and update an emailable entity

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps. Download the sample: [Work with entity metadata](https://code.msdn.microsoft.com/Samples-of-entities-916efa41).  

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create an entity that can be used in the **To** field of an email activity. It uses the <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest> message.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[entities#CreateUpdateEmailableEntity](../../snippets/csharp/CRMV8/entities/cs/createupdateemailableentity.cs#createupdateemailableentity)]  
  
### <a name="see-also"></a>Xem thêm  
 [Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md)   
 [Customize entity metadata](../customize-entity-metadata.md)   
 [Sample: Dump Entity Metadata to a File](sample-dump-entity-metadata-file.md)   
 [Create and Update an Emailable Entity](create-update-entity-emailed.md)
