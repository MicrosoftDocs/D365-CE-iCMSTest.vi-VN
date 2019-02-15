---
title: Build queries with FetchXML (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: FetchXML is a proprietary query language that is used in Dynamics 365 for Customer Engagement (online) Customer Engagement. A FetchXML query can be executed by using the IOrganizationService.QueryBase) method. FetchXML query can be converted to a query expression with the FetchXmlToQueryExpressionRequest message
ms.custom: ''
ms.date: 12/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 8ff32261-4a9a-4186-bf2f-ee28496b16ef
caps.latest.revision: 47
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 470da07f682ab19da7798d2b0e641ff040ab1378
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388540"
---
# <a name="build-queries-with-fetchxml"></a><span data-ttu-id="05e61-105">Build queries with FetchXML</span><span class="sxs-lookup"><span data-stu-id="05e61-105">Build queries with FetchXML</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="05e61-106">FetchXML is a proprietary query language that is used in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="05e61-106">FetchXML is a proprietary query language that is used in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="05e61-107">It’s based on a schema that describes the capabilities of the language.</span><span class="sxs-lookup"><span data-stu-id="05e61-107">It’s based on a schema that describes the capabilities of the language.</span></span> <span data-ttu-id="05e61-108">The FetchXML language supports similar query capabilities as query expressions.</span><span class="sxs-lookup"><span data-stu-id="05e61-108">The FetchXML language supports similar query capabilities as query expressions.</span></span> <span data-ttu-id="05e61-109">In addition, it’s used as a serialized form of query, used to save a query as a user-owned saved view in the [UserQuery Entity](../entities/userquery.md) and as an organization-owned saved view in the [SavedQuery Entity](../entities/savedquery.md).</span><span class="sxs-lookup"><span data-stu-id="05e61-109">In addition, it’s used as a serialized form of query, used to save a query as a user-owned saved view in the [UserQuery Entity](../entities/userquery.md) and as an organization-owned saved view in the [SavedQuery Entity](../entities/savedquery.md).</span></span>  
  
## <a name="execute-queries-in-code"></a><span data-ttu-id="05e61-110">Execute queries in code</span><span class="sxs-lookup"><span data-stu-id="05e61-110">Execute queries in code</span></span>
<span data-ttu-id="05e61-111">A FetchXML query can be executed by using either the Web API or the Organization service.</span><span class="sxs-lookup"><span data-stu-id="05e61-111">A FetchXML query can be executed by using either the Web API or the Organization service.</span></span>

