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
# <a name="sample-import-data-using-complex-data-map"></a><span data-ttu-id="123dc-103">Sample: Import data using complex data map</span><span class="sxs-lookup"><span data-stu-id="123dc-103">Sample: Import data using complex data map</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="123dc-104">This sample code is for Dynamics 365 for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="123dc-104">This sample code is for Dynamics 365 for Customer Engagement.</span></span> <span data-ttu-id="123dc-105">Download the sample: [Work with importing data](https://code.msdn.microsoft.com/Samples-of-data-import-bd371c8c).</span><span class="sxs-lookup"><span data-stu-id="123dc-105">Download the sample: [Work with importing data](https://code.msdn.microsoft.com/Samples-of-data-import-bd371c8c).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="123dc-106">The source data for this sample is contained in the following file:</span><span class="sxs-lookup"><span data-stu-id="123dc-106">The source data for this sample is contained in the following file:</span></span>   
> `Import data\C#\import accounts.csv`

## <a name="prerequisites"></a><span data-ttu-id="123dc-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="123dc-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="123dc-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="123dc-108">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="123dc-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="123dc-109">Demonstrates</span></span>  
 <span data-ttu-id="123dc-110">This sample shows how to create new records in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] for Customer Engagement by using data import.</span><span class="sxs-lookup"><span data-stu-id="123dc-110">This sample shows how to create new records in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] for Customer Engagement by using data import.</span></span> <span data-ttu-id="123dc-111">The sample uses a complex data map.</span><span class="sxs-lookup"><span data-stu-id="123dc-111">The sample uses a complex data map.</span></span>  
  
## <a name="example"></a><span data-ttu-id="123dc-112">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="123dc-112">Example</span></span>  
 [!code-csharp[DataImport#ImportWithCreate](../snippets/csharp/CRMV8/dataimport/cs/importwithcreate.cs#importwithcreate)]  
  
### <a name="see-also"></a><span data-ttu-id="123dc-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="123dc-113">See also</span></span>  
 <span data-ttu-id="123dc-114">[Import Data in Dynamics 365 for Customer Engagement apps](import-data.md) </span><span class="sxs-lookup"><span data-stu-id="123dc-114">[Import Data in Dynamics 365 for Customer Engagement apps](import-data.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.GetHeaderColumnsImportFileRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.ParseImportRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.GetDistinctValuesImportFileRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveParsedDataImportFileRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.TransformImportRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.ImportRecordsImportRequest>
