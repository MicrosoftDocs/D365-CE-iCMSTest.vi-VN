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
# <a name="build-queries-with-fetchxml"></a>Build queries with FetchXML

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

FetchXML is a proprietary query language that is used in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement. It’s based on a schema that describes the capabilities of the language. The FetchXML language supports similar query capabilities as query expressions. In addition, it’s used as a serialized form of query, used to save a query as a user-owned saved view in the [UserQuery Entity](../entities/userquery.md) and as an organization-owned saved view in the [SavedQuery Entity](../entities/savedquery.md).  
  
## <a name="execute-queries-in-code"></a>Execute queries in code
A FetchXML query can be executed by using either the Web API or the Organization service.

### <a name="web-api"></a>API Web
You can pass a URL encoded FetchXml string to the appropriate entityset using the `fetchXml` query string parameter. More information: [Use custom FetchXML](../webapi/retrieve-and-execute-predefined-queries.md#use-custom-fetchxml).

### <a name="organization-service"></a>Organization service
Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> method passing an <xref:Microsoft.Xrm.Sdk.Query.FetchExpression> where the <xref:Microsoft.Xrm.Sdk.Query.FetchExpression.Query> property contains the FetchXml query.

You can convert a FetchXML query to a query expression with the <xref:Microsoft.Crm.Sdk.Messages.FetchXmlToQueryExpressionRequest> message.  
  
## <a name="tools"></a>Công cụ

The [XrmToolBox FetchXML Builder](https://www.xrmtoolbox.com/plugins/Cinteros.Xrm.FetchXmlBuilder/) provides a user interface to compose and execute FetchXml queries.
> [!NOTE]
> The XrmToolBox FetchXML Builder is not a product of [!include[pn_microsoft_dynamics](../../includes/pn-microsoft-dynamics.md)] and does not extend support to it. If you have questions pertaining to the FetchXML Builder, please contact the [publisher](http://fxb.xrmtoolbox.com/).

Advanced Find includes the capability to download the FetchXML for the query using the **Dowload Fetch XML** command. Thông tin khác: [Tạo, chỉnh sửa hoặc lưu Tìm kiếm Nâng cao](../../basics/save-advanced-find-search.md)
  
## <a name="in-this-section"></a>In This Section

[Use FetchXML to Construct a Query](use-fetchxml-construct-query.md)<br />
[Use FetchXML Aggregation](use-fetchxml-aggregation.md)<br />
[Page Large Result Sets with FetchXML](page-large-result-sets-with-fetchxml.md)<br />
[Fiscal Date Query Operators in FetchXML](fiscal-date-older-datetime-query-operators-fetchxml.md)<br />
[Use a left outer join in FetchXML to query for records not in](use-left-outer-join-fetchxml-query-records-not-in.md)<br />
[Sample: Use Aggregation in FetchXML](sample-use-aggregation-fetchxml.md)<br />
[Sample: Use FetchXML with a Paging Cookie](sample-use-fetchxml-paging-cookie.md)<br />
[Sample: Convert Queries Between Fetch and Query Expression](sample-convert-queries-fetch-queryexpression.md)<br />
[Sample: Validate and execute a saved query](sample-validate-execute-saved-query.md)<br />
  
## <a name="related-sections"></a>Các phần liên quan

[Build queries with LINQ (.NET language-integrated query)](build-queries-with-linq-net-language-integrated-query.md)<br />
[Build queries with QueryExpression](build-queries-with-queryexpression.md)<br />
[Retrieve Records for Many-To-Many Relationships using Intersect Entities](retrieve-records-many-to-many-relationships-intersect-entities.md)<br />
[FetchXML schema](fetchxml-schema.md)<br />