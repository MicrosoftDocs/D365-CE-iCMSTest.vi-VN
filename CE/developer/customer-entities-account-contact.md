---
title: Customer entities (account, contact) (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: The account and contact entities in Dynamics 365 for Customer Engagement apps are essential for identifying and managing customers, selling products and services, and providing superior service to the customers. A customer address entity is used to store address and shipping information for a customer.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d126ea83-97c4-4460-a971-15e21073d6d6
caps.latest.revision: 29
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f31f2f87e41d247d9341fb555d88c0c8aa1fd571
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386066"
---
# <a name="customer-entities-account-contact"></a><span data-ttu-id="37e40-104">Customer entities (account, contact)</span><span class="sxs-lookup"><span data-stu-id="37e40-104">Customer entities (account, contact)</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="37e40-105">The *account* and *contact* entities in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps are essential for identifying and managing customers, selling products and services, and providing superior service to the customers.</span><span class="sxs-lookup"><span data-stu-id="37e40-105">The *account* and *contact* entities in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps are essential for identifying and managing customers, selling products and services, and providing superior service to the customers.</span></span> <span data-ttu-id="37e40-106">A *customer address* entity is used to store address and shipping information for a customer.</span><span class="sxs-lookup"><span data-stu-id="37e40-106">A *customer address* entity is used to store address and shipping information for a customer.</span></span>  
  
 <span data-ttu-id="37e40-107">The account entity is one of the entities in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps to which most other entities are attached or parented.</span><span class="sxs-lookup"><span data-stu-id="37e40-107">The account entity is one of the entities in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps to which most other entities are attached or parented.</span></span> <span data-ttu-id="37e40-108">In [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, an account represents a company with which the business unit has a relationship.</span><span class="sxs-lookup"><span data-stu-id="37e40-108">In [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, an account represents a company with which the business unit has a relationship.</span></span> <span data-ttu-id="37e40-109">Information that is included in an account is all relevant contact information, company information, category, relationship type, and address information.</span><span class="sxs-lookup"><span data-stu-id="37e40-109">Information that is included in an account is all relevant contact information, company information, category, relationship type, and address information.</span></span> <span data-ttu-id="37e40-110">Other information that applies includes the following items:</span><span class="sxs-lookup"><span data-stu-id="37e40-110">Other information that applies includes the following items:</span></span>  
  
- <span data-ttu-id="37e40-111">An account can be a parent to almost any other entity.</span><span class="sxs-lookup"><span data-stu-id="37e40-111">An account can be a parent to almost any other entity.</span></span> <span data-ttu-id="37e40-112">This includes another account.</span><span class="sxs-lookup"><span data-stu-id="37e40-112">This includes another account.</span></span>  
  
- <span data-ttu-id="37e40-113">An account can be a standalone entity.</span><span class="sxs-lookup"><span data-stu-id="37e40-113">An account can be a standalone entity.</span></span>  
  
- <span data-ttu-id="37e40-114">An account can have only one account as its parent.</span><span class="sxs-lookup"><span data-stu-id="37e40-114">An account can have only one account as its parent.</span></span>  
  
- <span data-ttu-id="37e40-115">Accounts can have multiple child accounts and child contacts.</span><span class="sxs-lookup"><span data-stu-id="37e40-115">Accounts can have multiple child accounts and child contacts.</span></span>  
  
  <span data-ttu-id="37e40-116">Account management is one of the important concepts of business-to-business customer relationship management (Dynamics 365 for Customer Engagement apps) because an organization wants to see all the activities they have with another company All these activities come together at the account level.</span><span class="sxs-lookup"><span data-stu-id="37e40-116">Account management is one of the important concepts of business-to-business customer relationship management (Dynamics 365 for Customer Engagement apps) because an organization wants to see all the activities they have with another company All these activities come together at the account level.</span></span>  
  
  <span data-ttu-id="37e40-117">In [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, a contact represents a person, usually an individual, with whom a business unit has a relationship, such as a customer, a supplier, or a colleague.</span><span class="sxs-lookup"><span data-stu-id="37e40-117">In [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, a contact represents a person, usually an individual, with whom a business unit has a relationship, such as a customer, a supplier, or a colleague.</span></span> <span data-ttu-id="37e40-118">The contact entity is one of the entities that most other entities are linked to.</span><span class="sxs-lookup"><span data-stu-id="37e40-118">The contact entity is one of the entities that most other entities are linked to.</span></span> <span data-ttu-id="37e40-119">A contact can be a stand-alone entity.</span><span class="sxs-lookup"><span data-stu-id="37e40-119">A contact can be a stand-alone entity.</span></span> <span data-ttu-id="37e40-120">Included in this entity are professional, personal, and family information, and multiple addresses.</span><span class="sxs-lookup"><span data-stu-id="37e40-120">Included in this entity are professional, personal, and family information, and multiple addresses.</span></span>  
  
  <span data-ttu-id="37e40-121">Both accounts and contacts are part of managing customers and are related to one another in the following ways:</span><span class="sxs-lookup"><span data-stu-id="37e40-121">Both accounts and contacts are part of managing customers and are related to one another in the following ways:</span></span>  
  
- <span data-ttu-id="37e40-122">A contact can be a parent to every other entity except accounts and contacts.</span><span class="sxs-lookup"><span data-stu-id="37e40-122">A contact can be a parent to every other entity except accounts and contacts.</span></span>  
  
- <span data-ttu-id="37e40-123">A contact can have only one account as its parent.</span><span class="sxs-lookup"><span data-stu-id="37e40-123">A contact can have only one account as its parent.</span></span>  
  
- <span data-ttu-id="37e40-124">A contact can be marked as the primary contact person for an account by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*> method.</span><span class="sxs-lookup"><span data-stu-id="37e40-124">A contact can be marked as the primary contact person for an account by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*> method.</span></span>  
  
  <span data-ttu-id="37e40-125">The contact entity stores all information about a person such as an email address, street address, telephone numbers, and other related information, such as the birthday or anniversary date.</span><span class="sxs-lookup"><span data-stu-id="37e40-125">The contact entity stores all information about a person such as an email address, street address, telephone numbers, and other related information, such as the birthday or anniversary date.</span></span> <span data-ttu-id="37e40-126">Depending on the type of customers a business unit has, it needs either only contacts, or contacts and accounts, to give a full view of its customers.</span><span class="sxs-lookup"><span data-stu-id="37e40-126">Depending on the type of customers a business unit has, it needs either only contacts, or contacts and accounts, to give a full view of its customers.</span></span>  
  
  <span data-ttu-id="37e40-127">The basic operations that you can perform on a contact include Create, Read, Update, and Delete.</span><span class="sxs-lookup"><span data-stu-id="37e40-127">The basic operations that you can perform on a contact include Create, Read, Update, and Delete.</span></span>  
  
  <span data-ttu-id="37e40-128">Linking entities such as activities and notes to the contact entity lets user see all the communication the user has had with a customer, any actions the user has taken on behalf of the customer, and all information the user needs about the customer.</span><span class="sxs-lookup"><span data-stu-id="37e40-128">Linking entities such as activities and notes to the contact entity lets user see all the communication the user has had with a customer, any actions the user has taken on behalf of the customer, and all information the user needs about the customer.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="37e40-129">In This Section</span><span class="sxs-lookup"><span data-stu-id="37e40-129">In This Section</span></span>  
 [<span data-ttu-id="37e40-130">Account Entity</span><span class="sxs-lookup"><span data-stu-id="37e40-130">Account Entity</span></span>](entities/account.md)  
  
 [<span data-ttu-id="37e40-131">Contact Entity</span><span class="sxs-lookup"><span data-stu-id="37e40-131">Contact Entity</span></span>](entities/contact.md)  
  
 [<span data-ttu-id="37e40-132">CustomerAddress Entity</span><span class="sxs-lookup"><span data-stu-id="37e40-132">CustomerAddress Entity</span></span>](entities/customeraddress.md)  
  
## <a name="related-sections"></a><span data-ttu-id="37e40-133">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="37e40-133">Related Sections</span></span>  
 [<span data-ttu-id="37e40-134">Model Your Business Data With Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="37e40-134">Model Your Business Data With Dynamics 365 for Customer Engagement apps</span></span>](model-business-data.md)  
  
 [<span data-ttu-id="37e40-135">Business Management Entities</span><span class="sxs-lookup"><span data-stu-id="37e40-135">Business Management Entities</span></span>](business-management-entities.md)
