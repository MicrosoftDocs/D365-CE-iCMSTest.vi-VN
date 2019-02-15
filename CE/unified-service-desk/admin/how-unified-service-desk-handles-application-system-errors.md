---
title: How Unified Service Desk for Dynamics 365 for Customer Engagement apps handles application and system errors | MicrosoftDocs
description: Understand how application and system faults are managed in Unifed Service Desk.
ms.custom:
- dyn365-USD, dyn365-admin
ms.date: 08/23/2017
ms.prod: usd2.0
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Unified Service Desk 2.0
ms.assetid: 01878a81-2b67-44ab-a11d-b19adc407177
caps.latest.revision: 5
author: kabala123
ms.author: kabala
ms.service: dynamics-365-customerservice
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: b052e5cfa96cda2594d1e28510a35ceac7942450
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382482"
---
# <a name="application-and-system-faults"></a><span data-ttu-id="590d4-103">Application and system faults</span><span class="sxs-lookup"><span data-stu-id="590d4-103">Application and system faults</span></span>
<span data-ttu-id="590d4-104">Việc thu thập báo cáo và nhật ký chi tiết, toàn diện về lỗi khi bị trục trặc về thành phần, ứng dụng hoặc hệ thống có thể giúp xác định thời điểm và cách thức diễn ra lỗi.</span><span class="sxs-lookup"><span data-stu-id="590d4-104">Having detailed and comprehensive logging and reporting that occurs during a  component, application, or system fault can help identify when and how the fault occurred.</span></span> <span data-ttu-id="590d4-105">Máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] có thể ghi lại nhật ký chẩn đoán, chi tiết trạng thái hệ thống và ứng dụng cũng như kết xuất bộ nhớ hệ thống trong trường hợp ngoại lệ trong máy khác [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="590d4-105">The [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client can record diagnostics logs, system and application state details, and application memory dumps in the event of an exception in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.</span></span>  
  
> [!NOTE]
> - <span data-ttu-id="590d4-106">Các tính năng báo cáo chẩn đoán lỗi được mô tả tại đây lần đầu được giới thiệu trong [!INCLUDE[pn_unified_service_desk_2_2dot2](../../includes/pn-unified-service-desk-2-2dot2.md)].</span><span class="sxs-lookup"><span data-stu-id="590d4-106">The error diagnostics reporting features described here were  first introduced in [!INCLUDE[pn_unified_service_desk_2_2dot2](../../includes/pn-unified-service-desk-2-2dot2.md)].</span></span>  
>   -   <span data-ttu-id="590d4-107">For more information about the error diagnostics reporting files that are mentioned here, see [Error diagnostics reporting](../../unified-service-desk/admin/configure-client-diagnostic-logging-unified-service-desk.md#exceptionlogging).</span><span class="sxs-lookup"><span data-stu-id="590d4-107">For more information about the error diagnostics reporting files that are mentioned here, see [Error diagnostics reporting](../../unified-service-desk/admin/configure-client-diagnostic-logging-unified-service-desk.md#exceptionlogging).</span></span>  
  
 
<a name="typesofexceptions"></a>   
## <a name="types-of-exceptions"></a><span data-ttu-id="590d4-108">Các loại ngoại lệ</span><span class="sxs-lookup"><span data-stu-id="590d4-108">Types of exceptions</span></span>  
 <span data-ttu-id="590d4-109">Các ngoại lệ có thể là nghiêm trọng hoặc không nghiêm trọng.</span><span class="sxs-lookup"><span data-stu-id="590d4-109">Exceptions can be either fatal or non-fatal.</span></span>  
  
### <a name="fatal-exceptions"></a><span data-ttu-id="590d4-110">Các ngoại lệ nghiêm trọng</span><span class="sxs-lookup"><span data-stu-id="590d4-110">Fatal exceptions</span></span>  
 <span data-ttu-id="590d4-111">Đây là những sự cố máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] không thể giải quyết hoặc bỏ qua và thường khiến ứng dụng thoát hoặc không phản hồi.</span><span class="sxs-lookup"><span data-stu-id="590d4-111">These are issues that cannot be resolved or ignored by the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client and typically cause the application to quit or become unresponsive.</span></span> <span data-ttu-id="590d4-112">Ví dụ về ngoại lệ nghiêm trọng được xử lý là trường hợp khi hệ thống hết bộ nhớ.</span><span class="sxs-lookup"><span data-stu-id="590d4-112">An example of a handled fatal exception is a case when the system runs out of memory.</span></span> <span data-ttu-id="590d4-113">Ví dụ về ngoại lệ nghiêm trọng không được xử lý là tràn ngăn xếp hệ điều hành.</span><span class="sxs-lookup"><span data-stu-id="590d4-113">An example of an unhandled fatal exception is an operating system stack overflow.</span></span> <span data-ttu-id="590d4-114">Khi ngoại lệ nghiêm trọng diễn ra, máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] phải khởi động lại để tiếp tục.</span><span class="sxs-lookup"><span data-stu-id="590d4-114">When a fatal exception occurs, the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client must restart to continue.</span></span>  
  
 <span data-ttu-id="590d4-115">![Unified Service Desk exception dialog](../../unified-service-desk/media/usd-exception-dialog.jpg "Unified Service Desk exception dialog")</span><span class="sxs-lookup"><span data-stu-id="590d4-115">![Unified Service Desk exception dialog](../../unified-service-desk/media/usd-exception-dialog.jpg "Unified Service Desk exception dialog")</span></span>  
  
 <span data-ttu-id="590d4-116">Việc bấm vào **Có** trên hộp hội thoại lỗi sẽ bắt đầu tập hợp các tệp báo cáo chẩn đoán lỗi và khởi động lại máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="590d4-116">Clicking **Yes** on the error dialog box begins the collection of the error diagnostics reporting files and restarts the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.</span></span> <span data-ttu-id="590d4-117">Clicking **No** begins the collection of the error diagnostics reporting files but does not restart the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.</span><span class="sxs-lookup"><span data-stu-id="590d4-117">Clicking **No** begins the collection of the error diagnostics reporting files but does not restart the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.</span></span>  
  
 <span data-ttu-id="590d4-118">Tiếp theo, hộp thoại này sẽ xuất hiện trong vài giây để bạn có thể bấm vào **Hủy** nếu không muốn tệp tràn bộ nhớ được tạo.</span><span class="sxs-lookup"><span data-stu-id="590d4-118">Next, this dialog box  appears for a few seconds so that you can click **Cancel** if you don’t want a memory dump file created.</span></span> <span data-ttu-id="590d4-119">Nếu không bấm vào Hủy, một tệp tràn bộ nhớ đầy đủ của quá trình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sẽ được tạo.</span><span class="sxs-lookup"><span data-stu-id="590d4-119">If Cancel is not clicked, a full memory dump file of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] process is created.</span></span>  
  
 <span data-ttu-id="590d4-120">![Unified Service Desk dump file collection](../../unified-service-desk/media/usd-dump-file-collection.jpg "Unified Service Desk dump file collection")</span><span class="sxs-lookup"><span data-stu-id="590d4-120">![Unified Service Desk dump file collection](../../unified-service-desk/media/usd-dump-file-collection.jpg "Unified Service Desk dump file collection")</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="590d4-121">Các tệp tràn bộ nhớ lớn và yêu cầu số lượng lớn tài nguyên bộ xử lý và RAM trên máy tính để hoàn tất.</span><span class="sxs-lookup"><span data-stu-id="590d4-121">Memory dump files are large and require a significant amount of processor and RAM computer resources  to complete.</span></span>  
  
