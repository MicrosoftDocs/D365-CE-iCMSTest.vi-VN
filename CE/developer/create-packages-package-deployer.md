---
title: Create packages for the Dynamics 365 for Customer Engagement Package deployer (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 8def31d9-ee2a-4527-a29a-f16b53fc9229
caps.latest.revision: 59
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6cba3d2f18dda7b4c1fd76d1727846466e246124
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386979"
---
# <a name="create-packages-for-the-dynamics-365-for-customer-engagement-package-deployer"></a><span data-ttu-id="cc626-102">Create packages for the Dynamics 365 for Customer Engagement Package deployer</span><span class="sxs-lookup"><span data-stu-id="cc626-102">Create packages for the Dynamics 365 for Customer Engagement Package deployer</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_package_deployer_long](../includes/pn-package-deployer-long.md)] <span data-ttu-id="cc626-103">lets administrators       deploy packages on [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps and [!INCLUDE[pn_crm_op_edition](../includes/pn-crm-onprem.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="cc626-103">lets administrators       deploy packages on [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps and [!INCLUDE[pn_crm_op_edition](../includes/pn-crm-onprem.md)] apps instance.</span></span> <span data-ttu-id="cc626-104">Một "gói" có thể bao gồm bất kỳ hoặc tất cả những điều sau đây:</span><span class="sxs-lookup"><span data-stu-id="cc626-104">A “package” can consist of any or all of the following:</span></span>  

- <span data-ttu-id="cc626-105">Một hoặc nhiều tệp giải pháp ứng dụng [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="cc626-105">One or more [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps solution files.</span></span>  

- <span data-ttu-id="cc626-106">Flat files or exported configuration data file from the Configuration Migration tool.</span><span class="sxs-lookup"><span data-stu-id="cc626-106">Flat files or exported configuration data file from the Configuration Migration tool.</span></span> <span data-ttu-id="cc626-107">For more information about the tool, see [Manage your configuration data](https://technet.microsoft.com/library/dn647421.aspx).</span><span class="sxs-lookup"><span data-stu-id="cc626-107">For more information about the tool, see [Manage your configuration data](https://technet.microsoft.com/library/dn647421.aspx).</span></span>  

- <span data-ttu-id="cc626-108">Custom code that can run before, while, or after the package is deployed to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="cc626-108">Custom code that can run before, while, or after the package is deployed to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span></span>  

- <span data-ttu-id="cc626-109">HTML content specific to the package that can display at the beginning and end of the deployment process.</span><span class="sxs-lookup"><span data-stu-id="cc626-109">HTML content specific to the package that can display at the beginning and end of the deployment process.</span></span> <span data-ttu-id="cc626-110">Điều này có thể hữu ích để cung cấp một mô tả về các giải pháp và tập tin đã được triển khai trong gói.</span><span class="sxs-lookup"><span data-stu-id="cc626-110">This can be useful to provide a description of the solutions and files that are deployed in the package.</span></span>  

[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)] 

[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="cc626-111">apps provide you with a [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] template for creating these packages that can be used with the Package Deployer tool to deploy them to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="cc626-111">apps provide you with a [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] template for creating these packages that can be used with the Package Deployer tool to deploy them to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span></span>

<a name="Prereq"></a>   
## <a name="prerequisites"></a><span data-ttu-id="cc626-112">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="cc626-112">Prerequisites</span></span>  

- <span data-ttu-id="cc626-113">Ensure that you have all the solutions and files ready that you want to include in the package.</span><span class="sxs-lookup"><span data-stu-id="cc626-113">Ensure that you have all the solutions and files ready that you want to include in the package.</span></span>  

- [!INCLUDE[pn_NET_Framework_452_long](../includes/pn-net-framework-452-long.md)]  

- [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)]<span data-ttu-id="cc626-114">, [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]</span><span class="sxs-lookup"><span data-stu-id="cc626-114">, [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]</span></span>  

- [!INCLUDE[tn_nuget_package_manager](../includes/tn-nuget-package-manager.md)] <span data-ttu-id="cc626-115">for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)</span><span class="sxs-lookup"><span data-stu-id="cc626-115">for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)</span></span>  

- <span data-ttu-id="cc626-116">Microsoft Dynamics 365 for Customer Engagement apps SDK Templates for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contains the package template.</span><span class="sxs-lookup"><span data-stu-id="cc626-116">Microsoft Dynamics 365 for Customer Engagement apps SDK Templates for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contains the package template.</span></span> <span data-ttu-id="cc626-117">You can get it by downloading the [Microsoft Dynamics 365 for Customer Engagement apps SDK Templates](http://go.microsoft.com/fwlink/p/?LinkId=400925) and double-click the `CRMSDKTemplates.vsix` file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span><span class="sxs-lookup"><span data-stu-id="cc626-117">You can get it by downloading the [Microsoft Dynamics 365 for Customer Engagement apps SDK Templates](http://go.microsoft.com/fwlink/p/?LinkId=400925) and double-click the `CRMSDKTemplates.vsix` file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span></span>  



<a name="HowTo"></a>   
## <a name="create-a-package"></a><span data-ttu-id="cc626-118">Create a package</span><span class="sxs-lookup"><span data-stu-id="cc626-118">Create a package</span></span>  
 <span data-ttu-id="cc626-119">Perform the following five steps to create a package:</span><span class="sxs-lookup"><span data-stu-id="cc626-119">Perform the following five steps to create a package:</span></span>  

 [<span data-ttu-id="cc626-120">Step 1: Create a project using the template</span><span class="sxs-lookup"><span data-stu-id="cc626-120">Step 1: Create a project using the template</span></span>](create-packages-package-deployer.md#Step1)  

 [<span data-ttu-id="cc626-121">Step 2: Add your files to the project</span><span class="sxs-lookup"><span data-stu-id="cc626-121">Step 2: Add your files to the project</span></span>](create-packages-package-deployer.md#Step2)  

 [<span data-ttu-id="cc626-122">Step 3: Update the HTML files</span><span class="sxs-lookup"><span data-stu-id="cc626-122">Step 3: Update the HTML files</span></span>](create-packages-package-deployer.md#Step3)  

 [<span data-ttu-id="cc626-123">Step 4: Specify the configuration values for the package</span><span class="sxs-lookup"><span data-stu-id="cc626-123">Step 4: Specify the configuration values for the package</span></span>](create-packages-package-deployer.md#Step4)  

 [<span data-ttu-id="cc626-124">Step 5: Define custom code for your package</span><span class="sxs-lookup"><span data-stu-id="cc626-124">Step 5: Define custom code for your package</span></span>](create-packages-package-deployer.md#Step5)  

<a name="Step1"></a>   
#### <a name="step-1-create-a-project-using-the-template"></a><span data-ttu-id="cc626-125">Step 1: Create a project using the template</span><span class="sxs-lookup"><span data-stu-id="cc626-125">Step 1: Create a project using the template</span></span>  

1. <span data-ttu-id="cc626-126">Bắt đầu [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] và tạo một dự án mới.</span><span class="sxs-lookup"><span data-stu-id="cc626-126">Start [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)], and create a new project.</span></span>  

2. <span data-ttu-id="cc626-127">In the **New Project** dialog box:</span><span class="sxs-lookup"><span data-stu-id="cc626-127">In the **New Project** dialog box:</span></span>  

   1. <span data-ttu-id="cc626-128">From the list of installed templates, expand **Visual C#**, and select **Dynamics 365 for Customer Engagement apps SDK Templates**.</span><span class="sxs-lookup"><span data-stu-id="cc626-128">From the list of installed templates, expand **Visual C#**, and select **Dynamics 365 for Customer Engagement apps SDK Templates**.</span></span>  

   2. <span data-ttu-id="cc626-129">Ensure that **[!INCLUDE[pn_NET_Framework_452_short](../includes/pn-net-framework-452-short.md)]** is selected.</span><span class="sxs-lookup"><span data-stu-id="cc626-129">Ensure that **[!INCLUDE[pn_NET_Framework_452_short](../includes/pn-net-framework-452-short.md)]** is selected.</span></span>  

   3. <span data-ttu-id="cc626-130">Select **Dynamics 365 for Customer Engagement Package**.</span><span class="sxs-lookup"><span data-stu-id="cc626-130">Select **Dynamics 365 for Customer Engagement Package**.</span></span>  

   4. <span data-ttu-id="cc626-131">Specify the name and location of the project, and click **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc626-131">Specify the name and location of the project, and click **OK**.</span></span>  

   <span data-ttu-id="cc626-132">![New project for creating a custom package](media/crm-sdkv6-packagedeployer-01.png "New project for creating a custom package")</span><span class="sxs-lookup"><span data-stu-id="cc626-132">![New project for creating a custom package](media/crm-sdkv6-packagedeployer-01.png "New project for creating a custom package")</span></span>  

<a name="Step2"></a>   
#### <a name="step-2-add-your-files-to-the-project"></a><span data-ttu-id="cc626-133">Step 2: Add your files to the project</span><span class="sxs-lookup"><span data-stu-id="cc626-133">Step 2: Add your files to the project</span></span>  

1.  <span data-ttu-id="cc626-134">In the **Solutions Explorer** pane, add your solutions and files under the **PkgFolder** folder.</span><span class="sxs-lookup"><span data-stu-id="cc626-134">In the **Solutions Explorer** pane, add your solutions and files under the **PkgFolder** folder.</span></span>  

2.  <span data-ttu-id="cc626-135">For each file that you add under the **PkgFolder** folder, in the **Properties** pane, set the **Copy to Output Directory** value to **Copy Always**.</span><span class="sxs-lookup"><span data-stu-id="cc626-135">For each file that you add under the **PkgFolder** folder, in the **Properties** pane, set the **Copy to Output Directory** value to **Copy Always**.</span></span>                 <span data-ttu-id="cc626-136">This ensures that your file is available in the generated package.</span><span class="sxs-lookup"><span data-stu-id="cc626-136">This ensures that your file is available in the generated package.</span></span>  

<a name="Step3"></a>   
#### <a name="step-3-update-the-html-files-english-and-other-languages"></a><span data-ttu-id="cc626-137">Step 3: Update the HTML files: English and other languages</span><span class="sxs-lookup"><span data-stu-id="cc626-137">Step 3: Update the HTML files: English and other languages</span></span>  

1.  <span data-ttu-id="cc626-138">In the Solution Explorer pane, expand **PkgFolder** > **Content** > **en-us**.</span><span class="sxs-lookup"><span data-stu-id="cc626-138">In the Solution Explorer pane, expand **PkgFolder** > **Content** > **en-us**.</span></span> <span data-ttu-id="cc626-139">You’ll find two folders called EndHTML and WelcomeHTML.</span><span class="sxs-lookup"><span data-stu-id="cc626-139">You’ll find two folders called EndHTML and WelcomeHTML.</span></span> <span data-ttu-id="cc626-140">These folders contain the                 HTML and associated files that enable you to display information at the end and beginning of the package deployment process.</span><span class="sxs-lookup"><span data-stu-id="cc626-140">These folders contain the                 HTML and associated files that enable you to display information at the end and beginning of the package deployment process.</span></span> <span data-ttu-id="cc626-141">Edit the                 files in the HTML folder of these folders to add information for your package.</span><span class="sxs-lookup"><span data-stu-id="cc626-141">Edit the                 files in the HTML folder of these folders to add information for your package.</span></span>  

2.  <span data-ttu-id="cc626-142">You can also add the HTML files in your package in other languages so that the content in the HTML appears in the language based on the locale settings of the user’s computer.</span><span class="sxs-lookup"><span data-stu-id="cc626-142">You can also add the HTML files in your package in other languages so that the content in the HTML appears in the language based on the locale settings of the user’s computer.</span></span> <span data-ttu-id="cc626-143">To do so:</span><span class="sxs-lookup"><span data-stu-id="cc626-143">To do so:</span></span>  

    1.  <span data-ttu-id="cc626-144">Create a copy of the **en-us** folder under **PkgFolder** > **Content**.</span><span class="sxs-lookup"><span data-stu-id="cc626-144">Create a copy of the **en-us** folder under **PkgFolder** > **Content**.</span></span>  

    2.  <span data-ttu-id="cc626-145">Rename the copied folder to the appropriate language.</span><span class="sxs-lookup"><span data-stu-id="cc626-145">Rename the copied folder to the appropriate language.</span></span> <span data-ttu-id="cc626-146">For example, for the Spanish language, rename it to **es-ES**.</span><span class="sxs-lookup"><span data-stu-id="cc626-146">For example, for the Spanish language, rename it to **es-ES**.</span></span>  

    3.  <span data-ttu-id="cc626-147">Modify the content of the HTML files to add Spanish content.</span><span class="sxs-lookup"><span data-stu-id="cc626-147">Modify the content of the HTML files to add Spanish content.</span></span>  

<a name="Step4"></a>   
#### <a name="step-4-specify-the-configuration-values-for-the-package"></a><span data-ttu-id="cc626-148">Step 4: Specify the configuration values for the package</span><span class="sxs-lookup"><span data-stu-id="cc626-148">Step 4: Specify the configuration values for the package</span></span>  

1. <span data-ttu-id="cc626-149">Define the package configuration by adding information about your package in the **ImportConfig.xml** file available in the **PkgFolder**.</span><span class="sxs-lookup"><span data-stu-id="cc626-149">Define the package configuration by adding information about your package in the **ImportConfig.xml** file available in the **PkgFolder**.</span></span> <span data-ttu-id="cc626-150">Double-click the file to open it for editing.</span><span class="sxs-lookup"><span data-stu-id="cc626-150">Double-click the file to open it for editing.</span></span> <span data-ttu-id="cc626-151">The following list provides information about each parameter and node in the config file.</span><span class="sxs-lookup"><span data-stu-id="cc626-151">The following list provides information about each parameter and node in the config file.</span></span>  

    <span data-ttu-id="cc626-152">installsampledata</span><span class="sxs-lookup"><span data-stu-id="cc626-152">installsampledata</span></span>  
    <span data-ttu-id="cc626-153">`True` or `false`.</span><span class="sxs-lookup"><span data-stu-id="cc626-153">`True` or `false`.</span></span> <span data-ttu-id="cc626-154">If `true`, installs sample data to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance.</span><span class="sxs-lookup"><span data-stu-id="cc626-154">If `true`, installs sample data to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance.</span></span> <span data-ttu-id="cc626-155">This is the same sample data that you can install from **Settings** > **Data Management** area in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="cc626-155">This is the same sample data that you can install from **Settings** > **Data Management** area in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span>  

    <span data-ttu-id="cc626-156">waitforsampledatatoinstall</span><span class="sxs-lookup"><span data-stu-id="cc626-156">waitforsampledatatoinstall</span></span>  
   <span data-ttu-id="cc626-157">**True** or **false**.</span><span class="sxs-lookup"><span data-stu-id="cc626-157">**True** or **false**.</span></span> <span data-ttu-id="cc626-158">If **true**, and if **installsampledata** is also set to **true**, waits for sample data to install before deploying the package.</span><span class="sxs-lookup"><span data-stu-id="cc626-158">If **true**, and if **installsampledata** is also set to **true**, waits for sample data to install before deploying the package.</span></span>  

   > [!NOTE]
   >  <span data-ttu-id="cc626-159">Ensure that you set **installsampledata** to **true** if you are setting `waitforsampledatatoinstall` to **true**.</span><span class="sxs-lookup"><span data-stu-id="cc626-159">Ensure that you set **installsampledata** to **true** if you are setting `waitforsampledatatoinstall` to **true**.</span></span>  

    <span data-ttu-id="cc626-160">agentdesktopzipfile</span><span class="sxs-lookup"><span data-stu-id="cc626-160">agentdesktopzipfile</span></span>  
    <span data-ttu-id="cc626-161">File name of the zip file to unpack.</span><span class="sxs-lookup"><span data-stu-id="cc626-161">File name of the zip file to unpack.</span></span> <span data-ttu-id="cc626-162">If you specify a .zip file name here, it adds a screen during the package deployment process that prompts you to                         select a location where you want to unpack the contents of the file.</span><span class="sxs-lookup"><span data-stu-id="cc626-162">If you specify a .zip file name here, it adds a screen during the package deployment process that prompts you to                         select a location where you want to unpack the contents of the file.</span></span>  

    <span data-ttu-id="cc626-163">This is commonly used for creating packages for [!INCLUDE[pn_unified_service_desk_for_crm](../includes/pn-unified-service-desk-for-crm.md)].</span><span class="sxs-lookup"><span data-stu-id="cc626-163">This is commonly used for creating packages for [!INCLUDE[pn_unified_service_desk_for_crm](../includes/pn-unified-service-desk-for-crm.md)].</span></span> <span data-ttu-id="cc626-164">For information about [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Unified Service Desk Administration Guide](https://technet.microsoft.com/library/dn499779.aspx).</span><span class="sxs-lookup"><span data-stu-id="cc626-164">For information about [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Unified Service Desk Administration Guide](https://technet.microsoft.com/library/dn499779.aspx).</span></span>  

    <span data-ttu-id="cc626-165">agentdesktopexename</span><span class="sxs-lookup"><span data-stu-id="cc626-165">agentdesktopexename</span></span>  
    <span data-ttu-id="cc626-166">Name of the .exe or .msi file in the zip file or a URL to be invoked at the end of the deployment process.</span><span class="sxs-lookup"><span data-stu-id="cc626-166">Name of the .exe or .msi file in the zip file or a URL to be invoked at the end of the deployment process.</span></span>  

    <span data-ttu-id="cc626-167">This is commonly used for creating packages for [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="cc626-167">This is commonly used for creating packages for [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  

    <span data-ttu-id="cc626-168">crmmigdataimportfile</span><span class="sxs-lookup"><span data-stu-id="cc626-168">crmmigdataimportfile</span></span>  
    <span data-ttu-id="cc626-169">File name of the default configuration data file (.zip) exported using the Configuration Migration tool.</span><span class="sxs-lookup"><span data-stu-id="cc626-169">File name of the default configuration data file (.zip) exported using the Configuration Migration tool.</span></span>  

   - <span data-ttu-id="cc626-170">You can also import a localized version of the configuration data file based on the locale ID (LCID) specified using new runtime settings while running                             the package deployer.</span><span class="sxs-lookup"><span data-stu-id="cc626-170">You can also import a localized version of the configuration data file based on the locale ID (LCID) specified using new runtime settings while running                             the package deployer.</span></span> <span data-ttu-id="cc626-171">Use the `<cmtdatafile>` node (explained later) to specify the localized versions of the                             configuration data file in a package and then use the  `OverrideConfigurationDataFileLanguage` method (explained later)                             to specify the logic for importing the configuration data file based on the locale ID specified using the runtime settings.</span><span class="sxs-lookup"><span data-stu-id="cc626-171">Use the `<cmtdatafile>` node (explained later) to specify the localized versions of the                             configuration data file in a package and then use the  `OverrideConfigurationDataFileLanguage` method (explained later)                             to specify the logic for importing the configuration data file based on the locale ID specified using the runtime settings.</span></span> <span data-ttu-id="cc626-172">You cannot import more than                             one configuration data file using a package at a time.</span><span class="sxs-lookup"><span data-stu-id="cc626-172">You cannot import more than                             one configuration data file using a package at a time.</span></span>  

   - <span data-ttu-id="cc626-173">For [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] (on-premises) apps, if your configuration data file contains user information, and both the source and target [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instances are on the same Active Directory Domain, user information will be imported to the target [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="cc626-173">For [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] (on-premises) apps, if your configuration data file contains user information, and both the source and target [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instances are on the same Active Directory Domain, user information will be imported to the target [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span></span> <span data-ttu-id="cc626-174">To import user information to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] (on-premises) apps instance on a different domain, you must include the user map file (.xml) generated using the Configuration Migration tool in your project, and specify it along with the configuration data file using the `usermapfilename` attribute in the `<cmtdatafile>` node explained later.</span><span class="sxs-lookup"><span data-stu-id="cc626-174">To import user information to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] (on-premises) apps instance on a different domain, you must include the user map file (.xml) generated using the Configuration Migration tool in your project, and specify it along with the configuration data file using the `usermapfilename` attribute in the `<cmtdatafile>` node explained later.</span></span> <span data-ttu-id="cc626-175">User information cannot be imported to [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="cc626-175">User information cannot be imported to [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] apps instance.</span></span>  

     <span data-ttu-id="cc626-176">`<solutions>` node</span><span class="sxs-lookup"><span data-stu-id="cc626-176">`<solutions>` node</span></span>  
     <span data-ttu-id="cc626-177">Contains an array of `<configsolutionfile>` nodes that describe the solutions to import.</span><span class="sxs-lookup"><span data-stu-id="cc626-177">Contains an array of `<configsolutionfile>` nodes that describe the solutions to import.</span></span> <span data-ttu-id="cc626-178">The order of the solutions under this                         node indicates the order in which the solutions will be imported on the target [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="cc626-178">The order of the solutions under this                         node indicates the order in which the solutions will be imported on the target [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span></span>  

     <span data-ttu-id="cc626-179">`<configsolutionfile>` node</span><span class="sxs-lookup"><span data-stu-id="cc626-179">`<configsolutionfile>` node</span></span>  
     <span data-ttu-id="cc626-180">Use this node under the `<solutions>` node to specify the individual solutions and the following information for each solution to be imported:</span><span class="sxs-lookup"><span data-stu-id="cc626-180">Use this node under the `<solutions>` node to specify the individual solutions and the following information for each solution to be imported:</span></span>  

   - <span data-ttu-id="cc626-181">`solutionpackagefilename`: Specify the .zip file name of your solution.</span><span class="sxs-lookup"><span data-stu-id="cc626-181">`solutionpackagefilename`: Specify the .zip file name of your solution.</span></span> <span data-ttu-id="cc626-182">Yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="cc626-182">Required.</span></span>  

   - <span data-ttu-id="cc626-183">`overwriteunmanagedcustomizations`: Specify whether to overwrite any unmanaged customizations when importing a solution that already exists in the target Dynamics 365 for Customer Engagement apps instance.</span><span class="sxs-lookup"><span data-stu-id="cc626-183">`overwriteunmanagedcustomizations`: Specify whether to overwrite any unmanaged customizations when importing a solution that already exists in the target Dynamics 365 for Customer Engagement apps instance.</span></span> <span data-ttu-id="cc626-184">This is optional, and if you do not specify this attribute, by default the unmanaged customizations in the existing solution are maintained on the target Dynamics 365 for Customer Engagement apps instance.</span><span class="sxs-lookup"><span data-stu-id="cc626-184">This is optional, and if you do not specify this attribute, by default the unmanaged customizations in the existing solution are maintained on the target Dynamics 365 for Customer Engagement apps instance.</span></span>  

   - <span data-ttu-id="cc626-185">`publishworkflowsandactivateplugins`: Specify whether to publish workflows and activate plug-ins in the target Dynamics 365 for Customer Engagement apps instance after the solution is imported.</span><span class="sxs-lookup"><span data-stu-id="cc626-185">`publishworkflowsandactivateplugins`: Specify whether to publish workflows and activate plug-ins in the target Dynamics 365 for Customer Engagement apps instance after the solution is imported.</span></span> <span data-ttu-id="cc626-186">This is optional, and if you do not specify not specify this attribute, by default the workflows are published and plug-ins are activated after the solution is imported on the target Dynamics 365 for Customer Engagement apps instance.</span><span class="sxs-lookup"><span data-stu-id="cc626-186">This is optional, and if you do not specify not specify this attribute, by default the workflows are published and plug-ins are activated after the solution is imported on the target Dynamics 365 for Customer Engagement apps instance.</span></span>  

     <span data-ttu-id="cc626-187">You can add multiple solution file names in a package by adding as many `<configsolutionfile>` nodes.</span><span class="sxs-lookup"><span data-stu-id="cc626-187">You can add multiple solution file names in a package by adding as many `<configsolutionfile>` nodes.</span></span> <span data-ttu-id="cc626-188">For example, if you want three solution files to be imported, add them like this:</span><span class="sxs-lookup"><span data-stu-id="cc626-188">For example, if you want three solution files to be imported, add them like this:</span></span>  

   ```xml  

   <solutions>  
   <configsolutionfile solutionpackagefilename="SampleSolutionOne_1_0_managed.zip"  
   overwriteunmanagedcustomizations="false"  
   publishworkflowsandactivateplugins="true"/>  
   <configsolutionfile solutionpackagefilename="SampleSolutionTwo_1_0_managed.zip"  
   overwriteunmanagedcustomizations="false"  
   publishworkflowsandactivateplugins="true"/>  
   <configsolutionfile solutionpackagefilename="SampleSolutionThree_1_0_managed.zip" />  
   </solutions>  

   ```  

    <span data-ttu-id="cc626-189">`<filestoimportnode>` node</span><span class="sxs-lookup"><span data-stu-id="cc626-189">`<filestoimportnode>` node</span></span>  
    <span data-ttu-id="cc626-190">Contains an array of `<configimportfile>` and `<zipimportdetails>` nodes that are used to describe                         individual files and zip files respectively to be imported.</span><span class="sxs-lookup"><span data-stu-id="cc626-190">Contains an array of `<configimportfile>` and `<zipimportdetails>` nodes that are used to describe                         individual files and zip files respectively to be imported.</span></span>  

    <span data-ttu-id="cc626-191">`<configimportfile>` node</span><span class="sxs-lookup"><span data-stu-id="cc626-191">`<configimportfile>` node</span></span>  
    <span data-ttu-id="cc626-192">Use this node under the `<configimportfile>` node to describe a file to be imported to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="cc626-192">Use this node under the `<configimportfile>` node to describe a file to be imported to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="cc626-193">You can add multiple                         files in a package by adding as many `<configimportfile>` nodes.</span><span class="sxs-lookup"><span data-stu-id="cc626-193">You can add multiple                         files in a package by adding as many `<configimportfile>` nodes.</span></span>  

   ```xml  

   <filestoimport>  
   <configimportfile filename="File.csv"  
   filetype="CSV"  
   associatedmap="FileMap"  
   importtoentity="FileEntity"  
   datadelimiter=""  
   fielddelimiter="comma"  
   enableduplicatedetection="true"  
   isfirstrowheader="true"  
   isrecordownerateam="false"  
   owneruser=""  
   waitforimporttocomplete="true" />  
   <configimportfile filename="File.zip"  
   filetype="ZIP"  
   associatedmap="FileMapName"  
   importtoentity="FileEntity"  
   datadelimiter=""  
   fielddelimiter="comma"  
   enableduplicatedetection="true"  
   isfirstrowheader="true"  
   isrecordownerateam="false"  
   owneruser=""  
   waitforimporttocomplete="true"/>  

   </filestoimport>  

   ```  

    <span data-ttu-id="cc626-194">This has the following attributes:</span><span class="sxs-lookup"><span data-stu-id="cc626-194">This has the following attributes:</span></span>  


   |         <span data-ttu-id="cc626-195">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="cc626-195">Attribute</span></span>          |                                                                                                       <span data-ttu-id="cc626-196">Mô tả</span><span class="sxs-lookup"><span data-stu-id="cc626-196">Description</span></span>                                                                                                       |
   |----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |         `filename`         | <span data-ttu-id="cc626-197">Name of the file that contains the import data.</span><span class="sxs-lookup"><span data-stu-id="cc626-197">Name of the file that contains the import data.</span></span> <span data-ttu-id="cc626-198">If the file is a .zip file, a `<zipimportdetails>` node must be present with a                                 `<zipimportdetail>` node for each file in the .zip file.</span><span class="sxs-lookup"><span data-stu-id="cc626-198">If the file is a .zip file, a `<zipimportdetails>` node must be present with a                                 `<zipimportdetail>` node for each file in the .zip file.</span></span> |
   |         `filetype`         |                                                                                              <span data-ttu-id="cc626-199">This can be csv, xml, or zip.</span><span class="sxs-lookup"><span data-stu-id="cc626-199">This can be csv, xml, or zip.</span></span>                                                                                              |
   |      `associatedmap`       |           <span data-ttu-id="cc626-200">Name of the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps import data map to use with this file.</span><span class="sxs-lookup"><span data-stu-id="cc626-200">Name of the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps import data map to use with this file.</span></span> <span data-ttu-id="cc626-201">If blank, attempts to use the system determined import data map name for this file.</span><span class="sxs-lookup"><span data-stu-id="cc626-201">If blank, attempts to use the system determined import data map name for this file.</span></span>            |
   |      `importtoentity`      |                                                <span data-ttu-id="cc626-202">Can be the name of the exe in the zip file, a URL, or an .msi file to provide a link to invoke at the end of the process.</span><span class="sxs-lookup"><span data-stu-id="cc626-202">Can be the name of the exe in the zip file, a URL, or an .msi file to provide a link to invoke at the end of the process.</span></span>                                                |
   |      `datadelimiter`       |                                                            <span data-ttu-id="cc626-203">Name of the data delimiter used in the import file.</span><span class="sxs-lookup"><span data-stu-id="cc626-203">Name of the data delimiter used in the import file.</span></span> <span data-ttu-id="cc626-204">Valid values are singlequote or doublequotes.</span><span class="sxs-lookup"><span data-stu-id="cc626-204">Valid values are singlequote or doublequotes.</span></span>                                                            |
   |      `fielddelimiter`      |                                          <span data-ttu-id="cc626-205">Name of the field delimiter used in the import file.</span><span class="sxs-lookup"><span data-stu-id="cc626-205">Name of the field delimiter used in the import file.</span></span> <span data-ttu-id="cc626-206">Valid values are comma or colon, or                                 singlequote.</span><span class="sxs-lookup"><span data-stu-id="cc626-206">Valid values are comma or colon, or                                 singlequote.</span></span>                                          |
   | `enableduplicatedetection` |                                                     <span data-ttu-id="cc626-207">Indicates whether to enable duplicate detections rules on data import.</span><span class="sxs-lookup"><span data-stu-id="cc626-207">Indicates whether to enable duplicate detections rules on data import.</span></span> <span data-ttu-id="cc626-208">Valid values are **true** or **false**.</span><span class="sxs-lookup"><span data-stu-id="cc626-208">Valid values are **true** or **false**.</span></span>                                                      |
   |     `isfirstrowheader`     |                                                   <span data-ttu-id="cc626-209">Used to denote that the first row of the import file contains the field names.</span><span class="sxs-lookup"><span data-stu-id="cc626-209">Used to denote that the first row of the import file contains the field names.</span></span> <span data-ttu-id="cc626-210">Valid values are `true` or `false`.</span><span class="sxs-lookup"><span data-stu-id="cc626-210">Valid values are `true` or `false`.</span></span>                                                    |
   |    `isrecordownerateam`    |                                                        <span data-ttu-id="cc626-211">Indicates whether the owner of the record on import should be a team.</span><span class="sxs-lookup"><span data-stu-id="cc626-211">Indicates whether the owner of the record on import should be a team.</span></span> <span data-ttu-id="cc626-212">Valid values are `true` or `false`.</span><span class="sxs-lookup"><span data-stu-id="cc626-212">Valid values are `true` or `false`.</span></span>                                                        |
   |        `owneruser`         |                                                          <span data-ttu-id="cc626-213">Indicates the user ID that should own the records.</span><span class="sxs-lookup"><span data-stu-id="cc626-213">Indicates the user ID that should own the records.</span></span> <span data-ttu-id="cc626-214">The default value is the currently logged in user.</span><span class="sxs-lookup"><span data-stu-id="cc626-214">The default value is the currently logged in user.</span></span>                                                          |
   | `waitforimporttocomplete`  |                                                 <span data-ttu-id="cc626-215">If `true`, the system waits for the import to complete before proceeding.</span><span class="sxs-lookup"><span data-stu-id="cc626-215">If `true`, the system waits for the import to complete before proceeding.</span></span> <span data-ttu-id="cc626-216">If `false`, it queues the jobs and moves on.</span><span class="sxs-lookup"><span data-stu-id="cc626-216">If `false`, it queues the jobs and moves on.</span></span>                                                  |

    <span data-ttu-id="cc626-217">`<zipimportdetails>` node</span><span class="sxs-lookup"><span data-stu-id="cc626-217">`<zipimportdetails>` node</span></span>  
    <span data-ttu-id="cc626-218">This node contains an array of `<zipimportdetail>` nodes that describe the files included in a zip file that is used to import to Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="cc626-218">This node contains an array of `<zipimportdetail>` nodes that describe the files included in a zip file that is used to import to Dynamics 365 for Customer Engagement apps.</span></span>  

    <span data-ttu-id="cc626-219">`<zipimportdetail>` node</span><span class="sxs-lookup"><span data-stu-id="cc626-219">`<zipimportdetail>` node</span></span>  
    <span data-ttu-id="cc626-220">Use this node under the `<zipimportdetails>` node to provide information about an individual file in a .zip file that is specified in the                         `<configimportfile>` node.</span><span class="sxs-lookup"><span data-stu-id="cc626-220">Use this node under the `<zipimportdetails>` node to provide information about an individual file in a .zip file that is specified in the                         `<configimportfile>` node.</span></span>  

   ```xml  

   <filestoimport>  
   ...  
   ...  
   <zipimportdetails>  
   <zipimportdetail filename="subfile1.csv" filetype="csv" importtoentity="account" />  
   <zipimportdetail filename="subfile2.csv" filetype="csv" importtoentity="contact" />  
   </zipimportdetails>  
   </filestoimport>  

   ```  

    <span data-ttu-id="cc626-221">This has the following attributes:</span><span class="sxs-lookup"><span data-stu-id="cc626-221">This has the following attributes:</span></span>  

   |<span data-ttu-id="cc626-222">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="cc626-222">Attribute</span></span>|<span data-ttu-id="cc626-223">Mô tả</span><span class="sxs-lookup"><span data-stu-id="cc626-223">Description</span></span>|  
   |---------------|-----------------|  
   |`filename`|<span data-ttu-id="cc626-224">Name of the file that contains the import data.</span><span class="sxs-lookup"><span data-stu-id="cc626-224">Name of the file that contains the import data.</span></span>|  
   |`filetype`|<span data-ttu-id="cc626-225">This can be csv or xml.</span><span class="sxs-lookup"><span data-stu-id="cc626-225">This can be csv or xml.</span></span>|  
   |`importtoentity`|<span data-ttu-id="cc626-226">Can be the name of the exe in the zip file, a url, or an .msi file to provide a link to invoke at the end of the process.</span><span class="sxs-lookup"><span data-stu-id="cc626-226">Can be the name of the exe in the zip file, a url, or an .msi file to provide a link to invoke at the end of the process.</span></span>|  

    <span data-ttu-id="cc626-227">`<filesmapstoimport>` node</span><span class="sxs-lookup"><span data-stu-id="cc626-227">`<filesmapstoimport>` node</span></span>  
    <span data-ttu-id="cc626-228">This node contains an array of `<configmapimportfile>` nodes to import.</span><span class="sxs-lookup"><span data-stu-id="cc626-228">This node contains an array of `<configmapimportfile>` nodes to import.</span></span> <span data-ttu-id="cc626-229">The order of the map files in this node indicates the order in                         which they are imported.</span><span class="sxs-lookup"><span data-stu-id="cc626-229">The order of the map files in this node indicates the order in                         which they are imported.</span></span> <span data-ttu-id="cc626-230">For information about data maps, see [Create Data Maps for Import](create-data-maps-for-import.md).</span><span class="sxs-lookup"><span data-stu-id="cc626-230">For information about data maps, see [Create Data Maps for Import](create-data-maps-for-import.md).</span></span>  

    <span data-ttu-id="cc626-231">`<configimportmapfile>` node</span><span class="sxs-lookup"><span data-stu-id="cc626-231">`<configimportmapfile>` node</span></span>  
    <span data-ttu-id="cc626-232">Use this node under the `<filesmapstoimport>` node to provide information about an individual map file to import in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="cc626-232">Use this node under the `<filesmapstoimport>` node to provide information about an individual map file to import in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span>  

   ```xml  

   <filesmapstoimport>  
   <configimportmapfile filename="FileMap.xml" />  
   </filesmapstoimport>  

   ```  

    <span data-ttu-id="cc626-233">`<cmtdatafiles>` node</span><span class="sxs-lookup"><span data-stu-id="cc626-233">`<cmtdatafiles>` node</span></span>  
    <span data-ttu-id="cc626-234">This node contains an array of `<cmtdatafile>` nodes that containslocalized version of the configuration data file to be imported.</span><span class="sxs-lookup"><span data-stu-id="cc626-234">This node contains an array of `<cmtdatafile>` nodes that containslocalized version of the configuration data file to be imported.</span></span>  

    <span data-ttu-id="cc626-235">`<cmtdatafile>` node</span><span class="sxs-lookup"><span data-stu-id="cc626-235">`<cmtdatafile>` node</span></span>  
    <span data-ttu-id="cc626-236">Use this node under the `<cmtdatafiles>` node to specify the localized configuration                         data files along with                         locale ID (required) and user information map file (optional).</span><span class="sxs-lookup"><span data-stu-id="cc626-236">Use this node under the `<cmtdatafiles>` node to specify the localized configuration                         data files along with                         locale ID (required) and user information map file (optional).</span></span> <span data-ttu-id="cc626-237">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="cc626-237">For example:</span></span>  

   ```xml  

   <cmtdatafiles>  
   <cmtdatafile filename="data_1033.zip" lcid="1033" usermapfilename="UserMap.xml" />  
   <cmtdatafile filename="data_1041.zip" lcid="1041" usermapfilename="" />  
   </cmtdatafiles>  

   ```  

    <span data-ttu-id="cc626-238">You can define your custom logic in the `OverrideConfigurationDataFileLanguage` method (explained later) to import  a localized                         configuration data file instead of the default one (specified in crmmigdataimportfile) based on the locale ID (LCID) value                         specified using the runtime settings (explained later).</span><span class="sxs-lookup"><span data-stu-id="cc626-238">You can define your custom logic in the `OverrideConfigurationDataFileLanguage` method (explained later) to import  a localized                         configuration data file instead of the default one (specified in crmmigdataimportfile) based on the locale ID (LCID) value                         specified using the runtime settings (explained later).</span></span>  

2. <span data-ttu-id="cc626-239">Click **Save All**.</span><span class="sxs-lookup"><span data-stu-id="cc626-239">Click **Save All**.</span></span>  

    <span data-ttu-id="cc626-240">The following represents the contents of a sample `ImportConfig.xml` file.</span><span class="sxs-lookup"><span data-stu-id="cc626-240">The following represents the contents of a sample `ImportConfig.xml` file.</span></span>  

   ```xml  

   <?xml version="1.0" encoding="utf-16"?>  
   <configdatastorage xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  
   xmlns:xsd="http://www.w3.org/2001/XMLSchema"  
   installsampledata="true"  
   waitforsampledatatoinstall="true"  
   agentdesktopzipfile=""  
   agentdesktopexename=""  
   crmmigdataimportfile="data_1033.zip">  
   <solutions>  
   <configsolutionfile solutionpackagefilename="SampleSolutionOne_1_0_managed.zip"  
   overwriteunmanagedcustomizations="false"  
   publishworkflowsandactivateplugins="true"/>  
   <configsolutionfile solutionpackagefilename="SampleSolutionTwo_1_0_managed.zip"  
   overwriteunmanagedcustomizations="false"  
   publishworkflowsandactivateplugins="true"/>  
   <configsolutionfile solutionpackagefilename="SampleSolutionThree_1_0_managed.zip" />  
   </solutions>  
   <filestoimport>  
   <configimportfile filename="SampleOption.csv"  
   filetype="CSV"  
   associatedmap="SampleOption"  
   importtoentity="sample_option"  
   datadelimiter=""  
   fielddelimiter="comma"  
   enableduplicatedetection="true"  
   isfirstrowheader="true"  
   isrecordownerateam="false"  
   owneruser=""  
   waitforimporttocomplete="false"/>  
   <configimportfile filename="File.zip"  
   filetype="ZIP"  
   associatedmap="FileMapName"  
   importtoentity="FileEntity"  
   datadelimiter=""  
   fielddelimiter="comma"  
   enableduplicatedetection="true"  
   isfirstrowheader="true"  
   isrecordownerateam="false"  
   owneruser=""  
   waitforimporttocomplete="true"/>  
   <zipimportdetails>  
   <zipimportdetail filename="subfile1.csv"  
   filetype="csv"  
   importtoentity="account" />  
   <zipimportdetail filename="subfile2.csv"  
   filetype="csv"  
   importtoentity="contact" />  
   </zipimportdetails>  
   </filestoimport>  
   <filesmapstoimport>  
   <configimportmapfile filename="SampleOption.xml" />  
   </filesmapstoimport>  
   <cmtdatafiles>  
   <cmtdatafile filename="data_1033.zip"  
   lcid="1033"  
   usermapfilename="UserMap.xml" />  
   <cmtdatafile filename="data_1041.zip"  
   lcid="1041"  
   usermapfilename="" />  
   </cmtdatafiles>  
   </configdatastorage>  

   ```  

<a name="Step5"></a>   
#### <a name="step-5-define-custom-code-for-your-package"></a><span data-ttu-id="cc626-241">Step 5: Define custom code for your package</span><span class="sxs-lookup"><span data-stu-id="cc626-241">Step 5: Define custom code for your package</span></span>  

1. <span data-ttu-id="cc626-242">In the Solution Explorer pane, double-click the **PackageTemplate.cs** file at the root to edit it.</span><span class="sxs-lookup"><span data-stu-id="cc626-242">In the Solution Explorer pane, double-click the **PackageTemplate.cs** file at the root to edit it.</span></span>  

2. <span data-ttu-id="cc626-243">In the PackageTemplate.cs file, you can:</span><span class="sxs-lookup"><span data-stu-id="cc626-243">In the PackageTemplate.cs file, you can:</span></span>  

   1. <span data-ttu-id="cc626-244">Enter custom code to execute when the package is initialized in the override method definition of `InitializeCustomExtension`.</span><span class="sxs-lookup"><span data-stu-id="cc626-244">Enter custom code to execute when the package is initialized in the override method definition of `InitializeCustomExtension`.</span></span>  

       <span data-ttu-id="cc626-245">This method can be used to let users use the runtime parameters while running a package.</span><span class="sxs-lookup"><span data-stu-id="cc626-245">This method can be used to let users use the runtime parameters while running a package.</span></span> <span data-ttu-id="cc626-246">As a developer, you can add support for                     any runtime parameter to your package by using the                     <xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.IImportExtensions2.RuntimeSettings> property as long as you have code                     to process it based on the user input.</span><span class="sxs-lookup"><span data-stu-id="cc626-246">As a developer, you can add support for                     any runtime parameter to your package by using the                     <xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.IImportExtensions2.RuntimeSettings> property as long as you have code                     to process it based on the user input.</span></span>  

       <span data-ttu-id="cc626-247">For example, the following sample code enables a runtime parameter called `SkipChecks` for the package that has two possible values:                     true or false.</span><span class="sxs-lookup"><span data-stu-id="cc626-247">For example, the following sample code enables a runtime parameter called `SkipChecks` for the package that has two possible values:                     true or false.</span></span> <span data-ttu-id="cc626-248">The sample code checks if the user has specified any runtime parameters while running [!INCLUDE[pn_package_deployer_short](../includes/pn-package-deployer-short.md)] (either by using the command line or PowerShell), and then accordingly processes the information.</span><span class="sxs-lookup"><span data-stu-id="cc626-248">The sample code checks if the user has specified any runtime parameters while running [!INCLUDE[pn_package_deployer_short](../includes/pn-package-deployer-short.md)] (either by using the command line or PowerShell), and then accordingly processes the information.</span></span> <span data-ttu-id="cc626-249">If no runtime parameter is specified                     by the user while running the package, the value of the <xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.IImportExtensions2.RuntimeSettings> property will be null.</span><span class="sxs-lookup"><span data-stu-id="cc626-249">If no runtime parameter is specified                     by the user while running the package, the value of the <xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.IImportExtensions2.RuntimeSettings> property will be null.</span></span>  

      ```csharp  

      public override void InitializeCustomExtension()  
      {  
      // Do nothing.  

      // Validate the state of the runtime settings object.  
      if (RuntimeSettings != null)  
      {  
      PackageLog.Log(string.Format("Runtime Settings populated.  Count = {0}", RuntimeSettings.Count));  
      foreach (var setting in RuntimeSettings)  
      {  
      PackageLog.Log(string.Format("Key={0} | Value={1}", setting.Key, setting.Value.ToString()));  
      }  

      // Check to see if skip checks is present.  
      if ( RuntimeSettings.ContainsKey("SkipChecks") )  
      {  
      bool bSkipChecks = false;  
      if (bool.TryParse((string)RuntimeSettings["SkipChecks"], out bSkipChecks))  
      OverrideDataImportSafetyChecks = bSkipChecks;  
      }  
      }  
      else  
      PackageLog.Log("Runtime Settings not populated");  
      }  

      ```  

       <span data-ttu-id="cc626-250">This lets the administrator use the command line or the [Import-CrmPackage](https://technet.microsoft.com/library/dn756301.aspx) cmdlet to specify whether to skip the safety checks while running the Package Deployer tool to import the package.</span><span class="sxs-lookup"><span data-stu-id="cc626-250">This lets the administrator use the command line or the [Import-CrmPackage](https://technet.microsoft.com/library/dn756301.aspx) cmdlet to specify whether to skip the safety checks while running the Package Deployer tool to import the package.</span></span> <span data-ttu-id="cc626-251">More information: [Deploy packages using CRM Package Deployer and Windows PowerShell](https://technet.microsoft.com/library/dn647420.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc626-251">More information: [Deploy packages using CRM Package Deployer and Windows PowerShell](https://technet.microsoft.com/library/dn647420.aspx)</span></span>  

   2. <span data-ttu-id="cc626-252">Enter custom code to execute before the solutions are imported in  the override method definition of `PreSolutionImport` to specify whether to maintain or overwrite customizations while updating the specified solution in a target [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance, and whether to automatically activate plug-ins and workflows.</span><span class="sxs-lookup"><span data-stu-id="cc626-252">Enter custom code to execute before the solutions are imported in  the override method definition of `PreSolutionImport` to specify whether to maintain or overwrite customizations while updating the specified solution in a target [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance, and whether to automatically activate plug-ins and workflows.</span></span>  

   3. <span data-ttu-id="cc626-253">Use the override method definition of `RunSolutionUpgradeMigrationStep` to perform data transformation or upgrade between two versions of a solution.</span><span class="sxs-lookup"><span data-stu-id="cc626-253">Use the override method definition of `RunSolutionUpgradeMigrationStep` to perform data transformation or upgrade between two versions of a solution.</span></span> <span data-ttu-id="cc626-254">This method is called only if the solution you are importing is already present in the target [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance.</span><span class="sxs-lookup"><span data-stu-id="cc626-254">This method is called only if the solution you are importing is already present in the target [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance.</span></span>  

       <span data-ttu-id="cc626-255">This function expects the following parameters:</span><span class="sxs-lookup"><span data-stu-id="cc626-255">This function expects the following parameters:</span></span>  


      |    <span data-ttu-id="cc626-256">Tham số</span><span class="sxs-lookup"><span data-stu-id="cc626-256">Parameter</span></span>    |            <span data-ttu-id="cc626-257">Mô tả</span><span class="sxs-lookup"><span data-stu-id="cc626-257">Description</span></span>             |
      |-----------------|------------------------------------|
      | `solutionName`  |        <span data-ttu-id="cc626-258">Name of the solution</span><span class="sxs-lookup"><span data-stu-id="cc626-258">Name of the solution</span></span>        |
      |  `oldVersion`   | <span data-ttu-id="cc626-259">Version number of the old solution</span><span class="sxs-lookup"><span data-stu-id="cc626-259">Version number of the old solution</span></span> |
      |  `newVersion`   | <span data-ttu-id="cc626-260">Version number of the new solution</span><span class="sxs-lookup"><span data-stu-id="cc626-260">Version number of the new solution</span></span> |
      | `oldSolutionId` |     <span data-ttu-id="cc626-261">GUID of the old solution.</span><span class="sxs-lookup"><span data-stu-id="cc626-261">GUID of the old solution.</span></span>      |
      | `newSolutionId` |     <span data-ttu-id="cc626-262">GUID of the new solution.</span><span class="sxs-lookup"><span data-stu-id="cc626-262">GUID of the new solution.</span></span>      |


   4. <span data-ttu-id="cc626-263">Enter custom code to execute before the solution import completes in the override definition of the `BeforeImportStage` method.</span><span class="sxs-lookup"><span data-stu-id="cc626-263">Enter custom code to execute before the solution import completes in the override definition of the `BeforeImportStage` method.</span></span>                     <span data-ttu-id="cc626-264">The sample data and some flat files for solutions specified in the `ImportConfig.xml` file are imported before the solution import completes.</span><span class="sxs-lookup"><span data-stu-id="cc626-264">The sample data and some flat files for solutions specified in the `ImportConfig.xml` file are imported before the solution import completes.</span></span>  

   5. <span data-ttu-id="cc626-265">Override the currently-selected language for configuration data import using the                     override method definition of `OverrideConfigurationDataFileLanguage`.</span><span class="sxs-lookup"><span data-stu-id="cc626-265">Override the currently-selected language for configuration data import using the                     override method definition of `OverrideConfigurationDataFileLanguage`.</span></span> <span data-ttu-id="cc626-266">If the specified locale ID (LCID) of the specified language is                     not found in the list of available languages in the package, the default data file is imported.</span><span class="sxs-lookup"><span data-stu-id="cc626-266">If the specified locale ID (LCID) of the specified language is                     not found in the list of available languages in the package, the default data file is imported.</span></span>  

       <span data-ttu-id="cc626-267">You specify the available languages for the configuration data in the `<cmtdatafiles>` node in the                     `ImportConfig.xml` file.</span><span class="sxs-lookup"><span data-stu-id="cc626-267">You specify the available languages for the configuration data in the `<cmtdatafiles>` node in the                     `ImportConfig.xml` file.</span></span> <span data-ttu-id="cc626-268">The default configuration data import file is specified in the `crmmigdataimportfile` attribute in the                     `ImportConfig.xml` file.</span><span class="sxs-lookup"><span data-stu-id="cc626-268">The default configuration data import file is specified in the `crmmigdataimportfile` attribute in the                     `ImportConfig.xml` file.</span></span>  

       <span data-ttu-id="cc626-269">Skipping data checks (<xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.IImportExtensions2.OverrideDataImportSafetyChecks> = true)                     can be effective here if you are sure that the target [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance does not contain any data.</span><span class="sxs-lookup"><span data-stu-id="cc626-269">Skipping data checks (<xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.IImportExtensions2.OverrideDataImportSafetyChecks> = true)                     can be effective here if you are sure that the target [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance does not contain any data.</span></span>  

   6. <span data-ttu-id="cc626-270">Enter custom code to execute after the import completes in the override definition of `AfterPrimaryImport`>method.</span><span class="sxs-lookup"><span data-stu-id="cc626-270">Enter custom code to execute after the import completes in the override definition of `AfterPrimaryImport`>method.</span></span>                     <span data-ttu-id="cc626-271">The remaining flat files that were not imported earlier, before the solution import started, are imported now.</span><span class="sxs-lookup"><span data-stu-id="cc626-271">The remaining flat files that were not imported earlier, before the solution import started, are imported now.</span></span>  

   7. <span data-ttu-id="cc626-272">Change the default name of your package folder from PkgFolder to the package name that you want.</span><span class="sxs-lookup"><span data-stu-id="cc626-272">Change the default name of your package folder from PkgFolder to the package name that you want.</span></span>                     <span data-ttu-id="cc626-273">To do so, rename the `PkgFolder`>folder in the **Solution Explorer** pane, and then edit the return value under the                     `GetImportPackageDataFolderName` property.</span><span class="sxs-lookup"><span data-stu-id="cc626-273">To do so, rename the `PkgFolder`>folder in the **Solution Explorer** pane, and then edit the return value under the                     `GetImportPackageDataFolderName` property.</span></span>  

      ```csharp  

      public override string GetImportPackageDataFolderName  
      {  
      get  
      {  
      // WARNING this value directly correlates to the folder name in the Solution Explorer where the ImportConfig.xml and sub content is located.  
      // Changing this name requires that you also change the correlating name in the Solution Explorer  
      return "PkgFolder";  
      }  
      }  

      ```  

   8. <span data-ttu-id="cc626-274">Change the package name by editing the return value under the `GetNameOfImport` property.</span><span class="sxs-lookup"><span data-stu-id="cc626-274">Change the package name by editing the return value under the `GetNameOfImport` property.</span></span>  

      ```csharp  

      public override string GetNameOfImport(bool plural)  
      {  
      return "Package Short Name";  
      }  

      ```  

       <span data-ttu-id="cc626-275">This is the name of your package that will appear on the package selection page in the [!INCLUDE[pn_package_deployer_short](../includes/pn-package-deployer-short.md)] wizard.</span><span class="sxs-lookup"><span data-stu-id="cc626-275">This is the name of your package that will appear on the package selection page in the [!INCLUDE[pn_package_deployer_short](../includes/pn-package-deployer-short.md)] wizard.</span></span>  

   9. <span data-ttu-id="cc626-276">Change the package description by editing the return value under the `GetImportPackageDescriptionText` property.</span><span class="sxs-lookup"><span data-stu-id="cc626-276">Change the package description by editing the return value under the `GetImportPackageDescriptionText` property.</span></span>  

       ```csharp  

       public override string GetImportPackageDescriptionText  
       {  
       get { return "Package Description"; }  
       }  

       ```  

        <span data-ttu-id="cc626-277">This is the package description that will appear alongside the package name on the on the package selection page in the Package Deployer wizard.</span><span class="sxs-lookup"><span data-stu-id="cc626-277">This is the package description that will appear alongside the package name on the on the package selection page in the Package Deployer wizard.</span></span>  

   10. <span data-ttu-id="cc626-278">Change the package long name by editing the return value under the `GetLongNameOfImport` property.</span><span class="sxs-lookup"><span data-stu-id="cc626-278">Change the package long name by editing the return value under the `GetLongNameOfImport` property.</span></span>  

       ```csharp  

       public override string GetLongNameOfImport  
       {  
       get { return "Package Long Name"; }  
       }  

       ```  

        <span data-ttu-id="cc626-279">The package long name appears on the next page after you have selected the package to install.</span><span class="sxs-lookup"><span data-stu-id="cc626-279">The package long name appears on the next page after you have selected the package to install.</span></span>  

3. <span data-ttu-id="cc626-280">Additionally, the following function and variables are available to the package:</span><span class="sxs-lookup"><span data-stu-id="cc626-280">Additionally, the following function and variables are available to the package:</span></span>  


   |                                                                                                      <span data-ttu-id="cc626-281">Tên</span><span class="sxs-lookup"><span data-stu-id="cc626-281">Name</span></span>                                                                                                      |     <span data-ttu-id="cc626-282">Loại</span><span class="sxs-lookup"><span data-stu-id="cc626-282">Type</span></span>      |                                                                                                                                                                                                        <span data-ttu-id="cc626-283">Mô tả</span><span class="sxs-lookup"><span data-stu-id="cc626-283">Description</span></span>                                                                                                                                                                                                        |
   |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |                                            <xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.ImportExtension.CreateProgressItem(System.String)>                                            |   <span data-ttu-id="cc626-284">Hàm</span><span class="sxs-lookup"><span data-stu-id="cc626-284">Function</span></span>    |                                                                                                                                                                              <span data-ttu-id="cc626-285">Used to create a new progress item in the user interface (UI).</span><span class="sxs-lookup"><span data-stu-id="cc626-285">Used to create a new progress item in the user interface (UI).</span></span>                                                                                                                                                                               |
   | <xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.ImportExtension.RaiseUpdateEvent(System.String,Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.ProgressPanelItemStatus)> |   <span data-ttu-id="cc626-286">Hàm</span><span class="sxs-lookup"><span data-stu-id="cc626-286">Function</span></span>    | <span data-ttu-id="cc626-287">Used to update the progress created by the call to <xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.ImportExtension.CreateProgressItem(System.String)>.</span><span class="sxs-lookup"><span data-stu-id="cc626-287">Used to update the progress created by the call to <xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.ImportExtension.CreateProgressItem(System.String)>.</span></span><br /><br /> <span data-ttu-id="cc626-288"><xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.ProgressPanelItemStatus> is an enum with the following values:</span><span class="sxs-lookup"><span data-stu-id="cc626-288"><xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.ProgressPanelItemStatus> is an enum with the following values:</span></span><br /><br /> <span data-ttu-id="cc626-289">Working = 0</span><span class="sxs-lookup"><span data-stu-id="cc626-289">Working = 0</span></span><br /><span data-ttu-id="cc626-290">Complete = 1</span><span class="sxs-lookup"><span data-stu-id="cc626-290">Complete = 1</span></span><br /><span data-ttu-id="cc626-291">Failed = 2</span><span class="sxs-lookup"><span data-stu-id="cc626-291">Failed = 2</span></span><br /><span data-ttu-id="cc626-292">Warning = 3</span><span class="sxs-lookup"><span data-stu-id="cc626-292">Warning = 3</span></span><br /><span data-ttu-id="cc626-293">Unknown = 4</span><span class="sxs-lookup"><span data-stu-id="cc626-293">Unknown = 4</span></span> |
   |                                     <xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.ImportExtension.RaiseFailEvent(System.String,System.Exception)>                                      |   <span data-ttu-id="cc626-294">Hàm</span><span class="sxs-lookup"><span data-stu-id="cc626-294">Function</span></span>    |                                                                                                                                                                             <span data-ttu-id="cc626-295">Used to fail the current status import with an exception message.</span><span class="sxs-lookup"><span data-stu-id="cc626-295">Used to fail the current status import with an exception message.</span></span>                                                                                                                                                                             |
   |                                    <xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.ImportExtension.IsRoleAssoicatedWithTeam(System.Guid,System.Guid)>                                    |   <span data-ttu-id="cc626-296">Hàm</span><span class="sxs-lookup"><span data-stu-id="cc626-296">Function</span></span>    |                                                                                                                                                                             <span data-ttu-id="cc626-297">Used to determine if a role is associated with a specified team.</span><span class="sxs-lookup"><span data-stu-id="cc626-297">Used to determine if a role is associated with a specified team.</span></span>                                                                                                                                                                              |
   |                                              <xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.ImportExtension.IsWorkflowActive(System.Guid)>                                              |   <span data-ttu-id="cc626-298">Hàm</span><span class="sxs-lookup"><span data-stu-id="cc626-298">Function</span></span>    |                                                                                                                                                                                   <span data-ttu-id="cc626-299">Used to determine if a specified workflow is active.</span><span class="sxs-lookup"><span data-stu-id="cc626-299">Used to determine if a specified workflow is active.</span></span>                                                                                                                                                                                    |
   |                                                       <xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.ImportExtension.PackageLog>                                                        | <span data-ttu-id="cc626-300">Class Pointer</span><span class="sxs-lookup"><span data-stu-id="cc626-300">Class Pointer</span></span> |                                                                                                                            <span data-ttu-id="cc626-301">This is a pointer to the initialized logging interface for the package.</span><span class="sxs-lookup"><span data-stu-id="cc626-301">This is a pointer to the initialized logging interface for the package.</span></span> <span data-ttu-id="cc626-302">This interface is used by a package to log messages and exceptions to the package log file.</span><span class="sxs-lookup"><span data-stu-id="cc626-302">This interface is used by a package to log messages and exceptions to the package log file.</span></span>                                                                                                                            |
   |                                                  <xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.ImportExtension.RootControlDispatcher>                                                  |   <span data-ttu-id="cc626-303">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="cc626-303">Property</span></span>    |                                                         <span data-ttu-id="cc626-304">This is a dispatcher interface used to allow your control to render its own UI during package deployment.</span><span class="sxs-lookup"><span data-stu-id="cc626-304">This is a dispatcher interface used to allow your control to render its own UI during package deployment.</span></span> <span data-ttu-id="cc626-305">Use this interface to wrap any UI elements or commands.</span><span class="sxs-lookup"><span data-stu-id="cc626-305">Use this interface to wrap any UI elements or commands.</span></span>                         <span data-ttu-id="cc626-306">It is important to check this variable for null values before using it as it may or may not be set to a value.</span><span class="sxs-lookup"><span data-stu-id="cc626-306">It is important to check this variable for null values before using it as it may or may not be set to a value.</span></span>                                                          |
   |                                                         <xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.ImportExtension.CrmSvc>                                                          |   <span data-ttu-id="cc626-307">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="cc626-307">Property</span></span>    |                                                                                        <span data-ttu-id="cc626-308">This is a pointer to <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient> class that allows for a package to address Dynamics 365 for Customer Engagement apps from within the package.</span><span class="sxs-lookup"><span data-stu-id="cc626-308">This is a pointer to <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient> class that allows for a package to address Dynamics 365 for Customer Engagement apps from within the package.</span></span> <span data-ttu-id="cc626-309">Use this to execute SDK methods and other actions in the overridden methods.</span><span class="sxs-lookup"><span data-stu-id="cc626-309">Use this to execute SDK methods and other actions in the overridden methods.</span></span>                                                                                         |
   |                                                   <xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.IImportExtensions2.DataImportBypass>                                                   |   <span data-ttu-id="cc626-310">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="cc626-310">Property</span></span>    |                    <span data-ttu-id="cc626-311">Use this to specify whether [!INCLUDE[pn_package_deployer_short](../includes/pn-package-deployer-short.md)] apps skip all data import operations such as importing [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps sample data,                         flat file data, and data exported from the Configuration Migration tool.</span><span class="sxs-lookup"><span data-stu-id="cc626-311">Use this to specify whether [!INCLUDE[pn_package_deployer_short](../includes/pn-package-deployer-short.md)] apps skip all data import operations such as importing [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps sample data,                         flat file data, and data exported from the Configuration Migration tool.</span></span> <span data-ttu-id="cc626-312">Specify true or false.</span><span class="sxs-lookup"><span data-stu-id="cc626-312">Specify true or false.</span></span> <span data-ttu-id="cc626-313">Default is `false`.</span><span class="sxs-lookup"><span data-stu-id="cc626-313">Default is `false`.</span></span>                    |
   |                                            <xref:Microsoft.Xrm.Tooling.PackageDeployment.CrmPackageExtentionBase.IImportExtensions2.OverrideDataImportSafetyChecks>                                            |   <span data-ttu-id="cc626-314">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="cc626-314">Property</span></span>    |      <span data-ttu-id="cc626-315">Use this to specify whether [!INCLUDE[pn_package_deployer_short](../includes/pn-package-deployer-short.md)] will bypass some of its safety checks, which helps in improving the import performance.</span><span class="sxs-lookup"><span data-stu-id="cc626-315">Use this to specify whether [!INCLUDE[pn_package_deployer_short](../includes/pn-package-deployer-short.md)] will bypass some of its safety checks, which helps in improving the import performance.</span></span> <span data-ttu-id="cc626-316">Specify `true` or `false`.</span><span class="sxs-lookup"><span data-stu-id="cc626-316">Specify `true` or `false`.</span></span> <span data-ttu-id="cc626-317">Default is `false`.</span><span class="sxs-lookup"><span data-stu-id="cc626-317">Default is `false`.</span></span><br /><br /> <span data-ttu-id="cc626-318">You should set this to `true` only if the target [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance does not contain any data.</span><span class="sxs-lookup"><span data-stu-id="cc626-318">You should set this to `true` only if the target [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance does not contain any data.</span></span>      |


4. <span data-ttu-id="cc626-319">Save your project, and then build it (**Build** > **Build Solution**) to create the package.</span><span class="sxs-lookup"><span data-stu-id="cc626-319">Save your project, and then build it (**Build** > **Build Solution**) to create the package.</span></span> <span data-ttu-id="cc626-320">Your package is the following files under the *\<Project>* \Bin\Debug folder</span><span class="sxs-lookup"><span data-stu-id="cc626-320">Your package is the following files under the *\<Project>* \Bin\Debug folder</span></span>  

   - <span data-ttu-id="cc626-321">**\<PackageName> folder**: The folder name is the same as the one you changed for your package folder name in step 2.g of this section (Step 5: Define custom code for your package).</span><span class="sxs-lookup"><span data-stu-id="cc626-321">**\<PackageName> folder**: The folder name is the same as the one you changed for your package folder name in step 2.g of this section (Step 5: Define custom code for your package).</span></span> <span data-ttu-id="cc626-322">This folder contains  all solutions,  configuration data, flat files, and the contents for your package.</span><span class="sxs-lookup"><span data-stu-id="cc626-322">This folder contains  all solutions,  configuration data, flat files, and the contents for your package.</span></span>  

   - <span data-ttu-id="cc626-323">**\<PackageName>.dll**: The assembly contains the custom code for your package.</span><span class="sxs-lookup"><span data-stu-id="cc626-323">**\<PackageName>.dll**: The assembly contains the custom code for your package.</span></span> <span data-ttu-id="cc626-324">Theo mặc định, tên của cụm chính là tên dự án [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] của bạn.</span><span class="sxs-lookup"><span data-stu-id="cc626-324">By default, the name of the assembly is the same as your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project name.</span></span>  

     <span data-ttu-id="cc626-325">The next step is to deploy your package.</span><span class="sxs-lookup"><span data-stu-id="cc626-325">The next step is to deploy your package.</span></span>  

<a name="UsethePackage"></a>   
## <a name="deploy-a-package"></a><span data-ttu-id="cc626-326">Deploy a package</span><span class="sxs-lookup"><span data-stu-id="cc626-326">Deploy a package</span></span>  
 <span data-ttu-id="cc626-327">After you create a package, you can deploy it on the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance by using either the Package Deployer tool or [!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)].</span><span class="sxs-lookup"><span data-stu-id="cc626-327">After you create a package, you can deploy it on the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance by using either the Package Deployer tool or [!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)].</span></span> 

 <span data-ttu-id="cc626-328">The package deployer tool is distributed as part of the [Microsoft.CrmSdk.XrmTooling.PackageDeployment.WPF](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment) NuGet package.To download the package deployer tool, see [Download tools from NuGet](download-tools-nuget.md).</span><span class="sxs-lookup"><span data-stu-id="cc626-328">The package deployer tool is distributed as part of the [Microsoft.CrmSdk.XrmTooling.PackageDeployment.WPF](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment) NuGet package.To download the package deployer tool, see [Download tools from NuGet](download-tools-nuget.md).</span></span>

 <span data-ttu-id="cc626-329">For detailed information, see [Deploy packages using CRM Package Deployer or Windows PowerShell](https://technet.microsoft.com/library/dn647420.aspx).</span><span class="sxs-lookup"><span data-stu-id="cc626-329">For detailed information, see [Deploy packages using CRM Package Deployer or Windows PowerShell](https://technet.microsoft.com/library/dn647420.aspx).</span></span>  

<a name="BestPractices"></a>   
## <a name="best-practices-for-creating-and-deploying-packages"></a><span data-ttu-id="cc626-330">Best practices for creating and deploying packages</span><span class="sxs-lookup"><span data-stu-id="cc626-330">Best practices for creating and deploying packages</span></span>  
 <span data-ttu-id="cc626-331">While creating packages, developers must ensure that the package assemblies are signed.</span><span class="sxs-lookup"><span data-stu-id="cc626-331">While creating packages, developers must ensure that the package assemblies are signed.</span></span>  

 <span data-ttu-id="cc626-332">While deploying the packages, [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps administrators must:</span><span class="sxs-lookup"><span data-stu-id="cc626-332">While deploying the packages, [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps administrators must:</span></span>  

-   <span data-ttu-id="cc626-333">Insist on a signed package assembly so that you can track an assembly back to its source.</span><span class="sxs-lookup"><span data-stu-id="cc626-333">Insist on a signed package assembly so that you can track an assembly back to its source.</span></span>  

-   <span data-ttu-id="cc626-334">Test the package on a pre-production instance (preferably a mirror image of the production instance) before running it on a production instance.</span><span class="sxs-lookup"><span data-stu-id="cc626-334">Test the package on a pre-production instance (preferably a mirror image of the production instance) before running it on a production instance.</span></span>  

-   <span data-ttu-id="cc626-335">Back up the production instance before deploying the package.</span><span class="sxs-lookup"><span data-stu-id="cc626-335">Back up the production instance before deploying the package.</span></span>  

### <a name="see-also"></a><span data-ttu-id="cc626-336">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="cc626-336">See also</span></span>  
 [<span data-ttu-id="cc626-337">What's New for Developers</span><span class="sxs-lookup"><span data-stu-id="cc626-337">What's New for Developers</span></span>](whats-new-developers.md)
