---
title: Customize login and splash screens in Unified Service Desk | MicrosoftDocs
description: The topic explains how to customize the branding of Unified Service Desk login and splash screens to change the name and appearance of the application name on the login screen and change the application name, appearance, foreground and background colors of the splash screen by modifying XAML styles.
ms.custom:
- dyn365-USD
ms.date: 08/23/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: b28f7509-bea1-4bb4-84a7-691665eaff03
caps.latest.revision: 12
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: d2aafe503996293b3fe3a4840a2a2228f711babe
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387163"
---
# <a name="customize-login-and-splash-screens-in-unified-service-desk"></a><span data-ttu-id="a70e8-103">Customize login and splash screens in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="a70e8-103">Customize login and splash screens in Unified Service Desk</span></span>
<span data-ttu-id="a70e8-104">You can customize the branding of [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] login and splash screens to change the name and appearance of the application name on the login screen and change the application name, appearance, foreground and background colors of the splash screen by modifying XAML styles.</span><span class="sxs-lookup"><span data-stu-id="a70e8-104">You can customize the branding of [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] login and splash screens to change the name and appearance of the application name on the login screen and change the application name, appearance, foreground and background colors of the splash screen by modifying XAML styles.</span></span>  
  
<a name="What"></a>   
## <a name="what-you-can-customize"></a><span data-ttu-id="a70e8-105">What you can customize?</span><span class="sxs-lookup"><span data-stu-id="a70e8-105">What you can customize?</span></span>  
 <span data-ttu-id="a70e8-106">The following XAML is used to customize the branding of login and splash screens in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="a70e8-106">The following XAML is used to customize the branding of login and splash screens in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  
  
```xaml  
<ResourceDictionary xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"  
                    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"  
                    xmlns:resx1="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Properties">  
  
  <Style x:Key="FormAppNameStyle" TargetType="TextBlock">  
    <Setter Property="Foreground" Value="Black"></Setter>  
    <Setter Property="FontFamily" Value="Segoe UI"></Setter>  
    <Setter Property="FontSize" Value="30"></Setter>  
    <Setter Property="Background" Value="White"></Setter>  
    <Setter Property="Text" Value="Unified Service Desk"></Setter>  
  </Style>  
  
  <Style x:Key="SplashAppNameStyle" TargetType="Label">  
    <Setter Property="Foreground" Value="White"></Setter>  
    <Setter Property="FontFamily" Value="/UnifiedServiceDesk;component/Fonts/#Segoe UI"></Setter>  
    <Setter Property="FontSize" Value="40"></Setter>  
    <Setter Property="Content" Value="Unified Service Desk"></Setter>  
  </Style>  
  
  <Style x:Key="SplashScreenDefaultFontStyle" TargetType="TextBlock">  
    <Setter Property="FontSize" Value="12px"/>  
    <Setter Property="Foreground" Value="White"/>  
    <Setter Property="TextWrapping" Value="Wrap"/>  
    <Setter Property="TextTrimming" Value="WordEllipsis"/>  
    <Setter Property="FontFamily" Value="Segoe UI"/>  
  </Style>  
  
  <Style x:Key="SplashGridBgColor" TargetType="Grid">  
    <Setter Property="Background" Value="Blue"></Setter>  
  </Style>  
  
</ResourceDictionary>  
```  
  
 <span data-ttu-id="a70e8-107">The XAML file contains the following four styles for which you must specify appropriate values in the `Setter Property`:</span><span class="sxs-lookup"><span data-stu-id="a70e8-107">The XAML file contains the following four styles for which you must specify appropriate values in the `Setter Property`:</span></span>  
  
|<span data-ttu-id="a70e8-108">XAML Style</span><span class="sxs-lookup"><span data-stu-id="a70e8-108">XAML Style</span></span>|<span data-ttu-id="a70e8-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a70e8-109">Description</span></span>|  
|----------------|-----------------|  
|<span data-ttu-id="a70e8-110">FormAppNameStyle</span><span class="sxs-lookup"><span data-stu-id="a70e8-110">FormAppNameStyle</span></span>|<span data-ttu-id="a70e8-111">Change the content and appearance of application name on login screen.</span><span class="sxs-lookup"><span data-stu-id="a70e8-111">Change the content and appearance of application name on login screen.</span></span>|  
|<span data-ttu-id="a70e8-112">SplashAppNameStyle</span><span class="sxs-lookup"><span data-stu-id="a70e8-112">SplashAppNameStyle</span></span>|<span data-ttu-id="a70e8-113">Change the content and appearance of application name on splash screen.</span><span class="sxs-lookup"><span data-stu-id="a70e8-113">Change the content and appearance of application name on splash screen.</span></span>|  
|<span data-ttu-id="a70e8-114">SplashScreenDefaultFontStyle</span><span class="sxs-lookup"><span data-stu-id="a70e8-114">SplashScreenDefaultFontStyle</span></span>|<span data-ttu-id="a70e8-115">Change the appearance of status text on splash screen.</span><span class="sxs-lookup"><span data-stu-id="a70e8-115">Change the appearance of status text on splash screen.</span></span>|  
|<span data-ttu-id="a70e8-116">SplashGridBgColor</span><span class="sxs-lookup"><span data-stu-id="a70e8-116">SplashGridBgColor</span></span>|<span data-ttu-id="a70e8-117">Change the background color of splash screen.</span><span class="sxs-lookup"><span data-stu-id="a70e8-117">Change the background color of splash screen.</span></span>|  
  
