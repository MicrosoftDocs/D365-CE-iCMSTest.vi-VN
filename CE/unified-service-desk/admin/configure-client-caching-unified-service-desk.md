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
# <a name="client-caching-overview"></a>Client caching overview
Client caching enables you to reduce the amount of bandwidth required at the startup of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client on the call center agent’s computers, and over the life cycle of the client application. Bộ nhớ đệm ứng dụng cung cấp một phương tiện để lưu vào bộ nhớ đệm phần lớn [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] dữ liệu cấu hình cục bộ tại máy tính của tổng đài viên trung tâm cuộc gọi, do đó làm giảm nhu cầu dữ liệu phổ biến được truy xuất từ máy chủ. Khả năng này làm tăng hiệu suất khởi động đáng kể của [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].  
  
> [!IMPORTANT]
>  This feature has privacy impact because enabling client caching in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] leads to some of your data being stored locally on the user’s computer, which is outside the [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps services boundary.  
  
<a name="WhenToUse"></a>   
## <a name="when-should-you-use-client-caching"></a>Khi nào bạn nên sử dụng bộ đệm ứng dụng?  
 Bộ nhớ đệm ứng dụng có thể cung cấp một cải tiến đáng kể trong thời gian khởi động, giảm tổng thể băng thông và giảm đáng kể các truy vấn để đối với [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] máy chủ cho dữ liệu phổ biến [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].  
  
 Bộ nhớ đệm ứng dụng được sử dụng tốt nhất trong môi trường thử nghiệm hiệu suất, đào tạo và sản xuất. Nó không được khuyến khích cho môi trường phát triển bởi vì các thay đổi được chỉ sao chép khi khóa bộ nhớ đệm kiểm soát được cập nhật.  
  
<a name="HowItWorks"></a>   
## <a name="how-client-caching-works"></a>Cách thức hoạt động của bộ nhớ đệm ứng dụng  
 Khi bạn bật bộ nhớ đệm ứng dụng, quá trình sau được thực hiện khi bạn đăng nhập bằng cách sử dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] ứng dụng khách:  
  
1.  The **Options** and **User Settings** entities are queried for the startup keys to determine if client caching is enabled.  
  
2.  Nếu đã được bật, giải quyết số phiên bản bộ nhớ đệm của ứng dụng và bất kỳ sửa đổi bộ nhớ đệm nào.  
  
3.  Nếu bộ nhớ đệm ứng dụng được bật và đã có số phiên bản, xác định vị trí lưu trữ bộ nhớ đệm cục bộ và xác định khóa phiên bản bộ nhớ đệm.  
  
    1.  Nếu số phiên bản bộ nhớ đệm là số hiện tại, mã hóa và tải lưu trữ bộ nhớ đệm vào bộ nhớ.  
  
    2.  Nếu số phiên bản của bộ nhớ đệm không chính xác, xóa đối tượng bộ nhớ đệm.  
  
<a name="EnableCaching"></a>   
## <a name="enable-client-caching"></a>Bật bộ nhớ đệm ứng dụng  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  
  
2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]  
  
3. Bấm vào **Tùy chọn**.  
  
4. Bấm vào **Mới** trên thanh lệnh để tạo tùy chọn mới.  
  
5. Đối với các tùy chọn mới, nhập **ClientCacheVersionNumber** trong hộp **tên** và số gồm số và chữ cái trong hộp **giá trị**. Giá trị số và chữ cái được sử dụng như là khóa bộ nhớ đệm cho [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].  
  
6. Bấm vào **Lưu**.  
  
   Khi các tùy chọn đã có và được xác định, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sẽ kích hoạt bộ nhớ đệm ứng dụng.  
  
<a name="CachingStoreLocation"></a>   
## <a name="client-caching-store-location"></a>Vị trí lưu trữ bộ nhớ đệm ứng dụng  
 Khi được bật, bộ nhớ đệm ứng dụng lưu trữ các tệp của mình dưới định dạng mã hóa và nén trong thư mục chuyển vùng của người dùng: %appData%\Microsoft\USD  
  
 For example, for a user called agent1 running the client application on [!INCLUDE[pn_windows8](../../includes/pn-windows8.md)], the client caching files will be available at c:\Users\agent1\AppData\Roaming\Microsoft\USD.  
  
 Thông tin trong thư mục này chỉ có thể được truy cập bằng tài khoản người dùng tạo ra nó.  
  
