---
title: Supported types, triggers, entities, and actions for processes (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: 'The topic provides information about the supported types and entities for processes in Dynamics 365 for Customer Engagement, supported triggers for workflows, entities that are supported for the CreateEntity activity, and supported actions for workflows. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: b2c14b32-e7da-4f9b-b7b1-659596c456ca
caps.latest.revision: 33
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3d84ecb1b29d9c58ea91c2863964bc93fa465bf9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387093"
---
# <a name="supported-types-triggers-entities-and-actions-for-processes"></a>Supported types, triggers, entities, and actions for processes

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This topic provides information about the supported types and entities for processes in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement, supported triggers for workflows, entities that are supported for the <xref:Microsoft.Xrm.Sdk.Workflow.Activities.CreateEntity> activity, and supported actions for workflows.  

<a name="bkmk_triggersWorkflows"></a>   
## <a name="supported-triggers-for-workflows"></a>Supported triggers for workflows  
 The following actions can be used to trigger a workflow automatically.  

|Yêu cầu|Thông báo|Bộ kích hoạt|  
|-------------|-------------|-------------|  
|<xref:Microsoft.Crm.Sdk.Messages.AssignRequest>|Chỉ định|Record is assigned.|  
|<xref:Microsoft.Crm.Sdk.Messages.BookRequest>|Book|Record is created.|  
|<xref:Microsoft.Crm.Sdk.Messages.CancelContractRequest><br /><br /> <xref:Microsoft.Crm.Sdk.Messages.CancelSalesOrderRequest>|Hủy|Record status changes.|  
|<xref:Microsoft.Crm.Sdk.Messages.CloneContractRequest>|Sao y|Record is created.|  
|<xref:Microsoft.Crm.Sdk.Messages.CloseIncidentRequest><br /><br /> <xref:Microsoft.Crm.Sdk.Messages.CloseQuoteRequest>|Đóng|Record status changes.|  
|<xref:Microsoft.Crm.Sdk.Messages.CompoundCreateRequest>|CompoundCreate|Record is created.|  
|<xref:Microsoft.Crm.Sdk.Messages.CompoundUpdateRequest>|CompoundUpdate|Record is updated.|  
|<xref:Microsoft.Crm.Sdk.Messages.ConvertKitToProductRequest>|ConvertKitToProduct|Record is updated.|  
|<xref:Microsoft.Crm.Sdk.Messages.ConvertQuoteToSalesOrderRequest>|ConvertProductToKit|Record is updated.|  
|<xref:Microsoft.Crm.Sdk.Messages.ConvertQuoteToSalesOrderRequest>|ConvertQuoteToSalesOrder|Record is created.|  
|<xref:Microsoft.Crm.Sdk.Messages.ConvertSalesOrderToInvoiceRequest>|ConvertSalesOrderToInvoice|Record is created.|  
|<xref:Microsoft.Crm.Sdk.Messages.CopyCampaignRequest><br /><br /> <xref:Microsoft.Crm.Sdk.Messages.CopyMembersListRequest>|Sao chép|Record is created.|  
|<xref:Microsoft.Xrm.Sdk.Messages.CreateRequest>|Tạo|Record is created.|  
|<xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest>|Xóa|Record is deleted.|  
|<xref:Microsoft.Crm.Sdk.Messages.DeliverIncomingEmailRequest>|DeliverIncoming|Record is created.|  
|<xref:Microsoft.Crm.Sdk.Messages.DeliverPromoteEmailRequest>|DeliverPromote|Record is created.|  
|<xref:Microsoft.Crm.Sdk.Messages.FulfillSalesOrderRequest>|Fulfill|Record status changes.|  
|<xref:Microsoft.Crm.Sdk.Messages.GenerateInvoiceFromOpportunityRequest>|GenerateInvoiceFromOpportunity|Record is created.|  
|<xref:Microsoft.Crm.Sdk.Messages.GenerateQuoteFromOpportunityRequest>|GenerateQuoteFromOpportunity|Record is created.|  
|<xref:Microsoft.Crm.Sdk.Messages.GenerateSalesOrderFromOpportunityRequest>|GenerateSalesOrderFromOpportunity|Record is created.|  
|<xref:Microsoft.Crm.Sdk.Messages.GetInvoiceProductsFromOpportunityRequest>|GetInvoiceProductsFromOpportunity|Record is created.|  
|<xref:Microsoft.Crm.Sdk.Messages.GetQuoteProductsFromOpportunityRequest>|GetQuoteProductsFromOpportunity|Record is created.|  
|<xref:Microsoft.Crm.Sdk.Messages.GetSalesOrderProductsFromOpportunityRequest>|GetSalesOrderProductsFromOpportunity|Record is created.|  
|<xref:Microsoft.Crm.Sdk.Messages.LockInvoicePricingRequest>|LockInvoicePricing|Record is updated.|  
|<xref:Microsoft.Crm.Sdk.Messages.LockSalesOrderPricingRequest>|LockSalesOrderPricing|Record is updated.|  
|<xref:Microsoft.Crm.Sdk.Messages.LoseOpportunityRequest>|Lose|Record status changes.|  
|<xref:Microsoft.Crm.Sdk.Messages.MakeAvailableToOrganizationReportRequest><br /><br /> <xref:Microsoft.Crm.Sdk.Messages.MakeAvailableToOrganizationTemplateRequest>|MakeAvailableToOrganization|Record is updated.|  
|<xref:Microsoft.Crm.Sdk.Messages.MakeUnavailableToOrganizationReportRequest><br /><br /> <xref:Microsoft.Crm.Sdk.Messages.MakeUnavailableToOrganizationTemplateRequest>|MakeUnavailableToOrganization|Record is updated.|  
|<xref:Microsoft.Crm.Sdk.Messages.MergeRequest>|Hợp nhất|Record is updated.|  
|<xref:Microsoft.Crm.Sdk.Messages.RemoveParentRequest>|RemoveParent|Record is updated.|  
|<xref:Microsoft.Crm.Sdk.Messages.RenewContractRequest>|Renew|Record is created.|  
|<xref:Microsoft.Crm.Sdk.Messages.RescheduleRequest>|Reschedule|Record is updated.|  
|<xref:Microsoft.Crm.Sdk.Messages.ReviseQuoteRequest>|Sửa lại|Record is created.|  
|<xref:Microsoft.Crm.Sdk.Messages.SendBulkMailRequest>|SendBulkMail|Record status changes.|  
|<xref:Microsoft.Crm.Sdk.Messages.SendEmailFromTemplateRequest>|SendEmailFromTemplate|Record is created.|  
|<xref:Microsoft.Crm.Sdk.Messages.SendFaxRequest>|SendFax|Record status changes.|  
|<xref:Microsoft.Crm.Sdk.Messages.SetBusinessEquipmentRequest><br /><br /> <xref:Microsoft.Crm.Sdk.Messages.SetBusinessSystemUserRequest>|SetBusiness|Record is updated.|  
|<xref:Microsoft.Crm.Sdk.Messages.SetParentBusinessUnitRequest><br /><br /> <xref:Microsoft.Crm.Sdk.Messages.SetParentSystemUserRequest><br /><br /> <xref:Microsoft.Crm.Sdk.Messages.SetParentTeamRequest>|SetParent|Record is updated.|  
|<xref:Microsoft.Crm.Sdk.Messages.SetStateRequest>|SetState|Record status changes.|  
|<xref:Microsoft.Crm.Sdk.Messages.UnlockInvoicePricingRequest>|UnlockInvoicePricing|Record is updated.|  
|<xref:Microsoft.Crm.Sdk.Messages.UnlockSalesOrderPricingRequest>|UnlockSalesOrderPricing|Record is updated.|  
|<xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest>|Update|Record is updated.|  
|<xref:Microsoft.Crm.Sdk.Messages.WinOpportunityRequest><br /><br /> <xref:Microsoft.Crm.Sdk.Messages.WinQuoteRequest>|Win|Record status changes.|  

<a name="bkmk_typesProcesses"></a>   
## <a name="supported-types-for-processes"></a>Supported types for processes  
 This topic provides the supported types that you can use in your code for processes in[!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].  

### <a name="microsoft-net-framework-452"></a>Microsoft .NET Framework 4.5.2  

|Không gian tên|Type name|  
|---------------|---------------|  
|System.Activities.Statements|AddToCollection\<T>|  
|System.Activities.Statements|Chỉ định|  
|System.Activities.Statements|Catch\<TException>|  
|System.Activities.Statements|ClearCollection\<T>|  
|System.Activities.Statements|DoWhile|  
|System.Activities.Statements|ExistsInCollection\<T>|  
|System.Activities.Statements|ForEach\<T>|  
|System.Activities.Statements|If|  
|System.Activities.Statements|Interop|  
|System.Activities.Statements|InvokeMethod|  
|System.Activities.Statements|Persist|  
|System.Activities.Statements|RemoveFromCollection\<T>|  
|System.Activities.Statements|Rethrow|  
|System.Activities.Statements|Sequence|  
|System.Activities.Statements|Switch\<T>|  
|System.Activities.Statements|TerminateWorkflow|  
|System.Activities.Statements|Throw|  
|System.Activities.Statements|TryCatch|  
|System.Activities.Statements|While|  
|System.Activities.Statements|Receive|  
|System.Activities.Statements|Gửi|  
|System.ServiceModel.Activities.Presentation.Factories|SendAndReceiveReplyFactory|  

 For information about each type, see the following documentation for the respective namespaces:  

-   [System.Activities.Statements Namespace](https://msdn.microsoft.com/library/system.activities.statements.aspx)  

-   [System.ServiceModel.Activities Namespace](https://msdn.microsoft.com/library/system.servicemodel.activities.aspx)  

-   [System.ServiceModel.Activities.Presentation.Factories](https://msdn.microsoft.com/library/system.servicemodel.activities.presentation.factories.aspx)  

### [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]  

|Không gian tên|Type name|  
|---------------|---------------|  
|<xref:Microsoft.Xrm.Sdk>|All types|  
|<xref:Microsoft.Xrm.Sdk.Workflow>|All types|  
|<xref:Microsoft.Xrm.Sdk.Workflow.Activities>|All types|  
|<xref:Microsoft.Crm.Sdk>|All types|  

<a name="bkmk_EntitiesProcess"></a>   
## <a name="supported-entities-for-processes"></a>Supported entities for processes  
 The following table lists the entities that can be used to trigger process execution or to create a record within a process by using the <xref:Microsoft.Xrm.Sdk.Workflow.Activities.CreateEntity> class. This list is determined by the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanTriggerWorkflow> property for each entity.  

|Tên thực thể|Trigger a process|Used for CreateEntity|  
|-----------------|-----------------------|---------------------------|  
|Khách hàng|Có|Có|  
|Annotation|Có|Có|  
|Cuộc hẹn|Có|Có|  
|Đơn vị kinh doanh|Có|Không|  
|BusinessUnitNewsArticle|Có|Không|  
|Chiến dịch|Có|Có|  
|CampaignActivity|Có|Có|  
|CampaignResponse|Có|Có|  
|Đối thủ cạnh tranh|Có|Có|  
|Connection|Có|Có|  
|Vai trò Kết nối|Có|Không|  
|ConstraintbasedGroup|Có|Không|  
|người liên hệ|Có|Có|  
|Hợp đồng|Có|Có|  
|ContractDetail|Có|Không|  
|ContractTemplate|Có|Không|  
|CustomerAddress|Có|Không|  
|CustomerOpportunityRole|Có|Không|  
|CustomerRelationship|Có|Không|  
|Giảm giá|Có|Không|  
|DiscountType|Có|Không|  
|Email|Có|Có|  
|Thiết bị|Có|Không|  
|Fax|Có|Có|  
|Mục tiêu|Có|Có|  
|Sự cố|Có|Có|  
|Hóa đơn|Có|Có|  
|InvoiceDetail|Có|Không|  
|KbArticle|Có|Không|  
|KbArticleComment|Có|Không|  
|KbArticleTemplate|Có|Không|  
|Khách hàng tiềm năng|Có|Có|  
|Thư tín|Có|Có|  
|Danh sách|Có|Có|  
|Metric|Không|Có|  
|MailMergeTemplate|Có|Không|  
|Cơ hội|Có|Có|  
|OpportunityProduct|Có|Không|  
|Cuộc gọi Điện thoại |Có|Có|  
|PriceLevel|Có|Có|  
|ProcessSession|Có|Không|  
|Sản phẩm|Có|Không|  
|ProductPriceLevel|Có|Không|  
|Hàng đợi|Có|Có|  
|QueueItem|Không|Có|  
|Báo giá|Có|Có|  
|QuoteDetail|Có|Không|  
|RecurringAppointmentMaster|Có|Có|  
|Trường tổng số|Không|Có|  
|RelationshipRole|Có|Không|  
|Báo cáo|Có|Không|  
|SalesLiterature|Có|Có|  
|SalesLiteratureItem|Có|Không|  
|SalesOrder|Có|Có|  
|SalesOrderDetail|Có|Không|  
|Dịch vụ |Có|Không|  
|ServiceAppointment|Có|Có|  
|SharePointDocumentLocation|Có|Có|  
|Trang SharePoint|Có|Có|  
|Trang|Có|Có|  
|Chủ đề|Có|Không|  
|Người dùng hệ thống|Có|Có|  
|Nhiệm vụ|Có|Có|  
|Nhóm|Có|Không|  
|Mẫu|Có|Không|  
|Vùng lãnh thổ|Có|Có|  
|TransactionCurrency|Có|Không|  

<a name="BKMK_Actions"></a>   
## <a name="supported-actions-for-processes"></a>Supported actions for processes  
 You can choose to perform following actions using workflows in [!INCLUDE[pn_dyn_365](../includes/pn-dyn-365.md)]. Use the `sdkmessage.workflowsdkstepenabled` attribute to find the list of supported actions available under a workflow step. You can use the following Web API query to retrieve the list of supported actions:  

```
[Organization URI]/api/data/v9.0/sdkmessages?$select=name&$filter=workflowsdkstepenabled%20eq%20true  
```  


|                Hành động                |                                                                                              Mô tả                                                                                               |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              AddToQueue              |                                                                          <xref:Microsoft.Crm.Sdk.Messages.AddToQueueRequest>                                                                           |
|         AddUserToRecordTeam          |                                                                      <xref:Microsoft.Crm.Sdk.Messages.AddUserToRecordTeamRequest>                                                                      |
|           ApplyRoutingRule           |                                                                       <xref:Microsoft.Crm.Sdk.Messages.ApplyRoutingRuleRequest>                                                                        |
|         CalculateActualValue         |                                                                <xref:Microsoft.Crm.Sdk.Messages.CalculateActualValueOpportunityRequest>                                                                |
|           CloseOpportunity           |                                                                        <xref:Microsoft.Crm.Sdk.Messages.WinOpportunityRequest>                                                                         |
|   GetQuoteProductsFromOpportunity    |                                                                <xref:Microsoft.Crm.Sdk.Messages.GetQuoteProductsFromOpportunityRequest>                                                                |
| GetSalesOrderProductsFromOpportunity |                                                             <xref:Microsoft.Crm.Sdk.Messages.GetSalesOrderProductsFromOpportunityRequest>                                                              |
|          LockInvoicePricing          |                                                                      <xref:Microsoft.Crm.Sdk.Messages.LockInvoicePricingRequest>                                                                       |
|        LockSalesOrderPricing         |                                                                     <xref:Microsoft.Crm.Sdk.Messages.LockSalesOrderPricingRequest>                                                                     |
|             QualifyLead              |                                                                          <xref:Microsoft.Crm.Sdk.Messages.QualifyLeadRequest>                                                                          |
|       RemoveUserFromRecordTeam       |                                                                   <xref:Microsoft.Crm.Sdk.Messages.RemoveUserFromRecordTeamRequest>                                                                    |
|           ResolveIncident            |                                                                         <xref:Microsoft.Crm.Sdk.Messages.CloseIncidentRequest>                                                                         |
|             ResolveQuote             |                                                                          <xref:Microsoft.Crm.Sdk.Messages.CloseQuoteRequest>                                                                           |
|             ReviseQuote              |                                                                          <xref:Microsoft.Crm.Sdk.Messages.ReviseQuoteRequest>                                                                          |
|              SetProcess              |                                                                          <xref:Microsoft.Crm.Sdk.Messages.SetProcessRequest>                                                                           |
|           SetWordTemplate            | Custom action to create a word template. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Using Word templates in Dynamics 365 for Customer Engagement](../admin/using-word-templates-dynamics-365.md) |
|         UnlockInvoicePricing         |                                                                     <xref:Microsoft.Crm.Sdk.Messages.UnlockInvoicePricingRequest>                                                                      |
|       UnlockSalesOrderPricing        |                                                                    <xref:Microsoft.Crm.Sdk.Messages.UnlockSalesOrderPricingRequest>                                                                    |

### <a name="see-also"></a>Xem thêm  
 [Create your own actions](create-own-actions.md)   
 [Processes in Dynamics 365 for Customer Engagement apps(formerly Workflows)](automate-business-processes-customer-engagement.md)   
 [Custom workflow activities (workflow assemblies)](custom-workflow-activities-workflow-assemblies.md)   
 <xref:Microsoft.Xrm.Sdk.Workflow.Activities.CreateEntity>
