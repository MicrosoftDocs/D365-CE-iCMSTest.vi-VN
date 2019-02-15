---
title: Configure client caching in Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn how to set client caching.
ms.custom:
- dyn365-USD, dyn365-admin
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
ms.assetid: 4aab0a03-2d52-4ced-b6cf-9694d1edbdb7
author: kabala123
ms.author: kabala
manager: shujoshi
tags:
- MigrationHO
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 50cc1efe27b884bd91c1bd2934e8c465c4da5cd2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382526"
---
# <a name="client-caching-overview"></a><span data-ttu-id="28451-103">Client caching overview</span><span class="sxs-lookup"><span data-stu-id="28451-103">Client caching overview</span></span>
<span data-ttu-id="28451-104">Client caching enables you to reduce the amount of bandwidth required at the startup of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client on the call center agent’s computers, and over the life cycle of the client application.</span><span class="sxs-lookup"><span data-stu-id="28451-104">Client caching enables you to reduce the amount of bandwidth required at the startup of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client on the call center agent’s computers, and over the life cycle of the client application.</span></span> <span data-ttu-id="28451-105">Bộ nhớ đệm ứng dụng cung cấp một phương tiện để lưu vào bộ nhớ đệm phần lớn [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] dữ liệu cấu hình cục bộ tại máy tính của tổng đài viên trung tâm cuộc gọi, do đó làm giảm nhu cầu dữ liệu phổ biến được truy xuất từ máy chủ.</span><span class="sxs-lookup"><span data-stu-id="28451-105">Client caching provides a means to cache the majority of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration data locally on the call center agent’s computer, thereby reducing the need for common data to be retrieved from the server.</span></span> <span data-ttu-id="28451-106">Khả năng này làm tăng hiệu suất khởi động đáng kể của [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="28451-106">This capability provides a noticeable increase in the startup performance of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="28451-107">This feature has privacy impact because enabling client caching in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] leads to some of your data being stored locally on the user’s computer, which is outside the [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps services boundary.</span><span class="sxs-lookup"><span data-stu-id="28451-107">This feature has privacy impact because enabling client caching in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] leads to some of your data being stored locally on the user’s computer, which is outside the [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps services boundary.</span></span>  
  
<a name="WhenToUse"></a>   
## <a name="when-should-you-use-client-caching"></a><span data-ttu-id="28451-108">Khi nào bạn nên sử dụng bộ đệm ứng dụng?</span><span class="sxs-lookup"><span data-stu-id="28451-108">When should you use client caching?</span></span>  
 <span data-ttu-id="28451-109">Bộ nhớ đệm ứng dụng có thể cung cấp một cải tiến đáng kể trong thời gian khởi động, giảm tổng thể băng thông và giảm đáng kể các truy vấn để đối với [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] máy chủ cho dữ liệu phổ biến [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="28451-109">Client caching can provide a significant improvement in startup times, a reduction in overall bandwidth, and a significant reduction in queries to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] server for common [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] data.</span></span>  
  
 <span data-ttu-id="28451-110">Bộ nhớ đệm ứng dụng được sử dụng tốt nhất trong môi trường thử nghiệm hiệu suất, đào tạo và sản xuất.</span><span class="sxs-lookup"><span data-stu-id="28451-110">Client caching is best employed in performance testing, training, and production environments.</span></span> <span data-ttu-id="28451-111">Nó không được khuyến khích cho môi trường phát triển bởi vì các thay đổi được chỉ sao chép khi khóa bộ nhớ đệm kiểm soát được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="28451-111">It isn’t recommended for development environments because changes are only replicated when the control cache key is updated.</span></span>  
  
<a name="HowItWorks"></a>   
## <a name="how-client-caching-works"></a><span data-ttu-id="28451-112">Cách thức hoạt động của bộ nhớ đệm ứng dụng</span><span class="sxs-lookup"><span data-stu-id="28451-112">How client caching works</span></span>  
 <span data-ttu-id="28451-113">Khi bạn bật bộ nhớ đệm ứng dụng, quá trình sau được thực hiện khi bạn đăng nhập bằng cách sử dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] ứng dụng khách:</span><span class="sxs-lookup"><span data-stu-id="28451-113">When you enable client caching, the following process is executed when you log on using the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application:</span></span>  
  
