---
title: Search data using entity searches in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Entity searches are FetchXML definitions that query the Dynamics 365 for Customer Engagement web services to return data. Bạn cũng có thể sử dụng tham số thay thế trong truy vấn FetchXML trong một tìm kiếm thực thể.
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
ms.assetid: d003e22b-75a7-4491-9660-14529fa581bd
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
ms.openlocfilehash: ab767df26913315db75b68d447ad46171a20f593
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385861"
---
# <a name="search-data-using-entity-searches-in-unified-service-desk"></a><span data-ttu-id="087c5-104">Search data using entity searches in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="087c5-104">Search data using entity searches in Unified Service Desk</span></span>
<span data-ttu-id="087c5-105">Tìm kiếm thực thể là định nghĩa FetchXML truy vấn dịch vụ web [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] để trả về dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="087c5-105">Entity searches are FetchXML definitions that query the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] web services to return data.</span></span> <span data-ttu-id="087c5-106">Bạn cũng có thể sử dụng tham số thay thế trong truy vấn FetchXML trong một tìm kiếm thực thể.</span><span class="sxs-lookup"><span data-stu-id="087c5-106">You can also use replacement parameters within the FetchXML queries in an entity search.</span></span> <span data-ttu-id="087c5-107">Entity searches can be used in window navigation rules both as a source to access data which is not displayed on the form, and as a destination to look up the data using a web service call to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps, and then populate the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] context data so that it can be used in replacement parameters.</span><span class="sxs-lookup"><span data-stu-id="087c5-107">Entity searches can be used in window navigation rules both as a source to access data which is not displayed on the form, and as a destination to look up the data using a web service call to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps, and then populate the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] context data so that it can be used in replacement parameters.</span></span> <span data-ttu-id="087c5-108">You can also use entity searches in the [DoSearch](../unified-service-desk/global-manager-hosted-control.md#DoSearch) action for the Global Manager hosted control to search for your data.</span><span class="sxs-lookup"><span data-stu-id="087c5-108">You can also use entity searches in the [DoSearch](../unified-service-desk/global-manager-hosted-control.md#DoSearch) action for the Global Manager hosted control to search for your data.</span></span>  
  
 <span data-ttu-id="087c5-109">You define an entity search in the **Entity Searches** area (**Settings** > **Unified Service Desk** > **Entity Searches**) in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="087c5-109">You define an entity search in the **Entity Searches** area (**Settings** > **Unified Service Desk** > **Entity Searches**) in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span></span> <span data-ttu-id="087c5-110">Để xác định tìm kiếm thực thể, bạn cần phải chỉ định ba điều: tên, thực thể áp dụng tìm kiếm và truy vấn FetchXML đại diện cho các truy vấn để lấy dữ liệu từ máy chủ.</span><span class="sxs-lookup"><span data-stu-id="087c5-110">To define an entity search, you need to specify three things: a name, the entity that the search applies to, and the FetchXML query that represents the query to retrieve data from the server.</span></span>  
  
 <span data-ttu-id="087c5-111">Truy vấn FetchXML sau đây trả về chi tiết tên và địa chỉ của tài khoản dựa trên ID khách hàng có sẵn từ một trường hợp:</span><span class="sxs-lookup"><span data-stu-id="087c5-111">The following FetchXML query returns name and address details of an account based on a customer ID available from a case:</span></span>  
  
```  
<fetch version="1.0" output-format="xml-platform" mapping="logical" distinct="false">  
  <entity name="account">  
    <attribute name="name" />  
    <attribute name="emailaddress1" />  
    <attribute name="telephone1" />     
    <attribute name="address1_line1" />  
    <attribute name="address1_city" />  
    <attribute name="address1_stateorprovince" />  
    <attribute name="address1_postalcode" />  
   <attribute name="address1_country" />  
   <attribute name="msdyusd_facebook"/>  
   <attribute name="msdyusd_twitter"/>  
    <order attribute="name" descending="false" />  
    <filter type="and">  
      <condition attribute="accountid" operator="eq" value="{[[incident.customerid.Id]x]}" />  
    </filter>  
  </entity>  
</fetch>  
```  
  
 <span data-ttu-id="087c5-112">Đây là cách thể hiện định nghĩa tìm kiếm thực thể:</span><span class="sxs-lookup"><span data-stu-id="087c5-112">This is how the entity search definition looks like:</span></span>  
  
 <span data-ttu-id="087c5-113">![Sample entity search definition](../unified-service-desk/media/usd-entity-search-definition.png "Sample entity search definition")</span><span class="sxs-lookup"><span data-stu-id="087c5-113">![Sample entity search definition](../unified-service-desk/media/usd-entity-search-definition.png "Sample entity search definition")</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="087c5-114">Trong khi xác định truy vấn FetchXML trong tìm kiếm thực thể, bạn chỉ nên trả về các trường được yêu cầu cho mục đích.</span><span class="sxs-lookup"><span data-stu-id="087c5-114">While defining FetchXML queries in an entity search, you should only return the fields that are required for the purpose.</span></span> <span data-ttu-id="087c5-115">Điều này giảm thiểu tác động trên mạng bằng cách hạn chế kích thước của các yêu cầu và các dữ liệu được trả về, do đó tối ưu hóa việc sử dụng tài nguyên.</span><span class="sxs-lookup"><span data-stu-id="087c5-115">This minimizes the impact on the network by limiting the size of the request and the data being returned, thus optimizing the resource usage.</span></span>  
  
 <span data-ttu-id="087c5-116">Developers can also reuse an existing entity search definition in their code to search for records in Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="087c5-116">Developers can also reuse an existing entity search definition in their code to search for records in Dynamics 365 for Customer Engagement apps.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="087c5-117">[Reuse Entity Search definition in your custom code](../unified-service-desk/reuse-entity-search-definition-custom-code.md)</span><span class="sxs-lookup"><span data-stu-id="087c5-117">[Reuse Entity Search definition in your custom code](../unified-service-desk/reuse-entity-search-definition-custom-code.md)</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="087c5-118">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="087c5-118">See also</span></span>  
 <span data-ttu-id="087c5-119">[Reuse Entity Search definition in your custom code](../unified-service-desk/reuse-entity-search-definition-custom-code.md) </span><span class="sxs-lookup"><span data-stu-id="087c5-119">[Reuse Entity Search definition in your custom code](../unified-service-desk/reuse-entity-search-definition-custom-code.md) </span></span>  
 <span data-ttu-id="087c5-120">[Use window navigation rules in Unified Service Desk](../unified-service-desk/use-window-navigation-rules-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="087c5-120">[Use window navigation rules in Unified Service Desk](../unified-service-desk/use-window-navigation-rules-unified-service-desk.md) </span></span>  
 <span data-ttu-id="087c5-121">[Cuộc gọi hành động](../unified-service-desk/action-calls.md) </span><span class="sxs-lookup"><span data-stu-id="087c5-121">[Action calls](../unified-service-desk/action-calls.md) </span></span>  
 <span data-ttu-id="087c5-122">[Learn to configure Unified Service Desk](../unified-service-desk/learn-to-use-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="087c5-122">[Learn to configure Unified Service Desk](../unified-service-desk/learn-to-use-unified-service-desk.md) </span></span>  
 [<span data-ttu-id="087c5-123">Cách: Sử dụng bộ chuyển đổi trình nghe chung để định tuyến sự kiện CTI</span><span class="sxs-lookup"><span data-stu-id="087c5-123">Walkthrough: Use the generic listener adapter for CTI event routing</span></span>](../unified-service-desk/walkthrough-use-the-generic-listener-adapter-for-cti-event-routing.md)
