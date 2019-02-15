---
title: Annotation (note) entity | MicrosoftDocs
description: Learn about annotation entity to append additional information to any record in the database. The annotation  entity represents an annotation and contains the annotation text, who created and modified the annotation, and whether a file is attached to the annotation.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 662cf95d-3bca-464a-983b-54b572e79aa2
caps.latest.revision: 29
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 87206e8a3da4643147cdc494576a337e1ab3b539
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387496"
---
# <a name="annotation-note-entity"></a><span data-ttu-id="6b22d-104">Annotation (note) entity</span><span class="sxs-lookup"><span data-stu-id="6b22d-104">Annotation (note) entity</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6b22d-105">The *annotations (notes)* provide easy ways to append additional information to any record in the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] database.</span><span class="sxs-lookup"><span data-stu-id="6b22d-105">The *annotations (notes)* provide easy ways to append additional information to any record in the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] database.</span></span> <span data-ttu-id="6b22d-106">An annotation (note) is a text entry that can be associated with any entity in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="6b22d-106">An annotation (note) is a text entry that can be associated with any entity in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="6b22d-107">However, you can associate annotations with only those custom entities that are created with the <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest.HasNotes> property set to `true` in the <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest> class.</span><span class="sxs-lookup"><span data-stu-id="6b22d-107">However, you can associate annotations with only those custom entities that are created with the <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest.HasNotes> property set to `true` in the <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest> class.</span></span> <span data-ttu-id="6b22d-108">You can update a custom entity, which is not enabled for notes, to have notes by setting the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest>.<xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest.HasNotes></span><span class="sxs-lookup"><span data-stu-id="6b22d-108">You can update a custom entity, which is not enabled for notes, to have notes by setting the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest>.<xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest.HasNotes></span></span> <span data-ttu-id="6b22d-109">property to `true`.</span><span class="sxs-lookup"><span data-stu-id="6b22d-109">property to `true`.</span></span>  

<span data-ttu-id="6b22d-110">Using the Web API, set the `HasNotes` property of the <xref:Microsoft.Dynamics.CRM.EntityMetadata> EntityType controls this.</span><span class="sxs-lookup"><span data-stu-id="6b22d-110">Using the Web API, set the `HasNotes` property of the <xref:Microsoft.Dynamics.CRM.EntityMetadata> EntityType controls this.</span></span>
  
 <span data-ttu-id="6b22d-111">The `Annotation` entity represents an annotation (note), and contains the following information:</span><span class="sxs-lookup"><span data-stu-id="6b22d-111">The `Annotation` entity represents an annotation (note), and contains the following information:</span></span>  
  
- <span data-ttu-id="6b22d-112">Annotation (note) text</span><span class="sxs-lookup"><span data-stu-id="6b22d-112">Annotation (note) text</span></span>  
  
- <span data-ttu-id="6b22d-113">Who created and modified the annotation (note)</span><span class="sxs-lookup"><span data-stu-id="6b22d-113">Who created and modified the annotation (note)</span></span>  
  
- <span data-ttu-id="6b22d-114">Whether a file is attached to the annotation (note)</span><span class="sxs-lookup"><span data-stu-id="6b22d-114">Whether a file is attached to the annotation (note)</span></span>  
  
  <span data-ttu-id="6b22d-115">An attached file can be any standard computer file format that includes [!INCLUDE[pn_MS_Word_Full](../includes/pn-ms-word-full.md)] documents, [!INCLUDE[pn_MS_Excel_Full](../includes/pn-ms-excel-full.md)] spreadsheets, CAD files, and PDF files.</span><span class="sxs-lookup"><span data-stu-id="6b22d-115">An attached file can be any standard computer file format that includes [!INCLUDE[pn_MS_Word_Full](../includes/pn-ms-word-full.md)] documents, [!INCLUDE[pn_MS_Excel_Full](../includes/pn-ms-excel-full.md)] spreadsheets, CAD files, and PDF files.</span></span> <span data-ttu-id="6b22d-116">An attachment can be associated with any object, other than an annotation (note), in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="6b22d-116">An attachment can be associated with any object, other than an annotation (note), in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span>  
  
  <span data-ttu-id="6b22d-117">To upload or remove an attachment, use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span><span class="sxs-lookup"><span data-stu-id="6b22d-117">To upload or remove an attachment, use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span></span> <span data-ttu-id="6b22d-118">method or <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message, setting the `Annotation.Filename` and `Annotation.MimeType` properties.</span><span class="sxs-lookup"><span data-stu-id="6b22d-118">method or <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message, setting the `Annotation.Filename` and `Annotation.MimeType` properties.</span></span> <span data-ttu-id="6b22d-119">This uploads an attachment that has been decoded into a base64 string format.</span><span class="sxs-lookup"><span data-stu-id="6b22d-119">This uploads an attachment that has been decoded into a base64 string format.</span></span> <span data-ttu-id="6b22d-120">The [System.Convert.ToBase64String](https://msdn.microsoft.com/library/system.convert.tobase64string.aspx) method can be used to convert the contents of a data file into a base64-formatted string.</span><span class="sxs-lookup"><span data-stu-id="6b22d-120">The [System.Convert.ToBase64String](https://msdn.microsoft.com/library/system.convert.tobase64string.aspx) method can be used to convert the contents of a data file into a base64-formatted string.</span></span> [!INCLUDE[sdk_MaxUploadFileSize](../includes/sdk-maxuploadfilesize.md)]  
  
## <a name="in-this-section"></a><span data-ttu-id="6b22d-121">In This Section</span><span class="sxs-lookup"><span data-stu-id="6b22d-121">In This Section</span></span>  
 [<span data-ttu-id="6b22d-122">Sample: Upload, Retrieve, and Download an Attachment</span><span class="sxs-lookup"><span data-stu-id="6b22d-122">Sample: Upload, Retrieve, and Download an Attachment</span></span>](sample-upload-retrieve-download-attachment.md)  
  
### <a name="see-also"></a><span data-ttu-id="6b22d-123">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="6b22d-123">See also</span></span> 
 <span data-ttu-id="6b22d-124">[Annotation Entity](entities/annotation.md) </span><span class="sxs-lookup"><span data-stu-id="6b22d-124">[Annotation Entity](entities/annotation.md) </span></span>  
 <span data-ttu-id="6b22d-125">[Model Your Business Data](model-business-data.md) </span><span class="sxs-lookup"><span data-stu-id="6b22d-125">[Model Your Business Data](model-business-data.md) </span></span>  
 [<span data-ttu-id="6b22d-126">UserQuery (Saved View) Entity</span><span class="sxs-lookup"><span data-stu-id="6b22d-126">UserQuery (Saved View) Entity</span></span>](userquery-saved-view-entity.md)
