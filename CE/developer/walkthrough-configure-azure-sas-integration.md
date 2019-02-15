---
title: 'Walkthrough: Configure Microsoft Azure (SAS) for integration with Dynamics 365 for Customer Engagement apps| MicrosoftDocs'
description: 'The walkthrough guides you through configuring the Azure Service Bus issuer, scope, and rules to allow a listener application to read the Dynamics 365 for Customer Engagement messages posted to the Azure Service Bus. '
ms.custom: ''
ms.date: 05/16/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1977e223-2d7b-4019-a584-e81d1b832785
caps.latest.revision: 8
author: JimDaly
ms.author: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2c404f519a29334e7bdb3c27db4beaa3f509112b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387899"
---
# <a name="walkthrough-configure-azure-sas-for-integration-with-customer-engagement-apps"></a><span data-ttu-id="e71bf-103">Walkthrough: Configure Azure (SAS) for integration with Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="e71bf-103">Walkthrough: Configure Azure (SAS) for integration with Customer Engagement apps</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e71bf-104">This walkthrough guides you through configuring the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] issuer, scope, and rules to allow a listener application to read the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement messages posted to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span><span class="sxs-lookup"><span data-stu-id="e71bf-104">This walkthrough guides you through configuring the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] issuer, scope, and rules to allow a listener application to read the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement messages posted to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e71bf-105">This walkthrough applies to any [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] deployment when using SAS authorization for [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)]-[!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] messaging.</span><span class="sxs-lookup"><span data-stu-id="e71bf-105">This walkthrough applies to any [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] deployment when using SAS authorization for [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)]-[!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] messaging.</span></span> [!INCLUDE[sdk_for_more_info_about](../includes/sdk-for-more-info-about.md)]<span data-ttu-id="e71bf-106">[!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] authorization see [Service Bus authentication and authorization](https://azure.microsoft.com/en-us/documentation/articles/service-bus-authentication-and-authorization/).</span><span class="sxs-lookup"><span data-stu-id="e71bf-106">[!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] authorization see [Service Bus authentication and authorization](https://azure.microsoft.com/en-us/documentation/articles/service-bus-authentication-and-authorization/).</span></span>  
> 
> <span data-ttu-id="e71bf-107">You must use the Plug-in Registration Tool.</span><span class="sxs-lookup"><span data-stu-id="e71bf-107">You must use the Plug-in Registration Tool.</span></span> <span data-ttu-id="e71bf-108">To download the plug-in registration tool, see [Download tools from NuGet](download-tools-NuGet.md).</span><span class="sxs-lookup"><span data-stu-id="e71bf-108">To download the plug-in registration tool, see [Download tools from NuGet](download-tools-NuGet.md).</span></span>
  
## <a name="prerequisites"></a><span data-ttu-id="e71bf-109">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="e71bf-109">Prerequisites</span></span>  
  
- <span data-ttu-id="e71bf-110">An [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] account with a license to create Service Bus entities.</span><span class="sxs-lookup"><span data-stu-id="e71bf-110">An [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] account with a license to create Service Bus entities.</span></span>  
  
- <span data-ttu-id="e71bf-111">A SAS configured service bus namespace.</span><span class="sxs-lookup"><span data-stu-id="e71bf-111">A SAS configured service bus namespace.</span></span>  
  
- <span data-ttu-id="e71bf-112">A SAS configured service bus messaging entity: queue, topic, relay, or event hub.</span><span class="sxs-lookup"><span data-stu-id="e71bf-112">A SAS configured service bus messaging entity: queue, topic, relay, or event hub.</span></span>  
  
- <span data-ttu-id="e71bf-113">The messaging entity must have the `Send` policy permission at a minimum.</span><span class="sxs-lookup"><span data-stu-id="e71bf-113">The messaging entity must have the `Send` policy permission at a minimum.</span></span> <span data-ttu-id="e71bf-114">For a two-way relay, the policy must also have the `Listen` permission.</span><span class="sxs-lookup"><span data-stu-id="e71bf-114">For a two-way relay, the policy must also have the `Listen` permission.</span></span>  
- <span data-ttu-id="e71bf-115">The authorization connection string of your messaging entity.</span><span class="sxs-lookup"><span data-stu-id="e71bf-115">The authorization connection string of your messaging entity.</span></span> 
  
  <span data-ttu-id="e71bf-116">![Define the Azure policy permissions](media/policy-permissions.png "Define the Azure policy permissions")</span><span class="sxs-lookup"><span data-stu-id="e71bf-116">![Define the Azure policy permissions](media/policy-permissions.png "Define the Azure policy permissions")</span></span>  
  
  <span data-ttu-id="e71bf-117">Refer to the [Create a Service Bus namespace using the Azure portal](/azure/service-bus-messaging/service-bus-create-namespace-portal) for instructions on how to create a Service Bus namespace and messaging entity.</span><span class="sxs-lookup"><span data-stu-id="e71bf-117">Refer to the [Create a Service Bus namespace using the Azure portal](/azure/service-bus-messaging/service-bus-create-namespace-portal) for instructions on how to create a Service Bus namespace and messaging entity.</span></span>  
  
