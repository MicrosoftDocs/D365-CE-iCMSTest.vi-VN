---
title: Visual Studio and the .NET Framework (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: Learn about managed code development tools and requirements.
keywords: ''
ms.date: 09/13/2018
ms.service: crm-online
ms.custom: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement (on-premises)
- Dynamics CRM 2016
- Dynamics CRM Online
ms.assetid: b2d572f9-6114-4694-a2d1-127cff861a96
author: JimDaly
ms.author: kvivek
manager: kvivek
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 20
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b78dd2f89f9613dacc7101f7c376623e1ce07d58
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387180"
---
# <a name="visual-studio-and-the-net-framework"></a><span data-ttu-id="0cbc3-103">Visual Studio and the .NET Framework</span><span class="sxs-lookup"><span data-stu-id="0cbc3-103">Visual Studio and the .NET Framework</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="0cbc3-104">The .NET SDK assemblies for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] are built on [!INCLUDE[pn_NET_Framework_452_short](../includes/pn-net-framework-452-short.md)].</span><span class="sxs-lookup"><span data-stu-id="0cbc3-104">The .NET SDK assemblies for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] are built on [!INCLUDE[pn_NET_Framework_452_short](../includes/pn-net-framework-452-short.md)].</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="0cbc3-105">Do not use .NET Framework versions greater than 4.5.2 when developing plug-ins.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-105">Do not use .NET Framework versions greater than 4.5.2 when developing plug-ins.</span></span>

<span data-ttu-id="0cbc3-106">You can use [!INCLUDE[pn-visual-studio-short](../includes/pn-visual-studio-short.md)] to build your managed code applications using [!INCLUDE[pn_NET_Framework_452_short](../includes/pn-net-framework-452-short.md)] or later.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-106">You can use [!INCLUDE[pn-visual-studio-short](../includes/pn-visual-studio-short.md)] to build your managed code applications using [!INCLUDE[pn_NET_Framework_452_short](../includes/pn-net-framework-452-short.md)] or later.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="0cbc3-107">You should build any custom client applications using [!INCLUDE [pn-net-framework-462-long](../includes/pn-net-framework-462-long.md)] or later.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-107">You should build any custom client applications using [!INCLUDE [pn-net-framework-462-long](../includes/pn-net-framework-462-long.md)] or later.</span></span>
> <span data-ttu-id="0cbc3-108">Starting with the [!INCLUDE [pn-crm-9-0-0-online](../includes/pn-crm-9-0-0-online.md)], only applications using Transport Level Security (TLS) 1.2 or better security will be allowed to connect.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-108">Starting with the [!INCLUDE [pn-crm-9-0-0-online](../includes/pn-crm-9-0-0-online.md)], only applications using Transport Level Security (TLS) 1.2 or better security will be allowed to connect.</span></span> <span data-ttu-id="0cbc3-109">TLS 1.2 is not the default protocol used by [!INCLUDE [pn-net-framework-452-short](../includes/pn-net-framework-452-short.md)], but it is in  [!INCLUDE [pn-net-framework-462-short](../includes/pn-net-framework-462-short.md)].</span><span class="sxs-lookup"><span data-stu-id="0cbc3-109">TLS 1.2 is not the default protocol used by [!INCLUDE [pn-net-framework-452-short](../includes/pn-net-framework-452-short.md)], but it is in  [!INCLUDE [pn-net-framework-462-short](../includes/pn-net-framework-462-short.md)].</span></span>
> 
> <span data-ttu-id="0cbc3-110">Enforcement of this higher standard for security will only be applied to [!INCLUDE [pn-crm-9-0-0-online](../includes/pn-crm-9-0-0-online.md)] at this time.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-110">Enforcement of this higher standard for security will only be applied to [!INCLUDE [pn-crm-9-0-0-online](../includes/pn-crm-9-0-0-online.md)] at this time.</span></span> <span data-ttu-id="0cbc3-111">If your clients are designed to connect to any version or deployment type you can prepare by re-compling the application to use [!INCLUDE [pn-net-framework-462-short](../includes/pn-net-framework-462-short.md)].</span><span class="sxs-lookup"><span data-stu-id="0cbc3-111">If your clients are designed to connect to any version or deployment type you can prepare by re-compling the application to use [!INCLUDE [pn-net-framework-462-short](../includes/pn-net-framework-462-short.md)].</span></span>
> <span data-ttu-id="0cbc3-112">More information: [Blog Post: Updates coming to Dynamics 365 for Customer Engagement apps connection security](https://blogs.msdn.microsoft.com/crm/2017/09/28/updates-coming-to-dynamics-365-customer-engagement-connection-security/)</span><span class="sxs-lookup"><span data-stu-id="0cbc3-112">More information: [Blog Post: Updates coming to Dynamics 365 for Customer Engagement apps connection security](https://blogs.msdn.microsoft.com/crm/2017/09/28/updates-coming-to-dynamics-365-customer-engagement-connection-security/)</span></span>
> 
> [!TIP]
> <span data-ttu-id="0cbc3-113">When installing [!INCLUDE[pn-net-framework-462-short.md](../includes/pn-net-framework-462-short.md)] on your development computer, be sure to install the developer pack and not just the run-time.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-113">When installing [!INCLUDE[pn-net-framework-462-short.md](../includes/pn-net-framework-462-short.md)] on your development computer, be sure to install the developer pack and not just the run-time.</span></span> <span data-ttu-id="0cbc3-114">This will enable the 4.6.2 framework to be chosen in the **New Project** dialog box of [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] and in the target framework drop-down menu of the project’s properties.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-114">This will enable the 4.6.2 framework to be chosen in the **New Project** dialog box of [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] and in the target framework drop-down menu of the project’s properties.</span></span>  

<span data-ttu-id="0cbc3-115">You can use a [!INCLUDE[pn_MS_VS_Community](../includes/pn-vs-community.md)] edition for development.</span><span class="sxs-lookup"><span data-stu-id="0cbc3-115">You can use a [!INCLUDE[pn_MS_VS_Community](../includes/pn-vs-community.md)] edition for development.</span></span> 

[!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0cbc3-116">[Support for .NET Framework versions](../developer/supported-extensions.md#SupportNET)</span><span class="sxs-lookup"><span data-stu-id="0cbc3-116">[Support for .NET Framework versions](../developer/supported-extensions.md#SupportNET)</span></span>


<span data-ttu-id="0cbc3-117">For a complete statement of supported and unsupported development, see [Supported Extensions for Dynamics 365 for Customer Engagement apps](../developer/supported-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="0cbc3-117">For a complete statement of supported and unsupported development, see [Supported Extensions for Dynamics 365 for Customer Engagement apps](../developer/supported-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0cbc3-118">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="0cbc3-118">See Also</span></span>

 [<span data-ttu-id="0cbc3-119">Developer Tools</span><span class="sxs-lookup"><span data-stu-id="0cbc3-119">Developer Tools</span></span>](../developer/developer-tools.md)
