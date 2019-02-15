---
title: Work with Dynamics 365 for Customer Engagement apps data using web resources (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: This doc explains how you can use JavaScript web resources to access Dynamics 365 for Customer Engagement (online) data from within the application.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: f1a0de36-a963-43c9-a878-c85c793cd089
caps.latest.revision: 28
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c4c62be8c0d412c308f7d310935fdca37ca3be15
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385856"
---
# <a name="work-with-customer-engagement-apps-data-using-web-resources"></a><span data-ttu-id="cc23e-103">Work with Customer Engagement apps data using web resources</span><span class="sxs-lookup"><span data-stu-id="cc23e-103">Work with Customer Engagement apps data using web resources</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="cc23e-104">You can use [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] web resources to access [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] data from within the application.</span><span class="sxs-lookup"><span data-stu-id="cc23e-104">You can use [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] web resources to access [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] data from within the application.</span></span> <span data-ttu-id="cc23e-105">There are three web services you can use in the application to access data by using [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)].</span><span class="sxs-lookup"><span data-stu-id="cc23e-105">There are three web services you can use in the application to access data by using [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)].</span></span> <span data-ttu-id="cc23e-106">The Organization data service is deprecated with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="cc23e-106">The Organization data service is deprecated with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="cc23e-107">It is recommended to use Web API instead of Organization service when creating applications that connect to the [!INCLUDE[cc_dyn365_ce_web_services](../includes/cc-dyn365-ce-web-services.md)] and invoke methods to perform common business data operations like create, delete, update, and find.</span><span class="sxs-lookup"><span data-stu-id="cc23e-107">It is recommended to use Web API instead of Organization service when creating applications that connect to the [!INCLUDE[cc_dyn365_ce_web_services](../includes/cc-dyn365-ce-web-services.md)] and invoke methods to perform common business data operations like create, delete, update, and find.</span></span>    


|                                                         <span data-ttu-id="cc23e-108">Dịch vụ Web</span><span class="sxs-lookup"><span data-stu-id="cc23e-108">Web Service</span></span>                                                          |                                                                                                                                                                                                                                                                                                          <span data-ttu-id="cc23e-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="cc23e-109">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                                         <span data-ttu-id="cc23e-110">**API Web**</span><span class="sxs-lookup"><span data-stu-id="cc23e-110">**Web API**</span></span>                                                          |                                   <span data-ttu-id="cc23e-111">The Web API was introduced with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="cc23e-111">The Web API was introduced with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="cc23e-112">It provides a RESTful web service with full compatibility with the organization service.</span><span class="sxs-lookup"><span data-stu-id="cc23e-112">It provides a RESTful web service with full compatibility with the organization service.</span></span> <span data-ttu-id="cc23e-113">It uses JSON in the body of the HTTP requests and responses, which makes it very suitable for use with [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)].</span><span class="sxs-lookup"><span data-stu-id="cc23e-113">It uses JSON in the body of the HTTP requests and responses, which makes it very suitable for use with [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="cc23e-114">[Get started with the Web API (client-side JavaScript)](webapi/get-started-web-api-client-side-javascript.md)</span><span class="sxs-lookup"><span data-stu-id="cc23e-114">[Get started with the Web API (client-side JavaScript)](webapi/get-started-web-api-client-side-javascript.md)</span></span>                                    |
|      <span data-ttu-id="cc23e-115">**Dịch vụ dữ liệu tổ chức**</span><span class="sxs-lookup"><span data-stu-id="cc23e-115">**Organization Data Service**</span></span><br /><br /> <span data-ttu-id="cc23e-116">Also known as the “OData endpoint” or “REST endpoint for web resources.”</span><span class="sxs-lookup"><span data-stu-id="cc23e-116">Also known as the “OData endpoint” or “REST endpoint for web resources.”</span></span>      | <span data-ttu-id="cc23e-117">The organization data service is deprecated with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="cc23e-117">The organization data service is deprecated with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="cc23e-118">Use the Web API to access [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] data for solutions that don’t need to work with earlier versions.</span><span class="sxs-lookup"><span data-stu-id="cc23e-118">Use the Web API to access [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] data for solutions that don’t need to work with earlier versions.</span></span> <span data-ttu-id="cc23e-119">The organization data service remains available and you can use it so that code written for earlier versions will continue to work.</span><span class="sxs-lookup"><span data-stu-id="cc23e-119">The organization data service remains available and you can use it so that code written for earlier versions will continue to work.</span></span> <span data-ttu-id="cc23e-120">For more information, see the [!INCLUDE[pn_crm_2015](../includes/pn-crm-2015.md)] SDK topic: [Use the OData endpoint with web resources](https://msdn.microsoft.com/library/gg334279\(v=crm.7\).aspx).</span><span class="sxs-lookup"><span data-stu-id="cc23e-120">For more information, see the [!INCLUDE[pn_crm_2015](../includes/pn-crm-2015.md)] SDK topic: [Use the OData endpoint with web resources](https://msdn.microsoft.com/library/gg334279\(v=crm.7\).aspx).</span></span> |
| <span data-ttu-id="cc23e-121">**Organization service**</span><span class="sxs-lookup"><span data-stu-id="cc23e-121">**Organization service**</span></span><br /><br /> <span data-ttu-id="cc23e-122">Also known as the “Modern app SOAP endpoint” and the “SOAP endpoint for web resources.”</span><span class="sxs-lookup"><span data-stu-id="cc23e-122">Also known as the “Modern app SOAP endpoint” and the “SOAP endpoint for web resources.”</span></span> |                                                           <span data-ttu-id="cc23e-123">The organization service can be used but it is much more complex than the Web API with [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] because the HTTP requests and responses are sent using XML, which must conform to specific schema and namespaces.</span><span class="sxs-lookup"><span data-stu-id="cc23e-123">The organization service can be used but it is much more complex than the Web API with [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] because the HTTP requests and responses are sent using XML, which must conform to specific schema and namespaces.</span></span> <span data-ttu-id="cc23e-124">For more information, see the [!INCLUDE[pn_crm_2015](../includes/pn-crm-2015.md)] SDK topic: [Use the Modern app SOAP endpoint for modern applications with web resources](https://msdn.microsoft.com/library/gg490657\(v=crm.7\).aspx).</span><span class="sxs-lookup"><span data-stu-id="cc23e-124">For more information, see the [!INCLUDE[pn_crm_2015](../includes/pn-crm-2015.md)] SDK topic: [Use the Modern app SOAP endpoint for modern applications with web resources](https://msdn.microsoft.com/library/gg490657\(v=crm.7\).aspx).</span></span>                                                            |

 <span data-ttu-id="cc23e-125">Each of these web services can use the authentication provided by the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] application within web resources without the need to include any code to implement authentication.</span><span class="sxs-lookup"><span data-stu-id="cc23e-125">Each of these web services can use the authentication provided by the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] application within web resources without the need to include any code to implement authentication.</span></span> <span data-ttu-id="cc23e-126">For information about how to use these endpoints with authentication from outside the application, see [Write mobile and modern apps](../developer/write-mobile-modern-apps.md).</span><span class="sxs-lookup"><span data-stu-id="cc23e-126">For information about how to use these endpoints with authentication from outside the application, see [Write mobile and modern apps](../developer/write-mobile-modern-apps.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="cc23e-127">In This Section</span><span class="sxs-lookup"><span data-stu-id="cc23e-127">In This Section</span></span>  

## <a name="related-sections"></a><span data-ttu-id="cc23e-128">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="cc23e-128">Related Sections</span></span>  
 [<span data-ttu-id="cc23e-129">Get started with the Web API (client-side JavaScript)</span><span class="sxs-lookup"><span data-stu-id="cc23e-129">Get started with the Web API (client-side JavaScript)</span></span>](webapi/get-started-web-api-client-side-javascript.md)  

 [<span data-ttu-id="cc23e-130">Extend Dynamics 365 for Customer Engagement on the client</span><span class="sxs-lookup"><span data-stu-id="cc23e-130">Extend Dynamics 365 for Customer Engagement on the client</span></span>](extend-client.md)  

 [<span data-ttu-id="cc23e-131">Use JavaScript with Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="cc23e-131">Use JavaScript with Dynamics 365 for Customer Engagement apps</span></span>](use-javascript.md)  

 [<span data-ttu-id="cc23e-132">Client scripting in Customer Engagement apps using JavaScript</span><span class="sxs-lookup"><span data-stu-id="cc23e-132">Client scripting in Customer Engagement apps using JavaScript</span></span>](clientapi/client-scripting.md)  

 [<span data-ttu-id="cc23e-133">Open Forms, Views, Dialogs and Reports with a URL</span><span class="sxs-lookup"><span data-stu-id="cc23e-133">Open Forms, Views, Dialogs and Reports with a URL</span></span>](open-forms-views-dialogs-reports-url.md)  

 [<span data-ttu-id="cc23e-134">Open forms, views, and dashboards in Dynamics 365 for Customer Engagement mobile client with a URL</span><span class="sxs-lookup"><span data-stu-id="cc23e-134">Open forms, views, and dashboards in Dynamics 365 for Customer Engagement mobile client with a URL</span></span>](open-forms-views-dashboards-mobile-client-url.md)  

 [<span data-ttu-id="cc23e-135">Web Resources for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="cc23e-135">Web Resources for Dynamics 365 for Customer Engagement apps</span></span>](web-resources.md)  

 [<span data-ttu-id="cc23e-136">Client scripting in Customer Engagement apps using JavaScript</span><span class="sxs-lookup"><span data-stu-id="cc23e-136">Client scripting in Customer Engagement apps using JavaScript</span></span>](clientapi/client-scripting.md)  

 [<span data-ttu-id="cc23e-137">Client API Reference</span><span class="sxs-lookup"><span data-stu-id="cc23e-137">Client API Reference</span></span>](clientapi/reference.md)