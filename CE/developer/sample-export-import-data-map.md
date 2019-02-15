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
# <a name="sample-export-and-import-a-data-map"></a><span data-ttu-id="4bdbc-103">Sample: Export and import a data map</span><span class="sxs-lookup"><span data-stu-id="4bdbc-103">Sample: Export and import a data map</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="4bdbc-104">This sample code is for Dynamics 365 for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="4bdbc-104">This sample code is for Dynamics 365 for Customer Engagement.</span></span> <span data-ttu-id="4bdbc-105">Download the sample: [Work with importing data](https://code.msdn.microsoft.com/Samples-of-data-import-bd371c8c).</span><span class="sxs-lookup"><span data-stu-id="4bdbc-105">Download the sample: [Work with importing data](https://code.msdn.microsoft.com/Samples-of-data-import-bd371c8c).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="4bdbc-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="4bdbc-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="4bdbc-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="4bdbc-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="4bdbc-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="4bdbc-108">Demonstrates</span></span>  
 <span data-ttu-id="4bdbc-109">This sample shows how to create an import map (data map) in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] for Customer Engagement, export it as an XML formatted data, import modified mappings, and create a new import map in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] for Customer Engagement based on the imported mappings.</span><span class="sxs-lookup"><span data-stu-id="4bdbc-109">This sample shows how to create an import map (data map) in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] for Customer Engagement, export it as an XML formatted data, import modified mappings, and create a new import map in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] for Customer Engagement based on the imported mappings.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4bdbc-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="4bdbc-110">Example</span></span>  
 [!code-csharp[DataImport#UsingExportAndImportMappings](../snippets/csharp/CRMV8/dataimport/cs/usingexportandimportmappings.cs#usingexportandimportmappings)]  
  
### <a name="see-also"></a><span data-ttu-id="4bdbc-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="4bdbc-111">See also</span></span>  
 <span data-ttu-id="4bdbc-112">[Import Data in Dynamics 365 for Customer Engagement apps](import-data.md) </span><span class="sxs-lookup"><span data-stu-id="4bdbc-112">[Import Data in Dynamics 365 for Customer Engagement apps](import-data.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.ExportMappingsImportMapRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.ImportMappingsImportMapRequest>   
 [<span data-ttu-id="4bdbc-113">Sample: Import Data Using Complex Data Map</span><span class="sxs-lookup"><span data-stu-id="4bdbc-113">Sample: Import Data Using Complex Data Map</span></span>](sample-import-data-complex-data-map.md)
