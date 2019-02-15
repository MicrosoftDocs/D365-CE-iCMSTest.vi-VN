---
title: Action calls | MicrosoftDocs
description: Learn about actions that represents a call to a UII action associated with a hosted control. Action calls are used to pass parameters required to execute the underlying UII action in Unified Service Desk.
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
ms.assetid: 1f5a1817-28c8-4171-a83b-6941a57a5a6b
caps.latest.revision: 7
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 7f204b88552ae3aead0ede5ffbfac549d2ed97ce
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387699"
---
# <a name="action-calls"></a><span data-ttu-id="bd222-104">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="bd222-104">Action calls</span></span>
<span data-ttu-id="bd222-105">Một cuộc gọi hành động đại diện cho một cuộc gọi đến một hành động UII được liên kết với kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="bd222-105">An action call represents a call to a UII action associated with a hosted control.</span></span> <span data-ttu-id="bd222-106">Cuộc gọi hành động được sử dụng để vượt qua các tham số cần thiết để thực hiện các hành động UII cơ bản trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="bd222-106">Action calls are used to pass parameters required to execute the underlying UII action in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
 <span data-ttu-id="bd222-107">Một cuộc gọi hành động có thể được gắn liền với những điều sau trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] vì vậy chúng được thực hiện khi:</span><span class="sxs-lookup"><span data-stu-id="bd222-107">An action call can be attached to the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] so that they are executed when:</span></span>  
  
- <span data-ttu-id="bd222-108">Phát sinh một sự kiện.</span><span class="sxs-lookup"><span data-stu-id="bd222-108">An event is raised.</span></span>  
  
- <span data-ttu-id="bd222-109">Nguyên tắc điều hướng cửa đã được xử lý.</span><span class="sxs-lookup"><span data-stu-id="bd222-109">A window navigation rule is processed.</span></span>  
  
- <span data-ttu-id="bd222-110">Nút thanh công cụ được nhấp.</span><span class="sxs-lookup"><span data-stu-id="bd222-110">A toolbar button is clicked.</span></span>  
  
- <span data-ttu-id="bd222-111">Mã lệnh tổng đài viên đang chạy hoặc câu trả lời được nhấp vào.</span><span class="sxs-lookup"><span data-stu-id="bd222-111">An agent script is run or an answer is clicked.</span></span>  
  
  <span data-ttu-id="bd222-112">The action calls, and the sequence in which they are called, define the behavior of the configured system.</span><span class="sxs-lookup"><span data-stu-id="bd222-112">The action calls, and the sequence in which they are called, define the behavior of the configured system.</span></span> <span data-ttu-id="bd222-113">Hành động cuộc gọi có thể được dùng như cuộc gọi chức năng riêng của nó, nơi các hành động UII là định nghĩa hoặc chữ ký chức năng.</span><span class="sxs-lookup"><span data-stu-id="bd222-113">Action calls can be thought of as the function call itself, where the UII action is the function signature or definition.</span></span>  
  
  <span data-ttu-id="bd222-114">You can also attach action calls to another action call to execute the attached action calls when the parent action call is executed.</span><span class="sxs-lookup"><span data-stu-id="bd222-114">You can also attach action calls to another action call to execute the attached action calls when the parent action call is executed.</span></span> <span data-ttu-id="bd222-115">The action calls attached to an action call are called the sub-action calls.</span><span class="sxs-lookup"><span data-stu-id="bd222-115">The action calls attached to an action call are called the sub-action calls.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="bd222-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="bd222-116">See also</span></span>  
 <span data-ttu-id="bd222-117">[Create an action call for a UII action](../unified-service-desk/create-action-call-uii-action.md) </span><span class="sxs-lookup"><span data-stu-id="bd222-117">[Create an action call for a UII action](../unified-service-desk/create-action-call-uii-action.md) </span></span>  
 <span data-ttu-id="bd222-118">[Add action calls to an event](../unified-service-desk/add-action-calls-event.md) </span><span class="sxs-lookup"><span data-stu-id="bd222-118">[Add action calls to an event](../unified-service-desk/add-action-calls-event.md) </span></span>  
 <span data-ttu-id="bd222-119">[Hành động UII](../unified-service-desk/uii-actions.md) </span><span class="sxs-lookup"><span data-stu-id="bd222-119">[UII actions](../unified-service-desk/uii-actions.md) </span></span>  
 [<span data-ttu-id="bd222-120">Manage hosted controls, actions, and events</span><span class="sxs-lookup"><span data-stu-id="bd222-120">Manage hosted controls, actions, and events</span></span>](../unified-service-desk/manage-hosted-controls-actions-events.md)
