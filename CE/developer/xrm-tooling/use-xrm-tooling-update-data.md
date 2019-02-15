---
title: Use XRM tooling to update data (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Use CrmServiceClient class to update data on Dynamics 365 for Customer Engagement
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 8ec3d4ca-d836-4e7e-b2bf-9d9f806bd145
caps.latest.revision: 14
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3e69a533673f0ee6fcec9a4274f0bb35116be135
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388806"
---
# <a name="use-xrm-tooling-to-update-data"></a><span data-ttu-id="1263b-103">Use XRM tooling to update data</span><span class="sxs-lookup"><span data-stu-id="1263b-103">Use XRM tooling to update data</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="1263b-104">There are two methods available in the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient> class for updating data in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps: <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient.UpdateEntity(System.String,System.String,System.Guid,System.Collections.Generic.Dictionary{System.String,Microsoft.Xrm.Tooling.Connector.CrmDataTypeWrapper},System.String,System.Boolean,System.Guid)> and <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient.UpdateStateAndStatusForEntity(System.String,System.Guid,System.String,System.String,System.Guid)>.</span><span class="sxs-lookup"><span data-stu-id="1263b-104">There are two methods available in the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient> class for updating data in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps: <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient.UpdateEntity(System.String,System.String,System.Guid,System.Collections.Generic.Dictionary{System.String,Microsoft.Xrm.Tooling.Connector.CrmDataTypeWrapper},System.String,System.Boolean,System.Guid)> and <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient.UpdateStateAndStatusForEntity(System.String,System.Guid,System.String,System.String,System.Guid)>.</span></span>  
  
 <span data-ttu-id="1263b-105">An update action using XRM Tooling API requires a data payload.</span><span class="sxs-lookup"><span data-stu-id="1263b-105">An update action using XRM Tooling API requires a data payload.</span></span> <span data-ttu-id="1263b-106">The data payload takes the form of a Dictionary\<string, CrmDataTypeWrapper> object.</span><span class="sxs-lookup"><span data-stu-id="1263b-106">The data payload takes the form of a Dictionary\<string, CrmDataTypeWrapper> object.</span></span> <span data-ttu-id="1263b-107"><xref:Microsoft.Xrm.Tooling.Connector.CrmDataTypeWrapper> is used to inform the interface what sort of handling needs to be applied to the data point you are referencing.</span><span class="sxs-lookup"><span data-stu-id="1263b-107"><xref:Microsoft.Xrm.Tooling.Connector.CrmDataTypeWrapper> is used to inform the interface what sort of handling needs to be applied to the data point you are referencing.</span></span>  
  
## <a name="updateentity"></a><span data-ttu-id="1263b-108">Cập nhật thực thể</span><span class="sxs-lookup"><span data-stu-id="1263b-108">UpdateEntity</span></span>  

 <span data-ttu-id="1263b-109">This is the anchor method for updating any record in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], with the exception of setting status or state of a record.</span><span class="sxs-lookup"><span data-stu-id="1263b-109">This is the anchor method for updating any record in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], with the exception of setting status or state of a record.</span></span> <span data-ttu-id="1263b-110">To use it, you need to know the following information: schema name of the entity you want to update, the primary key field of the entity you want to update, the GUID of the record you want to update, and finally the data payload array to update it with.</span><span class="sxs-lookup"><span data-stu-id="1263b-110">To use it, you need to know the following information: schema name of the entity you want to update, the primary key field of the entity you want to update, the GUID of the record you want to update, and finally the data payload array to update it with.</span></span>  
  
