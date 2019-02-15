---
title: Solution component file reference (SolutionPackager) (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: This topic describes the folder structure and file naming scheme used by the SolutionPackager tool. The tool is used to decompose (unpack) Dynamics 365 for Customer Engagement solution files into XML files that can be managed by a source code control system.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: e463a858-2bbd-4fab-b180-36901d238a7e
caps.latest.revision: 27
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: fe72b4acccd69dabe93c899e6f37c1eb47e8c27e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387116"
---
# <a name="solution-component-file-reference-solutionpackager"></a><span data-ttu-id="5575f-104">Solution component file reference (SolutionPackager)</span><span class="sxs-lookup"><span data-stu-id="5575f-104">Solution component file reference (SolutionPackager)</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5575f-105">This topic describes the folder structure and file naming scheme used by the SolutionPackager tool.</span><span class="sxs-lookup"><span data-stu-id="5575f-105">This topic describes the folder structure and file naming scheme used by the SolutionPackager tool.</span></span> <span data-ttu-id="5575f-106">The tool is used to decompose (unpack) [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] solution files into XML files that can be managed by a source code control system.</span><span class="sxs-lookup"><span data-stu-id="5575f-106">The tool is used to decompose (unpack) [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] solution files into XML files that can be managed by a source code control system.</span></span> <span data-ttu-id="5575f-107">The tool can also compile (pack) these individual XML files into a solution file that can be imported into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="5575f-107">The tool can also compile (pack) these individual XML files into a solution file that can be imported into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span> <span data-ttu-id="5575f-108">For more information about the SolutionPackager tool, see [Solution Tools for Team Development](solution-tools-team-development.md).</span><span class="sxs-lookup"><span data-stu-id="5575f-108">For more information about the SolutionPackager tool, see [Solution Tools for Team Development](solution-tools-team-development.md).</span></span>  
  
 <span data-ttu-id="5575f-109">The following sections describe the files that will be created for each solution component type, and which of these files are less suited to inclusion in source control.</span><span class="sxs-lookup"><span data-stu-id="5575f-109">The following sections describe the files that will be created for each solution component type, and which of these files are less suited to inclusion in source control.</span></span> <span data-ttu-id="5575f-110">The folders indicated in the sections are all relative to the folder specified in the `/folder` parameter of the **SolutionPackager** command.</span><span class="sxs-lookup"><span data-stu-id="5575f-110">The folders indicated in the sections are all relative to the folder specified in the `/folder` parameter of the **SolutionPackager** command.</span></span>  
  
<a name="entity_bm"></a>   
## <a name="entity"></a><span data-ttu-id="5575f-111">Thực thể</span><span class="sxs-lookup"><span data-stu-id="5575f-111">Entity</span></span>  
 <span data-ttu-id="5575f-112">Differs in managed solutions: Yes</span><span class="sxs-lookup"><span data-stu-id="5575f-112">Differs in managed solutions: Yes</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-113">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-113">Notes</span></span>  
  
1.  <span data-ttu-id="5575f-114">Each entity has a distinct folder.</span><span class="sxs-lookup"><span data-stu-id="5575f-114">Each entity has a distinct folder.</span></span>  
  
2.  <span data-ttu-id="5575f-115">Each Form, View & Visualization gets their own file in the respective sub-folder.</span><span class="sxs-lookup"><span data-stu-id="5575f-115">Each Form, View & Visualization gets their own file in the respective sub-folder.</span></span>  
  
3.  <span data-ttu-id="5575f-116">The Form file names will vary by Managed or Unmanaged Solution types.</span><span class="sxs-lookup"><span data-stu-id="5575f-116">The Form file names will vary by Managed or Unmanaged Solution types.</span></span>  
  
4.  <span data-ttu-id="5575f-117">Direct editing of RibbonDiff.xml to customize entity specific ribbons is supported.</span><span class="sxs-lookup"><span data-stu-id="5575f-117">Direct editing of RibbonDiff.xml to customize entity specific ribbons is supported.</span></span>  
  
5.  <span data-ttu-id="5575f-118">Manual editing of the XML files under the FormXml and SavedQueries folders is supported but optional.</span><span class="sxs-lookup"><span data-stu-id="5575f-118">Manual editing of the XML files under the FormXml and SavedQueries folders is supported but optional.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-119">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-119">Files</span></span>  
 <span data-ttu-id="5575f-120">\Entities\\<Entity Schema Name\>\\</span><span class="sxs-lookup"><span data-stu-id="5575f-120">\Entities\\<Entity Schema Name\>\\</span></span>  
  
 <span data-ttu-id="5575f-121">Entity.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-121">Entity.xml</span></span>  
<span data-ttu-id="5575f-122">RibbonDiff.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-122">RibbonDiff.xml</span></span>  
  
 <span data-ttu-id="5575f-123">FormXml\Main\\</span><span class="sxs-lookup"><span data-stu-id="5575f-123">FormXml\Main\\</span></span>  
  
 <span data-ttu-id="5575f-124">{guid 1}.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-124">{guid 1}.xml</span></span>  
<span data-ttu-id="5575f-125">{guid 1_managed}.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-125">{guid 1_managed}.xml</span></span>  
<span data-ttu-id="5575f-126">{guid n}.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-126">{guid n}.xml</span></span>  
<span data-ttu-id="5575f-127">{guid n_managed}.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-127">{guid n_managed}.xml</span></span>  
  
 <span data-ttu-id="5575f-128">FormXml\Mobile\\</span><span class="sxs-lookup"><span data-stu-id="5575f-128">FormXml\Mobile\\</span></span>  
  
 <span data-ttu-id="5575f-129">{guid 1}.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-129">{guid 1}.xml</span></span>  
<span data-ttu-id="5575f-130">{guid 1_managed}.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-130">{guid 1_managed}.xml</span></span>  
<span data-ttu-id="5575f-131">{guid n}.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-131">{guid n}.xml</span></span>  
<span data-ttu-id="5575f-132">{guid n_managed}.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-132">{guid n_managed}.xml</span></span>  
  
 <span data-ttu-id="5575f-133">SavedQueries\\</span><span class="sxs-lookup"><span data-stu-id="5575f-133">SavedQueries\\</span></span>  
  
 <span data-ttu-id="5575f-134">{guid 1}.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-134">{guid 1}.xml</span></span>  
<span data-ttu-id="5575f-135">{guid n}.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-135">{guid n}.xml</span></span>  
  
 <span data-ttu-id="5575f-136">Visualizations\\</span><span class="sxs-lookup"><span data-stu-id="5575f-136">Visualizations\\</span></span>  
  
 <span data-ttu-id="5575f-137">{guid 1}.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-137">{guid 1}.xml</span></span>  
<span data-ttu-id="5575f-138">{guid n}.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-138">{guid n}.xml</span></span>  
  
<a name="optionset_bm"></a>   
## <a name="option-set"></a><span data-ttu-id="5575f-139">Bộ tùy chọn</span><span class="sxs-lookup"><span data-stu-id="5575f-139">Option set</span></span>  
 <span data-ttu-id="5575f-140">Differs in managed solutions: No</span><span class="sxs-lookup"><span data-stu-id="5575f-140">Differs in managed solutions: No</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-141">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-141">Notes</span></span>  
 <span data-ttu-id="5575f-142">Each option set is stored in a distinct file.</span><span class="sxs-lookup"><span data-stu-id="5575f-142">Each option set is stored in a distinct file.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-143">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-143">Files</span></span>  
 <span data-ttu-id="5575f-144">\OptionSets\\</span><span class="sxs-lookup"><span data-stu-id="5575f-144">\OptionSets\\</span></span>  
  
 <span data-ttu-id="5575f-145">\<schema name 1>.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-145">\<schema name 1>.xml</span></span>  
<span data-ttu-id="5575f-146">\<schema name n>.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-146">\<schema name n>.xml</span></span>  
  
<a name="relationship_bm"></a>   
## <a name="entity-relationship"></a><span data-ttu-id="5575f-147">Entity relationship</span><span class="sxs-lookup"><span data-stu-id="5575f-147">Entity relationship</span></span>  
 <span data-ttu-id="5575f-148">Differs in managed solutions: Yes</span><span class="sxs-lookup"><span data-stu-id="5575f-148">Differs in managed solutions: Yes</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-149">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-149">Notes</span></span>  
  
1.  <span data-ttu-id="5575f-150">Each entity has a distinct file that contains all relationships where for:</span><span class="sxs-lookup"><span data-stu-id="5575f-150">Each entity has a distinct file that contains all relationships where for:</span></span>  
  
    1.  <span data-ttu-id="5575f-151">N:N it is the first listed entity</span><span class="sxs-lookup"><span data-stu-id="5575f-151">N:N it is the first listed entity</span></span>  
  
    2.  <span data-ttu-id="5575f-152">1:N it is the referenced entity</span><span class="sxs-lookup"><span data-stu-id="5575f-152">1:N it is the referenced entity</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-153">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-153">Files</span></span>  
 <span data-ttu-id="5575f-154">\Other\Relationships\\</span><span class="sxs-lookup"><span data-stu-id="5575f-154">\Other\Relationships\\</span></span>  
  
 <span data-ttu-id="5575f-155">\<Entity schema name 1>.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-155">\<Entity schema name 1>.xml</span></span>  
<span data-ttu-id="5575f-156">\<Entity schema name n>.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-156">\<Entity schema name n>.xml</span></span>  
  
<a name="ribbon_bm"></a>   
## <a name="ribbon-customization"></a><span data-ttu-id="5575f-157">Ribbon customization</span><span class="sxs-lookup"><span data-stu-id="5575f-157">Ribbon customization</span></span>  
 <span data-ttu-id="5575f-158">Differs in managed solutions: No</span><span class="sxs-lookup"><span data-stu-id="5575f-158">Differs in managed solutions: No</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-159">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-159">Notes</span></span>  
  
1.  <span data-ttu-id="5575f-160">All entity specific ribbon XML can be found in the respective folder for that entity.</span><span class="sxs-lookup"><span data-stu-id="5575f-160">All entity specific ribbon XML can be found in the respective folder for that entity.</span></span> <span data-ttu-id="5575f-161">All other ribbon XML will be in this file.</span><span class="sxs-lookup"><span data-stu-id="5575f-161">All other ribbon XML will be in this file.</span></span>  
  
2.  <span data-ttu-id="5575f-162">Direct editing of RibbonCustomizations.xml to customize the global ribbon is supported.</span><span class="sxs-lookup"><span data-stu-id="5575f-162">Direct editing of RibbonCustomizations.xml to customize the global ribbon is supported.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-163">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-163">Files</span></span>  
 <span data-ttu-id="5575f-164">\Other\RibbonCustomizations.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-164">\Other\RibbonCustomizations.xml</span></span>  
  
<a name="sitemap_bm"></a>   
## <a name="site-map"></a><span data-ttu-id="5575f-165">Sơ đồ trang web</span><span class="sxs-lookup"><span data-stu-id="5575f-165">Site map</span></span>  
 <span data-ttu-id="5575f-166">Differs in managed solutions: Yes</span><span class="sxs-lookup"><span data-stu-id="5575f-166">Differs in managed solutions: Yes</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-167">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-167">Notes</span></span>  
 <span data-ttu-id="5575f-168">Sitemap XML format is different for unmanaged & managed solutions.</span><span class="sxs-lookup"><span data-stu-id="5575f-168">Sitemap XML format is different for unmanaged & managed solutions.</span></span> <span data-ttu-id="5575f-169">Expect the file to be named as shown here.</span><span class="sxs-lookup"><span data-stu-id="5575f-169">Expect the file to be named as shown here.</span></span> <span data-ttu-id="5575f-170">When extracting both package types, both files are present.</span><span class="sxs-lookup"><span data-stu-id="5575f-170">When extracting both package types, both files are present.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-171">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-171">Files</span></span>  
 <span data-ttu-id="5575f-172">\Other\\</span><span class="sxs-lookup"><span data-stu-id="5575f-172">\Other\\</span></span>  
  
 <span data-ttu-id="5575f-173">SiteMap.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-173">SiteMap.xml</span></span>  
<span data-ttu-id="5575f-174">SiteMap_managed.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-174">SiteMap_managed.xml</span></span>  
  
<a name="resource_bm"></a>   
## <a name="web-resources"></a><span data-ttu-id="5575f-175">Các tài nguyên web</span><span class="sxs-lookup"><span data-stu-id="5575f-175">Web resources</span></span>  
 <span data-ttu-id="5575f-176">Differs in managed solutions: No</span><span class="sxs-lookup"><span data-stu-id="5575f-176">Differs in managed solutions: No</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-177">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-177">Notes</span></span>  
  
1.  <span data-ttu-id="5575f-178">The raw web resource is stored as a distinct file.</span><span class="sxs-lookup"><span data-stu-id="5575f-178">The raw web resource is stored as a distinct file.</span></span> <span data-ttu-id="5575f-179">The forward slash (/) characters are used to create folders.</span><span class="sxs-lookup"><span data-stu-id="5575f-179">The forward slash (/) characters are used to create folders.</span></span>  
  
2.  <span data-ttu-id="5575f-180">The web resource metadata is stored with a similar file name ending in .data.xml.</span><span class="sxs-lookup"><span data-stu-id="5575f-180">The web resource metadata is stored with a similar file name ending in .data.xml.</span></span>  
  
3.  <span data-ttu-id="5575f-181">It is recommended that the name of a web resource contain the natural file name extension.</span><span class="sxs-lookup"><span data-stu-id="5575f-181">It is recommended that the name of a web resource contain the natural file name extension.</span></span>  
  
4.  <span data-ttu-id="5575f-182">Adding the raw files to source control may cause duplication.</span><span class="sxs-lookup"><span data-stu-id="5575f-182">Adding the raw files to source control may cause duplication.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-183">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-183">Files</span></span>  
 <span data-ttu-id="5575f-184">\WebResources\\</span><span class="sxs-lookup"><span data-stu-id="5575f-184">\WebResources\\</span></span>  
  
 <span data-ttu-id="5575f-185">\<name 1></span><span class="sxs-lookup"><span data-stu-id="5575f-185">\<name 1></span></span>  
<span data-ttu-id="5575f-186">\<name 1>.data.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-186">\<name 1>.data.xml</span></span>  
<span data-ttu-id="5575f-187">\<name n></span><span class="sxs-lookup"><span data-stu-id="5575f-187">\<name n></span></span>  
<span data-ttu-id="5575f-188">\<name n>.data.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-188">\<name n>.data.xml</span></span>  
  
<a name="role_bm"></a>   
## <a name="role"></a><span data-ttu-id="5575f-189">Vai trò</span><span class="sxs-lookup"><span data-stu-id="5575f-189">Role</span></span>  
 <span data-ttu-id="5575f-190">Differs in managed solutions: No</span><span class="sxs-lookup"><span data-stu-id="5575f-190">Differs in managed solutions: No</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-191">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-191">Notes</span></span>  
 <span data-ttu-id="5575f-192">Each role is stored in a distinct file.</span><span class="sxs-lookup"><span data-stu-id="5575f-192">Each role is stored in a distinct file.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-193">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-193">Files</span></span>  
 <span data-ttu-id="5575f-194">\Roles\\</span><span class="sxs-lookup"><span data-stu-id="5575f-194">\Roles\\</span></span>  
  
 <span data-ttu-id="5575f-195">\<schema name>.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-195">\<schema name>.xml</span></span>  
  
<a name="connectionrole_bm"></a>   
## <a name="connection-role"></a><span data-ttu-id="5575f-196">Connection role</span><span class="sxs-lookup"><span data-stu-id="5575f-196">Connection role</span></span>  
 <span data-ttu-id="5575f-197">Differs in managed solutions: No</span><span class="sxs-lookup"><span data-stu-id="5575f-197">Differs in managed solutions: No</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-198">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-198">Notes</span></span>  
 <span data-ttu-id="5575f-199">All Connection Roles are stored jointly in one file.</span><span class="sxs-lookup"><span data-stu-id="5575f-199">All Connection Roles are stored jointly in one file.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-200">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-200">Files</span></span>  
 <span data-ttu-id="5575f-201">\Other\ConnectionRoles.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-201">\Other\ConnectionRoles.xml</span></span>  
  
<a name="dashboard_bm"></a>   
## <a name="dashboard"></a><span data-ttu-id="5575f-202">Bảng thông tin</span><span class="sxs-lookup"><span data-stu-id="5575f-202">Dashboard</span></span>  
 <span data-ttu-id="5575f-203">Differs in managed solutions: No</span><span class="sxs-lookup"><span data-stu-id="5575f-203">Differs in managed solutions: No</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-204">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-204">Notes</span></span>  
 <span data-ttu-id="5575f-205">Each dashboard is stored in a distinct file.</span><span class="sxs-lookup"><span data-stu-id="5575f-205">Each dashboard is stored in a distinct file.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-206">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-206">Files</span></span>  
 <span data-ttu-id="5575f-207">\Dashboards\\</span><span class="sxs-lookup"><span data-stu-id="5575f-207">\Dashboards\\</span></span>  
  
 <span data-ttu-id="5575f-208">{guid 1}.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-208">{guid 1}.xml</span></span>  
<span data-ttu-id="5575f-209">{guid n}.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-209">{guid n}.xml</span></span>  
  
<a name="workflow_bm"></a>   
## <a name="workflow"></a><span data-ttu-id="5575f-210">Quy trình</span><span class="sxs-lookup"><span data-stu-id="5575f-210">Workflow</span></span>  
 <span data-ttu-id="5575f-211">Differs in managed solutions: No</span><span class="sxs-lookup"><span data-stu-id="5575f-211">Differs in managed solutions: No</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-212">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-212">Notes</span></span>  
  
1.  <span data-ttu-id="5575f-213">The XAML for each workflow is stored in a distinct file.</span><span class="sxs-lookup"><span data-stu-id="5575f-213">The XAML for each workflow is stored in a distinct file.</span></span>  
  
2.  <span data-ttu-id="5575f-214">Metadata for each workflow resides in a similarly named file ending in .data.xml.</span><span class="sxs-lookup"><span data-stu-id="5575f-214">Metadata for each workflow resides in a similarly named file ending in .data.xml.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-215">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-215">Files</span></span>  
 <span data-ttu-id="5575f-216">\Workflows\\</span><span class="sxs-lookup"><span data-stu-id="5575f-216">\Workflows\\</span></span>  
  
 <span data-ttu-id="5575f-217">\<XamlFileName 1>.xaml</span><span class="sxs-lookup"><span data-stu-id="5575f-217">\<XamlFileName 1>.xaml</span></span>  
<span data-ttu-id="5575f-218">\<XamlFileName 1>.xaml.data.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-218">\<XamlFileName 1>.xaml.data.xml</span></span>  
<span data-ttu-id="5575f-219">\<XamlFileName n>.xaml</span><span class="sxs-lookup"><span data-stu-id="5575f-219">\<XamlFileName n>.xaml</span></span>  
<span data-ttu-id="5575f-220">\<XamlFileName n>.xaml.data.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-220">\<XamlFileName n>.xaml.data.xml</span></span>  
  
<a name="emailtemplate_bm"></a>   
## <a name="email-template"></a><span data-ttu-id="5575f-221">Email template</span><span class="sxs-lookup"><span data-stu-id="5575f-221">Email template</span></span>  
 <span data-ttu-id="5575f-222">Differs in managed solutions: No</span><span class="sxs-lookup"><span data-stu-id="5575f-222">Differs in managed solutions: No</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-223">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-223">Notes</span></span>  
  
1.  <span data-ttu-id="5575f-224">All email template metadata is stored in a single file.</span><span class="sxs-lookup"><span data-stu-id="5575f-224">All email template metadata is stored in a single file.</span></span>  
  
2.  <span data-ttu-id="5575f-225">Each email template uses four distinct files per language.</span><span class="sxs-lookup"><span data-stu-id="5575f-225">Each email template uses four distinct files per language.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-226">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-226">Files</span></span>  
 <span data-ttu-id="5575f-227">\Templates\\</span><span class="sxs-lookup"><span data-stu-id="5575f-227">\Templates\\</span></span>  
  
 <span data-ttu-id="5575f-228">EmailTemplates.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-228">EmailTemplates.xml</span></span>  
  
 <span data-ttu-id="5575f-229">EmailDocuments\\</span><span class="sxs-lookup"><span data-stu-id="5575f-229">EmailDocuments\\</span></span>  
  
 <span data-ttu-id="5575f-230">\<LCID 1>\\{guid 1}\\</span><span class="sxs-lookup"><span data-stu-id="5575f-230">\<LCID 1>\\{guid 1}\\</span></span>  
  
 <span data-ttu-id="5575f-231">Body.xsl</span><span class="sxs-lookup"><span data-stu-id="5575f-231">Body.xsl</span></span>  
<span data-ttu-id="5575f-232">Presentation.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-232">Presentation.xml</span></span>  
<span data-ttu-id="5575f-233">Subject.xsl</span><span class="sxs-lookup"><span data-stu-id="5575f-233">Subject.xsl</span></span>  
<span data-ttu-id="5575f-234">Subjectpresentation.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-234">Subjectpresentation.xml</span></span>  
  
 <span data-ttu-id="5575f-235">\<LCID 1>\\{guid n}\\</span><span class="sxs-lookup"><span data-stu-id="5575f-235">\<LCID 1>\\{guid n}\\</span></span>  
  
 <span data-ttu-id="5575f-236">Body.xsl</span><span class="sxs-lookup"><span data-stu-id="5575f-236">Body.xsl</span></span>  
<span data-ttu-id="5575f-237">Presentation.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-237">Presentation.xml</span></span>  
<span data-ttu-id="5575f-238">Subject.xsl</span><span class="sxs-lookup"><span data-stu-id="5575f-238">Subject.xsl</span></span>  
<span data-ttu-id="5575f-239">Subjectpresentation.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-239">Subjectpresentation.xml</span></span>  
  
 <span data-ttu-id="5575f-240">\<LCID n>\\{guid 1}\\</span><span class="sxs-lookup"><span data-stu-id="5575f-240">\<LCID n>\\{guid 1}\\</span></span>  
  
 <span data-ttu-id="5575f-241">Body.xsl</span><span class="sxs-lookup"><span data-stu-id="5575f-241">Body.xsl</span></span>  
<span data-ttu-id="5575f-242">Presentation.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-242">Presentation.xml</span></span>  
<span data-ttu-id="5575f-243">Subject.xsl</span><span class="sxs-lookup"><span data-stu-id="5575f-243">Subject.xsl</span></span>  
<span data-ttu-id="5575f-244">Subjectpresentation.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-244">Subjectpresentation.xml</span></span>  
  
 <span data-ttu-id="5575f-245">\<LCID n>\\{guid n}\\</span><span class="sxs-lookup"><span data-stu-id="5575f-245">\<LCID n>\\{guid n}\\</span></span>  
  
 <span data-ttu-id="5575f-246">Body.xsl</span><span class="sxs-lookup"><span data-stu-id="5575f-246">Body.xsl</span></span>  
<span data-ttu-id="5575f-247">Presentation.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-247">Presentation.xml</span></span>  
<span data-ttu-id="5575f-248">Subject.xsl</span><span class="sxs-lookup"><span data-stu-id="5575f-248">Subject.xsl</span></span>  
<span data-ttu-id="5575f-249">Subjectpresentation.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-249">Subjectpresentation.xml</span></span>  
  
<a name="contracttemplate_bm"></a>   
## <a name="contract-template"></a><span data-ttu-id="5575f-250">Contract template</span><span class="sxs-lookup"><span data-stu-id="5575f-250">Contract template</span></span>  
 <span data-ttu-id="5575f-251">Differs in managed solutions: No</span><span class="sxs-lookup"><span data-stu-id="5575f-251">Differs in managed solutions: No</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-252">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-252">Notes</span></span>  
 <span data-ttu-id="5575f-253">All Contract template metadata is stored in a single file.</span><span class="sxs-lookup"><span data-stu-id="5575f-253">All Contract template metadata is stored in a single file.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-254">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-254">Files</span></span>  
 <span data-ttu-id="5575f-255">\Templates\ContractTemplates.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-255">\Templates\ContractTemplates.xml</span></span>  
  
<a name="kbarticle_bm"></a>   
## <a name="kb-article-template"></a><span data-ttu-id="5575f-256">Kb article template</span><span class="sxs-lookup"><span data-stu-id="5575f-256">Kb article template</span></span>  
 <span data-ttu-id="5575f-257">Differs in managed solutions: No</span><span class="sxs-lookup"><span data-stu-id="5575f-257">Differs in managed solutions: No</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-258">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-258">Notes</span></span>  
  
1.  <span data-ttu-id="5575f-259">All contract template metadata is stored in a single file.</span><span class="sxs-lookup"><span data-stu-id="5575f-259">All contract template metadata is stored in a single file.</span></span>  
  
2.  <span data-ttu-id="5575f-260">Each contract template uses two distinct files per language.</span><span class="sxs-lookup"><span data-stu-id="5575f-260">Each contract template uses two distinct files per language.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-261">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-261">Files</span></span>  
 <span data-ttu-id="5575f-262">\Templates\\</span><span class="sxs-lookup"><span data-stu-id="5575f-262">\Templates\\</span></span>  
  
 <span data-ttu-id="5575f-263">KBArticleTemplates.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-263">KBArticleTemplates.xml</span></span>  
  
 <span data-ttu-id="5575f-264">KBArticleTemplates\\</span><span class="sxs-lookup"><span data-stu-id="5575f-264">KBArticleTemplates\\</span></span>  
  
 <span data-ttu-id="5575f-265">\<LCID 1>\\{guid 1}\\</span><span class="sxs-lookup"><span data-stu-id="5575f-265">\<LCID 1>\\{guid 1}\\</span></span>  
  
 <span data-ttu-id="5575f-266">formatxml.xsl</span><span class="sxs-lookup"><span data-stu-id="5575f-266">formatxml.xsl</span></span>  
<span data-ttu-id="5575f-267">Structurexml.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-267">Structurexml.xml</span></span>  
  
 <span data-ttu-id="5575f-268">\<LCID 1>\\{guid n}\\</span><span class="sxs-lookup"><span data-stu-id="5575f-268">\<LCID 1>\\{guid n}\\</span></span>  
  
 <span data-ttu-id="5575f-269">formatxml.xsl</span><span class="sxs-lookup"><span data-stu-id="5575f-269">formatxml.xsl</span></span>  
<span data-ttu-id="5575f-270">Structurexml.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-270">Structurexml.xml</span></span>  
  
 <span data-ttu-id="5575f-271">\<LCID n>\\{guid 1}\\</span><span class="sxs-lookup"><span data-stu-id="5575f-271">\<LCID n>\\{guid 1}\\</span></span>  
  
 <span data-ttu-id="5575f-272">formatxml.xsl</span><span class="sxs-lookup"><span data-stu-id="5575f-272">formatxml.xsl</span></span>  
<span data-ttu-id="5575f-273">Structurexml.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-273">Structurexml.xml</span></span>  
  
 <span data-ttu-id="5575f-274">\<LCID n>\\{guid n}\\</span><span class="sxs-lookup"><span data-stu-id="5575f-274">\<LCID n>\\{guid n}\\</span></span>  
  
 <span data-ttu-id="5575f-275">formatxml.xsl</span><span class="sxs-lookup"><span data-stu-id="5575f-275">formatxml.xsl</span></span>  
<span data-ttu-id="5575f-276">Structurexml.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-276">Structurexml.xml</span></span>  
  
<a name="mailmerge_bm"></a>   
## <a name="mail-merge-template"></a><span data-ttu-id="5575f-277">Mail merge template</span><span class="sxs-lookup"><span data-stu-id="5575f-277">Mail merge template</span></span>  
 <span data-ttu-id="5575f-278">Differs in managed solutions: No</span><span class="sxs-lookup"><span data-stu-id="5575f-278">Differs in managed solutions: No</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-279">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-279">Notes</span></span>  
  
1.  <span data-ttu-id="5575f-280">All mail merge template metadata is stored in a single file.</span><span class="sxs-lookup"><span data-stu-id="5575f-280">All mail merge template metadata is stored in a single file.</span></span>  
  
2.  <span data-ttu-id="5575f-281">Each mail merge template uses two distinct files per language.</span><span class="sxs-lookup"><span data-stu-id="5575f-281">Each mail merge template uses two distinct files per language.</span></span>  
  
3.  <span data-ttu-id="5575f-282">Documents that are shared across multiple templates will be stored in a single distinct file.</span><span class="sxs-lookup"><span data-stu-id="5575f-282">Documents that are shared across multiple templates will be stored in a single distinct file.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-283">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-283">Files</span></span>  
 <span data-ttu-id="5575f-284">\Templates\\</span><span class="sxs-lookup"><span data-stu-id="5575f-284">\Templates\\</span></span>  
  
 <span data-ttu-id="5575f-285">MailMergeTemplates.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-285">MailMergeTemplates.xml</span></span>  
  
 <span data-ttu-id="5575f-286">MailMergeDocuments\\</span><span class="sxs-lookup"><span data-stu-id="5575f-286">MailMergeDocuments\\</span></span>  
  
 <span data-ttu-id="5575f-287">\<LCID 1>\\{guid 1}\\<document name 1>.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-287">\<LCID 1>\\{guid 1}\\<document name 1>.xml</span></span>  
<span data-ttu-id="5575f-288">\<LCID 1>\\{guid n}\\<document name n\>.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-288">\<LCID 1>\\{guid n}\\<document name n\>.xml</span></span>  
<span data-ttu-id="5575f-289">\<LCID n>\\{guid 1}\\<document name 1>.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-289">\<LCID n>\\{guid 1}\\<document name 1>.xml</span></span>  
<span data-ttu-id="5575f-290">\<LCID n>\\{guid n}\\<document name n\>.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-290">\<LCID n>\\{guid n}\\<document name n\>.xml</span></span>  
  
<a name="pluginassembly_bm"></a>   
## <a name="pluginassembly"></a><span data-ttu-id="5575f-291">PluginAssembly</span><span class="sxs-lookup"><span data-stu-id="5575f-291">PluginAssembly</span></span>  
 <span data-ttu-id="5575f-292">Differs in managed solutions: No</span><span class="sxs-lookup"><span data-stu-id="5575f-292">Differs in managed solutions: No</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-293">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-293">Notes</span></span>  
  
1.  <span data-ttu-id="5575f-294">Each plug-in assembly will have a distinct file for the raw assembly bytes.</span><span class="sxs-lookup"><span data-stu-id="5575f-294">Each plug-in assembly will have a distinct file for the raw assembly bytes.</span></span>  
  
2.  <span data-ttu-id="5575f-295">Plug-in assembly metadata is stored in a similar named file ending in .data.xml.</span><span class="sxs-lookup"><span data-stu-id="5575f-295">Plug-in assembly metadata is stored in a similar named file ending in .data.xml.</span></span>  
  
3.  <span data-ttu-id="5575f-296">Including the raw assembly in source control is not recommended.</span><span class="sxs-lookup"><span data-stu-id="5575f-296">Including the raw assembly in source control is not recommended.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-297">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-297">Files</span></span>  
 <span data-ttu-id="5575f-298">\PluginAssemblies\\</span><span class="sxs-lookup"><span data-stu-id="5575f-298">\PluginAssemblies\\</span></span>  
  
 <span data-ttu-id="5575f-299">\<Assembly Name 1>-{guid 1}\\</span><span class="sxs-lookup"><span data-stu-id="5575f-299">\<Assembly Name 1>-{guid 1}\\</span></span>  
  
 <span data-ttu-id="5575f-300">\<Assembly Name 1>.dll</span><span class="sxs-lookup"><span data-stu-id="5575f-300">\<Assembly Name 1>.dll</span></span>  
<span data-ttu-id="5575f-301">\<Assembly Name 1>.dll.data.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-301">\<Assembly Name 1>.dll.data.xml</span></span>  
  
 <span data-ttu-id="5575f-302">\<Assembly Name n>-{guid n}\\</span><span class="sxs-lookup"><span data-stu-id="5575f-302">\<Assembly Name n>-{guid n}\\</span></span>  
  
 <span data-ttu-id="5575f-303">\<Assembly Name n>.dll</span><span class="sxs-lookup"><span data-stu-id="5575f-303">\<Assembly Name n>.dll</span></span>  
<span data-ttu-id="5575f-304">\<Assembly Name n>.dll.data.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-304">\<Assembly Name n>.dll.data.xml</span></span>  
  
<a name="step_bm"></a>   
## <a name="sdkmessageprocessingstep"></a><span data-ttu-id="5575f-305">SdkMessageProcessingStep</span><span class="sxs-lookup"><span data-stu-id="5575f-305">SdkMessageProcessingStep</span></span>  
 <span data-ttu-id="5575f-306">Differs in managed solutions: No</span><span class="sxs-lookup"><span data-stu-id="5575f-306">Differs in managed solutions: No</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-307">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-307">Notes</span></span>  
 <span data-ttu-id="5575f-308">Each SDK message processing step is stored in a distinct file.</span><span class="sxs-lookup"><span data-stu-id="5575f-308">Each SDK message processing step is stored in a distinct file.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-309">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-309">Files</span></span>  
 <span data-ttu-id="5575f-310">\SdkMessageProcessingSteps\\</span><span class="sxs-lookup"><span data-stu-id="5575f-310">\SdkMessageProcessingSteps\\</span></span>  
  
 <span data-ttu-id="5575f-311">{guid 1}.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-311">{guid 1}.xml</span></span>  
<span data-ttu-id="5575f-312">{guid n}.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-312">{guid n}.xml</span></span>  
  
<a name="serviceendpoint_bm"></a>   
## <a name="serviceendpoint"></a><span data-ttu-id="5575f-313">ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5575f-313">ServiceEndpoint</span></span>  
 <span data-ttu-id="5575f-314">Differs in managed solutions: No</span><span class="sxs-lookup"><span data-stu-id="5575f-314">Differs in managed solutions: No</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-315">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-315">Notes</span></span>  
 <span data-ttu-id="5575f-316">All service end point metadata is jointly stored in one file.</span><span class="sxs-lookup"><span data-stu-id="5575f-316">All service end point metadata is jointly stored in one file.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-317">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-317">Files</span></span>  
 <span data-ttu-id="5575f-318">\PluginAssemblies\ServiceEndpoints.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-318">\PluginAssemblies\ServiceEndpoints.xml</span></span>  
  
<a name="reports_bm"></a>   
## <a name="reports"></a><span data-ttu-id="5575f-319">Báo cáo</span><span class="sxs-lookup"><span data-stu-id="5575f-319">Reports</span></span>  
 <span data-ttu-id="5575f-320">Differs in managed solutions: No</span><span class="sxs-lookup"><span data-stu-id="5575f-320">Differs in managed solutions: No</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-321">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-321">Notes</span></span>  
  
1.  <span data-ttu-id="5575f-322">Reports are stored in a distinct sub-folder per language.</span><span class="sxs-lookup"><span data-stu-id="5575f-322">Reports are stored in a distinct sub-folder per language.</span></span>  
  
2.  <span data-ttu-id="5575f-323">Each report has a distinct file within that folder.</span><span class="sxs-lookup"><span data-stu-id="5575f-323">Each report has a distinct file within that folder.</span></span>  
  
3.  <span data-ttu-id="5575f-324">Metadata for each report is stored within a similar named file ending in .data.xml.</span><span class="sxs-lookup"><span data-stu-id="5575f-324">Metadata for each report is stored within a similar named file ending in .data.xml.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-325">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-325">Files</span></span>  
 <span data-ttu-id="5575f-326">\Reports\\</span><span class="sxs-lookup"><span data-stu-id="5575f-326">\Reports\\</span></span>  
  
 <span data-ttu-id="5575f-327">ReportSignatureIdMappings.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-327">ReportSignatureIdMappings.xml</span></span>  
  
 <span data-ttu-id="5575f-328">ReportLinks.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-328">ReportLinks.xml</span></span>  
  
 <span data-ttu-id="5575f-329">\<LCID 1>\\{guid 1}\\</span><span class="sxs-lookup"><span data-stu-id="5575f-329">\<LCID 1>\\{guid 1}\\</span></span>  
  
 <span data-ttu-id="5575f-330">\<Report Name 1>.rdl</span><span class="sxs-lookup"><span data-stu-id="5575f-330">\<Report Name 1>.rdl</span></span>  
<span data-ttu-id="5575f-331">\<Report Name 1>.rdl.data.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-331">\<Report Name 1>.rdl.data.xml</span></span>  
  
 <span data-ttu-id="5575f-332">\<LCID 1>\\{guid n}\\</span><span class="sxs-lookup"><span data-stu-id="5575f-332">\<LCID 1>\\{guid n}\\</span></span>  
  
 <span data-ttu-id="5575f-333">\<Report Name n>.rdl</span><span class="sxs-lookup"><span data-stu-id="5575f-333">\<Report Name n>.rdl</span></span>  
<span data-ttu-id="5575f-334">\<Report Name n>.rdl.data.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-334">\<Report Name n>.rdl.data.xml</span></span>  
  
 <span data-ttu-id="5575f-335">\<LCID n>\\{guid 1}\\</span><span class="sxs-lookup"><span data-stu-id="5575f-335">\<LCID n>\\{guid 1}\\</span></span>  
  
 <span data-ttu-id="5575f-336">\<Report Name 1>.rdl</span><span class="sxs-lookup"><span data-stu-id="5575f-336">\<Report Name 1>.rdl</span></span>  
<span data-ttu-id="5575f-337">\<Report Name 1>.rdl.data.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-337">\<Report Name 1>.rdl.data.xml</span></span>  
  
 <span data-ttu-id="5575f-338">\<LCID n>\\{guid n}\\</span><span class="sxs-lookup"><span data-stu-id="5575f-338">\<LCID n>\\{guid n}\\</span></span>  
  
 <span data-ttu-id="5575f-339">\<Report Name n>.rdl</span><span class="sxs-lookup"><span data-stu-id="5575f-339">\<Report Name n>.rdl</span></span>  
<span data-ttu-id="5575f-340">\<Report Name n>.rdl.data.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-340">\<Report Name n>.rdl.data.xml</span></span>  
  
<a name="entitymap_bm"></a>   
## <a name="entitymap"></a><span data-ttu-id="5575f-341">EntityMap</span><span class="sxs-lookup"><span data-stu-id="5575f-341">EntityMap</span></span>  
 <span data-ttu-id="5575f-342">Differs in managed solutions: No</span><span class="sxs-lookup"><span data-stu-id="5575f-342">Differs in managed solutions: No</span></span>  
  
### <a name="notes"></a><span data-ttu-id="5575f-343">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="5575f-343">Notes</span></span>  
 <span data-ttu-id="5575f-344">All entity maps are stored in a single file.</span><span class="sxs-lookup"><span data-stu-id="5575f-344">All entity maps are stored in a single file.</span></span>  
  
### <a name="files"></a><span data-ttu-id="5575f-345">Files</span><span class="sxs-lookup"><span data-stu-id="5575f-345">Files</span></span>  
 <span data-ttu-id="5575f-346">\Other\EntityMaps.xml</span><span class="sxs-lookup"><span data-stu-id="5575f-346">\Other\EntityMaps.xml</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="5575f-347">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="5575f-347">See also</span></span>  
 <span data-ttu-id="5575f-348">[Solution Tools for Team Development](solution-tools-team-development.md) </span><span class="sxs-lookup"><span data-stu-id="5575f-348">[Solution Tools for Team Development](solution-tools-team-development.md) </span></span>  
 <span data-ttu-id="5575f-349">[Use the SolutionPackager Tool to Compress and Extract a Solution File](compress-extract-solution-file-solutionpackager.md) </span><span class="sxs-lookup"><span data-stu-id="5575f-349">[Use the SolutionPackager Tool to Compress and Extract a Solution File](compress-extract-solution-file-solutionpackager.md) </span></span>  
 [<span data-ttu-id="5575f-350">Programming Reference for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="5575f-350">Programming Reference for Dynamics 365 for Customer Engagement apps</span></span>](programming-reference.md)