### <a name="non-fatal-exceptions"></a><span data-ttu-id="590d4-122">Các ngoại lệ không nghiêm trọng</span><span class="sxs-lookup"><span data-stu-id="590d4-122">Non-fatal exceptions</span></span>  
 <span data-ttu-id="590d4-123">Đây là những sự cố được máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] xử lý và thường không gây mất ổn định đối với ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="590d4-123">These are issues that are handled by the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client and typically don’t destabilize the application.</span></span> <span data-ttu-id="590d4-124">Ví dụ về ngoại lệ không nghiêm trọng là khi kiểm soát tổ chức đưa ra yêu cầu không hợp lệ, chẳng hạn như chia cho 0.</span><span class="sxs-lookup"><span data-stu-id="590d4-124">An example of a non-fatal exception is when a hosted control makes an invalid request, such as divide by zero.</span></span> <span data-ttu-id="590d4-125">Khi ngoại lệ không nghiêm trọng diễn ra, thường thì máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] có thể tiếp tục chạy.</span><span class="sxs-lookup"><span data-stu-id="590d4-125">When a non-fatal exception occurs, often the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client can continue running.</span></span> <span data-ttu-id="590d4-126">Bấm vào **Có** trên hộp thoại để thu thập nhật ký thoát báo cáo chẩn đoán lỗi (các tệp tràn bộ nhớ không được thu thập) và khởi động lại máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="590d4-126">Click **Yes** on the dialog box to collect error diagnostics reporting exit logs (memory dump files are not collected) and restart the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.</span></span> <span data-ttu-id="590d4-127">Click **No** to continue working in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client without collecting any error diagnostics reporting files.</span><span class="sxs-lookup"><span data-stu-id="590d4-127">Click **No** to continue working in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client without collecting any error diagnostics reporting files.</span></span>  
  
 <span data-ttu-id="590d4-128">![Unified Service Desk non-fatal exception dialog](../../unified-service-desk/media/usd-nonfatal-exception.jpg "Unified Service Desk non-fatal exception dialog")</span><span class="sxs-lookup"><span data-stu-id="590d4-128">![Unified Service Desk non-fatal exception dialog](../../unified-service-desk/media/usd-nonfatal-exception.jpg "Unified Service Desk non-fatal exception dialog")</span></span>  
  
<a name="ondemandDump"></a>   
## <a name="create-a-memory-dump-on-demand"></a><span data-ttu-id="590d4-129">Tạo tràn bộ nhớ theo yêu cầu</span><span class="sxs-lookup"><span data-stu-id="590d4-129">Create a memory dump on-demand</span></span>  
 <span data-ttu-id="590d4-130">Bất kỳ lúc nào, các tác nhân đang chạy [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] có thể thu hồi tràn bộ nhớ đầy đủ theo yêu cầu của ứng dụng máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="590d4-130">At any time agents running [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] can invoke an on-demand full memory dump of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application.</span></span> <span data-ttu-id="590d4-131">Theo mặc định, tổ hợp phím tắt để thu hồi việc tạo thủ công tệp tràn là CTRL+ALT+a.</span><span class="sxs-lookup"><span data-stu-id="590d4-131">By default, the shortcut key combination to invoke the manual creation of a  dump file is CTRL+ALT+a.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="590d4-132">Memory dump files are large and require a significant amount of processor and RAM computer resources  to complete.</span><span class="sxs-lookup"><span data-stu-id="590d4-132">Memory dump files are large and require a significant amount of processor and RAM computer resources  to complete.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="590d4-133">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="590d4-133">See also</span></span>  
 [<span data-ttu-id="590d4-134">Manage Options for Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="590d4-134">Manage Options for Unified Service Desk</span></span>](../../unified-service-desk/admin/manage-options-unified-service-desk.md)