## <a name="create-a-service-endpoint"></a><span data-ttu-id="e71bf-118">Create a service endpoint</span><span class="sxs-lookup"><span data-stu-id="e71bf-118">Create a service endpoint</span></span>  
 <span data-ttu-id="e71bf-119">A [ServiceEndpoint Entity ](entities/serviceendpoint.md) contains configuration data that is required for external messaging with a [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] solution endpoint.</span><span class="sxs-lookup"><span data-stu-id="e71bf-119">A [ServiceEndpoint Entity ](entities/serviceendpoint.md) contains configuration data that is required for external messaging with a [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] solution endpoint.</span></span> <span data-ttu-id="e71bf-120">By using the Plug-in Registration Tool, you can easily create a service endpoint entity in a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] organization and configure  the service bus endpoint issuer, scope, and rules.</span><span class="sxs-lookup"><span data-stu-id="e71bf-120">By using the Plug-in Registration Tool, you can easily create a service endpoint entity in a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] organization and configure  the service bus endpoint issuer, scope, and rules.</span></span>  
  
### <a name="register-a-service-endpoint"></a><span data-ttu-id="e71bf-121">Register a Service Endpoint</span><span class="sxs-lookup"><span data-stu-id="e71bf-121">Register a Service Endpoint</span></span>  
  
1. <span data-ttu-id="e71bf-122">Run the Plug-in Registration Tool and log into your target [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] organization.</span><span class="sxs-lookup"><span data-stu-id="e71bf-122">Run the Plug-in Registration Tool and log into your target [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] organization.</span></span>  
  
2. <span data-ttu-id="e71bf-123">Select **Register > Register New Service Endpoint**.</span><span class="sxs-lookup"><span data-stu-id="e71bf-123">Select **Register > Register New Service Endpoint**.</span></span>  
  
3. <span data-ttu-id="e71bf-124">Check **Let's Start with the connection string from the Azure Service Bus Portal** and paste the connection string of your service bus messaging entity.</span><span class="sxs-lookup"><span data-stu-id="e71bf-124">Check **Let's Start with the connection string from the Azure Service Bus Portal** and paste the connection string of your service bus messaging entity.</span></span>  
  
   <span data-ttu-id="e71bf-125">![Provide authorization connection string](media/sas-connection-string.PNG "Provide authorization connection string")</span><span class="sxs-lookup"><span data-stu-id="e71bf-125">![Provide authorization connection string](media/sas-connection-string.PNG "Provide authorization connection string")</span></span>  
  
4. <span data-ttu-id="e71bf-126">Chọn **Tiếp theo**.</span><span class="sxs-lookup"><span data-stu-id="e71bf-126">Select **Next**.</span></span>  
  
5. <span data-ttu-id="e71bf-127">Fill out the **Service Endpoint Registration** form by entering the **Designation Type**, **Message Format**, and optionally the **User Information Sent** and **Description** fields</span><span class="sxs-lookup"><span data-stu-id="e71bf-127">Fill out the **Service Endpoint Registration** form by entering the **Designation Type**, **Message Format**, and optionally the **User Information Sent** and **Description** fields</span></span>  
  
   <span data-ttu-id="e71bf-128">![Service endpoint registration](media/service-endpoint-registration.PNG "Service endpoint registration")</span><span class="sxs-lookup"><span data-stu-id="e71bf-128">![Service endpoint registration](media/service-endpoint-registration.PNG "Service endpoint registration")</span></span>  
  
   <span data-ttu-id="e71bf-129">For more information about the message format, see [Write a listener application for a Azure solution](write-listener-application-azure-solution.md).</span><span class="sxs-lookup"><span data-stu-id="e71bf-129">For more information about the message format, see [Write a listener application for a Azure solution](write-listener-application-azure-solution.md).</span></span>  
  
6. <span data-ttu-id="e71bf-130">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="e71bf-130">Select **Save**.</span></span>  
  
7. <span data-ttu-id="e71bf-131">After a few seconds or so, you will see the new service endpoint in the **Registered Plug-ins & Custom Workflow Activities** list.</span><span class="sxs-lookup"><span data-stu-id="e71bf-131">After a few seconds or so, you will see the new service endpoint in the **Registered Plug-ins & Custom Workflow Activities** list.</span></span>  
  
   <span data-ttu-id="e71bf-132">![New service endpoint](media/new-service-endpoint.PNG "New service endpoint")</span><span class="sxs-lookup"><span data-stu-id="e71bf-132">![New service endpoint](media/new-service-endpoint.PNG "New service endpoint")</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e71bf-133">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e71bf-133">See also</span></span>  
 <span data-ttu-id="e71bf-134">[Azure extensions for Dynamics 365 for Customer Engagement apps](azure-extensions.md) </span><span class="sxs-lookup"><span data-stu-id="e71bf-134">[Azure extensions for Dynamics 365 for Customer Engagement apps](azure-extensions.md) </span></span>  
 [<span data-ttu-id="e71bf-135">Azure Service Bus</span><span class="sxs-lookup"><span data-stu-id="e71bf-135">Azure Service Bus</span></span>](/azure/service-bus-messaging/service-bus-fundamentals-hybrid-solutions)
