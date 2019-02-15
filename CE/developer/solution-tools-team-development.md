---
title: Solution tools for team development (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: This topic gives details about tools that can be used for team development of Dynamics 365 for Customer Engagement solutions and for source code control
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: af0cb38e-58f4-4aa6-82c4-da67f07115f9
caps.latest.revision: 17
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9278d0d7a58cfbaf332da37e5bf211ee069c30bf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388202"
---
# <a name="solution-tools-for-team-development"></a><span data-ttu-id="3c186-103">Solution tools for team development</span><span class="sxs-lookup"><span data-stu-id="3c186-103">Solution tools for team development</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3c186-104">A [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] solution is a compressed (.zip) file that contains multiple customized components that have been exported from a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server so that they may be transported and imported into another server.</span><span class="sxs-lookup"><span data-stu-id="3c186-104">A [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] solution is a compressed (.zip) file that contains multiple customized components that have been exported from a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server so that they may be transported and imported into another server.</span></span> <span data-ttu-id="3c186-105">However, a solution file is a single binary file that does not lend itself to source code control or team development.</span><span class="sxs-lookup"><span data-stu-id="3c186-105">However, a solution file is a single binary file that does not lend itself to source code control or team development.</span></span> <span data-ttu-id="3c186-106">There is no way for multiple developers to work on the custom components in the solution.</span><span class="sxs-lookup"><span data-stu-id="3c186-106">There is no way for multiple developers to work on the custom components in the solution.</span></span>  
  
 <span data-ttu-id="3c186-107">The SolutionPackager tool resolves the problem of source code control and team development of solution files.</span><span class="sxs-lookup"><span data-stu-id="3c186-107">The SolutionPackager tool resolves the problem of source code control and team development of solution files.</span></span> <span data-ttu-id="3c186-108">The tool identifies individual components in the compressed solution file and extracts them out to individual files.</span><span class="sxs-lookup"><span data-stu-id="3c186-108">The tool identifies individual components in the compressed solution file and extracts them out to individual files.</span></span> <span data-ttu-id="3c186-109">The tool can also re-create a solution file by packing the files that had been previously extracted.</span><span class="sxs-lookup"><span data-stu-id="3c186-109">The tool can also re-create a solution file by packing the files that had been previously extracted.</span></span> <span data-ttu-id="3c186-110">This enables multiple people to work independently on a single solution and extract their changes into a common location.</span><span class="sxs-lookup"><span data-stu-id="3c186-110">This enables multiple people to work independently on a single solution and extract their changes into a common location.</span></span> <span data-ttu-id="3c186-111">Because each component in the solution file is broken into multiple files, it becomes possible to merge customizations without overwriting prior changes.</span><span class="sxs-lookup"><span data-stu-id="3c186-111">Because each component in the solution file is broken into multiple files, it becomes possible to merge customizations without overwriting prior changes.</span></span> <span data-ttu-id="3c186-112">A secondary use of the SolutionPackager tool is that it can be invoked from an automated build process to generate a compressed solution file from previously extracted component files without needing an active [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server.</span><span class="sxs-lookup"><span data-stu-id="3c186-112">A secondary use of the SolutionPackager tool is that it can be invoked from an automated build process to generate a compressed solution file from previously extracted component files without needing an active [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server.</span></span>

 <span data-ttu-id="3c186-113">The SolutionPackager tool is distributed as part of the [Microsoft.CrmSdk.CoreTools](https://www.nuget.org/packages/Microsoft.CrmSdk.CoreTools) NuGet package.</span><span class="sxs-lookup"><span data-stu-id="3c186-113">The SolutionPackager tool is distributed as part of the [Microsoft.CrmSdk.CoreTools](https://www.nuget.org/packages/Microsoft.CrmSdk.CoreTools) NuGet package.</span></span> <span data-ttu-id="3c186-114">See [Download tools from NuGet](download-tools-nuget.md) for information about how to download it.</span><span class="sxs-lookup"><span data-stu-id="3c186-114">See [Download tools from NuGet](download-tools-nuget.md) for information about how to download it.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="3c186-115">In This Section</span><span class="sxs-lookup"><span data-stu-id="3c186-115">In This Section</span></span>  
 [<span data-ttu-id="3c186-116">Use the SolutionPackager Tool to Compress and Extract a Solution File</span><span class="sxs-lookup"><span data-stu-id="3c186-116">Use the SolutionPackager Tool to Compress and Extract a Solution File</span></span>](compress-extract-solution-file-solutionpackager.md)  
  
 [<span data-ttu-id="3c186-117">Use Source Control with Solution Files</span><span class="sxs-lookup"><span data-stu-id="3c186-117">Use Source Control with Solution Files</span></span>](use-source-control-solution-files.md)  
  
 [<span data-ttu-id="3c186-118">Solution Component File Reference (SolutionPackager)</span><span class="sxs-lookup"><span data-stu-id="3c186-118">Solution Component File Reference (SolutionPackager)</span></span>](solution-component-file-reference-solutionpackager.md)  
  
## <a name="related-sections"></a><span data-ttu-id="3c186-119">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="3c186-119">Related Sections</span></span>  
 [<span data-ttu-id="3c186-120">Developer Tools</span><span class="sxs-lookup"><span data-stu-id="3c186-120">Developer Tools</span></span>](developer-tools.md)  
  
 [<span data-ttu-id="3c186-121">Package and Distribute Extensions with Dynamics 365 for Customer Engagement Solutions</span><span class="sxs-lookup"><span data-stu-id="3c186-121">Package and Distribute Extensions with Dynamics 365 for Customer Engagement Solutions</span></span>](package-distribute-extensions-use-solutions.md)
