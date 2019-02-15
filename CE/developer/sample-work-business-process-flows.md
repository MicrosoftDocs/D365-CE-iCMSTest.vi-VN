---
title: 'Sample: Work with business process flows (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: The sample demonstrates how to programmatically work with business process flows such as retrieving the business process flow instances for an entity record, retrieving active path for a business process flow instance and its process stages, and changing the active stage.
ms.custom: ''
ms.date: 04/05/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 7d378504-b4b2-4a09-838c-69ee094072ef
caps.latest.revision: 15
author: KumarVivek
ms.author: kvivek
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2b73c0417ff0a27d4fa35428b29b35ad53595a81
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387485"
---
# <a name="sample-work-with-business-process-flows"></a><span data-ttu-id="79fba-103">Sample: Work with business process flows</span><span class="sxs-lookup"><span data-stu-id="79fba-103">Sample: Work with business process flows</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="79fba-104">This sample demonstrates how to programmatically work with business process flows such as retrieving the business process flow instances for an entity record, retrieving active path for a business process flow instance and its process stages, and changing the active stage.</span><span class="sxs-lookup"><span data-stu-id="79fba-104">This sample demonstrates how to programmatically work with business process flows such as retrieving the business process flow instances for an entity record, retrieving active path for a business process flow instance and its process stages, and changing the active stage.</span></span> <span data-ttu-id="79fba-105">For information about these concepts, see [Model business process flows](model-business-process-flows.md)</span><span class="sxs-lookup"><span data-stu-id="79fba-105">For information about these concepts, see [Model business process flows](model-business-process-flows.md)</span></span>  

 <span data-ttu-id="79fba-106">This sample is for [!INCLUDE[pn_crm_8_2_0_both](../includes/pn-crm-8-2-0-both.md)], and is available to download from [Sample: Work with business process flows](https://go.microsoft.com/fwlink/p/?LinkId=846108).</span><span class="sxs-lookup"><span data-stu-id="79fba-106">This sample is for [!INCLUDE[pn_crm_8_2_0_both](../includes/pn-crm-8-2-0-both.md)], and is available to download from [Sample: Work with business process flows](https://go.microsoft.com/fwlink/p/?LinkId=846108).</span></span>  

<a name="BKMK_Prerequisites"></a>   
## <a name="prerequisites"></a><span data-ttu-id="79fba-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="79fba-107">Prerequisites</span></span>  
 <span data-ttu-id="79fba-108">Before you can run the sample:</span><span class="sxs-lookup"><span data-stu-id="79fba-108">Before you can run the sample:</span></span>  

1. <span data-ttu-id="79fba-109">Have access to a [!INCLUDE[pn_crm_8_2_0_both](../includes/pn-crm-8-2-0-both.md)] or later organization.</span><span class="sxs-lookup"><span data-stu-id="79fba-109">Have access to a [!INCLUDE[pn_crm_8_2_0_both](../includes/pn-crm-8-2-0-both.md)] or later organization.</span></span>  

2. <span data-ttu-id="79fba-110">Have appropriate privileges on the Lead, Opportunity, and Workflow entities and business process  flow definition entity records used in this sample.</span><span class="sxs-lookup"><span data-stu-id="79fba-110">Have appropriate privileges on the Lead, Opportunity, and Workflow entities and business process  flow definition entity records used in this sample.</span></span>  

3. <span data-ttu-id="79fba-111">Have [!INCLUDE[pn_microsoft_visual_studio_2015](../includes/pn-microsoft-visual-studio-2015.md)] or later to run the sample.</span><span class="sxs-lookup"><span data-stu-id="79fba-111">Have [!INCLUDE[pn_microsoft_visual_studio_2015](../includes/pn-microsoft-visual-studio-2015.md)] or later to run the sample.</span></span>  

4. <span data-ttu-id="79fba-112">Have Internet connection to download the sample project and to restore the NuGet packages used in the sample project.</span><span class="sxs-lookup"><span data-stu-id="79fba-112">Have Internet connection to download the sample project and to restore the NuGet packages used in the sample project.</span></span>  

<a name="BKMK_WhatThisSampleDoes"></a>   
## <a name="what-this-sample-does"></a><span data-ttu-id="79fba-113">What this sample does</span><span class="sxs-lookup"><span data-stu-id="79fba-113">What this sample does</span></span>  

1.  <span data-ttu-id="79fba-114">Creates a sample Lead record.</span><span class="sxs-lookup"><span data-stu-id="79fba-114">Creates a sample Lead record.</span></span> <span data-ttu-id="79fba-115">This automatically creates an instance of the "Lead To Opportunity Sales Process" business process flow for the Lead record.</span><span class="sxs-lookup"><span data-stu-id="79fba-115">This automatically creates an instance of the "Lead To Opportunity Sales Process" business process flow for the Lead record.</span></span>  

2.  <span data-ttu-id="79fba-116">Converts the Lead record to an Opportunity record.</span><span class="sxs-lookup"><span data-stu-id="79fba-116">Converts the Lead record to an Opportunity record.</span></span>  


4.  <span data-ttu-id="79fba-117">Retrieves the business process flow instances associated with the "Opportunity" record using the `RetrieveProcessInstances` message.</span><span class="sxs-lookup"><span data-stu-id="79fba-117">Retrieves the business process flow instances associated with the "Opportunity" record using the `RetrieveProcessInstances` message.</span></span> <span data-ttu-id="79fba-118">The first record in the returned collection is the active business process flow  instance for the opportunity record, which is "Lead To Opportunity Sales Process" in this case.</span><span class="sxs-lookup"><span data-stu-id="79fba-118">The first record in the returned collection is the active business process flow  instance for the opportunity record, which is "Lead To Opportunity Sales Process" in this case.</span></span>  

5.  <span data-ttu-id="79fba-119">Retrieves the active path and the process stages for the "Lead To Opportunity Sales Process" instance using the `RetrieveActivePath` message.</span><span class="sxs-lookup"><span data-stu-id="79fba-119">Retrieves the active path and the process stages for the "Lead To Opportunity Sales Process" instance using the `RetrieveActivePath` message.</span></span>  

6.  <span data-ttu-id="79fba-120">Retrieves the currently active stage for the "Lead To Opportunity Sales Process" instance, and prompts the user whether to move to the next stage.</span><span class="sxs-lookup"><span data-stu-id="79fba-120">Retrieves the currently active stage for the "Lead To Opportunity Sales Process" instance, and prompts the user whether to move to the next stage.</span></span> <span data-ttu-id="79fba-121">On confirmation to move, sets the next stage in the active path as the active stage for the "Lead To Opportunity Sales Process" instance.</span><span class="sxs-lookup"><span data-stu-id="79fba-121">On confirmation to move, sets the next stage in the active path as the active stage for the "Lead To Opportunity Sales Process" instance.</span></span>  

7.  <span data-ttu-id="79fba-122">Finally, prompts the user whether to delete the records created during the sample run.</span><span class="sxs-lookup"><span data-stu-id="79fba-122">Finally, prompts the user whether to delete the records created during the sample run.</span></span>  

     <span data-ttu-id="79fba-123">Here is the output of the sample:</span><span class="sxs-lookup"><span data-stu-id="79fba-123">Here is the output of the sample:</span></span>  

    <span data-ttu-id="79fba-124">![Sample output](media/work-with-bpf-sample-output.png "Sample output")</span><span class="sxs-lookup"><span data-stu-id="79fba-124">![Sample output](media/work-with-bpf-sample-output.png "Sample output")</span></span>  

<a name="BKMK_runSample"></a>   
## <a name="run-the-sample"></a><span data-ttu-id="79fba-125">Run the sample</span><span class="sxs-lookup"><span data-stu-id="79fba-125">Run the sample</span></span>  

1. <span data-ttu-id="79fba-126">[Download](https://go.microsoft.com/fwlink/p/?LinkId=846108) the WorkWithBPF[!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] sample project, and extract it to a folder on your computer.</span><span class="sxs-lookup"><span data-stu-id="79fba-126">[Download](https://go.microsoft.com/fwlink/p/?LinkId=846108) the WorkWithBPF[!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] sample project, and extract it to a folder on your computer.</span></span>  

2. <span data-ttu-id="79fba-127">Locate the `WorkWithBPF.sln` file in your extracted folder, and open it in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="79fba-127">Locate the `WorkWithBPF.sln` file in your extracted folder, and open it in Visual Studio.</span></span>  

3. <span data-ttu-id="79fba-128">The sample project uses NuGet packages that must be restored before running the sample.</span><span class="sxs-lookup"><span data-stu-id="79fba-128">The sample project uses NuGet packages that must be restored before running the sample.</span></span> <span data-ttu-id="79fba-129">Ensure that automatic restore of NuGet packages is enabled in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="79fba-129">Ensure that automatic restore of NuGet packages is enabled in Visual Studio.</span></span> <span data-ttu-id="79fba-130">More information: [Enabling and disabling NuGet package restore](https://go.microsoft.com/fwlink/?linkid=846106)</span><span class="sxs-lookup"><span data-stu-id="79fba-130">More information: [Enabling and disabling NuGet package restore](https://go.microsoft.com/fwlink/?linkid=846106)</span></span>  

    <span data-ttu-id="79fba-131">Alternatively, select **Project** > **Manage NuGet Packages**, and select **Restore** to manually restore the packages used in the sample.</span><span class="sxs-lookup"><span data-stu-id="79fba-131">Alternatively, select **Project** > **Manage NuGet Packages**, and select **Restore** to manually restore the packages used in the sample.</span></span>  

4. <span data-ttu-id="79fba-132">Press F5 or select **Debug** > **Start Debugging**.</span><span class="sxs-lookup"><span data-stu-id="79fba-132">Press F5 or select **Debug** > **Start Debugging**.</span></span>  

5. <span data-ttu-id="79fba-133">If you have not previously run one of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement managed code samples before, you’ll need to enter information to run the code, otherwise enter the number for one of the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] servers you have previously set up.</span><span class="sxs-lookup"><span data-stu-id="79fba-133">If you have not previously run one of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement managed code samples before, you’ll need to enter information to run the code, otherwise enter the number for one of the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] servers you have previously set up.</span></span>  


   |                                 <span data-ttu-id="79fba-134">Prompt</span><span class="sxs-lookup"><span data-stu-id="79fba-134">Prompt</span></span>                                  |                                                                                             <span data-ttu-id="79fba-135">Mô tả</span><span class="sxs-lookup"><span data-stu-id="79fba-135">Description</span></span>                                                                                             |
   |-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |      <span data-ttu-id="79fba-136">Enter a Dynamics 365 for Customer Engagement server name and port [crm.dynamics.com]</span><span class="sxs-lookup"><span data-stu-id="79fba-136">Enter a Dynamics 365 for Customer Engagement server name and port [crm.dynamics.com]</span></span>       | <span data-ttu-id="79fba-137">Type the name of your Dynamics 365 for Customer Engagement server.</span><span class="sxs-lookup"><span data-stu-id="79fba-137">Type the name of your Dynamics 365 for Customer Engagement server.</span></span> <span data-ttu-id="79fba-138">The default is [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] (crm.dynamics.com) in North America.</span><span class="sxs-lookup"><span data-stu-id="79fba-138">The default is [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] (crm.dynamics.com) in North America.</span></span><br /><br /> <span data-ttu-id="79fba-139">Ví dụ: </span><span class="sxs-lookup"><span data-stu-id="79fba-139">Example:</span></span> <br /><span data-ttu-id="79fba-140">crm5.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="79fba-140">crm5.dynamics.com</span></span> |
   | <span data-ttu-id="79fba-141">Is this organization provisioned in Microsoft online services (y/n) [n]</span><span class="sxs-lookup"><span data-stu-id="79fba-141">Is this organization provisioned in Microsoft online services (y/n) [n]</span></span> |                                                 <span data-ttu-id="79fba-142">Type **y** if this is a Microsoft online services provisioned organization.</span><span class="sxs-lookup"><span data-stu-id="79fba-142">Type **y** if this is a Microsoft online services provisioned organization.</span></span> <span data-ttu-id="79fba-143">Otherwise, type **n**.</span><span class="sxs-lookup"><span data-stu-id="79fba-143">Otherwise, type **n**.</span></span>                                                  |
   |                          <span data-ttu-id="79fba-144">Enter domain\username</span><span class="sxs-lookup"><span data-stu-id="79fba-144">Enter domain\username</span></span>                          |                                                                                    <span data-ttu-id="79fba-145">Type your Microsoft account.</span><span class="sxs-lookup"><span data-stu-id="79fba-145">Type your Microsoft account.</span></span>                                                                                     |
   |                             <span data-ttu-id="79fba-146">Enter password</span><span class="sxs-lookup"><span data-stu-id="79fba-146">Enter password</span></span>                              |                      <span data-ttu-id="79fba-147">Type your password.</span><span class="sxs-lookup"><span data-stu-id="79fba-147">Type your password.</span></span> <span data-ttu-id="79fba-148">The characters will show as “\*” in the window.</span><span class="sxs-lookup"><span data-stu-id="79fba-148">The characters will show as “\*” in the window.</span></span> <span data-ttu-id="79fba-149">Your password is securely saved in the Microsoft Credential Manager for later reuse.</span><span class="sxs-lookup"><span data-stu-id="79fba-149">Your password is securely saved in the Microsoft Credential Manager for later reuse.</span></span>                       |
   |                <span data-ttu-id="79fba-150">Specify an organization number (1-n) [1]</span><span class="sxs-lookup"><span data-stu-id="79fba-150">Specify an organization number (1-n) [1]</span></span>                 |                      <span data-ttu-id="79fba-151">From the list of organizations shown that you belong to, type the corresponding number.</span><span class="sxs-lookup"><span data-stu-id="79fba-151">From the list of organizations shown that you belong to, type the corresponding number.</span></span> <span data-ttu-id="79fba-152">The default is 1, indicating the first organization in the list.</span><span class="sxs-lookup"><span data-stu-id="79fba-152">The default is 1, indicating the first organization in the list.</span></span>                       |


6. <span data-ttu-id="79fba-153">The sample will perform the operations described in [What this sample does](sample-insert-update-record-upsert.md#BKMK_WhatThisSampleDoes) and may prompt you with additional options</span><span class="sxs-lookup"><span data-stu-id="79fba-153">The sample will perform the operations described in [What this sample does](sample-insert-update-record-upsert.md#BKMK_WhatThisSampleDoes) and may prompt you with additional options</span></span>  

7. <span data-ttu-id="79fba-154">When the sample is complete, press ENTER to close the console window.</span><span class="sxs-lookup"><span data-stu-id="79fba-154">When the sample is complete, press ENTER to close the console window.</span></span>  

### <a name="see-also"></a><span data-ttu-id="79fba-155">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="79fba-155">See also</span></span>  
 [<span data-ttu-id="79fba-156">Model business process flows</span><span class="sxs-lookup"><span data-stu-id="79fba-156">Model business process flows</span></span>](model-business-process-flows.md)
