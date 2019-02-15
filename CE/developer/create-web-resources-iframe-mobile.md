---
title: Create web resources and IFrame content for use with the Dynamics 365 for Customer Engagement apps for mobile clients (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: 'Learn about creating web resources and IFrames to use with the Dynamics 365 for Customer Engagement apps for mobile clients: iOS, Android, and Windows 10.'
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 2cf94cbb-d3a1-4aaf-8dc4-bfe5f81f22d1
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e041bf4a4d7bead0a391002c9eb4b1961dcc039f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387732"
---
# <a name="create-web-resources-and-iframe-content-for-use-with-the-dynamics-365-for-customer-engagement-apps-for-mobile-clients"></a><span data-ttu-id="9a4da-103">Create web resources and IFrame content for use with the Dynamics 365 for Customer Engagement apps for mobile clients</span><span class="sxs-lookup"><span data-stu-id="9a4da-103">Create web resources and IFrame content for use with the Dynamics 365 for Customer Engagement apps for mobile clients</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

> [!NOTE]
> - <span data-ttu-id="9a4da-104">The capability to display web resources and Iframes in phone clients was introduced in [!INCLUDE[../includes/pn-crm-9-0-0-online.md](../includes/pn-crm-9-0-0-online.md)].</span><span class="sxs-lookup"><span data-stu-id="9a4da-104">The capability to display web resources and Iframes in phone clients was introduced in [!INCLUDE[../includes/pn-crm-9-0-0-online.md](../includes/pn-crm-9-0-0-online.md)].</span></span>
> - <span data-ttu-id="9a4da-105">The capability to display web resources and iframes in tablet clients was introdced in Dynamics CRM Online 2016 Update and CRM 2016 (on-premises).</span><span class="sxs-lookup"><span data-stu-id="9a4da-105">The capability to display web resources and iframes in tablet clients was introdced in Dynamics CRM Online 2016 Update and CRM 2016 (on-premises).</span></span>


<span data-ttu-id="9a4da-106">You can create web resources and IFrames to use with mobile (tablet and phone) clients in all the client forms: iOS, [!INCLUDE[tn_android](../includes/tn-android.md)], and [!INCLUDE[pn_windows_10](../includes/pn-windows-10.md)].</span><span class="sxs-lookup"><span data-stu-id="9a4da-106">You can create web resources and IFrames to use with mobile (tablet and phone) clients in all the client forms: iOS, [!INCLUDE[tn_android](../includes/tn-android.md)], and [!INCLUDE[pn_windows_10](../includes/pn-windows-10.md)].</span></span> 
  
 <span data-ttu-id="9a4da-107">You can configure IFrames and web resources in forms and dashboards in the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] web app, which can be configured to display in mobile clients.</span><span class="sxs-lookup"><span data-stu-id="9a4da-107">You can configure IFrames and web resources in forms and dashboards in the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] web app, which can be configured to display in mobile clients.</span></span>  
  
<a name="BKMK_ConfigureWebResource"></a>   

## <a name="configure-a-web-resource-to-be-displayed-in-mobile-clients"></a><span data-ttu-id="9a4da-108">Configure a web resource to be displayed in mobile clients</span><span class="sxs-lookup"><span data-stu-id="9a4da-108">Configure a web resource to be displayed in mobile clients</span></span>  

<span data-ttu-id="9a4da-109">To use this feature, you can enable **Webpage (HTML)** and image types of web resources by selecting the **Enable for mobile** check box in the web resource form.</span><span class="sxs-lookup"><span data-stu-id="9a4da-109">To use this feature, you can enable **Webpage (HTML)** and image types of web resources by selecting the **Enable for mobile** check box in the web resource form.</span></span> <span data-ttu-id="9a4da-110">The `WebResource.IsEnabledForMobileClient` attribute stores this data.</span><span class="sxs-lookup"><span data-stu-id="9a4da-110">The `WebResource.IsEnabledForMobileClient` attribute stores this data.</span></span>  

<span data-ttu-id="9a4da-111">Additionally, for these types of web resources, you can select the **Available Offline** check box to make a web resource available to users of mobile clients while working in the offline mode.</span><span class="sxs-lookup"><span data-stu-id="9a4da-111">Additionally, for these types of web resources, you can select the **Available Offline** check box to make a web resource available to users of mobile clients while working in the offline mode.</span></span> <span data-ttu-id="9a4da-112">The `WebResource.IsAvailableForMobileOffline` attribute stores this data.</span><span class="sxs-lookup"><span data-stu-id="9a4da-112">The `WebResource.IsAvailableForMobileOffline` attribute stores this data.</span></span>  

