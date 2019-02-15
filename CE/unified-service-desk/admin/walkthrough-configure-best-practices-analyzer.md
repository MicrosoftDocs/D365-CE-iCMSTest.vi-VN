---
title: 'Walkthrough: Configure Best Practices Analyzer in Unified Service Desk (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: Learn about downloading and installing the Best Practices Analyzer.
ms.custom: ''
ms.date: 05/15/2018
ms.service: usd
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: C1F329C3-2E00-40A5-8BA3-1B6BC16444EA
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: d049d824bdf545b659d79999f4d081d586835658
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382469"
---
# <a name="walkthrough-configure-includepn-best-practices-analyzerincludespn-best-practices-analyzermd-in-includepnunifiedservicedeskincludespn-unified-service-deskmd"></a>Walkthrough: Configure [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]

This walkthrough demonstrates how to configure and setup [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] in your agent application.

![Generate Best Practices Analyzer report](../media/bpa-report-generation-new.gif "Generate Best Practices Analyzer report")

<a name="Step1"></a>   
## <a name="step-1-create-a-includepn-best-practices-analyzerincludespn-best-practices-analyzermd-and-toolbar-container-hosted-control"></a>Step 1: Create a [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] and toolbar container hosted control

In this step, you will create a [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] and toolbar container hosted control.

1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]

3. Bấm **Kiểm soát Tổ chức**.  

4. Bấm vào **Mới**.  

5. Trên trang **Kiểm soát tổ chức mới**, chỉ định các giá trị sau:  


   |         Trường          |                                         Value                                         |
   |------------------------|---------------------------------------------------------------------------------------|
   |          Tên          | [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]  |
   |      Tên Hiển thị      | [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]  |
   |   Loại thành phần USD   |                                  USD Hosted Control                                   |
   | Ứng dụng toàn cầu  |                                        Đã kiểm tra                                        |
   |     Nhóm hiển thị      |                                       Bảng điều khiển chính                                       |
   | Ứng dụng động |                                        Đã kiểm tra                                        |
   |     Người dùng có thể đóng     |                                        Đã kiểm tra                                        |
   |      URI cụm tổ hợp      |               `Microsoft.Crm.UnifiedServiceDesk.BestPracticesAnalyser`                |
   |     Loại cụm tổ hợp      | `Microsoft.Crm.UnifiedServiceDesk.BestPracticesAnalyser.BestPracticesAnalyserControl` |

    ![Create Best Practices Analyzer hosted control](../media/usd-create-bpa-hosted-control.PNG "Create Best Practices Analyzer hosted control")

6. Bấm vào **Lưu**.

7. Bấm vào **Mới**.  

8. Trên trang **Kiểm soát tổ chức mới**, chỉ định các giá trị sau  

   |Trường|Value|  
   |-----------|-----------|
   |Tên|About Toolbar Container|
   |USD Component Type|Bộ chứa thanh công cụ|
   |Nhóm hiển thị|AboutPanel|

    ![Create Toolbar Container hosted control](../media/usd-create-about-toolbar-container-hosted-control.PNG "Create Toolbar Container hosted control")

9. Bấm vào **Lưu**.

<a name="Step2"></a>   
## <a name="step-2-add-a-toolbar-and-attach-it-to-the-toolbar-container"></a>Bước 2: Thêm thanh công cụ và gắn nó vào bộ chứa thanh công cụ

 In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 1.

1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]

3. Bấm vào **Thanh công cụ**.  

4. Bấm vào **Mới**.

5. On the **New Toolbar** page, type **About Toolbar** in the **Name** box, and then click **Save**.  

6. Attach the toolbar to the toolbar container hosted control created in step 1. On the nav bar, click the down arrow next to **About Toolbar**, and click **Hosted Controls**.  

7. On the next page, click **Add Existing Hosted Control**, type `About Toolbar Container` in the search bar, and then press **ENTER** or click the search icon.

