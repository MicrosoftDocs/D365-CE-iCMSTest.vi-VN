---
title: Use an alternate key to create a record (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Alternate keys can be used to create instances of Entity and EntityReference classes. This topic discusses the usage patterns and possible exceptions that might be thrown when using alternate keys.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: fa8762cd-b714-49df-8756-ba0a70e6fc97
caps.latest.revision: 15
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2daba632f48679fc2ff5647cb62d4e693939ea21
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388088"
---
# <a name="use-an-alternate-key-to-create-a-record"></a><span data-ttu-id="61117-104">Use an alternate key to create a record</span><span class="sxs-lookup"><span data-stu-id="61117-104">Use an alternate key to create a record</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="61117-105">You   can now use alternate keys to create instances of <xref:Microsoft.Xrm.Sdk.Entity> and <xref:Microsoft.Xrm.Sdk.EntityReference> classes.</span><span class="sxs-lookup"><span data-stu-id="61117-105">You   can now use alternate keys to create instances of <xref:Microsoft.Xrm.Sdk.Entity> and <xref:Microsoft.Xrm.Sdk.EntityReference> classes.</span></span> <span data-ttu-id="61117-106">This topic discusses the usage patterns and possible exceptions that might be thrown when using alternate keys.</span><span class="sxs-lookup"><span data-stu-id="61117-106">This topic discusses the usage patterns and possible exceptions that might be thrown when using alternate keys.</span></span> <span data-ttu-id="61117-107">To understand how to define alternate keys for an entity, see [Define alternate keys for an entity](define-alternate-keys-entity.md).</span><span class="sxs-lookup"><span data-stu-id="61117-107">To understand how to define alternate keys for an entity, see [Define alternate keys for an entity](define-alternate-keys-entity.md).</span></span>  
  
<a name="BKMK_entity"></a>   
## <a name="using-alternate-keys-to-create-an-entity"></a><span data-ttu-id="61117-108">Using alternate keys to create an entity</span><span class="sxs-lookup"><span data-stu-id="61117-108">Using alternate keys to create an entity</span></span>  
 <span data-ttu-id="61117-109">You can now create an <xref:Microsoft.Xrm.Sdk.Entity> with a primary ID or with a single `KeyAttribute` in a single call using the new constructor.</span><span class="sxs-lookup"><span data-stu-id="61117-109">You can now create an <xref:Microsoft.Xrm.Sdk.Entity> with a primary ID or with a single `KeyAttribute` in a single call using the new constructor.</span></span>  
  
```csharp  
public Entity (string logicalName, Guid id) {…}    
public Entity (string logicalName, string keyName, object keyValue) {…}  
public Entity (string logicalName, KeyAttributeCollection keyAttributes) {…}  
  
```  
  
 <span data-ttu-id="61117-110">A valid <xref:Microsoft.Xrm.Sdk.Entity> used for update operations includes a logical name of the entity and one of the following:</span><span class="sxs-lookup"><span data-stu-id="61117-110">A valid <xref:Microsoft.Xrm.Sdk.Entity> used for update operations includes a logical name of the entity and one of the following:</span></span>  
  
-   <span data-ttu-id="61117-111">A value for ID (primary key GUID value) (or)</span><span class="sxs-lookup"><span data-stu-id="61117-111">A value for ID (primary key GUID value) (or)</span></span>  
  
-   <span data-ttu-id="61117-112">A <xref:Microsoft.Xrm.Sdk.KeyAttributeCollection> with a valid set of attributes matching a defined key for the entity.</span><span class="sxs-lookup"><span data-stu-id="61117-112">A <xref:Microsoft.Xrm.Sdk.KeyAttributeCollection> with a valid set of attributes matching a defined key for the entity.</span></span>  
  
<a name="BKMK_EntityReference"></a>   
## <a name="using-alternate-keys-to-create-an-entityreference"></a><span data-ttu-id="61117-113">Using alternate keys to create an EntityReference</span><span class="sxs-lookup"><span data-stu-id="61117-113">Using alternate keys to create an EntityReference</span></span>  
 <span data-ttu-id="61117-114">You can also create an <xref:Microsoft.Xrm.Sdk.EntityReference> without a primary ID, and with a single `KeyAttribute` in a single call using the new constructor.</span><span class="sxs-lookup"><span data-stu-id="61117-114">You can also create an <xref:Microsoft.Xrm.Sdk.EntityReference> without a primary ID, and with a single `KeyAttribute` in a single call using the new constructor.</span></span>  
  
```csharp  
public EntityReference(string logicalName, Guid id) {…}    
public EntityReference(string logicalName, string keyName, object keyValue) {…}    
public EntityReference(string logicalName, KeyAttributeCollection keyAttributeCollection) {…}  
  
```  
  
 <span data-ttu-id="61117-115">A valid <xref:Microsoft.Xrm.Sdk.EntityReference> includes a logical name of the entity and either:</span><span class="sxs-lookup"><span data-stu-id="61117-115">A valid <xref:Microsoft.Xrm.Sdk.EntityReference> includes a logical name of the entity and either:</span></span>  
  
-   <span data-ttu-id="61117-116">A value for ID (primary key GUID value) or</span><span class="sxs-lookup"><span data-stu-id="61117-116">A value for ID (primary key GUID value) or</span></span>  
  
-   <span data-ttu-id="61117-117">A <xref:Microsoft.Xrm.Sdk.KeyAttributeCollection> collection with a valid set of attributes matching a defined key for the entity.</span><span class="sxs-lookup"><span data-stu-id="61117-117">A <xref:Microsoft.Xrm.Sdk.KeyAttributeCollection> collection with a valid set of attributes matching a defined key for the entity.</span></span>  
  
<a name="BKMK_input"></a>   
## <a name="alternative-input-to-messages"></a><span data-ttu-id="61117-118">Alternative input to messages</span><span class="sxs-lookup"><span data-stu-id="61117-118">Alternative input to messages</span></span>  
 <span data-ttu-id="61117-119">When passing entities to <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> and <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest>, values provided for Lookup attributes using an <xref:Microsoft.Xrm.Sdk.EntityReference> can now use <xref:Microsoft.Xrm.Sdk.EntityReference> with alternate keys defined in <xref:Microsoft.Xrm.Sdk.EntityReference.KeyAttributes> to specify related record.</span><span class="sxs-lookup"><span data-stu-id="61117-119">When passing entities to <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> and <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest>, values provided for Lookup attributes using an <xref:Microsoft.Xrm.Sdk.EntityReference> can now use <xref:Microsoft.Xrm.Sdk.EntityReference> with alternate keys defined in <xref:Microsoft.Xrm.Sdk.EntityReference.KeyAttributes> to specify related record.</span></span>  <span data-ttu-id="61117-120">These will be resolved to and replaced by primary ID based entity references before the messages are processed.</span><span class="sxs-lookup"><span data-stu-id="61117-120">These will be resolved to and replaced by primary ID based entity references before the messages are processed.</span></span>  
  
<a name="BKMK_Exceptions"></a>   
## <a name="exceptions-when-using-alternate-keys"></a><span data-ttu-id="61117-121">Exceptions when using alternate keys</span><span class="sxs-lookup"><span data-stu-id="61117-121">Exceptions when using alternate keys</span></span>  
 <span data-ttu-id="61117-122">You have to be aware of the following conditions and possible exceptions when using alternate keys:</span><span class="sxs-lookup"><span data-stu-id="61117-122">You have to be aware of the following conditions and possible exceptions when using alternate keys:</span></span>  
  
-   <span data-ttu-id="61117-123">The primary ID is used if it is provided.</span><span class="sxs-lookup"><span data-stu-id="61117-123">The primary ID is used if it is provided.</span></span> <span data-ttu-id="61117-124">If it is not provided, it will examine the <xref:Microsoft.Xrm.Sdk.KeyAttributeCollection>.</span><span class="sxs-lookup"><span data-stu-id="61117-124">If it is not provided, it will examine the <xref:Microsoft.Xrm.Sdk.KeyAttributeCollection>.</span></span>  <span data-ttu-id="61117-125">If the <xref:Microsoft.Xrm.Sdk.KeyAttributeCollection> is not provided, it will throw an error.</span><span class="sxs-lookup"><span data-stu-id="61117-125">If the <xref:Microsoft.Xrm.Sdk.KeyAttributeCollection> is not provided, it will throw an error.</span></span>  
  
-   <span data-ttu-id="61117-126">If the provided <xref:Microsoft.Xrm.Sdk.KeyAttributeCollection> includes one attribute that is the primary key of the entity and the value is valid, it populates the ID property of the <xref:Microsoft.Xrm.Sdk.Entity> or <xref:Microsoft.Xrm.Sdk.EntityReference> with the provided value.</span><span class="sxs-lookup"><span data-stu-id="61117-126">If the provided <xref:Microsoft.Xrm.Sdk.KeyAttributeCollection> includes one attribute that is the primary key of the entity and the value is valid, it populates the ID property of the <xref:Microsoft.Xrm.Sdk.Entity> or <xref:Microsoft.Xrm.Sdk.EntityReference> with the provided value.</span></span>  
  
-   <span data-ttu-id="61117-127">If the key attributes are provided, the system attempts to match the set of attributes provided with the keys defined for the <xref:Microsoft.Xrm.Sdk.Entity>.</span><span class="sxs-lookup"><span data-stu-id="61117-127">If the key attributes are provided, the system attempts to match the set of attributes provided with the keys defined for the <xref:Microsoft.Xrm.Sdk.Entity>.</span></span>  <span data-ttu-id="61117-128">If it does not find a match, it will throw an error.</span><span class="sxs-lookup"><span data-stu-id="61117-128">If it does not find a match, it will throw an error.</span></span>  <span data-ttu-id="61117-129">If it does find a match, it will validate the provided values for those attributes.</span><span class="sxs-lookup"><span data-stu-id="61117-129">If it does find a match, it will validate the provided values for those attributes.</span></span> <span data-ttu-id="61117-130">If valid, it will retrieve the ID of the record that matched the provided key values, and populate the ID value of the <xref:Microsoft.Xrm.Sdk.Entity> or <xref:Microsoft.Xrm.Sdk.EntityReference> with this value.</span><span class="sxs-lookup"><span data-stu-id="61117-130">If valid, it will retrieve the ID of the record that matched the provided key values, and populate the ID value of the <xref:Microsoft.Xrm.Sdk.Entity> or <xref:Microsoft.Xrm.Sdk.EntityReference> with this value.</span></span>  
  
-   <span data-ttu-id="61117-131">If you specify an attribute set that is not defined as a unique key, an error will be thrown indicating that use of unique key attributes is required.</span><span class="sxs-lookup"><span data-stu-id="61117-131">If you specify an attribute set that is not defined as a unique key, an error will be thrown indicating that use of unique key attributes is required.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="61117-132">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="61117-132">See also</span></span>  
 <span data-ttu-id="61117-133">[Define alternate keys for an entity](define-alternate-keys-entity.md) </span><span class="sxs-lookup"><span data-stu-id="61117-133">[Define alternate keys for an entity](define-alternate-keys-entity.md) </span></span>  
 <span data-ttu-id="61117-134">[Use change tracking to synchronize data with external systems](use-change-tracking-synchronize-data-external-systems.md) </span><span class="sxs-lookup"><span data-stu-id="61117-134">[Use change tracking to synchronize data with external systems](use-change-tracking-synchronize-data-external-systems.md) </span></span>  
 [<span data-ttu-id="61117-135">Use Upsert to insert or update a record</span><span class="sxs-lookup"><span data-stu-id="61117-135">Use Upsert to insert or update a record</span></span>](use-upsert-insert-update-record.md)
