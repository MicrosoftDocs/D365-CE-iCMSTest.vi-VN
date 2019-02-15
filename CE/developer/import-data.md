---
title: Import data (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Overview of the data import feature, which enables data upload from various customer relationship management systems and other data sources.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- Import Data wizard, capabilities of the
- importing data in Microsoft Dynamics CRM, data import defined
- importing data in Microsoft Dynamics CRM, capabilities of the Import Data wizard
- importing data in Microsoft Dynamics CRM, overview
- importing data in Microsoft Dynamics CRM, uploading data from different CRM systems and sources into Microsoft Dynamics CRM
- uploading data from different systems and sources into Microsoft Dynamics CRM
- importing data in Microsoft Dynamics CRM, general tasks
ms.assetid: 4ab8f0b9-eb38-45b1-9026-b0415f1ab30e
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e4718a2112c0c9bdf11ca36255cf1577b8b5c907
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388388"
---
# <a name="import-data"></a><span data-ttu-id="7a6a7-103">Nhập dữ liệu</span><span class="sxs-lookup"><span data-stu-id="7a6a7-103">Import data</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="7a6a7-104">If you want to import data into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, you can use the *data import* feature.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-104">If you want to import data into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, you can use the *data import* feature.</span></span> <span data-ttu-id="7a6a7-105">Data import lets you upload data from various customer relationship management systems and data sources into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-105">Data import lets you upload data from various customer relationship management systems and data sources into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span> <span data-ttu-id="7a6a7-106">You can import data into standard and customized attributes of most business and custom entities.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-106">You can import data into standard and customized attributes of most business and custom entities.</span></span> <span data-ttu-id="7a6a7-107">You can also include related data, such as notes and attachments.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-107">You can also include related data, such as notes and attachments.</span></span>  
  
 [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] <span data-ttu-id="7a6a7-108">apps include a web application tool called Import Data Wizard.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-108">apps include a web application tool called Import Data Wizard.</span></span> <span data-ttu-id="7a6a7-109">You use this tool to import data records from one or more comma-separated values (.csv), XML Spreadsheet 2003 (.xml), or text files.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-109">You use this tool to import data records from one or more comma-separated values (.csv), XML Spreadsheet 2003 (.xml), or text files.</span></span>  
  
 <span data-ttu-id="7a6a7-110">For more information about the Import Data Wizard, see [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps Help.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-110">For more information about the Import Data Wizard, see [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps Help.</span></span>  
  
 <span data-ttu-id="7a6a7-111">The [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] web services provide the following additional capabilities that aren’t available in the Import Data Wizard:</span><span class="sxs-lookup"><span data-stu-id="7a6a7-111">The [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] web services provide the following additional capabilities that aren’t available in the Import Data Wizard:</span></span>  
  
- <span data-ttu-id="7a6a7-112">Create data maps that include complex transformation mapping, such as concatenation, split, and replace.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-112">Create data maps that include complex transformation mapping, such as concatenation, split, and replace.</span></span>  
  
- <span data-ttu-id="7a6a7-113">Define custom transformation mapping.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-113">Define custom transformation mapping.</span></span>  
  
- <span data-ttu-id="7a6a7-114">View source data that is stored inside the temporary parse tables.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-114">View source data that is stored inside the temporary parse tables.</span></span>  
  
- <span data-ttu-id="7a6a7-115">Access error logs to build custom error reporting tools with improved error logging views.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-115">Access error logs to build custom error reporting tools with improved error logging views.</span></span>  
  
- <span data-ttu-id="7a6a7-116">Run data import by using command-line scripts.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-116">Run data import by using command-line scripts.</span></span>  
  
- <span data-ttu-id="7a6a7-117">Add `LookupMap`XML tags in the data map to indicate that the data lookup will be initiated and performed on a source file that is used in the import.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-117">Add `LookupMap`XML tags in the data map to indicate that the data lookup will be initiated and performed on a source file that is used in the import.</span></span>  
  
- <span data-ttu-id="7a6a7-118">Add custom `OwnerMetadata`XML tags in the data map to match the user records in the source file with the records of the user (system user) in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-118">Add custom `OwnerMetadata`XML tags in the data map to match the user records in the source file with the records of the user (system user) in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
- <span data-ttu-id="7a6a7-119">Use optional validation checks.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-119">Use optional validation checks.</span></span>  
  
  > [!NOTE]
  >  <span data-ttu-id="7a6a7-120">Validation isn’t optional in the Import Data Wizard.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-120">Validation isn’t optional in the Import Data Wizard.</span></span>  
  
  <span data-ttu-id="7a6a7-121">To implement data import, you typically do the following:</span><span class="sxs-lookup"><span data-stu-id="7a6a7-121">To implement data import, you typically do the following:</span></span>  
  
- <span data-ttu-id="7a6a7-122">Create a comma-separated values (CSV), XML Spreadsheet 2003 (XMLSS), or text source file.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-122">Create a comma-separated values (CSV), XML Spreadsheet 2003 (XMLSS), or text source file.</span></span>  
  
- <span data-ttu-id="7a6a7-123">Create a data map or use an existing data map.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-123">Create a data map or use an existing data map.</span></span>  
  
- <span data-ttu-id="7a6a7-124">Associate an import file with a data map.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-124">Associate an import file with a data map.</span></span>  
  
- <span data-ttu-id="7a6a7-125">Upload the content from a source file to the associated import file.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-125">Upload the content from a source file to the associated import file.</span></span>  
  
- <span data-ttu-id="7a6a7-126">Parse the import file.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-126">Parse the import file.</span></span>  
  
- <span data-ttu-id="7a6a7-127">Transform the parsed data.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-127">Transform the parsed data.</span></span>  
  
- <span data-ttu-id="7a6a7-128">Upload the transformed data into the target [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps server.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-128">Upload the transformed data into the target [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps server.</span></span>  
  
  <span data-ttu-id="7a6a7-129">Bạn có thể nhập dữ liệu từ một tệp nguồn hoặc một số tệp nguồn.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-129">You can import data from one source file or several source files.</span></span> <span data-ttu-id="7a6a7-130">Tệp nguồn có thể chứa dữ liệu cho một loại thực thể hoặc nhiều loại thực thể.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-130">A source file can contain data for one entity type or multiple entity types.</span></span>  
  
  <span data-ttu-id="7a6a7-131">Parsing, transforming, and uploading of data is done by the asynchronous jobs that run in the background.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-131">Parsing, transforming, and uploading of data is done by the asynchronous jobs that run in the background.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7a6a7-132">By default, all custom entities are enabled for import.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-132">By default, all custom entities are enabled for import.</span></span> <span data-ttu-id="7a6a7-133">To determine if a business entity is enabled for import, see the entity metadata for the specific entity.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-133">To determine if a business entity is enabled for import, see the entity metadata for the specific entity.</span></span> <span data-ttu-id="7a6a7-134">If an entity is enabled for import, the entity metadata property `IsImportable` is set to `true`.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-134">If an entity is enabled for import, the entity metadata property `IsImportable` is set to `true`.</span></span> <span data-ttu-id="7a6a7-135">The value of this property can’t be changed for the out-of-the-box business entities.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-135">The value of this property can’t be changed for the out-of-the-box business entities.</span></span> [!INCLUDE[metadata_browser](../includes/metadata-browser.md)]  
  
## <a name="in-this-section"></a><span data-ttu-id="7a6a7-136">In This Section</span><span class="sxs-lookup"><span data-stu-id="7a6a7-136">In This Section</span></span>  
 [<span data-ttu-id="7a6a7-137">Prepare Source Files</span><span class="sxs-lookup"><span data-stu-id="7a6a7-137">Prepare Source Files</span></span>](prepare-source-files-import.md)  
  
 [<span data-ttu-id="7a6a7-138">Create Data Maps</span><span class="sxs-lookup"><span data-stu-id="7a6a7-138">Create Data Maps</span></span>](create-data-maps-for-import.md)  
  
 [<span data-ttu-id="7a6a7-139">Add Transformation Mapping</span><span class="sxs-lookup"><span data-stu-id="7a6a7-139">Add Transformation Mapping</span></span>](add-transformation-mappings-import.md)  
  
 [<span data-ttu-id="7a6a7-140">Configure Data Import</span><span class="sxs-lookup"><span data-stu-id="7a6a7-140">Configure Data Import</span></span>](configure-data-import.md)  
  
 [<span data-ttu-id="7a6a7-141">Run Data Import</span><span class="sxs-lookup"><span data-stu-id="7a6a7-141">Run Data Import</span></span>](run-data-import.md)  
  
 [<span data-ttu-id="7a6a7-142">Data Import Entities</span><span class="sxs-lookup"><span data-stu-id="7a6a7-142">Data Import Entities</span></span>](data-import-entities.md)  
  
 [<span data-ttu-id="7a6a7-143">Sample: Export and Import a Data Map</span><span class="sxs-lookup"><span data-stu-id="7a6a7-143">Sample: Export and Import a Data Map</span></span>](sample-export-import-data-map.md)  
  
 [<span data-ttu-id="7a6a7-144">Sample: Import Data Using Complex Data Map</span><span class="sxs-lookup"><span data-stu-id="7a6a7-144">Sample: Import Data Using Complex Data Map</span></span>](sample-import-data-complex-data-map.md)  
  
## <a name="related-sections"></a><span data-ttu-id="7a6a7-145">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="7a6a7-145">Related Sections</span></span>  
 [<span data-ttu-id="7a6a7-146">Data Management in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="7a6a7-146">Data Management in Dynamics 365 for Customer Engagement apps</span></span>](manage-data.md)
