---
title: Configure and manage agent scripts | MicrosoftDocs
description: Learn about configuring and managing agent scripts.
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
ms.assetid: c4b63840-4613-46d9-a843-23233c259b60
caps.latest.revision: 6
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: ef58211e72f1680503113829e5dd85be5e65e6ad
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386852"
---
# <a name="configure-and-manage-agent-scripts"></a>Configure and manage agent scripts
Mỗi bước trong mã lệnh tổng đài viên được thể hiện như một nhiệm vụ mã lệnh tổng đài viên. Nhiệm vụ mã lệnh tổng đài viên có thể có một hoặc nhiều câu trả lời (lựa chọn) cho các bước tiếp theo; câu trả lời được đại diện như là một ngăn xếp của các nút trong vùng mã lệnh tổng đài viên trong ứng dụng của bạn. Một hành động có thể được thực hiện khi nhấp vào một trong các câu trả lời hoặc khi bạn đi đến công việc tiếp theo. Chủ đề này cung cấp thông tin về cách bạn có thể tạo một tác vụ mã lệnh tổng đài viên và sau đó cấu hình nó bằng cách thêm câu trả lời, hành động và bộ khởi động.  

 For more information about how agent scripts work in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Guide customer interactions with agent scripts](../unified-service-desk/guide-customer-interactions-agent-scripts.md). For a walkthrough that demonstrates the agent scripting functionality, see [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md).  

<a name="create"></a>   
## <a name="create-an-agent-script-task"></a>Tạo một tác vụ mã lệnh tổng đài viên  

1. Sign in to Microsoft Dynamics 365 for Customer Engagement apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Click **Agent Scripts**. Trang hiển thị tác vụ mã lệnh tổng đài viên có sẵn.  

   ![Active agent script tasks](../unified-service-desk/media/usd-agent-scripts.png "Active agent script tasks")  

