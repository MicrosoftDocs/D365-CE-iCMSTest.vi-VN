---
title: Guide customer interactions with agent scripts in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Agent scripting in Unified Service Desk provides guidance to agents about what they should say on calls or what they should type on chat conversations. It includes a script that can use values from any loaded entity on the agent application, hosted control, or the Unified Service Desk context (using replacement parameters).
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
ms.assetid: 2e6af283-c0c9-4cce-92b1-88485748e0a8
caps.latest.revision: 5
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 0fec68eceb08b5a464641fb0d893b4cbeb25480c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385477"
---
# <a name="guide-customer-interactions-with-agent-scripts-in-unified-service-desk"></a><span data-ttu-id="f36a1-104">Guide customer interactions with agent scripts in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="f36a1-104">Guide customer interactions with agent scripts in Unified Service Desk</span></span>
<span data-ttu-id="f36a1-105">Mã lệnh tổng đài viên trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] cung cấp hướng dẫn cho các tổng đài viên về những gì họ nên nói về các cuộc gọi hoặc những gì họ nên nhập vào cuộc hội thoại trò chuyện.</span><span class="sxs-lookup"><span data-stu-id="f36a1-105">Agent scripting in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] provides guidance to agents about what they should say on calls or what they should type on chat conversations.</span></span> <span data-ttu-id="f36a1-106">Nó bao gồm mã lệnh mà có thể sử dụng các giá trị từ bất kỳ thực thể được tải nào trên ứng dụng tổng đài viên, kiểm soát tổ chức, hoặc bối cảnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] (bằng cách sử dụng tham số thay thế).</span><span class="sxs-lookup"><span data-stu-id="f36a1-106">It includes a script that can use values from any loaded entity on the agent application, hosted control, or the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] context (using replacement parameters).</span></span> <span data-ttu-id="f36a1-107">Mã lệnh tổng đài viên cũng cung cấp một cơ chế để hiển thị hướng dẫn cho tổng đài viên về cách và những gì cần thực hiện tác vụ cần thiết để hoàn thành công việc của họ.</span><span class="sxs-lookup"><span data-stu-id="f36a1-107">Agent scripting also provides a mechanism to display instructions to the agent on what and how to perform the tasks necessary to complete their work.</span></span>  
  
 <span data-ttu-id="f36a1-108">Các mô-đun mã lệnh hỗ trợ phân nhánh cho luồng công việc tổng đại lý phi tuyến tính.</span><span class="sxs-lookup"><span data-stu-id="f36a1-108">The scripting module supports branching for non-linear agent workflow.</span></span> <span data-ttu-id="f36a1-109">Nó cũng hỗ trợ việc chuyển sang mã lệnh cụ thể dựa trên các biến như nút được xác định trong giao diện người dùng, sự kiện tích hợp điện thoại máy tính (CTI) và thông số chẳng hạn như dịch vụ xác định số được quay (DNIS).</span><span class="sxs-lookup"><span data-stu-id="f36a1-109">It also supports jumping to specific scripts based on variables such as buttons defined in the UI, computer telephony integration (CTI) events, and parameters such as dialed number identification service (DNIS).</span></span> <span data-ttu-id="f36a1-110">Lịch sử của các bước được giữ trong danh sách thả xuống để người dùng có thể quay trở lại bước đã truy cập trước đó.</span><span class="sxs-lookup"><span data-stu-id="f36a1-110">A history of steps is kept in a drop-down list so that the user can return to a previously visited step.</span></span> <span data-ttu-id="f36a1-111">Hành động đã được thực hiện trên quá trình không hoàn tác khi tổng đài viên trở lại bước trước.</span><span class="sxs-lookup"><span data-stu-id="f36a1-111">Actions that were performed along the way aren’t undone when an agent returns to a previous step.</span></span> <span data-ttu-id="f36a1-112">Nếu câu trả lời đã được truy cập, hộp kiểm sẽ xuất hiện bên cạnh nó.</span><span class="sxs-lookup"><span data-stu-id="f36a1-112">If an answer has already been visited, a check box will appear next to it.</span></span>  
  
