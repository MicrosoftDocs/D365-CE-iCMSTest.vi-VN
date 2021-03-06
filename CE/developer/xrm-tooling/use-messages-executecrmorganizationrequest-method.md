---
title: Use messages with the ExecuteCrmOrganizationRequest method (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Learn how to use messages with the ExecuteCrmOrganizationRequest method. The samples demonstrate how to execute CreateRequest and RetrieveMultipleRequest message using the CrmServiceClient.String) method.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1ba60f67-522d-4540-a6f9-0787d7074a79
caps.latest.revision: 17
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f4fbf6506e41aa14031bf4ca8ca78651144b968c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386045"
---
# <a name="use-messages-with-the-executecrmorganizationrequest-method"></a>Use messages with the ExecuteCrmOrganizationRequest method

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

In addition to using the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*> method, you can now use the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient>.<xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient.ExecuteCrmOrganizationRequest*> method to execute the xRM and [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Customer Engagement messages. Similar to the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*> method, the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient.ExecuteCrmOrganizationRequest*> method takes a message request class as a parameter and returns a message response class. For a list of messages that you can execute using the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient>.<xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient.ExecuteCrmOrganizationRequest*> method, see [xRM Messages in the Organization Service](../org-service/xrm-messages-organization-service.md) and [Dynamics 365 for Customer Engagement apps Messages in the Organization Service](../org-service/organization-service-messages.md).  
  
 The following code samples demonstrate how you can execute messages using the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient.ExecuteCrmOrganizationRequest*> method.  
  
## <a name="example-1-createrequest-message"></a>Example 1: CreateRequest message  

 The following code sample demonstrates how to execute the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message using the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient>.<xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient.ExecuteCrmOrganizationRequest*> method. In this example, you create an account, and then display the ID in the response object.  
  
```csharp 
CrmServiceClient crmSvc = new CrmServiceClient(new System.Net.NetworkCredential("<UserName>", "<Password>", "<Domain>"),"<Server>", "<Port>", "<OrgName>");  
  
// Verify that you are connected.  
if (crmSvc != null && crmSvc.IsReady)  
{  
    //Display the CRM version number and org name that you are connected to.  
    Console.WriteLine("Connected to CRM! (Version: {0}; Org: {1}",   
    crmSvc.ConnectedOrgVersion, crmSvc.ConnectedOrgUniqueName);  
  
    CreateRequest request = new CreateRequest();  
    Entity newAccount = new Entity("account");  
    newAccount.Attributes.Add("name", "Sample Test Account");  
    request.Target = newAccount;  
    CreateResponse response = (CreateResponse)crmSvc.ExecuteCrmOrganizationRequest(request);  
  
    // Display the ID of the newly created account record.  
    Console.WriteLine("Account record created with the following ID: {0}", response.id.ToString());  
}  
else  
{  
    // Display the last error.  
    Console.WriteLine("An error occurred: {0}", crmSvc.LastCrmError);  
  
    // Display the last exception message if any.  
    Console.WriteLine(crmSvc.LastCrmException.Message);  
    Console.WriteLine(crmSvc.LastCrmException.Source);  
    Console.WriteLine(crmSvc.LastCrmException.StackTrace);  
  
    return;  
}  
```  
  
## <a name="example-2-retrievemultiplerequest"></a>Example 2: RetrieveMultipleRequest  

 The following code sample demonstrates how to execute the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest> message using the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient>.<xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient.ExecuteCrmOrganizationRequest*> method. In this example, you execute a retrieve multiple request to fetch all the contacts in the system, and display their full name.  
  
```csharp  
CrmServiceClient crmSvc = new CrmServiceClient(new System.Net.NetworkCredential("<UserName>", "<Password>", "<Domain>"),"<Server>", "<Port>", "<OrgName>");  
  
// Verify that you are connected.  
if (crmSvc != null && crmSvc.IsReady)  
{  
    //Display the CRM version number and org name that you are connected to.  
    Console.WriteLine("Connected to CRM! (Version: {0}; Org: {1}",   
    crmSvc.ConnectedOrgVersion, crmSvc.ConnectedOrgUniqueName);  
  
    QueryExpression userSettingsQuery = new QueryExpression("contact");  
    userSettingsQuery.ColumnSet.AllColumns = true;  
    var retrieveRequest = new RetrieveMultipleRequest()  
    {  
        Query = userSettingsQuery  
    };  
    EntityCollection EntCol = (crmSvc.ExecuteCrmOrganizationRequest(retrieveRequest) as RetrieveMultipleResponse).EntityCollection;  
    foreach (var a in EntCol.Entities)  
    {  
        Console.WriteLine("Account name: {0} {1}", a.Attributes["firstname"], a.Attributes["lastname"]);  
    }  
}  
else  
{  
    // Display the last error.  
    Console.WriteLine("An error occurred: {0}", crmSvc.LastCrmError);  
  
    // Display the last exception message if any.  
    Console.WriteLine(crmSvc.LastCrmException.Message);  
    Console.WriteLine(crmSvc.LastCrmException.Source);  
    Console.WriteLine(crmSvc.LastCrmException.StackTrace);  
  
    return;  
}  
```  
  
### <a name="see-also"></a>Xem thêm  

 [Use Messages (Request and Response Classes) with the Execute Method](../org-service/use-messages-request-response-classes-execute-method.md)   
 [Use XRM Tooling to connect to Dynamics 365 for Customer Engagement apps](use-crmserviceclient-constructors-connect.md)   
 [Use XRM Tooling API to execute actions in Dynamics 365 for Customer Engagement apps](use-xrm-tooling-execute-actions.md)
