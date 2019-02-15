---
title: 'Sample: Web resource utility (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: 'The sample demonstrates creating and updating Web Resources. The Web Resource Utility code demonstrates several applications of the Dynamics 365 for Customer Engagement (online) APIs: Managing connectionsa and Retrieving data about solutions. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- web resource
- web resource, import
ms.assetid: 27b065e3-1157-4a93-b1e6-b46f25afb595
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9e1f318aac3add979c9ba22b60070179f9608500
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388823"
---
# <a name="sample-web-resource-utility"></a><span data-ttu-id="a7579-104">Sample: Web resource utility</span><span class="sxs-lookup"><span data-stu-id="a7579-104">Sample: Web resource utility</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a7579-105">Manually creating Web resources one at a time using the customization tools can take a long time when you have to create many files.</span><span class="sxs-lookup"><span data-stu-id="a7579-105">Manually creating Web resources one at a time using the customization tools can take a long time when you have to create many files.</span></span> <span data-ttu-id="a7579-106">The Web Resource Utility is a WPF application project that you can compile and run to import many Web Resource eligible files from a folder structure with a consistent naming convention based on the folder structure.</span><span class="sxs-lookup"><span data-stu-id="a7579-106">The Web Resource Utility is a WPF application project that you can compile and run to import many Web Resource eligible files from a folder structure with a consistent naming convention based on the folder structure.</span></span>  
  
 <span data-ttu-id="a7579-107">Download the complete sample from here [Web Resource Utility sample](https://code.msdn.microsoft.com/Web-Resource-Utility-sample-eb3771e9).</span><span class="sxs-lookup"><span data-stu-id="a7579-107">Download the complete sample from here [Web Resource Utility sample](https://code.msdn.microsoft.com/Web-Resource-Utility-sample-eb3771e9).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="a7579-108">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="a7579-108">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="a7579-109">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="a7579-109">Requirements</span></span>  
 <span data-ttu-id="a7579-110">For more information, see the Readme.docx file.</span><span class="sxs-lookup"><span data-stu-id="a7579-110">For more information, see the Readme.docx file.</span></span>  
  
 <span data-ttu-id="a7579-111">The solution must be built in [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] before running.</span><span class="sxs-lookup"><span data-stu-id="a7579-111">The solution must be built in [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] before running.</span></span> <span data-ttu-id="a7579-112">Double-click the **WebResourceUtility.sln** to open the source code in [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)].</span><span class="sxs-lookup"><span data-stu-id="a7579-112">Double-click the **WebResourceUtility.sln** to open the source code in [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)].</span></span> <span data-ttu-id="a7579-113">Open and view the Solution Explorer.</span><span class="sxs-lookup"><span data-stu-id="a7579-113">Open and view the Solution Explorer.</span></span>  
  
 <span data-ttu-id="a7579-114">This solution uses linked files and requires access to the following files in order to compile:</span><span class="sxs-lookup"><span data-stu-id="a7579-114">This solution uses linked files and requires access to the following files in order to compile:</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="a7579-115">You may need to manually update the links for the files before trying to build the solution or you may experience compilation errors.</span><span class="sxs-lookup"><span data-stu-id="a7579-115">You may need to manually update the links for the files before trying to build the solution or you may experience compilation errors.</span></span>
  
## <a name="demonstrates"></a><span data-ttu-id="a7579-116">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="a7579-116">Demonstrates</span></span>  
 <span data-ttu-id="a7579-117">In addition to creating and updating Web Resources, the Web Resource Utility code demonstrates several applications of the [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] APIs:</span><span class="sxs-lookup"><span data-stu-id="a7579-117">In addition to creating and updating Web Resources, the Web Resource Utility code demonstrates several applications of the [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] APIs:</span></span>  
  
 <span data-ttu-id="a7579-118">**Managing connections**</span><span class="sxs-lookup"><span data-stu-id="a7579-118">**Managing connections**</span></span>  
 <span data-ttu-id="a7579-119">The Web Resource Utility preserves connections to multiple [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] servers so the user doesn’t need to enter connection information each time.</span><span class="sxs-lookup"><span data-stu-id="a7579-119">The Web Resource Utility preserves connections to multiple [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] servers so the user doesn’t need to enter connection information each time.</span></span>  
  
 <span data-ttu-id="a7579-120">**Retrieving data about solutions**</span><span class="sxs-lookup"><span data-stu-id="a7579-120">**Retrieving data about solutions**</span></span>  
 <span data-ttu-id="a7579-121">The Web Resource Utility retrieves data about available unmanaged solutions and creates Web Resources using the customization prefix defined by the publisher of the solution.</span><span class="sxs-lookup"><span data-stu-id="a7579-121">The Web Resource Utility retrieves data about available unmanaged solutions and creates Web Resources using the customization prefix defined by the publisher of the solution.</span></span>  
  
## <a name="web-resource-utility"></a><span data-ttu-id="a7579-122">Web Resource Utility</span><span class="sxs-lookup"><span data-stu-id="a7579-122">Web Resource Utility</span></span>  
 <span data-ttu-id="a7579-123">The following screenshot shows the Web Resource Utility user interface:</span><span class="sxs-lookup"><span data-stu-id="a7579-123">The following screenshot shows the Web Resource Utility user interface:</span></span>  
  
 <span data-ttu-id="a7579-124">![The Web Resource Utility user interface](media/web-resource-utility.png "The Web Resource Utility user interface")</span><span class="sxs-lookup"><span data-stu-id="a7579-124">![The Web Resource Utility user interface](media/web-resource-utility.png "The Web Resource Utility user interface")</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="a7579-125">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a7579-125">See also</span></span>  
 <span data-ttu-id="a7579-126">[Sample: Importing Files as Web Resources](sample-import-files-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="a7579-126">[Sample: Importing Files as Web Resources](sample-import-files-web-resources.md) </span></span>  
 <span data-ttu-id="a7579-127">[Web Resource Messages and Methods](webresource-entity-messages-methods.md) </span><span class="sxs-lookup"><span data-stu-id="a7579-127">[Web Resource Messages and Methods](webresource-entity-messages-methods.md) </span></span>  
 <span data-ttu-id="a7579-128">[Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="a7579-128">[Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md) </span></span>  
 [<span data-ttu-id="a7579-129">Streamline web resource development using Fiddler AutoResponder</span><span class="sxs-lookup"><span data-stu-id="a7579-129">Streamline web resource development using Fiddler AutoResponder</span></span>](streamline-javascript-development-fiddler-autoresponder.md)
