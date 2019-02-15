---
title: Query hierarchical data (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Dynamics 365 for Customer Engagement (online) Customer Engagement introduces the capability to define specific self-referencing one-to-many entity relationships as hierarchical. Read how you can build queries that return data in these hierarchies
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: ed3d7166-8865-433d-b889-b0fadba25d64
caps.latest.revision: 20
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 44aaf40830e2c51ba1e2243031402fb446cbc53e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386982"
---
# <a name="query-hierarchical-data"></a><span data-ttu-id="47b7e-104">Query hierarchical data</span><span class="sxs-lookup"><span data-stu-id="47b7e-104">Query hierarchical data</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] <span data-ttu-id="47b7e-105">Customer Engagement introduces the capability to define specific self-referencing one-to-many entity relationships as hierarchical.</span><span class="sxs-lookup"><span data-stu-id="47b7e-105">Customer Engagement introduces the capability to define specific self-referencing one-to-many entity relationships as hierarchical.</span></span> <span data-ttu-id="47b7e-106">You can write queries that return related data in these hierarchies.</span><span class="sxs-lookup"><span data-stu-id="47b7e-106">You can write queries that return related data in these hierarchies.</span></span>  
  
 <span data-ttu-id="47b7e-107">You can take advantage of new query condition operators to query entities with explicit hierarchical relationships.</span><span class="sxs-lookup"><span data-stu-id="47b7e-107">You can take advantage of new query condition operators to query entities with explicit hierarchical relationships.</span></span> <span data-ttu-id="47b7e-108">These operators only apply for the entity relationship specifically defined as a hierarchical relationship.</span><span class="sxs-lookup"><span data-stu-id="47b7e-108">These operators only apply for the entity relationship specifically defined as a hierarchical relationship.</span></span> <span data-ttu-id="47b7e-109">You can use new condition operators to retrieve this hierarchical data when you query using <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> or <xref:Microsoft.Xrm.Sdk.Query.FetchExpression>.</span><span class="sxs-lookup"><span data-stu-id="47b7e-109">You can use new condition operators to retrieve this hierarchical data when you query using <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> or <xref:Microsoft.Xrm.Sdk.Query.FetchExpression>.</span></span>  
  
<a name="BKMK_ConditionOperators"></a>   
## <a name="condition-operators-for-hierarchical-data"></a><span data-ttu-id="47b7e-110">Condition operators for hierarchical data</span><span class="sxs-lookup"><span data-stu-id="47b7e-110">Condition operators for hierarchical data</span></span>  
 <span data-ttu-id="47b7e-111">Use the following operators to set conditions when querying hierarchical data.</span><span class="sxs-lookup"><span data-stu-id="47b7e-111">Use the following operators to set conditions when querying hierarchical data.</span></span>  
  
|<span data-ttu-id="47b7e-112">XML tìm nạp dữ liệu</span><span class="sxs-lookup"><span data-stu-id="47b7e-112">FetchXML</span></span>|<span data-ttu-id="47b7e-113">ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="47b7e-113">ConditionOperator</span></span>|<span data-ttu-id="47b7e-114">Mô tả</span><span class="sxs-lookup"><span data-stu-id="47b7e-114">Description</span></span>|  
|--------------|-----------------------|-----------------|  
|`above`|`Above`|<span data-ttu-id="47b7e-115">Returns all records in referenced record's hierarchical ancestry line.</span><span class="sxs-lookup"><span data-stu-id="47b7e-115">Returns all records in referenced record's hierarchical ancestry line.</span></span>|  
|`eq-or-above`|`AboveOrEqual`|<span data-ttu-id="47b7e-116">Returns the referenced record and all records above it in the hierarchy.</span><span class="sxs-lookup"><span data-stu-id="47b7e-116">Returns the referenced record and all records above it in the hierarchy.</span></span>|  
|`under`|`Under`|<span data-ttu-id="47b7e-117">Returns all child records below the referenced record in the hierarchy</span><span class="sxs-lookup"><span data-stu-id="47b7e-117">Returns all child records below the referenced record in the hierarchy</span></span>|  
|`eq-or-under`|`UnderOrEqual`|<span data-ttu-id="47b7e-118">Returns the referenced record and all child records below it in the hierarchy</span><span class="sxs-lookup"><span data-stu-id="47b7e-118">Returns the referenced record and all child records below it in the hierarchy</span></span>|  
|`not-under`|`NotUnder`|<span data-ttu-id="47b7e-119">Returns all records not below the referenced record in the hierarchy</span><span class="sxs-lookup"><span data-stu-id="47b7e-119">Returns all records not below the referenced record in the hierarchy</span></span>|  
|`eq-owneduseroruserhierarchy`|`OwnedByMeOrMyReports`|<span data-ttu-id="47b7e-120">When hierarchical security models are used, Equals current user or his reporting hierarchy</span><span class="sxs-lookup"><span data-stu-id="47b7e-120">When hierarchical security models are used, Equals current user or his reporting hierarchy</span></span>|  
|`eq-useroruserhierarchyandteams`|`OwnedByMeOrMyReportsAndTeams`|<span data-ttu-id="47b7e-121">When hierarchical security models are used, Equals current user and his teams or his reporting hierarchy and their teams</span><span class="sxs-lookup"><span data-stu-id="47b7e-121">When hierarchical security models are used, Equals current user and his teams or his reporting hierarchy and their teams</span></span>|  
  
### <a name="recursion-limits-when-querying-hierarchical-data"></a><span data-ttu-id="47b7e-122">Recursion limits when querying hierarchical data</span><span class="sxs-lookup"><span data-stu-id="47b7e-122">Recursion limits when querying hierarchical data</span></span>  
 <span data-ttu-id="47b7e-123">Because querying hierarchical data can be resource intensive, there is a default limit of 100 recursions allowed conditions for hierarchical queries using the `Above`, `AboveOrEqual`, `Under`, `UnderOrEqual`, and `NotUnder` condition operators.</span><span class="sxs-lookup"><span data-stu-id="47b7e-123">Because querying hierarchical data can be resource intensive, there is a default limit of 100 recursions allowed conditions for hierarchical queries using the `Above`, `AboveOrEqual`, `Under`, `UnderOrEqual`, and `NotUnder` condition operators.</span></span>  
  
 <span data-ttu-id="47b7e-124">These limits can be adjusted using [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] commands through the deployment web service.</span><span class="sxs-lookup"><span data-stu-id="47b7e-124">These limits can be adjusted using [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] commands through the deployment web service.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="47b7e-125">[Administer the deployment using Windows PowerShell](https://technet.microsoft.com/library/dn531202.aspx).</span><span class="sxs-lookup"><span data-stu-id="47b7e-125">[Administer the deployment using Windows PowerShell](https://technet.microsoft.com/library/dn531202.aspx).</span></span>  
  
 <span data-ttu-id="47b7e-126">`OwnedByMeOrMyReports` and `OwnedByMeOrMyReportsAndTeams` are hierarchical security condition operators that depend on the **Hierarchy Depth** setting that can be found in **Settings** > **Security** > **Hierarchy Security**.</span><span class="sxs-lookup"><span data-stu-id="47b7e-126">`OwnedByMeOrMyReports` and `OwnedByMeOrMyReportsAndTeams` are hierarchical security condition operators that depend on the **Hierarchy Depth** setting that can be found in **Settings** > **Security** > **Hierarchy Security**.</span></span> <span data-ttu-id="47b7e-127">The value of this setting is stored in the `Organization.MaxDepthForHierarchicalSecurityModel` attribute.</span><span class="sxs-lookup"><span data-stu-id="47b7e-127">The value of this setting is stored in the `Organization.MaxDepthForHierarchicalSecurityModel` attribute.</span></span>  
  
<a name="BKMK_ChildCountAggregate"></a>   
## <a name="retrieve-the-number-of-hierarchically-related-child-records"></a><span data-ttu-id="47b7e-128">Retrieve the number of hierarchically related child records</span><span class="sxs-lookup"><span data-stu-id="47b7e-128">Retrieve the number of hierarchically related child records</span></span>  
 <span data-ttu-id="47b7e-129">Use the `rowaggregate` attribute in a FetchXML based query to retrieve the number of hierarchically related child records.</span><span class="sxs-lookup"><span data-stu-id="47b7e-129">Use the `rowaggregate` attribute in a FetchXML based query to retrieve the number of hierarchically related child records.</span></span> <span data-ttu-id="47b7e-130">When this value is set to `CountChildren` a value that includes the total number of child records for the record is included in the <xref:Microsoft.Xrm.Sdk.EntityCollection>.</span><span class="sxs-lookup"><span data-stu-id="47b7e-130">When this value is set to `CountChildren` a value that includes the total number of child records for the record is included in the <xref:Microsoft.Xrm.Sdk.EntityCollection>.</span></span> <span data-ttu-id="47b7e-131">For example, the following query will include an `AccountChildren` aggregate value representing the number of child account records in the hierarchical relationship where the `{0}` parameter represents the `AccountId` of the parent record.</span><span class="sxs-lookup"><span data-stu-id="47b7e-131">For example, the following query will include an `AccountChildren` aggregate value representing the number of child account records in the hierarchical relationship where the `{0}` parameter represents the `AccountId` of the parent record.</span></span>  
  
```xml  
<fetch distinct='false' no-lock='false' mapping='logical'>  
  <entity name='account'>  
    <attribute name='name' />  
    <attribute name='accountid' />  
    <attribute name='accountid' rowaggregate='CountChildren' alias='AccountChildren'/>  
    <filter type='and'>  
      <condition attribute='accountid' operator='under' value='{0}' />  
    </filter>  
  </entity>  
</fetch>  
  
```  
  
> [!NOTE]
>  <span data-ttu-id="47b7e-132">The aggregate value returned represents all the child records, including any that the user may not have access to read.</span><span class="sxs-lookup"><span data-stu-id="47b7e-132">The aggregate value returned represents all the child records, including any that the user may not have access to read.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="47b7e-133">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="47b7e-133">See also</span></span>  
 <span data-ttu-id="47b7e-134">[Customize entity relationship metadata](../customize-entity-relationship-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="47b7e-134">[Customize entity relationship metadata](../customize-entity-relationship-metadata.md) </span></span>  
 <span data-ttu-id="47b7e-135">[Build Queries with FetchXML](build-queries-fetchxml.md) </span><span class="sxs-lookup"><span data-stu-id="47b7e-135">[Build Queries with FetchXML](build-queries-fetchxml.md) </span></span>  
 <span data-ttu-id="47b7e-136">[Build Queries with QueryExpression](build-queries-with-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="47b7e-136">[Build Queries with QueryExpression](build-queries-with-queryexpression.md) </span></span>  
 <span data-ttu-id="47b7e-137">[FetchXML Schema](fetchxml-schema.md) </span><span class="sxs-lookup"><span data-stu-id="47b7e-137">[FetchXML Schema](fetchxml-schema.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Query.ConditionOperator>   
 [<span data-ttu-id="47b7e-138">Video: Hierarchy Visualization in Microsoft Dynamics CRM 2015</span><span class="sxs-lookup"><span data-stu-id="47b7e-138">Video: Hierarchy Visualization in Microsoft Dynamics CRM 2015</span></span>](http://youtu.be/_dGBE6icLNw)
