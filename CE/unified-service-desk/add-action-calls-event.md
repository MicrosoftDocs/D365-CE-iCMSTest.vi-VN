---
title: Add action calls to an event | MicrosoftDocs
description: Learn about adding action calls to an event.
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
ms.assetid: 78b6080d-dfe4-43ee-a3b0-0653ce58bacd
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
ms.openlocfilehash: 16bc72825c4c0fd4b8b096afb538ac310b7eca49
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386279"
---
# <a name="add-action-calls-to-an-event"></a><span data-ttu-id="b5ed8-103">Add action calls to an event</span><span class="sxs-lookup"><span data-stu-id="b5ed8-103">Add action calls to an event</span></span>
<span data-ttu-id="b5ed8-104">Bạn có thể thêm nhiều cuộc gọi hành động cho một sự kiện, và cuộc gọi hành động sẽ được thực hiện theo thứ tự được xác định trong trường **Thứ tự** của định nghĩa sự kiện.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-104">You can add multiple action calls to an event, and the action calls will be executed in the order that is defined in the **Order** field of the event definition.</span></span> <span data-ttu-id="b5ed8-105">To do so:</span><span class="sxs-lookup"><span data-stu-id="b5ed8-105">To do so:</span></span>  
  
1. <span data-ttu-id="b5ed8-106">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-106">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="b5ed8-107">Bấm **Sự kiện**.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-107">Click **Events**.</span></span>  
  
4. <span data-ttu-id="b5ed8-108">Trên trang danh sách sự kiện, nhấp vào tên của sự kiện trong cột **tên**mà bạn muốn thêm cuộc gọi hành động.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-108">On the events list page, click the name of the event in the **Name** column that you want to add the action call to.</span></span> <span data-ttu-id="b5ed8-109">Thao tác này sẽ mở trang sự kiện.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-109">This opens the event page.</span></span>  
  
5. <span data-ttu-id="b5ed8-110">On the event page, under the **Active Actions** area, click **+** to add action calls.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-110">On the event page, under the **Active Actions** area, click **+** to add action calls.</span></span>  
  
   <span data-ttu-id="b5ed8-111">![Add action call to an event](../unified-service-desk/media/usd-add-action-call-event.png "Add action call to an event")</span><span class="sxs-lookup"><span data-stu-id="b5ed8-111">![Add action call to an event](../unified-service-desk/media/usd-add-action-call-event.png "Add action call to an event")</span></span>  
  
6. <span data-ttu-id="b5ed8-112">Một hộp tìm kiếm xuất hiện nơi bạn có thể tìm kiếm cuộc gọi hành động mà bạn muốn thêm vào sự kiện nếu bạn muốn tạo cuộc gọi hành động mới.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-112">A search box appears where you can search for the action call that you want to add to the event, if you want to create a new action call.</span></span> <span data-ttu-id="b5ed8-113">Sau khi bạn tìm kiếm và chọn cuộc gọi hành động cần thiết, nó xuất hiện dưới vùng **hoạt động hiện hoạt**.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-113">After you search and select the required action call, it appears under the **Active Actions** area.</span></span>  
  
7. <span data-ttu-id="b5ed8-114">Thực hiện bước 5 và 6 cho mỗi cuộc gọi hành động bạn muốn thêm.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-114">Perform steps 5 and 6 for each action call you want to add.</span></span>  
  
8. <span data-ttu-id="b5ed8-115">Nếu bạn có thêm nhiều cuộc gọi hành động, bấm đúp vào mỗi hồ sơ cuộc gọi hành động được thêm, xác định giá trị **Thứ tự** và sau đó lưu hồ sơ cuộc gọi hành động.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-115">If you have added multiple action calls, double-click on each of the added action call record, specify the **Order** value, and then save the action call record.</span></span> <span data-ttu-id="b5ed8-116">Giá trị thứ tự được Cập Nhật trong vùng **hoạt động hiện hoạt**.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-116">The order values are updated in the **Active Actions** area.</span></span>  
  
   <span data-ttu-id="b5ed8-117">![Action calls added to the event](../unified-service-desk/media/usd-event-action-list.png "Action calls added to the event")</span><span class="sxs-lookup"><span data-stu-id="b5ed8-117">![Action calls added to the event](../unified-service-desk/media/usd-event-action-list.png "Action calls added to the event")</span></span>  
  
9. <span data-ttu-id="b5ed8-118">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-118">Click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b5ed8-119">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b5ed8-119">See also</span></span>  
 <span data-ttu-id="b5ed8-120">[Cuộc gọi hành động](../unified-service-desk/action-calls.md) </span><span class="sxs-lookup"><span data-stu-id="b5ed8-120">[Action calls](../unified-service-desk/action-calls.md) </span></span>  
 <span data-ttu-id="b5ed8-121">[Sự kiện](../unified-service-desk/events.md) </span><span class="sxs-lookup"><span data-stu-id="b5ed8-121">[Events](../unified-service-desk/events.md) </span></span>  
 [<span data-ttu-id="b5ed8-122">Manage hosted controls, actions, and events</span><span class="sxs-lookup"><span data-stu-id="b5ed8-122">Manage hosted controls, actions, and events</span></span>](../unified-service-desk/manage-hosted-controls-actions-events.md)