1.  <span data-ttu-id="28451-114">The **Options** and **User Settings** entities are queried for the startup keys to determine if client caching is enabled.</span><span class="sxs-lookup"><span data-stu-id="28451-114">The **Options** and **User Settings** entities are queried for the startup keys to determine if client caching is enabled.</span></span>  
  
2.  <span data-ttu-id="28451-115">Nếu đã được bật, giải quyết số phiên bản bộ nhớ đệm của ứng dụng và bất kỳ sửa đổi bộ nhớ đệm nào.</span><span class="sxs-lookup"><span data-stu-id="28451-115">If it is enabled, resolve client cache version number and any cache modifications.</span></span>  
  
3.  <span data-ttu-id="28451-116">Nếu bộ nhớ đệm ứng dụng được bật và đã có số phiên bản, xác định vị trí lưu trữ bộ nhớ đệm cục bộ và xác định khóa phiên bản bộ nhớ đệm.</span><span class="sxs-lookup"><span data-stu-id="28451-116">If client caching is enabled and a version number is available, locate the local cache store and determine the cache version key.</span></span>  
  
    1.  <span data-ttu-id="28451-117">Nếu số phiên bản bộ nhớ đệm là số hiện tại, mã hóa và tải lưu trữ bộ nhớ đệm vào bộ nhớ.</span><span class="sxs-lookup"><span data-stu-id="28451-117">If cache version number is current, decrypt and load the cache store into memory.</span></span>  
  
    2.  <span data-ttu-id="28451-118">Nếu số phiên bản của bộ nhớ đệm không chính xác, xóa đối tượng bộ nhớ đệm.</span><span class="sxs-lookup"><span data-stu-id="28451-118">If the cache version number is incorrect, delete the cache object.</span></span>  
  
<a name="EnableCaching"></a>   
## <a name="enable-client-caching"></a><span data-ttu-id="28451-119">Bật bộ nhớ đệm ứng dụng</span><span class="sxs-lookup"><span data-stu-id="28451-119">Enable client caching</span></span>  
  
1. <span data-ttu-id="28451-120">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="28451-120">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="28451-121">Bấm vào **Tùy chọn**.</span><span class="sxs-lookup"><span data-stu-id="28451-121">Click **Options**.</span></span>  
  
4. <span data-ttu-id="28451-122">Bấm vào **Mới** trên thanh lệnh để tạo tùy chọn mới.</span><span class="sxs-lookup"><span data-stu-id="28451-122">Click **New** on the command bar to create a new option.</span></span>  
  
5. <span data-ttu-id="28451-123">Đối với các tùy chọn mới, nhập **ClientCacheVersionNumber** trong hộp **tên** và số gồm số và chữ cái trong hộp **giá trị**.</span><span class="sxs-lookup"><span data-stu-id="28451-123">For the new option, type **ClientCacheVersionNumber** in the **Name** box, and an alphanumeric number in the **Value** box.</span></span> <span data-ttu-id="28451-124">Giá trị số và chữ cái được sử dụng như là khóa bộ nhớ đệm cho [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="28451-124">The alphanumeric value is used as the cache key for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span>  
  
6. <span data-ttu-id="28451-125">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="28451-125">Click **Save**.</span></span>  
  
   <span data-ttu-id="28451-126">Khi các tùy chọn đã có và được xác định, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sẽ kích hoạt bộ nhớ đệm ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="28451-126">When the option is present and populated, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] will activate the client caching.</span></span>  
  
