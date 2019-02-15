---
title: Create a user-defined event | MicrosoftDocs
description: Unified Service Desk provides you with predefined events for hosted controls based on the type of the hosted control. Apart from these predefined events, you can also create your own events in Unified Service Desk, which are called user-defined events. You can use the FireEvent action or the event moniker to run user-defined events.
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
ms.assetid: d9bc82cb-4d6c-4f3b-9aa5-2bb757de116b
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
ms.openlocfilehash: 947ddeaa1a6724dd91f24532e8e9c31d808f5ec9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386784"
---
# <a name="create-a-user-defined-event"></a><span data-ttu-id="ed1bf-105">Create a user-defined event</span><span class="sxs-lookup"><span data-stu-id="ed1bf-105">Create a user-defined event</span></span>
[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]<span data-ttu-id="ed1bf-106">cung cấp cho bạn sự kiện được xác định trước cho kiểm soát tổ chức dựa trên loại kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="ed1bf-106">provides you with predefined events for hosted controls based on the type of the hosted control.</span></span> <span data-ttu-id="ed1bf-107">Ngoài những sự kiện được xác định trước này, bạn cũng có thể tạo sự kiện của riêng bạn trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], mà được gọi là sự kiện do người dùng xác định.</span><span class="sxs-lookup"><span data-stu-id="ed1bf-107">Apart from these predefined events, you can also create your own events in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], which are called user-defined events.</span></span> <span data-ttu-id="ed1bf-108">You can use the **FireEvent** action or the event moniker to run user-defined events.</span><span class="sxs-lookup"><span data-stu-id="ed1bf-108">You can use the **FireEvent** action or the event moniker to run user-defined events.</span></span>  

<a name="FireEvent"></a>   
## <a name="use-the-fireevent-action"></a><span data-ttu-id="ed1bf-109">Use the FireEvent action</span><span class="sxs-lookup"><span data-stu-id="ed1bf-109">Use the FireEvent action</span></span>  
 <span data-ttu-id="ed1bf-110">Tất cả loại kiểm soát tổ chức [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] được xác định trước và tùy chỉnh, ngoại trừ **Ứng dụng tổ chức CCA** có một hành động UII đặc biệt được gọi là **FireEvent**.</span><span class="sxs-lookup"><span data-stu-id="ed1bf-110">All of the predefined and custom [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] hosted control types, except for the **CCA Hosted Application** have a special UII action called **FireEvent**.</span></span> <span data-ttu-id="ed1bf-111">Bạn có thể gọi hành động này để bắt đầu một sự kiện do người dùng xác định từ kiểm soát đó.</span><span class="sxs-lookup"><span data-stu-id="ed1bf-111">You can call this action to initiate a user-defined event from that control.</span></span> <span data-ttu-id="ed1bf-112">Đây là một cách thuận tiện để nhóm nhiều cuộc gọi hành động thành một cuộc gọi duy nhất, tạo hàm trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] có hiệu quả.</span><span class="sxs-lookup"><span data-stu-id="ed1bf-112">This is a convenient way to group multiple action calls into a single call, effectively creating a function within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="ed1bf-113">Nó cũng là một cách hợp lý để kiểm tra sự kiện và trình tự hành động trước khi triển khai.</span><span class="sxs-lookup"><span data-stu-id="ed1bf-113">It is also a reasonable way to test events and their action sequences before deployment.</span></span>  

 <span data-ttu-id="ed1bf-114">Các tham số đầu tiên vào **FireEvent** là tên của sự kiện này:</span><span class="sxs-lookup"><span data-stu-id="ed1bf-114">The first parameter to the **FireEvent** is the name of the event:</span></span>  

```  
name=MyEvent  
```  

 <span data-ttu-id="ed1bf-115">Tất cả các cặp tên/giá trị tiếp theo trở thành các tham số cho sự kiện này và do đó có thể được sử dụng như thay thế thông số trong các hành động được gọi như kết quả.</span><span class="sxs-lookup"><span data-stu-id="ed1bf-115">All subsequent name/value pairs become the parameters to the event and thus can be used as replacement parameters within the actions that are called as a result.</span></span> <span data-ttu-id="ed1bf-116">Ví dụ, nếu bạn vượt qua danh sách tham số sau đây:</span><span class="sxs-lookup"><span data-stu-id="ed1bf-116">For example, if you pass the following parameter list:</span></span>  

