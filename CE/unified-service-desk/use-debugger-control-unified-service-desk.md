---
title: Use the Debugger control in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn how to use the Debugger hosted control test your UII actions and action calls, view debug output, and view replacement parameters captured during execution in Unifed Service Desk.
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
ms.assetid: 787baba8-0e58-454a-835b-09cc6161d353
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
ms.openlocfilehash: df2cec1f357b0f0f83e7d173568089701ea1754d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388218"
---
# <a name="use-the-debugger-control-in-unified-service-desk"></a>Use the Debugger control in Unified Service Desk
To use debugger control in one of your sample [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] applications, start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client, click the down arrow next to **Settings**, and then click **Debug**. You can also configure a debugger control if you are configuring Unified Service Desk from scratch. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md)  
  
 The debugger control provides information under these tabs: **Action Calls**, **Debug Output**, and **Data Parameters**. Ngoài ra, trình gỡ lỗi cũng cho phép bạn kiểm tra cuộc gọi hành động hiện có và hành động UII có sẵn trong hệ thống.  
  
<a name="ActionCalls"></a>   
## <a name="action-calls-tab"></a>Tab Cuộc gọi hành động  
 The first tab in the debugger is **Action Calls**. Action calls are the primary mechanisms by which things occur in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Theo dõi tiến độ của quá trình, cũng như các giá trị được sử dụng trong các tham số thay thế, có thể cung cấp cho bạn thông tin giá trị về kiểm soát tổ chức.  
  
 ![Unified Service Desk Debugger Action Calls tab](../unified-service-desk/media/usd-debugger-action-calls.png "Unified Service Desk Debugger Action Calls tab")  
  
 Những điểm nổi bật màu sắc sau đây được sử dụng cho hồ sơ trong tab **cuộc gọi hành động**:  
  
- Yellow indicates an action call didn’t run because a condition failed.  
  
- Red indicates the condition succeeded but the action failed, either due to an exception or because required parameters in the data weren’t replaceable.  
  
  ![Unified Service Desk Debugger Action Call fail](../unified-service-desk/media/usd-debugger-action-calls-issues.PNG "Unified Service Desk Debugger Action Call fail")  
  
  Right-click on a row or multiple rows in the **Action Calls** tab, and select **Copy Data To Clipboard** from the shortcut menu to copy action call data and then paste it in another application (say Microsoft Word or Notepad) to easily review the data or share the copied data with others using email for troubleshooting.  
  
  You can also refresh the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to use the latest configuration changes on the server without having to manually restart it by clicking the refresh icon (![Refresh Unified Service Desk Configuration symbol](../unified-service-desk/media/usd-action-call-refresh-icon.png "Refresh Unified Service Desk Configuration symbol")). On clicking this icon, you are prompted whether to reload the configuration. Click **Yes** to reload the configuration or click **No** to cancel.  
  
<a name="DebugOutput"></a>   
## <a name="debug-output-tab"></a>Gỡ lỗi Tab Đầu ra  
 Tab này sẽ hiển thị người nghe để lại dấu vết. Nếu bạn đính kèm trình gỡ lỗi mã cho các ứng dụng, điều này là đầu ra bạn sẽ nhìn thấy. Nó cũng sẽ hiển thị văn bản sẽ được ghi vào tệp nhật ký.  
  
 ![Unified Service Desk Debug Output tab](../unified-service-desk/media/usd-debugger-debug-output.png "Unified Service Desk Debug Output tab")  
  
<a name="DataParameters"></a>   
## <a name="data-parameters-tab"></a>Tab Tham số dữ liệu  
 Tab này sẽ hiển thị tham số dữ liệu được giữ trong thời gian thực hiện của ứng dụng. Danh sách giá trị sẵn có sẽ thay đổi thường xuyên vì dữ liệu được khám phá từ nhiều cách khác nhau trong khi sử dụng ứng dụng. Các tham số dữ liệu có thể được sử dụng khi đang gọi hành động, để hiển thị, hoặc các mục đích khác trong các ứng dụng bằng cách sử dụng tham số thay thế. System data parameters typically start with “$,” such as “$Global" to help separate them from general data parameters. For more information, see:  [Replacement parameters](../unified-service-desk/replacement-parameters.md).  
  
 You can refresh data parameters by clicking the **Update data parameters** button. Bạn cũng có thể sao chép các thông số dữ liệu vào clipboard của bạn.  
  
 ![Unified Service Desk Debug Data Parameters  tab](../unified-service-desk/media/usd-debugger-data-parameters.png "Unified Service Desk Debug Data Parameters  tab")  
  
<a name="Test"></a>   
## <a name="test-your-action-calls-and-uii-actions"></a>Test your action calls and UII actions  
 The debugger also lets you test the existing action calls and UII actions using different conditions and replacement parameters to experiment and view results however you need. To display the area where you can test action calls and UII actions, click the down arrow above the **Action Calls** tab.  
  
 ![Test action calls & UII actions in debugger](../unified-service-desk/media/usd-customize-display-2.png "Test action calls & UII actions in debugger")  
  
- In the **Action Calls** tab, select an action call from the drop-down list, and then click the **Run Action Call** button ![USD debugger Run Action Call button](../unified-service-desk/media/usd-run-action-call-icon.png "USD debugger Run Action Call button") to view the results of the action call. For more information about testing an action call, see the [Test the action call for customizing your display](https://msdn.microsoft.com/library/dn864892.aspx#Test) section in the topic for customizing a theme.  
  
- Trong tab **Hành động trực tiếp**, bạn có thể trực tiếp gọi hành động UII trên kiểm soát tổ chức trong hệ thống. This is a great way to test action call configuration before creating an action call for the UII action. Tham số thay thế có thể được sử dụng trong trường **dữ liệu** trong khi thử nghiệm hành động UII. If you have the required permissions, you can also create hosted controls and UII actions by clicking the Add buttons next to the respective drop-down lists. This opens the **New Hosted Control** or **New UII Action** page in Internet Explorer based on what you chose to create. For more information about testing a UII action, see the [Run the Unified Service Desk client to work with custom hosted control](https://msdn.microsoft.com/library/dn864925.aspx#run) section in the topic for creating a custom [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] hosted control.  
  
### <a name="see-also"></a>Xem thêm  
 [Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md)   
 [Debug your custom code for Unified Service Desk](../unified-service-desk/debug-custom-code-unified-service-desk.md)
