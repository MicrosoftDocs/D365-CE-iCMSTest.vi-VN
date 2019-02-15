---
title: Service calendar appearance configuration | MicrosoftDocs
description: Learn about the configuration of the service calendar appearance configuration.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- service calendar, appearance
- isv.config
ms.assetid: b529c857-c2b9-4a02-9993-bd99008d7998
caps.latest.revision: 22
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: da6dff287cac1c7d40e80383066dcfb893cf255f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385481"
---
# <a name="service-calendar-appearance-configuration"></a><span data-ttu-id="69d3b-103">Service calendar appearance configuration</span><span class="sxs-lookup"><span data-stu-id="69d3b-103">Service calendar appearance configuration</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="69d3b-104">You can control the appearance and behavior of the service calendar in the following ways:</span><span class="sxs-lookup"><span data-stu-id="69d3b-104">You can control the appearance and behavior of the service calendar in the following ways:</span></span>  
  
- [<span data-ttu-id="69d3b-105">Set time block appearance</span><span class="sxs-lookup"><span data-stu-id="69d3b-105">Set time block appearance</span></span>](service-calendar-appearance-configuration.md#BKMK_TimeBlock)  
  
- [<span data-ttu-id="69d3b-106">Set smooth scroll limit</span><span class="sxs-lookup"><span data-stu-id="69d3b-106">Set smooth scroll limit</span></span>](service-calendar-appearance-configuration.md#BKMK_SmoothScrollLimit)  
  
- [<span data-ttu-id="69d3b-107">Set validation chunk size</span><span class="sxs-lookup"><span data-stu-id="69d3b-107">Set validation chunk size</span></span>](service-calendar-appearance-configuration.md#BKMK_ValidationChunkSize)  
  
  <span data-ttu-id="69d3b-108">To edit these settings you must export the ISV.Config file by adding it as part of a solution, edit the `<IsvConfig>` element in the customizations.xml file, and then re-import and publish the solution.</span><span class="sxs-lookup"><span data-stu-id="69d3b-108">To edit these settings you must export the ISV.Config file by adding it as part of a solution, edit the `<IsvConfig>` element in the customizations.xml file, and then re-import and publish the solution.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="69d3b-109">[Export the ISV.Config](service-calendar-appearance-configuration.md#BKMK_ExportISVConfig)</span><span class="sxs-lookup"><span data-stu-id="69d3b-109">[Export the ISV.Config](service-calendar-appearance-configuration.md#BKMK_ExportISVConfig)</span></span>  
  
<a name="BKMK_TimeBlock"></a>   
## <a name="set-time-block-appearance"></a><span data-ttu-id="69d3b-110">Set time block appearance</span><span class="sxs-lookup"><span data-stu-id="69d3b-110">Set time block appearance</span></span>  
 <span data-ttu-id="69d3b-111">You can control the appearance of the rendered blocks in the service calendar.</span><span class="sxs-lookup"><span data-stu-id="69d3b-111">You can control the appearance of the rendered blocks in the service calendar.</span></span> <span data-ttu-id="69d3b-112">You can control the color used to render the given entity type and status code.</span><span class="sxs-lookup"><span data-stu-id="69d3b-112">You can control the color used to render the given entity type and status code.</span></span>  
  
 <span data-ttu-id="69d3b-113">Create a CSS web resource with a display name of “AppointmentBookConfig”.</span><span class="sxs-lookup"><span data-stu-id="69d3b-113">Create a CSS web resource with a display name of “AppointmentBookConfig”.</span></span> <span data-ttu-id="69d3b-114">In the CSS web resource, define CSS classes using the following naming convention:</span><span class="sxs-lookup"><span data-stu-id="69d3b-114">In the CSS web resource, define CSS classes using the following naming convention:</span></span>  
  
 `[div.ganttBlock<entitylogicalname>Status<statuscode>]`  
  
 <span data-ttu-id="69d3b-115">The following example shows how the CSS classes should be defined.</span><span class="sxs-lookup"><span data-stu-id="69d3b-115">The following example shows how the CSS classes should be defined.</span></span>  
  
```css  
div.ganttBlockserviceappointmentStatus1  
{  
    border: 1px solid #FF0000;  
    FILTER: progid:DXImageTransform.Microsoft.gradient(GradientType=0,startColorstr='#FF0000',endColorstr='#FF0000');  
    background: -moz-linear-gradient(top,  #FF0000 0%, #FF0000 100%);  
    background: -webkit-linear-gradient(top,  #FF0000 0%,#FF0000 100%);  
    background: -ms-linear-gradient(top,  #FF0000 0%,#FF0000 100%);  
    background: linear-gradient(top,  #FF0000 0%,#FF0000 100%);  
}   
  
div.ganttBlockserviceappointmentStatus2  
{  
    border: 1px solid #00FF00;  
    FILTER: progid:DXImageTransform.Microsoft.gradient(GradientType=0,startColorstr='#00FF00',endColorstr='#00FF00');  
    background: -moz-linear-gradient(top,  #00FF00 0%, #00FF00 100%);  
    background: -webkit-linear-gradient(top,  #00FF00 0%,#00FF00 100%);  
    background: -ms-linear-gradient(top,  #00FF00 0%,#00FF00 100%);  
    background: linear-gradient(top,  #00FF00 0%,#00FF00 100%);  
}  
  
div.ganttBlockserviceappointmentStatus3  
{  
    border: 1px solid #0000FF;  
    FILTER: progid:DXImageTransform.Microsoft.gradient(GradientType=0,startColorstr='#0000FF',endColorstr='#0000FF');  
    background: -moz-linear-gradient(top,  #0000FF 0%, #0000FF 100%);  
    background: -webkit-linear-gradient(top,  #0000FF 0%,#0000FF 100%);  
    background: -ms-linear-gradient(top,  #0000FF 0%,#0000FF 100%);  
    background: linear-gradient(top,  #0000FF 0%,#0000FF 100%);  
}   
  
div.ganttBlockserviceappointmentStatus4  
{  
    border: 1px solid #FFFF00;  
    FILTER: progid:DXImageTransform.Microsoft.gradient(GradientType=0,startColorstr='#FFFF00',endColorstr='#FFFF00');  
    background: -moz-linear-gradient(top,  #FFFF00 0%, #FFFF00 100%);  
    background: -webkit-linear-gradient(top,  #FFFF00 0%,#FFFF00 100%);  
    background: -ms-linear-gradient(top,  #FFFF00 0%,#FFFF00 100%);  
    background: linear-gradient(top,  #FFFF00 0%,#FFFF00 100%);  
}   
  
div.ganttBlockserviceappointmentStatus6  
{  
    border: 1px solid #FF00FF;  
    FILTER: progid:DXImageTransform.Microsoft.gradient(GradientType=0,startColorstr='#FF00FF',endColorstr='#FF00FF');  
    background: -moz-linear-gradient(top,  #FF00FF 0%, #FF00FF 100%);  
    background: -webkit-linear-gradient(top,  #FF00FF 0%,#FF00FF 100%);  
    background: -ms-linear-gradient(top,  #FF00FF 0%,#FF00FF 100%);  
    background: linear-gradient(top,  #FF00FF 0%,#FF00FF 100%);  
}   
  
div.ganttBlockserviceappointmentStatus7  
{  
    border: 1px solid #00FFFF;  
    FILTER: progid:DXImageTransform.Microsoft.gradient(GradientType=0,startColorstr='#00FFFF',endColorstr='#00FFFF');  
    background: -moz-linear-gradient(top,  #00FFFF 0%, #00FFFF 100%);  
    background: -webkit-linear-gradient(top,  #00FFFF 0%,#00FFFF 100%);  
    background: -ms-linear-gradient(top,  #00FFFF 0%,#00FFFF 100%);  
    background: linear-gradient(top,  #00FFFF 0%,#00FFFF 100%);  
}  
  
div.ganttBlockserviceappointmentStatus8  
{  
    border: 1px solid #7F7F7F;  
    FILTER: progid:DXImageTransform.Microsoft.gradient(GradientType=0,startColorstr='#7F7F7F',endColorstr='#7F7F7F');  
    background: -moz-linear-gradient(top,  #7F7F7F 0%, #7F7F7F 100%);  
    background: -webkit-linear-gradient(top,  #7F7F7F 0%,#7F7F7F 100%);  
    background: -ms-linear-gradient(top,  #7F7F7F 0%,#7F7F7F 100%);  
    background: linear-gradient(top,  #7F7F7F 0%,#7F7F7F 100%);  
}  
  
```  
  
<a name="BKMK_SmoothScrollLimit"></a>   
## <a name="set-smooth-scroll-limit"></a><span data-ttu-id="69d3b-116">Set smooth scroll limit</span><span class="sxs-lookup"><span data-stu-id="69d3b-116">Set smooth scroll limit</span></span>  
 <span data-ttu-id="69d3b-117">You can specify the limit when smooth scrolling is used based on the number of blocks rendered in the service calendar.</span><span class="sxs-lookup"><span data-stu-id="69d3b-117">You can specify the limit when smooth scrolling is used based on the number of blocks rendered in the service calendar.</span></span>  
  
 <span data-ttu-id="69d3b-118">When the service calendar renders more blocks than indicated in the `SmoothScrollLimit` element, the behavior changes from scrolling to simply jumping to the first appointment.</span><span class="sxs-lookup"><span data-stu-id="69d3b-118">When the service calendar renders more blocks than indicated in the `SmoothScrollLimit` element, the behavior changes from scrolling to simply jumping to the first appointment.</span></span> <span data-ttu-id="69d3b-119">The service calendar automatically scrolls to the first appointment when it’s first displayed and when a row is selected.</span><span class="sxs-lookup"><span data-stu-id="69d3b-119">The service calendar automatically scrolls to the first appointment when it’s first displayed and when a row is selected.</span></span>  
  
 <span data-ttu-id="69d3b-120">To set this value, you must export the ISV.Config file as part of a solution and locate the `SmoothScrollLimit` element at `/ImportExportXml/IsvConfig/configuration/ServiceManagement/AppointmentBook/SmoothScrollLimit`.</span><span class="sxs-lookup"><span data-stu-id="69d3b-120">To set this value, you must export the ISV.Config file as part of a solution and locate the `SmoothScrollLimit` element at `/ImportExportXml/IsvConfig/configuration/ServiceManagement/AppointmentBook/SmoothScrollLimit`.</span></span>  
  
 <span data-ttu-id="69d3b-121">Giá trị mặc định là 2000.</span><span class="sxs-lookup"><span data-stu-id="69d3b-121">The default value is 2000.</span></span> <span data-ttu-id="69d3b-122">You must edit the value, and the re-import and publish the solution before the change will take effect.</span><span class="sxs-lookup"><span data-stu-id="69d3b-122">You must edit the value, and the re-import and publish the solution before the change will take effect.</span></span>  
  
<a name="BKMK_ValidationChunkSize"></a>   
## <a name="set-validation-chunk-size"></a><span data-ttu-id="69d3b-123">Set validation chunk size</span><span class="sxs-lookup"><span data-stu-id="69d3b-123">Set validation chunk size</span></span>  
 <span data-ttu-id="69d3b-124">You can specify the number of appointments or service activities that are passed to the server at a time to check for scheduling errors in the service calendar.</span><span class="sxs-lookup"><span data-stu-id="69d3b-124">You can specify the number of appointments or service activities that are passed to the server at a time to check for scheduling errors in the service calendar.</span></span>  
  
 <span data-ttu-id="69d3b-125">To set this value you must export the ISV.Config file as part of a solution and locate the `ValidationChunkSize` element at  `/ImportExportXml/IsvConfig/configuration/ServiceManagement/AppointmentBook/ValidationChunkSize`.</span><span class="sxs-lookup"><span data-stu-id="69d3b-125">To set this value you must export the ISV.Config file as part of a solution and locate the `ValidationChunkSize` element at  `/ImportExportXml/IsvConfig/configuration/ServiceManagement/AppointmentBook/ValidationChunkSize`.</span></span> <span data-ttu-id="69d3b-126">This element isn’t included in the ISV.Config file by default so you must add it as a child of the `AppointmentBook` element.</span><span class="sxs-lookup"><span data-stu-id="69d3b-126">This element isn’t included in the ISV.Config file by default so you must add it as a child of the `AppointmentBook` element.</span></span>  
  
<a name="BKMK_ExportISVConfig"></a>   
## <a name="export-the-isvconfig"></a><span data-ttu-id="69d3b-127">Export the ISV.Config</span><span class="sxs-lookup"><span data-stu-id="69d3b-127">Export the ISV.Config</span></span>  
 <span data-ttu-id="69d3b-128">When you export a solution the **Export Solution** dialog box provides the **Export System Settings (Advanced)** option page.</span><span class="sxs-lookup"><span data-stu-id="69d3b-128">When you export a solution the **Export Solution** dialog box provides the **Export System Settings (Advanced)** option page.</span></span> <span data-ttu-id="69d3b-129">Select **ISV Config** as an option.</span><span class="sxs-lookup"><span data-stu-id="69d3b-129">Select **ISV Config** as an option.</span></span> <span data-ttu-id="69d3b-130">The `IsvConfig` element will be included as a child of the `ImportExportXml` node.</span><span class="sxs-lookup"><span data-stu-id="69d3b-130">The `IsvConfig` element will be included as a child of the `ImportExportXml` node.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="69d3b-131">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="69d3b-131">See also</span></span>  
 <span data-ttu-id="69d3b-132">[Customize Entity Views](customize-entity-views.md) </span><span class="sxs-lookup"><span data-stu-id="69d3b-132">[Customize Entity Views](customize-entity-views.md) </span></span>  
 <span data-ttu-id="69d3b-133">[ISV Configuration File Schema](isv-configuration-file-schema.md) </span><span class="sxs-lookup"><span data-stu-id="69d3b-133">[ISV Configuration File Schema](isv-configuration-file-schema.md) </span></span>  
 <span data-ttu-id="69d3b-134">[Customize Microsoft Dynamics 365 for Customer Engagement](customize-applications.md) </span><span class="sxs-lookup"><span data-stu-id="69d3b-134">[Customize Microsoft Dynamics 365 for Customer Engagement](customize-applications.md) </span></span>  
 <span data-ttu-id="69d3b-135">[Create, Export, or Import an Unmanaged Solution](../create-export-import-unmanaged-solution.md) </span><span class="sxs-lookup"><span data-stu-id="69d3b-135">[Create, Export, or Import an Unmanaged Solution](../create-export-import-unmanaged-solution.md) </span></span>  
 <span data-ttu-id="69d3b-136">[Support for Editing the Customization File](when-edit-customization-file.md) </span><span class="sxs-lookup"><span data-stu-id="69d3b-136">[Support for Editing the Customization File](when-edit-customization-file.md) </span></span>  
 <span data-ttu-id="69d3b-137">[Publish Customizations](publish-customizations.md) </span><span class="sxs-lookup"><span data-stu-id="69d3b-137">[Publish Customizations](publish-customizations.md) </span></span>  
 [<span data-ttu-id="69d3b-138">ISV Configuration File Schema</span><span class="sxs-lookup"><span data-stu-id="69d3b-138">ISV Configuration File Schema</span></span>](isv-configuration-file-schema.md)
