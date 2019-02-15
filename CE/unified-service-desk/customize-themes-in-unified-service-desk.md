---
title: Customize themes in Unified Service Desk | MicrosoftDocs
description: Themes in Unified Service Desk define the look and feel of the agent application. A theme in Unified Service Desk consists of a XAML resource library, and can be placed on any web server and referenced via URL or can be compile into .NET assemblies (dll), and distributed with the agent applications.
keywords: ''
ms.date: 08/17/2018
ms.service:
- dynamics-365-customerservice
ms.custom:
- dyn365-USD
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 27b60bcc-787e-451d-b795-be9b0efbc57d
author: kabala123
ms.author: kabala
manager: shujoshi
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: a806ae95a2a23c14934d798e104ad7d5a1dcb4b8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385846"
---
# <a name="customize-themes-in-unified-service-desk"></a><span data-ttu-id="a95fe-104">Customize themes in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="a95fe-104">Customize themes in Unified Service Desk</span></span>
<span data-ttu-id="a95fe-105">Các chủ đề trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] xác định giao diện của ứng dụng tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="a95fe-105">Themes in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] define the look and feel of the agent application.</span></span> <span data-ttu-id="a95fe-106">Một chủ đề trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] bao gồm một thư viện tài nguyên XAML và có thể được đặt trên bất kỳ máy chủ web nào và được tham chiếu thông qua URL hoặc có thể được tạo thành cụm .NET (dll) và phân phối với các ứng dụng tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="a95fe-106">A theme in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] consists of a XAML resource library, and can be placed on any web server and referenced via URL or can be compile into .NET assemblies (dll), and distributed with the agent applications.</span></span>  
  
  <span data-ttu-id="a95fe-107">The predefined [Air Theme](../unified-service-desk/customize-themes-in-unified-service-desk.md#AirTheme) supports the high-contrast mode.</span><span class="sxs-lookup"><span data-stu-id="a95fe-107">The predefined [Air Theme](../unified-service-desk/customize-themes-in-unified-service-desk.md#AirTheme) supports the high-contrast mode.</span></span> <span data-ttu-id="a95fe-108">The high-contrast mode in [!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] helps you read the text on screen clearly by increasing the color contrast.</span><span class="sxs-lookup"><span data-stu-id="a95fe-108">The high-contrast mode in [!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] helps you read the text on screen clearly by increasing the color contrast.</span></span> <span data-ttu-id="a95fe-109">When you turn on high-contrast mode on your computer and are using the  `Air Theme`, the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client will automatically switch to the high-contrast mode.</span><span class="sxs-lookup"><span data-stu-id="a95fe-109">When you turn on high-contrast mode on your computer and are using the  `Air Theme`, the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client will automatically switch to the high-contrast mode.</span></span> <span data-ttu-id="a95fe-110">Similarly, disabling the high-contrast mode on your computer will cause the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to automatically switch to the normal display mode.</span><span class="sxs-lookup"><span data-stu-id="a95fe-110">Similarly, disabling the high-contrast mode on your computer will cause the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to automatically switch to the normal display mode.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a95fe-111">The automatic switching between normal and high-contrast modes in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client is supported only for the  predefined [Air Theme](../unified-service-desk/customize-themes-in-unified-service-desk.md#AirTheme).</span><span class="sxs-lookup"><span data-stu-id="a95fe-111">The automatic switching between normal and high-contrast modes in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client is supported only for the  predefined [Air Theme](../unified-service-desk/customize-themes-in-unified-service-desk.md#AirTheme).</span></span> <span data-ttu-id="a95fe-112">If you are using custom themes or custom hosted controls that supports high-contrast mode, the switching happens only after you restart the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client after switching to normal or high-contrast mode on your computer.</span><span class="sxs-lookup"><span data-stu-id="a95fe-112">If you are using custom themes or custom hosted controls that supports high-contrast mode, the switching happens only after you restart the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client after switching to normal or high-contrast mode on your computer.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a95fe-113">[High-contrast mode support  for custom themes](#HighContrast)</span><span class="sxs-lookup"><span data-stu-id="a95fe-113">[High-contrast mode support  for custom themes](#HighContrast)</span></span>  
  
<a name="PredefinedThemes"></a>   
## <a name="predefined-themes-available-in-unified-service-desk"></a><span data-ttu-id="a95fe-114">Chủ đề xác định trước có sẵn trong Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="a95fe-114">Predefined Themes available in Unified Service Desk</span></span>  
 [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]<span data-ttu-id="a95fe-115">đi kèm với ba chủ đề được xác định trước.</span><span class="sxs-lookup"><span data-stu-id="a95fe-115">comes with three predefined themes.</span></span>  

::: moniker range=">=dynamics-usd-4"

<a name="UnifiedBlueTheme"></a>   
### <a name="unified-blue-theme"></a><span data-ttu-id="a95fe-116">Unified Blue Theme</span><span class="sxs-lookup"><span data-stu-id="a95fe-116">Unified Blue Theme</span></span>

<span data-ttu-id="a95fe-117">This is Unified Blue theme, which is the predefined theme for Unified Service Desk when you are using Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="a95fe-117">This is Unified Blue theme, which is the predefined theme for Unified Service Desk when you are using Unified Interface App.</span></span>

<span data-ttu-id="a95fe-118">![Unified Blue in Unified Service Desk](media/unified-blue-theme.png "Unified Blue in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="a95fe-118">![Unified Blue in Unified Service Desk](media/unified-blue-theme.png "Unified Blue in Unified Service Desk")</span></span> 

::: moniker-end

<a name="AirTheme"></a>   
### <a name="air-theme"></a><span data-ttu-id="a95fe-119">Chủ đề về không khí</span><span class="sxs-lookup"><span data-stu-id="a95fe-119">Air Theme</span></span>  
 <span data-ttu-id="a95fe-120">Đây là chủ đề về không khí.</span><span class="sxs-lookup"><span data-stu-id="a95fe-120">This is the Air theme.</span></span> <span data-ttu-id="a95fe-121">This theme supports high-contrast mode.</span><span class="sxs-lookup"><span data-stu-id="a95fe-121">This theme supports high-contrast mode.</span></span>  
  
 <span data-ttu-id="a95fe-122">![Air theme in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-themeair.png "Air theme in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="a95fe-122">![Air theme in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-themeair.png "Air theme in Unified Service Desk")</span></span>  
  
### <a name="blue-theme"></a><span data-ttu-id="a95fe-123">Chủ đề màu xanh</span><span class="sxs-lookup"><span data-stu-id="a95fe-123">Blue Theme</span></span>  
 <span data-ttu-id="a95fe-124">Đây là chủ đề màu xanh.</span><span class="sxs-lookup"><span data-stu-id="a95fe-124">This is the Blue theme.</span></span> <span data-ttu-id="a95fe-125">This theme doesn't support high-contrast setting, and is deprecated in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] 2.2 release.</span><span class="sxs-lookup"><span data-stu-id="a95fe-125">This theme doesn't support high-contrast setting, and is deprecated in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] 2.2 release.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a95fe-126">[Blog: Deprecating some predefined Unified Service Desk themes](https://blogs.msdn.microsoft.com/usd/2016/08/24/deprecating-some-predefined-unified-service-desk-themes/)</span><span class="sxs-lookup"><span data-stu-id="a95fe-126">[Blog: Deprecating some predefined Unified Service Desk themes](https://blogs.msdn.microsoft.com/usd/2016/08/24/deprecating-some-predefined-unified-service-desk-themes/)</span></span>  
  
 <span data-ttu-id="a95fe-127">![Blue theme in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-themeblue.png "Blue theme in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="a95fe-127">![Blue theme in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-themeblue.png "Blue theme in Unified Service Desk")</span></span>  
  
### <a name="style-theme"></a><span data-ttu-id="a95fe-128">Style Theme</span><span class="sxs-lookup"><span data-stu-id="a95fe-128">Style Theme</span></span>  
 <span data-ttu-id="a95fe-129">This is the Style theme.</span><span class="sxs-lookup"><span data-stu-id="a95fe-129">This is the Style theme.</span></span> <span data-ttu-id="a95fe-130">This theme doesn't support high-contrast setting, and is deprecated in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] 2.2 release.</span><span class="sxs-lookup"><span data-stu-id="a95fe-130">This theme doesn't support high-contrast setting, and is deprecated in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] 2.2 release.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a95fe-131">[Blog: Deprecating some predefined Unified Service Desk themes](https://blogs.msdn.microsoft.com/usd/2016/08/24/deprecating-some-predefined-unified-service-desk-themes/)</span><span class="sxs-lookup"><span data-stu-id="a95fe-131">[Blog: Deprecating some predefined Unified Service Desk themes](https://blogs.msdn.microsoft.com/usd/2016/08/24/deprecating-some-predefined-unified-service-desk-themes/)</span></span>  
  
 <span data-ttu-id="a95fe-132">![Style theme in Unified Service Desk](../unified-service-desk/media/crmusd-theme-style.png "Style theme in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="a95fe-132">![Style theme in Unified Service Desk](../unified-service-desk/media/crmusd-theme-style.png "Style theme in Unified Service Desk")</span></span>  
  
<a name="SetPredefinedTheme"></a>   
## <a name="set-a-predefined-theme"></a><span data-ttu-id="a95fe-133">Đặt chủ đề được xác định trước</span><span class="sxs-lookup"><span data-stu-id="a95fe-133">Set a predefined theme</span></span>  
 <span data-ttu-id="a95fe-134">Thao tác **SetTheme** cho kiểm soát tổ chức trình quản lý chung cho phép bạn thiết lập một chủ đề trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="a95fe-134">The **SetTheme** action for the Global Manager hosted control lets you set a theme in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="a95fe-135">You can create an action call to the **SetTheme** action, and pass the predefined theme call in the **Data** field using the following syntax to set one of the predefined themes:</span><span class="sxs-lookup"><span data-stu-id="a95fe-135">You can create an action call to the **SetTheme** action, and pass the predefined theme call in the **Data** field using the following syntax to set one of the predefined themes:</span></span>  
  
```  
/UnifiedServiceDesk;component/Styles/<Theme_Style>.xaml  
```  
  
 <span data-ttu-id="a95fe-136">Bảng dưới đây cung cấp các cú pháp cho trường **dữ liệu** trong cuộc gọi hành động của bạn để thiết lập một chủ đề được xác định trước:</span><span class="sxs-lookup"><span data-stu-id="a95fe-136">The following table provides the syntax for the **Data** field in your action call to set a predefined theme:</span></span>  
  
|<span data-ttu-id="a95fe-137">Chủ đề</span><span class="sxs-lookup"><span data-stu-id="a95fe-137">Theme</span></span>|<span data-ttu-id="a95fe-138">Cú pháp cho trường dữ liệu</span><span class="sxs-lookup"><span data-stu-id="a95fe-138">Syntax for the Data field</span></span>|  
|-----------|-------------------------------|  
|<span data-ttu-id="a95fe-139">Không khí</span><span class="sxs-lookup"><span data-stu-id="a95fe-139">Air</span></span>|<span data-ttu-id="a95fe-140">/UnifiedServiceDesk;component/Styles/AirStyle.XAML</span><span class="sxs-lookup"><span data-stu-id="a95fe-140">/UnifiedServiceDesk;component/Styles/AirStyle.xaml</span></span>|  
|<span data-ttu-id="a95fe-141">Màu xanh</span><span class="sxs-lookup"><span data-stu-id="a95fe-141">Blue</span></span>|<span data-ttu-id="a95fe-142">/UnifiedServiceDesk;component/Styles/BlueStyle.xaml</span><span class="sxs-lookup"><span data-stu-id="a95fe-142">/UnifiedServiceDesk;component/Styles/BlueStyle.xaml</span></span>|  
|<span data-ttu-id="a95fe-143">Kiểu</span><span class="sxs-lookup"><span data-stu-id="a95fe-143">Style</span></span>|<span data-ttu-id="a95fe-144">/UnifiedServiceDesk;component/Styles/Style.xaml</span><span class="sxs-lookup"><span data-stu-id="a95fe-144">/UnifiedServiceDesk;component/Styles/Style.xaml</span></span>|  
  
 <span data-ttu-id="a95fe-145">Trong mẫu [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] ứng dụng khách, tổng đài viên có thể thiết lập chủ đề bằng cách nhấp vào mũi tên xuống bên cạnh biểu tượng cài đặt ở góc trên cùng bên phải, sau đó lựa chọn một chủ đề được xác định trước từ menu phụ **đặt chủ đề**.</span><span class="sxs-lookup"><span data-stu-id="a95fe-145">In the sample [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, agents can set the theme by clicking the down arrow next to the settings icon at the top-right corner, and then selecting a predefined theme from the **Set Theme** submenu.</span></span>  
  
 <span data-ttu-id="a95fe-146">Nhấn vào một chủ đề trong menu phụ **đặt chủ đề** sẽ thực hiện cuộc gọi hành động đến thao tác **SetTheme** với cú pháp thích hợp trong trường **dữ liệu** như đã đề cập trước đó.</span><span class="sxs-lookup"><span data-stu-id="a95fe-146">Clicking a theme in the **Set Theme** submenu makes an action call to the **SetTheme** action with the appropriate syntax in the **Data** field as mentioned earlier.</span></span> <span data-ttu-id="a95fe-147">Ví dụ, đây là định nghĩa cuộc gọi hành động cho kiểu chủ đề về không khí:</span><span class="sxs-lookup"><span data-stu-id="a95fe-147">For example, this is the action call definition for the Air style:</span></span>  
  
 <span data-ttu-id="a95fe-148">![Action call definition for Air theme](../unified-service-desk/media/crm-itpro-usd-actioncallforairstyle.png "Action call definition for Air theme")</span><span class="sxs-lookup"><span data-stu-id="a95fe-148">![Action call definition for Air theme](../unified-service-desk/media/crm-itpro-usd-actioncallforairstyle.png "Action call definition for Air theme")</span></span>  
  
<a name="Customize"></a>   
## <a name="customize-themes-in-unified-service-desk"></a><span data-ttu-id="a95fe-149">Customize themes in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="a95fe-149">Customize themes in Unified Service Desk</span></span>  
 <span data-ttu-id="a95fe-150">Ngoài việc có thể để lựa chọn từ nhiều chủ đề khác nhau được xác định trước, bạn có thể tùy chỉnh chủ đề trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="a95fe-150">Apart from being able to choose from various predefined themes, you can customize a theme in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="a95fe-151">This is done by updating selective controls and then merging it with the existing theme in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to customize the appearance.</span><span class="sxs-lookup"><span data-stu-id="a95fe-151">This is done by updating selective controls and then merging it with the existing theme in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to customize the appearance.</span></span> [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="a95fe-152">provides a default style (XAML file) and a bunch of XAML brush resources that you can use to understand the various WPF controls and layout that define the appearance of your agent application.</span><span class="sxs-lookup"><span data-stu-id="a95fe-152">provides a default style (XAML file) and a bunch of XAML brush resources that you can use to understand the various WPF controls and layout that define the appearance of your agent application.</span></span> <span data-ttu-id="a95fe-153">You can find the default style for [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application, **DefaultStyle.xaml**, along with other XAML brush resources in the [!INCLUDE[pn_user_interface_integration](../includes/pn-user-interface-integration.md)] SDK download package.</span><span class="sxs-lookup"><span data-stu-id="a95fe-153">You can find the default style for [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application, **DefaultStyle.xaml**, along with other XAML brush resources in the [!INCLUDE[pn_user_interface_integration](../includes/pn-user-interface-integration.md)] SDK download package.</span></span> <span data-ttu-id="a95fe-154">[Download](http://go.microsoft.com/fwlink/p/?LinkId=395257) the package, and extract it to view the file and its contents under the "UII\USD Developer Assets\USD Layout and Style Sheet" directory.</span><span class="sxs-lookup"><span data-stu-id="a95fe-154">[Download](http://go.microsoft.com/fwlink/p/?LinkId=395257) the package, and extract it to view the file and its contents under the "UII\USD Developer Assets\USD Layout and Style Sheet" directory.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a95fe-155">Ghi mã lệnh WPF và XAML là kỹ năng cần thiết cần thiết để tuỳ chỉnh hiển thị các ứng dụng tác nhân của bạn bằng cách thực hiện thao tác điều khiển trong tệp XAML.</span><span class="sxs-lookup"><span data-stu-id="a95fe-155">WPF and XAML scripting are essential skills required for customizing the display of your agent applications by manipulating controls in a XAML file.</span></span>  
  
 <span data-ttu-id="a95fe-156">Use the **SetTheme** action for the Global Manager hosted application to customize the default style of the agent application.</span><span class="sxs-lookup"><span data-stu-id="a95fe-156">Use the **SetTheme** action for the Global Manager hosted application to customize the default style of the agent application.</span></span> [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="a95fe-157">supports merging of your customizations with the existing theme or display style of the agent application.</span><span class="sxs-lookup"><span data-stu-id="a95fe-157">supports merging of your customizations with the existing theme or display style of the agent application.</span></span> <span data-ttu-id="a95fe-158">Điều này có hiệu quả có nghĩa là bạn chỉ cần xác định các điều khiển hoặc các khu vực mà bạn muốn thay đổi cùng với khối tham khảo ResourceDictionary để tùy chỉnh kiểu hiển thị sẵn có.</span><span class="sxs-lookup"><span data-stu-id="a95fe-158">This effectively means that you just need to specify the controls or areas that you want to be changed along with the ResourceDictionary reference block to customize an existing display style.</span></span> <span data-ttu-id="a95fe-159">For general information about ResourceDictionary, click [ResourceDictionary and XAML resource references](https://msdn.microsoft.com/library/windows/apps/Hh968442.aspx).</span><span class="sxs-lookup"><span data-stu-id="a95fe-159">For general information about ResourceDictionary, click [ResourceDictionary and XAML resource references](https://msdn.microsoft.com/library/windows/apps/Hh968442.aspx).</span></span>  
  
 <span data-ttu-id="a95fe-160">Hãy để chúng tôi tạo ra cuộc gọi thao tác để thay đổi văn bản trong tiêu đề và màu nền của ứng dụng tác nhân thành màu vàng.</span><span class="sxs-lookup"><span data-stu-id="a95fe-160">Let us create an action call to change the text in the title and the skin color of the agent application to Yellow.</span></span> <span data-ttu-id="a95fe-161">Đảm bảo rằng bạn có sẵn tệp DefaultStyle.xaml vì chúng tôi sẽ cần đến tệp đó.</span><span class="sxs-lookup"><span data-stu-id="a95fe-161">Make sure you have the DefaultStyle.xaml file handy as we will need it.</span></span>  
  
1. <span data-ttu-id="a95fe-162">Đăng nhập vào ứng dụng Microsoft Dynamics 365 for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="a95fe-162">Sign in to Microsoft Dynamics 365 for Customer Engagement apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="a95fe-163">Click **Action Calls**.</span><span class="sxs-lookup"><span data-stu-id="a95fe-163">Click **Action Calls**.</span></span>  
  
4. <span data-ttu-id="a95fe-164">Bấm vào **MỚI** để tạo cuộc gọi thao tác.</span><span class="sxs-lookup"><span data-stu-id="a95fe-164">Click **NEW** to create an action call.</span></span>  
  
5. <span data-ttu-id="a95fe-165">Trên trang **Cuộc gọi thao tác mới**, đặt các thuộc tính chung:</span><span class="sxs-lookup"><span data-stu-id="a95fe-165">On the **New Action Call** page, set the general properties:</span></span>  
  
   1.  <span data-ttu-id="a95fe-166">Trong trường **tên**, nhập **Cuộc gọi thao tác cho hiển thị tùy chỉnh**.</span><span class="sxs-lookup"><span data-stu-id="a95fe-166">In the **Name** field, type **Action Call for Custom Display**.</span></span>  
  
   2.  <span data-ttu-id="a95fe-167">In the **Hosted Control** field, select **Dynamics 365 for Customer Engagement apps Global Manager**.</span><span class="sxs-lookup"><span data-stu-id="a95fe-167">In the **Hosted Control** field, select **Dynamics 365 for Customer Engagement apps Global Manager**.</span></span> <span data-ttu-id="a95fe-168">Nếu có một tên khác nhau cho loại kiểm soát tổ chức của trình quản lý chung của bạn, hãy chỉ định tên đó để thay thế.</span><span class="sxs-lookup"><span data-stu-id="a95fe-168">If you have a different name for your Global Manager hosted control type, specify that name instead.</span></span>  
  
   3.  <span data-ttu-id="a95fe-169">Trong trường **Thao tác**, chọn **SetTheme**.</span><span class="sxs-lookup"><span data-stu-id="a95fe-169">In the **Action** field, select **SetTheme**.</span></span>  
  
6. <span data-ttu-id="a95fe-170">Bây giờ, chúng tôi sẽ đặt các tham số để tuỳ chỉnh màn hình.</span><span class="sxs-lookup"><span data-stu-id="a95fe-170">Now, we will set the parameter for customizing the display.</span></span> <span data-ttu-id="a95fe-171">Trong trường **dữ liệu**, sao chép tài liệu tham khảo ResourceDictionary sau đây:</span><span class="sxs-lookup"><span data-stu-id="a95fe-171">In the **Data** field, copy the following ResourceDictionary reference:</span></span>  
  
   ```  
  
   <ResourceDictionary xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"  
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"  
        xmlns:Microsoft_Windows_Themes="clr-namespace:Microsoft.Windows.Themes;assembly=PresentationFramework.Classic"  
        xmlns:themes="clr-namespace:Microsoft.Windows.Themes;assembly=PresentationFramework.Luna"  
        xmlns:ribbon="clr-namespace:Microsoft.Windows.Controls.Ribbon;assembly=RibbonControlsLibrary"  
        xmlns:classic="clr-namespace:Microsoft.Windows.Themes;assembly=PresentationFramework.Classic"  
        xmlns:shell="clr-namespace:Microsoft.Windows.Shell;assembly=Microsoft.Windows.Shell"  
        xmlns:system="clr-namespace:System;assembly=mscorlib">  
   ```  
  
   > [!IMPORTANT]
   >  <span data-ttu-id="a95fe-172">This `ResourceDictionary` reference must be included in every action call that you use to customize the default style.</span><span class="sxs-lookup"><span data-stu-id="a95fe-172">This `ResourceDictionary` reference must be included in every action call that you use to customize the default style.</span></span>  
  
7. <span data-ttu-id="a95fe-173">Sao chép các lệnh sau đây trong trường **dữ liệu** sau khi tài liệu tham khảo ResourceDictionary mà bạn đã sao chép trước đó.</span><span class="sxs-lookup"><span data-stu-id="a95fe-173">Copy the following command in the **Data** field after the ResourceDictionary reference that you copied earlier.</span></span>  
  
   ```  
   <SolidColorBrush x:Key="WindowBackgroundStyle" Color="Yellow"/>  
   ```  
  
    <span data-ttu-id="a95fe-174">Điều này sẽ thay đổi màu nền của ứng dụng tác nhân sang màu vàng.</span><span class="sxs-lookup"><span data-stu-id="a95fe-174">This will change the skin of the agent application to Yellow.</span></span> <span data-ttu-id="a95fe-175">You will find this command to set the background color in the `<!-- Region General -->` section in the `DefaultStyle.xaml` file.</span><span class="sxs-lookup"><span data-stu-id="a95fe-175">You will find this command to set the background color in the `<!-- Region General -->` section in the `DefaultStyle.xaml` file.</span></span>  
  
8. <span data-ttu-id="a95fe-176">Sao chép lệnh sau đây sau lệnh mà bạn sao chép ở bước trước:</span><span class="sxs-lookup"><span data-stu-id="a95fe-176">Copy the following command after the command that you copied in the previous step:</span></span>  
  
   ```  
   <Style x:Key="MainWindow" TargetType="{x:Type Window}" BasedOn="{StaticResource {x:Type Window}}">  
       <Setter Property="Title" Value="CUSTOM TITLE: Agent Application for CONTOSO INC."/>  
       <Setter Property="Icon" Value="/UnifiedServiceDesk;component/imageResources/dynamics16-32-48-256.ico"/>  
       <Setter Property="FontFamily" Value="Segoe UI" />  
   </Style>  
   ```  
  
    <span data-ttu-id="a95fe-177">Điều này sẽ thay đổi văn bản trong thanh tiêu đề "TÙY CHỈNH TIÊU ĐỀ: Ứng dụng tác nhân cho CONTOSO Inc".</span><span class="sxs-lookup"><span data-stu-id="a95fe-177">This will change the text in the title bar to “CUSTOM TITLE: Agent Application for CONTOSO INC.”.</span></span> <span data-ttu-id="a95fe-178">Bạn sẽ tìm thấy lệnh này để đặt tiêu đề cửa sổ trong `<!-- Region Window --> section in the DefaultStyle.xaml file.`</span><span class="sxs-lookup"><span data-stu-id="a95fe-178">You will find this command to set the Window title in the `<!-- Region Window --> section in the DefaultStyle.xaml file.`</span></span>  
  
9. <span data-ttu-id="a95fe-179">Đóng thẻ ResourceDictionary bằng cách thêm mục sau vào cuối trường **dữ liệu**:</span><span class="sxs-lookup"><span data-stu-id="a95fe-179">Close the ResourceDictionary tag by adding the following at the end of the **Data** field:</span></span>  
  
    ```  
    </ResourceDictionary>  
    ```  
  
     <span data-ttu-id="a95fe-180">Đây là cách xác định định nghĩa cuộc gọi thao tác:</span><span class="sxs-lookup"><span data-stu-id="a95fe-180">This is how your action call definition looks like:</span></span>  
  
   <span data-ttu-id="a95fe-181">![Define action call for customizing display](../unified-service-desk/media/crm-itpro-usd-customizedisplay01.png "Define action call for customizing display")</span><span class="sxs-lookup"><span data-stu-id="a95fe-181">![Define action call for customizing display](../unified-service-desk/media/crm-itpro-usd-customizedisplay01.png "Define action call for customizing display")</span></span>  
  
10. <span data-ttu-id="a95fe-182">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a95fe-182">Click **Save**.</span></span>  
  
    <span data-ttu-id="a95fe-183">Bạn đã hoàn tất và bây giờ hãy sẵn sàng để thử nghiệm cuộc gọi thao tác trong ứng dụng tác nhân.</span><span class="sxs-lookup"><span data-stu-id="a95fe-183">You are done, and now ready to test the action call in the agent application.</span></span>  
  
<a name="Test"></a>   
## <a name="test-the-action-call-for-customizing-your-display"></a><span data-ttu-id="a95fe-184">Kiểm tra cuộc gọi hành động để tuỳ chỉnh màn hình của bạn</span><span class="sxs-lookup"><span data-stu-id="a95fe-184">Test the action call for customizing your display</span></span>  
 <span data-ttu-id="a95fe-185">Bạn có thể gọi thao tác này bằng cách tạo nút thanh công cụ, sau đó gắn cuộc gọi hành động vào nút đó.</span><span class="sxs-lookup"><span data-stu-id="a95fe-185">You can call this action call by creating a toolbar button, and then attaching the action call to it.</span></span> <span data-ttu-id="a95fe-186">Để đảm bảo ngắn gọn, chúng tôi sẽ sử dụng ứng dụng tổ chức trình gỡ lỗi để kiểm tra cuộc gọi hành động.</span><span class="sxs-lookup"><span data-stu-id="a95fe-186">For the sake of brevity, we will use the Debugger hosted application to test the action call.</span></span>  
  
1. <span data-ttu-id="a95fe-187">Start [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to your Dynamics 365 for Customer Engagement server.</span><span class="sxs-lookup"><span data-stu-id="a95fe-187">Start [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to your Dynamics 365 for Customer Engagement server.</span></span>  
  
2. <span data-ttu-id="a95fe-188">Trong ứng dụng khách, bắt đầu trình gỡ lỗi bằng cách nhấp vào mũi tên xuống bên cạnh trình đơn cài đặt ở góc trên cùng bên phải, bấm vào **gỡ lỗi**.</span><span class="sxs-lookup"><span data-stu-id="a95fe-188">In the client application, start Debugger by clicking down arrow next to the settings menu in the top-right corner, and clicking **Debug**.</span></span>  
  
3. <span data-ttu-id="a95fe-189">Trong trình gỡ lỗi, hãy nhấp vào mũi tên xuống trên tab **cuộc gọi hành động** để hiển thị các khu vực nơi bạn có thể kiểm tra cuộc gọi hành động và thao tác UII.</span><span class="sxs-lookup"><span data-stu-id="a95fe-189">In Debugger, click the down arrow above the **Action Calls** tab to display the area where you can test action calls and UII actions.</span></span>  
  
   <span data-ttu-id="a95fe-190">![Test action calls & UII actions in debugger](../unified-service-desk/media/usd-customize-display-2.png "Test action calls & UII actions in debugger")</span><span class="sxs-lookup"><span data-stu-id="a95fe-190">![Test action calls & UII actions in debugger](../unified-service-desk/media/usd-customize-display-2.png "Test action calls & UII actions in debugger")</span></span>  
  
4. <span data-ttu-id="a95fe-191">From the **Action Calls** drop-down list, select **Action Call for Custom Theme**, and click the **Run Action Call** icon (![USD debugger Run Action Call button](../unified-service-desk/media/usd-run-action-call-icon.png "USD debugger Run Action Call button")).</span><span class="sxs-lookup"><span data-stu-id="a95fe-191">From the **Action Calls** drop-down list, select **Action Call for Custom Theme**, and click the **Run Action Call** icon (![USD debugger Run Action Call button](../unified-service-desk/media/usd-run-action-call-icon.png "USD debugger Run Action Call button")).</span></span> <span data-ttu-id="a95fe-192">Thay đổi văn bản trong thanh tiêu đề và màu nền của ứng dụng tác nhân.</span><span class="sxs-lookup"><span data-stu-id="a95fe-192">The text in the title bar and skin color of the agent application change.</span></span>  
  
   <span data-ttu-id="a95fe-193">![Customized display of the client application](../unified-service-desk/media/crm-itpro-usd-customizedisplay03.PNG "Customized display of the client application")</span><span class="sxs-lookup"><span data-stu-id="a95fe-193">![Customized display of the client application](../unified-service-desk/media/crm-itpro-usd-customizedisplay03.PNG "Customized display of the client application")</span></span>  
  
   <span data-ttu-id="a95fe-194">Để hoàn tác những thay đổi, chọn một trong các chủ đề được xác định trước trong các ứng dụng khách.</span><span class="sxs-lookup"><span data-stu-id="a95fe-194">To undo the changes, select one of the predefined themes in the client application.</span></span>  
  
<a name="HighContrast"></a>   
## <a name="high-contrast-mode-support--for-custom-themes"></a><span data-ttu-id="a95fe-195">High-contrast mode support  for custom themes</span><span class="sxs-lookup"><span data-stu-id="a95fe-195">High-contrast mode support  for custom themes</span></span>  
 [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="a95fe-196">internally uses normal and high-contrast mode XAML brush resources to display its UI elements depending on the high-contrast mode setting on your computer.</span><span class="sxs-lookup"><span data-stu-id="a95fe-196">internally uses normal and high-contrast mode XAML brush resources to display its UI elements depending on the high-contrast mode setting on your computer.</span></span> <span data-ttu-id="a95fe-197">You can find the XAML brush resources in the [!INCLUDE[pn_user_interface_integration](../includes/pn-user-interface-integration.md)] SDK download package.</span><span class="sxs-lookup"><span data-stu-id="a95fe-197">You can find the XAML brush resources in the [!INCLUDE[pn_user_interface_integration](../includes/pn-user-interface-integration.md)] SDK download package.</span></span> <span data-ttu-id="a95fe-198">[Download](http://go.microsoft.com/fwlink/p/?LinkId=395257) the package, and extract it to view the file and its contents under the "UII\USD Developer Assets\USD Layout and Style Sheet" directory.</span><span class="sxs-lookup"><span data-stu-id="a95fe-198">[Download](http://go.microsoft.com/fwlink/p/?LinkId=395257) the package, and extract it to view the file and its contents under the "UII\USD Developer Assets\USD Layout and Style Sheet" directory.</span></span>  
  
 <span data-ttu-id="a95fe-199">To support high-contrast mode in your custom themes, consider the following:</span><span class="sxs-lookup"><span data-stu-id="a95fe-199">To support high-contrast mode in your custom themes, consider the following:</span></span>  
  
-   <span data-ttu-id="a95fe-200">Create two action calls for setting a custom theme: one for the *normal* mode and the other for the *high-contrast* mode.</span><span class="sxs-lookup"><span data-stu-id="a95fe-200">Create two action calls for setting a custom theme: one for the *normal* mode and the other for the *high-contrast* mode.</span></span> <span data-ttu-id="a95fe-201">For example, while defining the color property of a XAML brush, use:</span><span class="sxs-lookup"><span data-stu-id="a95fe-201">For example, while defining the color property of a XAML brush, use:</span></span>  
  
    -   <span data-ttu-id="a95fe-202">One of the predefined colors as defined in the [Colors](https://msdn.microsoft.com/en-us/library/system.windows.media.colors\(v=vs.110\).aspx) class for the *normal* mode:</span><span class="sxs-lookup"><span data-stu-id="a95fe-202">One of the predefined colors as defined in the [Colors](https://msdn.microsoft.com/en-us/library/system.windows.media.colors\(v=vs.110\).aspx) class for the *normal* mode:</span></span>  
  
        ```  
        <SolidColorBrush x:Key="WindowBackgroundStyle" Color="Yellow"/>  
        ```  
  
    -   <span data-ttu-id="a95fe-203">One of the system colors as defined in the [SystemColors](https://msdn.microsoft.com/en-us/library/system.windows.systemcolors.windowcolor\(v=vs.110\).aspx) class for the *high-contrast* mode:</span><span class="sxs-lookup"><span data-stu-id="a95fe-203">One of the system colors as defined in the [SystemColors](https://msdn.microsoft.com/en-us/library/system.windows.systemcolors.windowcolor\(v=vs.110\).aspx) class for the *high-contrast* mode:</span></span>  
  
        ```  
        <SolidColorBrush x:Key="WindowBackgroundStyle" Color="{x:Static SystemColors.WindowColor}"/>  
        ```  
  
-   <span data-ttu-id="a95fe-204">Use the new  `$SystemParameters.HighContrast` replacement parameter in each of your action call definition as a condition to ensure that a action call is fired appropriately.</span><span class="sxs-lookup"><span data-stu-id="a95fe-204">Use the new  `$SystemParameters.HighContrast` replacement parameter in each of your action call definition as a condition to ensure that a action call is fired appropriately.</span></span> <span data-ttu-id="a95fe-205">For example, in the action call definition for setting custom theme for:</span><span class="sxs-lookup"><span data-stu-id="a95fe-205">For example, in the action call definition for setting custom theme for:</span></span>  
  
    -   <span data-ttu-id="a95fe-206">The *normal* mode, use the following in the **Condition** field to check that the high-contrast mode is not set on your computer:</span><span class="sxs-lookup"><span data-stu-id="a95fe-206">The *normal* mode, use the following in the **Condition** field to check that the high-contrast mode is not set on your computer:</span></span>  
  
        ```  
        "[[$SystemParameters.HighContrast]g]"=="False"  
        ```  
  
    -   <span data-ttu-id="a95fe-207">The *high-contrast* mode, use the following in the **Condition** field to check that the high-contrast mode is set on your computer:</span><span class="sxs-lookup"><span data-stu-id="a95fe-207">The *high-contrast* mode, use the following in the **Condition** field to check that the high-contrast mode is set on your computer:</span></span>  
  
        ```  
        "[[$SystemParameters.HighContrast]g]"=="True"  
        ```  
  
### <a name="see-also"></a><span data-ttu-id="a95fe-208">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a95fe-208">See also</span></span>  
 <span data-ttu-id="a95fe-209">[Customize themes for High Contrast settings](../unified-service-desk/customize-themes-in-unified-service-desk.md ) </span><span class="sxs-lookup"><span data-stu-id="a95fe-209">[Customize themes for High Contrast settings](../unified-service-desk/customize-themes-in-unified-service-desk.md ) </span></span>  
 <span data-ttu-id="a95fe-210">[Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="a95fe-210">[Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md) </span></span>  
 <span data-ttu-id="a95fe-211">[Sử dụng chủ đề để tùy chỉnh giao diện ứng dụng của bạn](../unified-service-desk/customize-appearance-application.md) </span><span class="sxs-lookup"><span data-stu-id="a95fe-211">[Use themes to customize the appearance of your application](../unified-service-desk/customize-appearance-application.md) </span></span>  
 [<span data-ttu-id="a95fe-212">Hosted control types and action/event reference</span><span class="sxs-lookup"><span data-stu-id="a95fe-212">Hosted control types and action/event reference</span></span>](../unified-service-desk/hosted-control-types-action-event-reference.md)   
