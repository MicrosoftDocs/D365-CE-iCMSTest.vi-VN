---
title: 'Sample: Export and import a data map (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: Sample demonstrates how to create an import map, export it as XML-formatted data, import modified mappings, and create a new import map based on the imported mappings.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 66255050-1a19-4bd2-a839-3cc45e7947d8
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
helpviewer_keywords:
- sample for exporting and importing data maps
- exporting and importing data maps sample
- importing data in Microsoft Dynamics CRM, sample for exporting and importing data maps
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5860dad657d81c207bbf0427826a1ea4700391fd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388526"
---
# <a name="sample-export-and-import-a-data-map"></a>Sample: Export and import a data map

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for Dynamics 365 for Customer Engagement. Download the sample: [Work with importing data](https://code.msdn.microsoft.com/Samples-of-data-import-bd371c8c).  

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create an import map (data map) in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] for Customer Engagement, export it as an XML formatted data, import modified mappings, and create a new import map in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] for Customer Engagement based on the imported mappings.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[DataImport#UsingExportAndImportMappings](../snippets/csharp/CRMV8/dataimport/cs/usingexportandimportmappings.cs#usingexportandimportmappings)]  
  
### <a name="see-also"></a>Xem thêm  
 [Import Data in Dynamics 365 for Customer Engagement apps](import-data.md)   
 <xref:Microsoft.Crm.Sdk.Messages.ExportMappingsImportMapRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.ImportMappingsImportMapRequest>   
 [Sample: Import Data Using Complex Data Map](sample-import-data-complex-data-map.md)