8. From the search result, click **About Toolbar Container** to add.

     ![Create toolbar and attach it to Toolbar Container hosted control](../media/usd-create-toolbar-attach-toolbar-container-hosted-control.PNG "Create toolbar and attach it to Toolbar Container hosted control")

9. Bấm vào **Lưu**.

<a name="Step3"></a>   
## <a name="step-3-add-toolbar-button"></a>Step 3: Add toolbar button

 In this step, you’ll create two buttons - **Settings** and **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**, and **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** button under **Settings** button.

1. Sau khi bạn lưu thanh công cụ trong bước 2, vùng **nút** sẽ có sẵn. In the **Buttons** area, click **+** on the right corner to add a button.  

2. Trên trang **Nút thanh công cụ mới**, chỉ định các giá trị sau:  

    |Trường|Value|  
    |-----------|-----------|  
    |Tên|Thiết đặt|
    |Hình ảnh|msdyusd_settings_16|
    |Chú giải công cụ|Thiết đặt|  
    |Thứ tự|100|

     ![Create Settings toolbar button](../media/usd-create-settings-toolbar-button.PNG "Create Settings toolbar button")

3. Bấm vào **Lưu**.

4. After you save the **Settings** toolbar button, Click **New** to create another button called **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**.

5. On the **New Toolbar Button** page, specify the following values:  


   |    Trường    |                                        Value                                         |
   |-------------|--------------------------------------------------------------------------------------|
   |    Tên     | [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] |
   | Văn bản nút |                         [[$Resources.BestPracticesAnalyzer]]                         |
   |   Chú giải công cụ   | [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] |
   |    Thứ tự    |                                          4                                           |

    ![Create Best Practices Analyzer toolbar button](../media/usd-create-best-practices-analyzer-button.PNG "Create Best Practices Analyzer toolbar button")

6. Attach the  **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** button under **Settings** button. On the nav bar, click the down arrow next to **Settings**, and click **Toolbar Buttons**.  

7. On the next page, click **Add Existing Toolbar Button**, type `Best Practices Analyzer` in the search bar, and then press **ENTER** or click the search icon.

Bấm vào **Lưu**.

<a name="Step4"></a>   
## <a name="step-4-add-action-calls-to-display-the-includepn-best-practices-analyzerincludespn-best-practices-analyzermd"></a>Step 4: Add action calls to display the [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]

In this step, you'll add actions calls the to **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** toolbar button so that when you click on it, **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** tab is displayed in the hosted control that you created in step 1.

1. In the **Settings** toolbar button page, on the nav bar, click the down arrow next to **Settings**, and click **Toolbar Buttons**.

2. Select **Best Practices Analyzer** toolbar button from the list.

3. In the **Actions** area, click **+** on the right corner to add a button, and press **ENTER** or click the search icon.  

4. Trong hộp tìm kiếm kết quả, bấm vào **Mới** ở góc dưới bên phải để tạo ra cuộc gọi hành động cho nút thanh công cụ này.

5. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:


   |     Trường      |                                               Value                                               |
   |----------------|---------------------------------------------------------------------------------------------------|
   |      Tên      | Action Call: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] |
   |     Thứ tự      |                                                 1                                                 |
   | Kiểm soát được lưu trữ |       [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]        |
   |     Hành động     |                                              mặc định                                              |

    ![Create action call for Best Practices Analyzer](../media/usd-create-action-call-best-practices-analyzer.PNG "Create action call for Best Practices Analyzer")

6. Bấm vào **Lưu**.

7. In the **Actions** area, click **+** on the right corner and type **Action Call: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** in the text box and Press **ENTER** or click on the search icon.

8. Select the **Action Call: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**. <br>
   The new action call is added to the **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** button.

9. You’ll add another action call to the button to set the focus on the hosted control that show the [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] in the client application. In the **Actions** area, click **+** on the right corner to add an action call.

10. In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.  

11. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.


    |     Trường      |                                            Value                                            |
    |----------------|---------------------------------------------------------------------------------------------|
    |      Tên      | Focus: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] |
    |     Thứ tự      |                                              4                                              |
    | Kiểm soát được lưu trữ |                                     Trình quản lý Chung CRM                                      |
    |     Hành động     |                                           Hiển thị tab                                           |
    |      Dữ liệu      |    [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]     |

    ![Create action call to focus on Best Practices Analyzer](../media/usd-create-action-call-focus-best-practices-analyzer.PNG "Create action call to focus on Best Practices Analyzer")    

12. Bấm vào **Lưu**.

13. In the **Actions** area, click **+** on the right corner and type **Focus: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** in the text box and Press **ENTER** or click on the search icon.

14. Select the **Focus: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**.<br>
    The new action call is added to the **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** button.

<a name="Step5"></a>   
## <a name="step-5-add-the-controls-to-the-configuration"></a>Bước 5: Thêm kiểm soát vào cấu hình  
 In this step, you’ll add the action call, hosted control, toolbar, toolbar buttons, and action calls that were created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration. If you have not created **Contoso Configuration**. Visit, [Walkthrough 1: Build a simple agent application](../../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).

 Thêm sau đây vào **Cấu hình Contoso**.


|                                           Tên kiểm soát                                            |  Loại kiểm soát  |
|---------------------------------------------------------------------------------------------------|----------------|
| Action Call: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] |  Cuộc gọi hành động   |
|    Focus: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]    |  Cuộc gọi hành động   |
|                                      About Toolbar Container                                      | Kiểm soát được lưu trữ |
|       [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]        | Kiểm soát được lưu trữ |
|                                           About Toolbar                                           |    Thanh công cụ     |

 Để thêm kiểm soát vào cấu hình:  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]

3. Bấm **Cấu hình**.  

4. Bấm vào **Cấu hình Contoso** để mở định nghĩa.  

5. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.  

6. On the next page, click **Add Existing Action Call**, type **Action Call: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** in the search bar, and then press **ENTER** or click the search icon.  

7. The action call listed earlier are displayed in the search results. Add these action call.

8. Similarly, add the hosted control and the toolbar by clicking the down arrow next to **Contoso Configuration**, and clicking **Hosted Controls** and **Toolbars** respectively.

9. Bấm vào **Lưu**.

<a name="Step6"></a>   
## <a name="step-6-test-includepn-best-practices-analyzerincludespn-best-practices-analyzermd-in-your-agent-application"></a>Step 6: Test [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] in your agent application

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] is a hosted control that helps you analyze the various parameters of your local computer (system configurations and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]), [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations in Dynamics 365, and Internet Explorer settings in your local computer. After the analysis, [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] displays a report that recommends mitigation steps in case of a warning or error.

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] works best when you handle the warning and error as recommended—this helps you to serve your customers without interruption.

To analyze parameters on your computer, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations, and internet settings, against the best practices rules:

1. Sign in to the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application.

2. On the toolbar, select the **Settings** list.

3. Select **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**.

    ![Create action call to focus on Best Practices Analyzer](../media/best-practices-analyzer-button.PNG "Create action call to focus on Best Practices Analyzer")

4. Select **Start Analysis**.<br>
   [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] displays the report—it can help you determine your next steps.

> [!Note]
> When you relaunch [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and select **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**, the last report that was generated appears in the report area.

## <a name="see-also"></a>Xem thêm

[Analyze best practices in Unified Service Desk](../admin/analyze-best-practices-unified-service-desk.md)

[Download and install Best Practices Analyzer](../admin/download-install-best-practices-analyzer.md)

[Read Best Practices Analyzer report](../admin/read-best-practices-analyzer-report.md)

[Best practice rule categories and parameters](../admin/compliance-categories-parameters-bpa.md)

[System configurations](../admin/system-configurations-bpa.md)

[Internet Explorer settings](../admin/internet-explorer-settings-bpa.md)

[Unified Service Desk configurations](../admin/unified-service-desk-configurations-bpa.md)
