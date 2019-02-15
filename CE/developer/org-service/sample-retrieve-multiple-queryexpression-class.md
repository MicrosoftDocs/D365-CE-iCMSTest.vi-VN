---
title: 'Sample: Retrieve multiple with the QueryExpression class (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to retrieve multiple entities using the QueryBase) method with QueryExpression along with their related entity columns. The code returns columns from the primary account record as well as the firstname and lastname of the primary contacts associated with the account
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 2bdd259c-1003-4b37-a7db-61bf2278c7e4
caps.latest.revision: 20
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2626d5876745b5b90f3d0f669863310af67d7b15
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386738"
---
# <a name="sample-retrieve-multiple-with-the-queryexpression-class"></a><span data-ttu-id="7e342-104">Sample: Retrieve multiple with the QueryExpression class</span><span class="sxs-lookup"><span data-stu-id="7e342-104">Sample: Retrieve multiple with the QueryExpression class</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

## <a name="prerequisites"></a><span data-ttu-id="7e342-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="7e342-105">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="example"></a><span data-ttu-id="7e342-106">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="7e342-106">Example</span></span>  
 <span data-ttu-id="7e342-107">This sample shows how to retrieve multiple entities using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple(Microsoft.Xrm.Sdk.Query.QueryBase)></span><span class="sxs-lookup"><span data-stu-id="7e342-107">This sample shows how to retrieve multiple entities using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple(Microsoft.Xrm.Sdk.Query.QueryBase)></span></span> <span data-ttu-id="7e342-108">method with <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> along with their related entity columns.</span><span class="sxs-lookup"><span data-stu-id="7e342-108">method with <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> along with their related entity columns.</span></span> <span data-ttu-id="7e342-109">The code returns columns from the primary account record as well as the firstname and lastname of the primary contacts associated with the account.</span><span class="sxs-lookup"><span data-stu-id="7e342-109">The code returns columns from the primary account record as well as the firstname and lastname of the primary contacts associated with the account.</span></span>  
 
<span data-ttu-id="7e342-110">To access aliased values, use the <xref:Microsoft.Xrm.Sdk.Entity>.<xref:Microsoft.Xrm.Sdk.Entity.GetAttributeValue``1(System.String)></span><span class="sxs-lookup"><span data-stu-id="7e342-110">To access aliased values, use the <xref:Microsoft.Xrm.Sdk.Entity>.<xref:Microsoft.Xrm.Sdk.Entity.GetAttributeValue``1(System.String)></span></span> <span data-ttu-id="7e342-111">to get the <xref:Microsoft.Xrm.Sdk.AliasedValue>.<xref:Microsoft.Xrm.Sdk.AliasedValue.Value>.</span><span class="sxs-lookup"><span data-stu-id="7e342-111">to get the <xref:Microsoft.Xrm.Sdk.AliasedValue>.<xref:Microsoft.Xrm.Sdk.AliasedValue.Value>.</span></span>
  
```csharp  
static void RetrieveMultipleWithRelatedEntityColumns(IOrganizationService service)
{
    Console.WriteLine("Entering:RetrieveMultipleWithRelatedEntityColumns");
    //Create multiple accounts with primary contacts  
    Entity contact = new Entity("contact");
    contact.Attributes["firstname"] = "ContactFirstName";
    contact.Attributes["lastname"] = "ContactLastName";
    Guid contactId = service.Create(contact);

    Entity account = new Entity("account");
    account["name"] = "Test Account1";
    EntityReference primaryContactId = new EntityReference("contact", contactId);
    account["primarycontactid"] = primaryContactId;

    Guid accountId1 = service.Create(account);
    account["name"] = "Test Account2";
    Guid accountId2 = service.Create(account);
    account["name"] = "Test Account3";
    Guid accountId3 = service.Create(account);

    //Create a query expression specifying the link entity alias and the columns of the link entity that you want to return  
    QueryExpression qe = new QueryExpression();
    qe.EntityName = "account";
    qe.ColumnSet = new ColumnSet();
    qe.ColumnSet.Columns.Add("name");

    qe.LinkEntities.Add(new LinkEntity("account", "contact", "primarycontactid", "contactid", JoinOperator.Inner));
    qe.LinkEntities[0].Columns.AddColumns("firstname", "lastname");
    qe.LinkEntities[0].EntityAlias = "primarycontact";

    EntityCollection ec = service.RetrieveMultiple(qe);

    Console.WriteLine("Retrieved {0} entities", ec.Entities.Count);
    foreach (Entity act in ec.Entities)
    {
        Console.WriteLine("account name: {0}", act["name"]);
        Console.WriteLine("primary contact first name: {0}", act.GetAttributeValue<AliasedValue>("primarycontact.firstname").Value);
        Console.WriteLine("primary contact first name: {0}", act.GetAttributeValue<AliasedValue>("primarycontact.lastname").Value);
    }
} 
```  
<span data-ttu-id="7e342-112">The code will output the following:</span><span class="sxs-lookup"><span data-stu-id="7e342-112">The code will output the following:</span></span>
```ms-dos
Entering:RetrieveMultipleWithRelatedEntityColumns
Retrieved 3 entities
account name: Test Account1
primary contact first name: ContactFirstName
primary contact first name: ContactLastName
account name: Test Account2
primary contact first name: ContactFirstName
primary contact first name: ContactLastName
account name: Test Account3
primary contact first name: ContactFirstName
primary contact first name: ContactLastName
```
  
### <a name="see-also"></a><span data-ttu-id="7e342-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="7e342-113">See also</span></span>  
 <span data-ttu-id="7e342-114">[Use the QueryExpression Class](use-queryexpression-class.md) </span><span class="sxs-lookup"><span data-stu-id="7e342-114">[Use the QueryExpression Class](use-queryexpression-class.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple(Microsoft.Xrm.Sdk.Query.QueryBase)>   
 <xref:Microsoft.Xrm.Sdk.Query.QueryExpression>   
 <span data-ttu-id="7e342-115">[Build Queries with QueryExpression](build-queries-with-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="7e342-115">[Build Queries with QueryExpression](build-queries-with-queryexpression.md) </span></span>  
 <span data-ttu-id="7e342-116">[Sample: Convert queries between Fetch and QueryExpression](sample-convert-queries-fetch-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="7e342-116">[Sample: Convert queries between Fetch and QueryExpression](sample-convert-queries-fetch-queryexpression.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Query.QueryExpression>