## <a name="components-of-an-agent-script"></a><span data-ttu-id="f36a1-113">Thành phần của mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="f36a1-113">Components of an agent script</span></span>  
 <span data-ttu-id="f36a1-114">Sau đây là mã lệnh tổng đài viên mẫu trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="f36a1-114">The following is a sample agent script in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  
  
 <span data-ttu-id="f36a1-115">![Agent script in Unified Service Desk](../unified-service-desk/media/usd-agent-script.png "Agent script in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="f36a1-115">![Agent script in Unified Service Desk](../unified-service-desk/media/usd-agent-script.png "Agent script in Unified Service Desk")</span></span>  
  
- <span data-ttu-id="f36a1-116">**Lịch sử và bước hiện tại**: Danh sách thả xuống (chào mừng bạn đến với Phiên liên hệ) hiển thị bước hiện tại.</span><span class="sxs-lookup"><span data-stu-id="f36a1-116">**Current step and history**: The drop down list (Welcome to Contact Session) shows the current step.</span></span> <span data-ttu-id="f36a1-117">Nếu bạn nhấp vào danh sách, bạn sẽ thấy một lịch sử về nơi bạn đã ở.</span><span class="sxs-lookup"><span data-stu-id="f36a1-117">If you click the list, you’ll see a history of where you have been.</span></span> <span data-ttu-id="f36a1-118">Bạn có thể chọn một bước trước đó từ danh sách này để trở về nó.</span><span class="sxs-lookup"><span data-stu-id="f36a1-118">You can select a previous step from this list to return to it.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="f36a1-119">Nếu bạn trở lại một điểm trước đó bằng cách sử dụng danh sách thả-xuống, hành động và đầu vào mà bạn thực hiện trên các ứng dụng trong các bước tiếp theo sẽ không thể quay lại.</span><span class="sxs-lookup"><span data-stu-id="f36a1-119">If you go back to a previous point using the drop-down list, the actions and input that you performed on applications during the subsequent steps aren’t rolled back.</span></span>  
  
- <span data-ttu-id="f36a1-120">**Văn bản giới thiệu**: Đây là văn bản được sử dụng bằng tổng đài viên để bắt đầu cuộc trò chuyện với khách hàng.</span><span class="sxs-lookup"><span data-stu-id="f36a1-120">**Introductory text**: This is the text that is used by the agent to initiate conversation with the customer.</span></span> <span data-ttu-id="f36a1-121">Văn bản này hỗ trợ các tham số thay thế từ ngữ cảnh dữ liệu [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="f36a1-121">This text supports replaceable parameters from the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] data context.</span></span> <span data-ttu-id="f36a1-122">Nếu trường này bị để trống khi bạn tạo mã lệnh tổng đài viên, phần sẽ không được trình bày trong màn hình cho tổng đài viên và tiêu đề mã lệnh sẽ bị xóa.</span><span class="sxs-lookup"><span data-stu-id="f36a1-122">If this field is left blank when you create the agent script, the section won’t be present in the display to the agents and the script header will be removed.</span></span>  
  
     <span data-ttu-id="f36a1-123">Nếu một cuộc hội thoại trò chuyện bắt đầu phiên, nút sẽ hiển thị bên cạnh mã lệnh tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="f36a1-123">If a chat conversation initiates the session, a button will show next to the agent script.</span></span> <span data-ttu-id="f36a1-124">Khi nút này được nhấn vào, các văn bản sẽ được sao chép vào đầu ra tương thích trò chuyện tự động.</span><span class="sxs-lookup"><span data-stu-id="f36a1-124">When this button is clicked, the text will be copied to the compatible chat output automatically.</span></span>  
  
- <span data-ttu-id="f36a1-125">**Hướng dẫn cho tổng đài viên**: văn bản này cung cấp hướng dẫn cho tổng đài viên về hoạt động cần được thực hiện.</span><span class="sxs-lookup"><span data-stu-id="f36a1-125">**Instructions to agent**: This text provides instructions to the agent about the action that should be performed.</span></span> <span data-ttu-id="f36a1-126">Nó có thể cung cấp gợi ý hoặc các hướng dẫn khác.</span><span class="sxs-lookup"><span data-stu-id="f36a1-126">It may provide hints or other instructions as well.</span></span> <span data-ttu-id="f36a1-127">Nếu trường này bị để trống khi bạn tạo mã lệnh tổng đài viên, tiêu đề và văn bản sẽ không hiển thị cho ứng dụng khi đang thực hiện tác vụ này.</span><span class="sxs-lookup"><span data-stu-id="f36a1-127">If this field is left blank when you create the agent script, the header and the text won’t display to the client while on this task.</span></span> <span data-ttu-id="f36a1-128">Văn bản hướng dẫn này xuất hiện trong các phông chữ khác nhau từ mã lệnh giới thiệu.</span><span class="sxs-lookup"><span data-stu-id="f36a1-128">This instructional text appears in different font from the introductory script.</span></span>  
  
- <span data-ttu-id="f36a1-129">**Bước/ Câu trả lời kế tiếp**: Ngăn xếp chồng các nút này cho thấy các lựa chọn có thể cho bước tiếp theo.</span><span class="sxs-lookup"><span data-stu-id="f36a1-129">**Next Steps/Answers**: This stack of buttons shows possible choices for next steps.</span></span> <span data-ttu-id="f36a1-130">Một hành động có thể được thực hiện để đáp ứng với việc nhấp vào một trong các câu trả lời hoặc một hành động có thể thực hiện khi đạt đến công việc tiếp theo.</span><span class="sxs-lookup"><span data-stu-id="f36a1-130">An action may be performed in response to clicking one of the answers or an action may execute when reaching the next task.</span></span>  
  
  [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="f36a1-131">[Configure and manage agent scripts](../unified-service-desk/configure-manage-agent-scripts.md)</span><span class="sxs-lookup"><span data-stu-id="f36a1-131">[Configure and manage agent scripts](../unified-service-desk/configure-manage-agent-scripts.md)</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f36a1-132">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="f36a1-132">See also</span></span>  
 <span data-ttu-id="f36a1-133">[Mã lệnh tổng đài viên (Kiểm soát tổ chức)](../unified-service-desk/agent-scripting-hosted-control.md) </span><span class="sxs-lookup"><span data-stu-id="f36a1-133">[Agent Scripting (Hosted Control)](../unified-service-desk/agent-scripting-hosted-control.md) </span></span>  
 <span data-ttu-id="f36a1-134">[Thông số thay thế](../unified-service-desk/replacement-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="f36a1-134">[Replacement parameters](../unified-service-desk/replacement-parameters.md) </span></span>  
 <span data-ttu-id="f36a1-135">[UII Computer Telephony Integration (CTI) framework](../unified-service-desk/uii-computer-telephony-integration-cti-framework.md) </span><span class="sxs-lookup"><span data-stu-id="f36a1-135">[UII Computer Telephony Integration (CTI) framework](../unified-service-desk/uii-computer-telephony-integration-cti-framework.md) </span></span>  
 [<span data-ttu-id="f36a1-136">Cách 7: Đặt cấu hình mã lệnh tổng đài viên trong ứng dụng tổng đài viên của bạn</span><span class="sxs-lookup"><span data-stu-id="f36a1-136">Walkthrough 7: Configure agent scripting in your agent application</span></span>](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md)
