---
title: Configure Unified Service Desk to use Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn about the knowledge management solution in Microsoft Dynamics 365 for Customer Engagement apps that guides you through the process of creating and publishing rich knowledge articles with multimedia data like pictures and videos.
keywords: ''
ms.date: 08/17/2018
ms.service:
- dynamics-365-customerservice
ms.custom:
- dyn365-USD
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: c2e0f4b1-c09a-413c-b703-03ff851ffb9d
author: kabala123
ms.author: kabala
manager: shujoshi
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: d15878ee913d1827bfcf1c8b3ff321301d2c3100
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387900"
---
# <a name="configure-unified-service-desk-to-use-dynamics-365-for-customer-engagement-apps"></a>Configure Unified Service Desk to use Dynamics 365 for Customer Engagement apps
The **KM Control** and **Unified Interface KM Control** type of hosted controls expose a bunch of events and action calls to configure an integrated experience for your agents to easily search for knowledge base articles in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps from within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and then perform various actions on the search result items.  
  
::: moniker range="dynamics-usd-3"
 Tạo một phiên bản của loại kiểm soát tổ chức **Kiểm soát KM** để bắt đầu với cấu hình của bạn. Sau khi bạn đã tạo ra phiên bản kiểm soát tổ chức, bạn có thể đặt cấu hình các mục đề cập sau trong chủ đề này.  
::: moniker-end

::: moniker range=">=dynamics-usd-4"
 Create an instance of the **KM Control** or **Unified Interface KM Control** type of hosted control to begin with your configuration. After you have created an instance of the hosted control, you can configure things mentioned later in this topic.
 ::: moniker-end
  
