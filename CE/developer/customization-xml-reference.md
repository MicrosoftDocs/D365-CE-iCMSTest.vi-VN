---
title: Customization XML reference | MicrosoftDocs
description: 'The customizations.xml file is one of the files included in an exported unmanaged solution. The file contains all or selected portions of the customizations and configurations for your system. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: bcdcc975-4918-4513-b04a-6a9d3d04f08c
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 165b9884e72aa6a0af71a36423501f1c4f9d359a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385587"
---
# <a name="customization-xml-reference"></a><span data-ttu-id="9f488-104">Customization XML reference</span><span class="sxs-lookup"><span data-stu-id="9f488-104">Customization XML reference</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="9f488-105">The customizations.xml file is one of the files included in an exported unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="9f488-105">The customizations.xml file is one of the files included in an exported unmanaged solution.</span></span> <span data-ttu-id="9f488-106">The file contains all or selected portions of the customizations and configurations for your system.</span><span class="sxs-lookup"><span data-stu-id="9f488-106">The file contains all or selected portions of the customizations and configurations for your system.</span></span> 
  
 <span data-ttu-id="9f488-107">The solutions file is exported as a compressed .zip file.</span><span class="sxs-lookup"><span data-stu-id="9f488-107">The solutions file is exported as a compressed .zip file.</span></span> <span data-ttu-id="9f488-108">The contents of the unmanaged solutions file must be extracted before the customizations file can be edited.</span><span class="sxs-lookup"><span data-stu-id="9f488-108">The contents of the unmanaged solutions file must be extracted before the customizations file can be edited.</span></span> <span data-ttu-id="9f488-109">All the files of the unmanaged solution must be added to a compressed .zip file before it can be re-imported.</span><span class="sxs-lookup"><span data-stu-id="9f488-109">All the files of the unmanaged solution must be added to a compressed .zip file before it can be re-imported.</span></span>  

> [!NOTE]
> - <span data-ttu-id="9f488-110">Editing a managed solution file is not supported.</span><span class="sxs-lookup"><span data-stu-id="9f488-110">Editing a managed solution file is not supported.</span></span>  
> - <span data-ttu-id="9f488-111">Not all elements of the customizations.xml file can be edited.</span><span class="sxs-lookup"><span data-stu-id="9f488-111">Not all elements of the customizations.xml file can be edited.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="9f488-112">[Support for Editing the Customization File](customize-dev/when-edit-customization-file.md)</span><span class="sxs-lookup"><span data-stu-id="9f488-112">[Support for Editing the Customization File](customize-dev/when-edit-customization-file.md)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9f488-113">In This Section</span><span class="sxs-lookup"><span data-stu-id="9f488-113">In This Section</span></span>

 [<span data-ttu-id="9f488-114">Ribbon core schema</span><span class="sxs-lookup"><span data-stu-id="9f488-114">Ribbon core schema</span></span>](customize-dev/ribbon-core-schema.md)  
 [<span data-ttu-id="9f488-115">Ribbon types schema</span><span class="sxs-lookup"><span data-stu-id="9f488-115">Ribbon types schema</span></span>](customize-dev/ribbon-types-schema.md)  
 [<span data-ttu-id="9f488-116">Ribbon WSS schema</span><span class="sxs-lookup"><span data-stu-id="9f488-116">Ribbon WSS schema</span></span>](customize-dev/ribbon-wss-schema.md)  
 [<span data-ttu-id="9f488-117">SiteMap schema</span><span class="sxs-lookup"><span data-stu-id="9f488-117">SiteMap schema</span></span>](customize-dev/sitemap-schema.md)  
 [<span data-ttu-id="9f488-118">Form XML schema</span><span class="sxs-lookup"><span data-stu-id="9f488-118">Form XML schema</span></span>](customize-dev/form-xml-schema.md)  
 [<span data-ttu-id="9f488-119">FetchXML schema</span><span class="sxs-lookup"><span data-stu-id="9f488-119">FetchXML schema</span></span>](org-service/fetchxml-schema.md)  

## <a name="related-sections"></a><span data-ttu-id="9f488-120">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="9f488-120">Related Sections</span></span>

 [<span data-ttu-id="9f488-121">Schemas used in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="9f488-121">Schemas used in Dynamics 365 for Customer Engagement apps</span></span>](schemas-used-dynamics-365.md)  
 [<span data-ttu-id="9f488-122">When to Edit the Customizations File</span><span class="sxs-lookup"><span data-stu-id="9f488-122">When to Edit the Customizations File</span></span>](customize-dev/when-edit-customization-file.md)  
 [<span data-ttu-id="9f488-123">Edit the Customizations file with Schema Validation</span><span class="sxs-lookup"><span data-stu-id="9f488-123">Edit the Customizations file with Schema Validation</span></span>](customize-dev/edit-customizations-xml-file-schema-validation.md)  
 [<span data-ttu-id="9f488-124">Customize the Ribbon for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="9f488-124">Customize the Ribbon for Dynamics 365 for Customer Engagement apps</span></span>](customize-dev/customize-commands-ribbon.md)  
 [<span data-ttu-id="9f488-125">Change Application Navigation using the SiteMap</span><span class="sxs-lookup"><span data-stu-id="9f488-125">Change Application Navigation using the SiteMap</span></span>](/developer/customize-dev/change-application-navigation-using-sitemap.md)
