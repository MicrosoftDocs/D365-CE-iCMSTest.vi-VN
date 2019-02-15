---
title: Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#) (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Dynamics 365 for Customer Engagement Web API Helper Library assists in performing common tasks, such as application configuration, authentication against a Dynamics 365 for Customer Engagement service, and HTTP response error handling
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: ba9d94fe-d189-4873-aef5-0010f3ccecba
caps.latest.revision: 7
author: JimDaly
ms.author: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 255ff322da94def110c263dce43daaa00662495d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385983"
---
# <a name="use-the-dynamics-365-for-customer-engagement-web-api-helper-library-c"></a><span data-ttu-id="206e2-103">Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)</span><span class="sxs-lookup"><span data-stu-id="206e2-103">Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="206e2-104">Most of the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps Web API C#  code samples described in this SDK use the  *Dynamics 365 for Customer Engagement Web API Helper Library* to assist in performing common tasks, such as application configuration, authentication against a [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps service, and HTTP response error handling.</span><span class="sxs-lookup"><span data-stu-id="206e2-104">Most of the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps Web API C#  code samples described in this SDK use the  *Dynamics 365 for Customer Engagement Web API Helper Library* to assist in performing common tasks, such as application configuration, authentication against a [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps service, and HTTP response error handling.</span></span> <span data-ttu-id="206e2-105">You might also find this helper code useful in your [!INCLUDE[pn_NET_Framework](../../includes/pn-net-framework.md)]-based projects.</span><span class="sxs-lookup"><span data-stu-id="206e2-105">You might also find this helper code useful in your [!INCLUDE[pn_NET_Framework](../../includes/pn-net-framework.md)]-based projects.</span></span>  
  
## <a name="obtain-and-use-the-helper-library"></a><span data-ttu-id="206e2-106">Obtain and use the helper library</span><span class="sxs-lookup"><span data-stu-id="206e2-106">Obtain and use the helper library</span></span>  
 <span data-ttu-id="206e2-107">The Dynamics 365 for Customer Engagement Web API Helper Library is distributed as the NuGet package [Microsoft.CrmSdk.WebApi.Samples.HelperCode](https://www.nuget.org/packages/Microsoft.CrmSdk.WebApi.Samples.HelperCode).</span><span class="sxs-lookup"><span data-stu-id="206e2-107">The Dynamics 365 for Customer Engagement Web API Helper Library is distributed as the NuGet package [Microsoft.CrmSdk.WebApi.Samples.HelperCode](https://www.nuget.org/packages/Microsoft.CrmSdk.WebApi.Samples.HelperCode).</span></span> <span data-ttu-id="206e2-108">If you are unfamiliar with downloading and installing NuGet packages in Visual Studio projects, see the section [Add all required resources to your project](start-web-api-project-visual-studio-csharp.md#bkmk_addAllRequiredResources).</span><span class="sxs-lookup"><span data-stu-id="206e2-108">If you are unfamiliar with downloading and installing NuGet packages in Visual Studio projects, see the section [Add all required resources to your project](start-web-api-project-visual-studio-csharp.md#bkmk_addAllRequiredResources).</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="206e2-109">This Nuget package  is the authoritative source for the helper library.</span><span class="sxs-lookup"><span data-stu-id="206e2-109">This Nuget package  is the authoritative source for the helper library.</span></span>  <span data-ttu-id="206e2-110">For your convenience, the topics in this section contain a code listing for each class in the helper library.</span><span class="sxs-lookup"><span data-stu-id="206e2-110">For your convenience, the topics in this section contain a code listing for each class in the helper library.</span></span> <span data-ttu-id="206e2-111">However, these listings are not guaranteed to be complete or current, so they should not be used in projects.</span><span class="sxs-lookup"><span data-stu-id="206e2-111">However, these listings are not guaranteed to be complete or current, so they should not be used in projects.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="206e2-112">In this section</span><span class="sxs-lookup"><span data-stu-id="206e2-112">In this section</span></span>  
 [<span data-ttu-id="206e2-113">Helper code: Configuration classes</span><span class="sxs-lookup"><span data-stu-id="206e2-113">Helper code: Configuration classes</span></span>](web-api-helper-code-configuration-classes.md)  
  
 [<span data-ttu-id="206e2-114">Helper code: Authentication class</span><span class="sxs-lookup"><span data-stu-id="206e2-114">Helper code: Authentication class</span></span>](web-api-helper-code-authentication-class.md)  
  
 [<span data-ttu-id="206e2-115">Helper code: CrmHttpResponseException class</span><span class="sxs-lookup"><span data-stu-id="206e2-115">Helper code: CrmHttpResponseException class</span></span>](web-api-helper-code-crmhttpresponseexception-class.md)  
  
### <a name="see-also"></a><span data-ttu-id="206e2-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="206e2-116">See also</span></span>  
 <span data-ttu-id="206e2-117">[Get Started with the Web API (C#)](get-started-dynamics-365-web-api-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="206e2-117">[Get Started with the Web API (C#)](get-started-dynamics-365-web-api-csharp.md) </span></span>  
 <span data-ttu-id="206e2-118">[Start a Web API project in Visual Studio (C#)](start-web-api-project-visual-studio-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="206e2-118">[Start a Web API project in Visual Studio (C#)](start-web-api-project-visual-studio-csharp.md) </span></span>  
 [<span data-ttu-id="206e2-119">Perform operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="206e2-119">Perform operations using the Web API</span></span>](perform-operations-web-api.md)
