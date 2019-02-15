---
title: Start a Dynamics 365 for Customer Engagement Web API project in Visual Studio (C#) (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Create a new project in Visual Studio to build a console application that uses Dynamics 365 for Customer Engagement Web API
ms.custom: ''
ms.date: 12/11/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 08377156-32c7-492a-8e66-50a47a330dc6
caps.latest.revision: 14
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 1d0f0746d70118b5b1445d18d94a1f6fc18e84b5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386586"
---
# <a name="start-a-dynamics-365-for-customer-engagement-web-api-project-in-visual-studio-c"></a><span data-ttu-id="cf72b-103">Start a Dynamics 365 for Customer Engagement Web API project in Visual Studio (C#)</span><span class="sxs-lookup"><span data-stu-id="cf72b-103">Start a Dynamics 365 for Customer Engagement Web API project in Visual Studio (C#)</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="cf72b-104">This topic demonstrates how to create a new project in [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] that builds a console application that uses the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps Web API.</span><span class="sxs-lookup"><span data-stu-id="cf72b-104">This topic demonstrates how to create a new project in [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] that builds a console application that uses the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps Web API.</span></span> <span data-ttu-id="cf72b-105">It illustrates the common references and project resources that most applications, including the SDK C# samples, use to implement Web API-based solutions.</span><span class="sxs-lookup"><span data-stu-id="cf72b-105">It illustrates the common references and project resources that most applications, including the SDK C# samples, use to implement Web API-based solutions.</span></span>  
  
<a name="bkmk_prerequisites"></a>   
## <a name="prerequisites"></a><span data-ttu-id="cf72b-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="cf72b-106">Prerequisites</span></span>  
 <span data-ttu-id="cf72b-107">The following prerequisites are required to build the console application described in this section.</span><span class="sxs-lookup"><span data-stu-id="cf72b-107">The following prerequisites are required to build the console application described in this section.</span></span>  
  
- [!INCLUDE[pn_microsoft_visual_studio_2015](../../includes/pn-microsoft-visual-studio-2015.md)] <span data-ttu-id="cf72b-108">installed on your development computer.</span><span class="sxs-lookup"><span data-stu-id="cf72b-108">installed on your development computer.</span></span> <span data-ttu-id="cf72b-109">Any edition, including [Visual Studio Express](https://www.visualstudio.com/products/visual-studio-express-vs.aspx), should be sufficient to work with the Dynamics 365 for Customer Engagement Web API.</span><span class="sxs-lookup"><span data-stu-id="cf72b-109">Any edition, including [Visual Studio Express](https://www.visualstudio.com/products/visual-studio-express-vs.aspx), should be sufficient to work with the Dynamics 365 for Customer Engagement Web API.</span></span>
  
- <span data-ttu-id="cf72b-110">A [!INCLUDE[tn_nuget](../../includes/tn-nuget.md)] client must be installed: either the command-line utility or the Visual Studio extension.</span><span class="sxs-lookup"><span data-stu-id="cf72b-110">A [!INCLUDE[tn_nuget](../../includes/tn-nuget.md)] client must be installed: either the command-line utility or the Visual Studio extension.</span></span> <span data-ttu-id="cf72b-111">For more information, see [Installing NuGet](https://docs.nuget.org/consume/installing-nuget).</span><span class="sxs-lookup"><span data-stu-id="cf72b-111">For more information, see [Installing NuGet](https://docs.nuget.org/consume/installing-nuget).</span></span>  
  
- <span data-ttu-id="cf72b-112">An internet connection is required to download the [!INCLUDE[tn_nuget](../../includes/tn-nuget.md)] package containing the Dynamics 365 for Customer Engagement Web API Helper Library, and other dependent packages.</span><span class="sxs-lookup"><span data-stu-id="cf72b-112">An internet connection is required to download the [!INCLUDE[tn_nuget](../../includes/tn-nuget.md)] package containing the Dynamics 365 for Customer Engagement Web API Helper Library, and other dependent packages.</span></span>
  
<a name="bkmk_createProject"></a>   
## <a name="create-a-project"></a><span data-ttu-id="cf72b-113">Tạo dự án</span><span class="sxs-lookup"><span data-stu-id="cf72b-113">Create a project</span></span>  
 <span data-ttu-id="cf72b-114">The following procedure demonstrates how to create a console application project in C# that uses the [!INCLUDE[pn_Microsoft_.Net_Framework](../../includes/pn-microsoft-net-framework.md)].</span><span class="sxs-lookup"><span data-stu-id="cf72b-114">The following procedure demonstrates how to create a console application project in C# that uses the [!INCLUDE[pn_Microsoft_.Net_Framework](../../includes/pn-microsoft-net-framework.md)].</span></span> <span data-ttu-id="cf72b-115">For more information on supported versions of the .NET Framework, see [Supported extensions](../supported-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="cf72b-115">For more information on supported versions of the .NET Framework, see [Supported extensions](../supported-extensions.md).</span></span>  
  
<a name="bkmk_newProject"></a>   
### <a name="new-project"></a><span data-ttu-id="cf72b-116">New Project</span><span class="sxs-lookup"><span data-stu-id="cf72b-116">New Project</span></span>  
  
1. <span data-ttu-id="cf72b-117">In [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)], click **New Project**.</span><span class="sxs-lookup"><span data-stu-id="cf72b-117">In [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)], click **New Project**.</span></span> <span data-ttu-id="cf72b-118">The **New Project** dialog is displayed.</span><span class="sxs-lookup"><span data-stu-id="cf72b-118">The **New Project** dialog is displayed.</span></span>  
  
2. <span data-ttu-id="cf72b-119">In the left navigation pane under **Templates**, select **Visual C#**.</span><span class="sxs-lookup"><span data-stu-id="cf72b-119">In the left navigation pane under **Templates**, select **Visual C#**.</span></span>  
  
3. <span data-ttu-id="cf72b-120">Above the list of available templates, select **.NET Framework 4.5.2**.</span><span class="sxs-lookup"><span data-stu-id="cf72b-120">Above the list of available templates, select **.NET Framework 4.5.2**.</span></span>  
  
4. <span data-ttu-id="cf72b-121">In the list of templates, select **Console Application**.</span><span class="sxs-lookup"><span data-stu-id="cf72b-121">In the list of templates, select **Console Application**.</span></span> <span data-ttu-id="cf72b-122">(Alternately choose the project type suited to your solution.)  All of the Web API C# samples are console applications.</span><span class="sxs-lookup"><span data-stu-id="cf72b-122">(Alternately choose the project type suited to your solution.)  All of the Web API C# samples are console applications.</span></span>  
  
   <span data-ttu-id="cf72b-123">![A new console app project dialog in Dynamics 365 for Customer Engagement apps](../media/new-project.PNG "A new console app project dialog in Dynamics 365 for Customer Engagement apps")</span><span class="sxs-lookup"><span data-stu-id="cf72b-123">![A new console app project dialog in Dynamics 365 for Customer Engagement apps](../media/new-project.PNG "A new console app project dialog in Dynamics 365 for Customer Engagement apps")</span></span>  
  
5. <span data-ttu-id="cf72b-124">In the text boxes near the bottom of the form, supply the project name and location, and then select OK.</span><span class="sxs-lookup"><span data-stu-id="cf72b-124">In the text boxes near the bottom of the form, supply the project name and location, and then select OK.</span></span> <span data-ttu-id="cf72b-125">(For this topic, the solution name “StartWebAPI-CS” was used.) The initial solution files will be generated and the solution loaded into [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)].</span><span class="sxs-lookup"><span data-stu-id="cf72b-125">(For this topic, the solution name “StartWebAPI-CS” was used.) The initial solution files will be generated and the solution loaded into [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)].</span></span>  
  
