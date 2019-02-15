---
title: Developer resources page (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: Read how you can find your organization unique name, Discovery service endpoint address, Organization service endpoint address and issuer name to access Azure Service Bus using the Developer Resources page
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 826ddda1-2038-40ba-a5a9-8b443a7a6b02
caps.latest.revision: 61
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a2a56f54db0a1174288a1430403c9918a42be4c9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388416"
---
# <a name="developer-resources-page"></a><span data-ttu-id="fa049-103">Developer resources page</span><span class="sxs-lookup"><span data-stu-id="fa049-103">Developer resources page</span></span> 

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="fa049-104">The Developer Resources page in the [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] web application provides important resources.</span><span class="sxs-lookup"><span data-stu-id="fa049-104">The Developer Resources page in the [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] web application provides important resources.</span></span> <span data-ttu-id="fa049-105">Included on this page are the web service endpoint URLs, a certificate for accessing [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)], and other organization information that you'll need during development.</span><span class="sxs-lookup"><span data-stu-id="fa049-105">Included on this page are the web service endpoint URLs, a certificate for accessing [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)], and other organization information that you'll need during development.</span></span> <span data-ttu-id="fa049-106">To access the page in the web application, click **Settings** > **Customizations**, and then click **Developer Resources**.</span><span class="sxs-lookup"><span data-stu-id="fa049-106">To access the page in the web application, click **Settings** > **Customizations**, and then click **Developer Resources**.</span></span>  
  
 <span data-ttu-id="fa049-107">For the Organization service and Organization data service sections in this topic, the example URLs include an `OrganizationName`.</span><span class="sxs-lookup"><span data-stu-id="fa049-107">For the Organization service and Organization data service sections in this topic, the example URLs include an `OrganizationName`.</span></span> <span data-ttu-id="fa049-108">This refers to the organization that you specify in the URL when you access the web application.</span><span class="sxs-lookup"><span data-stu-id="fa049-108">This refers to the organization that you specify in the URL when you access the web application.</span></span> <span data-ttu-id="fa049-109">For example, for Contoso.crm.dynamics.com, the `OrganizationName` is Contoso.</span><span class="sxs-lookup"><span data-stu-id="fa049-109">For example, for Contoso.crm.dynamics.com, the `OrganizationName` is Contoso.</span></span>  <span data-ttu-id="fa049-110">`ServerName` refers to the name of the server, including the port number, for example, myserver or myserver:5555.</span><span class="sxs-lookup"><span data-stu-id="fa049-110">`ServerName` refers to the name of the server, including the port number, for example, myserver or myserver:5555.</span></span>  
  
[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)]

<a name="org_unique"></a>   

## <a name="organization-unique-name"></a><span data-ttu-id="fa049-111">Organization unique name</span><span class="sxs-lookup"><span data-stu-id="fa049-111">Organization unique name</span></span>  

 <span data-ttu-id="fa049-112">Shows the unique name for your organization, which is needed when interacting with the discovery service.</span><span class="sxs-lookup"><span data-stu-id="fa049-112">Shows the unique name for your organization, which is needed when interacting with the discovery service.</span></span> <span data-ttu-id="fa049-113">Note that this may not be the same as the name that’s specified in the URL.</span><span class="sxs-lookup"><span data-stu-id="fa049-113">Note that this may not be the same as the name that’s specified in the URL.</span></span> <span data-ttu-id="fa049-114">This name can be found in the following properties:</span><span class="sxs-lookup"><span data-stu-id="fa049-114">This name can be found in the following properties:</span></span>  
  
- <span data-ttu-id="fa049-115">Deployment web service: <xref:Microsoft.Xrm.Sdk.Deployment.Organization.UniqueName></span><span class="sxs-lookup"><span data-stu-id="fa049-115">Deployment web service: <xref:Microsoft.Xrm.Sdk.Deployment.Organization.UniqueName></span></span>  
  
- <span data-ttu-id="fa049-116">Discovery web service: <xref:Microsoft.Xrm.Sdk.Discovery.OrganizationDetail.UniqueName></span><span class="sxs-lookup"><span data-stu-id="fa049-116">Discovery web service: <xref:Microsoft.Xrm.Sdk.Discovery.OrganizationDetail.UniqueName></span></span>  
  
