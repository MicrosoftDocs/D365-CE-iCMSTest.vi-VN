---
title: Work with solutions (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: e8da920b-9660-4f23-aa6b-841a12ea91c1
caps.latest.revision: 18
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 07ea5ece6ad77006735f7078cf348128f036185c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387575"
---
# <a name="work-with-solutions"></a><span data-ttu-id="35f33-102">Work with solutions</span><span class="sxs-lookup"><span data-stu-id="35f33-102">Work with solutions</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="35f33-103">This topic presents specific programming tasks included in [Sample: Work With Solutions](sample-work-solutions.md) and [Sample: Detect Solution Dependencies](sample-detect-solution-dependencies.md).</span><span class="sxs-lookup"><span data-stu-id="35f33-103">This topic presents specific programming tasks included in [Sample: Work With Solutions](sample-work-solutions.md) and [Sample: Detect Solution Dependencies](sample-detect-solution-dependencies.md).</span></span>  
  
<a name="BKMK_CreatePublisher"></a>

## <a name="create-a-publisher"></a><span data-ttu-id="35f33-104">Create a publisher</span><span class="sxs-lookup"><span data-stu-id="35f33-104">Create a publisher</span></span>

 <span data-ttu-id="35f33-105">Every solution requires a publisher, represented by the [Publisher Entity](entities/publisher.md).</span><span class="sxs-lookup"><span data-stu-id="35f33-105">Every solution requires a publisher, represented by the [Publisher Entity](entities/publisher.md).</span></span> <span data-ttu-id="35f33-106">A solution cannot use the `Microsoft Corporation` publisher but it can use the `Default` publisher for the organization or a new publisher</span><span class="sxs-lookup"><span data-stu-id="35f33-106">A solution cannot use the `Microsoft Corporation` publisher but it can use the `Default` publisher for the organization or a new publisher</span></span>  
  
 <span data-ttu-id="35f33-107">A publisher requires the following:</span><span class="sxs-lookup"><span data-stu-id="35f33-107">A publisher requires the following:</span></span>  
  
- <span data-ttu-id="35f33-108">A customization prefix</span><span class="sxs-lookup"><span data-stu-id="35f33-108">A customization prefix</span></span>  
  
- <span data-ttu-id="35f33-109">A unique name</span><span class="sxs-lookup"><span data-stu-id="35f33-109">A unique name</span></span>  
  
- <span data-ttu-id="35f33-110">A friendly name</span><span class="sxs-lookup"><span data-stu-id="35f33-110">A friendly name</span></span>  
  
  <span data-ttu-id="35f33-111">The following sample first defines a publisher and then checks to see whether the publisher already exists based on the unique name.</span><span class="sxs-lookup"><span data-stu-id="35f33-111">The following sample first defines a publisher and then checks to see whether the publisher already exists based on the unique name.</span></span> <span data-ttu-id="35f33-112">If it already exists, the customization prefix may have been changed, so this sample seeks to capture the current customization prefix.</span><span class="sxs-lookup"><span data-stu-id="35f33-112">If it already exists, the customization prefix may have been changed, so this sample seeks to capture the current customization prefix.</span></span> <span data-ttu-id="35f33-113">The `PublisherId` is also captured so that the publisher record can be deleted.</span><span class="sxs-lookup"><span data-stu-id="35f33-113">The `PublisherId` is also captured so that the publisher record can be deleted.</span></span> <span data-ttu-id="35f33-114">If the publisher is not found, a new publisher is created using the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.</span><span class="sxs-lookup"><span data-stu-id="35f33-114">If the publisher is not found, a new publisher is created using the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.</span></span> <span data-ttu-id="35f33-115"><xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*> phương pháp</span><span class="sxs-lookup"><span data-stu-id="35f33-115"><xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*> method</span></span>  
  
  [!code-csharp[Solutions#WorkWithSolutions1](../snippets/csharp/CRMV8/solutions/cs/workwithsolutions1.cs#workwithsolutions1)]  
  
<a name="BKMK_RetrieveDefaultPublisher"></a>   
## <a name="retrieve-the-default-publisher"></a><span data-ttu-id="35f33-116">Retrieve the default publisher</span><span class="sxs-lookup"><span data-stu-id="35f33-116">Retrieve the default publisher</span></span>  
 <span data-ttu-id="35f33-117">This sample shows how toretrieve the default publisher.</span><span class="sxs-lookup"><span data-stu-id="35f33-117">This sample shows how toretrieve the default publisher.</span></span> <span data-ttu-id="35f33-118">The default publisher has a constant GUID value: `d21aab71-79e7-11dd-8874-00188b01e34f`.</span><span class="sxs-lookup"><span data-stu-id="35f33-118">The default publisher has a constant GUID value: `d21aab71-79e7-11dd-8874-00188b01e34f`.</span></span>  
  
 [!code-csharp[Solutions#WorkWithSolutions2](../snippets/csharp/CRMV8/solutions/cs/workwithsolutions2.cs#workwithsolutions2)]  
  
<a name="BKMK_CreateASolution"></a>
 
## <a name="create-a-solution"></a><span data-ttu-id="35f33-119">Create a solution</span><span class="sxs-lookup"><span data-stu-id="35f33-119">Create a solution</span></span>

 <span data-ttu-id="35f33-120">The following sample shows how to create an unmanaged solution using the SDK Samples publisher created in [Create a Publisher](work-solutions.md#BKMK_CreatePublisher).</span><span class="sxs-lookup"><span data-stu-id="35f33-120">The following sample shows how to create an unmanaged solution using the SDK Samples publisher created in [Create a Publisher](work-solutions.md#BKMK_CreatePublisher).</span></span>  
  
 <span data-ttu-id="35f33-121">A solution requires the following:</span><span class="sxs-lookup"><span data-stu-id="35f33-121">A solution requires the following:</span></span>  
  
- <span data-ttu-id="35f33-122">A Publisher</span><span class="sxs-lookup"><span data-stu-id="35f33-122">A Publisher</span></span>  
  
- <span data-ttu-id="35f33-123">A Friendly Name</span><span class="sxs-lookup"><span data-stu-id="35f33-123">A Friendly Name</span></span>  
  
- <span data-ttu-id="35f33-124">A Unique Name</span><span class="sxs-lookup"><span data-stu-id="35f33-124">A Unique Name</span></span>  
  
- <span data-ttu-id="35f33-125">A Version Number</span><span class="sxs-lookup"><span data-stu-id="35f33-125">A Version Number</span></span>  
  
  <span data-ttu-id="35f33-126">The variable `_crmSdkPublisherId` is a GUID value representing the `publisherid` value.</span><span class="sxs-lookup"><span data-stu-id="35f33-126">The variable `_crmSdkPublisherId` is a GUID value representing the `publisherid` value.</span></span>  
  
  <span data-ttu-id="35f33-127">This sample checks whether the Solution already exists in the organization based on the unique name.</span><span class="sxs-lookup"><span data-stu-id="35f33-127">This sample checks whether the Solution already exists in the organization based on the unique name.</span></span> <span data-ttu-id="35f33-128">If the solution does not exist it is created.</span><span class="sxs-lookup"><span data-stu-id="35f33-128">If the solution does not exist it is created.</span></span> <span data-ttu-id="35f33-129">The `SolutionId` value is captured so the solution can be deleted.</span><span class="sxs-lookup"><span data-stu-id="35f33-129">The `SolutionId` value is captured so the solution can be deleted.</span></span>  
  
  [!code-csharp[Solutions#WorkWithSolutions3](../snippets/csharp/CRMV8/solutions/cs/workwithsolutions3.cs#workwithsolutions3)]
  
<a name="BKMK_RetrieveASolution"></a>   
## <a name="retrieve-a-solution"></a><span data-ttu-id="35f33-130">Retrieve a solution</span><span class="sxs-lookup"><span data-stu-id="35f33-130">Retrieve a solution</span></span>  
 <span data-ttu-id="35f33-131">To retrieve a specific solution you can use the solution’s `UniqueName`.</span><span class="sxs-lookup"><span data-stu-id="35f33-131">To retrieve a specific solution you can use the solution’s `UniqueName`.</span></span> <span data-ttu-id="35f33-132">Each organization will have a default solution with a constant GUID value: `FD140AAF-4DF4-11DD-BD17-0019B9312238`.</span><span class="sxs-lookup"><span data-stu-id="35f33-132">Each organization will have a default solution with a constant GUID value: `FD140AAF-4DF4-11DD-BD17-0019B9312238`.</span></span>  
  
 <span data-ttu-id="35f33-133">This sample shows how to retrieve data for a solution with the unique name ”samplesolution”.</span><span class="sxs-lookup"><span data-stu-id="35f33-133">This sample shows how to retrieve data for a solution with the unique name ”samplesolution”.</span></span> <span data-ttu-id="35f33-134">A solution with this name is created in [Create a Solution](work-solutions.md#BKMK_CreateASolution).</span><span class="sxs-lookup"><span data-stu-id="35f33-134">A solution with this name is created in [Create a Solution](work-solutions.md#BKMK_CreateASolution).</span></span>  
  
 [!code-csharp[Solutions#WorkWithSolutions4](../snippets/csharp/CRMV8/solutions/cs/workwithsolutions4.cs#workwithsolutions4)] 
  
<a name="BKMK_AddANewSolutionComponent"></a>   
## <a name="add-a-new-solution-component"></a><span data-ttu-id="35f33-135">Add a new solution component</span><span class="sxs-lookup"><span data-stu-id="35f33-135">Add a new solution component</span></span>  
 <span data-ttu-id="35f33-136">This sample shows how to create a solution component that is associated with a specific solution.</span><span class="sxs-lookup"><span data-stu-id="35f33-136">This sample shows how to create a solution component that is associated with a specific solution.</span></span> <span data-ttu-id="35f33-137">If you don’t associate the solution component to a specific solution when it is created it will only be added to the default solution and you will need to add it to a solution manually or by using the code included in the [Add an Existing Solution Component](work-solutions.md#BKMK_AddExistingSolutionComponent).</span><span class="sxs-lookup"><span data-stu-id="35f33-137">If you don’t associate the solution component to a specific solution when it is created it will only be added to the default solution and you will need to add it to a solution manually or by using the code included in the [Add an Existing Solution Component](work-solutions.md#BKMK_AddExistingSolutionComponent).</span></span>  
  
 <span data-ttu-id="35f33-138">This code creates a new global option set and adds it to the solution with a unique name equal to `_primarySolutionName`.</span><span class="sxs-lookup"><span data-stu-id="35f33-138">This code creates a new global option set and adds it to the solution with a unique name equal to `_primarySolutionName`.</span></span>  
  
 [!code-csharp[Solutions#GetSolutionDependencies3](../snippets/csharp/CRMV8/solutions/cs/getsolutiondependencies3.cs#getsolutiondependencies3)]  
  
<a name="BKMK_AddExistingSolutionComponent"></a>   
## <a name="add-an-existing-solution-component"></a><span data-ttu-id="35f33-139">Add an existing solution component</span><span class="sxs-lookup"><span data-stu-id="35f33-139">Add an existing solution component</span></span>  
 <span data-ttu-id="35f33-140">This sample shows how to add an existing solution component to a solution.</span><span class="sxs-lookup"><span data-stu-id="35f33-140">This sample shows how to add an existing solution component to a solution.</span></span>  
  
 <span data-ttu-id="35f33-141">The following code uses the <xref:Microsoft.Crm.Sdk.Messages.AddSolutionComponentRequest> to add the `Account` entity as a solution component to an unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="35f33-141">The following code uses the <xref:Microsoft.Crm.Sdk.Messages.AddSolutionComponentRequest> to add the `Account` entity as a solution component to an unmanaged solution.</span></span>  
  
 [!code-csharp[Solutions#WorkWithSolutions5](../snippets/csharp/CRMV8/solutions/cs/workwithsolutions5.cs#workwithsolutions5)] 
  
<a name="BKMK_RemoveSolutionComponent"></a>   
## <a name="remove-a-solution-component"></a><span data-ttu-id="35f33-142">Remove a solution component</span><span class="sxs-lookup"><span data-stu-id="35f33-142">Remove a solution component</span></span>  
 <span data-ttu-id="35f33-143">This sample shows how to remove a solution component from an unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="35f33-143">This sample shows how to remove a solution component from an unmanaged solution.</span></span> <span data-ttu-id="35f33-144">The following code uses the <xref:Microsoft.Crm.Sdk.Messages.RemoveSolutionComponentRequest> to remove an entity solution component from an unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="35f33-144">The following code uses the <xref:Microsoft.Crm.Sdk.Messages.RemoveSolutionComponentRequest> to remove an entity solution component from an unmanaged solution.</span></span> <span data-ttu-id="35f33-145">The `solution.UniqueName` references the Solution created in the [Create a Solution](work-solutions.md#BKMK_CreateASolution).</span><span class="sxs-lookup"><span data-stu-id="35f33-145">The `solution.UniqueName` references the Solution created in the [Create a Solution](work-solutions.md#BKMK_CreateASolution).</span></span>  
  
 [!code-csharp[Solutions#WorkWithSolutions6](../snippets/csharp/CRMV8/solutions/cs/workwithsolutions6.cs#workwithsolutions6)]
  
<a name="BKMK_ExportPackageSolution"></a>   
## <a name="export-or-package-a-solution"></a><span data-ttu-id="35f33-146">Export or package a solution</span><span class="sxs-lookup"><span data-stu-id="35f33-146">Export or package a solution</span></span>  
 <span data-ttu-id="35f33-147">This sample shows how to export an unmanaged solution or package a managed solution.</span><span class="sxs-lookup"><span data-stu-id="35f33-147">This sample shows how to export an unmanaged solution or package a managed solution.</span></span> <span data-ttu-id="35f33-148">The code uses <xref:Microsoft.Crm.Sdk.Messages.ExportSolutionRequest> to export a compressed file representing an unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="35f33-148">The code uses <xref:Microsoft.Crm.Sdk.Messages.ExportSolutionRequest> to export a compressed file representing an unmanaged solution.</span></span> <span data-ttu-id="35f33-149">The option to create a managed solution is set using the <xref:Microsoft.Crm.Sdk.Messages.ExportSolutionRequest.Managed> property.</span><span class="sxs-lookup"><span data-stu-id="35f33-149">The option to create a managed solution is set using the <xref:Microsoft.Crm.Sdk.Messages.ExportSolutionRequest.Managed> property.</span></span> <span data-ttu-id="35f33-150">This sample saves a file named samplesolution.zip to the `c:\temp\` folder.</span><span class="sxs-lookup"><span data-stu-id="35f33-150">This sample saves a file named samplesolution.zip to the `c:\temp\` folder.</span></span>  
  
 [!code-csharp[Solutions#WorkWithSolutions7](../snippets/csharp/CRMV8/solutions/cs/workwithsolutions7.cs#workwithsolutions7)]
  
<a name="BKMK_InstallUpgradeSolution"></a>   
## <a name="install-or-upgrade-a-solution"></a><span data-ttu-id="35f33-151">Install or upgrade a solution</span><span class="sxs-lookup"><span data-stu-id="35f33-151">Install or upgrade a solution</span></span>  
 <span data-ttu-id="35f33-152">This sample shows how to install or upgrade a solution using the <xref:Microsoft.Crm.Sdk.Messages.ImportSolutionRequest> message.</span><span class="sxs-lookup"><span data-stu-id="35f33-152">This sample shows how to install or upgrade a solution using the <xref:Microsoft.Crm.Sdk.Messages.ImportSolutionRequest> message.</span></span>  
  
 <span data-ttu-id="35f33-153">You can use the `ImportJob` entity to capture data about the success of the import.</span><span class="sxs-lookup"><span data-stu-id="35f33-153">You can use the `ImportJob` entity to capture data about the success of the import.</span></span>  
  
 <span data-ttu-id="35f33-154">The following sample shows how to import a solution without tracking the success.</span><span class="sxs-lookup"><span data-stu-id="35f33-154">The following sample shows how to import a solution without tracking the success.</span></span>  
  
 [!code-csharp[Solutions#WorkWithSolutions8](../snippets/csharp/CRMV8/solutions/cs/workwithsolutions8.cs#workwithsolutions8)] 
  
### <a name="tracking-import-success"></a><span data-ttu-id="35f33-155">Tracking import success</span><span class="sxs-lookup"><span data-stu-id="35f33-155">Tracking import success</span></span>
 <span data-ttu-id="35f33-156">When you specify an <xref:Microsoft.Crm.Sdk.Messages.ImportSolutionRequest.ImportJobId> for the `ImportSolutionRequest`, you can use that value to query the `ImportJob` entity about the status of the import.</span><span class="sxs-lookup"><span data-stu-id="35f33-156">When you specify an <xref:Microsoft.Crm.Sdk.Messages.ImportSolutionRequest.ImportJobId> for the `ImportSolutionRequest`, you can use that value to query the `ImportJob` entity about the status of the import.</span></span>  
  
 <span data-ttu-id="35f33-157">The `ImportJobId` can also be used to download an import log file using the <xref:Microsoft.Crm.Sdk.Messages.RetrieveFormattedImportJobResultsRequest> message.</span><span class="sxs-lookup"><span data-stu-id="35f33-157">The `ImportJobId` can also be used to download an import log file using the <xref:Microsoft.Crm.Sdk.Messages.RetrieveFormattedImportJobResultsRequest> message.</span></span>  
  
#### <a name="retrieving-import-job-data"></a><span data-ttu-id="35f33-158">Retrieving import job data</span><span class="sxs-lookup"><span data-stu-id="35f33-158">Retrieving import job data</span></span>

 <span data-ttu-id="35f33-159">The following sample shows how to retrieve the import job record and the content of the `ImportJob.Data` attribute.</span><span class="sxs-lookup"><span data-stu-id="35f33-159">The following sample shows how to retrieve the import job record and the content of the `ImportJob.Data` attribute.</span></span>  
  
 [!code-csharp[Solutions#WorkWithSolutions9](../snippets/csharp/CRMV8/solutions/cs/workwithsolutions9.cs#workwithsolutions9)]  
  
 <span data-ttu-id="35f33-160">The contents of the `Data` property is a string representing an XML file.</span><span class="sxs-lookup"><span data-stu-id="35f33-160">The contents of the `Data` property is a string representing an XML file.</span></span> <span data-ttu-id="35f33-161">The following is a sample captured using the code in this sample.</span><span class="sxs-lookup"><span data-stu-id="35f33-161">The following is a sample captured using the code in this sample.</span></span> <span data-ttu-id="35f33-162">This managed solution contained a single global option set called `sample_tempsampleglobaloptionsetname`.</span><span class="sxs-lookup"><span data-stu-id="35f33-162">This managed solution contained a single global option set called `sample_tempsampleglobaloptionsetname`.</span></span>  
  
```xml  
<importexportxml start="634224017519682730"  
                 stop="634224017609764033"  
                 progress="80"  
                 processed="true">  
 <solutionManifests>  
  <solutionManifest languagecode="1033"  
                    id="samplesolutionforImport"  
                    LocalizedName="Sample Solution for Import"  
                    processed="true">  
   <UniqueName>samplesolutionforImport</UniqueName>  
   <LocalizedNames>  
    <LocalizedName description="Sample Solution for Import"  
                   languagecode="1033" />  
   </LocalizedNames>  
   <Descriptions>  
    <Description description="This solution was created by the WorkWithSolutions sample code in the Microsoft CRM SDK samples."  
                 languagecode="1033" />  
   </Descriptions>  
   <Version>1.0</Version>  
   <Managed>1</Managed>  
   <Publisher>  
    <UniqueName>sdksamples</UniqueName>  
    <LocalizedNames>  
     <LocalizedName description="Microsoft CRM SDK Samples"  
                    languagecode="1033" />  
    </LocalizedNames>  
    <Descriptions>  
     <Description description="This publisher was created with samples from the Microsoft CRM SDK"  
                  languagecode="1033" />  
    </Descriptions>  
    <EMailAddress>someone@microsoft.com</EMailAddress>  
    <SupportingWebsiteUrl>http://msdn.microsoft.com/en-us/dynamics/crm/default.aspx</SupportingWebsiteUrl>  
    <Addresses>  
     <Address>  
      <City />  
      <Country />  
      <Line1 />  
      <Line2 />  
      <PostalCode />  
      <StateOrProvince />  
      <Telephone1 />  
     </Address>  
    </Addresses>  
   </Publisher>  
   <results />  
   <result result="success"  
           errorcode="0"  
           errortext=""  
           datetime="20:49:12.08"  
           datetimeticks="634224269520845122" />  
  </solutionManifest>  
 </solutionManifests>  
 <upgradeSolutionPackageInformation>  
  <upgradeRequired>0</upgradeRequired>  
  <upgradeValid>1</upgradeValid>  
  <fileVersion>5.0.9669.0</fileVersion>  
  <currentVersion>5.0.9669.0</currentVersion>  
  <fileSku>OnPremise</fileSku>  
  <currentSku>OnPremise</currentSku>  
 </upgradeSolutionPackageInformation>  
 <entities />  
 <nodes />  
 <settings />  
 <dashboards />  
 <securityroles />  
 <workflows />  
 <templates />  
 <optionSets>  
  <optionSet id="sample_tempsampleglobaloptionsetname"  
             LocalizedName="Example Option Set"  
             Description=""  
             processed="true">  
   <result result="success"  
           errorcode="0"  
           errortext=""  
           datetime="20:49:16.10"  
           datetimeticks="634224269561025400" />  
  </optionSet>  
 </optionSets>  
 <ConnectionRoles />  
 <SolutionPluginAssemblies />  
 <SdkMessageProcessingSteps />  
 <ServiceEndpoints />  
 <webResources />  
 <reports />  
 <FieldSecurityProfiles />  
 <languages>  
  <language>  
   <result result="success"  
           errorcode="0"  
           errortext=""  
           datetime="20:49:12.00"  
           datetimeticks="634224269520092986" />  
  </language>  
 </languages>  
 <entitySubhandlers />  
 <publishes>  
  <publish processed="false" />  
 </publishes>  
 <rootComponents>  
  <rootComponent processed="true">  
   <result result="success"  
           errorcode="0"  
           errortext=""  
           datetime="20:49:20.83"  
           datetimeticks="634224269608387238" />  
  </rootComponent>  
 </rootComponents>  
 <dependencies>  
  <dependency processed="true">  
   <result result="success"  
           errorcode="0"  
           errortext=""  
           datetime="20:49:20.97"  
           datetimeticks="634224269609715208" />  
  </dependency>  
 </dependencies>  
</importexportxml>  
```  
  
<a name="BKMK_DeleteSolution"></a>

## <a name="delete-a-solution"></a><span data-ttu-id="35f33-163">Delete a solution</span><span class="sxs-lookup"><span data-stu-id="35f33-163">Delete a solution</span></span>

 <span data-ttu-id="35f33-164">This sample shows how to delete a solution.The following sample shows how to retrieve a solution using the solution `uniquename` and then extract the `solutionid` from the results.</span><span class="sxs-lookup"><span data-stu-id="35f33-164">This sample shows how to delete a solution.The following sample shows how to retrieve a solution using the solution `uniquename` and then extract the `solutionid` from the results.</span></span> <span data-ttu-id="35f33-165">Use the `solutionid` with the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.</span><span class="sxs-lookup"><span data-stu-id="35f33-165">Use the `solutionid` with the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.</span></span> <span data-ttu-id="35f33-166"><xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*> method.</span><span class="sxs-lookup"><span data-stu-id="35f33-166"><xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*> method.</span></span>  
  
 [!code-csharp[Solutions#WorkWithSolutions10](../snippets/csharp/CRMV8/solutions/cs/workwithsolutions10.cs#workwithsolutions10)] 
  
<a name="BKMK_DetectSolutionDependencies"></a>

## <a name="detect-solution-dependencies"></a><span data-ttu-id="35f33-167">Detect solution dependencies</span><span class="sxs-lookup"><span data-stu-id="35f33-167">Detect solution dependencies</span></span>

 <span data-ttu-id="35f33-168">This sample shows how to create a report showing the dependencies between solution components.</span><span class="sxs-lookup"><span data-stu-id="35f33-168">This sample shows how to create a report showing the dependencies between solution components.</span></span>  
  
 <span data-ttu-id="35f33-169">This code will:</span><span class="sxs-lookup"><span data-stu-id="35f33-169">This code will:</span></span>  
  
- <span data-ttu-id="35f33-170">Retrieve all the components for a solution.</span><span class="sxs-lookup"><span data-stu-id="35f33-170">Retrieve all the components for a solution.</span></span>  
  
- <span data-ttu-id="35f33-171">Retrieve all the dependencies for each component.</span><span class="sxs-lookup"><span data-stu-id="35f33-171">Retrieve all the dependencies for each component.</span></span>  
  
- <span data-ttu-id="35f33-172">For each dependency found display a report describing the dependency.</span><span class="sxs-lookup"><span data-stu-id="35f33-172">For each dependency found display a report describing the dependency.</span></span>  
  
  [!code-csharp[Solutions#GetSolutionDependencies1](../snippets/csharp/CRMV8/solutions/cs/getsolutiondependencies1.cs#getsolutiondependencies1)]
  
  <span data-ttu-id="35f33-173">The `DependencyReport` method is in the following code sample.</span><span class="sxs-lookup"><span data-stu-id="35f33-173">The `DependencyReport` method is in the following code sample.</span></span>  
  
### <a name="dependency-report"></a><span data-ttu-id="35f33-174">Dependency report</span><span class="sxs-lookup"><span data-stu-id="35f33-174">Dependency report</span></span>

 <span data-ttu-id="35f33-175">The `DependencyReport` method provides a friendlier message based on information found within the dependency.</span><span class="sxs-lookup"><span data-stu-id="35f33-175">The `DependencyReport` method provides a friendlier message based on information found within the dependency.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="35f33-176">In this sample the method is only partially implemented.</span><span class="sxs-lookup"><span data-stu-id="35f33-176">In this sample the method is only partially implemented.</span></span> <span data-ttu-id="35f33-177">It can display messages only for attribute and option set solution components.</span><span class="sxs-lookup"><span data-stu-id="35f33-177">It can display messages only for attribute and option set solution components.</span></span>  
  
 [!code-csharp[Solutions#GetSolutionDependencies7](../snippets/csharp/CRMV8/solutions/cs/getsolutiondependencies7.cs#getsolutiondependencies7)]
  
  
### <a name="detect-whether-a-solution-component-may-be-delete"></a><span data-ttu-id="35f33-178">Detect whether a solution component may be delete</span><span class="sxs-lookup"><span data-stu-id="35f33-178">Detect whether a solution component may be delete</span></span>

 <span data-ttu-id="35f33-179">Use the <xref:Microsoft.Crm.Sdk.Messages.RetrieveDependenciesForDeleteRequest> message to identify any other solution components which would prevent a given solution component from being deleted.</span><span class="sxs-lookup"><span data-stu-id="35f33-179">Use the <xref:Microsoft.Crm.Sdk.Messages.RetrieveDependenciesForDeleteRequest> message to identify any other solution components which would prevent a given solution component from being deleted.</span></span> <span data-ttu-id="35f33-180">The following code sample looks for any attributes using a known global optionset.</span><span class="sxs-lookup"><span data-stu-id="35f33-180">The following code sample looks for any attributes using a known global optionset.</span></span> <span data-ttu-id="35f33-181">Any attribute using the global optionset would prevent the global optionset from being deleted.</span><span class="sxs-lookup"><span data-stu-id="35f33-181">Any attribute using the global optionset would prevent the global optionset from being deleted.</span></span>  
  
 [!code-csharp[Solutions#GetSolutionDependencies8](../snippets/csharp/CRMV8/solutions/cs/getsolutiondependencies8.cs#getsolutiondependencies8)]

### <a name="see-also"></a><span data-ttu-id="35f33-182">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="35f33-182">See also</span></span>

 <span data-ttu-id="35f33-183">[Package and Distribute Extensions with Dynamics 365 for Customer Engagement Solutions](package-distribute-extensions-use-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="35f33-183">[Package and Distribute Extensions with Dynamics 365 for Customer Engagement Solutions](package-distribute-extensions-use-solutions.md) </span></span>  
 <span data-ttu-id="35f33-184">[Introduction to Solutions](introduction-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="35f33-184">[Introduction to Solutions](introduction-solutions.md) </span></span>  
 <span data-ttu-id="35f33-185">[Plan For Solution Development](plan-solution-development.md) </span><span class="sxs-lookup"><span data-stu-id="35f33-185">[Plan For Solution Development](plan-solution-development.md) </span></span>  
 <span data-ttu-id="35f33-186">[Dependency Tracking for Solution Components](dependency-tracking-solution-components.md) </span><span class="sxs-lookup"><span data-stu-id="35f33-186">[Dependency Tracking for Solution Components](dependency-tracking-solution-components.md) </span></span>  
 <span data-ttu-id="35f33-187">[Create, Export, or Import an Unmanaged Solution](create-export-import-unmanaged-solution.md) </span><span class="sxs-lookup"><span data-stu-id="35f33-187">[Create, Export, or Import an Unmanaged Solution](create-export-import-unmanaged-solution.md) </span></span>  
 <span data-ttu-id="35f33-188">[Create, Install, and Update a Managed Solution](create-install-update-managed-solution.md) </span><span class="sxs-lookup"><span data-stu-id="35f33-188">[Create, Install, and Update a Managed Solution](create-install-update-managed-solution.md) </span></span>  
 <span data-ttu-id="35f33-189">[Uninstall or Delete a solution](uninstall-delete-solution.md) </span><span class="sxs-lookup"><span data-stu-id="35f33-189">[Uninstall or Delete a solution](uninstall-delete-solution.md) </span></span>  
 <span data-ttu-id="35f33-190">[Solution Entities](solution-entities.md) </span><span class="sxs-lookup"><span data-stu-id="35f33-190">[Solution Entities](solution-entities.md) </span></span>  
 <span data-ttu-id="35f33-191">[Sample: Work With Solutions](sample-work-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="35f33-191">[Sample: Work With Solutions](sample-work-solutions.md) </span></span>  
 [<span data-ttu-id="35f33-192">Sample: Detect Solution Dependencies</span><span class="sxs-lookup"><span data-stu-id="35f33-192">Sample: Detect Solution Dependencies</span></span>](sample-detect-solution-dependencies.md)
