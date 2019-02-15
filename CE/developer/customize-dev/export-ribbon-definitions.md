---
title: Export ribbon definitions (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about exporting the ribbon definitions.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- ribbon, ribbon data
ms.assetid: f3992ccf-72c5-4347-a7db-a6796f8a4df0
caps.latest.revision: 28
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 07bbb6afafb529c3b9a37e79fbefb2d76badc150
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387694"
---
# <a name="export-ribbon-definitions"></a><span data-ttu-id="ba4ed-103">Export ribbon definitions</span><span class="sxs-lookup"><span data-stu-id="ba4ed-103">Export ribbon definitions</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ba4ed-104">To effectively define changes to the default RibbonXml, you must be able to reference the RibbonXml data that defines those ribbons.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-104">To effectively define changes to the default RibbonXml, you must be able to reference the RibbonXml data that defines those ribbons.</span></span>  
  
<a name="BKMK_AccessRibbonDefinitionsForYourOrganization"></a>   
## <a name="access-the-ribbon-definitions-for-your-organization"></a><span data-ttu-id="ba4ed-105">Access the ribbon definitions for your organization</span><span class="sxs-lookup"><span data-stu-id="ba4ed-105">Access the ribbon definitions for your organization</span></span>  
 <span data-ttu-id="ba4ed-106">If the Ribbon for your organization has been modified, you should export the current definitions if you intend to work with the customized ribbon elements.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-106">If the Ribbon for your organization has been modified, you should export the current definitions if you intend to work with the customized ribbon elements.</span></span> <span data-ttu-id="ba4ed-107">To do this, use the exportribbonxml sample located at `SampleCode\CS\Client\Ribbon\ExportRibbonXml`.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-107">To do this, use the exportribbonxml sample located at `SampleCode\CS\Client\Ribbon\ExportRibbonXml`.</span></span>  
  
<a name="BKMK_AccessDefaultRibbonData"></a>   
## <a name="access-the-default-ribbon-data"></a><span data-ttu-id="ba4ed-108">Access the default ribbon data</span><span class="sxs-lookup"><span data-stu-id="ba4ed-108">Access the default ribbon data</span></span>  
 <span data-ttu-id="ba4ed-109">The default ribbon definitions for [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement can be downloaded from [Microsoft Downloads: ExportedRibbonXml.zip](http://download.microsoft.com/download/C/2/A/C2A79C47-DD2D-4938-A595-092CAFF32D6B/ExportedRibbonXml.zip).</span><span class="sxs-lookup"><span data-stu-id="ba4ed-109">The default ribbon definitions for [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement can be downloaded from [Microsoft Downloads: ExportedRibbonXml.zip](http://download.microsoft.com/download/C/2/A/C2A79C47-DD2D-4938-A595-092CAFF32D6B/ExportedRibbonXml.zip).</span></span> 
  
 <span data-ttu-id="ba4ed-110">The applicationRibbon.xml file contains the definition of the core application ribbons.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-110">The applicationRibbon.xml file contains the definition of the core application ribbons.</span></span>  
  
 <span data-ttu-id="ba4ed-111">The remaining files contain the definitions used by entities that have ribbon definitions that differ from the entity template.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-111">The remaining files contain the definitions used by entities that have ribbon definitions that differ from the entity template.</span></span> <span data-ttu-id="ba4ed-112">Each file is named according to the name of the entity: logical entity name + Ribbon.xml.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-112">Each file is named according to the name of the entity: logical entity name + Ribbon.xml.</span></span>  
  
 <span data-ttu-id="ba4ed-113">These files represent the output of two messages using the [Sample: Export Ribbon Definitions](sample-export-ribbon-definitions.md):</span><span class="sxs-lookup"><span data-stu-id="ba4ed-113">These files represent the output of two messages using the [Sample: Export Ribbon Definitions](sample-export-ribbon-definitions.md):</span></span>  
  
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveApplicationRibbonRequest>  
 <span data-ttu-id="ba4ed-114">This message retrieves the core application ribbons including the entity template.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-114">This message retrieves the core application ribbons including the entity template.</span></span>  
  
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveEntityRibbonRequest>  
 <span data-ttu-id="ba4ed-115">This message retrieves the ribbon definition used for a specific entity.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-115">This message retrieves the ribbon definition used for a specific entity.</span></span>  
  
### <a name="decompress-the-ribbon-data"></a><span data-ttu-id="ba4ed-116">Decompress the ribbon data</span><span class="sxs-lookup"><span data-stu-id="ba4ed-116">Decompress the ribbon data</span></span>  
 <span data-ttu-id="ba4ed-117">The ribbon data is exported as a compressed file.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-117">The ribbon data is exported as a compressed file.</span></span> <span data-ttu-id="ba4ed-118">To decompress the file into XML you have to use the [System.IO.Packaging.ZipPackage](https://msdn.microsoft.com/library/system.io.packaging.zippackage.aspx) class.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-118">To decompress the file into XML you have to use the [System.IO.Packaging.ZipPackage](https://msdn.microsoft.com/library/system.io.packaging.zippackage.aspx) class.</span></span> <span data-ttu-id="ba4ed-119">The following example is a helper method used in the SDK sample to decompress the file.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-119">The following example is a helper method used in the SDK sample to decompress the file.</span></span>  
  
 [!code-csharp[ExportRibbonXml#ExportRibbonXml2](../../snippets/csharp/CRMV8/exportribbonxml/cs/exportribbonxml2.cs#exportribbonxml2)]  

  
### <a name="retrieve-the-application-ribbon-data"></a><span data-ttu-id="ba4ed-120">Retrieve the application ribbon data</span><span class="sxs-lookup"><span data-stu-id="ba4ed-120">Retrieve the application ribbon data</span></span>  
 <span data-ttu-id="ba4ed-121">The application ribbon can be retrieved using the <xref:Microsoft.Crm.Sdk.Messages.RetrieveApplicationRibbonRequest> as shown in the following sample.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-121">The application ribbon can be retrieved using the <xref:Microsoft.Crm.Sdk.Messages.RetrieveApplicationRibbonRequest> as shown in the following sample.</span></span>  
  
 [!code-csharp[ExportRibbonXml#ExportRibbonXml3](../../snippets/csharp/CRMV8/exportribbonxml/cs/exportribbonxml3.cs#exportribbonxml3)]  

  
### <a name="retrieve-entity-ribbons"></a><span data-ttu-id="ba4ed-122">Retrieve entity ribbons</span><span class="sxs-lookup"><span data-stu-id="ba4ed-122">Retrieve entity ribbons</span></span>  
 <span data-ttu-id="ba4ed-123">To retrieve the ribbon definition for entities, you can just include the name of the entity as a parameter to the <xref:Microsoft.Crm.Sdk.Messages.RetrieveEntityRibbonRequest>.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-123">To retrieve the ribbon definition for entities, you can just include the name of the entity as a parameter to the <xref:Microsoft.Crm.Sdk.Messages.RetrieveEntityRibbonRequest>.</span></span>  
  
 <span data-ttu-id="ba4ed-124">To retrieve the ribbon definitions for all entities that support the ribbon you need a list of those system entities that have ribbon definitions that vary from the entity ribbon template.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-124">To retrieve the ribbon definitions for all entities that support the ribbon you need a list of those system entities that have ribbon definitions that vary from the entity ribbon template.</span></span> <span data-ttu-id="ba4ed-125">The following sample shows an array of all the system entities that have ribbon definitions.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-125">The following sample shows an array of all the system entities that have ribbon definitions.</span></span>  
  
 [!code-csharp[ExportRibbonXml#ExportRibbonXml6](../../snippets/csharp/CRMV8/exportribbonxml/cs/exportribbonxml6.cs#exportribbonxml6)]  
  
 <span data-ttu-id="ba4ed-126">The following sample shows how to retrieve the ribbon definitions for a set of entities.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-126">The following sample shows how to retrieve the ribbon definitions for a set of entities.</span></span>  
  
 [!code-csharp[ExportRibbonXml#ExportRibbonXml4](../../snippets/csharp/CRMV8/exportribbonxml/cs/exportribbonxml4.cs#exportribbonxml4)]  
  
 <span data-ttu-id="ba4ed-127">Any custom entities also support ribbon customizations.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-127">Any custom entities also support ribbon customizations.</span></span> <span data-ttu-id="ba4ed-128">To get a list of custom entities, use the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest> and retrieve the names of custom entities.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-128">To get a list of custom entities, use the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest> and retrieve the names of custom entities.</span></span> <span data-ttu-id="ba4ed-129">The following sample shows how to retrieve ribbon definitions for all custom entities.</span><span class="sxs-lookup"><span data-stu-id="ba4ed-129">The following sample shows how to retrieve ribbon definitions for all custom entities.</span></span>  
  
 [!code-csharp[ExportRibbonXml#ExportRibbonXml5](../../snippets/csharp/CRMV8/exportribbonxml/cs/exportribbonxml5.cs#exportribbonxml5)]  
  
### <a name="see-also"></a><span data-ttu-id="ba4ed-130">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ba4ed-130">See also</span></span>  
 <span data-ttu-id="ba4ed-131">[Customize the Ribbon for Microsoft Dynamics 365 for Customer Engagement](customize-commands-ribbon.md) </span><span class="sxs-lookup"><span data-stu-id="ba4ed-131">[Customize the Ribbon for Microsoft Dynamics 365 for Customer Engagement](customize-commands-ribbon.md) </span></span>  
 <span data-ttu-id="ba4ed-132">[Command bar or ribbon presentation](command-bar-ribbon-presentation.md) </span><span class="sxs-lookup"><span data-stu-id="ba4ed-132">[Command bar or ribbon presentation](command-bar-ribbon-presentation.md) </span></span>  
 [<span data-ttu-id="ba4ed-133">Export, Prepare to Edit, and Import the Ribbon</span><span class="sxs-lookup"><span data-stu-id="ba4ed-133">Export, Prepare to Edit, and Import the Ribbon</span></span>](export-prepare-edit-import-ribbon.md)