<a name="CachingStoreLocation"></a>   
## <a name="client-caching-store-location"></a><span data-ttu-id="28451-127">Vị trí lưu trữ bộ nhớ đệm ứng dụng</span><span class="sxs-lookup"><span data-stu-id="28451-127">Client caching store location</span></span>  
 <span data-ttu-id="28451-128">Khi được bật, bộ nhớ đệm ứng dụng lưu trữ các tệp của mình dưới định dạng mã hóa và nén trong thư mục chuyển vùng của người dùng: %appData%\Microsoft\USD</span><span class="sxs-lookup"><span data-stu-id="28451-128">When enabled, client caching stores its files in a compressed and encrypted format in the users roaming directory: %appData%\Microsoft\USD</span></span>  
  
 <span data-ttu-id="28451-129">For example, for a user called agent1 running the client application on [!INCLUDE[pn_windows8](../../includes/pn-windows8.md)], the client caching files will be available at c:\Users\agent1\AppData\Roaming\Microsoft\USD.</span><span class="sxs-lookup"><span data-stu-id="28451-129">For example, for a user called agent1 running the client application on [!INCLUDE[pn_windows8](../../includes/pn-windows8.md)], the client caching files will be available at c:\Users\agent1\AppData\Roaming\Microsoft\USD.</span></span>  
  
 <span data-ttu-id="28451-130">Thông tin trong thư mục này chỉ có thể được truy cập bằng tài khoản người dùng tạo ra nó.</span><span class="sxs-lookup"><span data-stu-id="28451-130">Information in this directory can only be accessed by the user account that created it.</span></span>  
  
<a name="PushUpdatetoAllClients"></a>   
## <a name="push-an-update-to-clients"></a><span data-ttu-id="28451-131">Tạo bản cập nhập cho khách hàng</span><span class="sxs-lookup"><span data-stu-id="28451-131">Push an update to clients</span></span>  
 <span data-ttu-id="28451-132">Để tạo bản cập nhật cho tất cả khách hàng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], bạn phải chỉnh sửa giá trị của **ClientCacheVersionNumber** mà bạn tạo ra trước đó với giá trị số khác nhau.</span><span class="sxs-lookup"><span data-stu-id="28451-132">To push an update to all the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] clients, you must edit the value of the **ClientCacheVersionNumber** that you created earlier to a different alphanumeric value.</span></span> <span data-ttu-id="28451-133">Lần tiếp theo khi nhật ký tổng đài viên trung tâm cuộc gọi đang sử dụng ứng dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], nhật ký sẽ phát hiện giá trị khác nhau cho các phím tùy chọn **ClientCacheVersionNumber** và đọc tất cả cài đặt từ máy chủ trước khi khởi động.</span><span class="sxs-lookup"><span data-stu-id="28451-133">Next time when a call center agent logs in using the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client, it will detect the different value for the **ClientCacheVersionNumber** option key, and read all settings from the server before starting up.</span></span>  
  
<a name="DisableClientCachingforUser"></a>   
## <a name="disable-client-caching-for-a-specific-user"></a><span data-ttu-id="28451-134">Tắt bộ nhớ đệm ứng dụng cho một người dùng cụ thể</span><span class="sxs-lookup"><span data-stu-id="28451-134">Disable client caching for a specific user</span></span>  
 <span data-ttu-id="28451-135">Đôi khi nó việc loại trừ một số người dùng từ bộ nhớ đệm ứng dụng có thể cần thiết chẳng hạn như thử nghiệm giới hạn các cấu hình mới trong sản xuất, sản xuất, hoặc khắc phục sự cố khi nghi ngờ có sự cố bộ nhớ đệm hoặc sự cần thiết để thực hiện cập nhật nhanh cấu hình mà bạn muốn hoàn nguyên thay đổi của mình về đối tượng hiện được lưu trong bộ nhớ đệm.</span><span class="sxs-lookup"><span data-stu-id="28451-135">At times it may be necessary to exclude some users from client caching such as limited testing of new configurations in production, production, or troubleshooting where a cache problem is suspected, or the need to do rapid updates to a configuration where you want to revert your changes back to the currently cached objects.</span></span>  
  
1. <span data-ttu-id="28451-136">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="28451-136">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="28451-137">Click **User Settings**.</span><span class="sxs-lookup"><span data-stu-id="28451-137">Click **User Settings**.</span></span>  
  
