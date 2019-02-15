---
title: Open forms, views, and dashboards in Dynamics 365 for Customer Engagement apps mobile client with a URL (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Use the new application handler for Dynamics 365 for Customer Engagement apps mobile clients to directly link to Dynamics 365 for Customer Engagement forms, views, and dashboards from external applications so that when you click on the link in an external application, the target element opens in Dynamics 365 for phones or Dynamics 365 for tablets.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 5286807a-bca0-4d01-b08d-0fe4d56a3758
caps.latest.revision: 7
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e7f5ac6a2d26605e4b465a6407c1f45c079bd7ed
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388300"
---
# <a name="open-forms-views-and-dashboards-in-customer-engagement-mobile-client-with-a-url"></a><span data-ttu-id="70d37-103">Open forms, views, and dashboards in Customer Engagement mobile client with a URL</span><span class="sxs-lookup"><span data-stu-id="70d37-103">Open forms, views, and dashboards in Customer Engagement mobile client with a URL</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="70d37-104">Use the new application handler for [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps mobile clients to directly link to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps forms, views, and dashboards from external applications so that when you click on the link in an external application, the target element opens in [!INCLUDE[pn_Mobile_Express_short](../includes/pn-mobile-express-short.md)] apps or [!INCLUDE[pn_moca_short](../includes/pn-moca-short.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="70d37-104">Use the new application handler for [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps mobile clients to directly link to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps forms, views, and dashboards from external applications so that when you click on the link in an external application, the target element opens in [!INCLUDE[pn_Mobile_Express_short](../includes/pn-mobile-express-short.md)] apps or [!INCLUDE[pn_moca_short](../includes/pn-moca-short.md)] apps.</span></span> <span data-ttu-id="70d37-105">You can also open an empty form for creating an entity record.</span><span class="sxs-lookup"><span data-stu-id="70d37-105">You can also open an empty form for creating an entity record.</span></span>  
  
 <span data-ttu-id="70d37-106">If you are already signed in to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance in [!INCLUDE[pn_Mobile_Express_short](../includes/pn-mobile-express-short.md)] or [!INCLUDE[pn_moca_short](../includes/pn-moca-short.md)], the target record is displayed in the mobile client when you click the link in external application.</span><span class="sxs-lookup"><span data-stu-id="70d37-106">If you are already signed in to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance in [!INCLUDE[pn_Mobile_Express_short](../includes/pn-mobile-express-short.md)] or [!INCLUDE[pn_moca_short](../includes/pn-moca-short.md)], the target record is displayed in the mobile client when you click the link in external application.</span></span> <span data-ttu-id="70d37-107">Otherwise, you’re prompted to sign in to your Dynamics 365 for Customer Engagement apps instance in the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps mobile client, and upon doing so, the target element is displayed.</span><span class="sxs-lookup"><span data-stu-id="70d37-107">Otherwise, you’re prompted to sign in to your Dynamics 365 for Customer Engagement apps instance in the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps mobile client, and upon doing so, the target element is displayed.</span></span> <span data-ttu-id="70d37-108">You must have [!INCLUDE[pn_Mobile_Express_short](../includes/pn-mobile-express-short.md)] or [!INCLUDE[pn_moca_short](../includes/pn-moca-short.md)] installed on your mobile device to use this feature.</span><span class="sxs-lookup"><span data-stu-id="70d37-108">You must have [!INCLUDE[pn_Mobile_Express_short](../includes/pn-mobile-express-short.md)] or [!INCLUDE[pn_moca_short](../includes/pn-moca-short.md)] installed on your mobile device to use this feature.</span></span>  
  
<a name="Parameters"></a>

## <a name="query-string-parameters-for-the-url"></a><span data-ttu-id="70d37-109">Query string parameters for the URL</span><span class="sxs-lookup"><span data-stu-id="70d37-109">Query string parameters for the URL</span></span>

 <span data-ttu-id="70d37-110">Use the following application handler and query string parameters to compose the URL.</span><span class="sxs-lookup"><span data-stu-id="70d37-110">Use the following application handler and query string parameters to compose the URL.</span></span>  
  
```  
ms-dynamicsxrm://?pagetype=<VALUE>&etn=<VALUE>&id=<VALUE>  
```  
  
 <span data-ttu-id="70d37-111">The query string parameters shown in the following table are used.</span><span class="sxs-lookup"><span data-stu-id="70d37-111">The query string parameters shown in the following table are used.</span></span>  
  
|<span data-ttu-id="70d37-112">Query string parameter</span><span class="sxs-lookup"><span data-stu-id="70d37-112">Query string parameter</span></span>|<span data-ttu-id="70d37-113">Mô tả</span><span class="sxs-lookup"><span data-stu-id="70d37-113">Description</span></span>|  
|----------------------------|-----------------|  
|<span data-ttu-id="70d37-114">pagetype</span><span class="sxs-lookup"><span data-stu-id="70d37-114">pagetype</span></span>|<span data-ttu-id="70d37-115">Specify the page type to open.</span><span class="sxs-lookup"><span data-stu-id="70d37-115">Specify the page type to open.</span></span> <span data-ttu-id="70d37-116">Valid values are `entity`, `view`, `dashboard`, and `create`.</span><span class="sxs-lookup"><span data-stu-id="70d37-116">Valid values are `entity`, `view`, `dashboard`, and `create`.</span></span><br /><br /> <span data-ttu-id="70d37-117">This parameter is required.</span><span class="sxs-lookup"><span data-stu-id="70d37-117">This parameter is required.</span></span>|  
|<span data-ttu-id="70d37-118">etn</span><span class="sxs-lookup"><span data-stu-id="70d37-118">etn</span></span>|<span data-ttu-id="70d37-119">Specify the logical name of the entity for which you want to open or create a record.</span><span class="sxs-lookup"><span data-stu-id="70d37-119">Specify the logical name of the entity for which you want to open or create a record.</span></span>  <span data-ttu-id="70d37-120">Logical name of entities are in lowercase, and defined in the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.LogicalName></span><span class="sxs-lookup"><span data-stu-id="70d37-120">Logical name of entities are in lowercase, and defined in the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.LogicalName></span></span> <span data-ttu-id="70d37-121">property.</span><span class="sxs-lookup"><span data-stu-id="70d37-121">property.</span></span><br /><br /> <span data-ttu-id="70d37-122">This parameter is required if the `pagetype` parameter is set to `entity`, `view`, or `create`.</span><span class="sxs-lookup"><span data-stu-id="70d37-122">This parameter is required if the `pagetype` parameter is set to `entity`, `view`, or `create`.</span></span>|  
|<span data-ttu-id="70d37-123">ID</span><span class="sxs-lookup"><span data-stu-id="70d37-123">id</span></span>|<span data-ttu-id="70d37-124">Specify the ID of the entity, view, or dashboard record that you want to open.</span><span class="sxs-lookup"><span data-stu-id="70d37-124">Specify the ID of the entity, view, or dashboard record that you want to open.</span></span><br /><br /> <span data-ttu-id="70d37-125">This parameter is required if the `pagetype` parameter is set to `entity` or `dashboard`.</span><span class="sxs-lookup"><span data-stu-id="70d37-125">This parameter is required if the `pagetype` parameter is set to `entity` or `dashboard`.</span></span><br /><br /> <span data-ttu-id="70d37-126">It is optional if the `pagetype` parameter is set to `view`.</span><span class="sxs-lookup"><span data-stu-id="70d37-126">It is optional if the `pagetype` parameter is set to `view`.</span></span> <span data-ttu-id="70d37-127">If you do not specify the view ID, the default view for the entity specified in the `etn` parameter is displayed.</span><span class="sxs-lookup"><span data-stu-id="70d37-127">If you do not specify the view ID, the default view for the entity specified in the `etn` parameter is displayed.</span></span>|  
  
<a name="Example"></a>

## <a name="example-urls"></a><span data-ttu-id="70d37-128">Example URLs</span><span class="sxs-lookup"><span data-stu-id="70d37-128">Example URLs</span></span>

 <span data-ttu-id="70d37-129">Here are some example URLs for opening forms, views, and dashboards.</span><span class="sxs-lookup"><span data-stu-id="70d37-129">Here are some example URLs for opening forms, views, and dashboards.</span></span>  
  
|<span data-ttu-id="70d37-130">Hành động</span><span class="sxs-lookup"><span data-stu-id="70d37-130">Action</span></span>|<span data-ttu-id="70d37-131">Example URL</span><span class="sxs-lookup"><span data-stu-id="70d37-131">Example URL</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="70d37-132">Open an account entity with account record ID as 91330924-802A-4B0D-A900-34FD9D790829</span><span class="sxs-lookup"><span data-stu-id="70d37-132">Open an account entity with account record ID as 91330924-802A-4B0D-A900-34FD9D790829</span></span>|`ms-dynamicsxrm://?pagetype=entity&etn=account&id=91330924-802A-4B0D-A900-34FD9D790829`|  
|<span data-ttu-id="70d37-133">Open a view with the view record ID as 899D4FCF-F4D3-E011-9D26-00155DBA3819 for the contact entity</span><span class="sxs-lookup"><span data-stu-id="70d37-133">Open a view with the view record ID as 899D4FCF-F4D3-E011-9D26-00155DBA3819 for the contact entity</span></span>|`ms-dynamicsxrm://?pagetype=view&etn=contact&id=899D4FCF-F4D3-E011-9D26-00155DBA3819`|  
|<span data-ttu-id="70d37-134">Open a default view for the account entity</span><span class="sxs-lookup"><span data-stu-id="70d37-134">Open a default view for the account entity</span></span>|`ms-dynamicsxrm://?pagetype=view&etn=account`|  
|<span data-ttu-id="70d37-135">Open a dashboard with the dashboard record ID as 2E3D0841-FA6D-DF11-986C-00155D2E3002</span><span class="sxs-lookup"><span data-stu-id="70d37-135">Open a dashboard with the dashboard record ID as 2E3D0841-FA6D-DF11-986C-00155D2E3002</span></span>|`ms-dynamicsxrm://?pagetype=dashboard&id=2E3D0841-FA6D-DF11-986C-00155D2E3002`|  
|<span data-ttu-id="70d37-136">Open a form for creating an account record</span><span class="sxs-lookup"><span data-stu-id="70d37-136">Open a form for creating an account record</span></span>|`ms-dynamicsxrm://?pagetype=create&etn=account`|  
  
### <a name="see-also"></a><span data-ttu-id="70d37-137">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="70d37-137">See also</span></span>

 [<span data-ttu-id="70d37-138">Open Forms, Views, Dialogs and Reports with a URL</span><span class="sxs-lookup"><span data-stu-id="70d37-138">Open Forms, Views, Dialogs and Reports with a URL</span></span>](open-forms-views-dialogs-reports-url.md)  
    
 [<span data-ttu-id="70d37-139">Extend Dynamics 365 for Customer Engagement apps on the client</span><span class="sxs-lookup"><span data-stu-id="70d37-139">Extend Dynamics 365 for Customer Engagement apps on the client</span></span>](extend-client.md)
