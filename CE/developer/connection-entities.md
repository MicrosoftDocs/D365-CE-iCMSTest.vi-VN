---
title: Connection entities (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Connection entites help you enable, create, and query connections.
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
- creating graphs and charts to visually represent connections
- connection entities, using to create connections
- connecting two records
- creating multiple connections and roles for records
- querying connections for data
- connections, definition
- enabling connections, connection entities
- creating connection roles between records
- associating entity records, connection entities
ms.assetid: 98700871-a986-4982-900e-5fd5f6ee5a26
caps.latest.revision: 37
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 82df0c443732a1c5c6edd08b9329864aa7c35945
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388520"
---
# <a name="connection-entities"></a><span data-ttu-id="e2849-103">Connection entities</span><span class="sxs-lookup"><span data-stu-id="e2849-103">Connection entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e2849-104">The *connections* provide a flexible way to connect and describe the relationships between any two entity records [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="e2849-104">The *connections* provide a flexible way to connect and describe the relationships between any two entity records [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span> <span data-ttu-id="e2849-105">It helps you to promote teamwork, collaboration, and effective management of business and sales processes.</span><span class="sxs-lookup"><span data-stu-id="e2849-105">It helps you to promote teamwork, collaboration, and effective management of business and sales processes.</span></span> <span data-ttu-id="e2849-106">Kết nối cho phép bạn dễ dàng liên kết người dùng, liên hệ, báo giá, đơn hàng và nhiều hồ sơ thực thể khác với nhau.</span><span class="sxs-lookup"><span data-stu-id="e2849-106">Connections enable you to easily associate users, contacts, quotes, sales orders, and many other entity records with each other.</span></span> <span data-ttu-id="e2849-107">The records in the association can be assigned particular roles that help define the purpose of the relationship.</span><span class="sxs-lookup"><span data-stu-id="e2849-107">The records in the association can be assigned particular roles that help define the purpose of the relationship.</span></span>  
  
 <span data-ttu-id="e2849-108">Connections provide the following capabilities:</span><span class="sxs-lookup"><span data-stu-id="e2849-108">Connections provide the following capabilities:</span></span>  
  
- <span data-ttu-id="e2849-109">An easy and flexible way to make a connection between two records of most [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps entity types.</span><span class="sxs-lookup"><span data-stu-id="e2849-109">An easy and flexible way to make a connection between two records of most [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps entity types.</span></span> <span data-ttu-id="e2849-110">All customizable business and custom entities can be enabled for connections.</span><span class="sxs-lookup"><span data-stu-id="e2849-110">All customizable business and custom entities can be enabled for connections.</span></span>  
  
- <span data-ttu-id="e2849-111">An option to add useful information, such as a description of the connection and the duration.</span><span class="sxs-lookup"><span data-stu-id="e2849-111">An option to add useful information, such as a description of the connection and the duration.</span></span>  
  
- <span data-ttu-id="e2849-112">The ability to create connection roles that describe the relationship between two records, such as a relationship between a doctor and a patient, or a manager and an employee.</span><span class="sxs-lookup"><span data-stu-id="e2849-112">The ability to create connection roles that describe the relationship between two records, such as a relationship between a doctor and a patient, or a manager and an employee.</span></span>  
  
- <span data-ttu-id="e2849-113">A quick way to create multiple connections and roles for a particular record.</span><span class="sxs-lookup"><span data-stu-id="e2849-113">A quick way to create multiple connections and roles for a particular record.</span></span> <span data-ttu-id="e2849-114">For example, a contact may have many relationships with other contacts, accounts, or contracts.</span><span class="sxs-lookup"><span data-stu-id="e2849-114">For example, a contact may have many relationships with other contacts, accounts, or contracts.</span></span> <span data-ttu-id="e2849-115">In each relationship a contact may play a different role.</span><span class="sxs-lookup"><span data-stu-id="e2849-115">In each relationship a contact may play a different role.</span></span>  
  
- <span data-ttu-id="e2849-116">Information for building queries and creating graphs.</span><span class="sxs-lookup"><span data-stu-id="e2849-116">Information for building queries and creating graphs.</span></span> <span data-ttu-id="e2849-117">You can search for all connections and connection roles for a particular record and create graphs and charts for visual representation of the connections.</span><span class="sxs-lookup"><span data-stu-id="e2849-117">You can search for all connections and connection roles for a particular record and create graphs and charts for visual representation of the connections.</span></span>  
  
- <span data-ttu-id="e2849-118">Support for workflows and auditing for automating and improving business processes.</span><span class="sxs-lookup"><span data-stu-id="e2849-118">Support for workflows and auditing for automating and improving business processes.</span></span>  
  
## <a name="enabling-and-creating-connections"></a><span data-ttu-id="e2849-119">Enabling and creating connections</span><span class="sxs-lookup"><span data-stu-id="e2849-119">Enabling and creating connections</span></span>  
 <span data-ttu-id="e2849-120">You can enable any custom or customizable entity for connection by updating the entity metadata.</span><span class="sxs-lookup"><span data-stu-id="e2849-120">You can enable any custom or customizable entity for connection by updating the entity metadata.</span></span> <span data-ttu-id="e2849-121">Use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest> message to set the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsConnectionsEnabled> property to `true`.</span><span class="sxs-lookup"><span data-stu-id="e2849-121">Use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest> message to set the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsConnectionsEnabled> property to `true`.</span></span>  
  
 <span data-ttu-id="e2849-122">To create a connection between two records, use the `Connection` entity.</span><span class="sxs-lookup"><span data-stu-id="e2849-122">To create a connection between two records, use the `Connection` entity.</span></span> <span data-ttu-id="e2849-123">You must specify a record from which you create a connection (source) and a record to which you connect (target).</span><span class="sxs-lookup"><span data-stu-id="e2849-123">You must specify a record from which you create a connection (source) and a record to which you connect (target).</span></span> <span data-ttu-id="e2849-124">Use the `Connection.Record1Id` attribute to specify the source entity record and the `Connection.Record2Id` attribute to specify the target entity record.</span><span class="sxs-lookup"><span data-stu-id="e2849-124">Use the `Connection.Record1Id` attribute to specify the source entity record and the `Connection.Record2Id` attribute to specify the target entity record.</span></span> <span data-ttu-id="e2849-125">Optionally, you can specify the duration of the connection and the description.</span><span class="sxs-lookup"><span data-stu-id="e2849-125">Optionally, you can specify the duration of the connection and the description.</span></span> <span data-ttu-id="e2849-126">To describe the relationship between the participants in the connection, use the connection roles.</span><span class="sxs-lookup"><span data-stu-id="e2849-126">To describe the relationship between the participants in the connection, use the connection roles.</span></span> <span data-ttu-id="e2849-127">To specify the connection roles, use the `Connection.Record1RoleId` attribute and the `Connection.Record2RoleId` attribute.</span><span class="sxs-lookup"><span data-stu-id="e2849-127">To specify the connection roles, use the `Connection.Record1RoleId` attribute and the `Connection.Record2RoleId` attribute.</span></span>  
  
## <a name="querying-connections"></a><span data-ttu-id="e2849-128">Querying connections</span><span class="sxs-lookup"><span data-stu-id="e2849-128">Querying connections</span></span>  
 <span data-ttu-id="e2849-129">Querying connections gives you valuable data that you can use to create reports, graphs, or charts.</span><span class="sxs-lookup"><span data-stu-id="e2849-129">Querying connections gives you valuable data that you can use to create reports, graphs, or charts.</span></span> <span data-ttu-id="e2849-130">You can query connections by an entity record, by an entity type (Entity Type Code), by a particular role, or other criteria.</span><span class="sxs-lookup"><span data-stu-id="e2849-130">You can query connections by an entity record, by an entity type (Entity Type Code), by a particular role, or other criteria.</span></span> <span data-ttu-id="e2849-131">The following are examples of how you can query connections:</span><span class="sxs-lookup"><span data-stu-id="e2849-131">The following are examples of how you can query connections:</span></span>  
  
 <span data-ttu-id="e2849-132">By an entity record:</span><span class="sxs-lookup"><span data-stu-id="e2849-132">By an entity record:</span></span>  
  
- <span data-ttu-id="e2849-133">Show all connections for account A.</span><span class="sxs-lookup"><span data-stu-id="e2849-133">Show all connections for account A.</span></span>  
  
- <span data-ttu-id="e2849-134">Show all roles for account A.</span><span class="sxs-lookup"><span data-stu-id="e2849-134">Show all roles for account A.</span></span>  
  
  <span data-ttu-id="e2849-135">By an entity type (using Entity Type Codes):</span><span class="sxs-lookup"><span data-stu-id="e2849-135">By an entity type (using Entity Type Codes):</span></span>  
  
- <span data-ttu-id="e2849-136">Show all roles for the competitor entity.</span><span class="sxs-lookup"><span data-stu-id="e2849-136">Show all roles for the competitor entity.</span></span>  
  
- <span data-ttu-id="e2849-137">Find the total number of roles for the account entity.</span><span class="sxs-lookup"><span data-stu-id="e2849-137">Find the total number of roles for the account entity.</span></span>  
  
  <span data-ttu-id="e2849-138">By a role:</span><span class="sxs-lookup"><span data-stu-id="e2849-138">By a role:</span></span>  
  
- <span data-ttu-id="e2849-139">Find all connections where account A is a “Vendor”.</span><span class="sxs-lookup"><span data-stu-id="e2849-139">Find all connections where account A is a “Vendor”.</span></span>  
  
- <span data-ttu-id="e2849-140">Find all open opportunities over $20,000, where contact B is a “Salesperson”.</span><span class="sxs-lookup"><span data-stu-id="e2849-140">Find all open opportunities over $20,000, where contact B is a “Salesperson”.</span></span>  
  
- <span data-ttu-id="e2849-141">Find all matching roles for a “Doctor” role, such as “Patient”, “Nurse”, or “Medical Assistant”.</span><span class="sxs-lookup"><span data-stu-id="e2849-141">Find all matching roles for a “Doctor” role, such as “Patient”, “Nurse”, or “Medical Assistant”.</span></span>  
  
- <span data-ttu-id="e2849-142">Find all contacts that have the role “Friend”.</span><span class="sxs-lookup"><span data-stu-id="e2849-142">Find all contacts that have the role “Friend”.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="e2849-143">When you create a connection entity record, two records are created in the database.</span><span class="sxs-lookup"><span data-stu-id="e2849-143">When you create a connection entity record, two records are created in the database.</span></span> <span data-ttu-id="e2849-144">The first record represents a source to target connection and the second record represents a target to source connection.</span><span class="sxs-lookup"><span data-stu-id="e2849-144">The first record represents a source to target connection and the second record represents a target to source connection.</span></span> <span data-ttu-id="e2849-145">This guarantees that a query will find all connections that the record participates in, regardless whether the record is a source record or a target record in the connection.</span><span class="sxs-lookup"><span data-stu-id="e2849-145">This guarantees that a query will find all connections that the record participates in, regardless whether the record is a source record or a target record in the connection.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e2849-146">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e2849-146">See also</span></span>  
 <span data-ttu-id="e2849-147">[Describe a Relationship Between Entities with Connection Roles](describe-relationship-entities-connection-roles.md) </span><span class="sxs-lookup"><span data-stu-id="e2849-147">[Describe a Relationship Between Entities with Connection Roles](describe-relationship-entities-connection-roles.md) </span></span>  
 <span data-ttu-id="e2849-148">[Connection Entity](entities/connection.md) </span><span class="sxs-lookup"><span data-stu-id="e2849-148">[Connection Entity](entities/connection.md) </span></span>  
 <span data-ttu-id="e2849-149">[ConnectionRole Entity](entities/connectionrole.md) </span><span class="sxs-lookup"><span data-stu-id="e2849-149">[ConnectionRole Entity](entities/connectionrole.md) </span></span>  
 <span data-ttu-id="e2849-150">[Sample Code for Connection Entities](sample-code-connection-entities.md) </span><span class="sxs-lookup"><span data-stu-id="e2849-150">[Sample Code for Connection Entities](sample-code-connection-entities.md) </span></span>  
 <span data-ttu-id="e2849-151">[Business Management Entities](business-management-entities.md) </span><span class="sxs-lookup"><span data-stu-id="e2849-151">[Business Management Entities](business-management-entities.md) </span></span>  
 <span data-ttu-id="e2849-152">[View and Analyze Data with Visualizations and Dashboards in Dynamics 365 for Customer Engagement apps](customize-dev/customize-visualizations-dashboards.md) </span><span class="sxs-lookup"><span data-stu-id="e2849-152">[View and Analyze Data with Visualizations and Dashboards in Dynamics 365 for Customer Engagement apps](customize-dev/customize-visualizations-dashboards.md) </span></span>  
 [<span data-ttu-id="e2849-153">Fiscal Calendar and Territory Entities</span><span class="sxs-lookup"><span data-stu-id="e2849-153">Fiscal Calendar and Territory Entities</span></span>](fiscal-calendar-and-territory-entities.md)
