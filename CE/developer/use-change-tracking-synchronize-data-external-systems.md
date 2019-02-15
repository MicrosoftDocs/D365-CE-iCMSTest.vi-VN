---
title: Use change tracking to synchronize data with external systems (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: The change tracking feature in Dynamics 365 for Customer Engagement apps provides a way to keep the data synchronized in a performant way by detecting what data has changed since the data was initially extracted or last synchronized
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 8a927ac0-29c3-4222-8137-36549a0dc660
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 37e0f6ba6534cd1c705ee0aba1b032889d9f1de7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388555"
---
# <a name="use-change-tracking-to-synchronize-data-with-external-systems"></a><span data-ttu-id="66a28-103">Use change tracking to synchronize data with external systems</span><span class="sxs-lookup"><span data-stu-id="66a28-103">Use change tracking to synchronize data with external systems</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="66a28-104">The change tracking feature in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement provides a way to keep the data synchronized in a performant way by detecting what data has changed since the data was initially extracted or last synchronized.</span><span class="sxs-lookup"><span data-stu-id="66a28-104">The change tracking feature in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement provides a way to keep the data synchronized in a performant way by detecting what data has changed since the data was initially extracted or last synchronized.</span></span> <span data-ttu-id="66a28-105">Previously, without this new feature, it was difficult to build a reliable and efficient mechanism to determine what records had changed in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="66a28-105">Previously, without this new feature, it was difficult to build a reliable and efficient mechanism to determine what records had changed in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="66a28-106">This topic discusses how to retrieve changes for an entity.</span><span class="sxs-lookup"><span data-stu-id="66a28-106">This topic discusses how to retrieve changes for an entity.</span></span>  
  
<a name="BKMK_enable"></a>   
## <a name="enable-change-tracking-for-an-entity"></a><span data-ttu-id="66a28-107">Enable change tracking for an entity</span><span class="sxs-lookup"><span data-stu-id="66a28-107">Enable change tracking for an entity</span></span>  

 <span data-ttu-id="66a28-108">Before retrieving the changes for an entity, make sure that the change tracking feature is enabled for that entity.</span><span class="sxs-lookup"><span data-stu-id="66a28-108">Before retrieving the changes for an entity, make sure that the change tracking feature is enabled for that entity.</span></span> <span data-ttu-id="66a28-109">This feature can be enabled by using the customization user interface (UI) or programmatically by setting the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.ChangeTrackingEnabled> property to `True`.</span><span class="sxs-lookup"><span data-stu-id="66a28-109">This feature can be enabled by using the customization user interface (UI) or programmatically by setting the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.ChangeTrackingEnabled> property to `True`.</span></span> <span data-ttu-id="66a28-110">Annotation `Org.OData.Capabilities.V1.ChangeTracking ` gets added to entity sets that have change tracking enabled.</span><span class="sxs-lookup"><span data-stu-id="66a28-110">Annotation `Org.OData.Capabilities.V1.ChangeTracking ` gets added to entity sets that have change tracking enabled.</span></span> <span data-ttu-id="66a28-111">To see annotations in entity metadata, do</span><span class="sxs-lookup"><span data-stu-id="66a28-111">To see annotations in entity metadata, do</span></span> 

 ```http 
 GET [Organization URI]/api/data/v9.0/$metadata?annotations=true
 ```
 <span data-ttu-id="66a28-112">Read more about metadata annotations on [Metadata annotations](webapi/web-api-types-operations.md#bkmk_metannot).</span><span class="sxs-lookup"><span data-stu-id="66a28-112">Read more about metadata annotations on [Metadata annotations](webapi/web-api-types-operations.md#bkmk_metannot).</span></span>
 
 <span data-ttu-id="66a28-113">For more information about using the customization user interface (UI), see [Enable change tracking to control data synchronization](https://technet.microsoft.com/library/3fa9c316-9dc9-4b28-9abf-43a3fce5b01d.aspx).</span><span class="sxs-lookup"><span data-stu-id="66a28-113">For more information about using the customization user interface (UI), see [Enable change tracking to control data synchronization](https://technet.microsoft.com/library/3fa9c316-9dc9-4b28-9abf-43a3fce5b01d.aspx).</span></span>  
  
<a name="BKMK_webapi"></a>   
## <a name="retrieve-changes-for-an-entity-using-the-web-api"></a><span data-ttu-id="66a28-114">Retrieve changes for an entity using the Web API</span><span class="sxs-lookup"><span data-stu-id="66a28-114">Retrieve changes for an entity using the Web API</span></span>  
<span data-ttu-id="66a28-115">Changes made in entities can be tracked using Web API requests by adding `odata.track-changes` as a preference header.</span><span class="sxs-lookup"><span data-stu-id="66a28-115">Changes made in entities can be tracked using Web API requests by adding `odata.track-changes` as a preference header.</span></span> <span data-ttu-id="66a28-116">Preference header `odata.track-changes` is used to request that a *delta link* be returned which can subsequently be used to retrieve entity changes.</span><span class="sxs-lookup"><span data-stu-id="66a28-116">Preference header `odata.track-changes` is used to request that a *delta link* be returned which can subsequently be used to retrieve entity changes.</span></span>

<span data-ttu-id="66a28-117">Delta links are opaque, service-generated links that the client uses to retrieve subsequent changes to a result.</span><span class="sxs-lookup"><span data-stu-id="66a28-117">Delta links are opaque, service-generated links that the client uses to retrieve subsequent changes to a result.</span></span> <span data-ttu-id="66a28-118">They are based on a defining query that describes the set of results for which changes are being tracked; for example, the request that generated the results containing the delta link.</span><span class="sxs-lookup"><span data-stu-id="66a28-118">They are based on a defining query that describes the set of results for which changes are being tracked; for example, the request that generated the results containing the delta link.</span></span> <span data-ttu-id="66a28-119">The delta link encodes the collection of entities for which changes are being tracked, along with a starting point from which to track changes.</span><span class="sxs-lookup"><span data-stu-id="66a28-119">The delta link encodes the collection of entities for which changes are being tracked, along with a starting point from which to track changes.</span></span> <span data-ttu-id="66a28-120">Read more about delta links here [Oasis OData Version 4.0 - Delta Links](http://docs.oasis-open.org/odata/odata/v4.0/cs01/part1-protocol/odata-v4.0-cs01-part1-protocol.html#_Toc365046305)</span><span class="sxs-lookup"><span data-stu-id="66a28-120">Read more about delta links here [Oasis OData Version 4.0 - Delta Links](http://docs.oasis-open.org/odata/odata/v4.0/cs01/part1-protocol/odata-v4.0-cs01-part1-protocol.html#_Toc365046305)</span></span>

<a name="BKMK_webapiexample"></a>   
## <a name="retrieve-changes-in-entities-using-web-api-example"></a><span data-ttu-id="66a28-121">Retrieve changes in entities using Web API example</span><span class="sxs-lookup"><span data-stu-id="66a28-121">Retrieve changes in entities using Web API example</span></span>

<span data-ttu-id="66a28-122">This example shows how to retrieve changes made in accounts data using the Web API.</span><span class="sxs-lookup"><span data-stu-id="66a28-122">This example shows how to retrieve changes made in accounts data using the Web API.</span></span>

<span data-ttu-id="66a28-123">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="66a28-123">Request</span></span>
```http
GET [Organization URI]/org1/api/data/v9.0/accounts?$select=name,accountnumber,telephone1,fax HTTP/1.1
Prefer: odata.track-changes
Cache-Control: no-cache
OData-Version: 4.0
Content-Type: application/json
```
<span data-ttu-id="66a28-124">Phản hồi</span><span class="sxs-lookup"><span data-stu-id="66a28-124">Response</span></span>
```json
{
  "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#accounts(name,accountnumber,telephone1,fax)",
"@odata.deltaLink": "[Organization URI]/api/data/v9.0/accounts?$select=name,accountnumber,telephone1,fax&$deltatoken=919042%2108%2f22%2f2017%2008%3a10%3a44",
"value":[
           {
              "@odata.etag":"W/\"915244\"",
              "name":"Monte Orton",
              "accountnumber":null,
              "telephone1":"555000",
              "fax":"10101",
              "accountid":"60c4e274-0d87-e711-80e5-00155db19e6d"
           }
       ]
}
```
<span data-ttu-id="66a28-125">The delta link returned from the above example can be used to fetch changes in entities.</span><span class="sxs-lookup"><span data-stu-id="66a28-125">The delta link returned from the above example can be used to fetch changes in entities.</span></span> <span data-ttu-id="66a28-126">In this example a new account was created and an existing account deleted.</span><span class="sxs-lookup"><span data-stu-id="66a28-126">In this example a new account was created and an existing account deleted.</span></span> <span data-ttu-id="66a28-127">The delta link returned from the previous request fetches these changes, as shown in the example below.</span><span class="sxs-lookup"><span data-stu-id="66a28-127">The delta link returned from the previous request fetches these changes, as shown in the example below.</span></span>

<span data-ttu-id="66a28-128">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="66a28-128">Request</span></span>
```http
GET [Organization URI]/api/data/v9.0/accounts?$select=name,accountnumber,telephone1,fax&$deltatoken=919042%2108%2f22%2f2017%2008%3a10%3a44
```
<span data-ttu-id="66a28-129">Phản hồi</span><span class="sxs-lookup"><span data-stu-id="66a28-129">Response</span></span>
```json
{
          "@odata.context":"[Organization URI]/data/v9.0/$metadata#accounts(name,telephone1,fax)/$delta",
          "@odata.deltaLink":"[Organization URI]/api/data/v9.0/accounts?$select=name,telephone1,fax&$deltatoken=919058%2108%2f22%2f2017%2008%3a21%3a20",
"value":
    [
        {
            "@odata.etag":"W/\"915244\"",
            "name":"Monte Orton",
            "telephone1":"555000",
            "fax":"10101",
            "accountid":"60c4e274-0d87-e711-80e5-00155db19e6d"
        },
        {
            "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#accounts/$deletedEntity",
            "id":"2e451703-c686-e711-80e5-00155db19e6d",
            "reason":"deleted"
        }
    ]
}
```
<span data-ttu-id="66a28-130">The response for the delta link returned in the initial change tracking request contains another delta link.</span><span class="sxs-lookup"><span data-stu-id="66a28-130">The response for the delta link returned in the initial change tracking request contains another delta link.</span></span> <span data-ttu-id="66a28-131">This delta link helps in retrieving all the subsequent changes in entities.</span><span class="sxs-lookup"><span data-stu-id="66a28-131">This delta link helps in retrieving all the subsequent changes in entities.</span></span> <span data-ttu-id="66a28-132">An empty JSON response is returned if no entity changes have occurred after the initial change tracking request was called.</span><span class="sxs-lookup"><span data-stu-id="66a28-132">An empty JSON response is returned if no entity changes have occurred after the initial change tracking request was called.</span></span>

<a name="bkmk_count"></a>
## <a name="retrieve-count-of-the-changes-made-in-entities-using-web-api"></a><span data-ttu-id="66a28-133">Retrieve count of the changes made in entities using Web API</span><span class="sxs-lookup"><span data-stu-id="66a28-133">Retrieve count of the changes made in entities using Web API</span></span>
<span data-ttu-id="66a28-134">`$count` can be added to the delta link returned from the initial change tracking request, as shown in the example below to get the number of changes made.</span><span class="sxs-lookup"><span data-stu-id="66a28-134">`$count` can be added to the delta link returned from the initial change tracking request, as shown in the example below to get the number of changes made.</span></span>

<span data-ttu-id="66a28-135">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="66a28-135">Request</span></span>
```http
GET [Organization URI]/api/data/v9.0/accounts/$count?$deltatoken=919042%2108%2f22%2f2017%2008%3a10%3a44
```

<a name="bkmk_unsupported"></a>
## <a name="query-options-not-supported-in-change-tracking-web-api-request"></a><span data-ttu-id="66a28-136">Query options not supported in Change Tracking Web API request</span><span class="sxs-lookup"><span data-stu-id="66a28-136">Query options not supported in Change Tracking Web API request</span></span>
<span data-ttu-id="66a28-137">System query options `$filter`, `$orderby` and `$top` are not supported when using `odata.track-changes` as header in Web API request.</span><span class="sxs-lookup"><span data-stu-id="66a28-137">System query options `$filter`, `$orderby` and `$top` are not supported when using `odata.track-changes` as header in Web API request.</span></span> <span data-ttu-id="66a28-138">An error message saying "The `$filter`/ `$orderby`/ `$top` query parameter isn't supported when Change Tracking is enabled."</span><span class="sxs-lookup"><span data-stu-id="66a28-138">An error message saying "The `$filter`/ `$orderby`/ `$top` query parameter isn't supported when Change Tracking is enabled."</span></span> <span data-ttu-id="66a28-139">gets returned when using these query options in the Web API request.</span><span class="sxs-lookup"><span data-stu-id="66a28-139">gets returned when using these query options in the Web API request.</span></span>

<a name="BKMK_retrieve"></a>   
## <a name="retrieve-changes-for-an-entity-using-the-organization-service"></a><span data-ttu-id="66a28-140">Retrieve changes for an entity using the Organization Service</span><span class="sxs-lookup"><span data-stu-id="66a28-140">Retrieve changes for an entity using the Organization Service</span></span>
 <span data-ttu-id="66a28-141">When change tracking is enabled for an entity, you can use the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveEntityChangesRequest> message to retrieve the changes for that entity.</span><span class="sxs-lookup"><span data-stu-id="66a28-141">When change tracking is enabled for an entity, you can use the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveEntityChangesRequest> message to retrieve the changes for that entity.</span></span> <span data-ttu-id="66a28-142">The first time this message is used it returns all records for the entity and that data can be used to populate the external storage.</span><span class="sxs-lookup"><span data-stu-id="66a28-142">The first time this message is used it returns all records for the entity and that data can be used to populate the external storage.</span></span> <span data-ttu-id="66a28-143">The message also returns a version number that will be sent back with the next use of the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveEntityChangesRequest> message so that only data for those changes that occurred since that version will be returned.</span><span class="sxs-lookup"><span data-stu-id="66a28-143">The message also returns a version number that will be sent back with the next use of the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveEntityChangesRequest> message so that only data for those changes that occurred since that version will be returned.</span></span>  
  
 <span data-ttu-id="66a28-144">You should be aware of the following constraints when retrieving changes for an entity:</span><span class="sxs-lookup"><span data-stu-id="66a28-144">You should be aware of the following constraints when retrieving changes for an entity:</span></span>  
  
- <span data-ttu-id="66a28-145">Only one entity will be tracked in retrieve changes.</span><span class="sxs-lookup"><span data-stu-id="66a28-145">Only one entity will be tracked in retrieve changes.</span></span> <span data-ttu-id="66a28-146">If retrieve changes is executed with no version / or token, the server will treat it as the system minimum version, returning all of the records as new.</span><span class="sxs-lookup"><span data-stu-id="66a28-146">If retrieve changes is executed with no version / or token, the server will treat it as the system minimum version, returning all of the records as new.</span></span> <span data-ttu-id="66a28-147">Deleted objects won’t be returned.</span><span class="sxs-lookup"><span data-stu-id="66a28-147">Deleted objects won’t be returned.</span></span>  
  
- <span data-ttu-id="66a28-148">Changes will be returned if the last token is within a default value of 90 days.</span><span class="sxs-lookup"><span data-stu-id="66a28-148">Changes will be returned if the last token is within a default value of 90 days.</span></span> <span data-ttu-id="66a28-149">If it is more than 90 days, the system will return all the records.</span><span class="sxs-lookup"><span data-stu-id="66a28-149">If it is more than 90 days, the system will return all the records.</span></span>  
  
- <span data-ttu-id="66a28-150">If a client has a set of changes for an entity, say version 1, a record is created and deleted prior to the next query for changes, they will get the deleted item even if they didn’t have the item to begin with.</span><span class="sxs-lookup"><span data-stu-id="66a28-150">If a client has a set of changes for an entity, say version 1, a record is created and deleted prior to the next query for changes, they will get the deleted item even if they didn’t have the item to begin with.</span></span>  
  
- <span data-ttu-id="66a28-151">Records are retrieved in the order determined by server side logic.</span><span class="sxs-lookup"><span data-stu-id="66a28-151">Records are retrieved in the order determined by server side logic.</span></span> <span data-ttu-id="66a28-152">Usually, the end user will always get all new or updated records first (sorted by version number) followed by deleted records.</span><span class="sxs-lookup"><span data-stu-id="66a28-152">Usually, the end user will always get all new or updated records first (sorted by version number) followed by deleted records.</span></span>  <span data-ttu-id="66a28-153">If there are 3000 records created or updated and 2000 records deleted, [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] returns a collection of 5000 records, which have the first 3000 entries comprised of new or updated records and the last 2000 entries for deleted records.</span><span class="sxs-lookup"><span data-stu-id="66a28-153">If there are 3000 records created or updated and 2000 records deleted, [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] returns a collection of 5000 records, which have the first 3000 entries comprised of new or updated records and the last 2000 entries for deleted records.</span></span>  
  
- <span data-ttu-id="66a28-154">If the new or updated item collection is greater than 5000, the user can page through the collection.</span><span class="sxs-lookup"><span data-stu-id="66a28-154">If the new or updated item collection is greater than 5000, the user can page through the collection.</span></span>  
  
<a name="BKMK_SampleCode"></a>   
## <a name="sample-code"></a><span data-ttu-id="66a28-155">Mã mẫu</span><span class="sxs-lookup"><span data-stu-id="66a28-155">Sample code</span></span>  
 <span data-ttu-id="66a28-156">The following code snippet shows how the `RetrieveEntityChangesRequest` message is used to retrieve the changes for an entity.</span><span class="sxs-lookup"><span data-stu-id="66a28-156">The following code snippet shows how the `RetrieveEntityChangesRequest` message is used to retrieve the changes for an entity.</span></span> <span data-ttu-id="66a28-157">For the complete sample, see [Synchronize data with external systems using change tracking](http://go.microsoft.com/fwlink/p/?LinkId=533957).</span><span class="sxs-lookup"><span data-stu-id="66a28-157">For the complete sample, see [Synchronize data with external systems using change tracking](http://go.microsoft.com/fwlink/p/?LinkId=533957).</span></span>  
  
 [!code-csharp[ChangeTrackingSample#ChangeTrackingSample1](../snippets/csharp/CRMV8/changetrackingsample/cs/changetrackingsample1.cs#changetrackingsample1)]  
  
### <a name="see-also"></a><span data-ttu-id="66a28-158">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="66a28-158">See also</span></span>  
 <span data-ttu-id="66a28-159">[Define alternate keys for an entity](define-alternate-keys-entity.md) </span><span class="sxs-lookup"><span data-stu-id="66a28-159">[Define alternate keys for an entity](define-alternate-keys-entity.md) </span></span>  
 <span data-ttu-id="66a28-160">[Using alternate keys](use-alternate-key-create-record.md) </span><span class="sxs-lookup"><span data-stu-id="66a28-160">[Using alternate keys](use-alternate-key-create-record.md) </span></span>  
 [<span data-ttu-id="66a28-161">Update Dynamics 365 for Customer Engagement apps with external data using Upsert</span><span class="sxs-lookup"><span data-stu-id="66a28-161">Update Dynamics 365 for Customer Engagement apps with external data using Upsert</span></span>](use-upsert-insert-update-record.md)