![Enable a web resource for mobile clients](media/web-resource-enable-for-mobile.png)  

> [!NOTE]
> <span data-ttu-id="9a4da-114">If your **Webpage (HTML)** web resources reference on any other type of web resource which is not enabled for offline use, you must set those web resources as dependences for the HTML web resource so that they will be enabled for use offline.</span><span class="sxs-lookup"><span data-stu-id="9a4da-114">If your **Webpage (HTML)** web resources reference on any other type of web resource which is not enabled for offline use, you must set those web resources as dependences for the HTML web resource so that they will be enabled for use offline.</span></span> <span data-ttu-id="9a4da-115">Thông tin khác: [Quan hệ phụ thuộc tài nguyên web](web-resource-dependencies.md)</span><span class="sxs-lookup"><span data-stu-id="9a4da-115">More information: [Web resource dependencies](web-resource-dependencies.md)</span></span>
  
<a name="BKMK_ConfigureControl"></a>

## <a name="configure-a-form-or-dashboard-iframe-or-web-resource-control-to-display-in-dynamics-365-for-customer-engagement-apps-for-mobile-clients"></a><span data-ttu-id="9a4da-116">Configure a form or dashboard IFrame or web resource control to display in Dynamics 365 for Customer Engagement apps for mobile clients</span><span class="sxs-lookup"><span data-stu-id="9a4da-116">Configure a form or dashboard IFrame or web resource control to display in Dynamics 365 for Customer Engagement apps for mobile clients</span></span>  

<span data-ttu-id="9a4da-117">When you add an IFrame or a web resource to a form or dashboard, you must select the **Enable for mobile** check box in the **Add Web Resource** dialog box.</span><span class="sxs-lookup"><span data-stu-id="9a4da-117">When you add an IFrame or a web resource to a form or dashboard, you must select the **Enable for mobile** check box in the **Add Web Resource** dialog box.</span></span> <span data-ttu-id="9a4da-118">This sets the `<ShowOnMobileClient>` parameter value for the control.</span><span class="sxs-lookup"><span data-stu-id="9a4da-118">This sets the `<ShowOnMobileClient>` parameter value for the control.</span></span>  
  
 ![Select Enable for mobile check box](media/enable-mobile-web-resource-control.PNG)  
  
<a name="BKMK_KnownIssues"></a>

## <a name="known-issues"></a><span data-ttu-id="9a4da-120">Sự cố đã biết</span><span class="sxs-lookup"><span data-stu-id="9a4da-120">Known issues</span></span>  

 <span data-ttu-id="9a4da-121">These are some known issues with IFrames and web resources for mobile clients:</span><span class="sxs-lookup"><span data-stu-id="9a4da-121">These are some known issues with IFrames and web resources for mobile clients:</span></span>  
  
- <span data-ttu-id="9a4da-122">You can’t use popups for authentication or other purposes from within IFrames and web resources on mobile clients.</span><span class="sxs-lookup"><span data-stu-id="9a4da-122">You can’t use popups for authentication or other purposes from within IFrames and web resources on mobile clients.</span></span>    
- <span data-ttu-id="9a4da-123">Xác thực cho các trang web [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] được nhúng không có sẵn.</span><span class="sxs-lookup"><span data-stu-id="9a4da-123">Authentication for embedded [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] sites isn’t available.</span></span>    
- <span data-ttu-id="9a4da-124">Errors and memory leaks in IFrames and web resources can cause mobile clients to malfunction and can cause client-side data loss.</span><span class="sxs-lookup"><span data-stu-id="9a4da-124">Errors and memory leaks in IFrames and web resources can cause mobile clients to malfunction and can cause client-side data loss.</span></span>    
- [!INCLUDE[pn_MS_Silverlight_full](../includes/pn-ms-silverlight-full.md)] <span data-ttu-id="9a4da-125">web resources aren’t available on mobile clients.</span><span class="sxs-lookup"><span data-stu-id="9a4da-125">web resources aren’t available on mobile clients.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="9a4da-126">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="9a4da-126">See also</span></span>