<a name="How"></a>   
## <a name="how-you-can-customize"></a><span data-ttu-id="a70e8-118">How you can customize?</span><span class="sxs-lookup"><span data-stu-id="a70e8-118">How you can customize?</span></span>  
 <span data-ttu-id="a70e8-119">You can customize the  branding of login and splash screens in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] by following the steps below.</span><span class="sxs-lookup"><span data-stu-id="a70e8-119">You can customize the  branding of login and splash screens in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] by following the steps below.</span></span>  
  
1. <span data-ttu-id="a70e8-120">Open Notepad, and copy the entire contents of the XAML file mentioned in the previous section.</span><span class="sxs-lookup"><span data-stu-id="a70e8-120">Open Notepad, and copy the entire contents of the XAML file mentioned in the previous section.</span></span>  
  
2. <span data-ttu-id="a70e8-121">Under the appropriate XAML style block, change the `Value` of appropriate `Setter Property`.</span><span class="sxs-lookup"><span data-stu-id="a70e8-121">Under the appropriate XAML style block, change the `Value` of appropriate `Setter Property`.</span></span>  
  
    <span data-ttu-id="a70e8-122">For example, to modify the font size of the app name displayed on the splash screen, change the value of the `FontSize` setter property under the `SplashAppNameStyle` style.</span><span class="sxs-lookup"><span data-stu-id="a70e8-122">For example, to modify the font size of the app name displayed on the splash screen, change the value of the `FontSize` setter property under the `SplashAppNameStyle` style.</span></span>  
  
    <span data-ttu-id="a70e8-123">You can modify values for multiple setter properties under a XAML style or across multiple XAML styles.</span><span class="sxs-lookup"><span data-stu-id="a70e8-123">You can modify values for multiple setter properties under a XAML style or across multiple XAML styles.</span></span>  
  
3. <span data-ttu-id="a70e8-124">If you haven't changed setter property values under a XAML style, remove the style block from the Notepad file.</span><span class="sxs-lookup"><span data-stu-id="a70e8-124">If you haven't changed setter property values under a XAML style, remove the style block from the Notepad file.</span></span>  
  
    <span data-ttu-id="a70e8-125">For example, if you just changed setter properties for `SplashAppNameStyle`, remove the other styles to prevent the settings under those styles being applied to your client application.</span><span class="sxs-lookup"><span data-stu-id="a70e8-125">For example, if you just changed setter properties for `SplashAppNameStyle`, remove the other styles to prevent the settings under those styles being applied to your client application.</span></span> <span data-ttu-id="a70e8-126">See examples later in this topic.</span><span class="sxs-lookup"><span data-stu-id="a70e8-126">See examples later in this topic.</span></span>  
  
4. <span data-ttu-id="a70e8-127">Save the file as "CustomerSplashStyles.xaml".</span><span class="sxs-lookup"><span data-stu-id="a70e8-127">Save the file as "CustomerSplashStyles.xaml".</span></span>  
  
5. <span data-ttu-id="a70e8-128">Copy the "CustomerSplashStyles.xaml" to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client directory, typically "C:\Program Files\Microsoft Dynamics CRM USD\USD".</span><span class="sxs-lookup"><span data-stu-id="a70e8-128">Copy the "CustomerSplashStyles.xaml" to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client directory, typically "C:\Program Files\Microsoft Dynamics CRM USD\USD".</span></span> <span data-ttu-id="a70e8-129">You must have system administrator privileges to copy the file to the client directory.</span><span class="sxs-lookup"><span data-stu-id="a70e8-129">You must have system administrator privileges to copy the file to the client directory.</span></span>  
  
6. <span data-ttu-id="a70e8-130">If you are running the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client, restart it for the changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="a70e8-130">If you are running the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client, restart it for the changes to take effect.</span></span>  
  
