---
title: 'Step 4: Create an AppSource package for your app (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs'
description: Learn about how to create an AppSource package (.zip file) to include your solution and demo data files along with other required files.
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 64ca3ef3-0bfe-4c92-8f28-fb8b61ecb6c0
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 516ae408df00e9c86c61f5a369058ab6e3dccbb0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388825"
---
# <a name="step-4-create-an-appsource-package-for-your-app"></a><span data-ttu-id="8d2be-103">Step 4: Create an AppSource package for your app</span><span class="sxs-lookup"><span data-stu-id="8d2be-103">Step 4: Create an AppSource package for your app</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="8d2be-104">You must create an AppSource package (.zip file) to include your solution and demo data files along with other required files.</span><span class="sxs-lookup"><span data-stu-id="8d2be-104">You must create an AppSource package (.zip file) to include your solution and demo data files along with other required files.</span></span> <span data-ttu-id="8d2be-105">An AppSource package consists of the following files:</span><span class="sxs-lookup"><span data-stu-id="8d2be-105">An AppSource package consists of the following files:</span></span>

|<span data-ttu-id="8d2be-106">File</span><span class="sxs-lookup"><span data-stu-id="8d2be-106">File</span></span>|<span data-ttu-id="8d2be-107">Mô tả</span><span class="sxs-lookup"><span data-stu-id="8d2be-107">Description</span></span>|
|--|--|
|<span data-ttu-id="8d2be-108">Package file</span><span class="sxs-lookup"><span data-stu-id="8d2be-108">Package file</span></span>|<span data-ttu-id="8d2be-109">A package file used by Package Deployer tool to deploy your solutions and demo configuration data into multiple languages.</span><span class="sxs-lookup"><span data-stu-id="8d2be-109">A package file used by Package Deployer tool to deploy your solutions and demo configuration data into multiple languages.</span></span>|
|<span data-ttu-id="8d2be-110">[Content_Types].xml</span><span class="sxs-lookup"><span data-stu-id="8d2be-110">[Content_Types].xml</span></span>|<span data-ttu-id="8d2be-111">File that provides MIME type information of the file type extensions included in the AppSource package.</span><span class="sxs-lookup"><span data-stu-id="8d2be-111">File that provides MIME type information of the file type extensions included in the AppSource package.</span></span> <span data-ttu-id="8d2be-112">Typically, these are .config, .dll, .exe, .xml, and .zip file types, but you can add almost any file type that is supported by Windows.</span><span class="sxs-lookup"><span data-stu-id="8d2be-112">Typically, these are .config, .dll, .exe, .xml, and .zip file types, but you can add almost any file type that is supported by Windows.</span></span>|
|<span data-ttu-id="8d2be-113">Icon file</span><span class="sxs-lookup"><span data-stu-id="8d2be-113">Icon file</span></span>|<span data-ttu-id="8d2be-114">An image file for the appsource package icon; size should be 32x32 pixels.</span><span class="sxs-lookup"><span data-stu-id="8d2be-114">An image file for the appsource package icon; size should be 32x32 pixels.</span></span> <span data-ttu-id="8d2be-115">Valid image formats are PNG and JPG.</span><span class="sxs-lookup"><span data-stu-id="8d2be-115">Valid image formats are PNG and JPG.</span></span>|
|<span data-ttu-id="8d2be-116">Tệp HTML</span><span class="sxs-lookup"><span data-stu-id="8d2be-116">HTML file</span></span>|<span data-ttu-id="8d2be-117">File containing your License terms.</span><span class="sxs-lookup"><span data-stu-id="8d2be-117">File containing your License terms.</span></span>|
|<span data-ttu-id="8d2be-118">input.xml</span><span class="sxs-lookup"><span data-stu-id="8d2be-118">input.xml</span></span>|<span data-ttu-id="8d2be-119">Files that describes the assets in your AppSource package.</span><span class="sxs-lookup"><span data-stu-id="8d2be-119">Files that describes the assets in your AppSource package.</span></span>|


## <a name="create-a-package-file"></a><span data-ttu-id="8d2be-120">Create a Package file</span><span class="sxs-lookup"><span data-stu-id="8d2be-120">Create a Package file</span></span>

