---
title: Use source control with solution files (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: The SolutionPackager tool can be used with any source control system. After a solution .zip file has been extracted to a folder, simply add and submit the files to your source control system. These files can then be synchronized on another computer where they can be packed into a new identical solution .zip file.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: e2ca3f4c-201e-4d7e-be0d-85eef2ce3e73
caps.latest.revision: 15
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 92a4293e4cc4932f40c47cd5ff35c743aa5807c0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386786"
---
# <a name="use-source-control-with-solution-files"></a><span data-ttu-id="e71a1-105">Use source control with solution files</span><span class="sxs-lookup"><span data-stu-id="e71a1-105">Use source control with solution files</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e71a1-106">The SolutionPackager tool can be used with any source control system.</span><span class="sxs-lookup"><span data-stu-id="e71a1-106">The SolutionPackager tool can be used with any source control system.</span></span> <span data-ttu-id="e71a1-107">After a solution .zip file has been extracted to a folder, simply add and submit the files to your source control system.</span><span class="sxs-lookup"><span data-stu-id="e71a1-107">After a solution .zip file has been extracted to a folder, simply add and submit the files to your source control system.</span></span> <span data-ttu-id="e71a1-108">These files can then be synchronized on another computer where they can be packed into a new identical solution .zip file.</span><span class="sxs-lookup"><span data-stu-id="e71a1-108">These files can then be synchronized on another computer where they can be packed into a new identical solution .zip file.</span></span>  
  
 <span data-ttu-id="e71a1-109">An important aspect when using extracted component files in source control is that adding all the files into source control may cause unnecessary duplication.</span><span class="sxs-lookup"><span data-stu-id="e71a1-109">An important aspect when using extracted component files in source control is that adding all the files into source control may cause unnecessary duplication.</span></span> <span data-ttu-id="e71a1-110">See the [Solution Component File Reference](solution-component-file-reference-solutionpackager.md) to see which files are generated for each component type and which files are recommended for use in source control.</span><span class="sxs-lookup"><span data-stu-id="e71a1-110">See the [Solution Component File Reference](solution-component-file-reference-solutionpackager.md) to see which files are generated for each component type and which files are recommended for use in source control.</span></span>  
  
 <span data-ttu-id="e71a1-111">As further customizations and changes are necessary for the solution, developers should edit or customize components through existing means, export again to create a .zip file, and extract the compressed solution file into the same folder.</span><span class="sxs-lookup"><span data-stu-id="e71a1-111">As further customizations and changes are necessary for the solution, developers should edit or customize components through existing means, export again to create a .zip file, and extract the compressed solution file into the same folder.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="e71a1-112">Except for the sections described in [When to edit the customizations file](customize-dev/when-edit-customization-file.md), manual editing of extracted component files and .zip files is not supported.</span><span class="sxs-lookup"><span data-stu-id="e71a1-112">Except for the sections described in [When to edit the customizations file](customize-dev/when-edit-customization-file.md), manual editing of extracted component files and .zip files is not supported.</span></span>  
  
 <span data-ttu-id="e71a1-113">When the SolutionPackager tool extracts the component files it will not overwrite existing component files of the same name if the file contents are identical.</span><span class="sxs-lookup"><span data-stu-id="e71a1-113">When the SolutionPackager tool extracts the component files it will not overwrite existing component files of the same name if the file contents are identical.</span></span> <span data-ttu-id="e71a1-114">In addition, the tool honors the read-only attribute on component files producing a warning in the console window that particular files were not written.</span><span class="sxs-lookup"><span data-stu-id="e71a1-114">In addition, the tool honors the read-only attribute on component files producing a warning in the console window that particular files were not written.</span></span> <span data-ttu-id="e71a1-115">This enables the user to check out, from source control, the minimal set of files that are changing.</span><span class="sxs-lookup"><span data-stu-id="e71a1-115">This enables the user to check out, from source control, the minimal set of files that are changing.</span></span> <span data-ttu-id="e71a1-116">The `/clobber` parameter can be used to override and cause read-only files to be written or deleted.</span><span class="sxs-lookup"><span data-stu-id="e71a1-116">The `/clobber` parameter can be used to override and cause read-only files to be written or deleted.</span></span> <span data-ttu-id="e71a1-117">The `/allowWrite` parameter can be used to assess what impact an extract operation has without actually causing any files to be written or deleted.</span><span class="sxs-lookup"><span data-stu-id="e71a1-117">The `/allowWrite` parameter can be used to assess what impact an extract operation has without actually causing any files to be written or deleted.</span></span> <span data-ttu-id="e71a1-118">Use of the `/allowWrite` parameter with verbose logging is effective.</span><span class="sxs-lookup"><span data-stu-id="e71a1-118">Use of the `/allowWrite` parameter with verbose logging is effective.</span></span>  
  
 <span data-ttu-id="e71a1-119">After the extract operation is completed with the minimal set of files checked out from source control, a developer may submit the changed files back into source control, as is done with any other type of source file.</span><span class="sxs-lookup"><span data-stu-id="e71a1-119">After the extract operation is completed with the minimal set of files checked out from source control, a developer may submit the changed files back into source control, as is done with any other type of source file.</span></span>  
  
<a name="team_dev"></a>   
## <a name="team-development"></a><span data-ttu-id="e71a1-120">Team development</span><span class="sxs-lookup"><span data-stu-id="e71a1-120">Team development</span></span>  
 <span data-ttu-id="e71a1-121">When there are multiple developers working on the same solution component a conflict might arise where changes from two developers result in changes to a single file.</span><span class="sxs-lookup"><span data-stu-id="e71a1-121">When there are multiple developers working on the same solution component a conflict might arise where changes from two developers result in changes to a single file.</span></span> <span data-ttu-id="e71a1-122">This occurrence is minimized by decomposing each individually editable component or subcomponent into a distinct file.</span><span class="sxs-lookup"><span data-stu-id="e71a1-122">This occurrence is minimized by decomposing each individually editable component or subcomponent into a distinct file.</span></span> <span data-ttu-id="e71a1-123">Consider the following example.</span><span class="sxs-lookup"><span data-stu-id="e71a1-123">Consider the following example.</span></span>  
  
1. <span data-ttu-id="e71a1-124">Developer A and B are both working on the same solution.</span><span class="sxs-lookup"><span data-stu-id="e71a1-124">Developer A and B are both working on the same solution.</span></span>  
  
2. <span data-ttu-id="e71a1-125">On independent computers, they both get the latest sources of the solution from source control, pack, and import an unmanaged solution .zip file into independent [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement organizations.</span><span class="sxs-lookup"><span data-stu-id="e71a1-125">On independent computers, they both get the latest sources of the solution from source control, pack, and import an unmanaged solution .zip file into independent [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement organizations.</span></span>  
  
3. <span data-ttu-id="e71a1-126">Developer A customizes the “Active Contacts” system view and the main form for the Contact entity.</span><span class="sxs-lookup"><span data-stu-id="e71a1-126">Developer A customizes the “Active Contacts” system view and the main form for the Contact entity.</span></span>  
  
4. <span data-ttu-id="e71a1-127">Developer B customizes the main form for the Account entity and changes the “Contact Lookup View”.</span><span class="sxs-lookup"><span data-stu-id="e71a1-127">Developer B customizes the main form for the Account entity and changes the “Contact Lookup View”.</span></span>  
  
5. <span data-ttu-id="e71a1-128">Both developers export an unmanaged solution .zip file and extract.</span><span class="sxs-lookup"><span data-stu-id="e71a1-128">Both developers export an unmanaged solution .zip file and extract.</span></span>  
  
   1.  <span data-ttu-id="e71a1-129">Developer A will need to check out one file for the Contact main form, and one file for the “Active Contacts” view.</span><span class="sxs-lookup"><span data-stu-id="e71a1-129">Developer A will need to check out one file for the Contact main form, and one file for the “Active Contacts” view.</span></span>  
  
   2.  <span data-ttu-id="e71a1-130">Developer B will need to check out one file for the Account main form, and one file for the “Contact Lookup View”.</span><span class="sxs-lookup"><span data-stu-id="e71a1-130">Developer B will need to check out one file for the Account main form, and one file for the “Contact Lookup View”.</span></span>  
  
6. <span data-ttu-id="e71a1-131">Both developers may submit, in any order, as their respective changes touched separate files.</span><span class="sxs-lookup"><span data-stu-id="e71a1-131">Both developers may submit, in any order, as their respective changes touched separate files.</span></span>  
  
7. <span data-ttu-id="e71a1-132">After both submissions are complete, they can repeat step #2 and then continue to make further changes in their independent organizations.</span><span class="sxs-lookup"><span data-stu-id="e71a1-132">After both submissions are complete, they can repeat step #2 and then continue to make further changes in their independent organizations.</span></span> <span data-ttu-id="e71a1-133">They each have both sets of changes, with no overwrites of their own work.</span><span class="sxs-lookup"><span data-stu-id="e71a1-133">They each have both sets of changes, with no overwrites of their own work.</span></span>  
  
   <span data-ttu-id="e71a1-134">The previous example works only when there are changes to separate files.</span><span class="sxs-lookup"><span data-stu-id="e71a1-134">The previous example works only when there are changes to separate files.</span></span> <span data-ttu-id="e71a1-135">It is inevitable that independent customizations require changes within a single file.</span><span class="sxs-lookup"><span data-stu-id="e71a1-135">It is inevitable that independent customizations require changes within a single file.</span></span> <span data-ttu-id="e71a1-136">Based on the example shown above, consider that developer B customized the “Active Contacts” view while developer A was also customizing it.</span><span class="sxs-lookup"><span data-stu-id="e71a1-136">Based on the example shown above, consider that developer B customized the “Active Contacts” view while developer A was also customizing it.</span></span> <span data-ttu-id="e71a1-137">In this new example, the order of events becomes important.</span><span class="sxs-lookup"><span data-stu-id="e71a1-137">In this new example, the order of events becomes important.</span></span> <span data-ttu-id="e71a1-138">The correct process to reconcile this predicament, written out in full, is as follows.</span><span class="sxs-lookup"><span data-stu-id="e71a1-138">The correct process to reconcile this predicament, written out in full, is as follows.</span></span>  
  
8. <span data-ttu-id="e71a1-139">Developer A and B are both working on the same solution.</span><span class="sxs-lookup"><span data-stu-id="e71a1-139">Developer A and B are both working on the same solution.</span></span>  
  
9. <span data-ttu-id="e71a1-140">On independent computers, they both get the latest sources of the solution from source control, pack, and import an unmanaged solution .zip file into independent organizations.</span><span class="sxs-lookup"><span data-stu-id="e71a1-140">On independent computers, they both get the latest sources of the solution from source control, pack, and import an unmanaged solution .zip file into independent organizations.</span></span>  
  
10. <span data-ttu-id="e71a1-141">Developer A customizes the “Active Contacts” system view and the main form for the Contact entity.</span><span class="sxs-lookup"><span data-stu-id="e71a1-141">Developer A customizes the “Active Contacts” system view and the main form for the Contact entity.</span></span>  
  
11. <span data-ttu-id="e71a1-142">Developer B customizes the main form for the Account entity and changes the “Active Contacts”.</span><span class="sxs-lookup"><span data-stu-id="e71a1-142">Developer B customizes the main form for the Account entity and changes the “Active Contacts”.</span></span>  
  
12. <span data-ttu-id="e71a1-143">Both developers export an unmanaged solution .</span><span class="sxs-lookup"><span data-stu-id="e71a1-143">Both developers export an unmanaged solution .</span></span> <span data-ttu-id="e71a1-144">zip file and extract.</span><span class="sxs-lookup"><span data-stu-id="e71a1-144">zip file and extract.</span></span>  
  
    1.  <span data-ttu-id="e71a1-145">Developer A will need to check out one file for the Contact main form, and one file for the “Active Contacts” view.</span><span class="sxs-lookup"><span data-stu-id="e71a1-145">Developer A will need to check out one file for the Contact main form, and one file for the “Active Contacts” view.</span></span>  
  
    2.  <span data-ttu-id="e71a1-146">Developer B will need to check out one file for the Account main form, and one file for the “Active Contacts” view.</span><span class="sxs-lookup"><span data-stu-id="e71a1-146">Developer B will need to check out one file for the Account main form, and one file for the “Active Contacts” view.</span></span>  
  
13. <span data-ttu-id="e71a1-147">Developer A is ready first.</span><span class="sxs-lookup"><span data-stu-id="e71a1-147">Developer A is ready first.</span></span>  
  
    1.  <span data-ttu-id="e71a1-148">Before he submits to source control he must get latest sources to ensure no prior check-ins conflict with his changes.</span><span class="sxs-lookup"><span data-stu-id="e71a1-148">Before he submits to source control he must get latest sources to ensure no prior check-ins conflict with his changes.</span></span>  
  
    2.  <span data-ttu-id="e71a1-149">There are no conflicts so he is able to submit.</span><span class="sxs-lookup"><span data-stu-id="e71a1-149">There are no conflicts so he is able to submit.</span></span>  
  
14. <span data-ttu-id="e71a1-150">Developer B is ready next following developer A.</span><span class="sxs-lookup"><span data-stu-id="e71a1-150">Developer B is ready next following developer A.</span></span>  
  
    1.  <span data-ttu-id="e71a1-151">Before he submits he must get the latest sources to ensure no prior check-ins conflict with his changes.</span><span class="sxs-lookup"><span data-stu-id="e71a1-151">Before he submits he must get the latest sources to ensure no prior check-ins conflict with his changes.</span></span>  
  
    2.  <span data-ttu-id="e71a1-152">There is a conflict because the file for “Active Contacts” has been modified since he last retrieved the latest sources.</span><span class="sxs-lookup"><span data-stu-id="e71a1-152">There is a conflict because the file for “Active Contacts” has been modified since he last retrieved the latest sources.</span></span>  
  
    3.  <span data-ttu-id="e71a1-153">Developer B must reconcile the conflict.</span><span class="sxs-lookup"><span data-stu-id="e71a1-153">Developer B must reconcile the conflict.</span></span> <span data-ttu-id="e71a1-154">It is possible the capabilities of the source control system in use may aide this process; otherwise the following choices are all viable.</span><span class="sxs-lookup"><span data-stu-id="e71a1-154">It is possible the capabilities of the source control system in use may aide this process; otherwise the following choices are all viable.</span></span>  
  
        1.  <span data-ttu-id="e71a1-155">Developer B, through source control history, if available, can see that the developer A made the prior change.</span><span class="sxs-lookup"><span data-stu-id="e71a1-155">Developer B, through source control history, if available, can see that the developer A made the prior change.</span></span> <span data-ttu-id="e71a1-156">Through direct communication they can discuss each change.</span><span class="sxs-lookup"><span data-stu-id="e71a1-156">Through direct communication they can discuss each change.</span></span> <span data-ttu-id="e71a1-157">Then developer B only has to update his organization with the agreed resolution.</span><span class="sxs-lookup"><span data-stu-id="e71a1-157">Then developer B only has to update his organization with the agreed resolution.</span></span> <span data-ttu-id="e71a1-158">He then exports, extracts, and overwrites the conflicting file and submits.</span><span class="sxs-lookup"><span data-stu-id="e71a1-158">He then exports, extracts, and overwrites the conflicting file and submits.</span></span>  
  
        2.  <span data-ttu-id="e71a1-159">Allow source control to overwrite his local file.</span><span class="sxs-lookup"><span data-stu-id="e71a1-159">Allow source control to overwrite his local file.</span></span> <span data-ttu-id="e71a1-160">Developer B packs the solution and imports it into his organization, then assesses the state of the view and re-customizes it as necessary.</span><span class="sxs-lookup"><span data-stu-id="e71a1-160">Developer B packs the solution and imports it into his organization, then assesses the state of the view and re-customizes it as necessary.</span></span> <span data-ttu-id="e71a1-161">Next, he may export, extract, and overwrite the conflicting file.</span><span class="sxs-lookup"><span data-stu-id="e71a1-161">Next, he may export, extract, and overwrite the conflicting file.</span></span>  
  
        3.  <span data-ttu-id="e71a1-162">If the prior change can be deemed unnecessary, developer B allows his copy of the file to overwrite the version in source control and submits.</span><span class="sxs-lookup"><span data-stu-id="e71a1-162">If the prior change can be deemed unnecessary, developer B allows his copy of the file to overwrite the version in source control and submits.</span></span>  
  
    <span data-ttu-id="e71a1-163">Whether working on a shared organization or independent organizations, team development of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] solutions requires those actively working on a common solution to be aware of the work of others.</span><span class="sxs-lookup"><span data-stu-id="e71a1-163">Whether working on a shared organization or independent organizations, team development of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] solutions requires those actively working on a common solution to be aware of the work of others.</span></span> <span data-ttu-id="e71a1-164">The SolutionPackager tool does not fully remove this need but it does enable easy merging of non-conflicting changes at the source control level, and it proactively highlights the concise components where conflicts have arisen.</span><span class="sxs-lookup"><span data-stu-id="e71a1-164">The SolutionPackager tool does not fully remove this need but it does enable easy merging of non-conflicting changes at the source control level, and it proactively highlights the concise components where conflicts have arisen.</span></span>  
  
    <span data-ttu-id="e71a1-165">The next sections are the generic processes to effectively use the SolutionPackager tool in source control when developing with teams.</span><span class="sxs-lookup"><span data-stu-id="e71a1-165">The next sections are the generic processes to effectively use the SolutionPackager tool in source control when developing with teams.</span></span> <span data-ttu-id="e71a1-166">These work equally with independent organizations or shared development organizations, though with shared organizations the export and extract will naturally include all changes present within the solution, not just those made by the developer performing the export.</span><span class="sxs-lookup"><span data-stu-id="e71a1-166">These work equally with independent organizations or shared development organizations, though with shared organizations the export and extract will naturally include all changes present within the solution, not just those made by the developer performing the export.</span></span> <span data-ttu-id="e71a1-167">Similarly, when importing a solution .zip file the natural behavior to overwrite all components will occur.</span><span class="sxs-lookup"><span data-stu-id="e71a1-167">Similarly, when importing a solution .zip file the natural behavior to overwrite all components will occur.</span></span>  
  
<a name="create_sol"></a>   
## <a name="create-a-solution"></a><span data-ttu-id="e71a1-168">Tạo một giải pháp</span><span class="sxs-lookup"><span data-stu-id="e71a1-168">Create a solution</span></span>  
 <span data-ttu-id="e71a1-169">The following procedure identifies the typical steps used when first creating a solution.</span><span class="sxs-lookup"><span data-stu-id="e71a1-169">The following procedure identifies the typical steps used when first creating a solution.</span></span>  
  
1. <span data-ttu-id="e71a1-170">In a clean organization, create a solution on [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server, and then add or create components as necessary.</span><span class="sxs-lookup"><span data-stu-id="e71a1-170">In a clean organization, create a solution on [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server, and then add or create components as necessary.</span></span>  
  
2. <span data-ttu-id="e71a1-171">When you are ready to check in, do the following.</span><span class="sxs-lookup"><span data-stu-id="e71a1-171">When you are ready to check in, do the following.</span></span>  
  
   1.  <span data-ttu-id="e71a1-172">Export the unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="e71a1-172">Export the unmanaged solution.</span></span>  
  
   2.  <span data-ttu-id="e71a1-173">Using the SolutionPackager tool, extract the solution into component files.</span><span class="sxs-lookup"><span data-stu-id="e71a1-173">Using the SolutionPackager tool, extract the solution into component files.</span></span>  
  
   3.  <span data-ttu-id="e71a1-174">From those extracted component files, add the necessary files to source control.</span><span class="sxs-lookup"><span data-stu-id="e71a1-174">From those extracted component files, add the necessary files to source control.</span></span>  
  
   4.  <span data-ttu-id="e71a1-175">Submit these changes to source control.</span><span class="sxs-lookup"><span data-stu-id="e71a1-175">Submit these changes to source control.</span></span>  
  
<a name="modify_sol"></a>   
## <a name="modify-a-solution"></a><span data-ttu-id="e71a1-176">Modify a solution</span><span class="sxs-lookup"><span data-stu-id="e71a1-176">Modify a solution</span></span>  
 <span data-ttu-id="e71a1-177">The following procedure identifies the typical steps used when modifying an existing solution.</span><span class="sxs-lookup"><span data-stu-id="e71a1-177">The following procedure identifies the typical steps used when modifying an existing solution.</span></span>  
  
1. <span data-ttu-id="e71a1-178">Synchronize or get the latest solution component file sources.</span><span class="sxs-lookup"><span data-stu-id="e71a1-178">Synchronize or get the latest solution component file sources.</span></span>  
  
2. <span data-ttu-id="e71a1-179">Using the SolutionPackager tool, pack component files into an unmanaged solution .zip file.</span><span class="sxs-lookup"><span data-stu-id="e71a1-179">Using the SolutionPackager tool, pack component files into an unmanaged solution .zip file.</span></span>  
  
3. <span data-ttu-id="e71a1-180">Import the unmanaged solution file into an organization.</span><span class="sxs-lookup"><span data-stu-id="e71a1-180">Import the unmanaged solution file into an organization.</span></span>  
  
4. <span data-ttu-id="e71a1-181">Customize and edit the solution as necessary.</span><span class="sxs-lookup"><span data-stu-id="e71a1-181">Customize and edit the solution as necessary.</span></span>  
  
5. <span data-ttu-id="e71a1-182">When you are ready to check the changes into source control, do the following.</span><span class="sxs-lookup"><span data-stu-id="e71a1-182">When you are ready to check the changes into source control, do the following.</span></span>  
  
   1.  <span data-ttu-id="e71a1-183">Export the unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="e71a1-183">Export the unmanaged solution.</span></span>  
  
   2.  <span data-ttu-id="e71a1-184">Using the SolutionPackager tool, extract the exported solution into component files.</span><span class="sxs-lookup"><span data-stu-id="e71a1-184">Using the SolutionPackager tool, extract the exported solution into component files.</span></span>  
  
   3.  <span data-ttu-id="e71a1-185">Synchronize or get the latest sources from source control.</span><span class="sxs-lookup"><span data-stu-id="e71a1-185">Synchronize or get the latest sources from source control.</span></span>  
  
   4.  <span data-ttu-id="e71a1-186">Reconcile if any conflicts exist.</span><span class="sxs-lookup"><span data-stu-id="e71a1-186">Reconcile if any conflicts exist.</span></span>  
  
   5.  <span data-ttu-id="e71a1-187">Submit the changes to source control.</span><span class="sxs-lookup"><span data-stu-id="e71a1-187">Submit the changes to source control.</span></span>  
  
   <span data-ttu-id="e71a1-188">Steps 2 and 3 must be done before further customizations occur in the development organization.</span><span class="sxs-lookup"><span data-stu-id="e71a1-188">Steps 2 and 3 must be done before further customizations occur in the development organization.</span></span> <span data-ttu-id="e71a1-189">Within step 5, step b must be completed before step c.</span><span class="sxs-lookup"><span data-stu-id="e71a1-189">Within step 5, step b must be completed before step c.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e71a1-190">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e71a1-190">See also</span></span>  
 <span data-ttu-id="e71a1-191">[Solution Tools for Team Development](solution-tools-team-development.md) </span><span class="sxs-lookup"><span data-stu-id="e71a1-191">[Solution Tools for Team Development](solution-tools-team-development.md) </span></span>  
 <span data-ttu-id="e71a1-192">[Solution Component File Reference (SolutionPackager)](solution-component-file-reference-solutionpackager.md) </span><span class="sxs-lookup"><span data-stu-id="e71a1-192">[Solution Component File Reference (SolutionPackager)](solution-component-file-reference-solutionpackager.md) </span></span>  
 [<span data-ttu-id="e71a1-193">Use the SolutionPackager Tool to Compress and Extract a Solution File</span><span class="sxs-lookup"><span data-stu-id="e71a1-193">Use the SolutionPackager Tool to Compress and Extract a Solution File</span></span>](compress-extract-solution-file-solutionpackager.md)