```  
name=MyEvent  
var1=[[account.name]]  
```  

 <span data-ttu-id="ed1bf-117">This will fire the custom event **MyEvent** event enabling the ability to create an action call that uses the `var1` parameter as follows:</span><span class="sxs-lookup"><span data-stu-id="ed1bf-117">This will fire the custom event **MyEvent** event enabling the ability to create an action call that uses the `var1` parameter as follows:</span></span>  

```  
Hosted Control=Some Hosted Control  
UII Action=Some action on the Hosted Control  
Data=[[var1]]  
```  

 <span data-ttu-id="ed1bf-118">Điều này đi qua tham số sự kiện như là một tham số dữ liệu cho hành động của kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="ed1bf-118">This passes the event parameter as a data parameter to the hosted control action.</span></span> <span data-ttu-id="ed1bf-119">Trong ví dụ này, đó có nghĩa là các tham số dữ liệu cho kiểm soát tổ chức sẽ là già trí tên tài khoản từ phiên.</span><span class="sxs-lookup"><span data-stu-id="ed1bf-119">In this example, that means the data parameter to the hosted control will be the account.name value from the session.</span></span>  

<a name="EventMoniker"></a>   
## <a name="use-the-event-moniker"></a><span data-ttu-id="ed1bf-120">Use the event moniker</span><span class="sxs-lookup"><span data-stu-id="ed1bf-120">Use the event moniker</span></span>  
 <span data-ttu-id="ed1bf-121">You can create a custom event on a hosted control, and then call it using the following event moniker syntax:</span><span class="sxs-lookup"><span data-stu-id="ed1bf-121">You can create a custom event on a hosted control, and then call it using the following event moniker syntax:</span></span>  

```  
http://event/?EventName=<EVENT_NAME>&key=value&key=value&…  
```  

 <span data-ttu-id="ed1bf-122">In the syntax, you specify the `key=value` pair to pass parameter list to be used when the event is triggered.</span><span class="sxs-lookup"><span data-stu-id="ed1bf-122">In the syntax, you specify the `key=value` pair to pass parameter list to be used when the event is triggered.</span></span>  

 <span data-ttu-id="ed1bf-123">Consider an example where you want to raise a user-defined event whenever the title of the case on the case form changes in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="ed1bf-123">Consider an example where you want to raise a user-defined event whenever the title of the case on the case form changes in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span></span> <span data-ttu-id="ed1bf-124">To do this:</span><span class="sxs-lookup"><span data-stu-id="ed1bf-124">To do this:</span></span>  

1. <span data-ttu-id="ed1bf-125">Create a new event, called `TitleChanged`, for the **Incident** hosted control in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="ed1bf-125">Create a new event, called `TitleChanged`, for the **Incident** hosted control in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. <span data-ttu-id="ed1bf-126">Create an action call, called `Action Call for Title Change`, with the following values:</span><span class="sxs-lookup"><span data-stu-id="ed1bf-126">Create an action call, called `Action Call for Title Change`, with the following values:</span></span>  


   |     <span data-ttu-id="ed1bf-127">Trường</span><span class="sxs-lookup"><span data-stu-id="ed1bf-127">Field</span></span>      |                                                                                                                         <span data-ttu-id="ed1bf-128">Value</span><span class="sxs-lookup"><span data-stu-id="ed1bf-128">Value</span></span>                                                                                                                         |
   |----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |      <span data-ttu-id="ed1bf-129">Tên</span><span class="sxs-lookup"><span data-stu-id="ed1bf-129">Name</span></span>      |                                                                                                             <span data-ttu-id="ed1bf-130">Action Call for Title Change</span><span class="sxs-lookup"><span data-stu-id="ed1bf-130">Action Call for Title Change</span></span>                                                                                                              |
   | <span data-ttu-id="ed1bf-131">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="ed1bf-131">Hosted Control</span></span> |                                                                                                                       <span data-ttu-id="ed1bf-132">Sự cố</span><span class="sxs-lookup"><span data-stu-id="ed1bf-132">Incident</span></span>                                                                                                                        |
   |     <span data-ttu-id="ed1bf-133">Hành động</span><span class="sxs-lookup"><span data-stu-id="ed1bf-133">Action</span></span>     |                                                                                                                     <span data-ttu-id="ed1bf-134">Chạy lệnh Xrm</span><span class="sxs-lookup"><span data-stu-id="ed1bf-134">RunXrmCommand</span></span>                                                                                                                     |
   |      <span data-ttu-id="ed1bf-135">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="ed1bf-135">Data</span></span>      | <span data-ttu-id="ed1bf-136">function titleChangeReaction()  {</span><span class="sxs-lookup"><span data-stu-id="ed1bf-136">function titleChangeReaction()  {</span></span><br /> <span data-ttu-id="ed1bf-137">window.open("<http://event/?EventName=TitleChanged&NewTitle="+encodeURIComponent(Xrm.Page.getAttribute("title").getValue(>)));</span><span class="sxs-lookup"><span data-stu-id="ed1bf-137">window.open("<http://event/?EventName=TitleChanged&NewTitle="+encodeURIComponent(Xrm.Page.getAttribute("title").getValue(>)));</span></span><br /> <span data-ttu-id="ed1bf-138">}</span><span class="sxs-lookup"><span data-stu-id="ed1bf-138">}</span></span><br /> <span data-ttu-id="ed1bf-139">Xrm.Page.getAttribute("title").addOnChange(titleChangeReaction);</span><span class="sxs-lookup"><span data-stu-id="ed1bf-139">Xrm.Page.getAttribute("title").addOnChange(titleChangeReaction);</span></span> |


