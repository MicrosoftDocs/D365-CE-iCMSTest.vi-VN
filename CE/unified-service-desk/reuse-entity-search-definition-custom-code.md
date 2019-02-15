---
title: Reuse Entity Search definition in your custom code for Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Replacement parameters can be used throughout the application to pull data from data elements (called data parameters) captured during the execution of the application that augment and include the Unified Service Desk context.
ms.custom:
- dyn365-USD
ms.date: 08/23/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 082c58d0-3719-4150-935a-fe85ff6c1c9f
caps.latest.revision: 10
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 3fad0a1cffa9aee1271386a510edf60d96485ae9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386666"
---
# <a name="reuse-entity-search-definition-in-your-custom-code"></a><span data-ttu-id="c64ad-103">Reuse Entity Search definition in your custom code</span><span class="sxs-lookup"><span data-stu-id="c64ad-103">Reuse Entity Search definition in your custom code</span></span>
<span data-ttu-id="c64ad-104">Entity search in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] is exposed as a service for developers so that they can programmatically use an existing entity search definition in their custom code to search [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps data.</span><span class="sxs-lookup"><span data-stu-id="c64ad-104">Entity search in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] is exposed as a service for developers so that they can programmatically use an existing entity search definition in their custom code to search [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps data.</span></span> <span data-ttu-id="c64ad-105">Entity searches in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] use FetchXML to query the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps web services to return data.</span><span class="sxs-lookup"><span data-stu-id="c64ad-105">Entity searches in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] use FetchXML to query the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps web services to return data.</span></span> <span data-ttu-id="c64ad-106">For information about defining entity searches, see [Search data using entity searches in Unified Service Desk](../unified-service-desk/search-data-entity-searches.md).</span><span class="sxs-lookup"><span data-stu-id="c64ad-106">For information about defining entity searches, see [Search data using entity searches in Unified Service Desk](../unified-service-desk/search-data-entity-searches.md).</span></span>  
  
 <span data-ttu-id="c64ad-107">When you set up an entity search, you can choose whether to return an entire search result set or page the FetchXML results for large datasets by using a paging cookie for faster performance.</span><span class="sxs-lookup"><span data-stu-id="c64ad-107">When you set up an entity search, you can choose whether to return an entire search result set or page the FetchXML results for large datasets by using a paging cookie for faster performance.</span></span> <span data-ttu-id="c64ad-108">For more information about using paging cookie with FetchXML, see [Page large result sets with FetchXML](https://msdn.microsoft.com/library/gg309717.aspx).</span><span class="sxs-lookup"><span data-stu-id="c64ad-108">For more information about using paging cookie with FetchXML, see [Page large result sets with FetchXML](https://msdn.microsoft.com/library/gg309717.aspx).</span></span>  
  
 <span data-ttu-id="c64ad-109">Since you use an entity search name in your code to return data and not its FetchXML definition, updating the underlying FetchXML query definition of the entity search in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] without changing the entity search name ensures that you won’t have to update your custom control code, recompile, and redistribute it on the client computers.</span><span class="sxs-lookup"><span data-stu-id="c64ad-109">Since you use an entity search name in your code to return data and not its FetchXML definition, updating the underlying FetchXML query definition of the entity search in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] without changing the entity search name ensures that you won’t have to update your custom control code, recompile, and redistribute it on the client computers.</span></span>  
  
 <span data-ttu-id="c64ad-110">Use the new [EntitySearchRequest](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchrequest) message to construct a request, and then pass the request as parameter to the [EntitySearchService](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchservice).[EntitySearchResponse})](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchservice.getentitysearchresults\(microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchrequest,system.action{microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchresponse}\)) method to get the response ([EntitySearchResponse](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchresponse)).</span><span class="sxs-lookup"><span data-stu-id="c64ad-110">Use the new [EntitySearchRequest](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchrequest) message to construct a request, and then pass the request as parameter to the [EntitySearchService](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchservice).[EntitySearchResponse})](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchservice.getentitysearchresults\(microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchrequest,system.action{microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchresponse}\)) method to get the response ([EntitySearchResponse](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchresponse)).</span></span>  
  
