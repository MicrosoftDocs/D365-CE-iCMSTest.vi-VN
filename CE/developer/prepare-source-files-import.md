---
title: Prepare source files for import (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Data import supports source files formatted as comma-separated values (.csv), XML Spreadsheet 2003 (.xml), or text files.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- preparing source files for importing, providing maps for multiple-entity data
- importing source files, preparing source files for importing
- importing source files
- preparing source files for importing, creating data source files
- importing source files, creating data source files
- preparing source files for importing, allowable separators for field values
- preparing source files for importing, types of contents for allowable source files
- preparing source files for importing, allowable characters for field values
ms.assetid: 78230676-f2ed-453a-aba0-887c860329e0
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6094020b894f3d41daba04027fcf0dd063a9dce8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387410"
---
# <a name="prepare-source-files-for-import"></a><span data-ttu-id="82b1e-103">Prepare source files for import</span><span class="sxs-lookup"><span data-stu-id="82b1e-103">Prepare source files for import</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="82b1e-104">Before you can import data into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, you must create the source data files.</span><span class="sxs-lookup"><span data-stu-id="82b1e-104">Before you can import data into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, you must create the source data files.</span></span>  
  
<span data-ttu-id="82b1e-105">The data source files that you use in an import must be formatted as comma-separated values (.csv), XML Spreadsheet 2003 (.xml), or text files.</span><span class="sxs-lookup"><span data-stu-id="82b1e-105">The data source files that you use in an import must be formatted as comma-separated values (.csv), XML Spreadsheet 2003 (.xml), or text files.</span></span> <span data-ttu-id="82b1e-106">The use of source files enables the transfer of data from database systems that use different formats into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="82b1e-106">The use of source files enables the transfer of data from database systems that use different formats into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
<span data-ttu-id="82b1e-107">A source file may contain data for one entity type or multiple entity types, such as accounts and contacts.</span><span class="sxs-lookup"><span data-stu-id="82b1e-107">A source file may contain data for one entity type or multiple entity types, such as accounts and contacts.</span></span> <span data-ttu-id="82b1e-108">For the source files that contain multiple entity data, you must provide a map that includes the `<EntitiesPerFile>` tag.</span><span class="sxs-lookup"><span data-stu-id="82b1e-108">For the source files that contain multiple entity data, you must provide a map that includes the `<EntitiesPerFile>` tag.</span></span> <span data-ttu-id="82b1e-109">Set the value of this tag to “Multiple” to indicate that there is more than one entity type in the source file.</span><span class="sxs-lookup"><span data-stu-id="82b1e-109">Set the value of this tag to “Multiple” to indicate that there is more than one entity type in the source file.</span></span> <span data-ttu-id="82b1e-110">Add the `Dedupe = “Eliminate”` attribute to the `<EntityMap>` tag.</span><span class="sxs-lookup"><span data-stu-id="82b1e-110">Add the `Dedupe = “Eliminate”` attribute to the `<EntityMap>` tag.</span></span> <span data-ttu-id="82b1e-111">This assures that if the file contains duplicate rows for the entity type, a single row is used to minimize lookup related errors.</span><span class="sxs-lookup"><span data-stu-id="82b1e-111">This assures that if the file contains duplicate rows for the entity type, a single row is used to minimize lookup related errors.</span></span>  
  
<span data-ttu-id="82b1e-112">You can download an example of a data map with multiple entity types from [Microsoft Downloads: DataImportMaps.zip](http://download.microsoft.com/download/D/5/F/D5F73E15-439B-4EBC-BFFB-C6837B146C76/DataImportMaps.zip).</span><span class="sxs-lookup"><span data-stu-id="82b1e-112">You can download an example of a data map with multiple entity types from [Microsoft Downloads: DataImportMaps.zip](http://download.microsoft.com/download/D/5/F/D5F73E15-439B-4EBC-BFFB-C6837B146C76/DataImportMaps.zip).</span></span> <span data-ttu-id="82b1e-113">Look at the `MapForSalesForceContactAccount.xml` file.</span><span class="sxs-lookup"><span data-stu-id="82b1e-113">Look at the `MapForSalesForceContactAccount.xml` file.</span></span>  
  
 <span data-ttu-id="82b1e-114">The field values in the source file can be separated by commas, tabs, or other characters that are defined in the `ImportFile.FieldDelimiterCode` attribute.</span><span class="sxs-lookup"><span data-stu-id="82b1e-114">The field values in the source file can be separated by commas, tabs, or other characters that are defined in the `ImportFile.FieldDelimiterCode` attribute.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="82b1e-115">Do not use non-printable characters, **null** (\0) or break (\b), as delimiters for the field values.</span><span class="sxs-lookup"><span data-stu-id="82b1e-115">Do not use non-printable characters, **null** (\0) or break (\b), as delimiters for the field values.</span></span>  
  
 <span data-ttu-id="82b1e-116">The first row in the source file should contain column headings.</span><span class="sxs-lookup"><span data-stu-id="82b1e-116">The first row in the source file should contain column headings.</span></span> <span data-ttu-id="82b1e-117">If you do not include headings, use the `ImportFile.IsFirstRowHeader` attribute to specify that the first row represents actual data.</span><span class="sxs-lookup"><span data-stu-id="82b1e-117">If you do not include headings, use the `ImportFile.IsFirstRowHeader` attribute to specify that the first row represents actual data.</span></span> <span data-ttu-id="82b1e-118">In this case, default column headings are created with the names Col1, Col2, and so on.</span><span class="sxs-lookup"><span data-stu-id="82b1e-118">In this case, default column headings are created with the names Col1, Col2, and so on.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="82b1e-119">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="82b1e-119">See also</span></span>  
 <span data-ttu-id="82b1e-120">[Import Data in Dynamics 365 for Customer Engagement apps](import-data.md) </span><span class="sxs-lookup"><span data-stu-id="82b1e-120">[Import Data in Dynamics 365 for Customer Engagement apps](import-data.md) </span></span>  
 <span data-ttu-id="82b1e-121">[Create Data Maps](create-data-maps-for-import.md) </span><span class="sxs-lookup"><span data-stu-id="82b1e-121">[Create Data Maps](create-data-maps-for-import.md) </span></span>  
 [<span data-ttu-id="82b1e-122">Blog Post: How to Import attachments programmatically</span><span class="sxs-lookup"><span data-stu-id="82b1e-122">Blog Post: How to Import attachments programmatically</span></span>](http://blogs.msdn.com/b/crm/archive/2012/08/06/how-to-import-attachments-programmatically.aspx)
