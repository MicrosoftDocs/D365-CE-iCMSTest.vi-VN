---
title: Manage access using Unified Service Desk for Dynamics 365 for Customer Engagement apps configuration | MicrosoftDocs
description: Learn to control how agents use Unified Service Desk for Dynamics 365 for Customer Engagement apps by using configuration.
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
ms.assetid: 91772c31-da1f-453b-9934-0179bc50c398
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
ms.openlocfilehash: 5c7ca5b60aa7f17ca7c2addac4bc0bf4f8a922a8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382446"
---
# <a name="use-unified-service-desk-configuration-to-manage-access"></a>Use Unified Service Desk configuration to manage access
[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration is a great way to filter things that you want your agents to see without having to manage their security roles. Agents can see only those [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] components in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application that are added in a configuration assigned to them.  
  
 Bạn có thể thêm thành phần [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sau trong một cấu hình:  
  
-   Cuộc gọi hành động  
  
-   Mã lệnh tổng đài viên  
  
-   Tìm kiếm Thực thể.  
  
-   Sự kiện  
  
-   Biểu mẫu  
  
-   Kiểm soát tổ chức  
  
-   Tùy chọn  
  
-   Scriptlet  
  
-   Thông tin Phiên  
  
-   Thanh công cụ  
  
-   Nguyên tắc điều hướng cửa sổ  
  
<a name="Create"></a>   
## <a name="create-a-unified-service-desk-configuration"></a>Tạo cấu hình ứng dụng Unified Service Desk  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  
  
2. On the nav bar, click **Microsoft Dynamics 365 for Customer Engagement apps**, and then select **Settings**.  
  
3. Click **Settings** > **Unified Service Desk** > **Configuration**.  
  
4. Trên trang cấu hình, bấm vào **Mới**.  
  
5. On the **New Configuration** page, type the name of the configuration, and then click **Save**.  
  
6. Sau khi cấu hình mới được lưu, trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh tên cấu hình, và sau đó chọn Kiểm soát tổ chức. This shows the components that can be added to a configuration.  
  
   ![Menu with components added to configuration](../../unified-service-desk/media/usd-configuration-1.PNG "Menu with components added to configuration")  
  
7. Bấm vào thành phần để thêm. Trang tìm kiếm Thực thể cho thành phần tương ứng sẽ xuất hiện. Click **Add Existing > \<Component Name>** to search for the existing records. Ví dụ, nếu bạn chọn **cuộc gọi hành động**, bấm vào **thêm cuộc gọi hành động hiện có** trên trang tìm kiếm thực thể.  
  
8. Gõ tên của các thành phần trong hộp tìm kiếm, và sau đó nhấn ENTER hoặc nhấp vào nút tìm kiếm. If a record doesn’t exist, click **New** in the search results box to create an instance of the component you want to add.  
  
   ![Add existing component record](../../unified-service-desk/media/usd-configuration-2.PNG "Add existing component record")  
  
9. Repeat this with other components you want to add to the configuration.  
  
10. After you have added the components, click the **Save** button ![Auto save button](../../unified-service-desk/media/cust-auto-save-icon.png "Auto save button") to save the configuration.  
  
    > [!IMPORTANT]
    >  If no hosted controls are added to a configuration, or if certain hosted controls are not added, such as the Panel Layout, Global Manager, and Connection Manager hosted controls, assigned users may see a blank [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application window. For more information about how to create a sample configuration, see [Walkthrough 1: Build a simple agent application](../../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).  
  
<a name="default"></a>   
## <a name="set-a-configuration-as-the-default"></a>Set a configuration as the default  
 You can set a Configuration as the default configuration by using the Is Default attribute of the Configuration record. Then, any user not assigned to a Configuration will have only the Unified Service Desk components associated with the default configuration cached when they sign in to the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.  
  
### <a name="set-a-configuration-as-the-default"></a>Set a configuration as the default  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  
  
2. On the nav bar, click **Main** > **Settings** > **Unified Service Desk**.  
  
3. Bấm **Cấu hình**.  
  
4. In the Active Configuration list, select for the configuration record you want to make the default.  
  
5. Choose **Set As Default** from the actions menu.  
  
<a name="auditanddiag"></a>   
## <a name="associate-auditing-and-diagnostics-with-a-configuration"></a>Associate auditing and diagnostics with a configuration  
 When you associate an Audit & Diagnostics record with a configuration, only the auditing and diagnostics events specified in the Audit & Diagnostics record are logged, and only for users who are assigned to the configuration. The following procedure describes how to associate an existing Audit & Diagnostics record with a configuration. For information about how to create an Audit & Diagnostics record, see [Configure auditing and diagnostics in Unified Service Desk](../../unified-service-desk/admin/configure-auditing-diagnostics-unified-service-desk.md).  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  
  
2. On the nav bar, click **Main** > **Settings** > **Unified Service Desk**.  
  
3. Bấm **Cấu hình**.  
  
4. In the configuration list, select the configuration record you want to add an Audit & Diagnostic record for.  
  
5. Next to **Audit & Diagnostic Settings**, type the name of the Audit & Diagnostic record in the search box, and then press ENTER or click the search button.  
  
6. After you add the Audit & Diagnostics record, click the **Save** button ![Auto save button](../../unified-service-desk/media/cust-auto-save-icon.png "Auto save button") to save the configuration.  
  
<a name="Assign"></a>   
## <a name="assign-users-to-a-unified-service-desk-configuration"></a>Gán người dùng cho cấu hình ứng dụng Unified Service Desk  
 After you create a [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration, you can assign users to it. Người dùng được gán cho cấu hình chỉ truy cập các thành phần trong ứng dụng khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] được thêm vào trong một cấu hình.  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  
  
2. On the nav bar, click **Microsoft Dynamics 365 for Customer Engagement apps**, and then select **Settings**.  
  
3. Click **Settings** > **Unified Service Desk** > **Configuration**.  
  
4. Trong trang cấu hình, tìm kiếm đối với hồ sơ yêu cầu cấu hình.  
  
5. Để mở một định nghĩa cấu hình, hoặc nhấp vào tên cấu hình, hoặc chọn hồ sơ, và sau đó nhấp vào **chỉnh sửa**. Điều này sẽ mở ra định nghĩa cấu hình.  
  
6. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh tên cấu hình và sau đó bấm vào **Người dùng được gán**.  
  
   ![Navigation to assign users to a configuration](../../unified-service-desk/media/usd-configuration-3.PNG "Navigation to assign users to a configuration")  
  
7. Trên trang tiếp theo, bạn có thể hoặc chỉ định cấu hình cho người dùng hiện tại, hoặc tạo một người dùng mới và chỉ định cấu hình cho nó.  
  
8. Gõ tên của người dùng được yêu cầu trong hộp tìm kiếm, và sau đó nhấn ENTER hoặc nhấp vào nút tìm kiếm.  
  
9. Nhấp vào tên của người sử dụng cần thiết để thêm chúng vào cấu hình. Click the **Save** button ![Auto save button](../../unified-service-desk/media/cust-auto-save-icon.png "Auto save button") to save your changes.  
  
     Nếu bạn nhấp vào tên người dùng theo cột **tên**, Hồ sơ người sử dụng sẽ mở ra, và bạn có thể thấy rằng các [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] cấu hình được gán cho người dùng trong trường **USD cấu hình**.  
  
   ![USD configuration assigned to a user](../../unified-service-desk/media/usd-configuration-4.PNG "USD configuration assigned to a user")  
  
   A user can only be assigned to one Configuration. To assign a user to a different Configuration, you must first remove the existing Configuration.  
  
### <a name="remove-a-user-from-a-configuration"></a>Remove a user from a Configuration  
  
1.  Open the User form for the agent who you want to remove from a Configuration. One way you can do this is through **Settings** > **Security** > **Users**.  
  
2.  On the user form, click the **USD Configuration**.  
  
3.  Press the Delete key to remove the Configuration, and then save the form.  
  
<a name="clone"></a>   
## <a name="clone-a-configuration"></a>Clone a Configuration  
 You can copy a Configuration by cloning it. This lets you quickly copy an existing configuration and corresponding relationships to use for a different Configuration. Because a user can only belong to a single configuration, any users associated with configuration will not be associated with the cloned configuration.  
  
### <a name="clone-a-configuration"></a>Clone a configuration  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  
  
2. On the nav bar, click **Microsoft Dynamics 365 for Customer Engagement apps**, and then select **Settings**.  
  
3. Click **Settings** > **Unified Service Desk** > **Configuration**.  
  
4. In the configuration list, select for the configuration record you want to clone.  
  
5. Choose **Clone** on the actions menu, and when prompted, click **Clone**.  
  
## <a name="see-also"></a>Xem thêm  
 [Manage access using custom security roles](../../unified-service-desk/admin/manage-access-using-unified-service-desk-security-roles.md)   
 [Access management in Unified Service Desk](../../unified-service-desk/admin/security-unified-service-desk.md)   
 [Unified Service Desk Configuration Walkthroughs](../../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)