<a name="PushUpdatetoAllClients"></a>   
## <a name="push-an-update-to-clients"></a>Tạo bản cập nhập cho khách hàng  
 Để tạo bản cập nhật cho tất cả khách hàng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], bạn phải chỉnh sửa giá trị của **ClientCacheVersionNumber** mà bạn tạo ra trước đó với giá trị số khác nhau. Lần tiếp theo khi nhật ký tổng đài viên trung tâm cuộc gọi đang sử dụng ứng dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], nhật ký sẽ phát hiện giá trị khác nhau cho các phím tùy chọn **ClientCacheVersionNumber** và đọc tất cả cài đặt từ máy chủ trước khi khởi động.  
  
<a name="DisableClientCachingforUser"></a>   
## <a name="disable-client-caching-for-a-specific-user"></a>Tắt bộ nhớ đệm ứng dụng cho một người dùng cụ thể  
 Đôi khi nó việc loại trừ một số người dùng từ bộ nhớ đệm ứng dụng có thể cần thiết chẳng hạn như thử nghiệm giới hạn các cấu hình mới trong sản xuất, sản xuất, hoặc khắc phục sự cố khi nghi ngờ có sự cố bộ nhớ đệm hoặc sự cần thiết để thực hiện cập nhật nhanh cấu hình mà bạn muốn hoàn nguyên thay đổi của mình về đối tượng hiện được lưu trong bộ nhớ đệm.  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  
  
2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]  
  
3. Click **User Settings**.  
  
4. Bấm vào **Mới** trên thanh lệnh để tạo cài đặt mới.  
  
5. Trên trang **Cài đặt người dùng mới**:  
  
   1.  Trong trường **người dùng**, nhập hoặc chọn tên người dùng mà bạn muốn tắt bộ nhớ đệm ứng dụng.  
  
   2.  Trong trường **tên**, nhập **DisableCaching**. Để trống trường **giá trị**.  
  
   ![Disable client caching for a user](../../unified-service-desk/media/usd-disable-client-caching-user.PNG "Disable client caching for a user")  
  
6. Bấm vào **Lưu**.  
  
   Khi người dùng tiếp theo đăng nhập bằng cách sử dụng ứng dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], bộ nhớ đệm ứng dụng không được sử dụng. Tuy nhiên, nó không xóa hoặc làm mới lưu trữ bộ nhớ đệm ứng dụng cho người dùng. Khi khóa **DisableCaching** được xóa cho người dùng, người dùng sẽ quay lại sử dụng lưu trữ bộ nhớ đệm ứng dụng đã lưu trước đó.  
  
<a name="ForceCacheReset"></a>   
## <a name="force-a-cache-reset-for-a-specific-user"></a>Bắt buộc đặt lại bộ nhớ đệm cho người dùng cụ thể  
 Đôi khi, điều này có thể là cần thiết khi bắt buộc đặt lại bộ nhớ đệm cho người dùng cụ thể để xóa và đặt lại lưu trữ bộ nhớ đệm. Bạn có thể làm điều này bằng hai cách: từ máy chủ [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] hoặc bằng cách sử dụng các ứng dụng khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] trên máy tính của người dùng.  
  
<a name="UsingCRMServer"></a>   
### <a name="using-the-dynamics-365-for-customer-engagement-server"></a>Using the Dynamics 365 for Customer Engagement server  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  
  
2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]  
  
3. Click **User Settings**.  
  
4. Click **New** on the command bar to create a new setting.  
  
5. Trên trang **Cài đặt người dùng mới**:  
  
   1.  Trong trường **người dùng**, nhập hoặc chọn tên người dùng mà bạn muốn tắt bộ nhớ đệm ứng dụng.  
  
   2.  Trong trường **Tên**, nhập **ResetDesktopCache**. Leave the **Value** field empty.  
  
