---
title: Start a managed code project in Visual Studio (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: This topic shows you how to create a new project in Visual Studio that’s properly configured to build a console application that uses the Dynamics 365 for Customer Engagement web services (SDK).
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 7fefaeb8-5d8a-4b88-9032-a31e78970175
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2e24e5c59bd8ae56a5bd509416a568b01cfdb7a2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386888"
---
# <a name="start-a-managed-code-project-in-visual-studio"></a><span data-ttu-id="28954-103">Start a managed code project in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="28954-103">Start a managed code project in Visual Studio</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="28954-104">This topic shows you how to create a new project in [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] that’s properly configured to build a console application that uses the Organization Service with .NET SDK assemblies.</span><span class="sxs-lookup"><span data-stu-id="28954-104">This topic shows you how to create a new project in [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] that’s properly configured to build a console application that uses the Organization Service with .NET SDK assemblies.</span></span> <span data-ttu-id="28954-105">Learn what required references must be added to your project when building an application that links to the .NET SDK assemblies.</span><span class="sxs-lookup"><span data-stu-id="28954-105">Learn what required references must be added to your project when building an application that links to the .NET SDK assemblies.</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="28954-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="28954-106">Prerequisites</span></span>  
  
- [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] <span data-ttu-id="28954-107">installed on your development computer.</span><span class="sxs-lookup"><span data-stu-id="28954-107">installed on your development computer.</span></span>  
  
     <span data-ttu-id="28954-108">Any edition, including [!INCLUDE[pn_VS_Express](../../includes/pn-vs-express.md)], should work.</span><span class="sxs-lookup"><span data-stu-id="28954-108">Any edition, including [!INCLUDE[pn_VS_Express](../../includes/pn-vs-express.md)], should work.</span></span> <span data-ttu-id="28954-109">For more information about what versions of [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] are supported, see [Visual Studio and the .NET Framework](../visual-studio-dot-net-framework.md).</span><span class="sxs-lookup"><span data-stu-id="28954-109">For more information about what versions of [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] are supported, see [Visual Studio and the .NET Framework](../visual-studio-dot-net-framework.md).</span></span>
  
- <span data-ttu-id="28954-110">Access to a [!INCLUDE [pn-dynamics-365](../../includes/pn-dynamics-365.md)] on-line or on-premises organzation.</span><span class="sxs-lookup"><span data-stu-id="28954-110">Access to a [!INCLUDE [pn-dynamics-365](../../includes/pn-dynamics-365.md)] on-line or on-premises organzation.</span></span>
  
## <a name="create-a-project"></a><span data-ttu-id="28954-111">Create a project</span><span class="sxs-lookup"><span data-stu-id="28954-111">Create a project</span></span>  
 <span data-ttu-id="28954-112">The following procedure demonstrates how to create a console application project in the C# or VB language that uses [!INCLUDE [pn-net-framework-462-long](../../includes/pn-net-framework-462-long.md)].</span><span class="sxs-lookup"><span data-stu-id="28954-112">The following procedure demonstrates how to create a console application project in the C# or VB language that uses [!INCLUDE [pn-net-framework-462-long](../../includes/pn-net-framework-462-long.md)].</span></span> <span data-ttu-id="28954-113">For more information on supported versions of the [!INCLUDE[pn_NET_Framework](../../includes/pn-net-framework.md)], see [Supported extensions](../supported-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="28954-113">For more information on supported versions of the [!INCLUDE[pn_NET_Framework](../../includes/pn-net-framework.md)], see [Supported extensions](../supported-extensions.md).</span></span>  


  
#### <a name="new-project"></a><span data-ttu-id="28954-114">New project</span><span class="sxs-lookup"><span data-stu-id="28954-114">New project</span></span>  
  
1. <span data-ttu-id="28954-115">In [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)], select **New Project**.</span><span class="sxs-lookup"><span data-stu-id="28954-115">In [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)], select **New Project**.</span></span>  
  
