---
title: Discover the URL for your organization using the Web API (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Learn how you can use the Web API to discover at runtime the organizations, or instances that the logged-on user belongs to
ms.custom: ''
ms.date: 09/30/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 2db13b4e-0e7c-4f25-b7be-70a612fb96e2
caps.latest.revision: 18
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7b9d6c3ac3c0867c856c0c170f56cf345b8a351e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386770"
---
# <a name="discover-the-url-for-your-organization-using-the-web-api"></a><span data-ttu-id="380af-103">Discover the URL for your organization using the Web API</span><span class="sxs-lookup"><span data-stu-id="380af-103">Discover the URL for your organization using the Web API</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="380af-104">The Discovery service for the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps Web API enables your applications to determine at run-time the organizations, also known as *instances*, that the logged-on user belongs to.</span><span class="sxs-lookup"><span data-stu-id="380af-104">The Discovery service for the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps Web API enables your applications to determine at run-time the organizations, also known as *instances*, that the logged-on user belongs to.</span></span>  <span data-ttu-id="380af-105">You can retrieve detailed information about those instances like the instance service URL, the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] release version, the instance ID and more.</span><span class="sxs-lookup"><span data-stu-id="380af-105">You can retrieve detailed information about those instances like the instance service URL, the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] release version, the instance ID and more.</span></span> <span data-ttu-id="380af-106">You can use standard `$filter` and `$select` parameters to a Web API service request to customize the  returned list of instance data.</span><span class="sxs-lookup"><span data-stu-id="380af-106">You can use standard `$filter` and `$select` parameters to a Web API service request to customize the  returned list of instance data.</span></span> <span data-ttu-id="380af-107">The Discovery service is supported by all [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] deployment types: Online, on-premises, and IFD.</span><span class="sxs-lookup"><span data-stu-id="380af-107">The Discovery service is supported by all [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] deployment types: Online, on-premises, and IFD.</span></span>  
  
<span data-ttu-id="380af-108">Clients applications may need access to a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance where the instance URL may change over time.</span><span class="sxs-lookup"><span data-stu-id="380af-108">Clients applications may need access to a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance where the instance URL may change over time.</span></span>  <span data-ttu-id="380af-109">For example, when a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance is moved from one [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps datacenter to another.</span><span class="sxs-lookup"><span data-stu-id="380af-109">For example, when a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance is moved from one [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps datacenter to another.</span></span> <span data-ttu-id="380af-110">The Discovery service allows clients instance to persist the instance ID or instance unique name and then use the Discovery service to look-up the current instance access URL.</span><span class="sxs-lookup"><span data-stu-id="380af-110">The Discovery service allows clients instance to persist the instance ID or instance unique name and then use the Discovery service to look-up the current instance access URL.</span></span>  
  
<span data-ttu-id="380af-111">In addition to datacenter specific Discovery services, that are available on the 2011 (SOAP) endpoint and through the Web API, there is also a Web API only global Discovery service that spans all operational datacenters.</span><span class="sxs-lookup"><span data-stu-id="380af-111">In addition to datacenter specific Discovery services, that are available on the 2011 (SOAP) endpoint and through the Web API, there is also a Web API only global Discovery service that spans all operational datacenters.</span></span> <span data-ttu-id="380af-112">For more information about the Discovery service on the 2011 endpoint see [Discover the URL for your organization using the Organization Service](../org-service/discover-url-organization-organization-service.md).</span><span class="sxs-lookup"><span data-stu-id="380af-112">For more information about the Discovery service on the 2011 endpoint see [Discover the URL for your organization using the Organization Service](../org-service/discover-url-organization-organization-service.md).</span></span>  
  
## <a name="information-provided-by-the-discovery-service"></a><span data-ttu-id="380af-113">Information provided by the Discovery service</span><span class="sxs-lookup"><span data-stu-id="380af-113">Information provided by the Discovery service</span></span>

<span data-ttu-id="380af-114">Organization information is stored in the `Instance` entity of the Discovery service.</span><span class="sxs-lookup"><span data-stu-id="380af-114">Organization information is stored in the `Instance` entity of the Discovery service.</span></span>  <span data-ttu-id="380af-115">To see the kind of information contained in that entity, send an HTTP GET request to the service for one of your instances.</span><span class="sxs-lookup"><span data-stu-id="380af-115">To see the kind of information contained in that entity, send an HTTP GET request to the service for one of your instances.</span></span>  
  
```http  
GET https://globaldisco.crm.dynamics.com/api/discovery/v1.0/Instances(UniqueName='myorg')  
```  
  
<span data-ttu-id="380af-116">In the above example, the global Discovery service of [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps is used to obtain the organization information of the instance with a unique name of "myorg".</span><span class="sxs-lookup"><span data-stu-id="380af-116">In the above example, the global Discovery service of [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps is used to obtain the organization information of the instance with a unique name of "myorg".</span></span> <span data-ttu-id="380af-117">More details about this request is expanded upon later in this topic.</span><span class="sxs-lookup"><span data-stu-id="380af-117">More details about this request is expanded upon later in this topic.</span></span>  
  
### <a name="scope-of-the-returned-information"></a><span data-ttu-id="380af-118">Scope of the returned information</span><span class="sxs-lookup"><span data-stu-id="380af-118">Scope of the returned information</span></span>

<span data-ttu-id="380af-119">For the global Discovery service, the `Instances` entity set, returns the set of instances that the user has access to across all geographies, when no filters are applied.</span><span class="sxs-lookup"><span data-stu-id="380af-119">For the global Discovery service, the `Instances` entity set, returns the set of instances that the user has access to across all geographies, when no filters are applied.</span></span>   <span data-ttu-id="380af-120">The returned data has a scope as described below.</span><span class="sxs-lookup"><span data-stu-id="380af-120">The returned data has a scope as described below.</span></span>  
  
-   <span data-ttu-id="380af-121">Includes all instances in the commercial cloud where the user is provisioned and enabled, except sovereign clouds instances are not returned</span><span class="sxs-lookup"><span data-stu-id="380af-121">Includes all instances in the commercial cloud where the user is provisioned and enabled, except sovereign clouds instances are not returned</span></span>  
  
-   <span data-ttu-id="380af-122">Does not  include instances where the user's account is disabled</span><span class="sxs-lookup"><span data-stu-id="380af-122">Does not  include instances where the user's account is disabled</span></span>  
  
-   <span data-ttu-id="380af-123">Does not include instances where users have been filtered out based on an instance security group</span><span class="sxs-lookup"><span data-stu-id="380af-123">Does not include instances where users have been filtered out based on an instance security group</span></span>  
  
-   <span data-ttu-id="380af-124">Does not include instances where the user has access as a result of being a delegated administrator</span><span class="sxs-lookup"><span data-stu-id="380af-124">Does not include instances where the user has access as a result of being a delegated administrator</span></span>  
  
-   <span data-ttu-id="380af-125">If the calling user has access to no instances, the response simply returns an empty list</span><span class="sxs-lookup"><span data-stu-id="380af-125">If the calling user has access to no instances, the response simply returns an empty list</span></span>  
  
## <a name="how-to-access-the-discovery-services"></a><span data-ttu-id="380af-126">How to access the Discovery services</span><span class="sxs-lookup"><span data-stu-id="380af-126">How to access the Discovery services</span></span>

<span data-ttu-id="380af-127">In general, the Web API address of the Discovery service has the following format: `<service base address>/api/discovery/`.</span><span class="sxs-lookup"><span data-stu-id="380af-127">In general, the Web API address of the Discovery service has the following format: `<service base address>/api/discovery/`.</span></span>  <span data-ttu-id="380af-128">The addresses for  each deployment type are identified below.</span><span class="sxs-lookup"><span data-stu-id="380af-128">The addresses for  each deployment type are identified below.</span></span> <span data-ttu-id="380af-129">You can easily  find the Web API addresses and version number for your deployment in the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] web application by navigating to **Settings > Customization > Developer Resources**</span><span class="sxs-lookup"><span data-stu-id="380af-129">You can easily  find the Web API addresses and version number for your deployment in the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] web application by navigating to **Settings > Customization > Developer Resources**</span></span>  
  
### <a name="includepndynamicscrmonlineincludespn-dynamics-crm-onlinemd-discovery-services"></a>[!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] <span data-ttu-id="380af-130">Discovery services</span><span class="sxs-lookup"><span data-stu-id="380af-130">Discovery services</span></span>

<span data-ttu-id="380af-131">The service base address of the global Discovery service is : `https://globaldisco.crm.dynamics.com/`.</span><span class="sxs-lookup"><span data-stu-id="380af-131">The service base address of the global Discovery service is : `https://globaldisco.crm.dynamics.com/`.</span></span> <span data-ttu-id="380af-132">This results in the service address of `https://globaldisco.crm.dynamics.com/api/discovery/`.</span><span class="sxs-lookup"><span data-stu-id="380af-132">This results in the service address of `https://globaldisco.crm.dynamics.com/api/discovery/`.</span></span>  
  
<span data-ttu-id="380af-133">The service base address of the Discovery service for a datacenter is : `https://disco.crm[N].dynamics.com/`.</span><span class="sxs-lookup"><span data-stu-id="380af-133">The service base address of the Discovery service for a datacenter is : `https://disco.crm[N].dynamics.com/`.</span></span> <span data-ttu-id="380af-134">This results in the Discovery service address of `https://disco.crm[N].dynamics.com/api/discovery/`.</span><span class="sxs-lookup"><span data-stu-id="380af-134">This results in the Discovery service address of `https://disco.crm[N].dynamics.com/api/discovery/`.</span></span> <span data-ttu-id="380af-135">Each datacenter has an N number associated with it.</span><span class="sxs-lookup"><span data-stu-id="380af-135">Each datacenter has an N number associated with it.</span></span> <span data-ttu-id="380af-136">For a complete list of available [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps datacenters, and their N numbers,  see [Download endpoints using Developer resources page](../developer-resources-page.md).</span><span class="sxs-lookup"><span data-stu-id="380af-136">For a complete list of available [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps datacenters, and their N numbers,  see [Download endpoints using Developer resources page](../developer-resources-page.md).</span></span>  
  
### <a name="on-premises-and-ifd-discovery-service"></a><span data-ttu-id="380af-137">On-premises and IFD Discovery service</span><span class="sxs-lookup"><span data-stu-id="380af-137">On-premises and IFD Discovery service</span></span>

[!INCLUDE[cc_sdk_onpremises_note](../../includes/cc-sdk-onpremises-note.md)]

<span data-ttu-id="380af-138">The service base address of the Discovery service for an on-premises or IFD deployment is : `http[s]://{servername}/` or `http[s]://dev.{servername}/`.</span><span class="sxs-lookup"><span data-stu-id="380af-138">The service base address of the Discovery service for an on-premises or IFD deployment is : `http[s]://{servername}/` or `http[s]://dev.{servername}/`.</span></span> <span data-ttu-id="380af-139">This results in the service address of `http[s]://{servername}/api/discovery/` or `http[s]://dev.{servername}/api/discovery/`.</span><span class="sxs-lookup"><span data-stu-id="380af-139">This results in the service address of `http[s]://{servername}/api/discovery/` or `http[s]://dev.{servername}/api/discovery/`.</span></span>  
  
## <a name="using-the-discovery-service"></a><span data-ttu-id="380af-140">Using the Discovery service</span><span class="sxs-lookup"><span data-stu-id="380af-140">Using the Discovery service</span></span>  
 <span data-ttu-id="380af-141">An entity set named `Instances` is used to obtain instance information.</span><span class="sxs-lookup"><span data-stu-id="380af-141">An entity set named `Instances` is used to obtain instance information.</span></span> <span data-ttu-id="380af-142">You can use `$select` and `$filter` with the Instances entity set to filter the returned data.</span><span class="sxs-lookup"><span data-stu-id="380af-142">You can use `$select` and `$filter` with the Instances entity set to filter the returned data.</span></span> <span data-ttu-id="380af-143">You can also use `$metadata` to obtain the metadata document of the service.</span><span class="sxs-lookup"><span data-stu-id="380af-143">You can also use `$metadata` to obtain the metadata document of the service.</span></span>  
  
### <a name="authentication"></a><span data-ttu-id="380af-144">Authentication</span><span class="sxs-lookup"><span data-stu-id="380af-144">Authentication</span></span>

[!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] <span data-ttu-id="380af-145">apps Web API instances of the Discovery service require authentication with OAuth access tokens.</span><span class="sxs-lookup"><span data-stu-id="380af-145">apps Web API instances of the Discovery service require authentication with OAuth access tokens.</span></span> <span data-ttu-id="380af-146">On-premise or IFD instances of the Discovery Web API adopt the authentication model of their deployment, supporting either Integrated Windows Authentication (IWA) or OAuth tokens from a trusted token provider.</span><span class="sxs-lookup"><span data-stu-id="380af-146">On-premise or IFD instances of the Discovery Web API adopt the authentication model of their deployment, supporting either Integrated Windows Authentication (IWA) or OAuth tokens from a trusted token provider.</span></span> <span data-ttu-id="380af-147">Web Application Session authentication is not supported.</span><span class="sxs-lookup"><span data-stu-id="380af-147">Web Application Session authentication is not supported.</span></span>  
  
<span data-ttu-id="380af-148">When the Discovery service is configured for OAuth authentication, a request sent  to the service Web API without an access token triggers a bearer challenge with the authority of the “common” endpoint and the resource ID of the service.</span><span class="sxs-lookup"><span data-stu-id="380af-148">When the Discovery service is configured for OAuth authentication, a request sent  to the service Web API without an access token triggers a bearer challenge with the authority of the “common” endpoint and the resource ID of the service.</span></span>  <span data-ttu-id="380af-149">Similarly, when an on-premise deployment is configured for OAuth, a bearer challenge returns the on-premise authority URL and the resource ID of the service.</span><span class="sxs-lookup"><span data-stu-id="380af-149">Similarly, when an on-premise deployment is configured for OAuth, a bearer challenge returns the on-premise authority URL and the resource ID of the service.</span></span>  
  
### <a name="web-api-versioning"></a><span data-ttu-id="380af-150">Web API versioning</span><span class="sxs-lookup"><span data-stu-id="380af-150">Web API versioning</span></span>

<span data-ttu-id="380af-151">Versioning of the Discovery service for a datacenter or on-premises/IFD is supported and is consistent with version numbering as used by the Organization service .</span><span class="sxs-lookup"><span data-stu-id="380af-151">Versioning of the Discovery service for a datacenter or on-premises/IFD is supported and is consistent with version numbering as used by the Organization service .</span></span> <span data-ttu-id="380af-152">However, the global Discovery service of [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps is not tied to the version number of the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] deployment.</span><span class="sxs-lookup"><span data-stu-id="380af-152">However, the global Discovery service of [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps is not tied to the version number of the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] deployment.</span></span> <span data-ttu-id="380af-153">Instead, the global service uses its own version numbering.</span><span class="sxs-lookup"><span data-stu-id="380af-153">Instead, the global service uses its own version numbering.</span></span> <span data-ttu-id="380af-154">As of this writing, the global Discovery service of [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps is at version 1.0 (v1.0).</span><span class="sxs-lookup"><span data-stu-id="380af-154">As of this writing, the global Discovery service of [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps is at version 1.0 (v1.0).</span></span> <span data-ttu-id="380af-155">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="380af-155">For example:</span></span>  
  
```http  
GET https://globaldisco.crm.dynamics.com/api/discovery/v1.0/Instances(UniqueName='myorg')  
```  
  
### <a name="cors-support"></a><span data-ttu-id="380af-156">CORS support</span><span class="sxs-lookup"><span data-stu-id="380af-156">CORS support</span></span>

<span data-ttu-id="380af-157">The Discovery service Web API supports the CORS standard for cross-origin access as does the Web API.</span><span class="sxs-lookup"><span data-stu-id="380af-157">The Discovery service Web API supports the CORS standard for cross-origin access as does the Web API.</span></span>  <span data-ttu-id="380af-158">For more information about CORS support see [Use OAuth with Cross-Origin Resource Sharing  to connect a Single Page Application  to Dynamics 365 for Customer Engagement apps](../oauth-cross-origin-resource-sharing-connect-single-page-application.md).</span><span class="sxs-lookup"><span data-stu-id="380af-158">For more information about CORS support see [Use OAuth with Cross-Origin Resource Sharing  to connect a Single Page Application  to Dynamics 365 for Customer Engagement apps](../oauth-cross-origin-resource-sharing-connect-single-page-application.md).</span></span>  
  
### <a name="examples"></a><span data-ttu-id="380af-159">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="380af-159">Examples</span></span>  
  
-   <span data-ttu-id="380af-160">Get the details of a specific instance.</span><span class="sxs-lookup"><span data-stu-id="380af-160">Get the details of a specific instance.</span></span> <span data-ttu-id="380af-161">If you leave out the GUID, all instances that the authenticated user has access to are returned.</span><span class="sxs-lookup"><span data-stu-id="380af-161">If you leave out the GUID, all instances that the authenticated user has access to are returned.</span></span>  
  
    ```http  
    GET https://disco.crm.dynamics.com/api/discovery/v8.1/Instances(<guid>)  
    GET https://dev.crm.external.contoso.com/api/discovery/v8.1/Instances(<guid>)  
    ```  
  
-   <span data-ttu-id="380af-162">You can use the UniqueName attribute as an alternate key.</span><span class="sxs-lookup"><span data-stu-id="380af-162">You can use the UniqueName attribute as an alternate key.</span></span>  
  
    ```http  
    GET https://globaldisco.crm.dynamics.com/api/discovery/v1.0/Instances(UniqueName='myorg')  
    ```  
  
-   <span data-ttu-id="380af-163">Retrieve a list of available instances, filtered by production type.</span><span class="sxs-lookup"><span data-stu-id="380af-163">Retrieve a list of available instances, filtered by production type.</span></span>  
  
    ```http  
    GET https://globaldisco.crm.dynamics.com/api/discovery/v1.0/Instances?$select=DisplayName,Description&$filter=Type+eq+0   
    ```  
  
-   <span data-ttu-id="380af-164">Retrieve a specific instance's ID property value.</span><span class="sxs-lookup"><span data-stu-id="380af-164">Retrieve a specific instance's ID property value.</span></span>  
  
    ```http  
    GET https://disco.crm.dynamics.com/api/discovery/v8.1/Instances(UniqueName='myorg')/Id/$value  
    ```
