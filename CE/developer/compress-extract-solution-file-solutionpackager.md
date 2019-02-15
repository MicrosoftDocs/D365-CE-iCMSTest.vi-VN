---
title: Use the SolutionPackager tool to compress and extract a solution file (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: SolutionPackager is a tool that can reversibly decompose a Dynamics 365 for Customer Engagement apps compressed solution file into multiple XML files and other files so that these files can be easily managed by a source control system
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: dd682a4b-d04b-40c2-b680-9dec34b986f0
caps.latest.revision: 33
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 178f6a81210ea960f03a1950706690d381e30bfd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386792"
---
# <a name="use-the-solutionpackager-tool-to-compress-and-extract-a-solution-file"></a><span data-ttu-id="a9815-103">Use the SolutionPackager tool to compress and extract a solution file</span><span class="sxs-lookup"><span data-stu-id="a9815-103">Use the SolutionPackager tool to compress and extract a solution file</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a9815-104">SolutionPackager is a tool that can reversibly decompose a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps compressed solution file into multiple XML files and other files so that these files can be easily managed by a source control system.</span><span class="sxs-lookup"><span data-stu-id="a9815-104">SolutionPackager is a tool that can reversibly decompose a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps compressed solution file into multiple XML files and other files so that these files can be easily managed by a source control system.</span></span> <span data-ttu-id="a9815-105">The following sections show you how to run the tool and how to use the tool with managed and unmanaged solutions.</span><span class="sxs-lookup"><span data-stu-id="a9815-105">The following sections show you how to run the tool and how to use the tool with managed and unmanaged solutions.</span></span>  
  
<a name="bkm_where"></a>   
## <a name="where-to-find-the-solutionpackager-tool"></a><span data-ttu-id="a9815-106">Where to find the SolutionPackager tool</span><span class="sxs-lookup"><span data-stu-id="a9815-106">Where to find the SolutionPackager tool</span></span>  
 <span data-ttu-id="a9815-107">The SolutionPackager tool is distributed as part of the [Microsoft.CrmSdk.CoreTools](https://www.nuget.org/packages/Microsoft.CrmSdk.CoreTools) NuGet package.</span><span class="sxs-lookup"><span data-stu-id="a9815-107">The SolutionPackager tool is distributed as part of the [Microsoft.CrmSdk.CoreTools](https://www.nuget.org/packages/Microsoft.CrmSdk.CoreTools) NuGet package.</span></span> <span data-ttu-id="a9815-108">See [Download tools from NuGet](download-tools-nuget.md) for information about how to download it.</span><span class="sxs-lookup"><span data-stu-id="a9815-108">See [Download tools from NuGet](download-tools-nuget.md) for information about how to download it.</span></span>
  
  
<a name="arguments"></a>   
## <a name="solutionpackager-command-line-arguments"></a><span data-ttu-id="a9815-109">SolutionPackager command-line arguments</span><span class="sxs-lookup"><span data-stu-id="a9815-109">SolutionPackager command-line arguments</span></span>  
 <span data-ttu-id="a9815-110">SolutionPackager is a command-line tool that can be invoked with the parameters identified in the following table.</span><span class="sxs-lookup"><span data-stu-id="a9815-110">SolutionPackager is a command-line tool that can be invoked with the parameters identified in the following table.</span></span>  
  
|<span data-ttu-id="a9815-111">Đối số</span><span class="sxs-lookup"><span data-stu-id="a9815-111">Argument</span></span>|<span data-ttu-id="a9815-112">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a9815-112">Description</span></span>|  
|--------------|-----------------|  
|<span data-ttu-id="a9815-113">/action: {Extract&#124;Pack}</span><span class="sxs-lookup"><span data-stu-id="a9815-113">/action: {Extract&#124;Pack}</span></span>|<span data-ttu-id="a9815-114">Yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="a9815-114">Required.</span></span> <span data-ttu-id="a9815-115">The action to perform.</span><span class="sxs-lookup"><span data-stu-id="a9815-115">The action to perform.</span></span> <span data-ttu-id="a9815-116">The action can be either to extract a solution .zip file to a folder, or to pack a folder into a .zip file.</span><span class="sxs-lookup"><span data-stu-id="a9815-116">The action can be either to extract a solution .zip file to a folder, or to pack a folder into a .zip file.</span></span>|  
|<span data-ttu-id="a9815-117">/zipfile: \<file path></span><span class="sxs-lookup"><span data-stu-id="a9815-117">/zipfile: \<file path></span></span>|<span data-ttu-id="a9815-118">Yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="a9815-118">Required.</span></span> <span data-ttu-id="a9815-119">The path and name of a solution .zip file.</span><span class="sxs-lookup"><span data-stu-id="a9815-119">The path and name of a solution .zip file.</span></span> <span data-ttu-id="a9815-120">When extracting, the file must exist and will be read from.</span><span class="sxs-lookup"><span data-stu-id="a9815-120">When extracting, the file must exist and will be read from.</span></span> <span data-ttu-id="a9815-121">When packing, the file is replaced.</span><span class="sxs-lookup"><span data-stu-id="a9815-121">When packing, the file is replaced.</span></span>|  
|<span data-ttu-id="a9815-122">/folder: \<folder path></span><span class="sxs-lookup"><span data-stu-id="a9815-122">/folder: \<folder path></span></span>|<span data-ttu-id="a9815-123">Yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="a9815-123">Required.</span></span> <span data-ttu-id="a9815-124">The path to a folder.</span><span class="sxs-lookup"><span data-stu-id="a9815-124">The path to a folder.</span></span> <span data-ttu-id="a9815-125">When extracting, this folder is created and populated with component files.</span><span class="sxs-lookup"><span data-stu-id="a9815-125">When extracting, this folder is created and populated with component files.</span></span> <span data-ttu-id="a9815-126">When packing, this folder must already exist and contain previously extracted component files.</span><span class="sxs-lookup"><span data-stu-id="a9815-126">When packing, this folder must already exist and contain previously extracted component files.</span></span>|  
|<span data-ttu-id="a9815-127">/packagetype: {Unmanaged&#124;Managed&#124;Both}</span><span class="sxs-lookup"><span data-stu-id="a9815-127">/packagetype: {Unmanaged&#124;Managed&#124;Both}</span></span>|<span data-ttu-id="a9815-128">Tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="a9815-128">Optional.</span></span> <span data-ttu-id="a9815-129">The type of package to process.</span><span class="sxs-lookup"><span data-stu-id="a9815-129">The type of package to process.</span></span> <span data-ttu-id="a9815-130">The default value is Unmanaged.</span><span class="sxs-lookup"><span data-stu-id="a9815-130">The default value is Unmanaged.</span></span> <span data-ttu-id="a9815-131">This argument may be omitted in most occasions because the package type can be read from inside the .zip file or component files.</span><span class="sxs-lookup"><span data-stu-id="a9815-131">This argument may be omitted in most occasions because the package type can be read from inside the .zip file or component files.</span></span> <span data-ttu-id="a9815-132">When extracting and Both is specified, managed and unmanaged solution .zip files must be present and are processed into a single folder.</span><span class="sxs-lookup"><span data-stu-id="a9815-132">When extracting and Both is specified, managed and unmanaged solution .zip files must be present and are processed into a single folder.</span></span> <span data-ttu-id="a9815-133">When packing and Both is specified, managed and unmanaged solution .zip files will be produced from one folder.</span><span class="sxs-lookup"><span data-stu-id="a9815-133">When packing and Both is specified, managed and unmanaged solution .zip files will be produced from one folder.</span></span> <span data-ttu-id="a9815-134">For more information, see the section on working with managed and unmanaged solutions later in this topic.</span><span class="sxs-lookup"><span data-stu-id="a9815-134">For more information, see the section on working with managed and unmanaged solutions later in this topic.</span></span>|  
|<span data-ttu-id="a9815-135">/allowWrite:{Yes&#124;No}</span><span class="sxs-lookup"><span data-stu-id="a9815-135">/allowWrite:{Yes&#124;No}</span></span>|<span data-ttu-id="a9815-136">Tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="a9815-136">Optional.</span></span> <span data-ttu-id="a9815-137">Giá trị mặc định là Có.</span><span class="sxs-lookup"><span data-stu-id="a9815-137">The default value is Yes.</span></span> <span data-ttu-id="a9815-138">This argument is used only during an extraction.</span><span class="sxs-lookup"><span data-stu-id="a9815-138">This argument is used only during an extraction.</span></span> <span data-ttu-id="a9815-139">When /allowWrite:No is specified, the tool performs all operations but is prevented from writing or deleting any files.</span><span class="sxs-lookup"><span data-stu-id="a9815-139">When /allowWrite:No is specified, the tool performs all operations but is prevented from writing or deleting any files.</span></span> <span data-ttu-id="a9815-140">The extract operation can be safely assessed without overwriting or deleting any existing files.</span><span class="sxs-lookup"><span data-stu-id="a9815-140">The extract operation can be safely assessed without overwriting or deleting any existing files.</span></span>|  
|<span data-ttu-id="a9815-141">/allowDelete:{Yes&#124;No&#124;Prompt}</span><span class="sxs-lookup"><span data-stu-id="a9815-141">/allowDelete:{Yes&#124;No&#124;Prompt}</span></span>|<span data-ttu-id="a9815-142">Tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="a9815-142">Optional.</span></span> <span data-ttu-id="a9815-143">The default value is Prompt.</span><span class="sxs-lookup"><span data-stu-id="a9815-143">The default value is Prompt.</span></span> <span data-ttu-id="a9815-144">This argument is used only during an extraction.</span><span class="sxs-lookup"><span data-stu-id="a9815-144">This argument is used only during an extraction.</span></span> <span data-ttu-id="a9815-145">When /allowDelete:Yes is specified, any files present in the folder specified by the /folder parameter that are not expected are automatically deleted.</span><span class="sxs-lookup"><span data-stu-id="a9815-145">When /allowDelete:Yes is specified, any files present in the folder specified by the /folder parameter that are not expected are automatically deleted.</span></span> <span data-ttu-id="a9815-146">When /allowDelete:No is specified, no deletes will occur.</span><span class="sxs-lookup"><span data-stu-id="a9815-146">When /allowDelete:No is specified, no deletes will occur.</span></span> <span data-ttu-id="a9815-147">When /allowDelete:Prompt is specified, the user is prompted through the console to allow or deny all delete operations.</span><span class="sxs-lookup"><span data-stu-id="a9815-147">When /allowDelete:Prompt is specified, the user is prompted through the console to allow or deny all delete operations.</span></span> <span data-ttu-id="a9815-148">Note that if /allowWrite:No is specified, no deletes will occur even if /allowDelete:Yes is also specified.</span><span class="sxs-lookup"><span data-stu-id="a9815-148">Note that if /allowWrite:No is specified, no deletes will occur even if /allowDelete:Yes is also specified.</span></span>|  
|<span data-ttu-id="a9815-149">/clobber</span><span class="sxs-lookup"><span data-stu-id="a9815-149">/clobber</span></span>|<span data-ttu-id="a9815-150">Tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="a9815-150">Optional.</span></span> <span data-ttu-id="a9815-151">This argument is used only during an extraction.</span><span class="sxs-lookup"><span data-stu-id="a9815-151">This argument is used only during an extraction.</span></span> <span data-ttu-id="a9815-152">When /clobber is specified, files that have the read-only attribute set are overwritten or deleted.</span><span class="sxs-lookup"><span data-stu-id="a9815-152">When /clobber is specified, files that have the read-only attribute set are overwritten or deleted.</span></span> <span data-ttu-id="a9815-153">When not specified, files with the read-only attribute aren’t overwritten or deleted.</span><span class="sxs-lookup"><span data-stu-id="a9815-153">When not specified, files with the read-only attribute aren’t overwritten or deleted.</span></span>|  
|<span data-ttu-id="a9815-154">/errorlevel: {Off&#124;Error&#124;Warning&#124;Info&#124;Verbose}</span><span class="sxs-lookup"><span data-stu-id="a9815-154">/errorlevel: {Off&#124;Error&#124;Warning&#124;Info&#124;Verbose}</span></span>|<span data-ttu-id="a9815-155">Tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="a9815-155">Optional.</span></span> <span data-ttu-id="a9815-156">The default value is Info.</span><span class="sxs-lookup"><span data-stu-id="a9815-156">The default value is Info.</span></span> <span data-ttu-id="a9815-157">This argument indicates the level of logging information to output.</span><span class="sxs-lookup"><span data-stu-id="a9815-157">This argument indicates the level of logging information to output.</span></span>|  
|<span data-ttu-id="a9815-158">/map: \<file path></span><span class="sxs-lookup"><span data-stu-id="a9815-158">/map: \<file path></span></span>|<span data-ttu-id="a9815-159">Tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="a9815-159">Optional.</span></span> <span data-ttu-id="a9815-160">The path and name of an .xml file containing file mapping directives.</span><span class="sxs-lookup"><span data-stu-id="a9815-160">The path and name of an .xml file containing file mapping directives.</span></span> <span data-ttu-id="a9815-161">When used during an extraction, files typically read from inside the folder specified by the /folder parameter are read from alternate locations as specified in the mapping file.</span><span class="sxs-lookup"><span data-stu-id="a9815-161">When used during an extraction, files typically read from inside the folder specified by the /folder parameter are read from alternate locations as specified in the mapping file.</span></span> <span data-ttu-id="a9815-162">During a pack operation, files that match the directives aren’t written.</span><span class="sxs-lookup"><span data-stu-id="a9815-162">During a pack operation, files that match the directives aren’t written.</span></span>|  
|<span data-ttu-id="a9815-163">/nologo</span><span class="sxs-lookup"><span data-stu-id="a9815-163">/nologo</span></span>|<span data-ttu-id="a9815-164">Tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="a9815-164">Optional.</span></span> <span data-ttu-id="a9815-165">Suppress the banner at runtime.</span><span class="sxs-lookup"><span data-stu-id="a9815-165">Suppress the banner at runtime.</span></span>|  
|<span data-ttu-id="a9815-166">/log: \<file path></span><span class="sxs-lookup"><span data-stu-id="a9815-166">/log: \<file path></span></span>|<span data-ttu-id="a9815-167">Tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="a9815-167">Optional.</span></span> <span data-ttu-id="a9815-168">A path and name to a log file.</span><span class="sxs-lookup"><span data-stu-id="a9815-168">A path and name to a log file.</span></span> <span data-ttu-id="a9815-169">If the file already exists, new logging information is appended to the file.</span><span class="sxs-lookup"><span data-stu-id="a9815-169">If the file already exists, new logging information is appended to the file.</span></span>|  
|<span data-ttu-id="a9815-170">@ \<file path></span><span class="sxs-lookup"><span data-stu-id="a9815-170">@ \<file path></span></span>|<span data-ttu-id="a9815-171">Tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="a9815-171">Optional.</span></span> <span data-ttu-id="a9815-172">A path and name to a file that contains command-line arguments for the tool.</span><span class="sxs-lookup"><span data-stu-id="a9815-172">A path and name to a file that contains command-line arguments for the tool.</span></span>|  
|<span data-ttu-id="a9815-173">/sourceLoc: \<string></span><span class="sxs-lookup"><span data-stu-id="a9815-173">/sourceLoc: \<string></span></span>|<span data-ttu-id="a9815-174">Tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="a9815-174">Optional.</span></span> <span data-ttu-id="a9815-175">This argument generates a template resource file, and is valid only on extract.</span><span class="sxs-lookup"><span data-stu-id="a9815-175">This argument generates a template resource file, and is valid only on extract.</span></span><br /><br /> <span data-ttu-id="a9815-176">Possible values are `auto` or an LCID/ISO code for the language you want to export.</span><span class="sxs-lookup"><span data-stu-id="a9815-176">Possible values are `auto` or an LCID/ISO code for the language you want to export.</span></span> <span data-ttu-id="a9815-177">When this argument is used, the string resources from the given locale are extracted as a neutral .resx file.</span><span class="sxs-lookup"><span data-stu-id="a9815-177">When this argument is used, the string resources from the given locale are extracted as a neutral .resx file.</span></span> <span data-ttu-id="a9815-178">If `auto` or just the long or short form of the switch is specified, the base locale or the solution is used.</span><span class="sxs-lookup"><span data-stu-id="a9815-178">If `auto` or just the long or short form of the switch is specified, the base locale or the solution is used.</span></span> <span data-ttu-id="a9815-179">You can use the short form of the command: /src.</span><span class="sxs-lookup"><span data-stu-id="a9815-179">You can use the short form of the command: /src.</span></span>|  
|<span data-ttu-id="a9815-180">/localize</span><span class="sxs-lookup"><span data-stu-id="a9815-180">/localize</span></span>|<span data-ttu-id="a9815-181">Tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="a9815-181">Optional.</span></span> <span data-ttu-id="a9815-182">Extract or merge all string resources into .resx files.</span><span class="sxs-lookup"><span data-stu-id="a9815-182">Extract or merge all string resources into .resx files.</span></span> <span data-ttu-id="a9815-183">You can use the short form of the command: /loc.</span><span class="sxs-lookup"><span data-stu-id="a9815-183">You can use the short form of the command: /loc.</span></span>|  
  
<a name="use_command"></a>   
## <a name="use-the-map-command-argument"></a><span data-ttu-id="a9815-184">Use the /map command argument</span><span class="sxs-lookup"><span data-stu-id="a9815-184">Use the /map command argument</span></span>  
 <span data-ttu-id="a9815-185">The following discussion details the use of the /map argument to the SolutionPackager tool.</span><span class="sxs-lookup"><span data-stu-id="a9815-185">The following discussion details the use of the /map argument to the SolutionPackager tool.</span></span>  
  
 <span data-ttu-id="a9815-186">Files that are built in an automated build system, such as .xap[!INCLUDE[pn_Silverlight_short](../includes/pn-silverlight-short.md)] files and plug-in assemblies, are typically not checked into source control.</span><span class="sxs-lookup"><span data-stu-id="a9815-186">Files that are built in an automated build system, such as .xap[!INCLUDE[pn_Silverlight_short](../includes/pn-silverlight-short.md)] files and plug-in assemblies, are typically not checked into source control.</span></span> <span data-ttu-id="a9815-187">Web resources may already be present in source control in locations that are not directly compatible with the SolutionPackager tool.</span><span class="sxs-lookup"><span data-stu-id="a9815-187">Web resources may already be present in source control in locations that are not directly compatible with the SolutionPackager tool.</span></span> <span data-ttu-id="a9815-188">By including the /map parameter, the SolutionPackager tool can be directed to read and package such files from alternate locations and not from inside the Extract folder as it would typically be done.</span><span class="sxs-lookup"><span data-stu-id="a9815-188">By including the /map parameter, the SolutionPackager tool can be directed to read and package such files from alternate locations and not from inside the Extract folder as it would typically be done.</span></span> <span data-ttu-id="a9815-189">The /map parameter must specify the name and path to an XML file containing mapping directives that instruct the SolutionPackager to match files by their name and path, and indicate the alternate location to find the matched file.</span><span class="sxs-lookup"><span data-stu-id="a9815-189">The /map parameter must specify the name and path to an XML file containing mapping directives that instruct the SolutionPackager to match files by their name and path, and indicate the alternate location to find the matched file.</span></span> <span data-ttu-id="a9815-190">The following information applies to all directives equally.</span><span class="sxs-lookup"><span data-stu-id="a9815-190">The following information applies to all directives equally.</span></span>  
  
- <span data-ttu-id="a9815-191">Multiple directives may be listed including those that will match identical files.</span><span class="sxs-lookup"><span data-stu-id="a9815-191">Multiple directives may be listed including those that will match identical files.</span></span> <span data-ttu-id="a9815-192">Directives listed early in the file take precedence over those listed later.</span><span class="sxs-lookup"><span data-stu-id="a9815-192">Directives listed early in the file take precedence over those listed later.</span></span>  
  
- <span data-ttu-id="a9815-193">If a file is matched to any directive, it must be found in at least one alternative location.</span><span class="sxs-lookup"><span data-stu-id="a9815-193">If a file is matched to any directive, it must be found in at least one alternative location.</span></span> <span data-ttu-id="a9815-194">If no matching alternatives are found, the SolutionPackager will issue an error.</span><span class="sxs-lookup"><span data-stu-id="a9815-194">If no matching alternatives are found, the SolutionPackager will issue an error.</span></span>  
  
- <span data-ttu-id="a9815-195">Folder and file paths may be absolute or relative.</span><span class="sxs-lookup"><span data-stu-id="a9815-195">Folder and file paths may be absolute or relative.</span></span> <span data-ttu-id="a9815-196">Relative paths are always evaluated from the folder specified by the /folder parameter.</span><span class="sxs-lookup"><span data-stu-id="a9815-196">Relative paths are always evaluated from the folder specified by the /folder parameter.</span></span>  
  
- <span data-ttu-id="a9815-197">Environment variables may be specified by using a %variable% syntax.</span><span class="sxs-lookup"><span data-stu-id="a9815-197">Environment variables may be specified by using a %variable% syntax.</span></span>  
  
- <span data-ttu-id="a9815-198">A folder wildcard “\*\*” may be used to mean “in any sub-folder”.</span><span class="sxs-lookup"><span data-stu-id="a9815-198">A folder wildcard “\*\*” may be used to mean “in any sub-folder”.</span></span> <span data-ttu-id="a9815-199">It can only be used as the final part of a path, for example: “c:\folderA\\\*\*”.</span><span class="sxs-lookup"><span data-stu-id="a9815-199">It can only be used as the final part of a path, for example: “c:\folderA\\\*\*”.</span></span>  
  
- <span data-ttu-id="a9815-200">File name wildcards may be used only in the forms “\*.ext” or “\*.\*”.</span><span class="sxs-lookup"><span data-stu-id="a9815-200">File name wildcards may be used only in the forms “\*.ext” or “\*.\*”.</span></span> <span data-ttu-id="a9815-201">No other pattern is supported.</span><span class="sxs-lookup"><span data-stu-id="a9815-201">No other pattern is supported.</span></span>  
  
  <span data-ttu-id="a9815-202">The three types of directives mappings are described here, along with an example that shows you how to use them.</span><span class="sxs-lookup"><span data-stu-id="a9815-202">The three types of directives mappings are described here, along with an example that shows you how to use them.</span></span>  
  
<a name="Folder_mapping"></a>   
### <a name="folder-mapping"></a><span data-ttu-id="a9815-203">Folder mapping</span><span class="sxs-lookup"><span data-stu-id="a9815-203">Folder mapping</span></span>  
 <span data-ttu-id="a9815-204">The following provides detailed information on folder mapping.</span><span class="sxs-lookup"><span data-stu-id="a9815-204">The following provides detailed information on folder mapping.</span></span>  
  
 <span data-ttu-id="a9815-205">Xml Format</span><span class="sxs-lookup"><span data-stu-id="a9815-205">Xml Format</span></span>  
 `<Folder map="folderA" to="folderB" />`  
  
 <span data-ttu-id="a9815-206">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a9815-206">Description</span></span>  
 <span data-ttu-id="a9815-207">File paths that match “folderA” will be switched to “folderB”.</span><span class="sxs-lookup"><span data-stu-id="a9815-207">File paths that match “folderA” will be switched to “folderB”.</span></span>  
  
- <span data-ttu-id="a9815-208">The hierarchy of subfolders under each must exactly match.</span><span class="sxs-lookup"><span data-stu-id="a9815-208">The hierarchy of subfolders under each must exactly match.</span></span>  
  
- <span data-ttu-id="a9815-209">Folder wildcards are not supported.</span><span class="sxs-lookup"><span data-stu-id="a9815-209">Folder wildcards are not supported.</span></span>  
  
- <span data-ttu-id="a9815-210">No file names may be specified.</span><span class="sxs-lookup"><span data-stu-id="a9815-210">No file names may be specified.</span></span>  
  
  <span data-ttu-id="a9815-211">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="a9815-211">Examples</span></span>  
  ```xml  
  <Folder map="folderA" to="folderB" />  
  <Folder map="folderA\folderB" to="..\..\folderC\" />  
  <Folder map="WebResources\subFolder" to="%base%\WebResources" />  
  ```  
  
<a name="file_mapping"></a>   
### <a name="file-to-file-mapping"></a><span data-ttu-id="a9815-212">File To file mapping</span><span class="sxs-lookup"><span data-stu-id="a9815-212">File To file mapping</span></span>  
 <span data-ttu-id="a9815-213">The following provides detailed information on file-to-file mapping.</span><span class="sxs-lookup"><span data-stu-id="a9815-213">The following provides detailed information on file-to-file mapping.</span></span>  
  
 <span data-ttu-id="a9815-214">Xml Format</span><span class="sxs-lookup"><span data-stu-id="a9815-214">Xml Format</span></span>  
 `<FileToFile map="path\filename.ext" to="path\filename.ext" />`  
  
 <span data-ttu-id="a9815-215">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a9815-215">Description</span></span>  
 <span data-ttu-id="a9815-216">Any file matching the `map` parameter will be read from the name and path specified in the `to` parameter.</span><span class="sxs-lookup"><span data-stu-id="a9815-216">Any file matching the `map` parameter will be read from the name and path specified in the `to` parameter.</span></span>  
  
 <span data-ttu-id="a9815-217">For the `map` parameter:</span><span class="sxs-lookup"><span data-stu-id="a9815-217">For the `map` parameter:</span></span>  
  
- <span data-ttu-id="a9815-218">A file name must be specified.</span><span class="sxs-lookup"><span data-stu-id="a9815-218">A file name must be specified.</span></span> <span data-ttu-id="a9815-219">The path is optional.</span><span class="sxs-lookup"><span data-stu-id="a9815-219">The path is optional.</span></span> <span data-ttu-id="a9815-220">If no path is specified, files from any folder may be matched.</span><span class="sxs-lookup"><span data-stu-id="a9815-220">If no path is specified, files from any folder may be matched.</span></span>  
  
- <span data-ttu-id="a9815-221">File name wildcards are not supported.</span><span class="sxs-lookup"><span data-stu-id="a9815-221">File name wildcards are not supported.</span></span>  
  
- <span data-ttu-id="a9815-222">The folder wildcard is supported.</span><span class="sxs-lookup"><span data-stu-id="a9815-222">The folder wildcard is supported.</span></span>  
  
  <span data-ttu-id="a9815-223">For the `to` parameter:</span><span class="sxs-lookup"><span data-stu-id="a9815-223">For the `to` parameter:</span></span>  
  
- <span data-ttu-id="a9815-224">A file name and path must be specified.</span><span class="sxs-lookup"><span data-stu-id="a9815-224">A file name and path must be specified.</span></span>  
  
- <span data-ttu-id="a9815-225">The file name may differ from the name in the `map` parameter.</span><span class="sxs-lookup"><span data-stu-id="a9815-225">The file name may differ from the name in the `map` parameter.</span></span>  
  
- <span data-ttu-id="a9815-226">File name wildcards are not supported.</span><span class="sxs-lookup"><span data-stu-id="a9815-226">File name wildcards are not supported.</span></span>  
  
- <span data-ttu-id="a9815-227">The folder wildcard is supported.</span><span class="sxs-lookup"><span data-stu-id="a9815-227">The folder wildcard is supported.</span></span>  
  
  <span data-ttu-id="a9815-228">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="a9815-228">Examples</span></span>  
  ```xml  
  <FileToFile map="assembly.dll" to="c:\path\folder\assembly.dll" />  
  <FileToFile map="PluginAssemblies\**\this.dll" to="..\..\Plugins\**\that.dll" />  
  <FileToFile map="Webresrouces\ardvark.jpg" to="%SRCBASE%\CrmPackage\WebResources\JPG format\aardvark.jpg" />  
  ```  
  
<a name="file_path_mapping"></a>   
### <a name="file-to-path-mapping"></a><span data-ttu-id="a9815-229">File to path mapping</span><span class="sxs-lookup"><span data-stu-id="a9815-229">File to path mapping</span></span>  
 <span data-ttu-id="a9815-230">The following provides detailed information on file-to-path mapping.</span><span class="sxs-lookup"><span data-stu-id="a9815-230">The following provides detailed information on file-to-path mapping.</span></span>  
  
 <span data-ttu-id="a9815-231">Xml Format</span><span class="sxs-lookup"><span data-stu-id="a9815-231">Xml Format</span></span>  
 `<FileToPath map="path\filename.ext" to="path" />`  
  
 <span data-ttu-id="a9815-232">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a9815-232">Description</span></span>  
 <span data-ttu-id="a9815-233">Any file matching the `map` parameter is read from the path specified in the `to` parameter.</span><span class="sxs-lookup"><span data-stu-id="a9815-233">Any file matching the `map` parameter is read from the path specified in the `to` parameter.</span></span>  
  
 <span data-ttu-id="a9815-234">For the `map` parameter:</span><span class="sxs-lookup"><span data-stu-id="a9815-234">For the `map` parameter:</span></span>  
  
- <span data-ttu-id="a9815-235">A file name must be specified.</span><span class="sxs-lookup"><span data-stu-id="a9815-235">A file name must be specified.</span></span> <span data-ttu-id="a9815-236">The path is optional.</span><span class="sxs-lookup"><span data-stu-id="a9815-236">The path is optional.</span></span> <span data-ttu-id="a9815-237">If no path is specified, files from any folder may be matched.</span><span class="sxs-lookup"><span data-stu-id="a9815-237">If no path is specified, files from any folder may be matched.</span></span>  
  
- <span data-ttu-id="a9815-238">File name wildcards are supported.</span><span class="sxs-lookup"><span data-stu-id="a9815-238">File name wildcards are supported.</span></span>  
  
- <span data-ttu-id="a9815-239">The folder wildcard is supported.</span><span class="sxs-lookup"><span data-stu-id="a9815-239">The folder wildcard is supported.</span></span>  
  
  <span data-ttu-id="a9815-240">For the `to` parameter:</span><span class="sxs-lookup"><span data-stu-id="a9815-240">For the `to` parameter:</span></span>  
  
- <span data-ttu-id="a9815-241">A path must be specified.</span><span class="sxs-lookup"><span data-stu-id="a9815-241">A path must be specified.</span></span>  
  
- <span data-ttu-id="a9815-242">The folder wildcard is supported.</span><span class="sxs-lookup"><span data-stu-id="a9815-242">The folder wildcard is supported.</span></span>  
  
- <span data-ttu-id="a9815-243">A file name must not be specified.</span><span class="sxs-lookup"><span data-stu-id="a9815-243">A file name must not be specified.</span></span>  
  
  <span data-ttu-id="a9815-244">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="a9815-244">Examples</span></span>  
  ```xml  
  <FileToPath map="assembly.dll" to="c:\path\folder" />  
  <FileToPath map="PluginAssemblies\**\this.dll" to="..\..\Plugins\bin\**" />  
  <FileToPath map="*.jpg" to="%SRCBASE%\CrmPackage\WebResources\JPG format\" />  
  <FileToPath map="*.*" to="..\..\%ARCH%\%TYPE%\drop" />  
  ```  
  
<a name="Example_mapping"></a>   
### <a name="example-mapping"></a><span data-ttu-id="a9815-245">Example mapping</span><span class="sxs-lookup"><span data-stu-id="a9815-245">Example mapping</span></span>  
 <span data-ttu-id="a9815-246">The following XML code sample shows a complete mapping file that enables the SolutionPackager tool to read any web resource and the two default generated assemblies from a Developer Toolkit project named CRMDevTookitSample.</span><span class="sxs-lookup"><span data-stu-id="a9815-246">The following XML code sample shows a complete mapping file that enables the SolutionPackager tool to read any web resource and the two default generated assemblies from a Developer Toolkit project named CRMDevTookitSample.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<Mapping>  
       <!-- Match specific named files to an alternate folder -->  
       <FileToFile map="CRMDevTookitSamplePlugins.dll" to="..\..\Plugins\bin\**\CRMDevTookitSample.plugins.dll" />  
       <FileToFile map="CRMDevTookitSampleWorkflow.dll" to="..\..\Workflow\bin\**\CRMDevTookitSample.Workflow.dll" />  
       <!-- Match any file in and under WebResources to an alternate set of sub-folders -->  
       <FileToPath map="WebResources\*.*" to="..\..\CrmPackage\WebResources\**" />  
       <FileToPath map="WebResources\**\*.*" to="..\..\CrmPackage\WebResources\**" />  
</Mapping>  
```  
  
<a name="managed"></a>   
## <a name="managed-and-unmanaged-solutions"></a><span data-ttu-id="a9815-247">Giải pháp được quản lý và không được quản lý</span><span class="sxs-lookup"><span data-stu-id="a9815-247">Managed and unmanaged solutions</span></span>  
 <span data-ttu-id="a9815-248">A [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps compressed solution (.zip) file can be exported in one of two types as shown here.</span><span class="sxs-lookup"><span data-stu-id="a9815-248">A [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps compressed solution (.zip) file can be exported in one of two types as shown here.</span></span>  
  
 <span data-ttu-id="a9815-249">Managed solution</span><span class="sxs-lookup"><span data-stu-id="a9815-249">Managed solution</span></span>  
 <span data-ttu-id="a9815-250">A completed solution ready to be imported into an organization.</span><span class="sxs-lookup"><span data-stu-id="a9815-250">A completed solution ready to be imported into an organization.</span></span> <span data-ttu-id="a9815-251">Once imported, components can’t be added or removed, although they can optionally allow further customization.</span><span class="sxs-lookup"><span data-stu-id="a9815-251">Once imported, components can’t be added or removed, although they can optionally allow further customization.</span></span> <span data-ttu-id="a9815-252">This is recommended when development of the solution is complete.</span><span class="sxs-lookup"><span data-stu-id="a9815-252">This is recommended when development of the solution is complete.</span></span>  
  
 <span data-ttu-id="a9815-253">Unmanaged solution</span><span class="sxs-lookup"><span data-stu-id="a9815-253">Unmanaged solution</span></span>  
 <span data-ttu-id="a9815-254">An open solution with no restrictions on what can be added, removed, or modified.</span><span class="sxs-lookup"><span data-stu-id="a9815-254">An open solution with no restrictions on what can be added, removed, or modified.</span></span> <span data-ttu-id="a9815-255">This is recommended during development of a solution.</span><span class="sxs-lookup"><span data-stu-id="a9815-255">This is recommended during development of a solution.</span></span>  
  
 <span data-ttu-id="a9815-256">The format of a compressed solution file will be different based on its type, either managed or unmanaged.</span><span class="sxs-lookup"><span data-stu-id="a9815-256">The format of a compressed solution file will be different based on its type, either managed or unmanaged.</span></span> <span data-ttu-id="a9815-257">The SolutionPackager can process compressed solution files of either type.</span><span class="sxs-lookup"><span data-stu-id="a9815-257">The SolutionPackager can process compressed solution files of either type.</span></span> <span data-ttu-id="a9815-258">However, the tool can’t convert one type to another.</span><span class="sxs-lookup"><span data-stu-id="a9815-258">However, the tool can’t convert one type to another.</span></span> <span data-ttu-id="a9815-259">The only way to convert solution files to a different type, for example from unmanaged to managed, is by importing the unmanaged solution .zip file into a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps server and then exporting the solution as a managed solution.</span><span class="sxs-lookup"><span data-stu-id="a9815-259">The only way to convert solution files to a different type, for example from unmanaged to managed, is by importing the unmanaged solution .zip file into a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps server and then exporting the solution as a managed solution.</span></span>  
  
 <span data-ttu-id="a9815-260">The SolutionPackager can process unmanaged and managed solution .zip files as a combined set via the /PackageType:Both parameter.</span><span class="sxs-lookup"><span data-stu-id="a9815-260">The SolutionPackager can process unmanaged and managed solution .zip files as a combined set via the /PackageType:Both parameter.</span></span> <span data-ttu-id="a9815-261">To perform this operation, it is necessary to export your solution twice as each type, naming the .zip files as follows.</span><span class="sxs-lookup"><span data-stu-id="a9815-261">To perform this operation, it is necessary to export your solution twice as each type, naming the .zip files as follows.</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="a9815-262">Unmanaged .zip file: AnyName.zip</span><span class="sxs-lookup"><span data-stu-id="a9815-262">Unmanaged .zip file: AnyName.zip</span></span>|<span data-ttu-id="a9815-263">Managed .zip file: AnyName_managed.zip</span><span class="sxs-lookup"><span data-stu-id="a9815-263">Managed .zip file: AnyName_managed.zip</span></span>|  
  
 <span data-ttu-id="a9815-264">The tool will assume the presence of the managed zip file in the same folder as the unmanaged file and extract both files into a single folder preserving the differences where managed and unmanaged components exist.</span><span class="sxs-lookup"><span data-stu-id="a9815-264">The tool will assume the presence of the managed zip file in the same folder as the unmanaged file and extract both files into a single folder preserving the differences where managed and unmanaged components exist.</span></span>  
  
 <span data-ttu-id="a9815-265">After a solution has been extracted as both unmanaged and managed, it is possible from that single folder to pack both, or each type individually, using the /PackageType parameter to specify which type to create.</span><span class="sxs-lookup"><span data-stu-id="a9815-265">After a solution has been extracted as both unmanaged and managed, it is possible from that single folder to pack both, or each type individually, using the /PackageType parameter to specify which type to create.</span></span> <span data-ttu-id="a9815-266">When specifying both, two .zip files will be produced using the naming convention as above.</span><span class="sxs-lookup"><span data-stu-id="a9815-266">When specifying both, two .zip files will be produced using the naming convention as above.</span></span> <span data-ttu-id="a9815-267">If the /PackageType parameter is missing when packing from a dual managed and unmanaged folder, the default is to produce a single unmanaged .zip file.</span><span class="sxs-lookup"><span data-stu-id="a9815-267">If the /PackageType parameter is missing when packing from a dual managed and unmanaged folder, the default is to produce a single unmanaged .zip file.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="a9815-268">Khắc phục sự cố</span><span class="sxs-lookup"><span data-stu-id="a9815-268">Troubleshooting</span></span>  
 <span data-ttu-id="a9815-269">If you use [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)] to edit resource files created by the solution packager, you may receive a message when you repack similar to this: `“Failed to determine version id of the resource file <filename>.resx the resource file must be exported from the solutionpackager.exe tool in order to be used as part of the pack process.”` This happens because [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] replaces the resource file’s metadata tags with data tags.</span><span class="sxs-lookup"><span data-stu-id="a9815-269">If you use [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)] to edit resource files created by the solution packager, you may receive a message when you repack similar to this: `“Failed to determine version id of the resource file <filename>.resx the resource file must be exported from the solutionpackager.exe tool in order to be used as part of the pack process.”` This happens because [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] replaces the resource file’s metadata tags with data tags.</span></span>  
  
#### <a name="workaround"></a><span data-ttu-id="a9815-270">Giải pháp thay thế</span><span class="sxs-lookup"><span data-stu-id="a9815-270">Workaround</span></span>  
  
1. <span data-ttu-id="a9815-271">Open the resource file in your favorite text editor and locate and update the following tags:</span><span class="sxs-lookup"><span data-stu-id="a9815-271">Open the resource file in your favorite text editor and locate and update the following tags:</span></span>  
  
   ```xml  
   <data name="Source LCID" xml:space="preserve">  
   <data name="Source file" xml:space="preserve">  
   <data name="Source package type" xml:space="preserve">  
   <data name="SolutionPackager Version" mimetype="application/x-microsoft.net.object.binary.base64">  
  
   ```  
  
2. <span data-ttu-id="a9815-272">Change the node name from `<data>` to `<metadata>`.</span><span class="sxs-lookup"><span data-stu-id="a9815-272">Change the node name from `<data>` to `<metadata>`.</span></span>  
  
    <span data-ttu-id="a9815-273">For example, this string:</span><span class="sxs-lookup"><span data-stu-id="a9815-273">For example, this string:</span></span>  
  
   ```xml  
   <data name="Source LCID" xml:space="preserve">  
     <value>1033</value>  
   </data>  
  
   ```  
  
    <span data-ttu-id="a9815-274">Changes to:</span><span class="sxs-lookup"><span data-stu-id="a9815-274">Changes to:</span></span>  
  
   ```xml  
   <metadata name="Source LCID" xml:space="preserve">  
     <value>1033</value>  
   </metadata>  
  
   ```  
  
   <span data-ttu-id="a9815-275">This allows the solution packager to read and import the resource file.</span><span class="sxs-lookup"><span data-stu-id="a9815-275">This allows the solution packager to read and import the resource file.</span></span> <span data-ttu-id="a9815-276">This problem has only been observed when using the [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] Resource editor.</span><span class="sxs-lookup"><span data-stu-id="a9815-276">This problem has only been observed when using the [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] Resource editor.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="a9815-277">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a9815-277">See also</span></span>  
 <span data-ttu-id="a9815-278">[Solution Tools for Team Development](solution-tools-team-development.md) </span><span class="sxs-lookup"><span data-stu-id="a9815-278">[Solution Tools for Team Development](solution-tools-team-development.md) </span></span>  
 <span data-ttu-id="a9815-279">[Use Source Control with Solution Files](use-source-control-solution-files.md) </span><span class="sxs-lookup"><span data-stu-id="a9815-279">[Use Source Control with Solution Files](use-source-control-solution-files.md) </span></span>  
 <span data-ttu-id="a9815-280">[Solution Component File Reference](solution-component-file-reference-solutionpackager.md) </span><span class="sxs-lookup"><span data-stu-id="a9815-280">[Solution Component File Reference](solution-component-file-reference-solutionpackager.md) </span></span>  
 [<span data-ttu-id="a9815-281">Introduction to Solutions</span><span class="sxs-lookup"><span data-stu-id="a9815-281">Introduction to Solutions</span></span>](introduction-solutions.md)