6. <span data-ttu-id="cf72b-126">Under the **Project** menu, open the project’s properties form and verify the target framework is set to **.NET Framework 4.5.2**.</span><span class="sxs-lookup"><span data-stu-id="cf72b-126">Under the **Project** menu, open the project’s properties form and verify the target framework is set to **.NET Framework 4.5.2**.</span></span>  
  
<a name="bkmk_addAllRequiredResources"></a>   
### <a name="add-all-required-resources-to-your-project"></a><span data-ttu-id="cf72b-127">Add all required resources to your project</span><span class="sxs-lookup"><span data-stu-id="cf72b-127">Add all required resources to your project</span></span>  
 <span data-ttu-id="cf72b-128">The following procedures explain how to add all required managed references and packages to your project.</span><span class="sxs-lookup"><span data-stu-id="cf72b-128">The following procedures explain how to add all required managed references and packages to your project.</span></span> <span data-ttu-id="cf72b-129">Consider this a base set of resources that most managed code applications will need for invoking Web API operations.</span><span class="sxs-lookup"><span data-stu-id="cf72b-129">Consider this a base set of resources that most managed code applications will need for invoking Web API operations.</span></span>  
  
#### <a name="add-the-helper-library-nuget-package"></a><span data-ttu-id="cf72b-130">Add the helper library NuGet package</span><span class="sxs-lookup"><span data-stu-id="cf72b-130">Add the helper library NuGet package</span></span>  
 <span data-ttu-id="cf72b-131">The Dynamics 365 for Customer Engagement Web API Helper Library contains classes to assist with supplemental operations, such as application configuration, Dynamics 365 for Customer Engagement server authentication, exception handling, and Web communication.</span><span class="sxs-lookup"><span data-stu-id="cf72b-131">The Dynamics 365 for Customer Engagement Web API Helper Library contains classes to assist with supplemental operations, such as application configuration, Dynamics 365 for Customer Engagement server authentication, exception handling, and Web communication.</span></span> <span data-ttu-id="cf72b-132">For more information, see [Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md).</span><span class="sxs-lookup"><span data-stu-id="cf72b-132">For more information, see [Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md).</span></span> <span data-ttu-id="cf72b-133">The use of these classes is optional, although they are used extensively in the Web API samples.</span><span class="sxs-lookup"><span data-stu-id="cf72b-133">The use of these classes is optional, although they are used extensively in the Web API samples.</span></span>  <span data-ttu-id="cf72b-134">The Dynamics 365 for Customer Engagement Web API Helper Library is distributed in source code form as a NuGet package.</span><span class="sxs-lookup"><span data-stu-id="cf72b-134">The Dynamics 365 for Customer Engagement Web API Helper Library is distributed in source code form as a NuGet package.</span></span>  <span data-ttu-id="cf72b-135">Future updates will be distributed as NuGet package updates.</span><span class="sxs-lookup"><span data-stu-id="cf72b-135">Future updates will be distributed as NuGet package updates.</span></span>  
  
 <span data-ttu-id="cf72b-136">If you have installed the NuGet command line utility or are using the Package Manager Console in Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="cf72b-136">If you have installed the NuGet command line utility or are using the Package Manager Console in Visual Studio:</span></span>  
  