<span data-ttu-id="8d2be-121">A package lets you bundle and deploy multiple files related to your app at once.</span><span class="sxs-lookup"><span data-stu-id="8d2be-121">A package lets you bundle and deploy multiple files related to your app at once.</span></span> 

1. <span data-ttu-id="8d2be-122">Create a Dynamics 365 for Customer Engagement apps package to include the solution and configuration data files that you created in [Step 2: Create a managed solution for your app](create-solution-app-appsource.md).</span><span class="sxs-lookup"><span data-stu-id="8d2be-122">Create a Dynamics 365 for Customer Engagement apps package to include the solution and configuration data files that you created in [Step 2: Create a managed solution for your app](create-solution-app-appsource.md).</span></span> <span data-ttu-id="8d2be-123">A package can also contain custom code that can run before, while, or after the package is deployed to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance.</span><span class="sxs-lookup"><span data-stu-id="8d2be-123">A package can also contain custom code that can run before, while, or after the package is deployed to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance.</span></span> <span data-ttu-id="8d2be-124">For more information about creating a package file, see [Create packages for the Dynamics 365 for Customer Engagement Package deployer](create-packages-package-deployer.md).</span><span class="sxs-lookup"><span data-stu-id="8d2be-124">For more information about creating a package file, see [Create packages for the Dynamics 365 for Customer Engagement Package deployer](create-packages-package-deployer.md).</span></span>

    <span data-ttu-id="8d2be-125">After you have created a package, your package will consist of the following things:</span><span class="sxs-lookup"><span data-stu-id="8d2be-125">After you have created a package, your package will consist of the following things:</span></span>

    - <span data-ttu-id="8d2be-126">**\<PackageName> folder**: This folder contains  all solutions,  configuration data, flat files, and the contents for your package.</span><span class="sxs-lookup"><span data-stu-id="8d2be-126">**\<PackageName> folder**: This folder contains  all solutions,  configuration data, flat files, and the contents for your package.</span></span> <span data-ttu-id="8d2be-127">For example: **PkgFolder**.</span><span class="sxs-lookup"><span data-stu-id="8d2be-127">For example: **PkgFolder**.</span></span>  
  
    - <span data-ttu-id="8d2be-128">**\<PackageName>.dll**: The assembly contains the custom code for your package.</span><span class="sxs-lookup"><span data-stu-id="8d2be-128">**\<PackageName>.dll**: The assembly contains the custom code for your package.</span></span> <span data-ttu-id="8d2be-129">For example: **SamplePackage.dll**.</span><span class="sxs-lookup"><span data-stu-id="8d2be-129">For example: **SamplePackage.dll**.</span></span>

