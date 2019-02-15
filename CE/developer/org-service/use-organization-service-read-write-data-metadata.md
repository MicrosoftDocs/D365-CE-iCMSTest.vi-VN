---
title: Use the Organization Service to read and write data or metadata (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: IOrganizationService is the primary web service that accesses data and metadata for your organization. This web service contains the methods that you use to write code that uses all the data and metadata in Dynamics 365 for Customer Engagement
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 8c212d9c-cfd6-4dcb-9d11-04b7cb472dbc
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b8426038d0fc22a368571f754c6b4b1615fe14e4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386856"
---
# <a name="use-the-organization-service-to-read-and-write-data-or-metadata"></a><span data-ttu-id="806a5-104">Use the Organization Service to read and write data or metadata</span><span class="sxs-lookup"><span data-stu-id="806a5-104">Use the Organization Service to read and write data or metadata</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="806a5-105">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps, the primary web service that accesses data and metadata for your organization is <xref:Microsoft.Xrm.Sdk.IOrganizationService>.</span><span class="sxs-lookup"><span data-stu-id="806a5-105">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps, the primary web service that accesses data and metadata for your organization is <xref:Microsoft.Xrm.Sdk.IOrganizationService>.</span></span> <span data-ttu-id="806a5-106">This web service contains the methods that you use to write code that uses all the data and metadata in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="806a5-106">This web service contains the methods that you use to write code that uses all the data and metadata in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span></span>  
  
 <span data-ttu-id="806a5-107">To use the `IOrganizationService` web service, add a reference to the Microsoft.Xrm.Sdk.dll assembly to your [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] project.</span><span class="sxs-lookup"><span data-stu-id="806a5-107">To use the `IOrganizationService` web service, add a reference to the Microsoft.Xrm.Sdk.dll assembly to your [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] project.</span></span> <span data-ttu-id="806a5-108">To access the non-core xRM messages, add a reference to the Microsoft.Crm.Sdk.Proxy.dll assembly to your project also.</span><span class="sxs-lookup"><span data-stu-id="806a5-108">To access the non-core xRM messages, add a reference to the Microsoft.Crm.Sdk.Proxy.dll assembly to your project also.</span></span> <span data-ttu-id="806a5-109">Alternatively, add the service reference to your project.</span><span class="sxs-lookup"><span data-stu-id="806a5-109">Alternatively, add the service reference to your project.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="806a5-110">[Developer resources page](../developer-resources-page.md)</span><span class="sxs-lookup"><span data-stu-id="806a5-110">[Developer resources page](../developer-resources-page.md)</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="806a5-111">In This Section</span><span class="sxs-lookup"><span data-stu-id="806a5-111">In This Section</span></span>  
 [<span data-ttu-id="806a5-112">IOrganizationService Methods</span><span class="sxs-lookup"><span data-stu-id="806a5-112">IOrganizationService Methods</span></span>](organization-service-methods.md)  
  
 [<span data-ttu-id="806a5-113">Use Messages</span><span class="sxs-lookup"><span data-stu-id="806a5-113">Use Messages</span></span>](use-messages-request-response-classes-execute-method.md)  
  
 [<span data-ttu-id="806a5-114">Use Execute Multiple to Improve Performance</span><span class="sxs-lookup"><span data-stu-id="806a5-114">Use Execute Multiple to Improve Performance</span></span>](use-executemultiple-improve-performance-bulk-data-load.md)  
  
 [<span data-ttu-id="806a5-115">Microsoft.Xrm.Sdk Messages</span><span class="sxs-lookup"><span data-stu-id="806a5-115">Microsoft.Xrm.Sdk Messages</span></span>](xrm-messages-organization-service.md)  
  
 [<span data-ttu-id="806a5-116">Microsoft.Crm.Sdk Data Messages</span><span class="sxs-lookup"><span data-stu-id="806a5-116">Microsoft.Crm.Sdk Data Messages</span></span>](organization-service-messages.md)  
  
 [<span data-ttu-id="806a5-117">Perform specialized operations using Update</span><span class="sxs-lookup"><span data-stu-id="806a5-117">Perform specialized operations using Update</span></span>](perform-specialized-operations-using-update.md)  
  
 [<span data-ttu-id="806a5-118">IOrganizationService Entities</span><span class="sxs-lookup"><span data-stu-id="806a5-118">IOrganizationService Entities</span></span>](organization-service-entities.md)  
  
 [<span data-ttu-id="806a5-119">Sample: Execute Multiple Requests</span><span class="sxs-lookup"><span data-stu-id="806a5-119">Sample: Execute Multiple Requests</span></span>](sample-execute-multiple-requests.md)  
  
 [<span data-ttu-id="806a5-120">Sample: Execute multiple requests in transaction</span><span class="sxs-lookup"><span data-stu-id="806a5-120">Sample: Execute multiple requests in transaction</span></span>](sample-execute-multiple-requests-transaction.md)  
  
## <a name="related-sections"></a><span data-ttu-id="806a5-121">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="806a5-121">Related Sections</span></span>  
 [<span data-ttu-id="806a5-122">Use the Early Bound Entity Classes in Code</span><span class="sxs-lookup"><span data-stu-id="806a5-122">Use the Early Bound Entity Classes in Code</span></span>](use-early-bound-entity-classes-code.md)  
  
 [<span data-ttu-id="806a5-123">Use the Late Bound Entity Class in Code</span><span class="sxs-lookup"><span data-stu-id="806a5-123">Use the Late Bound Entity Class in Code</span></span>](use-late-bound-entity-class-code.md)  
  
 [<span data-ttu-id="806a5-124">Retrieve Data with Queries</span><span class="sxs-lookup"><span data-stu-id="806a5-124">Retrieve Data with Queries</span></span>](retrieve-data-queries-sdk-assemblies.md)  
  
 [<span data-ttu-id="806a5-125">Developing Custom Code</span><span class="sxs-lookup"><span data-stu-id="806a5-125">Developing Custom Code</span></span>](../extend-dynamics-365-server.md)  
  
 [<span data-ttu-id="806a5-126">Connecting to the Dynamics 365 for Customer Engagement apps Services - Authentication</span><span class="sxs-lookup"><span data-stu-id="806a5-126">Connecting to the Dynamics 365 for Customer Engagement apps Services - Authentication</span></span>](../authenticate-users.md)  
  
 [<span data-ttu-id="806a5-127">Discover the URL for your organization using the Organization Service</span><span class="sxs-lookup"><span data-stu-id="806a5-127">Discover the URL for your organization using the Organization Service</span></span>](discover-url-organization-organization-service.md)  
  
 [<span data-ttu-id="806a5-128">Quick Start: A Simple Program</span><span class="sxs-lookup"><span data-stu-id="806a5-128">Quick Start: A Simple Program</span></span>](../simple-program-web-services.md)
