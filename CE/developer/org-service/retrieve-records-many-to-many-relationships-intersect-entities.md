---
title: Retrieve records for many-to-many relationships using intersect entities (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: An intersect entity is automatically created when there is a many-to-many (N:N) relationship between two entities. Read how you can retrieve records for many-to-many relationships using intersect entities. This topic lists the intersect entities that are used in N:N relationships between default entities
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: b7987bf2-3915-4ddb-b76f-1cc4a1e44404
caps.latest.revision: 37
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 75b4a657a5d3248970ff5ea36fcc0dc30c604ef5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387289"
---
# <a name="retrieve-records-for-many-to-many-relationships-using-intersect-entities"></a>Retrieve records for many-to-many relationships using intersect entities

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, when there is a many-to-many (N:N) relationship between two entities, an intersect entity is automatically created. This is true for both system relationships built into the product as well as custom many-to-many relationships. The name of the entity is specified in the <xref:Microsoft.Xrm.Sdk.Metadata.ManyToManyRelationshipMetadata.IntersectEntityName> property in the relationship metadata. The name of the relationship is specified in the <xref:Microsoft.Xrm.Sdk.Relationship.SchemaName> property in the relationship metadata.  
  
 You can use the intersect entities to refine the result set in any query by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> method or the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest> message. However, you cannot retrieve the intersect entity records directly by using the <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> class. To retrieve the records in an intersect entity, you must use the <xref:Microsoft.Xrm.Sdk.Query.FetchExpression> class.  
  
<a name="BKMK_Entities"></a>   
## <a name="intersect-entities"></a>Intersect entities  
 The following table lists the intersect entities that are used in N:N relationships between default entities.  
  
|IntersectEntity|MtoM_SchemaName|MtoM_Entity1|MtoM_Entity2|  
|---------------------|----------------------|-------------------|-------------------|  
|accountleads|accountleads_association|tài khoản|Khách hàng tiềm năng|  
|campaignactivityitem|campaignactivitylist_association|hoạt động chiến dịch|list|  
|campaignactivityitem|campaignactivitysalesliterature_association|hoạt động chiến dịch|salesliterature|  
|campaignitem|campaigncampaign_association|chiến dịch|chiến dịch|  
|campaignitem|campaignlist_association|chiến dịch|list|  
|campaignitem|campaignproduct_association|chiến dịch|sản phẩm|  
|campaignitem|campaignsalesliterature_association|chiến dịch|salesliterature|  
|competitorproduct|competitorproduct_association|đối thủ cạnh tranh|sản phẩm|  
|competitorsalesliterature|competitorsalesliterature_association|salesliterature|đối thủ cạnh tranh|  
|connectionroleassociation|connectionroleassociation_association|connectionrole|connectionrole|  
|contactinvoices|contactinvoices_association|hóa đơn|người liên hệ|  
|contactleads|contactleads_association|người liên hệ|Khách hàng tiềm năng|  
|contactorders|contactorders_association|đơn bán hàng|người liên hệ|  
|contactquotes|contactquotes_association|báo giá|người liên hệ|  
|entitlementcontacts|entitlementcontacts_association|người liên hệ|quyền hưởng|  
|entitlementproducts|product_entitlement_association|sản phẩm|quyền hưởng|  
|entitlementtemplateproducts|product_entitlementtemplate_association|sản phẩm|mẫu quyền hưởng|  
|leadcompetitors|leadcompetitors_association|Khách hàng tiềm năng|đối thủ cạnh tranh|  
|leadproduct|leadproduct_association|Khách hàng tiềm năng|sản phẩm|  
|listmember|listaccount_association|list|tài khoản|  
|listmember|listcontact_association|list|người liên hệ|  
|listmember|listlead_association|list|Khách hàng tiềm năng|  
|opportunitycompetitors|opportunitycompetitors_association|cơ hội|đối thủ cạnh tranh|  
|liên kết sản phẩm|productassociation_association|sản phẩm|sản phẩm|  
|productsalesliterature|productsalesliterature_association|sản phẩm|salesliterature|  
|tiêu đề phụ sản phẩm|productsubstitute_association|sản phẩm|sản phẩm|  
|queuemembership|queuemembership_association|hàng đợi|người dùng hệ thống|  
|roleprivileges|roleprivileges_association|privilege|vai trò|  
|roletemplateprivileges|roletemplateprivileges_association|roletemplate|privilege|  
|servicecontractcontacts|servicecontractcontacts_association|người liên hệ|hợp đồng|  
|subscriptionmanuallytrackedobject|contact_subscription_association|Đăng ký |người liên hệ|  
|subscriptionmanuallytrackedobject|task_subscription_association|Đăng ký |nhiệm vụ|  
|systemuserprofiles|systemuserprofiles_association|người dùng hệ thống|fieldsecurityprofile|  
|systemuserroles|systemuserroles_association|người dùng hệ thống|vai trò|  
|teammembership|teammembership_association|nhóm|người dùng hệ thống|  
|teamprofiles|teamprofiles_association|nhóm|fieldsecurityprofile|  
|teamroles|teamroles_association|nhóm|vai trò|  
  
<a name="BKMK_metadata"></a>   
## <a name="intersect-entity-metadata"></a>Intersect entity metadata  
 Most intersect entities are simple, containing just the few properties that are needed to provide a link between to two entities in the N:N relationship. If you are using early bound types,  you can see an example, in the `ContactInvoices` intersect entity. This is the case for all custom many-to-many relationships. However, there are several intersect entities that have additional properties that are used for specific functionality for the relationship. To make it easier to write queries by using the special intersect entities, the attribute metadata is provided in the following topics:  
  
-   [Campaign Activity Item Intersect Entity](campaignactivityitem-intersect-entity-metadata.md)  
  
-   [Campaign Item Intersect Entity](campaignitem-intersect-entity-metadata.md)  
  
-   [List Member Intersect Entity](listmember-intersect-entity-metadata.md)  
  
-   [Role Privileges Intersect Entity](role-privileges-intersect-entity-metadata.md)  
  
### <a name="see-also"></a>Xem thêm  
 [Building Queries](build-queries-with-queryexpression.md)   
 [Customize entity relationship metadata](../customize-entity-relationship-metadata.md)   
 [Retrieve data with queries](retrieve-data-queries-sdk-assemblies.md)   
 [CampaignActivityItem intersect entity metadata](campaignactivityitem-intersect-entity-metadata.md)   
 [CampaignItem intersect entity metadata](campaignitem-intersect-entity-metadata.md)   
 [ListMember intersect entity metadata](listmember-intersect-entity-metadata.md)   
 [Role Privileges intersect entity metadata](role-privileges-intersect-entity-metadata.md)   
 [Sample: Retrieve Records from an Intersect Table](sample-retrieve-records-intersect-table.md)
