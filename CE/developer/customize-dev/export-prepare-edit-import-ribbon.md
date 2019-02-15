---
title: Export, prepare to edit, and import the ribbon (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: 'Learn about exporting the ribbon by including it in a solution and then exporting the solution. You can export all the customizations, but that can represent a large amount of data. We recommend that you use an existing unmanaged solution or create a new solution. '
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
- ribbon, export ribbons
- ribbon, import
- ribbon, editing
ms.assetid: 1052a9f4-9cb9-4d2f-a131-427a496cac00
caps.latest.revision: 36
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0945c6ded008081c5532b06e5f1630c3d92651af
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386371"
---
# <a name="export-prepare-to-edit-and-import-the-ribbon"></a><span data-ttu-id="3e19c-105">Export, prepare to edit, and import the ribbon</span><span class="sxs-lookup"><span data-stu-id="3e19c-105">Export, prepare to edit, and import the ribbon</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3e19c-106">To edit the ribbon, you must perform the following steps:</span><span class="sxs-lookup"><span data-stu-id="3e19c-106">To edit the ribbon, you must perform the following steps:</span></span>  
  
1.  [<span data-ttu-id="3e19c-107">Export the ribbon</span><span class="sxs-lookup"><span data-stu-id="3e19c-107">Export the ribbon</span></span>](export-prepare-edit-import-ribbon.md#BKMK_ExportTheRibbon)  
  
2.  [<span data-ttu-id="3e19c-108">Prepare to edit the XML</span><span class="sxs-lookup"><span data-stu-id="3e19c-108">Prepare to edit the XML</span></span>](export-prepare-edit-import-ribbon.md#BKMK_PrepareToEditTheXML)  
  
3.  <span data-ttu-id="3e19c-109">Edit the `<RibbonDiffXml>`</span><span class="sxs-lookup"><span data-stu-id="3e19c-109">Edit the `<RibbonDiffXml>`</span></span>  
  
4.  [<span data-ttu-id="3e19c-110">Import the ribbon</span><span class="sxs-lookup"><span data-stu-id="3e19c-110">Import the ribbon</span></span>](export-prepare-edit-import-ribbon.md#BKMK_ImportTheRibbon)  
  
<a name="BKMK_ExportTheRibbon"></a>   
## <a name="export-the-ribbon"></a><span data-ttu-id="3e19c-111">Export the ribbon</span><span class="sxs-lookup"><span data-stu-id="3e19c-111">Export the ribbon</span></span>  
 <span data-ttu-id="3e19c-112">You export the ribbon by including it in a solution and then exporting the solution.</span><span class="sxs-lookup"><span data-stu-id="3e19c-112">You export the ribbon by including it in a solution and then exporting the solution.</span></span> <span data-ttu-id="3e19c-113">You can export all the customizations, but that can represent a large amount of data.</span><span class="sxs-lookup"><span data-stu-id="3e19c-113">You can export all the customizations, but that can represent a large amount of data.</span></span> <span data-ttu-id="3e19c-114">We recommend that you use an existing unmanaged solution or create a new solution.</span><span class="sxs-lookup"><span data-stu-id="3e19c-114">We recommend that you use an existing unmanaged solution or create a new solution.</span></span>  
  
#### <a name="create-a-new-solution"></a><span data-ttu-id="3e19c-115">Tạo một giải pháp mới</span><span class="sxs-lookup"><span data-stu-id="3e19c-115">Create a new solution</span></span>  
  
1. [!INCLUDE[proc_logo_settings](../../includes/proc-logo-settings.md)]  
  
2. [!INCLUDE[proc_settings_customization](../../includes/proc-settings-customization.md)]  
  
3. [!INCLUDE[proc_settings_solutions](../../includes/proc-settings-solutions.md)]  
  
4. <span data-ttu-id="3e19c-116">Nhấp hoặc gõ nhẹ vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-116">Click or tap **New**.</span></span>  
  
5. <span data-ttu-id="3e19c-117">Type a meaningful **Display Name**, **Unique Name** and enter a **Publisher** and type a **Version** number.</span><span class="sxs-lookup"><span data-stu-id="3e19c-117">Type a meaningful **Display Name**, **Unique Name** and enter a **Publisher** and type a **Version** number.</span></span>  
  
   > [!NOTE]
   >  <span data-ttu-id="3e19c-118">You can usually use the default publisher for the organization.</span><span class="sxs-lookup"><span data-stu-id="3e19c-118">You can usually use the default publisher for the organization.</span></span>  
  
6. <span data-ttu-id="3e19c-119">Click the **Save** icon.</span><span class="sxs-lookup"><span data-stu-id="3e19c-119">Click the **Save** icon.</span></span>  
  
7. <span data-ttu-id="3e19c-120">If you want to edit the ribbon for specific entities:</span><span class="sxs-lookup"><span data-stu-id="3e19c-120">If you want to edit the ribbon for specific entities:</span></span>  
  
   1.  <span data-ttu-id="3e19c-121">Click **Add Existing** and then click **Entity**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-121">Click **Add Existing** and then click **Entity**.</span></span>  
  
   2.  <span data-ttu-id="3e19c-122">Select the entities you want to include in the Solution and then click **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-122">Select the entities you want to include in the Solution and then click **OK**.</span></span>  
  
       > [!NOTE]
       >  <span data-ttu-id="3e19c-123">For the purpose of editing entity ribbons, you do not have to include required components.</span><span class="sxs-lookup"><span data-stu-id="3e19c-123">For the purpose of editing entity ribbons, you do not have to include required components.</span></span> <span data-ttu-id="3e19c-124">If you intend to export this solution and apply it to another system, you should include required components.</span><span class="sxs-lookup"><span data-stu-id="3e19c-124">If you intend to export this solution and apply it to another system, you should include required components.</span></span>  
  
8. <span data-ttu-id="3e19c-125">If you want to edit global ribbons or add a custom group to all entities, click **Add Existing** and then click **Application Ribbons**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-125">If you want to edit global ribbons or add a custom group to all entities, click **Add Existing** and then click **Application Ribbons**.</span></span>  
  
9. <span data-ttu-id="3e19c-126">Click **Save and Close**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-126">Click **Save and Close**.</span></span>  
  
#### <a name="use-an-existing-solution"></a><span data-ttu-id="3e19c-127">Use an existing solution</span><span class="sxs-lookup"><span data-stu-id="3e19c-127">Use an existing solution</span></span>  
  
1. [!INCLUDE[proc_logo_settings](../../includes/proc-logo-settings.md)]  
  
2. [!INCLUDE[proc_settings_customization](../../includes/proc-settings-customization.md)]  
  
3. [!INCLUDE[proc_settings_solutions](../../includes/proc-settings-solutions.md)]  
  
4. <span data-ttu-id="3e19c-128">Double-click a solution to open it.</span><span class="sxs-lookup"><span data-stu-id="3e19c-128">Double-click a solution to open it.</span></span>  
  
5. <span data-ttu-id="3e19c-129">If you want to edit the ribbon for specific entities:</span><span class="sxs-lookup"><span data-stu-id="3e19c-129">If you want to edit the ribbon for specific entities:</span></span>  
  
   1.  <span data-ttu-id="3e19c-130">Click **Add Existing** and then click **Entity**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-130">Click **Add Existing** and then click **Entity**.</span></span>  
  
   2.  <span data-ttu-id="3e19c-131">Select the entities you want to include in the Solution and then click **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-131">Select the entities you want to include in the Solution and then click **OK**.</span></span>  
  
       > [!NOTE]
       >  <span data-ttu-id="3e19c-132">For the purpose of editing entity ribbons, you do not have to include required components.</span><span class="sxs-lookup"><span data-stu-id="3e19c-132">For the purpose of editing entity ribbons, you do not have to include required components.</span></span> <span data-ttu-id="3e19c-133">If you intend to export this solution and apply it to another system, you should include required components.</span><span class="sxs-lookup"><span data-stu-id="3e19c-133">If you intend to export this solution and apply it to another system, you should include required components.</span></span>  
  
6. <span data-ttu-id="3e19c-134">If you want to edit global ribbons, such as to add custom button to all entities: click **Add Existing** and then click **Application Ribbons**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-134">If you want to edit global ribbons, such as to add custom button to all entities: click **Add Existing** and then click **Application Ribbons**.</span></span>  
  
7. <span data-ttu-id="3e19c-135">Click **Save and Close**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-135">Click **Save and Close**.</span></span>  
  
#### <a name="export-the-ribbon"></a><span data-ttu-id="3e19c-136">Export the ribbon</span><span class="sxs-lookup"><span data-stu-id="3e19c-136">Export the ribbon</span></span>  
  
1. [!INCLUDE[proc_logo_settings](../../includes/proc-logo-settings.md)]  
  
2. [!INCLUDE[proc_settings_customization](../../includes/proc-settings-customization.md)]  
  
3. [!INCLUDE[proc_settings_solutions](../../includes/proc-settings-solutions.md)]  
  
4. <span data-ttu-id="3e19c-137">Select the solution you want and then click **Export**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-137">Select the solution you want and then click **Export**.</span></span>  
  
5. <span data-ttu-id="3e19c-138">If you have made recent changes that have not yet been published, click **Publish All Customizations**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-138">If you have made recent changes that have not yet been published, click **Publish All Customizations**.</span></span> <span data-ttu-id="3e19c-139">Nếu không, bấm vào **Tiếp tục**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-139">Otherwise, click **Next**.</span></span>  
  
6. <span data-ttu-id="3e19c-140">With the **Unmanaged** option selected, click **Export**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-140">With the **Unmanaged** option selected, click **Export**.</span></span>  
  
7. <span data-ttu-id="3e19c-141">Click **Save** in the **File Download** dialog box and then click **Open Folder** in the **Download complete** dialog box.</span><span class="sxs-lookup"><span data-stu-id="3e19c-141">Click **Save** in the **File Download** dialog box and then click **Open Folder** in the **Download complete** dialog box.</span></span>  
  
8. <span data-ttu-id="3e19c-142">Right-click the compressed .zip file that you downloaded and select **Extract All...** .</span><span class="sxs-lookup"><span data-stu-id="3e19c-142">Right-click the compressed .zip file that you downloaded and select **Extract All...** .</span></span>  
  
9. <span data-ttu-id="3e19c-143">Select a location to extract the files and then click **Extract**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-143">Select a location to extract the files and then click **Extract**.</span></span>  
  
10. <span data-ttu-id="3e19c-144">The customizations.xml file is the file that you will edit.</span><span class="sxs-lookup"><span data-stu-id="3e19c-144">The customizations.xml file is the file that you will edit.</span></span>  
  
<a name="BKMK_PrepareToEditTheXML"></a>   
## <a name="prepare-to-edit-the-xml"></a><span data-ttu-id="3e19c-145">Prepare to edit the XML</span><span class="sxs-lookup"><span data-stu-id="3e19c-145">Prepare to edit the XML</span></span>  
 <span data-ttu-id="3e19c-146">For a better experience, edit the customizations.xml file with an application that can use schema validation to provide [!INCLUDE[pn_IntelliSense](../../includes/pn-intellisense.md)] support.</span><span class="sxs-lookup"><span data-stu-id="3e19c-146">For a better experience, edit the customizations.xml file with an application that can use schema validation to provide [!INCLUDE[pn_IntelliSense](../../includes/pn-intellisense.md)] support.</span></span> <span data-ttu-id="3e19c-147">For more information, see [Edit the Customizations file with Schema Validation](edit-customizations-xml-file-schema-validation.md).</span><span class="sxs-lookup"><span data-stu-id="3e19c-147">For more information, see [Edit the Customizations file with Schema Validation](edit-customizations-xml-file-schema-validation.md).</span></span>  
  
<a name="BKMK_ImportTheRibbon"></a>   
## <a name="import-the-ribbon"></a><span data-ttu-id="3e19c-148">Import the ribbon</span><span class="sxs-lookup"><span data-stu-id="3e19c-148">Import the ribbon</span></span>  
  
1. <span data-ttu-id="3e19c-149">After you have edited the customization.xml file, from [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)] or [!INCLUDE[pn_MS_Visual_Web_Dev_2010_Express](../../includes/pn-ms-visual-web-dev-2010-express.md)], right-click the customization.xml tab and select **Open Containing Folder**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-149">After you have edited the customization.xml file, from [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)] or [!INCLUDE[pn_MS_Visual_Web_Dev_2010_Express](../../includes/pn-ms-visual-web-dev-2010-express.md)], right-click the customization.xml tab and select **Open Containing Folder**.</span></span>  
  
2. <span data-ttu-id="3e19c-150">Select all of the files or folders that were included when you extracted the solution.</span><span class="sxs-lookup"><span data-stu-id="3e19c-150">Select all of the files or folders that were included when you extracted the solution.</span></span> <span data-ttu-id="3e19c-151">Right-click the selected files, select **Send To**, and then select **Compressed (zipped) folder**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-151">Right-click the selected files, select **Send To**, and then select **Compressed (zipped) folder**.</span></span>  
  
   > [!NOTE]
   >  <span data-ttu-id="3e19c-152">This creates a compressed .zip file in the same folder.</span><span class="sxs-lookup"><span data-stu-id="3e19c-152">This creates a compressed .zip file in the same folder.</span></span> <span data-ttu-id="3e19c-153">The name of the file may vary, but it will be the same as one of the other files in the folder - except with a .zip file name extension.</span><span class="sxs-lookup"><span data-stu-id="3e19c-153">The name of the file may vary, but it will be the same as one of the other files in the folder - except with a .zip file name extension.</span></span>  
  
3. [!INCLUDE[proc_logo_settings](../../includes/proc-logo-settings.md)]  
  
4. [!INCLUDE[proc_settings_customization](../../includes/proc-settings-customization.md)]  
  
5. [!INCLUDE[proc_settings_solutions](../../includes/proc-settings-solutions.md)]  
  
6. <span data-ttu-id="3e19c-154">Bấm vào **Nhập**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-154">Click **Import**.</span></span>  
  
7. <span data-ttu-id="3e19c-155">Click **Browse** and locate the compressed .zip file that you created in step 2 of this procedure.</span><span class="sxs-lookup"><span data-stu-id="3e19c-155">Click **Browse** and locate the compressed .zip file that you created in step 2 of this procedure.</span></span>  
  
8. <span data-ttu-id="3e19c-156">Click **Next** and then click **Import**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-156">Click **Next** and then click **Import**.</span></span>  
  
9. <span data-ttu-id="3e19c-157">After the import has finished, you will see the message indicating that the import completed successfully.</span><span class="sxs-lookup"><span data-stu-id="3e19c-157">After the import has finished, you will see the message indicating that the import completed successfully.</span></span> <span data-ttu-id="3e19c-158">Bấm vào Đóng.</span><span class="sxs-lookup"><span data-stu-id="3e19c-158">Click Close.</span></span>  
  
10. <span data-ttu-id="3e19c-159">After you have successfully imported your solution, you must publish customizations before you can see the changes.</span><span class="sxs-lookup"><span data-stu-id="3e19c-159">After you have successfully imported your solution, you must publish customizations before you can see the changes.</span></span> <span data-ttu-id="3e19c-160">In the Solutions list, click **Publish All Customizations**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-160">In the Solutions list, click **Publish All Customizations**.</span></span>  
  
<a name="BKMK_DealWithErrorsOnImport"></a>   
### <a name="dealing-with-errors-on-import"></a><span data-ttu-id="3e19c-161">Dealing with errors on import</span><span class="sxs-lookup"><span data-stu-id="3e19c-161">Dealing with errors on import</span></span>  
  
1.  <span data-ttu-id="3e19c-162">If you receive a notification that there were errors that caused the import to fail, click **Export Log**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-162">If you receive a notification that there were errors that caused the import to fail, click **Export Log**.</span></span>  
  
2.  <span data-ttu-id="3e19c-163">Save the export log file.</span><span class="sxs-lookup"><span data-stu-id="3e19c-163">Save the export log file.</span></span> <span data-ttu-id="3e19c-164">Select the file and right-click it.</span><span class="sxs-lookup"><span data-stu-id="3e19c-164">Select the file and right-click it.</span></span> <span data-ttu-id="3e19c-165">Click **Open With** and then select **Microsoft Office Excel**.</span><span class="sxs-lookup"><span data-stu-id="3e19c-165">Click **Open With** and then select **Microsoft Office Excel**.</span></span>  
  
3.  <span data-ttu-id="3e19c-166">Select the **Components** worksheet and note any messages in the **ErrorText** column.</span><span class="sxs-lookup"><span data-stu-id="3e19c-166">Select the **Components** worksheet and note any messages in the **ErrorText** column.</span></span>  
  
    > [!TIP]
    >  <span data-ttu-id="3e19c-167">The most common type of failure is an error when referencing a dependent element in the RibbonDiffXml.</span><span class="sxs-lookup"><span data-stu-id="3e19c-167">The most common type of failure is an error when referencing a dependent element in the RibbonDiffXml.</span></span> <span data-ttu-id="3e19c-168">Perhaps you forgot to include a LocLabel that was referenced somewhere.</span><span class="sxs-lookup"><span data-stu-id="3e19c-168">Perhaps you forgot to include a LocLabel that was referenced somewhere.</span></span> <span data-ttu-id="3e19c-169">Perhaps there is an extra blank character included at the end of an XML attribute referencing another element.</span><span class="sxs-lookup"><span data-stu-id="3e19c-169">Perhaps there is an extra blank character included at the end of an XML attribute referencing another element.</span></span> <span data-ttu-id="3e19c-170">All references must match exactly.</span><span class="sxs-lookup"><span data-stu-id="3e19c-170">All references must match exactly.</span></span>  
  
4.  <span data-ttu-id="3e19c-171">After you have corrected the error, complete the steps to import the Ribbon again.</span><span class="sxs-lookup"><span data-stu-id="3e19c-171">After you have corrected the error, complete the steps to import the Ribbon again.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="3e19c-172">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3e19c-172">See also</span></span>  
 <span data-ttu-id="3e19c-173">[Customize the Ribbon for Microsoft Dynamics 365 for Customer Engagement](customize-commands-ribbon.md) </span><span class="sxs-lookup"><span data-stu-id="3e19c-173">[Customize the Ribbon for Microsoft Dynamics 365 for Customer Engagement](customize-commands-ribbon.md) </span></span>  
 <span data-ttu-id="3e19c-174">[Export Ribbon Definitions](export-ribbon-definitions.md) </span><span class="sxs-lookup"><span data-stu-id="3e19c-174">[Export Ribbon Definitions](export-ribbon-definitions.md) </span></span>  
 [<span data-ttu-id="3e19c-175">Use Localized Labels with Ribbons</span><span class="sxs-lookup"><span data-stu-id="3e19c-175">Use Localized Labels with Ribbons</span></span>](use-localized-labels-ribbons.md)
