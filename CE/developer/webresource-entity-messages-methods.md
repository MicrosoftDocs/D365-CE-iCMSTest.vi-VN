---
title: WebResource entity messages and methods (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about web resource that stores the data equivalent to files used in web development. Web resources are client-side components that provide custom user interface elements. The schema name for this entity is WebResource.
ms.custom: ''
ms.date: 12/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 6472bf88-4948-49f3-9f53-a4ef13abb702
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c286aeef3a939de6c715a24d83638c54699317a6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388720"
---
# <a name="webresource-entity-messages-and-methods"></a><span data-ttu-id="e970c-105">WebResource entity messages and methods</span><span class="sxs-lookup"><span data-stu-id="e970c-105">WebResource entity messages and methods</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e970c-106">A *web resource* stores the data equivalent to files used in web development.</span><span class="sxs-lookup"><span data-stu-id="e970c-106">A *web resource* stores the data equivalent to files used in web development.</span></span> <span data-ttu-id="e970c-107">Web resources are client-side components that provide custom user interface elements.</span><span class="sxs-lookup"><span data-stu-id="e970c-107">Web resources are client-side components that provide custom user interface elements.</span></span> <span data-ttu-id="e970c-108">These resources are stored in the [WebResource Entity](entities/webresource.md).</span><span class="sxs-lookup"><span data-stu-id="e970c-108">These resources are stored in the [WebResource Entity](entities/webresource.md).</span></span>  
  
 <span data-ttu-id="e970c-109">The following table describes the messages for this entity, which you use with the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span><span class="sxs-lookup"><span data-stu-id="e970c-109">The following table describes the messages for this entity, which you use with the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span></span> <span data-ttu-id="e970c-110">method.</span><span class="sxs-lookup"><span data-stu-id="e970c-110">method.</span></span>  
  
|<span data-ttu-id="e970c-111">Thông báo</span><span class="sxs-lookup"><span data-stu-id="e970c-111">Message</span></span>|<span data-ttu-id="e970c-112">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e970c-112">Description</span></span>|  
|-------------|-----------------|  
|<xref:Microsoft.Xrm.Sdk.Messages.CreateRequest>|<span data-ttu-id="e970c-113">Creates a web resource.</span><span class="sxs-lookup"><span data-stu-id="e970c-113">Creates a web resource.</span></span> <span data-ttu-id="e970c-114">You can also call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span><span class="sxs-lookup"><span data-stu-id="e970c-114">You can also call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span></span> <span data-ttu-id="e970c-115">method.</span><span class="sxs-lookup"><span data-stu-id="e970c-115">method.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest>|<span data-ttu-id="e970c-116">Deletes a web resource.</span><span class="sxs-lookup"><span data-stu-id="e970c-116">Deletes a web resource.</span></span> <span data-ttu-id="e970c-117">You can also call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span><span class="sxs-lookup"><span data-stu-id="e970c-117">You can also call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span></span> <span data-ttu-id="e970c-118">method.</span><span class="sxs-lookup"><span data-stu-id="e970c-118">method.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveRequest>|<span data-ttu-id="e970c-119">Retrieves a web resource.</span><span class="sxs-lookup"><span data-stu-id="e970c-119">Retrieves a web resource.</span></span> <span data-ttu-id="e970c-120">You can also call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span><span class="sxs-lookup"><span data-stu-id="e970c-120">You can also call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span></span> <span data-ttu-id="e970c-121">method.</span><span class="sxs-lookup"><span data-stu-id="e970c-121">method.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest>|<span data-ttu-id="e970c-122">Retrieves a collection of web resources.</span><span class="sxs-lookup"><span data-stu-id="e970c-122">Retrieves a collection of web resources.</span></span> <span data-ttu-id="e970c-123">You can also call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span><span class="sxs-lookup"><span data-stu-id="e970c-123">You can also call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span></span> <span data-ttu-id="e970c-124">method.</span><span class="sxs-lookup"><span data-stu-id="e970c-124">method.</span></span>|  
|<xref:Microsoft.Crm.Sdk.Messages.RetrieveUnpublishedRequest>|<span data-ttu-id="e970c-125">Retrieves the current saved definition of a web resource regardless whether it has been published.</span><span class="sxs-lookup"><span data-stu-id="e970c-125">Retrieves the current saved definition of a web resource regardless whether it has been published.</span></span>|  
|<xref:Microsoft.Crm.Sdk.Messages.RetrieveUnpublishedMultipleRequest>|<span data-ttu-id="e970c-126">Retrieves the current saved definition of web resources regardless whether they have been published.</span><span class="sxs-lookup"><span data-stu-id="e970c-126">Retrieves the current saved definition of web resources regardless whether they have been published.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest>|<span data-ttu-id="e970c-127">Updates a web resource.</span><span class="sxs-lookup"><span data-stu-id="e970c-127">Updates a web resource.</span></span> <span data-ttu-id="e970c-128">You can also call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span><span class="sxs-lookup"><span data-stu-id="e970c-128">You can also call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span></span> <span data-ttu-id="e970c-129">method.</span><span class="sxs-lookup"><span data-stu-id="e970c-129">method.</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="e970c-130">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e970c-130">See also</span></span>

 [<span data-ttu-id="e970c-131">Web Resources for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="e970c-131">Web Resources for Dynamics 365 for Customer Engagement apps</span></span>](web-resources.md)<br />
 [<span data-ttu-id="e970c-132">Sample: Pass Multiple Values to a  Web Resource Through the Data Parameter</span><span class="sxs-lookup"><span data-stu-id="e970c-132">Sample: Pass Multiple Values to a  Web Resource Through the Data Parameter</span></span>](sample-pass-multiple-values-web-resource-through-data-parameter.md)<br />