2. <span data-ttu-id="8d2be-130">Next, create a **[Content_Types].xml** file that provides MIME type information of the file type extensions that are included in your package.</span><span class="sxs-lookup"><span data-stu-id="8d2be-130">Next, create a **[Content_Types].xml** file that provides MIME type information of the file type extensions that are included in your package.</span></span> <span data-ttu-id="8d2be-131">This is separate from the one that will be included again in the AppSource package.</span><span class="sxs-lookup"><span data-stu-id="8d2be-131">This is separate from the one that will be included again in the AppSource package.</span></span> <span data-ttu-id="8d2be-132">Here is the sample contents of a Content_Types].xml file with file types listed:</span><span class="sxs-lookup"><span data-stu-id="8d2be-132">Here is the sample contents of a Content_Types].xml file with file types listed:</span></span>

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <Types xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
      <Default Extension="xml" ContentType="application/octet-stream" />
      <Default Extension="xaml" ContentType="application/octet-stream" />
      <Default Extension="dll" ContentType="application/octet-stream" />
      <Default Extension="zip" ContentType="application/octet-stream" />
      <Default Extension="jpg" ContentType="application/octet-stream" />
      <Default Extension="gif" ContentType="application/octet-stream" />
      <Default Extension="png" ContentType="application/octet-stream" />
      <Default Extension="htm" ContentType="application/octet-stream" />
      <Default Extension="html" ContentType="application/octet-stream" />
      <Default Extension="db" ContentType="application/octet-stream" />
      <Default Extension="css" ContentType="application/octet-stream" />
    </Types>
    ```

3. <span data-ttu-id="8d2be-133">Compress (zip) the following files into a file called *package.zip*:</span><span class="sxs-lookup"><span data-stu-id="8d2be-133">Compress (zip) the following files into a file called *package.zip*:</span></span>
   - <span data-ttu-id="8d2be-134">package folder (PkgFolder)</span><span class="sxs-lookup"><span data-stu-id="8d2be-134">package folder (PkgFolder)</span></span>
   - <span data-ttu-id="8d2be-135">package dll (SamplePackage.dll)</span><span class="sxs-lookup"><span data-stu-id="8d2be-135">package dll (SamplePackage.dll)</span></span>
   - <span data-ttu-id="8d2be-136">[Content_Types].xml</span><span class="sxs-lookup"><span data-stu-id="8d2be-136">[Content_Types].xml</span></span>

     <span data-ttu-id="8d2be-137">To compress these files, browse to the folder where these files are present, select them all, right-click and select **Send to** > **Compressed (zipped) folder**.</span><span class="sxs-lookup"><span data-stu-id="8d2be-137">To compress these files, browse to the folder where these files are present, select them all, right-click and select **Send to** > **Compressed (zipped) folder**.</span></span>

     ![Zip the files for a package](media/appsource-zip-package.png) 

4. <span data-ttu-id="8d2be-139">Rename the .zip file to **package.zip**.</span><span class="sxs-lookup"><span data-stu-id="8d2be-139">Rename the .zip file to **package.zip**.</span></span>

## <a name="create-contenttypesxml"></a><span data-ttu-id="8d2be-140">Create [Content_Types].xml</span><span class="sxs-lookup"><span data-stu-id="8d2be-140">Create [Content_Types].xml</span></span>

<span data-ttu-id="8d2be-141">You can reuse the **[Content_Types].xml** that you created in the previous section under step 2.</span><span class="sxs-lookup"><span data-stu-id="8d2be-141">You can reuse the **[Content_Types].xml** that you created in the previous section under step 2.</span></span>

## <a name="create-an-icon-for-your-appsource-package"></a><span data-ttu-id="8d2be-142">Create an icon for your AppSource package</span><span class="sxs-lookup"><span data-stu-id="8d2be-142">Create an icon for your AppSource package</span></span>

<span data-ttu-id="8d2be-143">Create an icon file of size 32x32 to display along with the preferred solution name and description in the Dynamics 365 for Customer Engagement apps Administration Center portal.</span><span class="sxs-lookup"><span data-stu-id="8d2be-143">Create an icon file of size 32x32 to display along with the preferred solution name and description in the Dynamics 365 for Customer Engagement apps Administration Center portal.</span></span> <span data-ttu-id="8d2be-144">Valid file formats are PNG and JPG.</span><span class="sxs-lookup"><span data-stu-id="8d2be-144">Valid file formats are PNG and JPG.</span></span>

## <a name="create-an-html-file-for-license-terms"></a><span data-ttu-id="8d2be-145">Create an HTML file for license terms</span><span class="sxs-lookup"><span data-stu-id="8d2be-145">Create an HTML file for license terms</span></span>

<span data-ttu-id="8d2be-146">Create an HTML file containing your license terms.</span><span class="sxs-lookup"><span data-stu-id="8d2be-146">Create an HTML file containing your license terms.</span></span> <span data-ttu-id="8d2be-147">You can have an HTML file per language to display the license terms in the user selected language if your app supports multiple languages.</span><span class="sxs-lookup"><span data-stu-id="8d2be-147">You can have an HTML file per language to display the license terms in the user selected language if your app supports multiple languages.</span></span>

## <a name="create-inputxml-file"></a><span data-ttu-id="8d2be-148">Create input.xml file</span><span class="sxs-lookup"><span data-stu-id="8d2be-148">Create input.xml file</span></span>

<span data-ttu-id="8d2be-149">Create an *input.xml* file that provides information about your package and the contents of the package.</span><span class="sxs-lookup"><span data-stu-id="8d2be-149">Create an *input.xml* file that provides information about your package and the contents of the package.</span></span> <span data-ttu-id="8d2be-150">Here is the contents of a sample **input.xml** file; each element is explained later in the table.</span><span class="sxs-lookup"><span data-stu-id="8d2be-150">Here is the contents of a sample **input.xml** file; each element is explained later in the table.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<PvsPackageData>
  <ProviderName>Microsoft</ProviderName>
  <PackageFile>package.zip</PackageFile>
  <SolutionAnchorName>SampleSolution.zip</SolutionAnchorName>
  <StartDate>12/01/2017</StartDate>
  <EndDate>01/01/2021</EndDate>
  <SupportedCountries>US,CA</SupportedCountries>
  <LearnMoreLink>http://www.microsoft.com</LearnMoreLink>
  <Locales>
    <PackageLocale Code="1033" IsDefault="true">
      <Logo>logo32x32.png</Logo>
      <Terms>
        <PackageTerm File="TermsOfUse.html" />
      </Terms>
    </PackageLocale>
  </Locales>
</PvsPackageData>
```


