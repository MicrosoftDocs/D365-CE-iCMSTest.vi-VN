---
title: 'Sample: Import data using complex data map (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: Sample demonstrates how to create new records with data import by using a complex data map.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1ed89b35-a84d-488e-b58c-4ed6eb26018c
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
helpviewer_keywords:
- importing data in Microsoft Dynamics CRM, sample for importing data by using complex data maps
- sample for importing data by using complex data maps
- sample for creating new records in Microsoft Dynamics CRM by using data import
- importing data in Microsoft Dynamics CRM, sample for creating new records in Microsoft Dynamics CRM by using data import
- creating new records in Microsoft Dynamics CRM by using data import sample
- importing data by using complex data maps sample
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ebf33a83ee2f556006a8cb3844f8d5f01b30e15e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387784"
---
# <a name="sample-import-data-using-complex-data-map"></a>Sample: Import data using complex data map

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for Dynamics 365 for Customer Engagement. Download the sample: [Work with importing data](https://code.msdn.microsoft.com/Samples-of-data-import-bd371c8c).
  
> [!NOTE]
>  The source data for this sample is contained in the following file:   
> `Import data\C#\import accounts.csv`

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create new records in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] for Customer Engagement by using data import. The sample uses a complex data map.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[DataImport#ImportWithCreate](../snippets/csharp/CRMV8/dataimport/cs/importwithcreate.cs#importwithcreate)]  
  
### <a name="see-also"></a>Xem thêm  
 [Import Data in Dynamics 365 for Customer Engagement apps](import-data.md)   
 <xref:Microsoft.Crm.Sdk.Messages.GetHeaderColumnsImportFileRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.ParseImportRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.GetDistinctValuesImportFileRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveParsedDataImportFileRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.TransformImportRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.ImportRecordsImportRequest>