4. <span data-ttu-id="28451-138">Bấm vào **Mới** trên thanh lệnh để tạo cài đặt mới.</span><span class="sxs-lookup"><span data-stu-id="28451-138">Click **New** on the command bar to create a new setting.</span></span>  
  
5. <span data-ttu-id="28451-139">Trên trang **Cài đặt người dùng mới**:</span><span class="sxs-lookup"><span data-stu-id="28451-139">On the **New User Setting** page:</span></span>  
  
   1.  <span data-ttu-id="28451-140">Trong trường **người dùng**, nhập hoặc chọn tên người dùng mà bạn muốn tắt bộ nhớ đệm ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="28451-140">In the **User** field, type or select the name of the user for which you want to disable client caching.</span></span>  
  
   2.  <span data-ttu-id="28451-141">Trong trường **tên**, nhập **DisableCaching**.</span><span class="sxs-lookup"><span data-stu-id="28451-141">In the **Name** field, type **DisableCaching**.</span></span> <span data-ttu-id="28451-142">Để trống trường **giá trị**.</span><span class="sxs-lookup"><span data-stu-id="28451-142">Leave the **Value** field empty.</span></span>  
  
   <span data-ttu-id="28451-143">![Disable client caching for a user](../../unified-service-desk/media/usd-disable-client-caching-user.PNG "Disable client caching for a user")</span><span class="sxs-lookup"><span data-stu-id="28451-143">![Disable client caching for a user](../../unified-service-desk/media/usd-disable-client-caching-user.PNG "Disable client caching for a user")</span></span>  
  
6. <span data-ttu-id="28451-144">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="28451-144">Click **Save**.</span></span>  
  
   <span data-ttu-id="28451-145">Khi người dùng tiếp theo đăng nhập bằng cách sử dụng ứng dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], bộ nhớ đệm ứng dụng không được sử dụng.</span><span class="sxs-lookup"><span data-stu-id="28451-145">When the user next signs in using the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client, client caching isn’t used.</span></span> <span data-ttu-id="28451-146">Tuy nhiên, nó không xóa hoặc làm mới lưu trữ bộ nhớ đệm ứng dụng cho người dùng.</span><span class="sxs-lookup"><span data-stu-id="28451-146">However, it doesn’t delete or refresh the client cache store for the user.</span></span> <span data-ttu-id="28451-147">Khi khóa **DisableCaching** được xóa cho người dùng, người dùng sẽ quay lại sử dụng lưu trữ bộ nhớ đệm ứng dụng đã lưu trước đó.</span><span class="sxs-lookup"><span data-stu-id="28451-147">When the **DisableCaching** key is removed for the user, the user will return to using the previously stored client cache store.</span></span>  
  
<a name="ForceCacheReset"></a>   
## <a name="force-a-cache-reset-for-a-specific-user"></a><span data-ttu-id="28451-148">Bắt buộc đặt lại bộ nhớ đệm cho người dùng cụ thể</span><span class="sxs-lookup"><span data-stu-id="28451-148">Force a cache reset for a specific user</span></span>  
 <span data-ttu-id="28451-149">Đôi khi, điều này có thể là cần thiết khi bắt buộc đặt lại bộ nhớ đệm cho người dùng cụ thể để xóa và đặt lại lưu trữ bộ nhớ đệm.</span><span class="sxs-lookup"><span data-stu-id="28451-149">At times, it may be necessary to force a cache reset for a specific user to clear and reset the cache store.</span></span> <span data-ttu-id="28451-150">Bạn có thể làm điều này bằng hai cách: từ máy chủ [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] hoặc bằng cách sử dụng các ứng dụng khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] trên máy tính của người dùng.</span><span class="sxs-lookup"><span data-stu-id="28451-150">You can do this in two ways: From the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] server or by using the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application on the user’s computer.</span></span>  
  
<a name="UsingCRMServer"></a>   
### <a name="using-the-dynamics-365-for-customer-engagement-server"></a><span data-ttu-id="28451-151">Using the Dynamics 365 for Customer Engagement server</span><span class="sxs-lookup"><span data-stu-id="28451-151">Using the Dynamics 365 for Customer Engagement server</span></span>  
  