[<span data-ttu-id="9a4da-127">Web resources for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="9a4da-127">Web resources for Dynamics 365 for Customer Engagement apps</span></span>](web-resources.md)<br />
[<span data-ttu-id="9a4da-128">Create accessible web resources</span><span class="sxs-lookup"><span data-stu-id="9a4da-128">Create accessible web resources</span></span>](create-accessible-web-resources.md)<br />
[<span data-ttu-id="9a4da-129">Create web resources and IFrame content for use with the Dynamics 365 for Customer Engagement apps for mobile clients</span><span class="sxs-lookup"><span data-stu-id="9a4da-129">Create web resources and IFrame content for use with the Dynamics 365 for Customer Engagement apps for mobile clients</span></span>](create-web-resources-iframe-mobile.md)<br />
[<span data-ttu-id="9a4da-130">Quan hệ phụ thuộc tài nguyên web</span><span class="sxs-lookup"><span data-stu-id="9a4da-130">Web resource dependencies</span></span>](web-resource-dependencies.md)<br />
[<span data-ttu-id="9a4da-131">Webpage (HTML) web resources</span><span class="sxs-lookup"><span data-stu-id="9a4da-131">Webpage (HTML) web resources</span></span>](webpage-html-web-resources.md)<br />
[<span data-ttu-id="9a4da-132">Silverlight (XAP) web resources</span><span class="sxs-lookup"><span data-stu-id="9a4da-132">Silverlight (XAP) web resources</span></span>](silverlight-xap-web-resources.md)<br />
[<span data-ttu-id="9a4da-133">Script (JScript) web resources</span><span class="sxs-lookup"><span data-stu-id="9a4da-133">Script (JScript) web resources</span></span>](script-jscript-web-resources.md)<br />
[<span data-ttu-id="9a4da-134">Image web resources</span><span class="sxs-lookup"><span data-stu-id="9a4da-134">Image web resources</span></span>](image-web-resources.md)<br />
[<span data-ttu-id="9a4da-135">Stylesheet (XSL) web resources</span><span class="sxs-lookup"><span data-stu-id="9a4da-135">Stylesheet (XSL) web resources</span></span>](stylesheet-xsl-web-resources.md)<br />
[<span data-ttu-id="9a4da-136">Data (XML) Web resources</span><span class="sxs-lookup"><span data-stu-id="9a4da-136">Data (XML) Web resources</span></span>](data-xml-web-resources.md)<br />
[<span data-ttu-id="9a4da-137">CSS web resources</span><span class="sxs-lookup"><span data-stu-id="9a4da-137">CSS web resources</span></span>](css-web-resources.md)<br />
[<span data-ttu-id="9a4da-138">RESX web resources</span><span class="sxs-lookup"><span data-stu-id="9a4da-138">RESX web resources</span></span>](resx-web-resources.md)<br />
[<span data-ttu-id="9a4da-139">WebResource entity messages and methods</span><span class="sxs-lookup"><span data-stu-id="9a4da-139">WebResource entity messages and methods</span></span>](webresource-entity-messages-methods.md)<br />
[<span data-ttu-id="9a4da-140">Sample: Pass multiple values to a  web resource through the data parameter</span><span class="sxs-lookup"><span data-stu-id="9a4da-140">Sample: Pass multiple values to a  web resource through the data parameter</span></span>](sample-pass-multiple-values-web-resource-through-data-parameter.md)<br />
[<span data-ttu-id="9a4da-141">Sample: Import files as web resources</span><span class="sxs-lookup"><span data-stu-id="9a4da-141">Sample: Import files as web resources</span></span>](sample-import-files-web-resources.md)<br />
[<span data-ttu-id="9a4da-142">Sample: Web resource utility</span><span class="sxs-lookup"><span data-stu-id="9a4da-142">Sample: Web resource utility</span></span>](sample-web-resource-utility.md)<br /><span data-ttu-id="9a4da-143"> 
[iFrame and web resource support in Dynamics 365 for tablets](../customize/iframe-web-resource-support-dynamics-365-phones-tablets.md)</span><span class="sxs-lookup"><span data-stu-id="9a4da-143"> 
[iFrame and web resource support in Dynamics 365 for tablets](../customize/iframe-web-resource-support-dynamics-365-phones-tablets.md)</span></span><br />