<a name="Request"></a>   
## <a name="create-an-entitysearchrequest-object"></a><span data-ttu-id="c64ad-111">Create an EntitySearchRequest object</span><span class="sxs-lookup"><span data-stu-id="c64ad-111">Create an EntitySearchRequest object</span></span>  
 <span data-ttu-id="c64ad-112">The [EntitySearchRequest](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchrequest) message is overloaded, and you must use any of the following three constructors to create a request object depending how you want the records to be returned.</span><span class="sxs-lookup"><span data-stu-id="c64ad-112">The [EntitySearchRequest](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchrequest) message is overloaded, and you must use any of the following three constructors to create a request object depending how you want the records to be returned.</span></span> <span data-ttu-id="c64ad-113">Creating a request object without using one of these three constructors is not supported.</span><span class="sxs-lookup"><span data-stu-id="c64ad-113">Creating a request object without using one of these three constructors is not supported.</span></span> <span data-ttu-id="c64ad-114">Before using an entity search name in the request object, ensure that the entity search is already defined in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] on your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="c64ad-114">Before using an entity search name in the request object, ensure that the entity search is already defined in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] on your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span></span>  
  
-   <span data-ttu-id="c64ad-115">Create a request object using just the entity search name.</span><span class="sxs-lookup"><span data-stu-id="c64ad-115">Create a request object using just the entity search name.</span></span> <span data-ttu-id="c64ad-116">Use this constructor to return all the records as a result of the entity search.</span><span class="sxs-lookup"><span data-stu-id="c64ad-116">Use this constructor to return all the records as a result of the entity search.</span></span>  
  
    ```csharp  
    EntitySearchRequest mySearchRequest = new EntitySearchRequest(string entitySearchName);  
    ```  
  
-   <span data-ttu-id="c64ad-117">Create a request object using the entity search name and the maximum count of the records to be returned.</span><span class="sxs-lookup"><span data-stu-id="c64ad-117">Create a request object using the entity search name and the maximum count of the records to be returned.</span></span> <span data-ttu-id="c64ad-118">Use this constructor to limit the number of records returned as a result of the entity search.</span><span class="sxs-lookup"><span data-stu-id="c64ad-118">Use this constructor to limit the number of records returned as a result of the entity search.</span></span>  
  
    ```csharp  
    EntitySearchRequest mySearchRequest = new EntitySearchRequest(string entitySearchName, int maxCount);  
    ```  
  
    > [!TIP]
    >  <span data-ttu-id="c64ad-119">Specify 0 for the `maxCount` parameter to return all the records.</span><span class="sxs-lookup"><span data-stu-id="c64ad-119">Specify 0 for the `maxCount` parameter to return all the records.</span></span>  
  
-   <span data-ttu-id="c64ad-120">Create a request object using the entity search name, page count, page number, and paging cookie.</span><span class="sxs-lookup"><span data-stu-id="c64ad-120">Create a request object using the entity search name, page count, page number, and paging cookie.</span></span> <span data-ttu-id="c64ad-121">Use this constructor to return large datasets in pages for faster performance.</span><span class="sxs-lookup"><span data-stu-id="c64ad-121">Use this constructor to return large datasets in pages for faster performance.</span></span>  
  
     <span data-ttu-id="c64ad-122">The `pageCount` parameter defines the number of records to return per page.</span><span class="sxs-lookup"><span data-stu-id="c64ad-122">The `pageCount` parameter defines the number of records to return per page.</span></span> <span data-ttu-id="c64ad-123">The `pageNumber` parameter defines the page number of the result set to return the data.</span><span class="sxs-lookup"><span data-stu-id="c64ad-123">The `pageNumber` parameter defines the page number of the result set to return the data.</span></span> <span data-ttu-id="c64ad-124">For example, if your query returns 500 records, you can specify `pageCount` as **50** to return 50 records in a page, which implies that you’ll have 10 pages of data (50 records \* 10 pages = 500).</span><span class="sxs-lookup"><span data-stu-id="c64ad-124">For example, if your query returns 500 records, you can specify `pageCount` as **50** to return 50 records in a page, which implies that you’ll have 10 pages of data (50 records \* 10 pages = 500).</span></span> <span data-ttu-id="c64ad-125">Now, if you want to return records 100-150, specify the `pageNumber` value as 3.</span><span class="sxs-lookup"><span data-stu-id="c64ad-125">Now, if you want to return records 100-150, specify the `pageNumber` value as 3.</span></span> <span data-ttu-id="c64ad-126">You must specify `pageCookie` as `empty` to retrieve the first page of the result set.</span><span class="sxs-lookup"><span data-stu-id="c64ad-126">You must specify `pageCookie` as `empty` to retrieve the first page of the result set.</span></span>  
  
    ```csharp  
    EntitySearchRequest mySearchRequest = new EntitySearchRequest(string entitySearchName, int pageCount, int pageNumber, string pageCookie);  
    ```  
  
    > [!NOTE]
    >  <span data-ttu-id="c64ad-127">When you execute the request object using this constructor to retrieve results in pages, the [EntitySearchResponse](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchresponse).[HasMoreRecords](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchresponse.hasmorerecords) property of the response object indicates if there are more records (value=1).</span><span class="sxs-lookup"><span data-stu-id="c64ad-127">When you execute the request object using this constructor to retrieve results in pages, the [EntitySearchResponse](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchresponse).[HasMoreRecords](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchresponse.hasmorerecords) property of the response object indicates if there are more records (value=1).</span></span> <span data-ttu-id="c64ad-128">Also, the value of the [EntitySearchResponse](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchresponse).[PageCookie](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchresponse.pagecookie) property is set to the paging cookie returned from current results.</span><span class="sxs-lookup"><span data-stu-id="c64ad-128">Also, the value of the [EntitySearchResponse](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchresponse).[PageCookie](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchresponse.pagecookie) property is set to the paging cookie returned from current results.</span></span>  
  
