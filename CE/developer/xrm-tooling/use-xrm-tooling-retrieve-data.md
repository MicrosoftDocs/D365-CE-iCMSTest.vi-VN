---
title: Use XRM tooling to retrieve data (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Use CrmServiceClient class to retrieve data from Dynamics 365 for Customer Engagement
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 2afc057e-8f70-4bea-bad4-d01e18ed92fd
caps.latest.revision: 14
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0b7a947a96e119d3f8a2ebba60d217be89abf69f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387833"
---
# <a name="use-xrm-tooling-to-retrieve-data"></a><span data-ttu-id="14fdd-103">Use XRM tooling to retrieve data</span><span class="sxs-lookup"><span data-stu-id="14fdd-103">Use XRM tooling to retrieve data</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="14fdd-104">There are many methods available in the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient> class for retrieving data in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="14fdd-104">There are many methods available in the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient> class for retrieving data in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span></span> <span data-ttu-id="14fdd-105">The following examples demonstrate how you can retrieve a record by ID or FetchXML query.</span><span class="sxs-lookup"><span data-stu-id="14fdd-105">The following examples demonstrate how you can retrieve a record by ID or FetchXML query.</span></span>  
  
## <a name="getentitydatabyid"></a><span data-ttu-id="14fdd-106">GetEntityDataById</span><span class="sxs-lookup"><span data-stu-id="14fdd-106">GetEntityDataById</span></span>  

 <span data-ttu-id="14fdd-107">This method searches for an entity by the specified ID.</span><span class="sxs-lookup"><span data-stu-id="14fdd-107">This method searches for an entity by the specified ID.</span></span> <span data-ttu-id="14fdd-108">In this sample, we specify null for the field list value to fetch all the attributes of the specified entity record (account), and then display the name of the retrieved account record.</span><span class="sxs-lookup"><span data-stu-id="14fdd-108">In this sample, we specify null for the field list value to fetch all the attributes of the specified entity record (account), and then display the name of the retrieved account record.</span></span>  
  
```csharp  
CrmServiceClient crmSvc = new CrmServiceClient(new System.Net.NetworkCredential("<UserName>", "<Password>", “<Domain>”),"<Server>", "<Port>", "<OrgName>");  
  
// Verify that you are connected.  
if (crmSvc != null && crmSvc.IsReady)  
{  
    //Display the CRM version number and org name that you are connected to  
    Console.WriteLine("Connected to CRM! (Version: {0}; Org: {1}",   
    crmSvc.ConnectedOrgVersion, crmSvc.ConnectedOrgUniqueName);  
  
    Dictionary<string, object> data = crmSvc.GetEntityDataById("account", <Account_ID>, null);  
    foreach (var pair in data)  
    {  
        if (pair.Key == "name")  
        {  
            Console.WriteLine("Name of the account is {0}", pair.Value);  
        }  
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
  
## <a name="getentitydatabyfetchsearchec"></a><span data-ttu-id="14fdd-109">GetEntityDataByFetchSearchEC</span><span class="sxs-lookup"><span data-stu-id="14fdd-109">GetEntityDataByFetchSearchEC</span></span>  

 <span data-ttu-id="14fdd-110">This method searches for the entity based on the specified FetchXML query.</span><span class="sxs-lookup"><span data-stu-id="14fdd-110">This method searches for the entity based on the specified FetchXML query.</span></span> <span data-ttu-id="14fdd-111">In this sample, we retrieve and display the count of all account records in the system.</span><span class="sxs-lookup"><span data-stu-id="14fdd-111">In this sample, we retrieve and display the count of all account records in the system.</span></span>  
  
```csharp  
CrmServiceClient crmSvc = new CrmServiceClient(new System.Net.NetworkCredential("<UserName>", "<Password>", “<Domain>”),"<Server>", "<Port>", "<OrgName>");  
  
// Verify that you are connected.  
if (crmSvc != null && crmSvc.IsReady)  
{  
    //Display the CRM version number and org name that you are connected to  
    Console.WriteLine("Connected to CRM! (Version: {0}; Org: {1}",   
    crmSvc.ConnectedOrgVersion, crmSvc.ConnectedOrgUniqueName);  
  
    string fetchXML =   
        @"<fetch version='1.0' output-format='xml-platform' mapping='logical' distinct='false' returntotalrecordcount='true' >  
            <entity name='account'>  
              <attribute name='accountid' />  
            </entity>  
        </fetch>";  
    var queryResult = crmSvc.GetEntityDataByFetchSearchEC(fetchXML);  
    if (queryResult != null)  
    {  
        Console.WriteLine(String.Format("Account Records Count : {0}", queryResult.TotalRecordCount));  
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
  
### <a name="see-also"></a><span data-ttu-id="14fdd-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="14fdd-112">See also</span></span>  

 <span data-ttu-id="14fdd-113">[Sample: Quick start for XRM Tooling API](sample-quick-start-xrm-tooling-api.md) </span><span class="sxs-lookup"><span data-stu-id="14fdd-113">[Sample: Quick start for XRM Tooling API](sample-quick-start-xrm-tooling-api.md) </span></span>  
 <span data-ttu-id="14fdd-114">[Use XRM Tooling to connect to Dynamics 365 for Customer Engagement apps](use-crmserviceclient-constructors-connect.md) </span><span class="sxs-lookup"><span data-stu-id="14fdd-114">[Use XRM Tooling to connect to Dynamics 365 for Customer Engagement apps](use-crmserviceclient-constructors-connect.md) </span></span>  
 [<span data-ttu-id="14fdd-115">Use XRM Tooling API to execute actions in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="14fdd-115">Use XRM Tooling API to execute actions in Dynamics 365 for Customer Engagement apps</span></span>](use-xrm-tooling-execute-actions.md)