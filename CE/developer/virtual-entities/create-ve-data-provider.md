---
title: Create a virtual entity data provider (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d329dade-16c5-46e9-8dec-4b8efb996d01
author: jimdaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d8a1ab94bedd9306158f57d711fdc3c61c917509
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385478"
---
# <a name="create-a-virtual-entity-data-provider"></a><span data-ttu-id="10bb3-102">Create a virtual entity data provider</span><span class="sxs-lookup"><span data-stu-id="10bb3-102">Create a virtual entity data provider</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="10bb3-103">There are two general categories of data provider you can create using the virtual entity data SDK assemblies: generic or targeted.</span><span class="sxs-lookup"><span data-stu-id="10bb3-103">There are two general categories of data provider you can create using the virtual entity data SDK assemblies: generic or targeted.</span></span>

|<span data-ttu-id="10bb3-104">Danh mục</span><span class="sxs-lookup"><span data-stu-id="10bb3-104">Category</span></span> |<span data-ttu-id="10bb3-105">Mô tả</span><span class="sxs-lookup"><span data-stu-id="10bb3-105">Description</span></span>|
|---------|-----------|
|<span data-ttu-id="10bb3-106"> Chung</span><span class="sxs-lookup"><span data-stu-id="10bb3-106">Generic</span></span> | <span data-ttu-id="10bb3-107">These providers understand how to use the Dynamics 365 for Customer Engagement metadata and the service documents for your external data to translate Dynamics 365 for Customer Engagement queries to the appropriate query for these services.</span><span class="sxs-lookup"><span data-stu-id="10bb3-107">These providers understand how to use the Dynamics 365 for Customer Engagement metadata and the service documents for your external data to translate Dynamics 365 for Customer Engagement queries to the appropriate query for these services.</span></span> <span data-ttu-id="10bb3-108">With this kind of data provider, the integration can be achieved without writing any code, but these the most complex kind of data provider to create.</span><span class="sxs-lookup"><span data-stu-id="10bb3-108">With this kind of data provider, the integration can be achieved without writing any code, but these the most complex kind of data provider to create.</span></span> <span data-ttu-id="10bb3-109">The Odata v4 and Azure DocumentDB data providers provided by Dynamics 365 for Customer Engagement are re-usable generic providers.</span><span class="sxs-lookup"><span data-stu-id="10bb3-109">The Odata v4 and Azure DocumentDB data providers provided by Dynamics 365 for Customer Engagement are re-usable generic providers.</span></span>|
|<span data-ttu-id="10bb3-110">Targeted</span><span class="sxs-lookup"><span data-stu-id="10bb3-110">Targeted</span></span> |<span data-ttu-id="10bb3-111">Rather than attempt to create a generic data provider, you can use your domain knowledge of Dynamics 365 for Customer Engagement and your external data to create a data provider which only attempts to provide a solution to the limited scope of this specific solution.</span><span class="sxs-lookup"><span data-stu-id="10bb3-111">Rather than attempt to create a generic data provider, you can use your domain knowledge of Dynamics 365 for Customer Engagement and your external data to create a data provider which only attempts to provide a solution to the limited scope of this specific solution.</span></span>|
| | |

<span data-ttu-id="10bb3-112">Because virtual entities in this release are read-only, you will write the data provider in the form of a plugin registered on the **Retrieve** and **RetrieveMultiple** events.</span><span class="sxs-lookup"><span data-stu-id="10bb3-112">Because virtual entities in this release are read-only, you will write the data provider in the form of a plugin registered on the **Retrieve** and **RetrieveMultiple** events.</span></span> <span data-ttu-id="10bb3-113">Each respective event will include information in the execution context which describe the kind of data to return.</span><span class="sxs-lookup"><span data-stu-id="10bb3-113">Each respective event will include information in the execution context which describe the kind of data to return.</span></span> 

|<span data-ttu-id="10bb3-114">Sự kiện</span><span class="sxs-lookup"><span data-stu-id="10bb3-114">Event</span></span> |<span data-ttu-id="10bb3-115">Execution Context</span><span class="sxs-lookup"><span data-stu-id="10bb3-115">Execution Context</span></span>|
|------|-----------------|
|<span data-ttu-id="10bb3-116">**Truy xuất**</span><span class="sxs-lookup"><span data-stu-id="10bb3-116">**Retrieve**</span></span>|<span data-ttu-id="10bb3-117">Describes which entity to retrieve as well as the attributes and any related entities to include.</span><span class="sxs-lookup"><span data-stu-id="10bb3-117">Describes which entity to retrieve as well as the attributes and any related entities to include.</span></span>|
|<span data-ttu-id="10bb3-118">**RetrieveMultiple**</span><span class="sxs-lookup"><span data-stu-id="10bb3-118">**RetrieveMultiple**</span></span>|<span data-ttu-id="10bb3-119">A [QueryExpression](https://msdn.microsoft.com/library/microsoft.xrm.sdk.query.queryexpression.aspx) object defining the query</span><span class="sxs-lookup"><span data-stu-id="10bb3-119">A [QueryExpression](https://msdn.microsoft.com/library/microsoft.xrm.sdk.query.queryexpression.aspx) object defining the query</span></span>|
| | |

<span data-ttu-id="10bb3-120">For both events, you must :</span><span class="sxs-lookup"><span data-stu-id="10bb3-120">For both events, you must :</span></span>
1. <span data-ttu-id="10bb3-121">Convert the respective information in the execution context into a query that will work for your external data source.</span><span class="sxs-lookup"><span data-stu-id="10bb3-121">Convert the respective information in the execution context into a query that will work for your external data source.</span></span>
2. <span data-ttu-id="10bb3-122">Retrieve the data from the external system.</span><span class="sxs-lookup"><span data-stu-id="10bb3-122">Retrieve the data from the external system.</span></span>
3. <span data-ttu-id="10bb3-123">Convert the data into either an [Entity](https://msdn.microsoft.com/library/microsoft.xrm.sdk.entity.aspx) or [EntityCollection](https://msdn.microsoft.com/library/microsoft.xrm.sdk.entitycollection.aspx) to be returned through the Dynamics 365 for Customer Engagement platform to the user executing the query.</span><span class="sxs-lookup"><span data-stu-id="10bb3-123">Convert the data into either an [Entity](https://msdn.microsoft.com/library/microsoft.xrm.sdk.entity.aspx) or [EntityCollection](https://msdn.microsoft.com/library/microsoft.xrm.sdk.entitycollection.aspx) to be returned through the Dynamics 365 for Customer Engagement platform to the user executing the query.</span></span>  
<span data-ttu-id="10bb3-124">If for any reason your code cannot achieve the expected result, you must throw the appropriate error.</span><span class="sxs-lookup"><span data-stu-id="10bb3-124">If for any reason your code cannot achieve the expected result, you must throw the appropriate error.</span></span> <span data-ttu-id="10bb3-125">The virtual entity data SDK provides a set of specific errors you can throw.</span><span class="sxs-lookup"><span data-stu-id="10bb3-125">The virtual entity data SDK provides a set of specific errors you can throw.</span></span>

<span data-ttu-id="10bb3-126">The virtual entity data SDK provides a framework you can use to map the Dynamics 365 for Customer Engagement query information from the execution context into a query in the format appropriate for your external data source.</span><span class="sxs-lookup"><span data-stu-id="10bb3-126">The virtual entity data SDK provides a framework you can use to map the Dynamics 365 for Customer Engagement query information from the execution context into a query in the format appropriate for your external data source.</span></span> <span data-ttu-id="10bb3-127">The same framework will help you convert the data returned in to the appropriate **Entity** or **EntityCollection** types expected by the Dynamics 365 for Customer Engagement platform.</span><span class="sxs-lookup"><span data-stu-id="10bb3-127">The same framework will help you convert the data returned in to the appropriate **Entity** or **EntityCollection** types expected by the Dynamics 365 for Customer Engagement platform.</span></span>

<span data-ttu-id="10bb3-128">Unlike an ordinary plugin, you will only use the Plugin Registration Tool (PRT) to register the assembly and the plugins for each event.</span><span class="sxs-lookup"><span data-stu-id="10bb3-128">Unlike an ordinary plugin, you will only use the Plugin Registration Tool (PRT) to register the assembly and the plugins for each event.</span></span> <span data-ttu-id="10bb3-129">You will not register specific steps.</span><span class="sxs-lookup"><span data-stu-id="10bb3-129">You will not register specific steps.</span></span> <span data-ttu-id="10bb3-130">Your plugin will run in stage 30, the main core transaction stage for the operation that is not available for ordinary plugin steps.</span><span class="sxs-lookup"><span data-stu-id="10bb3-130">Your plugin will run in stage 30, the main core transaction stage for the operation that is not available for ordinary plugin steps.</span></span> <span data-ttu-id="10bb3-131">Instead of registering steps, you will configure your data provider using the [EntityDataProvider](../entities/entitydataprovider.md) and [EntityDataSource](../entities/entitydatasource.md) entities.</span><span class="sxs-lookup"><span data-stu-id="10bb3-131">Instead of registering steps, you will configure your data provider using the [EntityDataProvider](../entities/entitydataprovider.md) and [EntityDataSource](../entities/entitydatasource.md) entities.</span></span> 

|<span data-ttu-id="10bb3-132">Thực thể</span><span class="sxs-lookup"><span data-stu-id="10bb3-132">Entity</span></span> |<span data-ttu-id="10bb3-133">Descrption</span><span class="sxs-lookup"><span data-stu-id="10bb3-133">Descrption</span></span>|
|-----|-----|
|<span data-ttu-id="10bb3-134">**EntityDataProvider**</span><span class="sxs-lookup"><span data-stu-id="10bb3-134">**EntityDataProvider**</span></span>|<span data-ttu-id="10bb3-135">Defines the plugins to use for each event and the logical name of the data source.</span><span class="sxs-lookup"><span data-stu-id="10bb3-135">Defines the plugins to use for each event and the logical name of the data source.</span></span>|
|<span data-ttu-id="10bb3-136">**EntityDataSource**</span><span class="sxs-lookup"><span data-stu-id="10bb3-136">**EntityDataSource**</span></span>|<span data-ttu-id="10bb3-137">Provides the entity and any connection information required for the external data source, including any secrets required to authenticate.</span><span class="sxs-lookup"><span data-stu-id="10bb3-137">Provides the entity and any connection information required for the external data source, including any secrets required to authenticate.</span></span>|
| | |

<span data-ttu-id="10bb3-138">When the metadata for your virtual entity is configured, your plugins are registered using the PRT and the correct configuration data is set in the **EntityDataProvider** and **EntityDataSource** entities, your virtual entity will start to respond to requests.</span><span class="sxs-lookup"><span data-stu-id="10bb3-138">When the metadata for your virtual entity is configured, your plugins are registered using the PRT and the correct configuration data is set in the **EntityDataProvider** and **EntityDataSource** entities, your virtual entity will start to respond to requests.</span></span>


