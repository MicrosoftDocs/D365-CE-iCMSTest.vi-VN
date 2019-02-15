---
title: Add a UII action to a hosted control | MicrosoftDocs
description: Learn about adding User Interface Integration (UII) actions to a hosted control type to provide new functionality.
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
ms.assetid: 0e082c56-76b8-405e-98ae-1d33802a19d0
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
ms.openlocfilehash: 9b36280b998feee417cae704d1738eb37a51b6ec
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386936"
---
# <a name="add-a-uii-action-to-a-hosted-control"></a><span data-ttu-id="727df-103">Add a UII action to a hosted control</span><span class="sxs-lookup"><span data-stu-id="727df-103">Add a UII action to a hosted control</span></span>
<span data-ttu-id="727df-104">Khi phiên bản mới của [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] được phát triển, các hành động [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] mới có thể được thêm vào loại kiểm soát tổ chức để cung cấp chức năng mới.</span><span class="sxs-lookup"><span data-stu-id="727df-104">As new versions of [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] are developed, new [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] actions might get added to a hosted control type to provide new functionality.</span></span> <span data-ttu-id="727df-105">Tuy nhiên, các hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] mới cho loại tổ chức kiểm soát sẽ chỉ khả dụng ngay mà không cần kích hoạt cho các phiên bản mới của loại kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="727df-105">However, the new [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions for a hosted control type will only be available out-of-box for the new instances of the hosted control type.</span></span> <span data-ttu-id="727df-106">Nếu bạn có các phiên bản hiện có của loại kiểm soát được lưu trữ trong cấu hình của bạn, hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] mới sẽ không khả dụng theo mặc định.</span><span class="sxs-lookup"><span data-stu-id="727df-106">If you have existing instances of a hosted control type in your configuration, the new [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions won’t become available by default.</span></span> <span data-ttu-id="727df-107">Bạn sẽ phải thêm hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] theo cách thủ công vào hồ sơ kiểm soát tổ chức (phiên bản) để có thể sử dụng hành động trong cuộc gọi hành động của bạn.</span><span class="sxs-lookup"><span data-stu-id="727df-107">You will have to manually add the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] action to the hosted control record (instance) to be able to use the action in your action calls.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="727df-108">Bạn phải thêm theo cách thủ công hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] vào phiên bản kiểm soát tổ chức chỉ khi hành động đó được hỗ trợ cho loại phiên bản kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="727df-108">You must manually add the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] action to a hosted control instance only if it is supported for the type of hosted control instance.</span></span> <span data-ttu-id="727df-109">Nếu không, hành động sẽ không hoạt động cho phiên bản kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="727df-109">Otherwise, the action won’t work for the hosted control instance.</span></span>  
  
 <span data-ttu-id="727df-110">Để thêm một hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] vào phiên bản kiểm soát tổ chức hiện có:</span><span class="sxs-lookup"><span data-stu-id="727df-110">To add a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] action to an existing hosted control instance:</span></span>  
  
1. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
2. <span data-ttu-id="727df-111">Bấm **Kiểm soát Tổ chức**.</span><span class="sxs-lookup"><span data-stu-id="727df-111">Click **Hosted Controls**.</span></span>  
  
3. <span data-ttu-id="727df-112">Tìm kiếm hồ sơ kiểm soát tổ chức mà bạn muốn thêm hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] vào đó, sau đó bấm vào tên kiểm soát tổ chức để mở định nghĩa.</span><span class="sxs-lookup"><span data-stu-id="727df-112">Search for the hosted control record that you want to add a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] action to, and then click the hosted control name to open its definition.</span></span>  
  
4. <span data-ttu-id="727df-113">Trên trang định nghĩa kiểm soát tổ chức, bấm vào mũi tên bên cạnh tên kiểm soát tổ chức, rồi bấm vào **Hành động UII**.</span><span class="sxs-lookup"><span data-stu-id="727df-113">On the hosted control definition page, click the arrow next to the hosted control name, and then click **UII Actions**.</span></span>  
  
5. <span data-ttu-id="727df-114">Bấm vào **Thêm Hoạt động UII mới**.</span><span class="sxs-lookup"><span data-stu-id="727df-114">Click **Add New UII Action**.</span></span>  
  
6. <span data-ttu-id="727df-115">Trên trang **Hành động UII Mới**, chỉ định tên của hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] trong trường **Tên** rồi bấm vào **Lưu và Đóng**.</span><span class="sxs-lookup"><span data-stu-id="727df-115">On the **New UII Action** page, specify the name of the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] action in the **Name** field, and then click **Save and Close**.</span></span> <span data-ttu-id="727df-116">Bạn không phải chỉ định bất kỳ giá trị nào khác trên trang này.</span><span class="sxs-lookup"><span data-stu-id="727df-116">You don’t have to specify any other value on this page.</span></span>  
  
   <span data-ttu-id="727df-117">![Add a UII action to a hosted control](../unified-service-desk/media/usd-new-uii-action-hc.png "Add a UII action to a hosted control")</span><span class="sxs-lookup"><span data-stu-id="727df-117">![Add a UII action to a hosted control](../unified-service-desk/media/usd-new-uii-action-hc.png "Add a UII action to a hosted control")</span></span>  
  
    <span data-ttu-id="727df-118">Hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] mới được thêm vào phiên bản kiểm soát tổ chức và có thể được sử dụng trong các cuộc gọi hành động của bạn.</span><span class="sxs-lookup"><span data-stu-id="727df-118">The new [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] action gets added to the hosted control instance, and can be used in your action calls.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="727df-119">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="727df-119">See also</span></span>  
 <span data-ttu-id="727df-120">[Create an action call for a UII action](../unified-service-desk/create-action-call-uii-action.md) </span><span class="sxs-lookup"><span data-stu-id="727df-120">[Create an action call for a UII action](../unified-service-desk/create-action-call-uii-action.md) </span></span>  
 [<span data-ttu-id="727df-121">Manage hosted controls, actions, and events</span><span class="sxs-lookup"><span data-stu-id="727df-121">Manage hosted controls, actions, and events</span></span>](../unified-service-desk/manage-hosted-controls-actions-events.md)