2. <span data-ttu-id="28954-116">In the left navigation pane under **Templates**, select **Visual C#** or **Visual Basic**.</span><span class="sxs-lookup"><span data-stu-id="28954-116">In the left navigation pane under **Templates**, select **Visual C#** or **Visual Basic**.</span></span>  
  
3. <span data-ttu-id="28954-117">Above the list of available templates, select [!INCLUDE [pn-net-framework-462-short](../../includes/pn-net-framework-462-short.md)].</span><span class="sxs-lookup"><span data-stu-id="28954-117">Above the list of available templates, select [!INCLUDE [pn-net-framework-462-short](../../includes/pn-net-framework-462-short.md)].</span></span>  
  
4. <span data-ttu-id="28954-118">In the list of templates, select **Console Application**.</span><span class="sxs-lookup"><span data-stu-id="28954-118">In the list of templates, select **Console Application**.</span></span>  
  
   <span data-ttu-id="28954-119">![A new console app project dialog in Dynamics 365 for Customer Engagement](../media/new-project.PNG "A new console app project dialog in Dynamics 365 for Customer Engagement")</span><span class="sxs-lookup"><span data-stu-id="28954-119">![A new console app project dialog in Dynamics 365 for Customer Engagement](../media/new-project.PNG "A new console app project dialog in Dynamics 365 for Customer Engagement")</span></span>  
  
5. <span data-ttu-id="28954-120">In the fields near the bottom of the form give the project a name and location, and then select **OK**.</span><span class="sxs-lookup"><span data-stu-id="28954-120">In the fields near the bottom of the form give the project a name and location, and then select **OK**.</span></span>  
  
6. <span data-ttu-id="28954-121">Under the **Project** menu, open the project’s properties form and verify the target framework is set to [!INCLUDE [pn-net-framework-462-short](../../includes/pn-net-framework-462-short.md)].</span><span class="sxs-lookup"><span data-stu-id="28954-121">Under the **Project** menu, open the project’s properties form and verify the target framework is set to [!INCLUDE [pn-net-framework-462-short](../../includes/pn-net-framework-462-short.md)].</span></span>
  
   <span data-ttu-id="28954-122">![Choose the target framework for the Dynamics 365 for Customer Engagement project](../media/new-project-framework.PNG "Choose the target framework for the Dynamics 365 for Customer Engagement project")</span><span class="sxs-lookup"><span data-stu-id="28954-122">![Choose the target framework for the Dynamics 365 for Customer Engagement project](../media/new-project-framework.PNG "Choose the target framework for the Dynamics 365 for Customer Engagement project")</span></span>  
  
## <a name="add-nuget-packages"></a><span data-ttu-id="28954-123">Add NuGet package(s)</span><span class="sxs-lookup"><span data-stu-id="28954-123">Add NuGet package(s)</span></span> 
 <span data-ttu-id="28954-124">The minimum set of assemblies you need are in the [Microsoft.CrmSdk.CoreAssemblies](http://www.nuget.org/packages/Microsoft.CrmSdk.CoreAssemblies/) NuGet package.</span><span class="sxs-lookup"><span data-stu-id="28954-124">The minimum set of assemblies you need are in the [Microsoft.CrmSdk.CoreAssemblies](http://www.nuget.org/packages/Microsoft.CrmSdk.CoreAssemblies/) NuGet package.</span></span> <span data-ttu-id="28954-125">Installing this package will add the required references to your project.</span><span class="sxs-lookup"><span data-stu-id="28954-125">Installing this package will add the required references to your project.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="28954-126">[Subscribe to SDK assembly updates using NuGet](subscribe-sdk-assembly-updates-using-nuget.md)</span><span class="sxs-lookup"><span data-stu-id="28954-126">[Subscribe to SDK assembly updates using NuGet](subscribe-sdk-assembly-updates-using-nuget.md)</span></span>
  
### <a name="see-also"></a><span data-ttu-id="28954-127">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="28954-127">See also</span></span>  
 [<span data-ttu-id="28954-128">Getting started with managed code application development</span><span class="sxs-lookup"><span data-stu-id="28954-128">Getting started with managed code application development</span></span>](get-started-managed-code-application-development.md)