1. <span data-ttu-id="28451-152">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="28451-152">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="28451-153">Click **User Settings**.</span><span class="sxs-lookup"><span data-stu-id="28451-153">Click **User Settings**.</span></span>  
  
4. <span data-ttu-id="28451-154">Click **New** on the command bar to create a new setting.</span><span class="sxs-lookup"><span data-stu-id="28451-154">Click **New** on the command bar to create a new setting.</span></span>  
  
5. <span data-ttu-id="28451-155">Trên trang **Cài đặt người dùng mới**:</span><span class="sxs-lookup"><span data-stu-id="28451-155">On the **New User Setting** page:</span></span>  
  
   1.  <span data-ttu-id="28451-156">Trong trường **người dùng**, nhập hoặc chọn tên người dùng mà bạn muốn tắt bộ nhớ đệm ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="28451-156">In the **User** field, type or select the name of the user that you want to disable client caching for.</span></span>  
  
   2.  <span data-ttu-id="28451-157">Trong trường **Tên**, nhập **ResetDesktopCache**.</span><span class="sxs-lookup"><span data-stu-id="28451-157">In the **Name** field, type **ResetDesktopCache**.</span></span> <span data-ttu-id="28451-158">Leave the **Value** field empty.</span><span class="sxs-lookup"><span data-stu-id="28451-158">Leave the **Value** field empty.</span></span>  
  
6. <span data-ttu-id="28451-159">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="28451-159">Click **Save**.</span></span>  
  
   <span data-ttu-id="28451-160">The ResetDesktopCache setting causes the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application to delete its local cache store and rebuild it from the server.</span><span class="sxs-lookup"><span data-stu-id="28451-160">The ResetDesktopCache setting causes the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application to delete its local cache store and rebuild it from the server.</span></span>  
  
   <span data-ttu-id="28451-161">To complete the cache reset process, two restarts of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client are required.</span><span class="sxs-lookup"><span data-stu-id="28451-161">To complete the cache reset process, two restarts of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client are required.</span></span>  
  
