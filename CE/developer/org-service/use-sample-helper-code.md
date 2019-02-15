---
title: Use the Organization Service sample and helper code (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Some tasks that are common to all Dynamics 365 for Customer Engagement samples such as connecting to Dynamics 365 for Customer Engagement web services, registering a computing device with Microsoft account and creating additional users in Active Directory and Dynamics 365 for Customer Engagement (online) Customer Engagement are done using the sample helper code available in Developers Guide for Dynamics 365 for Customer Engagement (SDK).
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 3afa448b-aa1d-42bb-a725-23b7f5eeb411
caps.latest.revision: 36
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d3d0171ef283bebceefca80cf88481daf105a9aa
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386275"
---
# <a name="use-the-organization-service-sample-and-helper-code"></a><span data-ttu-id="29286-103">Use the Organization Service sample and helper code</span><span class="sxs-lookup"><span data-stu-id="29286-103">Use the Organization Service sample and helper code</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="29286-104">Most managed code samples provided in the [!INCLUDE [pn-sdk](../../includes/pn-sdk.md)] that use the organization and discovery web services are using shared helper code to perform common tasks.</span><span class="sxs-lookup"><span data-stu-id="29286-104">Most managed code samples provided in the [!INCLUDE [pn-sdk](../../includes/pn-sdk.md)] that use the organization and discovery web services are using shared helper code to perform common tasks.</span></span> <span data-ttu-id="29286-105">You might find this helper code useful in applications that you write.</span><span class="sxs-lookup"><span data-stu-id="29286-105">You might find this helper code useful in applications that you write.</span></span> <span data-ttu-id="29286-106">This sample code is available as a NuGet package: [Microsoft.CrmSdk.Samples.HelperCode-CS](https://www.nuget.org/packages/Microsoft.CrmSdk.Samples.HelperCode-CS)</span><span class="sxs-lookup"><span data-stu-id="29286-106">This sample code is available as a NuGet package: [Microsoft.CrmSdk.Samples.HelperCode-CS](https://www.nuget.org/packages/Microsoft.CrmSdk.Samples.HelperCode-CS)</span></span>
  
 <span data-ttu-id="29286-107">When writing an application that uses the .NET SDK assemblies, you typically have to perform a number of steps to configure your application’s project.</span><span class="sxs-lookup"><span data-stu-id="29286-107">When writing an application that uses the .NET SDK assemblies, you typically have to perform a number of steps to configure your application’s project.</span></span> <span data-ttu-id="29286-108">To learn more about setting up a project in [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)], or other development environment, see [Start a managed code project in Visual Studio](start-managed-code-project-visual-studio.md).</span><span class="sxs-lookup"><span data-stu-id="29286-108">To learn more about setting up a project in [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)], or other development environment, see [Start a managed code project in Visual Studio](start-managed-code-project-visual-studio.md).</span></span>  
  
<span data-ttu-id="29286-109">To view a sample application that uses the helper code and includes the required .NET references, see [Run a simple program using Customer Engagement web services](../simple-program-web-services.md).</span><span class="sxs-lookup"><span data-stu-id="29286-109">To view a sample application that uses the helper code and includes the required .NET references, see [Run a simple program using Customer Engagement web services](../simple-program-web-services.md).</span></span>  
  
 <span data-ttu-id="29286-110">A non-customized early-bound types file that is named `MyOrganizationCrmSdkTypes` is included in the `Microsoft.CrmSdk.Samples.HelperCode-CS` NuGet package to help get you started.</span><span class="sxs-lookup"><span data-stu-id="29286-110">A non-customized early-bound types file that is named `MyOrganizationCrmSdkTypes` is included in the `Microsoft.CrmSdk.Samples.HelperCode-CS` NuGet package to help get you started.</span></span> <span data-ttu-id="29286-111">However, if your organization has custom or customized entities, you should generate a new early-bound types file.</span><span class="sxs-lookup"><span data-stu-id="29286-111">However, if your organization has custom or customized entities, you should generate a new early-bound types file.</span></span> <span data-ttu-id="29286-112">For the purposes of this documentation, the generated classes are included in the global namespace.</span><span class="sxs-lookup"><span data-stu-id="29286-112">For the purposes of this documentation, the generated classes are included in the global namespace.</span></span> <span data-ttu-id="29286-113">For more information, see [Create Early Bound Entity Classes with the Code Generation Tool (CrmSvcUtil.exe)](create-early-bound-entity-classes-code-generation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="29286-113">For more information, see [Create Early Bound Entity Classes with the Code Generation Tool (CrmSvcUtil.exe)](create-early-bound-entity-classes-code-generation-tool.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="29286-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="29286-114">See also</span></span>  
 <span data-ttu-id="29286-115">[Extend Dynamics 365 for Customer Engagement apps on the server](../extend-dynamics-365-server.md) </span><span class="sxs-lookup"><span data-stu-id="29286-115">[Extend Dynamics 365 for Customer Engagement apps on the server](../extend-dynamics-365-server.md) </span></span>  
 <span data-ttu-id="29286-116">[Best practices for developing with Dynamics 365 for Customer Engagement apps](../best-practices-sdk.md) </span><span class="sxs-lookup"><span data-stu-id="29286-116">[Best practices for developing with Dynamics 365 for Customer Engagement apps](../best-practices-sdk.md) </span></span>  
 [<span data-ttu-id="29286-117">Helper Code: ServerConnection Class</span><span class="sxs-lookup"><span data-stu-id="29286-117">Helper Code: ServerConnection Class</span></span>](helper-code-serverconnection-class.md)  
 <span data-ttu-id="29286-118">[Helper Code: SystemUserProvider class](helper-code-systemuserprovider-class.md) </span><span class="sxs-lookup"><span data-stu-id="29286-118">[Helper Code: SystemUserProvider class](helper-code-systemuserprovider-class.md) </span></span>  
 <span data-ttu-id="29286-119">[Helper Code: Enumerations for Option Sets](helper-code-enumerations-option-sets.md) </span><span class="sxs-lookup"><span data-stu-id="29286-119">[Helper Code: Enumerations for Option Sets](helper-code-enumerations-option-sets.md) </span></span>  
 <span data-ttu-id="29286-120">[Sample code directory for Dynamics 365 for Customer Engagement apps](../sample-code-directory.md) </span><span class="sxs-lookup"><span data-stu-id="29286-120">[Sample code directory for Dynamics 365 for Customer Engagement apps](../sample-code-directory.md) </span></span>  
 <span data-ttu-id="29286-121">[Assemblies Included in the Dynamics 365 for Customer Engagement apps SDK apps](assemblies-included-sdk.md) </span><span class="sxs-lookup"><span data-stu-id="29286-121">[Assemblies Included in the Dynamics 365 for Customer Engagement apps SDK apps](assemblies-included-sdk.md) </span></span>  
 [<span data-ttu-id="29286-122">Use Dynamics 365 for Customer Engagement apps Services in Code</span><span class="sxs-lookup"><span data-stu-id="29286-122">Use Dynamics 365 for Customer Engagement apps Services in Code</span></span>](use-services-in-code.md)