```csharp  
CrmServiceClient crmSvc = new CrmServiceClient(new System.Net.NetworkCredential("<UserName>", "<Password>", “<Domain>”),"<Server>", "<Port>", "<OrgName>");  
  
// Verify that you are connected  
if (crmSvc != null && crmSvc.IsReady)  
{  
    //Display the CRM version number and org name that you are connected to  
    Console.WriteLine("Connected to CRM! (Version: {0}; Org: {1}",   
    crmSvc.ConnectedOrgVersion, crmSvc.ConnectedOrgUniqueName);  
  
    // Update the account record  
    Dictionary<string, CrmDataTypeWrapper> updateData = new Dictionary<string, CrmDataTypeWrapper>();  
    updateData.Add("name", new CrmDataTypeWrapper("Updated Sample Account Name", CrmFieldType.String));  
    updateData.Add("address1_city", new CrmDataTypeWrapper("Boston", CrmFieldType.String));  
    updateData.Add("telephone1", new CrmDataTypeWrapper("555-0161", CrmFieldType.String));   
    bool updateAccountStatus = crmSvc.UpdateEntity("account","accountid",_accountId,updateData);  
  
    // Validate if the account record was updated successfully, and then display the updated information  
    if (updateAccountStatus == true)  
    {  
        Console.WriteLine("Updated the account details as follows:");  
        Dictionary<string, object> data = crmSvc.GetEntityDataById("account", accountId, null);  
        foreach (var pair in data)  
        {  
            if ((pair.Key == "name") || (pair.Key == "address1_city") || (pair.Key == "telephone1"))  
            {  
                Console.WriteLine(pair.Key.ToUpper() + ": " + pair.Value);  
            }  
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
  
## <a name="updatestateandstatusforentity"></a><span data-ttu-id="1263b-111">UpdateStateAndStatusForEntity</span><span class="sxs-lookup"><span data-stu-id="1263b-111">UpdateStateAndStatusForEntity</span></span> 
 
 <span data-ttu-id="1263b-112">This method is used to set the state of a record in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="1263b-112">This method is used to set the state of a record in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="1263b-113">For example, all records generally start in an “open” state.</span><span class="sxs-lookup"><span data-stu-id="1263b-113">For example, all records generally start in an “open” state.</span></span> <span data-ttu-id="1263b-114">The name of the state changes based on the kind of record, or even the developers choices.</span><span class="sxs-lookup"><span data-stu-id="1263b-114">The name of the state changes based on the kind of record, or even the developers choices.</span></span> <span data-ttu-id="1263b-115">A quote, for example, has several possible status and states, **Draft**, **Active**, **Close**, **Lost**, **Won**.</span><span class="sxs-lookup"><span data-stu-id="1263b-115">A quote, for example, has several possible status and states, **Draft**, **Active**, **Close**, **Lost**, **Won**.</span></span>  
  
> [!TIP]
>  <span data-ttu-id="1263b-116">You can use the OptionSets.cs file in the SDK\SampleCode\CS\HelperCode folder of the SDK download package to view and use the global option sets available for various entities in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="1263b-116">You can use the OptionSets.cs file in the SDK\SampleCode\CS\HelperCode folder of the SDK download package to view and use the global option sets available for various entities in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="1263b-117">For more information about global option sets, see [Customize Global Option Sets](../org-service/customize-global-option-sets.md).</span><span class="sxs-lookup"><span data-stu-id="1263b-117">For more information about global option sets, see [Customize Global Option Sets](../org-service/customize-global-option-sets.md).</span></span>  
  
 <span data-ttu-id="1263b-118">Updating the state of an entity requires that you know what the target state and status are, either by the names or IDs.</span><span class="sxs-lookup"><span data-stu-id="1263b-118">Updating the state of an entity requires that you know what the target state and status are, either by the names or IDs.</span></span> <span data-ttu-id="1263b-119">Both the names and the IDs can be found by querying the metadata for the entity and looking at the status and state fields.</span><span class="sxs-lookup"><span data-stu-id="1263b-119">Both the names and the IDs can be found by querying the metadata for the entity and looking at the status and state fields.</span></span> <span data-ttu-id="1263b-120">In this example, we will demonstrate how to set the status of an account record to **Inactive**.</span><span class="sxs-lookup"><span data-stu-id="1263b-120">In this example, we will demonstrate how to set the status of an account record to **Inactive**.</span></span>  
  
```csharp  
CrmServiceClient crmSvc = new CrmServiceClient(new System.Net.NetworkCredential("<UserName>", "<Password>", “<Domain>”),"<Server>", "<Port>", "<OrgName>");  
  
// Verify that you are connected  
if (crmSvc != null && crmSvc.IsReady)  
{   
    //Display the CRM version number and org name that you are connected to  
    Console.WriteLine("Connected to CRM! (Version: {0}; Org: {1}",  
    crmSvc.ConnectedOrgVersion, crmSvc.ConnectedOrgUniqueName);  
  
    // Here are the state and status code values  
    // statecode = 1 ( Inactive )   
    // statuscode = 2 ( Inactive )   
  
    crmSvc.UpdateStateAndStatusForEntity("account" , accountId , 1 , 2 );  
  
    // the same command using the second form of the method  
    crmSvc.UpdateStateAndStatusForEntity("account" , accountId , "Inactive" , "Inactive");  
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
  
### <a name="see-also"></a><span data-ttu-id="1263b-121">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1263b-121">See also</span></span>  

 <span data-ttu-id="1263b-122">[Sample: Quick start for XRM Tooling API](sample-quick-start-xrm-tooling-api.md) </span><span class="sxs-lookup"><span data-stu-id="1263b-122">[Sample: Quick start for XRM Tooling API](sample-quick-start-xrm-tooling-api.md) </span></span>  
 <span data-ttu-id="1263b-123">[Use XRM Tooling to connect to Dynamics 365 for Customer Engagement apps](use-crmserviceclient-constructors-connect.md) </span><span class="sxs-lookup"><span data-stu-id="1263b-123">[Use XRM Tooling to connect to Dynamics 365 for Customer Engagement apps](use-crmserviceclient-constructors-connect.md) </span></span>  
 <span data-ttu-id="1263b-124">[Use XRM Tooling API to execute actions in Dynamics 365 for Customer Engagement apps](use-xrm-tooling-execute-actions.md) </span><span class="sxs-lookup"><span data-stu-id="1263b-124">[Use XRM Tooling API to execute actions in Dynamics 365 for Customer Engagement apps](use-xrm-tooling-execute-actions.md) </span></span>  
 [<span data-ttu-id="1263b-125">Work with attribute metadata</span><span class="sxs-lookup"><span data-stu-id="1263b-125">Work with attribute metadata</span></span>](../org-service/work-attribute-metadata.md)