<a name="Search"></a>   
## <a name="configure-knowledge-base-search-options"></a>Đặt cấu hình các tùy chọn tìm kiếm cơ sở kiến thức  
 Sử dụng hành động `Search` trên kiểm soát tổ chức để xác định cách bạn muốn thực hiện và hiển thị kết quả tìm kiếm. Ví dụ: bạn có thể chỉ định số lượng các kết quả để được trả lại, loại bài viết cơ sở kiến thức sẽ được hiển thị trong kết quả tìm kiếm hoặc tùy chọn sắp xếp cho kết quả tìm kiếm. Bạn cũng có thể sử dụng các tham số thay thế để xác định chuỗi truy vấn để tìm kiếm. For example, here is the data parameter for the `Search` action to configure an action call to automatically search knowledge bases based on the case (incident) title, display five results, and return only published knowledge bases from [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps or [!INCLUDE[pn_parature](../includes/pn-parature.md)] when your agent performs a search in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:  
  
```  
query=[[incident.title]+]  
results=5  
filter=3  
  
```  
  
 For information about the `Search` action and its parameters, see [Search](../unified-service-desk/km-control-hosted-control.md#Search). For information on how to define an action call for searching the knowledge base, see [Step 4: Configure an action call to automatically search knowledge base using the incident (case) title](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step4) in the walkthrough.  
  
<a name="SetContext"></a>   
## <a name="set-the-knowledge-base-article-context"></a>Đặt ngữ cảnh bài viết cơ sở kiến thức  
 The knowledge base article returned in the search result contains the metadata of the article, such as article name, private URL, public URL, and unique ID. Bạn có thể sử dụng thông tin này trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], thông qua các tham số thay thế, trong các kiểm soát tổ chức khác nơi hiển thị các bài viết để tự động đặt tên tab hoặc để cung cấp hành động theo ngữ cảnh (sao chép liên kết, liên kết hoặc hủy liên kết với (sự cố) bài viết) hiện tại cho bài viết cơ sở kiến thức hiện tại. To use the metadata information of an article, use the [SetArticleContext](../unified-service-desk/km-control-hosted-control.md#SetArticleContext) action to set the context of the article and pass it on to the hosted control where it will be used.  
  
 Additionally, you must include the `SetArticleContext` action in the `ResultOpen` event of the hosted control if you’re displaying a knowledge base article in another hosted control to be able to use the context information in the target hosted control. You must include the action in the `SelectionChange` event if you’ll be configuring contextual actions for a selected knowledge base article in the KM Control itself. Include it in both the events if you’ll be configuring both the functionalities in your agent application. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Predefined events](../unified-service-desk/km-control-hosted-control.md#events)  
  
 For information on how to define an action call for setting the article context and include it in an event, see [Step 5: Configure hosted controls and action calls to display an article in a tab](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step5) in the walkthrough.  
  
<a name="AssociateDisassociate"></a>   
## <a name="associate-and-disassociate-a-knowledge-base-article-with-a-case-incident"></a>Associate and disassociate a knowledge base article with a case (incident)  
 You can use the knowledge base article context to associate and disassociate a knowledge base article with a case record from within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Use the [Associate](../unified-service-desk/km-control-hosted-control.md#Associate) and [Disassociate](../unified-service-desk/km-control-hosted-control.md#Disassociate) actions to do so.  
  
 Cú pháp sau hiển thị tham số dữ liệu mà bạn có thể sử dụng với hành động `Associate` trên `KM Control` (nói `KB Search`) để liên kết bài viết với một bản ghi sự cố.  
  
```  
entitytypename=incident  
recordid =[[incident.Id]]  
articleuniqueid=[[KB Search.articleUId]]  
articletitle=[[KB Search.question]]  
articleprivateurl=[[KB Search.serviceDeskUri]]  
articlepublicurl=[[KB Search.publicUrl]]  
```  
  
> [!NOTE]
>  If you are using the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps knowledge base, the `articleprivateurl` parameter isn’t applicable, and therefore the respective replacement parameter (in this case, `[[KB Search.serviceDeskUri]]` will always be null. So, you should use `articleprivateurl=[[KB Search.serviceDeskUri]+]` instead of `articleprivateurl=[[KB Search.serviceDeskUri]]` to ensure that a null or non-existent key is replaced with a blank string, or use conditions if you plan to use both [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps and Parature knowledge. Also, the replacement parameter for `articlepubliceurl` (in this case `[[KB Search.publicUrl]]`) will contain data only if the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps knowledge article is already published to an external portal (**Use an external portal** option is selected in the **Knowledge Base management Settings** dialog box in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps).  
  
 Cú pháp sau hiển thị tham số dữ liệu mà bạn có thể sử dụng với hành động `Disassociate` trên `KM Control` (nói `KB Search`) để hủy liên kết một bài viết từ một bản ghi sự cố.  
  
```  
articleuniqueid=[[KB Search.articleUId]]  
relatedentityrecordid=[[incident.Id]]  
articletitle=[[KB Search.question]]  
entitytypename=incident  
```  
  
 For information on how to use the `Associate` action to associate an article with an incident record, see [Step 6: Configure contextual actions for the knowledge base article in the tab](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step6) in the walkthrough.  
  
<a name="PopInOut"></a>   
## <a name="configure-the-pop-in-and-pop-out-feature-for-knowledge-base-articles"></a>Đặt cấu hình tính năng bật vào và bật ra cho bài viết cơ sở kiến thức  
 Bạn có thể đặt cấu hình để hiển thị bài viết cơ sở kiến thức trong tab khi bạn bấm vào tiêu đề liên kết trong bảng điều khiển tìm kiếm KB. You can further use the `FloatingPanel` in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to pop out a knowledge base article from the main panel so that users can display the article on another monitor in a multi-monitor environment. Để thực hiện các tính năng bật lên cho một bài viết cơ sở kiến thức, sử dụng hành động `MoveToPanel` trên kiểm soát tổ chức hiển thị bài viết trong tab bảng điều khiển chính và thiết lập tham số dữ liệu như `FloatingPanel`. This moves the hosted control that displays the article from `MainPanel` to `FloatingPanel`. Bạn có thể gọi hành động này từ nút thanh công cụ trên kiểm soát tổ chức.  
  
 ![Action call for configuring the pop-out feature](../unified-service-desk/media/usd-action-call-pop-out.png "Action call for configuring the pop-out feature")  
  
> [!NOTE]
>  Trong các ví dụ này, tên của kiểm soát tổ chức hiển thị bài viết là `KB Article`. Bạn phải sử dụng tên kiểm soát tổ chức thích hợp theo cấu hình của mình.  
  
 To configure the pop-in feature, again use the `MoveToPanel` action, but set the data parameter to `MainPanel`. This moves the hosted control that displays the article from `FloatingPanel` to `MainPanel`.  
  
 ![Action call for the pop-in feature](../unified-service-desk/media/usd-action-call-pop-in.png "Action call for the pop-in feature")  
  
 You can call this action from a toolbar button on the hosted control. Tuy nhiên, bạn phải đặt cấu hình nút thanh công cụ bật lên để chỉ hiển thị khi kiểm soát tổ chức có trong `FloatingPanel`. Bạn có thể thực hiện điều này bằng cách chỉ định điều kiện sau trong trường **Cột Hiển thị** của định nghĩa nút thanh công cụ bật lên.  
  
```  
"[[$Panel.KB Article]+]"=="FloatingPanel"  
```  
  
<a name="Events"></a>   
## <a name="use-the-events-to-configure-various-tasks"></a>Use the events to configure various tasks  
 Use the following three events specific to the knowledge hosted control to configure various tasks related to the knowledge base articles.  
  
- Sử dụng sự kiện `SearchComplete` để thêm cuộc gọi hành động mà bạn muốn được thực hiện khi tìm kiếm các bài viết cơ sở kiến thức là đầy đủ và các kết quả được tải trong kiểm soát tổ chức Kiểm soát KM (ngăn tìm kiếm KB).  
  
- Use the `ResultOpen` event to add action calls that you want to be executed when the title of a knowledge base article is clicked in the search results in the KM Control hosted control (KB search pane) to open the article.  
  
- Use the `SelectionChange` event to add action calls that you want to be executed when a knowledge base article is selected in the search results in the KM Control hosted control (KB search pane).  
  
  [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Predefined events for KM Control](../unified-service-desk/km-control-hosted-control.md#events)  and [Predefined events for Unified Interface KM Control (Hosted Control)](../unified-service-desk/unified-interface-km-control-hosted-control.md#events)
  
<a name="Other"></a>   
## <a name="configure-other-tasks-for-knowledge-base-articles"></a>Đặt cấu hình các tác vụ khác cho bài viết cơ sở kiến thức  
 You can configure other tasks for the knowledge base articles such as copy the link of an article or send an email with pre-populated values as the case title in the email subject and knowledge base article link in the email body. These tasks are available when you deploy the **Knowledge Management** sample application, and you can view the configuration for these tasks in your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps instance under **Settings** > **Unified Service Desk** ([How do I get there?](http://go.microsoft.com/fwlink/p/?LinkId=525636)).  
  
### <a name="see-also"></a>Xem thêm  
 [Use Dynamics 365 for Customer Engagement apps knowledge for effective customer engagement](../unified-service-desk/use-dynamics-365-knowledge-effective-customer-engagement.md) 

 [KM Control (Hosted Control)](../unified-service-desk/km-control-hosted-control.md)  

 [Unified Interface KM Control (Hosted Control)](../unified-service-desk/unified-interface-km-control-hosted-control.md) 

 [Walkthrough 8: Use Dynamics 365 for Customer Engagement apps knowledge within your agent application](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md)
