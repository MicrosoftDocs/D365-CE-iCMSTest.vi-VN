---
title: Configure data import (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: 'Configuration information that is required for importing data is contained in the data import entity and the import source file entity. '
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
- data importing, configuring
- configuring data importing, tasks for
- importing data, configuring
- configuring data importing, by using the import (data import) and import file (import source file) entities
ms.assetid: e0b5bdd7-b307-4b26-9171-518cb00ed7b0
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f23951961b5be7ee451c45cfa0b73d52180db49c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386627"
---
# <a name="configure-data-import"></a><span data-ttu-id="96481-103">Configure data import</span><span class="sxs-lookup"><span data-stu-id="96481-103">Configure data import</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="96481-104">The configuration information that is required for importing data is contained in the data import (`Import`) entity and the import source file (`ImportFile`) entity.</span><span class="sxs-lookup"><span data-stu-id="96481-104">The configuration information that is required for importing data is contained in the data import (`Import`) entity and the import source file (`ImportFile`) entity.</span></span>  
  
 <span data-ttu-id="96481-105">To configure data import, do the following:</span><span class="sxs-lookup"><span data-stu-id="96481-105">To configure data import, do the following:</span></span>  
  
- <span data-ttu-id="96481-106">Use the `Import.ModeCode` attribute to specify whether to create or update data during import.</span><span class="sxs-lookup"><span data-stu-id="96481-106">Use the `Import.ModeCode` attribute to specify whether to create or update data during import.</span></span> <span data-ttu-id="96481-107">If you are using early bound types, you can use the `ImportModeCode` enumeration.</span><span class="sxs-lookup"><span data-stu-id="96481-107">If you are using early bound types, you can use the `ImportModeCode` enumeration.</span></span> <span data-ttu-id="96481-108">For a list of the ModeCode values, see the picklist values for this entity.</span><span class="sxs-lookup"><span data-stu-id="96481-108">For a list of the ModeCode values, see the picklist values for this entity.</span></span> [!INCLUDE[metadata_browser](../includes/metadata-browser.md)]  
  
- <span data-ttu-id="96481-109">Use the `ImportFile.FileTypeCode` attribute to specify the type of the import file.</span><span class="sxs-lookup"><span data-stu-id="96481-109">Use the `ImportFile.FileTypeCode` attribute to specify the type of the import file.</span></span> <span data-ttu-id="96481-110">If you are using early bound types, you can use the `ImportFileType` enumeration.</span><span class="sxs-lookup"><span data-stu-id="96481-110">If you are using early bound types, you can use the `ImportFileType` enumeration.</span></span> <span data-ttu-id="96481-111">For a list of the FileTypeCode values, see the picklist values for this entity.</span><span class="sxs-lookup"><span data-stu-id="96481-111">For a list of the FileTypeCode values, see the picklist values for this entity.</span></span> <span data-ttu-id="96481-112">This attribute is only available in [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="96481-112">This attribute is only available in [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)].</span></span>  
  
- <span data-ttu-id="96481-113">Use the `ImportFile.DataDelimiterCode` attribute to specify the single character data delimiter in the import file.</span><span class="sxs-lookup"><span data-stu-id="96481-113">Use the `ImportFile.DataDelimiterCode` attribute to specify the single character data delimiter in the import file.</span></span> <span data-ttu-id="96481-114">If you are using early bound types, you can use the `ImportDataDelimiter` enumeration.</span><span class="sxs-lookup"><span data-stu-id="96481-114">If you are using early bound types, you can use the `ImportDataDelimiter` enumeration.</span></span> <span data-ttu-id="96481-115">For a list of the ImportDataDelimiter values, see the picklist values for this entity.</span><span class="sxs-lookup"><span data-stu-id="96481-115">For a list of the ImportDataDelimiter values, see the picklist values for this entity.</span></span>  
  
- <span data-ttu-id="96481-116">Use the `ImportFile.FieldDelimiterCode` attribute to specify the single character field delimiter in the import file.</span><span class="sxs-lookup"><span data-stu-id="96481-116">Use the `ImportFile.FieldDelimiterCode` attribute to specify the single character field delimiter in the import file.</span></span> <span data-ttu-id="96481-117">If you are using early bound types, you can use the `ImportFieldDelimiter` enumeration.</span><span class="sxs-lookup"><span data-stu-id="96481-117">If you are using early bound types, you can use the `ImportFieldDelimiter` enumeration.</span></span> <span data-ttu-id="96481-118">For a list of the FieldDelimiterCode values, see the picklist values for this entity.</span><span class="sxs-lookup"><span data-stu-id="96481-118">For a list of the FieldDelimiterCode values, see the picklist values for this entity.</span></span>  
  
- <span data-ttu-id="96481-119">Set `ImportFile.IsFirstRowHeader` to `true` to indicate that the first row in the source file contains column headings or to `false` to indicate that the first row contains actual data.</span><span class="sxs-lookup"><span data-stu-id="96481-119">Set `ImportFile.IsFirstRowHeader` to `true` to indicate that the first row in the source file contains column headings or to `false` to indicate that the first row contains actual data.</span></span> <span data-ttu-id="96481-120">If set to `false`, default column headings are generated.</span><span class="sxs-lookup"><span data-stu-id="96481-120">If set to `false`, default column headings are generated.</span></span>  
  
- <span data-ttu-id="96481-121">Set `ImportFile.ImportId` to the ID of the import (data import) that the import file is associated with.</span><span class="sxs-lookup"><span data-stu-id="96481-121">Set `ImportFile.ImportId` to the ID of the import (data import) that the import file is associated with.</span></span>  
  
- <span data-ttu-id="96481-122">Set `ImportFile.ImportMapId` to the ID of the associated import map (data map).</span><span class="sxs-lookup"><span data-stu-id="96481-122">Set `ImportFile.ImportMapId` to the ID of the associated import map (data map).</span></span>  
  
- <span data-ttu-id="96481-123">Set `ImportFile.EnableDuplicateDetection` to `true` to enable duplicate detection during data import.</span><span class="sxs-lookup"><span data-stu-id="96481-123">Set `ImportFile.EnableDuplicateDetection` to `true` to enable duplicate detection during data import.</span></span>  
  
- <span data-ttu-id="96481-124">Read the content of the source file into the `ImportFile.Content`.</span><span class="sxs-lookup"><span data-stu-id="96481-124">Read the content of the source file into the `ImportFile.Content`.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="96481-125">We do not recommend updating records by using data import programmatically.</span><span class="sxs-lookup"><span data-stu-id="96481-125">We do not recommend updating records by using data import programmatically.</span></span> <span data-ttu-id="96481-126">To update, use the data export and import capabilities of the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps Web application.</span><span class="sxs-lookup"><span data-stu-id="96481-126">To update, use the data export and import capabilities of the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps Web application.</span></span> <span data-ttu-id="96481-127">Use **Export to Excel** to export records to an XML Spreadsheet 2003 (.xml) file.</span><span class="sxs-lookup"><span data-stu-id="96481-127">Use **Export to Excel** to export records to an XML Spreadsheet 2003 (.xml) file.</span></span> <span data-ttu-id="96481-128">This is the only valid source file type for the Update mode.</span><span class="sxs-lookup"><span data-stu-id="96481-128">This is the only valid source file type for the Update mode.</span></span> <span data-ttu-id="96481-129">Re-importing data from the XML Spreadsheet 2003 (.xml) source file ensures that the data integrity in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps is maintained.</span><span class="sxs-lookup"><span data-stu-id="96481-129">Re-importing data from the XML Spreadsheet 2003 (.xml) source file ensures that the data integrity in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps is maintained.</span></span> <span data-ttu-id="96481-130">To import updated data, use the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps Import Data Wizard.</span><span class="sxs-lookup"><span data-stu-id="96481-130">To import updated data, use the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps Import Data Wizard.</span></span> <span data-ttu-id="96481-131">For more information about the Import Data Wizard, see [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps Help.</span><span class="sxs-lookup"><span data-stu-id="96481-131">For more information about the Import Data Wizard, see [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps Help.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="96481-132">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="96481-132">See also</span></span>  
 <span data-ttu-id="96481-133">[Import Data in Dynamics 365 for Customer Engagement apps](import-data.md) </span><span class="sxs-lookup"><span data-stu-id="96481-133">[Import Data in Dynamics 365 for Customer Engagement apps](import-data.md) </span></span>  
 <span data-ttu-id="96481-134">[Blog Post: How to Import attachments programmatically](http://blogs.msdn.com/b/crm/archive/2012/08/06/how-to-import-attachments-programmatically.aspx) </span><span class="sxs-lookup"><span data-stu-id="96481-134">[Blog Post: How to Import attachments programmatically](http://blogs.msdn.com/b/crm/archive/2012/08/06/how-to-import-attachments-programmatically.aspx) </span></span>  
 [<span data-ttu-id="96481-135">Run Data Import</span><span class="sxs-lookup"><span data-stu-id="96481-135">Run Data Import</span></span>](run-data-import.md)