<span data-ttu-id="8d2be-151">Here is a description of the elements in the **input.xml** file.</span><span class="sxs-lookup"><span data-stu-id="8d2be-151">Here is a description of the elements in the **input.xml** file.</span></span>

|<span data-ttu-id="8d2be-152">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="8d2be-152">Element</span></span>|<span data-ttu-id="8d2be-153">Mô tả</span><span class="sxs-lookup"><span data-stu-id="8d2be-153">Description</span></span>|
|--|--|
|<span data-ttu-id="8d2be-154">ProviderName</span><span class="sxs-lookup"><span data-stu-id="8d2be-154">ProviderName</span></span>|<span data-ttu-id="8d2be-155">Name of the solution provider.</span><span class="sxs-lookup"><span data-stu-id="8d2be-155">Name of the solution provider.</span></span> <span data-ttu-id="8d2be-156">If created by a Microsoft internal team, specify **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="8d2be-156">If created by a Microsoft internal team, specify **Microsoft**.</span></span>|
|<span data-ttu-id="8d2be-157">PackageFile</span><span class="sxs-lookup"><span data-stu-id="8d2be-157">PackageFile</span></span>|<span data-ttu-id="8d2be-158">Name of package (.zip file) for the Package Deployer tool.</span><span class="sxs-lookup"><span data-stu-id="8d2be-158">Name of package (.zip file) for the Package Deployer tool.</span></span> <span data-ttu-id="8d2be-159">This zip file should contain the package assembly, the package folder with your app assets, and the Content_Types.xml file.</span><span class="sxs-lookup"><span data-stu-id="8d2be-159">This zip file should contain the package assembly, the package folder with your app assets, and the Content_Types.xml file.</span></span> <span data-ttu-id="8d2be-160">For example, the package.zip file created under the [Create a Package file](#create-a-package-file) section.</span><span class="sxs-lookup"><span data-stu-id="8d2be-160">For example, the package.zip file created under the [Create a Package file](#create-a-package-file) section.</span></span>|
|<span data-ttu-id="8d2be-161">SolutionAnchorName</span><span class="sxs-lookup"><span data-stu-id="8d2be-161">SolutionAnchorName</span></span>|<span data-ttu-id="8d2be-162">Name of the solution zip file in the package that is use for the display name and description of solution assets.</span><span class="sxs-lookup"><span data-stu-id="8d2be-162">Name of the solution zip file in the package that is use for the display name and description of solution assets.</span></span>|
|<span data-ttu-id="8d2be-163">SolutionAnchorName</span><span class="sxs-lookup"><span data-stu-id="8d2be-163">SolutionAnchorName</span></span>|<span data-ttu-id="8d2be-164">Name of the solution zip file in the package that is use for the display name and description of solution assets.</span><span class="sxs-lookup"><span data-stu-id="8d2be-164">Name of the solution zip file in the package that is use for the display name and description of solution assets.</span></span>|
|<span data-ttu-id="8d2be-165">StartDate</span><span class="sxs-lookup"><span data-stu-id="8d2be-165">StartDate</span></span>|<span data-ttu-id="8d2be-166">Date on which the app becomes available on AppSource.</span><span class="sxs-lookup"><span data-stu-id="8d2be-166">Date on which the app becomes available on AppSource.</span></span> <span data-ttu-id="8d2be-167">The format is MM/DD/YYYY.</span><span class="sxs-lookup"><span data-stu-id="8d2be-167">The format is MM/DD/YYYY.</span></span>|
|<span data-ttu-id="8d2be-168">EndDate</span><span class="sxs-lookup"><span data-stu-id="8d2be-168">EndDate</span></span>|<span data-ttu-id="8d2be-169">Date on which the app stops being available on AppSource.</span><span class="sxs-lookup"><span data-stu-id="8d2be-169">Date on which the app stops being available on AppSource.</span></span> <span data-ttu-id="8d2be-170">The format is MM/DD/YYYY.</span><span class="sxs-lookup"><span data-stu-id="8d2be-170">The format is MM/DD/YYYY.</span></span>|
|<span data-ttu-id="8d2be-171">SupportedCountries</span><span class="sxs-lookup"><span data-stu-id="8d2be-171">SupportedCountries</span></span>|<span data-ttu-id="8d2be-172">This is a comma-separated list of countries or regions where the app should be available.</span><span class="sxs-lookup"><span data-stu-id="8d2be-172">This is a comma-separated list of countries or regions where the app should be available.</span></span> <span data-ttu-id="8d2be-173">At the time of writing this article, the supported countries list is the following: AE,AL,AM,AO,AR,AT,AU,AZ,BA,BB,BD,BE,BG,BH,BM,BN,BO,BR,BY,CA,CH,CI,CL,CM,CO,CR,CV,CW,CY,CZ,DE,DK,DO,DZ,EC,EE,EG,ES,FI,FR,GB,GE,GH,GR,GT,HK,HN,HR,HU,ID,IE,IL,IN,IQ,IS,IT,JM,JO,JP,KE,KG,KN,KR,KW,KY,KZ,LB,LK,LT,LU,LV,LY,MA,MC,MD,ME,MK,MN,MO,MT,MU,MX,MY,NG,NI,NL,NO,NZ,OM,PA,PE,PH,PK,PL,PR,PS,PT,PY,QA,RO,RS,RU,RW,SA,SE,SG,SI,SK,SN,SV,TH,TM,TN,TR,TT,TW,UA,US,UY,UZ,VE,VI,VN,ZA,ZW</span><span class="sxs-lookup"><span data-stu-id="8d2be-173">At the time of writing this article, the supported countries list is the following: AE,AL,AM,AO,AR,AT,AU,AZ,BA,BB,BD,BE,BG,BH,BM,BN,BO,BR,BY,CA,CH,CI,CL,CM,CO,CR,CV,CW,CY,CZ,DE,DK,DO,DZ,EC,EE,EG,ES,FI,FR,GB,GE,GH,GR,GT,HK,HN,HR,HU,ID,IE,IL,IN,IQ,IS,IT,JM,JO,JP,KE,KG,KN,KR,KW,KY,KZ,LB,LK,LT,LU,LV,LY,MA,MC,MD,ME,MK,MN,MO,MT,MU,MX,MY,NG,NI,NL,NO,NZ,OM,PA,PE,PH,PK,PL,PR,PS,PT,PY,QA,RO,RS,RU,RW,SA,SE,SG,SI,SK,SN,SV,TH,TM,TN,TR,TT,TW,UA,US,UY,UZ,VE,VI,VN,ZA,ZW</span></span>|
|<span data-ttu-id="8d2be-174">LearnMoreLink</span><span class="sxs-lookup"><span data-stu-id="8d2be-174">LearnMoreLink</span></span>|<span data-ttu-id="8d2be-175">URL to the detailed information page for this package.</span><span class="sxs-lookup"><span data-stu-id="8d2be-175">URL to the detailed information page for this package.</span></span>|
|<span data-ttu-id="8d2be-176">Locales</span><span class="sxs-lookup"><span data-stu-id="8d2be-176">Locales</span></span>|<span data-ttu-id="8d2be-177">An instance of this node for each language you want to support in the Preferred solution UI.</span><span class="sxs-lookup"><span data-stu-id="8d2be-177">An instance of this node for each language you want to support in the Preferred solution UI.</span></span> <span data-ttu-id="8d2be-178">This node contains the following children elements:</span><span class="sxs-lookup"><span data-stu-id="8d2be-178">This node contains the following children elements:</span></span><br/><span data-ttu-id="8d2be-179">- **PackageLocale.Code**: LCID of the language for this node.</span><span class="sxs-lookup"><span data-stu-id="8d2be-179">- **PackageLocale.Code**: LCID of the language for this node.</span></span> <span data-ttu-id="8d2be-180">Example: US English is 1033</span><span class="sxs-lookup"><span data-stu-id="8d2be-180">Example: US English is 1033</span></span><br/><span data-ttu-id="8d2be-181">- **PackageLocale.IsDefault**: Indicates the default language.</span><span class="sxs-lookup"><span data-stu-id="8d2be-181">- **PackageLocale.IsDefault**: Indicates the default language.</span></span> <span data-ttu-id="8d2be-182">This is used as the fallback language if the language chosen by the customer is not available.</span><span class="sxs-lookup"><span data-stu-id="8d2be-182">This is used as the fallback language if the language chosen by the customer is not available.</span></span><br/><span data-ttu-id="8d2be-183">- **Logo**: Logo for your app package.</span><span class="sxs-lookup"><span data-stu-id="8d2be-183">- **Logo**: Logo for your app package.</span></span> <span data-ttu-id="8d2be-184">Size of the image must be 32x32.</span><span class="sxs-lookup"><span data-stu-id="8d2be-184">Size of the image must be 32x32.</span></span> <span data-ttu-id="8d2be-185">Valid image formats are PNG and JPG.</span><span class="sxs-lookup"><span data-stu-id="8d2be-185">Valid image formats are PNG and JPG.</span></span><br/><span data-ttu-id="8d2be-186">- **Terms**: Name of the HTML file that contains your license terms for each language.</span><span class="sxs-lookup"><span data-stu-id="8d2be-186">- **Terms**: Name of the HTML file that contains your license terms for each language.</span></span>|

## <a name="add-the-items-to-an-appsource-package"></a><span data-ttu-id="8d2be-187">Add the items to an AppSource package</span><span class="sxs-lookup"><span data-stu-id="8d2be-187">Add the items to an AppSource package</span></span>

<span data-ttu-id="8d2be-188">The final step is to add all the components that you created earlier into a single compressed (zip) file, which will be your app source package.</span><span class="sxs-lookup"><span data-stu-id="8d2be-188">The final step is to add all the components that you created earlier into a single compressed (zip) file, which will be your app source package.</span></span>

1. <span data-ttu-id="8d2be-189">Navigate to the folder that contains the package file, [Content_Types].xml, icon, license terms file (HTML), select them all, right-click and then select **Send to** > **Compressed (zipped) folder**.</span><span class="sxs-lookup"><span data-stu-id="8d2be-189">Navigate to the folder that contains the package file, [Content_Types].xml, icon, license terms file (HTML), select them all, right-click and then select **Send to** > **Compressed (zipped) folder**.</span></span>

    ![AppSource package](media/appsource-package.png)

    > [!IMPORTANT]
    > <span data-ttu-id="8d2be-191">You must follow the content structure precisely for your package as described here otherwise, your package will fail during certification.</span><span class="sxs-lookup"><span data-stu-id="8d2be-191">You must follow the content structure precisely for your package as described here otherwise, your package will fail during certification.</span></span> <span data-ttu-id="8d2be-192">Some common issues that lead to certification failure are incorrect file names or a nested file structure.</span><span class="sxs-lookup"><span data-stu-id="8d2be-192">Some common issues that lead to certification failure are incorrect file names or a nested file structure.</span></span>

2. <span data-ttu-id="8d2be-193">Rename the file appropriately as per your app.</span><span class="sxs-lookup"><span data-stu-id="8d2be-193">Rename the file appropriately as per your app.</span></span> <span data-ttu-id="8d2be-194">We recommend that you include your company name and app name.</span><span class="sxs-lookup"><span data-stu-id="8d2be-194">We recommend that you include your company name and app name.</span></span> <span data-ttu-id="8d2be-195">For example: **Microsoft_SamplePackage.zip**.</span><span class="sxs-lookup"><span data-stu-id="8d2be-195">For example: **Microsoft_SamplePackage.zip**.</span></span>
 

> [!div class="nextstepaction"]
> [<span data-ttu-id="8d2be-196">Step 5: Store your AppSource Package on Azure Storage</span><span class="sxs-lookup"><span data-stu-id="8d2be-196">Step 5: Store your AppSource Package on Azure Storage</span></span>](store-appsource-package-azure-storage.md) 
  