4. Bấm vào **MỚI** trên thanh lệnh, và sau đó xác định các thông tin sau đây trong trang **Tác vụ mã lệnh tổng đài viên mới**:  


   |      Trường       |                                                                                                                                                                                                                                                                                                                                                                                       Mô tả                                                                                                                                                                                                                                                                                                                                                                                       |
   |------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |     **Tên**     |                                                                                                                                                                                                                                                                                                                                                              Tên mà sẽ xuất hiện trong vùng bước và lịch sử hiện tại.                                                                                                                                                                                                                                                                                                                                                              |
   |  **Bắt đầu nhiệm vụ**   | Chọn **có** hoặc **Không**:<br /><br /> - **Có**: nhiệm vụ này sẽ được hiển thị lúc bắt đầu một phiên.  Thông thường, bảo mật của người dùng sẽ chỉ cung cấp cho họ lúc bắt đầu nhiệm vụ.  Nhiệm vụ bắt đầu có thể đại diện cho các khu chức năng hoặc kỹ năng của tổng đài viên.  Khi tổng đài viên tích lũy được nhiều kinh nghiệm, họ có thể nhận được nhiều nhiệm vụ bắt đầu hơn (đào tạo liên kết).  Nếu hai hoặc nhiều nhiệm vụ bắt đầu được gán cho một tổng đài viên, **[Menu chính]** đặc biệt sẽ được hiển thị dưới dạng nhiệm vụ đầu tiên cho tổng đài viên.  Các nút sau đó sẽ trở thành các nhiệm vụ bắt đầu mà người dùng có thể truy cập.<br />- **No**: These may be accessed from answers of other tasks or you may call [GoToTask](../unified-service-desk/agent-scripting-hosted-control.md#GoToTask) action on the **Agent Scripting** hosted control to access a specific task. |
   |   **Hiển thị Tab**   |                                                                                                                                                                                                                                        Chọn kiểm soát tổ chức (tab) nên được thiết lập để tập trung khi nhiệm vụ này đạt được bởi người dùng.  Điều này có thể được sử dụng để đặt người dùng trên kiểm soát mà sẽ giúp người dùng thực hiện các hành động cần thiết cho bước công việc này.  Nếu trường này bị để trống, không có thay đổi nào cho tab tập trung.                                                                                                                                                                                                                                        |
   |   **Thể loại**   |                                                                                                                                                                                                                                                                                     Specify a category name to group, filter, or sort agent script tasks Microsoft Dynamics 365 for Customer Engagement apps while managing agent script tasks.<br /><br /> Giá trị loại không được sử dụng bởi tổng đài viên trong ứng dụng khách.                                                                                                                                                                                                                                                                                      |
   |  **Văn bản mã lệnh**  |                                                                                                                                                                                                                        Đây là mã lệnh mà tổng đài viên nên đọc cho người gọi ở giai đoạn này.  Trường này hỗ trợ thông số thay thế.  Để chèn biến bối cảnh, **họ và tên** vào mã lệnh, gõ **[[họ tên]]** vào dòng mã lệnh.  Tại thời gian chạy, nó sẽ thay thế văn bản này với giá trị từ bối cảnh cho phiên hiện tại.                                                                                                                                                                                                                        |
   | **Hướng dẫn** |                                                                                                                                                                                                                                                                                                   Đây là hướng dẫn cho người dùng về những gì họ nên làm để hoàn thành công việc của họ.  Thông tin này được hiển thị trong phông chữ khác so với **Văn bản mã lệnh** để giúp phân biệt nó.                                                                                                                                                                                                                                                                                                   |


5. Bấm vào **Lưu** để lưu hồ sơ và kích hoạt vùng **câu trả lời**.  

   Hình ảnh sau đây minh họa định nghĩa nhiệm vụ mã lệnh tổng đài viên.  

   ![Sample agent script task](../unified-service-desk/media/usd-sample-agent-script-task.png "Sample agent script task")  

<a name="Answers"></a>   
## <a name="add-answers-to-an-agent-script-task"></a>Thêm câu trả lời vào nhiệm vụ mã lệnh tổng đài viên  
 Nhiệm vụ có thể có một chuỗi câu trả lời được đính kèm vào.  Mỗi câu trả lời được thể hiện như một nút trong giao diện người dùng dưới mã lệnh và hướng dẫn.  

 Để thêm câu trả lời vào nhiệm vụ mã lệnh tổng đài viên:  

1. Open an agent script task definition by clicking its name on the agent scripts page (**Settings** > **Unified Service Desk** > **Agent Scripts**).  

2. Bạn có thể thêm câu trả lời trong một trong hai cách sau:  

   -   In the **Answers** area of the agent script task definition page, click **+**.  

   -   Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh tên nhiệm vụ mã lệnh tổng đài viên, bấm vào **câu trả lời**, và sau đó nhấp vào **thêm câu trả lời mã lệnh tổng đài viên hiện có**.  

   ![Add answer, action, or script task triggers](../unified-service-desk/media/usd-agent-script-answer.png "Add answer, action, or script task triggers")  

3. Trong hộp tìm kiếm cho câu trả lời hiện có, bấm biểu tượng tìm kiếm hoặc nhấn ENTER. Từ kết quả tìm kiếm, hãy nhấp vào **Mới** ở dưới cùng của ngăn kết quả tìm kiếm.  

4. Trên trang **Câu trả lời mã lệnh tổng đài viên mới**, chỉ định các chi tiết sau:  


   |      Trường      |                                                                              Mô tả                                                                              |
   |-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Tên**     | Đây là tê mô tả cho câu trả lời.  Tên này sẽ không được nhìn thấy bởi tổng đài viên.  Nó là hữu ích cho các mục đích hành chính trong việc phân biệt nhiệm vụ này với các nhiệm vụ khác. |
   | **Văn bản câu trả lời**  |                                                    Đây là nhãn được hiển thị trên nút trong ứng dụng tổng đài viên.                                                    |
   | **Nhiệm vụ được liên kết** |                               Khi người dùng nhấp vào câu trả lời này (các nút trong ứng dụng khách), họ sẽ đi đến nhiệm vụ liên kết.                               |
   |    **Đơn hàng**    |         Xác định thứ tự xuất hiện của câu trả lời (nút) trong ứng dụng khách nếu có rất nhiều câu trả lời được đính kèm vào một nhiệm vụ mã lệnh tổng đài viên.          |


5. Bấm vào **Lưu** để lưu hồ sơ.  

   Hình ảnh sau đây minh họa định nghĩa câu trả lời cụ thể.  

   ![Sample agent script answer](../unified-service-desk/media/usd-sample-agent-script-answer.png "Sample agent script answer")  

<a name="ActionCallsAnswers"></a>   
## <a name="add-action-calls-to-an-answer"></a>Thêm cuộc gọi hành động vào câu trả lời  
 Sau khi thêm câu trả lời cho nhiệm vụ mã lệnh tổng đài viên, bạn phải đính kèm các cuộc gọi hành động vào câu trả lời của bạn, xác định danh sách các hành động được thực hiện trong ứng dụng tổng đài viên khi các tổng đài viên nhấp vào câu trả lời. Những cuộc gọi hành động xảy ra trước khi chuyển sang công việc tiếp theo.  Cuộc gọi hành động là cơ chế trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để gọi hành động UII được xác định cho kiểm soát tổ chức. For more information, see [Action calls](../unified-service-desk/action-calls.md).  

 Để thêm cuộc gọi hành động vào câu trả lời:  

1. Mở câu trả lời mã lệnh tổng đài viên hiện có.  

2. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh tên câu trả lời và sau đó bấm vào **Hoạt động**.  

   ![Menu navigation to add an action call to an answer](../unified-service-desk/media/usd-action-call-answer.png "Menu navigation to add an action call to an answer")  

3. Trên trang tiếp theo, bấm vào **thêm cuộc gọi hành động hiện có** để tìm kiếm cuộc gọi hành động để thêm nó vào câu trả lời. Gõ tên cho các cuộc gọi hành động mà bạn muốn thêm, và nhấn ENTER hoặc nhấp biểu tượng tìm kiếm. To do a wildcard search, type a part of the action call name within asterisks (*); for example **\*account\\***. Điều này sẽ hiển thị tất cả các cuộc gọi hành động trong ngăn kết quả tìm kiếm, có "tài khoản" trong tên của họ.  

    Bạn cũng có thể tạo một cuộc gọi hành động mới bằng cách nhấn vào **Mới** ở dưới cùng của ngăn kết quả tìm kiếm. For information about creating a new action call, see [Create an action call for a UII action](../unified-service-desk/create-action-call-uii-action.md).  

4. Bạn có thể thêm nhiều cuộc gọi hành động vào một câu trả lời. Sau khi thêm nhiều cuộc gọi hành động, bấm đúp vào mỗi cuộc gọi hành động trong danh sách, và chỉ định **Thứ tự** mà bạn muốn cuộc gọi hành động được thực hiện khi tổng đài viên nhấp vào câu trả lời.  

5. Bấm vào **Lưu** để lưu hồ sơ.  

   Những hành động này thường được sử dụng khi một nhiệm vụ chung chính là bước tiếp theo.  Như vậy câu trả lời khác nhau có thể thực hiện hành động khác nhau, nhưng kết thúc tại nhiệm vụ tương tự, do đó giảm số lượng các công việc cần thiết để đáp ứng quy trình kinh doanh.  

<a name="ActionCallforTask"></a>   
## <a name="add-action-calls-to-an-agent-script-task"></a>Thêm cuộc gọi hành động vào nhiệm vụ mã lệnh tổng đài viên  
 Đây là cuộc gọi hành động ở cấp độ nhiệm vụ, và mỗi hành động trong danh sách được thực hiện khi các tổng đài viên đạt đến công việc trong ứng dụng khách.  Điều này có thể bao gồm các hoạt động tự động hóa của ứng dụng hiển thị hoặc các hành động khác mà đáp ứng yêu cầu kinh doanh.  

 Để thêm cuộc gọi hành động cho nhiệm vụ mã lệnh tổng đài viên:  

1. Open an agent script task definition by clicking its name on the agent scripts page (**Settings** > **Unified Service Desk** > **Agent Scripts**).  

2. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh tên nhiệm vụ mã lệnh tổng đài viên và sau đó bấm vào **Hoạt động**.  

   ![Add answer, action, or script task triggers](../unified-service-desk/media/usd-agent-script-answer.png "Add answer, action, or script task triggers")  

3. Trên trang tiếp theo, bấm vào **thêm cuộc gọi hành động hiện có** để tìm kiếm cuộc gọi hành động để thêm nó vào nhiệm vụ mã lệnh tổng đài viên. Gõ tên cho các cuộc gọi hành động mà bạn muốn thêm, và nhấn ENTER hoặc nhấp biểu tượng tìm kiếm. To do a wildcard search, type a part of the action call name within asterisks (*); for example **\*account\\***. This will display all the action calls in the search results pane that have “account” in their name.  

    You can also create a new action call by clicking **New** at the bottom of the search results pane. For information about creating a new action call, see [Create an action call for a UII action](../unified-service-desk/create-action-call-uii-action.md).  

4. You can add multiple action calls to an answer. Sau khi thêm nhiều cuộc gọi hành động, bấm đúp vào mỗi cuộc gọi hành động trong danh sách, và chỉ định **Thứ tự** mà bạn muốn cuộc gọi hành động được thực hiện khi tổng đài viên đạt đến nhiệm vụ.  

5. Bấm vào **Lưu** để lưu hồ sơ.  

<a name="AgentScriptTriggers"></a>   
## <a name="add-triggers-to-an-agent-script-task"></a>Thêm bộ khởi động cho nhiệm vụ mã lệnh tổng đài viên  
 Đây là những biến được dùng để chỉ một nhiệm vụ cụ thể. Để thêm bộ khởi động cho nhiệm vụ mã lệnh tổng đài viên:  

1. Open an agent script task definition by clicking its name on the agent scripts page (**Settings** > **Unified Service Desk** > **Agent Scripts**).  

2. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh tên nhiệm vụ mã lệnh tổng đài viên và sau đó bấm vào **Bộ khởi động nhiệm vụ mã lệnh**.  

   ![Add answer, action, or script task triggers](../unified-service-desk/media/usd-agent-script-answer.png "Add answer, action, or script task triggers")  

3. Trên trang tiếp theo, bấm vào **thêm bộ khởi động nhiệm vụ mã lệnh mới**.  

4. Trên trang **Bộ khởi động Tác vụ mã lệnh tổng đài viên mới**, chỉ định thông tin sau:  


   |  Trường   |                                                                                                                                                                                                                                                                                                                                     Mô tả                                                                                                                                                                                                                                                                                                                                      |
   |----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | **Tên** |                                                                                                                                                                                                                                                                                          Đây là tê mô tả cho bộ khởi động tác vụ mã lệnh.  Tên này sẽ không được nhìn thấy bởi tổng đài viên.                                                                                                                                                                                                                                                                                           |
   | **Loại** | Chọn từ các tùy chọn sau:<br /><br /> - **DNIS**: điều này có nghĩa cho kịch bản tích hợp CTI. Chọn tùy chọn này để thực hiện một nhiệm vụ mã lệnh tổng đài viên dựa trên cuộc gọi đến. **Note:** [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] does not ship with any out-of-box CTI adapters. Điều này chỉ áp dụng nếu bạn đang sử dụng bất kỳ giải pháp CTI với [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. For more information about CTI, see [Integrate CTI applications with Unified Service Desk](../unified-service-desk/integrate-cti-systems-cti-adapters.md).<br />- **Khác**: sử dụng thông tin này cho các kịch bản khác. |
   | **Dữ liệu** |                                                                                                                                                                                                                                                                                                                            Xác định các dữ liệu được thông qua.                                                                                                                                                                                                                                                                                                                            |


5. Bấm vào **Lưu** để lưu hồ sơ.  

<a name="Tips"></a>   
## <a name="tips-on-configuring-agent-scripts"></a>Lời khuyên về cấu hình mã lệnh tổng đài viên  
 Mã lệnh tổng đài viên có thể được sử dụng với các giải pháp CTI để cung cấp trải nghiệm tùy chỉnh tập trung vào khách hàng cho tổng đài viên của bạn. Ví dụ, trong trường hợp một trung tâm cuộc gọi cung ứng mà có thể đại diện cho nhiều công ty, bạn có thể sử dụng bộ khởi động mã lệnh tổng đài viên **DNIS** để hiển thị các mã lệnh đúng dựa trên số điện thoại của khách hàng gọi. Văn bản mã lệnh cũng có thể được sử dụng cho tuyên bố miễn trừ phải được đọc cho khách hàng như là một phần của tuân thủ pháp luật về các cuộc gọi bán hàng.  

 Bạn có thể sử dụng các câu trả lời để đại diện cho các thể loại để phân loại cuộc gọi.  Một khi các cuộc gọi đã được phân loại, một trường hợp sẽ được tạo ra và tự động điền bằng cách sử dụng một hành động. Phương pháp này có thể được kết hợp với danh sách ToDo để làm cho danh sách nhiệm vụ trở nên mạnh mẽ.  

 Một tính năng thú vị về tác vụ mã lệnh tổng đài viên là bất cứ khi nào nhiệm vụ được đạt tới trong các thành phần mã lệnh tổng đài viên, toàn bộ nội dung của các thực thể mà làm cho nhiệm vụ đó được đặt vào danh sách tham số thay thế trong dữ liệu bối cảnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  Điều này có thể được sử dụng để mở rộng các thực thể mã lệnh tổng đài viên để thêm văn bản mẫu email để bất cứ khi nào các đại lý đạt một bước trong mã lệnh, các văn bản mẫu email sẽ có sẵn trong dữ liệu bối cảnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] được sử dụng để xác định email.  

### <a name="see-also"></a>Xem thêm  
 [Hướng dẫn tương tác với khách hàng bằng mã lệnh tổng đài viên](../unified-service-desk/guide-customer-interactions-agent-scripts.md)   
 [Agent Scripting (Hosted Control)](../unified-service-desk/agent-scripting-hosted-control.md)   
 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)   
 [Configure your agent application using Unified Service Desk](../unified-service-desk/configure-agent-application-unified-service-desk.md)