3. <span data-ttu-id="ed1bf-140">Add the new action call that you created to the **BrowserDocumentComplete** event of the **Incident** hosted control.</span><span class="sxs-lookup"><span data-stu-id="ed1bf-140">Add the new action call that you created to the **BrowserDocumentComplete** event of the **Incident** hosted control.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="ed1bf-141">[Add action calls to an event](../unified-service-desk/add-action-calls-event.md)</span><span class="sxs-lookup"><span data-stu-id="ed1bf-141">[Add action calls to an event](../unified-service-desk/add-action-calls-event.md)</span></span>  

    <span data-ttu-id="ed1bf-142">When the `TitleChanged` event is triggered, the following request is raised: `http://event/?EventName=TitleChanged&NewTitle=<NEW_TITLE>`</span><span class="sxs-lookup"><span data-stu-id="ed1bf-142">When the `TitleChanged` event is triggered, the following request is raised: `http://event/?EventName=TitleChanged&NewTitle=<NEW_TITLE>`</span></span>  

    <span data-ttu-id="ed1bf-143">This will cause the `TitleChanged` event to be triggered with the following data parameter: `NewTitle=<NEW_TITLE>`</span><span class="sxs-lookup"><span data-stu-id="ed1bf-143">This will cause the `TitleChanged` event to be triggered with the following data parameter: `NewTitle=<NEW_TITLE>`</span></span>  

   <span data-ttu-id="ed1bf-144">If you use [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps to invoke an event in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the event moniker (`http://event/?EventName=<EVENT_NAME>&key=value&key=value&…`), you can use the `window.IsUSD` property to determine whether the [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] code is running under [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] when the event is invoked.</span><span class="sxs-lookup"><span data-stu-id="ed1bf-144">If you use [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps to invoke an event in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the event moniker (`http://event/?EventName=<EVENT_NAME>&key=value&key=value&…`), you can use the `window.IsUSD` property to determine whether the [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] code is running under [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] when the event is invoked.</span></span> <span data-ttu-id="ed1bf-145">The following code sample can be included in your [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] code to ensure that the event is invoked only when the calling [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] is running within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="ed1bf-145">The following code sample can be included in your [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] code to ensure that the event is invoked only when the calling [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] is running within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  

```  
if ((window.IsUSD != null) && (window.IsUSD == true))  
{  
   window.open(http://event/?EventName=<EVENT_NAME>&key=value&key=value&…);  
}  
```  

### <a name="see-also"></a><span data-ttu-id="ed1bf-146">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ed1bf-146">See also</span></span>  
 <span data-ttu-id="ed1bf-147">[Sự kiện](../unified-service-desk/events.md) </span><span class="sxs-lookup"><span data-stu-id="ed1bf-147">[Events](../unified-service-desk/events.md) </span></span>  
 <span data-ttu-id="ed1bf-148">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md) </span><span class="sxs-lookup"><span data-stu-id="ed1bf-148">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md) </span></span>  
 <span data-ttu-id="ed1bf-149">[Manage hosted controls, actions, and events](../unified-service-desk/manage-hosted-controls-actions-events.md) </span><span class="sxs-lookup"><span data-stu-id="ed1bf-149">[Manage hosted controls, actions, and events](../unified-service-desk/manage-hosted-controls-actions-events.md) </span></span>  
 [<span data-ttu-id="ed1bf-150">MSDN: Use JavaScript with Microsoft Dynamics CRM</span><span class="sxs-lookup"><span data-stu-id="ed1bf-150">MSDN: Use JavaScript with Microsoft Dynamics CRM</span></span>](https://msdn.microsoft.com/library/hh771584.aspx)
