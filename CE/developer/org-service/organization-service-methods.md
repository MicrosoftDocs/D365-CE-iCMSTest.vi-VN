---
title: Organization service methods (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read about the set of methods that IOrganizationService web service provides that can be used to perform common operations like Create, Retrieve, RetrieveMultiple, Update and Delete on system and custom entities and on the metadata for your organization
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 34f69739-16d5-492c-bfd3-eee6772cd5eb
caps.latest.revision: 28
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a2a61005eff98c0256613872d49dced20aceecb1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388767"
---
# <a name="organization-service-methods"></a><span data-ttu-id="178b5-103">Organization service methods</span><span class="sxs-lookup"><span data-stu-id="178b5-103">Organization service methods</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="178b5-104">The <xref:Microsoft.Xrm.Sdk.IOrganizationService> interface provides a set of methods used to perform the most common operations on system and custom entities and on the metadata for your organization.</span><span class="sxs-lookup"><span data-stu-id="178b5-104">The <xref:Microsoft.Xrm.Sdk.IOrganizationService> interface provides a set of methods used to perform the most common operations on system and custom entities and on the metadata for your organization.</span></span> <span data-ttu-id="178b5-105">These operations can also be performed by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span><span class="sxs-lookup"><span data-stu-id="178b5-105">These operations can also be performed by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span></span> <span data-ttu-id="178b5-106">method and the corresponding message.</span><span class="sxs-lookup"><span data-stu-id="178b5-106">method and the corresponding message.</span></span>  
  
## <a name="create"></a><span data-ttu-id="178b5-107">Tạo</span><span class="sxs-lookup"><span data-stu-id="178b5-107">Create</span></span>  
 <span data-ttu-id="178b5-108">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span><span class="sxs-lookup"><span data-stu-id="178b5-108">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span></span> <span data-ttu-id="178b5-109">method to create an instance (record) of any entity that supports the **Create** message, including custom entities.</span><span class="sxs-lookup"><span data-stu-id="178b5-109">method to create an instance (record) of any entity that supports the **Create** message, including custom entities.</span></span>  
  
## <a name="retrieve"></a><span data-ttu-id="178b5-110">Truy xuất</span><span class="sxs-lookup"><span data-stu-id="178b5-110">Retrieve</span></span>  
 <span data-ttu-id="178b5-111">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span><span class="sxs-lookup"><span data-stu-id="178b5-111">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span></span> <span data-ttu-id="178b5-112">method to retrieve an instance (record) of an entity.</span><span class="sxs-lookup"><span data-stu-id="178b5-112">method to retrieve an instance (record) of an entity.</span></span>  
  
## <a name="retrievemultiple"></a><span data-ttu-id="178b5-113">RetrieveMultiple</span><span class="sxs-lookup"><span data-stu-id="178b5-113">RetrieveMultiple</span></span>  
 <span data-ttu-id="178b5-114">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span><span class="sxs-lookup"><span data-stu-id="178b5-114">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span></span> <span data-ttu-id="178b5-115">method to retrieve a collection records.</span><span class="sxs-lookup"><span data-stu-id="178b5-115">method to retrieve a collection records.</span></span> <span data-ttu-id="178b5-116">The query can be specified using a query expression or Fetch XML query.</span><span class="sxs-lookup"><span data-stu-id="178b5-116">The query can be specified using a query expression or Fetch XML query.</span></span>  
  
## <a name="update"></a><span data-ttu-id="178b5-117">Update</span><span class="sxs-lookup"><span data-stu-id="178b5-117">Update</span></span>  
 <span data-ttu-id="178b5-118">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span><span class="sxs-lookup"><span data-stu-id="178b5-118">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span></span> <span data-ttu-id="178b5-119">method to update an existing record.</span><span class="sxs-lookup"><span data-stu-id="178b5-119">method to update an existing record.</span></span>  
  
## <a name="delete"></a><span data-ttu-id="178b5-120">Xóa</span><span class="sxs-lookup"><span data-stu-id="178b5-120">Delete</span></span>  
 <span data-ttu-id="178b5-121">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span><span class="sxs-lookup"><span data-stu-id="178b5-121">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span></span> <span data-ttu-id="178b5-122">method to delete an existing record.</span><span class="sxs-lookup"><span data-stu-id="178b5-122">method to delete an existing record.</span></span>  
  
## <a name="associate"></a><span data-ttu-id="178b5-123">Liên kết</span><span class="sxs-lookup"><span data-stu-id="178b5-123">Associate</span></span>  
 <span data-ttu-id="178b5-124">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Associate*></span><span class="sxs-lookup"><span data-stu-id="178b5-124">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Associate*></span></span> <span data-ttu-id="178b5-125">method to create a link between two records that participate in a relationship.</span><span class="sxs-lookup"><span data-stu-id="178b5-125">method to create a link between two records that participate in a relationship.</span></span>  
  
## <a name="disassociate"></a><span data-ttu-id="178b5-126">Dừng liên kết</span><span class="sxs-lookup"><span data-stu-id="178b5-126">Disassociate</span></span>  
 <span data-ttu-id="178b5-127">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Disassociate*></span><span class="sxs-lookup"><span data-stu-id="178b5-127">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Disassociate*></span></span> <span data-ttu-id="178b5-128">method to delete the link between two records.</span><span class="sxs-lookup"><span data-stu-id="178b5-128">method to delete the link between two records.</span></span>  
  
## <a name="execute"></a><span data-ttu-id="178b5-129">Thực thi</span><span class="sxs-lookup"><span data-stu-id="178b5-129">Execute</span></span>  
 <span data-ttu-id="178b5-130">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span><span class="sxs-lookup"><span data-stu-id="178b5-130">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span></span> <span data-ttu-id="178b5-131">method to execute a message.</span><span class="sxs-lookup"><span data-stu-id="178b5-131">method to execute a message.</span></span> <span data-ttu-id="178b5-132">This includes common processing like create and delete of data records and metadata, or it can be specialized processing such as import or detect duplicates.</span><span class="sxs-lookup"><span data-stu-id="178b5-132">This includes common processing like create and delete of data records and metadata, or it can be specialized processing such as import or detect duplicates.</span></span>  
  
## <a name="example"></a><span data-ttu-id="178b5-133">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="178b5-133">Example</span></span>  
 <span data-ttu-id="178b5-134">The following code shows how to use the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>, <xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>, and <xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*> methods using the strong types.</span><span class="sxs-lookup"><span data-stu-id="178b5-134">The following code shows how to use the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>, <xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>, and <xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*> methods using the strong types.</span></span>  
  
 [!code-csharp[StrongTypes#CompoundCreateUpdate1](../../snippets/csharp/CRMV8/strongtypes/cs/compoundcreateupdate1.cs#compoundcreateupdate1)]  
  
### <a name="see-also"></a><span data-ttu-id="178b5-135">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="178b5-135">See also</span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService><br />
 [<span data-ttu-id="178b5-136">Use the IOrganizationService web service to read and write data or metadata</span><span class="sxs-lookup"><span data-stu-id="178b5-136">Use the IOrganizationService web service to read and write data or metadata</span></span>](use-organization-service-read-write-data-metadata.md)<br />
 [<span data-ttu-id="178b5-137">Use messages (request and response classes) with the Execute method</span><span class="sxs-lookup"><span data-stu-id="178b5-137">Use messages (request and response classes) with the Execute method</span></span>](use-messages-request-response-classes-execute-method.md)<br />
 [<span data-ttu-id="178b5-138">Use ExecuteMultiple to improve performance for bulk data load</span><span class="sxs-lookup"><span data-stu-id="178b5-138">Use ExecuteMultiple to improve performance for bulk data load</span></span>](use-executemultiple-improve-performance-bulk-data-load.md)<br />
 [<span data-ttu-id="178b5-139">Microsoft.Xrm.Sdk Messages</span><span class="sxs-lookup"><span data-stu-id="178b5-139">Microsoft.Xrm.Sdk Messages</span></span>](xrm-messages-organization-service.md)<br />
 [<span data-ttu-id="178b5-140">Microsoft.Crm.Sdk Messages</span><span class="sxs-lookup"><span data-stu-id="178b5-140">Microsoft.Crm.Sdk Messages</span></span>](organization-service-messages.md)<br />
 [<span data-ttu-id="178b5-141">Authenticate users in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="178b5-141">Authenticate users in Dynamics 365 for Customer Engagement apps</span></span>](../authenticate-users.md)<br />
 [<span data-ttu-id="178b5-142">Sample: Create, Retrieve, Update and Delete (CRUD) Using Strong Types</span><span class="sxs-lookup"><span data-stu-id="178b5-142">Sample: Create, Retrieve, Update and Delete (CRUD) Using Strong Types</span></span>](sample-create-retrieve-update-delete-records-early-bound.md)<br />
 [<span data-ttu-id="178b5-143">Sample: Create, Retrieve, Update and Delete (CRUD) Using Property Bag (Loosely-typed)</span><span class="sxs-lookup"><span data-stu-id="178b5-143">Sample: Create, Retrieve, Update and Delete (CRUD) Using Property Bag (Loosely-typed)</span></span>](sample-create-retrieve-update-delete-late-bound.md)