<a name="Examples"></a>   
## <a name="customization-examples"></a><span data-ttu-id="a70e8-131">Customization examples</span><span class="sxs-lookup"><span data-stu-id="a70e8-131">Customization examples</span></span>  
 <span data-ttu-id="a70e8-132">Here are some customization examples.</span><span class="sxs-lookup"><span data-stu-id="a70e8-132">Here are some customization examples.</span></span>  
  
### <a name="change-the-application-name-of-login-screen"></a><span data-ttu-id="a70e8-133">Change the application name of login screen</span><span class="sxs-lookup"><span data-stu-id="a70e8-133">Change the application name of login screen</span></span>  
 <span data-ttu-id="a70e8-134">Update the contents of the `CustomerSplashStyles.xaml` file to the following:</span><span class="sxs-lookup"><span data-stu-id="a70e8-134">Update the contents of the `CustomerSplashStyles.xaml` file to the following:</span></span>  
  
```  
<ResourceDictionary xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"  
                    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"  
                    xmlns:resx1="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Properties">  
  
  <Style x:Key="FormAppNameStyle" TargetType="TextBlock">  
    <Setter Property="Foreground" Value="Blue"></Setter>  
    <Setter Property="FontFamily" Value="Segoe UI"></Setter>  
    <Setter Property="FontSize" Value="40"></Setter>  
    <Setter Property="Background" Value="White"></Setter>  
    <Setter Property="Text" Value="Contoso, Ltd."></Setter>  
  </Style>  
  
</ResourceDictionary>  
```  
  
 <span data-ttu-id="a70e8-135">This will be the customization outcome:</span><span class="sxs-lookup"><span data-stu-id="a70e8-135">This will be the customization outcome:</span></span>  
  
 <span data-ttu-id="a70e8-136">![Custom app name in the login screen](../unified-service-desk/media/usd-loginscreencustomization.png "Custom app name in the login screen")</span><span class="sxs-lookup"><span data-stu-id="a70e8-136">![Custom app name in the login screen](../unified-service-desk/media/usd-loginscreencustomization.png "Custom app name in the login screen")</span></span>  
  
### <a name="change-the-application-name-and-appearance-of-splash-screen"></a><span data-ttu-id="a70e8-137">Change the application name and appearance of splash screen</span><span class="sxs-lookup"><span data-stu-id="a70e8-137">Change the application name and appearance of splash screen</span></span>  
 <span data-ttu-id="a70e8-138">Update the contents of the `CustomerSplashStyles.xaml` file to the following:</span><span class="sxs-lookup"><span data-stu-id="a70e8-138">Update the contents of the `CustomerSplashStyles.xaml` file to the following:</span></span>  
  
```xaml  
<ResourceDictionary xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"  
                    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"  
                    xmlns:resx1="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Properties">  
  
  <Style x:Key="SplashAppNameStyle" TargetType="Label">  
    <Setter Property="Foreground" Value="Blue"></Setter>  
    <Setter Property="FontFamily" Value="/UnifiedServiceDesk;component/Fonts/#Segoe UI"></Setter>  
    <Setter Property="FontSize" Value="40"></Setter>  
    <Setter Property="Content" Value="Contoso, Ltd."></Setter>  
  </Style>  
  
  <Style x:Key="SplashScreenDefaultFontStyle" TargetType="TextBlock">  
    <Setter Property="FontSize" Value="14px"/>  
    <Setter Property="Foreground" Value="Black"/>  
    <Setter Property="TextWrapping" Value="Wrap"/>  
    <Setter Property="TextTrimming" Value="WordEllipsis"/>  
    <Setter Property="FontFamily" Value="Calibri"/>  
  </Style>  
  
  <Style x:Key="SplashGridBgColor" TargetType="Grid">  
    <Setter Property="Background" Value="Gray"></Setter>  
  </Style>  
  
</ResourceDictionary>  
```  
  
 <span data-ttu-id="a70e8-139">This will be the customization outcome:</span><span class="sxs-lookup"><span data-stu-id="a70e8-139">This will be the customization outcome:</span></span>  
  
 <span data-ttu-id="a70e8-140">![Custom splash screen](../unified-service-desk/media/usd-customsplashscreen.png "Custom splash screen")</span><span class="sxs-lookup"><span data-stu-id="a70e8-140">![Custom splash screen](../unified-service-desk/media/usd-customsplashscreen.png "Custom splash screen")</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="a70e8-141">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a70e8-141">See also</span></span>  
 [<span data-ttu-id="a70e8-142">Customize themes in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="a70e8-142">Customize themes in Unified Service Desk</span></span>](../unified-service-desk/customize-themes-in-unified-service-desk.md)
