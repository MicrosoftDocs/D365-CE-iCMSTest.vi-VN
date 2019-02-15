---
title: Use XRM tooling to delete data (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Use CrmServiceClient class to delete data from Dynamics 365 for Customer Engagement
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 7e503d2c-89df-4846-8528-632b5ee12bd5
caps.latest.revision: 14
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b7ac5728df1e07e8d364a4aacba826ccb24b69fc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385472"
---
# <a name="use-xrm-tooling-to-delete-data"></a><span data-ttu-id="cedca-103">Use XRM tooling to delete data</span><span class="sxs-lookup"><span data-stu-id="cedca-103">Use XRM tooling to delete data</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="cedca-104">There are two methods available in the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient> class for deleting data in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps: <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient.DeleteEntity(System.String,System.Guid,System.Guid)> and <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient.DeleteEntityAssociation(System.String,System.Guid,System.String,System.Guid,System.String,System.Guid)>.</span><span class="sxs-lookup"><span data-stu-id="cedca-104">There are two methods available in the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient> class for deleting data in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps: <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient.DeleteEntity(System.String,System.Guid,System.Guid)> and <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient.DeleteEntityAssociation(System.String,System.Guid,System.String,System.Guid,System.String,System.Guid)>.</span></span>  
  
## <a name="deleteentity"></a><span data-ttu-id="cedca-105">Xóa Thực thể</span><span class="sxs-lookup"><span data-stu-id="cedca-105">DeleteEntity</span></span>  

 <span data-ttu-id="cedca-106">DeleteEntity is used to remove a single row of data from [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="cedca-106">DeleteEntity is used to remove a single row of data from [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span></span> <span data-ttu-id="cedca-107">To use this method, you need to know the entity schema name you wish to affect, and the GUID of the row you want to remove.</span><span class="sxs-lookup"><span data-stu-id="cedca-107">To use this method, you need to know the entity schema name you wish to affect, and the GUID of the row you want to remove.</span></span>  
  
```csharp  
CrmServiceClient crmSvc = new CrmServiceClient(new System.Net.NetworkCredential("<UserName>", "<Password>", <Domain>),"<Server>", "<Port>", "<OrgName>");  
  
// Verify that you are connected  
if (crmSvc != null && crmSvc.IsReady)  
{  
    //Display the CRM version number and org name that you are connected to  
    Console.WriteLine("Connected to CRM! (Version: {0}; Org: {1}",   
    crmSvc.ConnectedOrgVersion, crmSvc.ConnectedOrgUniqueName);  
  
    // Delete the entity record  
    crmSvc.DeleteEntity("account", <accountId>);  
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
  
## <a name="deleteentityassociation"></a><span data-ttu-id="cedca-108">DeleteEntityAssociation</span><span class="sxs-lookup"><span data-stu-id="cedca-108">DeleteEntityAssociation</span></span>  

 <span data-ttu-id="cedca-109">DeleteEntityAssociation removes the many-to-many association between records in entities.</span><span class="sxs-lookup"><span data-stu-id="cedca-109">DeleteEntityAssociation removes the many-to-many association between records in entities.</span></span> <span data-ttu-id="cedca-110">In this example, we will remove the association between a record in the lead and account entities.</span><span class="sxs-lookup"><span data-stu-id="cedca-110">In this example, we will remove the association between a record in the lead and account entities.</span></span>  
  
```csharp  
CrmServiceClient crmSvc = new CrmServiceClient(new System.Net.NetworkCredential("<UserName>", "<Password>", <Domain>),"<Server>", "<Port>", "<OrgName>");  
  
// Verify that you are connected  
if (crmSvc != null && crmSvc.IsReady)  
{  
    Console.WriteLine("Connected to CRM! (Version: {0}; Org: {1}",   
    crmSvc.ConnectedOrgVersion, crmSvc.ConnectedOrgUniqueName);  
  
    Guid accountId = new Guid("<Account_GUID>");  
    Guid leadId = new Guid("<Lead_GUID>");  
    string accountLeadRelationshipName= "accountleads_association";   
    crmSvc.DeleteEntityAssociation("account" , accountId, "lead" ,  leadId, accountLeadRelationshipName)  
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
  
### <a name="see-also"></a><span data-ttu-id="cedca-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="cedca-111">See also</span></span>  

 <span data-ttu-id="cedca-112">[Sample: Quick start for XRM Tooling API](sample-quick-start-xrm-tooling-api.md) </span><span class="sxs-lookup"><span data-stu-id="cedca-112">[Sample: Quick start for XRM Tooling API](sample-quick-start-xrm-tooling-api.md) </span></span>  
 <span data-ttu-id="cedca-113">[Use XRM Tooling to connect to Dynamics 365 for Customer Engagement apps](use-crmserviceclient-constructors-connect.md) </span><span class="sxs-lookup"><span data-stu-id="cedca-113">[Use XRM Tooling to connect to Dynamics 365 for Customer Engagement apps](use-crmserviceclient-constructors-connect.md) </span></span>  
 [<span data-ttu-id="cedca-114">Use XRM Tooling API to execute actions in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="cedca-114">Use XRM Tooling API to execute actions in Dynamics 365 for Customer Engagement apps</span></span>](use-xrm-tooling-execute-actions.md)
