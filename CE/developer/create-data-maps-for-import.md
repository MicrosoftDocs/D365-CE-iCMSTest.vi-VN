---
title: Create data maps for import (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Data maps are required to import data, and contain mappings between the data contained in the source file and the respective entity attributes.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: ceb6ccb2-8a9f-4d96-9f93-8d7281e127fa
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 416301715965a410fdf59d9fce2db6a38f52665e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385741"
---
# <a name="create-data-maps-for-import"></a><span data-ttu-id="c2b13-103">Create data maps for import</span><span class="sxs-lookup"><span data-stu-id="c2b13-103">Create data maps for import</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="c2b13-104">To import data into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], you must provide the appropriate data maps.</span><span class="sxs-lookup"><span data-stu-id="c2b13-104">To import data into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], you must provide the appropriate data maps.</span></span>  
  
 <span data-ttu-id="c2b13-105">You can download examples of data maps from [Microsoft Downloads: DataImportMaps.zip](http://download.microsoft.com/download/D/5/F/D5F73E15-439B-4EBC-BFFB-C6837B146C76/DataImportMaps.zip).</span><span class="sxs-lookup"><span data-stu-id="c2b13-105">You can download examples of data maps from [Microsoft Downloads: DataImportMaps.zip](http://download.microsoft.com/download/D/5/F/D5F73E15-439B-4EBC-BFFB-C6837B146C76/DataImportMaps.zip).</span></span>
  
 <span data-ttu-id="c2b13-106">You use data maps to map the data contained in the source file to the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps entity attributes.</span><span class="sxs-lookup"><span data-stu-id="c2b13-106">You use data maps to map the data contained in the source file to the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps entity attributes.</span></span> <span data-ttu-id="c2b13-107">You must map every column in the source file to an appropriate attribute.</span><span class="sxs-lookup"><span data-stu-id="c2b13-107">You must map every column in the source file to an appropriate attribute.</span></span> <span data-ttu-id="c2b13-108">The data in the unmapped columns is not imported during the data import operation.</span><span class="sxs-lookup"><span data-stu-id="c2b13-108">The data in the unmapped columns is not imported during the data import operation.</span></span>  
  
 <span data-ttu-id="c2b13-109">The data map is represented by the import map (data map) entity.</span><span class="sxs-lookup"><span data-stu-id="c2b13-109">The data map is represented by the import map (data map) entity.</span></span> <span data-ttu-id="c2b13-110">You can create a new map by using the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message or update an existing map by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span><span class="sxs-lookup"><span data-stu-id="c2b13-110">You can create a new map by using the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message or update an existing map by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span></span> <span data-ttu-id="c2b13-111">method.</span><span class="sxs-lookup"><span data-stu-id="c2b13-111">method.</span></span> <span data-ttu-id="c2b13-112">The map has a unique name that is contained in the `ImportMap.Name` attribute.</span><span class="sxs-lookup"><span data-stu-id="c2b13-112">The map has a unique name that is contained in the `ImportMap.Name` attribute.</span></span> <span data-ttu-id="c2b13-113">You can specify the name of the import source for which this data map is created by using the `ImportMap.Source` attribute.</span><span class="sxs-lookup"><span data-stu-id="c2b13-113">You can specify the name of the import source for which this data map is created by using the `ImportMap.Source` attribute.</span></span>  
  
<a name="BKMK_Column"></a>   
## <a name="column-list-value-and-lookup-mappings"></a><span data-ttu-id="c2b13-114">Column, list value, and lookup mappings</span><span class="sxs-lookup"><span data-stu-id="c2b13-114">Column, list value, and lookup mappings</span></span>  
 <span data-ttu-id="c2b13-115">To map a column, a list value, or lookup value in the source file to a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps attribute, use the following mappings:</span><span class="sxs-lookup"><span data-stu-id="c2b13-115">To map a column, a list value, or lookup value in the source file to a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps attribute, use the following mappings:</span></span>  
  
 <span data-ttu-id="c2b13-116">**Column Mapping**</span><span class="sxs-lookup"><span data-stu-id="c2b13-116">**Column Mapping**</span></span>  
  
 <span data-ttu-id="c2b13-117">Maps a column in a source file to a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps entity attribute.</span><span class="sxs-lookup"><span data-stu-id="c2b13-117">Maps a column in a source file to a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps entity attribute.</span></span> <span data-ttu-id="c2b13-118">For column mapping, use the column mapping (`ColumnMapping`) entity.</span><span class="sxs-lookup"><span data-stu-id="c2b13-118">For column mapping, use the column mapping (`ColumnMapping`) entity.</span></span> <span data-ttu-id="c2b13-119">You can use 1:1 (one-to-one) or 1:N (one-to-many) relationships between source and target attributes.</span><span class="sxs-lookup"><span data-stu-id="c2b13-119">You can use 1:1 (one-to-one) or 1:N (one-to-many) relationships between source and target attributes.</span></span> <span data-ttu-id="c2b13-120">For example, you can map account address information to the billing and shipping addresses in an order.</span><span class="sxs-lookup"><span data-stu-id="c2b13-120">For example, you can map account address information to the billing and shipping addresses in an order.</span></span>  
  
 <span data-ttu-id="c2b13-121">**List Value Mapping**</span><span class="sxs-lookup"><span data-stu-id="c2b13-121">**List Value Mapping**</span></span>  
  
 <span data-ttu-id="c2b13-122">Maps a list value in a source file to a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps attribute of the <xref:Microsoft.Xrm.Sdk.OptionSetValue> type.</span><span class="sxs-lookup"><span data-stu-id="c2b13-122">Maps a list value in a source file to a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps attribute of the <xref:Microsoft.Xrm.Sdk.OptionSetValue> type.</span></span> <span data-ttu-id="c2b13-123">For list value mapping, use the picklist mapping (`PicklistMapping`) entity.</span><span class="sxs-lookup"><span data-stu-id="c2b13-123">For list value mapping, use the picklist mapping (`PicklistMapping`) entity.</span></span>  
  
 <span data-ttu-id="c2b13-124">If a value specified in the source file column is a list value, such as an OptionSetValue, Status, State, and Boolean, you must provide a list value mapping additionally to a column mapping.</span><span class="sxs-lookup"><span data-stu-id="c2b13-124">If a value specified in the source file column is a list value, such as an OptionSetValue, Status, State, and Boolean, you must provide a list value mapping additionally to a column mapping.</span></span> <span data-ttu-id="c2b13-125">For example, map the "bill" and "ship" list values in the source file to the bill and ship values of the <xref:Microsoft.Xrm.Sdk.OptionSetValue> type.</span><span class="sxs-lookup"><span data-stu-id="c2b13-125">For example, map the "bill" and "ship" list values in the source file to the bill and ship values of the <xref:Microsoft.Xrm.Sdk.OptionSetValue> type.</span></span>  
  
 <span data-ttu-id="c2b13-126">**Lookup Mapping**</span><span class="sxs-lookup"><span data-stu-id="c2b13-126">**Lookup Mapping**</span></span>  
  
 <span data-ttu-id="c2b13-127">Maps a lookup value in a source file to a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps attribute of the <xref:Microsoft.Xrm.Sdk.EntityReference> type.</span><span class="sxs-lookup"><span data-stu-id="c2b13-127">Maps a lookup value in a source file to a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps attribute of the <xref:Microsoft.Xrm.Sdk.EntityReference> type.</span></span> <span data-ttu-id="c2b13-128">For lookup mapping, use the lookup mapping (`LookupMapping`) entity.</span><span class="sxs-lookup"><span data-stu-id="c2b13-128">For lookup mapping, use the lookup mapping (`LookupMapping`) entity.</span></span>  
  
 <span data-ttu-id="c2b13-129">If the value specified in the source file references an entity, you must provide a lookup mapping for this value.</span><span class="sxs-lookup"><span data-stu-id="c2b13-129">If the value specified in the source file references an entity, you must provide a lookup mapping for this value.</span></span> <span data-ttu-id="c2b13-130">Use the `LookupMapping.LookupSourceCode` attribute to specify whether to search for the referenced entity inside the source file or inside [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="c2b13-130">Use the `LookupMapping.LookupSourceCode` attribute to specify whether to search for the referenced entity inside the source file or inside [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span> <span data-ttu-id="c2b13-131">If you are using early bound types, you can use the `LookupSourceType` enumeration to set the lookup values.</span><span class="sxs-lookup"><span data-stu-id="c2b13-131">If you are using early bound types, you can use the `LookupSourceType` enumeration to set the lookup values.</span></span> <span data-ttu-id="c2b13-132">To search inside the source file, use the `LookupSourceType.Source` value.</span><span class="sxs-lookup"><span data-stu-id="c2b13-132">To search inside the source file, use the `LookupSourceType.Source` value.</span></span> <span data-ttu-id="c2b13-133">To search inside [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, use the `LookupSourceType.System` value.</span><span class="sxs-lookup"><span data-stu-id="c2b13-133">To search inside [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, use the `LookupSourceType.System` value.</span></span> <span data-ttu-id="c2b13-134">For a list of the LookupSourceCode values, see the picklist values for this entity.</span><span class="sxs-lookup"><span data-stu-id="c2b13-134">For a list of the LookupSourceCode values, see the picklist values for this entity.</span></span> [!INCLUDE[metadata_browser](../includes/metadata-browser.md)] <span data-ttu-id="c2b13-135">You can provide multiple lookup mappings.</span><span class="sxs-lookup"><span data-stu-id="c2b13-135">You can provide multiple lookup mappings.</span></span> <span data-ttu-id="c2b13-136">The asynchronous transformation job processes all available mappings.</span><span class="sxs-lookup"><span data-stu-id="c2b13-136">The asynchronous transformation job processes all available mappings.</span></span> <span data-ttu-id="c2b13-137">It finds the referenced records and updates the parse table with the record unique identifiers.</span><span class="sxs-lookup"><span data-stu-id="c2b13-137">It finds the referenced records and updates the parse table with the record unique identifiers.</span></span> <span data-ttu-id="c2b13-138">For more information, see [Run Data Import](run-data-import.md).</span><span class="sxs-lookup"><span data-stu-id="c2b13-138">For more information, see [Run Data Import](run-data-import.md).</span></span>  
  
<a name="BKMK_Owner"></a>   
## <a name="owner-mapping"></a><span data-ttu-id="c2b13-139">Owner mapping</span><span class="sxs-lookup"><span data-stu-id="c2b13-139">Owner mapping</span></span>  
 <span data-ttu-id="c2b13-140">Use owner mapping to map a user specified in the source file to a user in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="c2b13-140">Use owner mapping to map a user specified in the source file to a user in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span> <span data-ttu-id="c2b13-141">For logging information, use the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps user logon name.</span><span class="sxs-lookup"><span data-stu-id="c2b13-141">For logging information, use the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps user logon name.</span></span> <span data-ttu-id="c2b13-142">For owner mapping, use the owner mapping (`OwnerMapping`) entity.</span><span class="sxs-lookup"><span data-stu-id="c2b13-142">For owner mapping, use the owner mapping (`OwnerMapping`) entity.</span></span>  
  
<a name="BKMK_Notes"></a>   
## <a name="notes-and-attachments"></a><span data-ttu-id="c2b13-143">Notes and attachments</span><span class="sxs-lookup"><span data-stu-id="c2b13-143">Notes and attachments</span></span>  
 <span data-ttu-id="c2b13-144">Mapping for notes and attachments is handled differently from other entities.</span><span class="sxs-lookup"><span data-stu-id="c2b13-144">Mapping for notes and attachments is handled differently from other entities.</span></span> <span data-ttu-id="c2b13-145">Notes and attachments are used to append additional information to a record in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="c2b13-145">Notes and attachments are used to append additional information to a record in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span> <span data-ttu-id="c2b13-146">Notes are stored as text and attachments are stored as files in the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps database.</span><span class="sxs-lookup"><span data-stu-id="c2b13-146">Notes are stored as text and attachments are stored as files in the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps database.</span></span>  
  
 <span data-ttu-id="c2b13-147">To create a note in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, set the `Annotation.IsDocument` attribute in the annotation (note) entity to `false`.</span><span class="sxs-lookup"><span data-stu-id="c2b13-147">To create a note in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, set the `Annotation.IsDocument` attribute in the annotation (note) entity to `false`.</span></span> <span data-ttu-id="c2b13-148">To create an attachment, set `IsDocument` to `true`.</span><span class="sxs-lookup"><span data-stu-id="c2b13-148">To create an attachment, set `IsDocument` to `true`.</span></span>  
  
 <span data-ttu-id="c2b13-149">Use the following settings for mapping notes and attachments:</span><span class="sxs-lookup"><span data-stu-id="c2b13-149">Use the following settings for mapping notes and attachments:</span></span>  
  
- <span data-ttu-id="c2b13-150">Set the `ColumnMapping.SourceAttributeName` attribute to “`true`” or “`false`”.</span><span class="sxs-lookup"><span data-stu-id="c2b13-150">Set the `ColumnMapping.SourceAttributeName` attribute to “`true`” or “`false`”.</span></span> <span data-ttu-id="c2b13-151">The “`true`” value indicates an attachment.</span><span class="sxs-lookup"><span data-stu-id="c2b13-151">The “`true`” value indicates an attachment.</span></span> <span data-ttu-id="c2b13-152">The “`false`” value indicates a note.</span><span class="sxs-lookup"><span data-stu-id="c2b13-152">The “`false`” value indicates a note.</span></span>  
  
- <span data-ttu-id="c2b13-153">Set the `ColumnMapping.TargetAttributeName` attribute to `IsDocument`.</span><span class="sxs-lookup"><span data-stu-id="c2b13-153">Set the `ColumnMapping.TargetAttributeName` attribute to `IsDocument`.</span></span>  
  
- <span data-ttu-id="c2b13-154">Set the `ColumnMapping.ProcessCode` attribute to the `ImportProcessCode.Internal` value of the `ImportProcessCode` enumeration, if you are using early bound types.</span><span class="sxs-lookup"><span data-stu-id="c2b13-154">Set the `ColumnMapping.ProcessCode` attribute to the `ImportProcessCode.Internal` value of the `ImportProcessCode` enumeration, if you are using early bound types.</span></span> <span data-ttu-id="c2b13-155">For a list of the ProcessCode values, see the picklist values for this entity.</span><span class="sxs-lookup"><span data-stu-id="c2b13-155">For a list of the ProcessCode values, see the picklist values for this entity.</span></span>  
  
  <span data-ttu-id="c2b13-156">If the source data represents a note, map the text of the note to the `Annotation.NoteText` attribute.</span><span class="sxs-lookup"><span data-stu-id="c2b13-156">If the source data represents a note, map the text of the note to the `Annotation.NoteText` attribute.</span></span> <span data-ttu-id="c2b13-157">If you are working with Salesforce files, they are usually stored on the disk under unique identification numbers.</span><span class="sxs-lookup"><span data-stu-id="c2b13-157">If you are working with Salesforce files, they are usually stored on the disk under unique identification numbers.</span></span> <span data-ttu-id="c2b13-158">To import an attachment, you must map a file identification number that is contained in the source file to the `Annotation.DocumentBody` attribute.</span><span class="sxs-lookup"><span data-stu-id="c2b13-158">To import an attachment, you must map a file identification number that is contained in the source file to the `Annotation.DocumentBody` attribute.</span></span> <span data-ttu-id="c2b13-159">The `DocumentBody` attribute stores the contents of the attachment.</span><span class="sxs-lookup"><span data-stu-id="c2b13-159">The `DocumentBody` attribute stores the contents of the attachment.</span></span>  
  
  <span data-ttu-id="c2b13-160">The import asynchronous job checks for mappings that have the source attribute name set to “`true`” and “`false`” to discover notes and attachments.</span><span class="sxs-lookup"><span data-stu-id="c2b13-160">The import asynchronous job checks for mappings that have the source attribute name set to “`true`” and “`false`” to discover notes and attachments.</span></span> <span data-ttu-id="c2b13-161">If it finds an attachment mapping, it looks for the specified files on the disk and uploads the file contents as attachments into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="c2b13-161">If it finds an attachment mapping, it looks for the specified files on the disk and uploads the file contents as attachments into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span> <span data-ttu-id="c2b13-162">If a file is not found, an error is returned.</span><span class="sxs-lookup"><span data-stu-id="c2b13-162">If a file is not found, an error is returned.</span></span>  
  
  <span data-ttu-id="c2b13-163">If you do not provide mapping for an annotation (note) entity, the import job generates a default mapping for the note.</span><span class="sxs-lookup"><span data-stu-id="c2b13-163">If you do not provide mapping for an annotation (note) entity, the import job generates a default mapping for the note.</span></span>  
  
> [!NOTE]
> [!INCLUDE[sdk_MaxUploadFileSize](../includes/sdk-maxuploadfilesize.md)] <span data-ttu-id="c2b13-164">However, an attachment size cannot exceed the maximum HTTP request size (the default is 16MB).</span><span class="sxs-lookup"><span data-stu-id="c2b13-164">However, an attachment size cannot exceed the maximum HTTP request size (the default is 16MB).</span></span> <span data-ttu-id="c2b13-165">For the change to take effect, reset [!INCLUDE[pn_Internet_Information_Services](../includes/pn-internet-information-services.md)].</span><span class="sxs-lookup"><span data-stu-id="c2b13-165">For the change to take effect, reset [!INCLUDE[pn_Internet_Information_Services](../includes/pn-internet-information-services.md)].</span></span> <span data-ttu-id="c2b13-166">Để làm điều này, bấm vào **bắt đầu**, bấm vào **chạy**, nhập `iisreset`, và sau đó nhấp vào **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2b13-166">To do this, click **Start**, click **Run**, type `iisreset`, and then click **OK**.</span></span>  
  
<a name="BKMK_ImportExport"></a>   
## <a name="import-and-export-data-maps"></a><span data-ttu-id="c2b13-167">Import and export data maps</span><span class="sxs-lookup"><span data-stu-id="c2b13-167">Import and export data maps</span></span>  
 <span data-ttu-id="c2b13-168">You can export an existing data map to an XML file and import XML data mappings into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="c2b13-168">You can export an existing data map to an XML file and import XML data mappings into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span> <span data-ttu-id="c2b13-169">To export a data map from [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], use the <xref:Microsoft.Crm.Sdk.Messages.ExportMappingsImportMapRequest> message.</span><span class="sxs-lookup"><span data-stu-id="c2b13-169">To export a data map from [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], use the <xref:Microsoft.Crm.Sdk.Messages.ExportMappingsImportMapRequest> message.</span></span> <span data-ttu-id="c2b13-170">To import XML data mappings and create a data map in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], use the <xref:Microsoft.Crm.Sdk.Messages.ImportMappingsImportMapRequest> message.</span><span class="sxs-lookup"><span data-stu-id="c2b13-170">To import XML data mappings and create a data map in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], use the <xref:Microsoft.Crm.Sdk.Messages.ImportMappingsImportMapRequest> message.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c2b13-171">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c2b13-171">See also</span></span>  
 <span data-ttu-id="c2b13-172">[Import Data in Dynamics 365 for Customer Engagement apps](import-data.md) </span><span class="sxs-lookup"><span data-stu-id="c2b13-172">[Import Data in Dynamics 365 for Customer Engagement apps](import-data.md) </span></span>  
 <span data-ttu-id="c2b13-173">[Add Transformation Mapping](add-transformation-mappings-import.md) </span><span class="sxs-lookup"><span data-stu-id="c2b13-173">[Add Transformation Mapping](add-transformation-mappings-import.md) </span></span>  
 [<span data-ttu-id="c2b13-174">Add Transformation Mappings for Import</span><span class="sxs-lookup"><span data-stu-id="c2b13-174">Add Transformation Mappings for Import</span></span>](add-transformation-mappings-import.md)