7. <span data-ttu-id="28451-162">After the first [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application restart, the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client loads data from the existing cache.</span><span class="sxs-lookup"><span data-stu-id="28451-162">After the first [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application restart, the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client loads data from the existing cache.</span></span> <span data-ttu-id="28451-163">Afterwards, the existing cache is deleted and the ResetDesktopCache setting is disabled.</span><span class="sxs-lookup"><span data-stu-id="28451-163">Afterwards, the existing cache is deleted and the ResetDesktopCache setting is disabled.</span></span>  
  
8. <span data-ttu-id="28451-164">After the second [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application restart, the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client loads the configuration directly from the server and re-creates the cache.</span><span class="sxs-lookup"><span data-stu-id="28451-164">After the second [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application restart, the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client loads the configuration directly from the server and re-creates the cache.</span></span>  <span data-ttu-id="28451-165">Notice that the time it takes for the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client to load during this time can increase significantly.</span><span class="sxs-lookup"><span data-stu-id="28451-165">Notice that the time it takes for the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client to load during this time can increase significantly.</span></span>  
  
### <a name="using-the-unified-service-desk-client"></a><span data-ttu-id="28451-166">Sử dụng ứng dụng Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="28451-166">Using the Unified Service Desk client</span></span>  
 <span data-ttu-id="28451-167">Bạn có thể hủy việc đặt lại từ ứng dụng khách bằng cách sử dụng thao tác UII ẩn được gọi là **ResetLocalCache** trên loại kiểm soát tổ chức **trình quản lý chung**.</span><span class="sxs-lookup"><span data-stu-id="28451-167">You can invoke a reset from the client application using a hidden UII action called **ResetLocalCache** on the **Global Manager** hosted control type.</span></span> <span data-ttu-id="28451-168">Bạn sẽ cần phải tạo thao tác UII trên loại kiểm soát tổ chức trình quản lý chung trước khi có thể sử dụng.</span><span class="sxs-lookup"><span data-stu-id="28451-168">You’ll need to create the UII action on the Global Manager hosted control type before you can use it.</span></span>  
  
1. <span data-ttu-id="28451-169">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="28451-169">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="28451-170">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="28451-170">Click **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="28451-171">Locate the **Dynamics 365 for Customer Engagement apps Global Manager** hosted control, and click its name in the **Name** column to open it for editing.</span><span class="sxs-lookup"><span data-stu-id="28451-171">Locate the **Dynamics 365 for Customer Engagement apps Global Manager** hosted control, and click its name in the **Name** column to open it for editing.</span></span>  
  
   > [!NOTE]
   > <span data-ttu-id="28451-172">**Dynamics 365 for Customer Engagement apps Global Manager** is the name of the hosted control in the sample [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] applications.</span><span class="sxs-lookup"><span data-stu-id="28451-172">**Dynamics 365 for Customer Engagement apps Global Manager** is the name of the hosted control in the sample [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] applications.</span></span> <span data-ttu-id="28451-173">Nếu bạn đã đặt tên khác cho kiểm soát tổ chức trình quản lý chung của mình, hãy chọn tên đó để thay thế.</span><span class="sxs-lookup"><span data-stu-id="28451-173">If you have named your Global Manager hosted control something else, select it instead.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="28451-174">[Global Manager (Hosted Control)](../../unified-service-desk/global-manager-hosted-control.md)</span><span class="sxs-lookup"><span data-stu-id="28451-174">[Global Manager (Hosted Control)](../../unified-service-desk/global-manager-hosted-control.md)</span></span>  
  
5. <span data-ttu-id="28451-175">On the nav bar, click the down arrow next to the **Dynamics 365 for Customer Engagement apps Global Manager** hosted control, and then select **UII Actions**.</span><span class="sxs-lookup"><span data-stu-id="28451-175">On the nav bar, click the down arrow next to the **Dynamics 365 for Customer Engagement apps Global Manager** hosted control, and then select **UII Actions**.</span></span>  
  
   <span data-ttu-id="28451-176">![Navigation to UII Actions for hosted control](../../unified-service-desk/media/usd-hosted-contro-uii-action.png "Navigation to UII Actions for hosted control")</span><span class="sxs-lookup"><span data-stu-id="28451-176">![Navigation to UII Actions for hosted control](../../unified-service-desk/media/usd-hosted-contro-uii-action.png "Navigation to UII Actions for hosted control")</span></span>  
  
6. <span data-ttu-id="28451-177">Trên trang tiếp theo, bấm vào **thêm hành động UII mới**.</span><span class="sxs-lookup"><span data-stu-id="28451-177">On the next page, click **Add New UII Action**.</span></span>  
  
7. <span data-ttu-id="28451-178">Trên trang **Hành động UII mới**, nhập **ResetLocalCache** trong trường **tên** sau đó nhấp vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="28451-178">On the **New UII Action** page, type **ResetLocalCache** in the **Name** field, and then click **Save**.</span></span> <span data-ttu-id="28451-179">Đóng các hành động UII và kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="28451-179">Close the UII Action and the hosted control.</span></span>  
  
    <span data-ttu-id="28451-180">Tiếp theo, chúng tôi sẽ thêm một cuộc gọi hành động để gọi hành động UII mà chúng tôi vừa tạo.</span><span class="sxs-lookup"><span data-stu-id="28451-180">Next, we will add an action call to call the UII action that we just created.</span></span>  
  
8. <span data-ttu-id="28451-181">On the nav bar, click **Settings** > **Unified Service Desk** > **Action Calls**.</span><span class="sxs-lookup"><span data-stu-id="28451-181">On the nav bar, click **Settings** > **Unified Service Desk** > **Action Calls**.</span></span>  
  
9. <span data-ttu-id="28451-182">Trên trang cuộc gọi hành động tiếp theo, bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="28451-182">On the action calls page, Click **New**.</span></span>  
  
10. <span data-ttu-id="28451-183">Trên trang **Cuộc gọi hành động mới**:</span><span class="sxs-lookup"><span data-stu-id="28451-183">On the **New Action Call** page:</span></span>  
  
    1. <span data-ttu-id="28451-184">Trong trường **Tên**, nhập **ResetClientCache**.</span><span class="sxs-lookup"><span data-stu-id="28451-184">In the **Name** field, type **ResetClientCache**.</span></span>  
  
    2. <span data-ttu-id="28451-185">In the **Hosted Control** field, specify the **Dynamics 365 for Customer Engagement apps Global Manager**.</span><span class="sxs-lookup"><span data-stu-id="28451-185">In the **Hosted Control** field, specify the **Dynamics 365 for Customer Engagement apps Global Manager**.</span></span>  
  
       > [!NOTE]
       > <span data-ttu-id="28451-186">**Dynamics 365 for Customer Engagement apps Global Manager** is the name of the hosted control in the sample [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] applications.</span><span class="sxs-lookup"><span data-stu-id="28451-186">**Dynamics 365 for Customer Engagement apps Global Manager** is the name of the hosted control in the sample [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] applications.</span></span> <span data-ttu-id="28451-187">If you have named your Global Manager hosted control something else, select it instead.</span><span class="sxs-lookup"><span data-stu-id="28451-187">If you have named your Global Manager hosted control something else, select it instead.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="28451-188">[Global Manager (Hosted Control)](../../unified-service-desk/global-manager-hosted-control.md)</span><span class="sxs-lookup"><span data-stu-id="28451-188">[Global Manager (Hosted Control)](../../unified-service-desk/global-manager-hosted-control.md)</span></span>  
  
    3. <span data-ttu-id="28451-189">Trong trường **Hành động**, chỉ định **ResetLocalCache**.</span><span class="sxs-lookup"><span data-stu-id="28451-189">In the **Action** field, specify **ResetLocalCache**.</span></span>  
  
11. <span data-ttu-id="28451-190">Bấm vào **Lưu** và sau đó đóng cuộc gọi hành động.</span><span class="sxs-lookup"><span data-stu-id="28451-190">Click **Save** and then close the action call.</span></span>  
  
    <span data-ttu-id="28451-191">After you have set up the UII action and the action call, you can add a toolbar button, event, or code to directly invoke the action call from the client application.</span><span class="sxs-lookup"><span data-stu-id="28451-191">After you have set up the UII action and the action call, you can add a toolbar button, event, or code to directly invoke the action call from the client application.</span></span> <span data-ttu-id="28451-192">This creates a **RestDesktopCache** setting in the **User Settings** area, which triggers the reset behavior as described earlier in [Using the Dynamics 365 for Customer Engagement server](../../unified-service-desk/admin/configure-client-caching-unified-service-desk.md#UsingCRMServer).</span><span class="sxs-lookup"><span data-stu-id="28451-192">This creates a **RestDesktopCache** setting in the **User Settings** area, which triggers the reset behavior as described earlier in [Using the Dynamics 365 for Customer Engagement server](../../unified-service-desk/admin/configure-client-caching-unified-service-desk.md#UsingCRMServer).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28451-193">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="28451-193">See also</span></span>  
 <span data-ttu-id="28451-194">[Ứng dụng Unified Service Desk mẫu](../../unified-service-desk/admin/sample-unified-service-desk-applications.md) </span><span class="sxs-lookup"><span data-stu-id="28451-194">[Sample Unified Service Desk applications](../../unified-service-desk/admin/sample-unified-service-desk-applications.md) </span></span>  
 <span data-ttu-id="28451-195">[Administer and manage Unified Service Desk](../../unified-service-desk/admin/administer-manage-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="28451-195">[Administer and manage Unified Service Desk](../../unified-service-desk/admin/administer-manage-unified-service-desk.md) </span></span>  
 [<span data-ttu-id="28451-196">Thêm một hành động UII vào một điều khiển tổ chức</span><span class="sxs-lookup"><span data-stu-id="28451-196">Add a UII action to a hosted control</span></span>](../../unified-service-desk/add-uii-action-hosted-control.md)   
 