- <span data-ttu-id="fa049-117">Organization web service using early bound classes: `Organization.UniqueName`</span><span class="sxs-lookup"><span data-stu-id="fa049-117">Organization web service using early bound classes: `Organization.UniqueName`</span></span>  
  
  <span data-ttu-id="fa049-118">You can also retrieve this from the discovery service by using the <xref:Microsoft.Xrm.Sdk.Discovery.RetrieveOrganizationsRequest> message.</span><span class="sxs-lookup"><span data-stu-id="fa049-118">You can also retrieve this from the discovery service by using the <xref:Microsoft.Xrm.Sdk.Discovery.RetrieveOrganizationsRequest> message.</span></span>  
  
<a name="Windows_Azure"></a>   

## <a name="microsoft-azure-service-bus-issuer-certificate"></a><span data-ttu-id="fa049-119">Microsoft Azure Service Bus issuer certificate</span><span class="sxs-lookup"><span data-stu-id="fa049-119">Microsoft Azure Service Bus issuer certificate</span></span>  

 <span data-ttu-id="fa049-120">Provides a download link to the public certificate that is required to configure [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps integration.</span><span class="sxs-lookup"><span data-stu-id="fa049-120">Provides a download link to the public certificate that is required to configure [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps integration.</span></span> <span data-ttu-id="fa049-121">For an on-premises or Internet-facing deployment, this information is only visible after [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] has been configured for [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] integration.</span><span class="sxs-lookup"><span data-stu-id="fa049-121">For an on-premises or Internet-facing deployment, this information is only visible after [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] has been configured for [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] integration.</span></span>  
  
 <span data-ttu-id="fa049-122">For more information, see [Azure Extensions for Dynamics 365 for Customer Engagement apps](azure-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="fa049-122">For more information, see [Azure Extensions for Dynamics 365 for Customer Engagement apps](azure-extensions.md).</span></span>  
 
  
<a name="discovery"></a>   

## <a name="discovery-service"></a><span data-ttu-id="fa049-123">Discovery service</span><span class="sxs-lookup"><span data-stu-id="fa049-123">Discovery service</span></span>  

 <span data-ttu-id="fa049-124">The Discovery Service web service provides information about the organizations available on the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps server.</span><span class="sxs-lookup"><span data-stu-id="fa049-124">The Discovery Service web service provides information about the organizations available on the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps server.</span></span> <span data-ttu-id="fa049-125">This information includes the web address (URL) for each organization.</span><span class="sxs-lookup"><span data-stu-id="fa049-125">This information includes the web address (URL) for each organization.</span></span>

  
### <a name="for-includepndynamicscrmonlineincludespn-dynamics-crm-onlinemd-apps"></a><span data-ttu-id="fa049-126">For [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps</span><span class="sxs-lookup"><span data-stu-id="fa049-126">For [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps</span></span>

<span data-ttu-id="fa049-127">You should generally use the Web API global discovery service because this will ignore regional groupings and allow you to retrieve available organizations world-wide.</span><span class="sxs-lookup"><span data-stu-id="fa049-127">You should generally use the Web API global discovery service because this will ignore regional groupings and allow you to retrieve available organizations world-wide.</span></span> <span data-ttu-id="fa049-128">See [Discover the URL for your organization using the Web API](webapi/discover-url-organization-web-api.md)</span><span class="sxs-lookup"><span data-stu-id="fa049-128">See [Discover the URL for your organization using the Web API](webapi/discover-url-organization-web-api.md)</span></span>


 <span data-ttu-id="fa049-129">If you want to scope the organizations to retrieve to individual regions use the following URLs to access the discovery service (use the appropriate URL for your location).</span><span class="sxs-lookup"><span data-stu-id="fa049-129">If you want to scope the organizations to retrieve to individual regions use the following URLs to access the discovery service (use the appropriate URL for your location).</span></span>  
  
[!INCLUDE [regional-discovery-services](../includes/regional-discovery-services.md)]
  
### <a name="for-on-premises-includepndynamicscrmincludespn-dynamics-crmmd-apps"></a><span data-ttu-id="fa049-130">For on-premises [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps</span><span class="sxs-lookup"><span data-stu-id="fa049-130">For on-premises [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps</span></span>
 <span data-ttu-id="fa049-131">Use the following URL to access the discovery service:</span><span class="sxs-lookup"><span data-stu-id="fa049-131">Use the following URL to access the discovery service:</span></span>  
  
 <span data-ttu-id="fa049-132">http://`ServerName`/XRMServices/2011/Discovery.svc</span><span class="sxs-lookup"><span data-stu-id="fa049-132">http://`ServerName`/XRMServices/2011/Discovery.svc</span></span>  

<span data-ttu-id="fa049-133">For more information, see [Discover the URL for your organization using the Organization Service](org-service/discover-url-organization-organization-service.md).</span><span class="sxs-lookup"><span data-stu-id="fa049-133">For more information, see [Discover the URL for your organization using the Organization Service](org-service/discover-url-organization-organization-service.md).</span></span>
  
<a name="OrganizationService"></a>   

## <a name="organization-service"></a><span data-ttu-id="fa049-134">Organization service</span><span class="sxs-lookup"><span data-stu-id="fa049-134">Organization service</span></span>  

 <span data-ttu-id="fa049-135">The organization service provides access to the business data and metadata of your organization by using the SOAP protocol.</span><span class="sxs-lookup"><span data-stu-id="fa049-135">The organization service provides access to the business data and metadata of your organization by using the SOAP protocol.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="fa049-136">[Use the Organization Service to read and write data or metadata](org-service/use-organization-service-read-write-data-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="fa049-136">[Use the Organization Service to read and write data or metadata](org-service/use-organization-service-read-write-data-metadata.md).</span></span>  
  
### <a name="for-includepndynamicscrmonlineincludespn-dynamics-crm-onlinemd-apps"></a><span data-ttu-id="fa049-137">For [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps</span><span class="sxs-lookup"><span data-stu-id="fa049-137">For [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps</span></span> 

 <span data-ttu-id="fa049-138">Use the following URLs to access the organization service (SOAP endpoint):</span><span class="sxs-lookup"><span data-stu-id="fa049-138">Use the following URLs to access the organization service (SOAP endpoint):</span></span>  

|<span data-ttu-id="fa049-139">Khu vực</span><span class="sxs-lookup"><span data-stu-id="fa049-139">Region</span></span>| <span data-ttu-id="fa049-140">URL</span><span class="sxs-lookup"><span data-stu-id="fa049-140">URL</span></span>|
|---|---|
|<span data-ttu-id="fa049-141">Bắc Mỹ</span><span class="sxs-lookup"><span data-stu-id="fa049-141">North America</span></span>|`https://OrganizationName.api.crm.dynamics.com/XrmServices/2011/Organization.svc`|
|<span data-ttu-id="fa049-142">North America 2</span><span class="sxs-lookup"><span data-stu-id="fa049-142">North America 2</span></span>|`https://OrganizationName.api.crm9.dynamics.com/XrmServices/2011/Organization.svc`|
|<span data-ttu-id="fa049-143">Nam Mỹ</span><span class="sxs-lookup"><span data-stu-id="fa049-143">South America</span></span>|`https://OrganizationName.api.crm2.dynamics.com/XrmServices/2011/Organization.svc`|
|<span data-ttu-id="fa049-144">Canada</span><span class="sxs-lookup"><span data-stu-id="fa049-144">Canada</span></span>|`https://OrganizationName.api.crm3.dynamics.com/XrmServices/2011/Organization.svc`|
|<span data-ttu-id="fa049-145">EMEA</span><span class="sxs-lookup"><span data-stu-id="fa049-145">EMEA</span></span>|`https://OrganizationName.api.crm4.dynamics.com/XrmServices/2011/Organization.svc`|
|<span data-ttu-id="fa049-146">APAC</span><span class="sxs-lookup"><span data-stu-id="fa049-146">APAC</span></span>|`https://OrganizationName.api.crm5.dynamics.com/XrmServices/2011/Organization.svc`|
|<span data-ttu-id="fa049-147">Châu Đại Dương</span><span class="sxs-lookup"><span data-stu-id="fa049-147">Oceania</span></span>|`https://OrganizationName.api.crm6.dynamics.com/XrmServices/2011/Organization.svc`|
|<span data-ttu-id="fa049-148">Nhật Bản</span><span class="sxs-lookup"><span data-stu-id="fa049-148">Japan</span></span>|`https://OrganizationName.api.crm7.dynamics.com/XrmServices/2011/Organization.svc`|
|<span data-ttu-id="fa049-149">Ấn Độ</span><span class="sxs-lookup"><span data-stu-id="fa049-149">India</span></span>|`https://OrganizationName.api.crm8.dynamics.com/XrmServices/2011/Organization.svc`|

  
### <a name="for-on-premises-includepndynamicscrmincludespn-dynamics-crmmd-apps"></a><span data-ttu-id="fa049-150">For on-premises [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps</span><span class="sxs-lookup"><span data-stu-id="fa049-150">For on-premises [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps</span></span>

 <span data-ttu-id="fa049-151">Use the following URL to access the organization service (SOAP endpoint):</span><span class="sxs-lookup"><span data-stu-id="fa049-151">Use the following URL to access the organization service (SOAP endpoint):</span></span>  
  
 `http[s]://ServerName/OrganizationName/XRMServices/2011/Organization.svc`  
  
<a name="OrganizationDataService"></a>   

## <a name="organization-data-service"></a><span data-ttu-id="fa049-152">Organization data service</span><span class="sxs-lookup"><span data-stu-id="fa049-152">Organization data service</span></span>  

 <span data-ttu-id="fa049-153">This Open Data (OData v2) Web service provides access to the business data of your organization by exposing a RESTAPI.</span><span class="sxs-lookup"><span data-stu-id="fa049-153">This Open Data (OData v2) Web service provides access to the business data of your organization by exposing a RESTAPI.</span></span> <span data-ttu-id="fa049-154">This link opens the Conceptual Schema Definition Language (CSDL) document that describes how to access your data by using this API.</span><span class="sxs-lookup"><span data-stu-id="fa049-154">This link opens the Conceptual Schema Definition Language (CSDL) document that describes how to access your data by using this API.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="fa049-155">The Organization Data service has been deprecated and replaced by the Web API.</span><span class="sxs-lookup"><span data-stu-id="fa049-155">The Organization Data service has been deprecated and replaced by the Web API.</span></span> <span data-ttu-id="fa049-156">For more information about the Web API see [Use the Dynamics 365 for Customer Engagement Web API](use-microsoft-dynamics-365-web-api.md).</span><span class="sxs-lookup"><span data-stu-id="fa049-156">For more information about the Web API see [Use the Dynamics 365 for Customer Engagement Web API](use-microsoft-dynamics-365-web-api.md).</span></span>  
  
### <a name="for-includepndynamicscrmonlineincludespn-dynamics-crm-onlinemd-apps"></a><span data-ttu-id="fa049-157">For [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps</span><span class="sxs-lookup"><span data-stu-id="fa049-157">For [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps</span></span>  

 <span data-ttu-id="fa049-158">Use the following URLs to access the organization data service (ODataREST endpoint):</span><span class="sxs-lookup"><span data-stu-id="fa049-158">Use the following URLs to access the organization data service (ODataREST endpoint):</span></span>  

|<span data-ttu-id="fa049-159">Khu vực</span><span class="sxs-lookup"><span data-stu-id="fa049-159">Region</span></span>| <span data-ttu-id="fa049-160">URL</span><span class="sxs-lookup"><span data-stu-id="fa049-160">URL</span></span>|
|---|---|
|<span data-ttu-id="fa049-161">Bắc Mỹ</span><span class="sxs-lookup"><span data-stu-id="fa049-161">North America</span></span>|`https://OrganizationName.api.crm.dynamics.com/XrmServices/2011/OrganizationData.svc`|
|<span data-ttu-id="fa049-162">North America 2</span><span class="sxs-lookup"><span data-stu-id="fa049-162">North America 2</span></span>|`https://OrganizationName.api.crm9.dynamics.com/XrmServices/2011/OrganizationData.svc`|
|<span data-ttu-id="fa049-163">Nam Mỹ</span><span class="sxs-lookup"><span data-stu-id="fa049-163">South America</span></span>|`https://OrganizationName.api.crm2.dynamics.com/XrmServices/2011/OrganizationData.svc`|
|<span data-ttu-id="fa049-164">Canada</span><span class="sxs-lookup"><span data-stu-id="fa049-164">Canada</span></span>|`https://OrganizationName.api.crm3.dynamics.com/XrmServices/2011/OrganizationData.svc`|
|<span data-ttu-id="fa049-165">EMEA</span><span class="sxs-lookup"><span data-stu-id="fa049-165">EMEA</span></span>|`https://OrganizationName.api.crm4.dynamics.com/XrmServices/2011/OrganizationData.svc`|
|<span data-ttu-id="fa049-166">APAC</span><span class="sxs-lookup"><span data-stu-id="fa049-166">APAC</span></span>|`https://OrganizationName.api.crm5.dynamics.com/XrmServices/2011/OrganizationData.svc`|
|<span data-ttu-id="fa049-167">Châu Đại Dương</span><span class="sxs-lookup"><span data-stu-id="fa049-167">Oceania</span></span>|`https://OrganizationName.api.crm6.dynamics.com/XrmServices/2011/OrganizationData.svc`|
|<span data-ttu-id="fa049-168">Nhật Bản</span><span class="sxs-lookup"><span data-stu-id="fa049-168">Japan</span></span>|`https://OrganizationName.api.crm7.dynamics.com/XrmServices/2011/OrganizationData.svc`|
|<span data-ttu-id="fa049-169">Ấn Độ</span><span class="sxs-lookup"><span data-stu-id="fa049-169">India</span></span>|`https://OrganizationName.api.crm8.dynamics.com/XrmServices/2011/OrganizationData.svc`|

  
### <a name="for-on-premises-includepndynamicscrmincludespn-dynamics-crmmd-apps"></a><span data-ttu-id="fa049-170">For on-premises [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps</span><span class="sxs-lookup"><span data-stu-id="fa049-170">For on-premises [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps</span></span>  
 <span data-ttu-id="fa049-171">Use the following URL to access the organization data service (ODataREST endpoint):</span><span class="sxs-lookup"><span data-stu-id="fa049-171">Use the following URL to access the organization data service (ODataREST endpoint):</span></span>  
  
 `http[s]://ServerName/OrganizationName/XRMServices/2011/OrganizationData.svc`  
  
<a name="wsdl"></a>

## <a name="using-the-wsdl"></a><span data-ttu-id="fa049-172">Using the WSDL</span><span class="sxs-lookup"><span data-stu-id="fa049-172">Using the WSDL</span></span>

 <span data-ttu-id="fa049-173">To add a service reference for these services to a [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] project, you must append `?WSDL` to the service URL when specifying the address in the **Add Service Reference** dialog box.</span><span class="sxs-lookup"><span data-stu-id="fa049-173">To add a service reference for these services to a [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] project, you must append `?WSDL` to the service URL when specifying the address in the **Add Service Reference** dialog box.</span></span> <span data-ttu-id="fa049-174">For example, the discovery service Web Services Description Language (WSDL) address is `http[s]://servername/xrmservices/2011/discovery.svc?wsdl`.</span><span class="sxs-lookup"><span data-stu-id="fa049-174">For example, the discovery service Web Services Description Language (WSDL) address is `http[s]://servername/xrmservices/2011/discovery.svc?wsdl`.</span></span>  
  
 <span data-ttu-id="fa049-175">The web services support SDK versioning.</span><span class="sxs-lookup"><span data-stu-id="fa049-175">The web services support SDK versioning.</span></span> <span data-ttu-id="fa049-176">Specifying an SDK version in the WSDL URL indicates a scope for the amount of data to be returned in the WSDL.</span><span class="sxs-lookup"><span data-stu-id="fa049-176">Specifying an SDK version in the WSDL URL indicates a scope for the amount of data to be returned in the WSDL.</span></span> <span data-ttu-id="fa049-177">The syntax for web service SDK versioning ends the URL in `?singleWSDL&sdkversion=X.X`.</span><span class="sxs-lookup"><span data-stu-id="fa049-177">The syntax for web service SDK versioning ends the URL in `?singleWSDL&sdkversion=X.X`.</span></span> <span data-ttu-id="fa049-178">For example, the URL would be `https://mydomain.crm.dynamics.com/xrmservices/2011/discovery.svc?singleWSDL&sdkversion=8.0`.</span><span class="sxs-lookup"><span data-stu-id="fa049-178">For example, the URL would be `https://mydomain.crm.dynamics.com/xrmservices/2011/discovery.svc?singleWSDL&sdkversion=8.0`.</span></span> <span data-ttu-id="fa049-179">In this example, you would have built your application using the v8.0 .NET assemblies.</span><span class="sxs-lookup"><span data-stu-id="fa049-179">In this example, you would have built your application using the v8.0 .NET assemblies.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="fa049-180">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="fa049-180">See also</span></span>

 <span data-ttu-id="fa049-181">[Write Code for Dynamics 365 for Customer Engagement Web Services](extend-dynamics-365-server.md) </span><span class="sxs-lookup"><span data-stu-id="fa049-181">[Write Code for Dynamics 365 for Customer Engagement Web Services](extend-dynamics-365-server.md) </span></span>  
 [<span data-ttu-id="fa049-182">Use the IOrganizationService web service to read and write data or metadata</span><span class="sxs-lookup"><span data-stu-id="fa049-182">Use the IOrganizationService web service to read and write data or metadata</span></span>](org-service/use-organization-service-read-write-data-metadata.md)   