<a name="Execute"></a>   
## <a name="execute-the-request-object"></a><span data-ttu-id="c64ad-129">Execute the request object</span><span class="sxs-lookup"><span data-stu-id="c64ad-129">Execute the request object</span></span>  
 <span data-ttu-id="c64ad-130">Use the [EntitySearchService](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchservice).[EntitySearchResponse})](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchservice.getentitysearchresults\(microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchrequest,system.action{microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchresponse}\)) method to execute the request object created as described in the previous section.</span><span class="sxs-lookup"><span data-stu-id="c64ad-130">Use the [EntitySearchService](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchservice).[EntitySearchResponse})](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchservice.getentitysearchresults\(microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchrequest,system.action{microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchresponse}\)) method to execute the request object created as described in the previous section.</span></span> <span data-ttu-id="c64ad-131">This method executes the [EntitySearchRequest](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchrequest) object, and returns a [EntitySearchResponse](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchresponse) object with the entity search results.</span><span class="sxs-lookup"><span data-stu-id="c64ad-131">This method executes the [EntitySearchRequest](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchrequest) object, and returns a [EntitySearchResponse](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.entitysearch.entitysearchresponse) object with the entity search results.</span></span>  
  
 <span data-ttu-id="c64ad-132">The following code sample demonstrates how you can reuse an existing entity search to retrieve results in pages.</span><span class="sxs-lookup"><span data-stu-id="c64ad-132">The following code sample demonstrates how you can reuse an existing entity search to retrieve results in pages.</span></span>  
  
```csharp  
// Define parameters for the entity search request object.  
string entitySearchName = "Sample Entity Search"; // Name of the entity search record defined in Unified Service Desk  
int pageCount = 10; // Retrieve 10 records per page.  
int pageNumber = 0;  
string pageCookie = String.Empty; // Retrieve the first page of the result set.  
  
var entityService = AifServiceContainer.Instance.GetService<IEntitySearchService>();  
  
// Create a request object.  
EntitySearchRequest entitySearchRequest = new EntitySearchRequest(searchName, pageCount, pageNumber, pageCookie);  
  
bool hasMoreRecords = true;  
  
while (hasMoreRecords)  
{  
   entityService.GetEntitySearchResults(entitySearchRequest, (entitySearchResponse) =>  
   {  
      foreach (Entity e in entitySearchResponse.Entities)  
      {  
         Console.WriteLine("Entity with id:\"{0}\" retrieved", e.Id);  
      }  
      if (entitySearchResponse.HasMoreRecords)  
      {  
         pageNumber++;  
         pageCookie = entitySearchResponse.PageCookie;  
         entitySearchRequest = new EntitySearchRequest(searchName, pageCount, pageNumber, pageCookie);  
      }  
      else  
      {  
         hasMoreRecords = false;  
      }  
   });  
}  
```  
  
### <a name="see-also"></a><span data-ttu-id="c64ad-133">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c64ad-133">See also</span></span>  
 <span data-ttu-id="c64ad-134">[Tìm kiếm dữ liệu bằng cách sử dụng tìm kiếm thực thể trong Unified Service Desk](../unified-service-desk/search-data-entity-searches.md) </span><span class="sxs-lookup"><span data-stu-id="c64ad-134">[Search data using entity searches in Unified Service Desk](../unified-service-desk/search-data-entity-searches.md) </span></span>  
 [<span data-ttu-id="c64ad-135">DoSearch</span><span class="sxs-lookup"><span data-stu-id="c64ad-135">DoSearch</span></span>](../unified-service-desk/global-manager-hosted-control.md#DoSearch)
