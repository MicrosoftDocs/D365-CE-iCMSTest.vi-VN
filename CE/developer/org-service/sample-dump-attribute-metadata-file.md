---
title: 'Sample: Dump attribute metadata to a file (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample shows how to write out all the attribute metadata to an XML file. It uses the RetrieveAllEntitiesRequest message.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: f2321671-f4dc-4abd-ac50-edddfa170fd2
author: JimDaly
ms.author: jdaly
manager: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 20a1f1ccdd78a4affa167e62d9cd7f9975a7f1da
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388691"
---
# <a name="sample-dump-attribute-metadata-to-a-file"></a>Sample: Dump attribute metadata to a file

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps. Download the sample: [Work with attribute metadata](https://code.msdn.microsoft.com/Samples-of-attributes-1c0f93e7).  

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to write out all the attribute metadata to an XML file. It uses the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest> message.  
  
 The following sample creates a new file at \Entities\bin\Debug\AllAttributeDesc.xml. You can open this file in [!INCLUDE[pn_MS_Excel_Full](../../includes/pn-ms-excel-full.md)] to see a tabular report. You can easily look up information such as which attributes can be specified in a create, retrieve, or update operation. This information can also be found in the “*EntityName* Entity Attribute Metadata” topic for each entity.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Attributes#DumpAttributeInfo](../../snippets/csharp/CRMV8/attributes/cs/dumpattributeinfo.cs#dumpattributeinfo)]  
  
### <a name="see-also"></a>Xem thêm  
 [Customize entity attribute metadata](../customize-entity-attribute-metadata.md)   
 [Sample: Dump attribute picklist metadata to a file](sample-dump-attribute-picklist-metadata-file.md)   
 [Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md)   
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest>   
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesResponse>