1. <span data-ttu-id="cf72b-137">Issue the following command to install the helper library package.</span><span class="sxs-lookup"><span data-stu-id="cf72b-137">Issue the following command to install the helper library package.</span></span>  
  
    `Install-Package Microsoft.CrmSdk.WebApi.Samples.HelperCode`  
  
2. <span data-ttu-id="cf72b-138">Several messages are displayed about processing dependency packages.</span><span class="sxs-lookup"><span data-stu-id="cf72b-138">Several messages are displayed about processing dependency packages.</span></span> <span data-ttu-id="cf72b-139">If a **License Acceptance** dialog is displayed, read the license terms and click **Accept**.</span><span class="sxs-lookup"><span data-stu-id="cf72b-139">If a **License Acceptance** dialog is displayed, read the license terms and click **Accept**.</span></span>  
  
3. <span data-ttu-id="cf72b-140">Skip to step 6 below to confirm the installation of the helper library package.</span><span class="sxs-lookup"><span data-stu-id="cf72b-140">Skip to step 6 below to confirm the installation of the helper library package.</span></span>  
  
 <span data-ttu-id="cf72b-141">If you have installed the NuGet Package Manager extension:</span><span class="sxs-lookup"><span data-stu-id="cf72b-141">If you have installed the NuGet Package Manager extension:</span></span>  
  
1. <span data-ttu-id="cf72b-142">From the **Project** menu, select **Manage NuGet Packages**.</span><span class="sxs-lookup"><span data-stu-id="cf72b-142">From the **Project** menu, select **Manage NuGet Packages**.</span></span>  <span data-ttu-id="cf72b-143">The **NuGet Package Manager** tab is displayed.</span><span class="sxs-lookup"><span data-stu-id="cf72b-143">The **NuGet Package Manager** tab is displayed.</span></span>  
  
2. <span data-ttu-id="cf72b-144">In the upper right-hand corner, set the **Package** source drop-down to **Nuget.org**.</span><span class="sxs-lookup"><span data-stu-id="cf72b-144">In the upper right-hand corner, set the **Package** source drop-down to **Nuget.org**.</span></span>  
  