6. Bấm vào **Lưu**.  
  
   The ResetDesktopCache setting causes the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application to delete its local cache store and rebuild it from the server.  
  
   To complete the cache reset process, two restarts of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client are required.  
  
7. After the first [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application restart, the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client loads data from the existing cache. Afterwards, the existing cache is deleted and the ResetDesktopCache setting is disabled.  
  
8. After the second [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application restart, the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client loads the configuration directly from the server and re-creates the cache.  Notice that the time it takes for the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client to load during this time can increase significantly.  
  
### <a name="using-the-unified-service-desk-client"></a>Sử dụng ứng dụng Unified Service Desk  
 Bạn có thể hủy việc đặt lại từ ứng dụng khách bằng cách sử dụng thao tác UII ẩn được gọi là **ResetLocalCache** trên loại kiểm soát tổ chức **trình quản lý chung**. Bạn sẽ cần phải tạo thao tác UII trên loại kiểm soát tổ chức trình quản lý chung trước khi có thể sử dụng.  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  
  
2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]  
  
3. Click **Hosted Controls**.  
  
4. Locate the **Dynamics 365 for Customer Engagement apps Global Manager** hosted control, and click its name in the **Name** column to open it for editing.  
  
   > [!NOTE]
   > **Dynamics 365 for Customer Engagement apps Global Manager** is the name of the hosted control in the sample [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] applications. Nếu bạn đã đặt tên khác cho kiểm soát tổ chức trình quản lý chung của mình, hãy chọn tên đó để thay thế. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Global Manager (Hosted Control)](../../unified-service-desk/global-manager-hosted-control.md)  
  
5. On the nav bar, click the down arrow next to the **Dynamics 365 for Customer Engagement apps Global Manager** hosted control, and then select **UII Actions**.  
  
   ![Navigation to UII Actions for hosted control](../../unified-service-desk/media/usd-hosted-contro-uii-action.png "Navigation to UII Actions for hosted control")  
  
6. Trên trang tiếp theo, bấm vào **thêm hành động UII mới**.  
  
7. Trên trang **Hành động UII mới**, nhập **ResetLocalCache** trong trường **tên** sau đó nhấp vào **Lưu**. Đóng các hành động UII và kiểm soát tổ chức.  
  
    Tiếp theo, chúng tôi sẽ thêm một cuộc gọi hành động để gọi hành động UII mà chúng tôi vừa tạo.  
  
8. On the nav bar, click **Settings** > **Unified Service Desk** > **Action Calls**.  
  
9. Trên trang cuộc gọi hành động tiếp theo, bấm vào **Mới**.  
  
10. Trên trang **Cuộc gọi hành động mới**:  
  
    1. Trong trường **Tên**, nhập **ResetClientCache**.  
  
    2. In the **Hosted Control** field, specify the **Dynamics 365 for Customer Engagement apps Global Manager**.  
  
       > [!NOTE]
       > **Dynamics 365 for Customer Engagement apps Global Manager** is the name of the hosted control in the sample [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] applications. If you have named your Global Manager hosted control something else, select it instead. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Global Manager (Hosted Control)](../../unified-service-desk/global-manager-hosted-control.md)  
  
    3. Trong trường **Hành động**, chỉ định **ResetLocalCache**.  
  
11. Bấm vào **Lưu** và sau đó đóng cuộc gọi hành động.  
  
    After you have set up the UII action and the action call, you can add a toolbar button, event, or code to directly invoke the action call from the client application. This creates a **RestDesktopCache** setting in the **User Settings** area, which triggers the reset behavior as described earlier in [Using the Dynamics 365 for Customer Engagement server](../../unified-service-desk/admin/configure-client-caching-unified-service-desk.md#UsingCRMServer).  
  
## <a name="see-also"></a>Xem thêm  
 [Ứng dụng Unified Service Desk mẫu](../../unified-service-desk/admin/sample-unified-service-desk-applications.md)   
 [Administer and manage Unified Service Desk](../../unified-service-desk/admin/administer-manage-unified-service-desk.md)   
 [Thêm một hành động UII vào một điều khiển tổ chức](../../unified-service-desk/add-uii-action-hosted-control.md)   
 