### <a name="web-api"></a><span data-ttu-id="05e61-112">API Web</span><span class="sxs-lookup"><span data-stu-id="05e61-112">Web API</span></span>
<span data-ttu-id="05e61-113">You can pass a URL encoded FetchXml string to the appropriate entityset using the `fetchXml` query string parameter.</span><span class="sxs-lookup"><span data-stu-id="05e61-113">You can pass a URL encoded FetchXml string to the appropriate entityset using the `fetchXml` query string parameter.</span></span> <span data-ttu-id="05e61-114">More information: [Use custom FetchXML](../webapi/retrieve-and-execute-predefined-queries.md#use-custom-fetchxml).</span><span class="sxs-lookup"><span data-stu-id="05e61-114">More information: [Use custom FetchXML](../webapi/retrieve-and-execute-predefined-queries.md#use-custom-fetchxml).</span></span>

### <a name="organization-service"></a><span data-ttu-id="05e61-115">Organization service</span><span class="sxs-lookup"><span data-stu-id="05e61-115">Organization service</span></span>
<span data-ttu-id="05e61-116">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span><span class="sxs-lookup"><span data-stu-id="05e61-116">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span></span> <span data-ttu-id="05e61-117">method passing an <xref:Microsoft.Xrm.Sdk.Query.FetchExpression> where the <xref:Microsoft.Xrm.Sdk.Query.FetchExpression.Query> property contains the FetchXml query.</span><span class="sxs-lookup"><span data-stu-id="05e61-117">method passing an <xref:Microsoft.Xrm.Sdk.Query.FetchExpression> where the <xref:Microsoft.Xrm.Sdk.Query.FetchExpression.Query> property contains the FetchXml query.</span></span>

<span data-ttu-id="05e61-118">You can convert a FetchXML query to a query expression with the <xref:Microsoft.Crm.Sdk.Messages.FetchXmlToQueryExpressionRequest> message.</span><span class="sxs-lookup"><span data-stu-id="05e61-118">You can convert a FetchXML query to a query expression with the <xref:Microsoft.Crm.Sdk.Messages.FetchXmlToQueryExpressionRequest> message.</span></span>  
  
## <a name="tools"></a><span data-ttu-id="05e61-119">Công cụ</span><span class="sxs-lookup"><span data-stu-id="05e61-119">Tools</span></span>

<span data-ttu-id="05e61-120">The [XrmToolBox FetchXML Builder](https://www.xrmtoolbox.com/plugins/Cinteros.Xrm.FetchXmlBuilder/) provides a user interface to compose and execute FetchXml queries.</span><span class="sxs-lookup"><span data-stu-id="05e61-120">The [XrmToolBox FetchXML Builder](https://www.xrmtoolbox.com/plugins/Cinteros.Xrm.FetchXmlBuilder/) provides a user interface to compose and execute FetchXml queries.</span></span>
> [!NOTE]
> <span data-ttu-id="05e61-121">The XrmToolBox FetchXML Builder is not a product of [!include[pn_microsoft_dynamics](../../includes/pn-microsoft-dynamics.md)] and does not extend support to it.</span><span class="sxs-lookup"><span data-stu-id="05e61-121">The XrmToolBox FetchXML Builder is not a product of [!include[pn_microsoft_dynamics](../../includes/pn-microsoft-dynamics.md)] and does not extend support to it.</span></span> <span data-ttu-id="05e61-122">If you have questions pertaining to the FetchXML Builder, please contact the [publisher](http://fxb.xrmtoolbox.com/).</span><span class="sxs-lookup"><span data-stu-id="05e61-122">If you have questions pertaining to the FetchXML Builder, please contact the [publisher](http://fxb.xrmtoolbox.com/).</span></span>

<span data-ttu-id="05e61-123">Advanced Find includes the capability to download the FetchXML for the query using the **Dowload Fetch XML** command.</span><span class="sxs-lookup"><span data-stu-id="05e61-123">Advanced Find includes the capability to download the FetchXML for the query using the **Dowload Fetch XML** command.</span></span> <span data-ttu-id="05e61-124">Thông tin khác: [Tạo, chỉnh sửa hoặc lưu Tìm kiếm Nâng cao](../../basics/save-advanced-find-search.md)</span><span class="sxs-lookup"><span data-stu-id="05e61-124">More information: [Create, edit, or save an Advanced Find search](../../basics/save-advanced-find-search.md)</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="05e61-125">In This Section</span><span class="sxs-lookup"><span data-stu-id="05e61-125">In This Section</span></span>

[<span data-ttu-id="05e61-126">Use FetchXML to Construct a Query</span><span class="sxs-lookup"><span data-stu-id="05e61-126">Use FetchXML to Construct a Query</span></span>](use-fetchxml-construct-query.md)<br />
[<span data-ttu-id="05e61-127">Use FetchXML Aggregation</span><span class="sxs-lookup"><span data-stu-id="05e61-127">Use FetchXML Aggregation</span></span>](use-fetchxml-aggregation.md)<br />
[<span data-ttu-id="05e61-128">Page Large Result Sets with FetchXML</span><span class="sxs-lookup"><span data-stu-id="05e61-128">Page Large Result Sets with FetchXML</span></span>](page-large-result-sets-with-fetchxml.md)<br />
[<span data-ttu-id="05e61-129">Fiscal Date Query Operators in FetchXML</span><span class="sxs-lookup"><span data-stu-id="05e61-129">Fiscal Date Query Operators in FetchXML</span></span>](fiscal-date-older-datetime-query-operators-fetchxml.md)<br />
[<span data-ttu-id="05e61-130">Use a left outer join in FetchXML to query for records not in</span><span class="sxs-lookup"><span data-stu-id="05e61-130">Use a left outer join in FetchXML to query for records not in</span></span>](use-left-outer-join-fetchxml-query-records-not-in.md)<br />
[<span data-ttu-id="05e61-131">Sample: Use Aggregation in FetchXML</span><span class="sxs-lookup"><span data-stu-id="05e61-131">Sample: Use Aggregation in FetchXML</span></span>](sample-use-aggregation-fetchxml.md)<br />
[<span data-ttu-id="05e61-132">Sample: Use FetchXML with a Paging Cookie</span><span class="sxs-lookup"><span data-stu-id="05e61-132">Sample: Use FetchXML with a Paging Cookie</span></span>](sample-use-fetchxml-paging-cookie.md)<br />
[<span data-ttu-id="05e61-133">Sample: Convert Queries Between Fetch and Query Expression</span><span class="sxs-lookup"><span data-stu-id="05e61-133">Sample: Convert Queries Between Fetch and Query Expression</span></span>](sample-convert-queries-fetch-queryexpression.md)<br />
[<span data-ttu-id="05e61-134">Sample: Validate and execute a saved query</span><span class="sxs-lookup"><span data-stu-id="05e61-134">Sample: Validate and execute a saved query</span></span>](sample-validate-execute-saved-query.md)<br />
  
## <a name="related-sections"></a><span data-ttu-id="05e61-135">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="05e61-135">Related Sections</span></span>

[<span data-ttu-id="05e61-136">Build queries with LINQ (.NET language-integrated query)</span><span class="sxs-lookup"><span data-stu-id="05e61-136">Build queries with LINQ (.NET language-integrated query)</span></span>](build-queries-with-linq-net-language-integrated-query.md)<br />
[<span data-ttu-id="05e61-137">Build queries with QueryExpression</span><span class="sxs-lookup"><span data-stu-id="05e61-137">Build queries with QueryExpression</span></span>](build-queries-with-queryexpression.md)<br />
[<span data-ttu-id="05e61-138">Retrieve Records for Many-To-Many Relationships using Intersect Entities</span><span class="sxs-lookup"><span data-stu-id="05e61-138">Retrieve Records for Many-To-Many Relationships using Intersect Entities</span></span>](retrieve-records-many-to-many-relationships-intersect-entities.md)<br />
[<span data-ttu-id="05e61-139">FetchXML schema</span><span class="sxs-lookup"><span data-stu-id="05e61-139">FetchXML schema</span></span>](fetchxml-schema.md)<br />