3. <span data-ttu-id="cf72b-145">In the upper left-hand corner, click on **Browse** then enter “`Dynamics 365 for Customer Engagement apps HelperCode`” in the search box and press Enter.</span><span class="sxs-lookup"><span data-stu-id="cf72b-145">In the upper left-hand corner, click on **Browse** then enter “`Dynamics 365 for Customer Engagement apps HelperCode`” in the search box and press Enter.</span></span>  
  
   <span data-ttu-id="cf72b-146">![NuGet Package Manager showing Dynamics 365 for Customer Engagement apps Helper Code Library (C#)](../media/package-manifest-helper-code.png "NuGet Package Manager showing Dynamics 365 for Customer Engagement apps Helper Code Library (C#)")</span><span class="sxs-lookup"><span data-stu-id="cf72b-146">![NuGet Package Manager showing Dynamics 365 for Customer Engagement apps Helper Code Library (C#)](../media/package-manifest-helper-code.png "NuGet Package Manager showing Dynamics 365 for Customer Engagement apps Helper Code Library (C#)")</span></span>  
  
4. <span data-ttu-id="cf72b-147">Bấm vào **cài đặt**.</span><span class="sxs-lookup"><span data-stu-id="cf72b-147">Click **Install**.</span></span>  <span data-ttu-id="cf72b-148">If the **Preview** dialog is displayed, click **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf72b-148">If the **Preview** dialog is displayed, click **OK**.</span></span>  
  
5. <span data-ttu-id="cf72b-149">The **License Acceptance** dialog is displayed.</span><span class="sxs-lookup"><span data-stu-id="cf72b-149">The **License Acceptance** dialog is displayed.</span></span> <span data-ttu-id="cf72b-150">Review the license terms and click **I Accept**.</span><span class="sxs-lookup"><span data-stu-id="cf72b-150">Review the license terms and click **I Accept**.</span></span>  
  
6. <span data-ttu-id="cf72b-151">Navigate to the **Solution Explorer** window.</span><span class="sxs-lookup"><span data-stu-id="cf72b-151">Navigate to the **Solution Explorer** window.</span></span> <span data-ttu-id="cf72b-152">Confirm that a new solution folder named **Web API Helper Code** was added.</span><span class="sxs-lookup"><span data-stu-id="cf72b-152">Confirm that a new solution folder named **Web API Helper Code** was added.</span></span>  
  
   <span data-ttu-id="cf72b-153">![VS Solution Explorer showing helper library files](../media/solution-explorer-helper-code.PNG "VS Solution Explorer showing helper library files")</span><span class="sxs-lookup"><span data-stu-id="cf72b-153">![VS Solution Explorer showing helper library files](../media/solution-explorer-helper-code.PNG "VS Solution Explorer showing helper library files")</span></span>  
  
   <span data-ttu-id="cf72b-154">The Dynamics 365 for Customer Engagement apps SDK Web API Helper Library package, [Microsoft.CrmSdk.WebApi.Samples.HelperCode](https://www.nuget.org/packages/Microsoft.CrmSdk.WebApi.Samples.HelperCode), depends upon the following other packages, which are automatically downloaded and installed alongside the helper library package:</span><span class="sxs-lookup"><span data-stu-id="cf72b-154">The Dynamics 365 for Customer Engagement apps SDK Web API Helper Library package, [Microsoft.CrmSdk.WebApi.Samples.HelperCode](https://www.nuget.org/packages/Microsoft.CrmSdk.WebApi.Samples.HelperCode), depends upon the following other packages, which are automatically downloaded and installed alongside the helper library package:</span></span>  
  
-   <span data-ttu-id="cf72b-155">[Newtonsoft.Json](https://www.nuget.org/packages/Newtonsoft.Json) – contains [Json.NET](http://www.newtonsoft.com/json), a popular, MIT-licensed JSON framework for .NET.</span><span class="sxs-lookup"><span data-stu-id="cf72b-155">[Newtonsoft.Json](https://www.nuget.org/packages/Newtonsoft.Json) – contains [Json.NET](http://www.newtonsoft.com/json), a popular, MIT-licensed JSON framework for .NET.</span></span>  
  
-   <span data-ttu-id="cf72b-156">[Microsoft.IdentityModel.Clients.ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/) – contains the binaries for the Active Directory Authentication Library ([ADAL](https://msdn.microsoft.com/library/azure/mt417579.aspx)), which provides authentication functionality for .NET clients.</span><span class="sxs-lookup"><span data-stu-id="cf72b-156">[Microsoft.IdentityModel.Clients.ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/) – contains the binaries for the Active Directory Authentication Library ([ADAL](https://msdn.microsoft.com/library/azure/mt417579.aspx)), which provides authentication functionality for .NET clients.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="cf72b-157">The Dynamics 365 for Customer Engagement apps SDK Web API Helper Library package was built against specific versions of these other two supporting packages.</span><span class="sxs-lookup"><span data-stu-id="cf72b-157">The Dynamics 365 for Customer Engagement apps SDK Web API Helper Library package was built against specific versions of these other two supporting packages.</span></span>  <span data-ttu-id="cf72b-158">Because of this, you should only directly update the helper library NuGet package.</span><span class="sxs-lookup"><span data-stu-id="cf72b-158">Because of this, you should only directly update the helper library NuGet package.</span></span>  <span data-ttu-id="cf72b-159">This operation will update the proper supporting packages if required.</span><span class="sxs-lookup"><span data-stu-id="cf72b-159">This operation will update the proper supporting packages if required.</span></span>  <span data-ttu-id="cf72b-160">If you separately update one of these supporting packages, a newer version of that package may be incompatible with the helper library.</span><span class="sxs-lookup"><span data-stu-id="cf72b-160">If you separately update one of these supporting packages, a newer version of that package may be incompatible with the helper library.</span></span>  
  
#### <a name="verify-the-required-assembly-references"></a><span data-ttu-id="cf72b-161">Verify the required assembly references</span><span class="sxs-lookup"><span data-stu-id="cf72b-161">Verify the required assembly references</span></span>  
  
1. <span data-ttu-id="cf72b-162">In **Solution Explorer**, expand the **References** node.</span><span class="sxs-lookup"><span data-stu-id="cf72b-162">In **Solution Explorer**, expand the **References** node.</span></span>  
  
2. <span data-ttu-id="cf72b-163">Confirm the at the following references have been added to the project.</span><span class="sxs-lookup"><span data-stu-id="cf72b-163">Confirm the at the following references have been added to the project.</span></span>  
  
   <span data-ttu-id="cf72b-164">![VS Solution Explorer showing references for the helper library](../media/solution-explorer-references-helper-code.png "VS Solution Explorer showing references for the helper library")</span><span class="sxs-lookup"><span data-stu-id="cf72b-164">![VS Solution Explorer showing references for the helper library](../media/solution-explorer-references-helper-code.png "VS Solution Explorer showing references for the helper library")</span></span>  
  
3. <span data-ttu-id="cf72b-165">If you have additional functionality that you routinely use in your applications, you can add the associated references to the required assemblies now.</span><span class="sxs-lookup"><span data-stu-id="cf72b-165">If you have additional functionality that you routinely use in your applications, you can add the associated references to the required assemblies now.</span></span> <span data-ttu-id="cf72b-166">For more information, see [How to: Add or Remove References by Using the Add Reference Dialog Box](https://msdn.microsoft.com/library/wkze6zky.aspx).</span><span class="sxs-lookup"><span data-stu-id="cf72b-166">For more information, see [How to: Add or Remove References by Using the Add Reference Dialog Box](https://msdn.microsoft.com/library/wkze6zky.aspx).</span></span>  
  
   <span data-ttu-id="cf72b-167">Because the Dynamics 365 for Customer Engagement Web API is based on REST principles, it does not require client-side assemblies to access.</span><span class="sxs-lookup"><span data-stu-id="cf72b-167">Because the Dynamics 365 for Customer Engagement Web API is based on REST principles, it does not require client-side assemblies to access.</span></span>  <span data-ttu-id="cf72b-168">However, other APIs supported by Dynamics 365 for Customer Engagement apps do require these; for more information, see [Assemblies included in Dynamics 365 for Customer Engagement apps SDK](../org-service/assemblies-included-sdk.md).</span><span class="sxs-lookup"><span data-stu-id="cf72b-168">However, other APIs supported by Dynamics 365 for Customer Engagement apps do require these; for more information, see [Assemblies included in Dynamics 365 for Customer Engagement apps SDK](../org-service/assemblies-included-sdk.md).</span></span>  
  
#### <a name="add-typical-using-statements"></a><span data-ttu-id="cf72b-169">Add typical using statements</span><span class="sxs-lookup"><span data-stu-id="cf72b-169">Add typical using statements</span></span>  
  
1.  <span data-ttu-id="cf72b-170">In the **Solution Explorer**, open **Program.cs** for editing.</span><span class="sxs-lookup"><span data-stu-id="cf72b-170">In the **Solution Explorer**, open **Program.cs** for editing.</span></span>  
  
2.  <span data-ttu-id="cf72b-171">At the top of the file, add the following `using` statements, which reference namespaces commonly used in Dynamics 365 for Customer Engagement Web API-based solutions.</span><span class="sxs-lookup"><span data-stu-id="cf72b-171">At the top of the file, add the following `using` statements, which reference namespaces commonly used in Dynamics 365 for Customer Engagement Web API-based solutions.</span></span>  
  
    ```csharp
    using Microsoft.Crm.Sdk.Samples.HelperCode;  
    using Newtonsoft.Json;  
    using Newtonsoft.Json.Linq;  
    using System.Net.Http;  
    using System.Net.Http.Headers;
    ```  
  
3.  <span data-ttu-id="cf72b-172">If you added routinely used assemblies or references in the previous sections, you may also want to add corresponding `using` statements for these resources.</span><span class="sxs-lookup"><span data-stu-id="cf72b-172">If you added routinely used assemblies or references in the previous sections, you may also want to add corresponding `using` statements for these resources.</span></span>  
  
4.  <span data-ttu-id="cf72b-173">Save the file.</span><span class="sxs-lookup"><span data-stu-id="cf72b-173">Save the file.</span></span>  
  
<a name="bkmk_addConnectionCode"></a>
 
### <a name="add-connection-code"></a><span data-ttu-id="cf72b-174">Add connection code</span><span class="sxs-lookup"><span data-stu-id="cf72b-174">Add connection code</span></span>

 <span data-ttu-id="cf72b-175">This section explains how to add a basic set of settings and instructions to perform these operations.</span><span class="sxs-lookup"><span data-stu-id="cf72b-175">This section explains how to add a basic set of settings and instructions to perform these operations.</span></span>  <span data-ttu-id="cf72b-176">For more information about the common code used, see [Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md)</span><span class="sxs-lookup"><span data-stu-id="cf72b-176">For more information about the common code used, see [Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md)</span></span>  
  
#### <a name="edit-the-application-configuration-file"></a><span data-ttu-id="cf72b-177">Edit the application configuration file</span><span class="sxs-lookup"><span data-stu-id="cf72b-177">Edit the application configuration file</span></span>
  
1.  <span data-ttu-id="cf72b-178">In **Solution Explorer**, open the **App.config** file for editing.</span><span class="sxs-lookup"><span data-stu-id="cf72b-178">In **Solution Explorer**, open the **App.config** file for editing.</span></span>  <span data-ttu-id="cf72b-179">Add the following two sections to it, after the existing `<startup>` section, then save the file.</span><span class="sxs-lookup"><span data-stu-id="cf72b-179">Add the following two sections to it, after the existing `<startup>` section, then save the file.</span></span>  
  
    ```xml  
  
    <connectionStrings>  
        <clear />  
  
        <!-- When providing a password, make sure to set the app.config file's security so that only you can read it. -->  
        <add name="default"   connectionString="Url=http://myserver/myorg/; Username=name; Password=password; Domain=domain" />  
        <add name="CrmOnline" connectionString="Url=https://mydomain.crm.dynamics.com/; Username=someone@mydomain.onmicrosoft.com; Password=password" />  
      </connectionStrings>  
  
      <appSettings>  
        <!--For information on how to register an app and obtain the ClientId and RedirectUrl  
            values see https://msdn.microsoft.com/dynamics/crm/mt149065 -->  
        <!--Active Directory application registration. -->  
        <!--These are dummy values and should be replaced with your actual app registration values.-->  
        <add key="ClientId" value="e5cf0024-a66a-4f16-85ce-99ba97a24bb2" />  
        <add key="RedirectUrl" value="http://localhost/SdkSample" />  
  
        <!-- Use an alternate configuration file for connection string and setting values. This optional setting  
        enables use of an app.config file shared among multiple applications. If the specified file does  
        not exist, this setting is ignored.-->  
        <add key="AlternateConfig" value="C:\Temp\crmsample.exe.config"/>  
      </appSettings>  
  
    ```  
  
2.  <span data-ttu-id="cf72b-180">When developing or deploying a solution, the actual connection and application registration values must be substituted for the example placeholder values.</span><span class="sxs-lookup"><span data-stu-id="cf72b-180">When developing or deploying a solution, the actual connection and application registration values must be substituted for the example placeholder values.</span></span>  <span data-ttu-id="cf72b-181">For more information, see [Helper code: Configuration classes](web-api-helper-code-configuration-classes.md).</span><span class="sxs-lookup"><span data-stu-id="cf72b-181">For more information, see [Helper code: Configuration classes](web-api-helper-code-configuration-classes.md).</span></span>  
  
<a name="bkmk_addCodeToCallHelperLibrary"></a>

#### <a name="add-code-to-call-the-helper-library"></a><span data-ttu-id="cf72b-182">Add code to call the helper library</span><span class="sxs-lookup"><span data-stu-id="cf72b-182">Add code to call the helper library</span></span>
  
1.  <span data-ttu-id="cf72b-183">Edit the Program.cs file.</span><span class="sxs-lookup"><span data-stu-id="cf72b-183">Edit the Program.cs file.</span></span>  
  
2.  <span data-ttu-id="cf72b-184">Add the following property to the Program class.</span><span class="sxs-lookup"><span data-stu-id="cf72b-184">Add the following property to the Program class.</span></span>  <span data-ttu-id="cf72b-185">This property will be initialized after a successful connection to a Dynamics 365 for Customer Engagement server.</span><span class="sxs-lookup"><span data-stu-id="cf72b-185">This property will be initialized after a successful connection to a Dynamics 365 for Customer Engagement server.</span></span>  
  
     `private HttpClient httpClient;`  
  
3.  <span data-ttu-id="cf72b-186">In the `Main` method, add the following statements.</span><span class="sxs-lookup"><span data-stu-id="cf72b-186">In the `Main` method, add the following statements.</span></span>  
  
    ```csharp  
  
    Program app = new Program();  
    try  
    {  
        String[] arguments = Environment.GetCommandLineArgs();  
        app.ConnectToCRM(arguments);  
    }  
    catch (System.Exception ex)  
    { ; }  
    finally  
    {  
        if (app.httpClient != null)  
        { app.httpClient.Dispose(); }  
    }  
  
    ```  
  
4.  <span data-ttu-id="cf72b-187">Next add the `ConnectToCRM` method, which uses the helper library `Configuration` and `Authentication` classes.</span><span class="sxs-lookup"><span data-stu-id="cf72b-187">Next add the `ConnectToCRM` method, which uses the helper library `Configuration` and `Authentication` classes.</span></span>  <span data-ttu-id="cf72b-188">The following code demonstrates assigning  values to the [HttpClient](https://msdn.microsoft.com/library/system.net.http.httpclient\(v=vs.118\).aspx) properties so that you can successfully access the release version of the Dynamics 365 for Customer Engagement Web API.</span><span class="sxs-lookup"><span data-stu-id="cf72b-188">The following code demonstrates assigning  values to the [HttpClient](https://msdn.microsoft.com/library/system.net.http.httpclient\(v=vs.118\).aspx) properties so that you can successfully access the release version of the Dynamics 365 for Customer Engagement Web API.</span></span>  
  
    ```csharp  
  
    private void ConnectToCRM(String[] cmdargs)  
    {  
        Configuration config = null;  
        if (cmdargs.Length > 0)  
            config = new FileConfiguration(cmdargs[0]);  
        else  
            config = new FileConfiguration(null);  
        Authentication auth = new Authentication(config);  
        httpClient = new HttpClient(auth.ClientHandler, true);  
        httpClient.BaseAddress = new Uri(config.ServiceUrl + "api/data/v8.1/");  
        httpClient.Timeout = new TimeSpan(0, 2, 0);  
        httpClient.DefaultRequestHeaders.Add("OData-MaxVersion", "4.0");  
        httpClient.DefaultRequestHeaders.Add("OData-Version", "4.0");  
        httpClient.DefaultRequestHeaders.Accept.Add(  
            new MediaTypeWithQualityHeaderValue("application/json"));  
    }  
  
    ```  
  
<a name="bkmk_addErrorHandlingCode"></a>

### <a name="add-error-handling-code"></a><span data-ttu-id="cf72b-189">Add error-handling code</span><span class="sxs-lookup"><span data-stu-id="cf72b-189">Add error-handling code</span></span>

 <span data-ttu-id="cf72b-190">The following changes add code to catch and report exceptions, including Web API errors, to the console.</span><span class="sxs-lookup"><span data-stu-id="cf72b-190">The following changes add code to catch and report exceptions, including Web API errors, to the console.</span></span>  <span data-ttu-id="cf72b-191">If you are targeting a different environment, then modify the exception-handling code appropriately for that environment.</span><span class="sxs-lookup"><span data-stu-id="cf72b-191">If you are targeting a different environment, then modify the exception-handling code appropriately for that environment.</span></span>  
  
1.  <span data-ttu-id="cf72b-192">In `Main`, add the following statement to the `catch` block.</span><span class="sxs-lookup"><span data-stu-id="cf72b-192">In `Main`, add the following statement to the `catch` block.</span></span>  
  
     `DisplayException(ex);`  
  
2.  <span data-ttu-id="cf72b-193">Add the corresponding method to the `Program` class.</span><span class="sxs-lookup"><span data-stu-id="cf72b-193">Add the corresponding method to the `Program` class.</span></span>  
  
    ```csharp  
  
    private static void DisplayException(Exception ex)  
    {  
        Console.WriteLine("The application terminated with an error.");  
        Console.WriteLine(ex.Message);  
        while (ex.InnerException != null)  
        {  
            Console.WriteLine("\t* {0}", ex.InnerException.Message);  
            ex = ex.InnerException;  
        }  
    }  
  
    ```  
  
3.  <span data-ttu-id="cf72b-194">Save all the files in the solution.</span><span class="sxs-lookup"><span data-stu-id="cf72b-194">Save all the files in the solution.</span></span>  
  
<a name="bkmk_nextSteps"></a>

### <a name="next-steps"></a><span data-ttu-id="cf72b-195">Bước tiếp theo</span><span class="sxs-lookup"><span data-stu-id="cf72b-195">Next steps</span></span>

 <span data-ttu-id="cf72b-196">At this point the solution can be built without errors.</span><span class="sxs-lookup"><span data-stu-id="cf72b-196">At this point the solution can be built without errors.</span></span>  <span data-ttu-id="cf72b-197">If you edit the application configuration file to supply values for your [!INCLUDE[pn_microsoftcrm_server](../../includes/pn-microsoftcrm-server.md)], the program should also successfully connect to that server.</span><span class="sxs-lookup"><span data-stu-id="cf72b-197">If you edit the application configuration file to supply values for your [!INCLUDE[pn_microsoftcrm_server](../../includes/pn-microsoftcrm-server.md)], the program should also successfully connect to that server.</span></span>  <span data-ttu-id="cf72b-198">The solution represents a skeletal frame that is ready to accept custom code, including calls to the Dynamics 365 for Customer Engagement Web API.</span><span class="sxs-lookup"><span data-stu-id="cf72b-198">The solution represents a skeletal frame that is ready to accept custom code, including calls to the Dynamics 365 for Customer Engagement Web API.</span></span>  
  
> [!TIP]
>  <span data-ttu-id="cf72b-199">Before you leave this topic, consider saving your project as a project template.</span><span class="sxs-lookup"><span data-stu-id="cf72b-199">Before you leave this topic, consider saving your project as a project template.</span></span> <span data-ttu-id="cf72b-200">You can then reuse that template for future learning projects and save yourself some time and effort in setting up new projects.</span><span class="sxs-lookup"><span data-stu-id="cf72b-200">You can then reuse that template for future learning projects and save yourself some time and effort in setting up new projects.</span></span> <span data-ttu-id="cf72b-201">To do this, while your project is open in Microsoft Visual Studio, in the **File** menu select **Export template**.</span><span class="sxs-lookup"><span data-stu-id="cf72b-201">To do this, while your project is open in Microsoft Visual Studio, in the **File** menu select **Export template**.</span></span> <span data-ttu-id="cf72b-202">Follow the [Export Template Wizard](https://msdn.microsoft.com/library/xkh1wxd8.aspx) instructions to create the template.</span><span class="sxs-lookup"><span data-stu-id="cf72b-202">Follow the [Export Template Wizard](https://msdn.microsoft.com/library/xkh1wxd8.aspx) instructions to create the template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="cf72b-203">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="cf72b-203">See also</span></span>

 <span data-ttu-id="cf72b-204">[Get Started with the Web API (C#)](get-started-dynamics-365-web-api-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="cf72b-204">[Get Started with the Web API (C#)](get-started-dynamics-365-web-api-csharp.md) </span></span>  
 <span data-ttu-id="cf72b-205">[Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="cf72b-205">[Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md) </span></span>  
 [<span data-ttu-id="cf72b-206">Perform operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="cf72b-206">Perform operations using the Web API</span></span>](perform-operations-web-api.md)
