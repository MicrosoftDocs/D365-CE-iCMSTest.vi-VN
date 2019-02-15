---
title: Add multilanguage support for your agent applications | MicrosoftDocs
description: Learn about adding multilanguage support for your agent applications. The multi-language support is available for all the components except for those that are surfaced through Customer Care Accelerator, which doesn’t support multi-language scenarios. Điều này bao gồm tên tab tổ chức kiểm soát.
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
ms.assetid: f11820ab-d009-4737-ab46-56d4587881e1
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: ae709ee5e03591fb113090ddb7e02b1e319a16be
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387378"
---
# <a name="add-and-manage-multilanguage-support-localized-resources-for-your-agent-applications"></a>Add and manage multilanguage support (localized resources) for your agent applications
[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]cho phép bạn bó trong chuỗi bản địa hóa cho giao diện kiểm sát của bạn để chúng xuất hiện trong ngôn ngữ dựa trên các thiết lập miền địa phương của máy tính của người dùng. Hỗ trợ đa ngôn ngữ có sẵn cho tất cả các thành phần ngoại trừ những người đó thiết đặt thông qua [!INCLUDE[pn_customer_care_accelerator](../includes/pn-customer-care-accelerator.md)], mà không hỗ trợ kịch bản đa ngôn ngữ. Điều này bao gồm tên tab tổ chức kiểm soát.  
  
 Để cung cấp tài nguyên bản địa hóa cho thành phần của bạn:  
  
1. Start by creating an XML file using the [!INCLUDE[pn_ASP.NET_short](../includes/pn-asp-net-short.md)]resx formatting. Đây là một ví dụ về định dạng này.  
  
   ```xml  
   <root>  
     <data name="Welcome">  
       <value>My Translated Welcome</value>   
     </data>  
   </root>  
   ```  
  
    Mỗi cụm từ mà bạn muốn cung cấp bản dịch cho phải được bao gồm trong một phần tử dữ liệu với một tên và giá trị phụ với các bản dịch.  
  
2. Lưu tệp này với các định danh ngôn ngữ trong tên tập tin. For example, if you have Spanish resources, you can save the file with the name “TranslationResource.es.xml.”  
  
3. Upload the file as a web resource to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps. Đặt tên tài nguyên web do đó bạn có thể xác định ngôn ngữ của các nguồn tài nguyên chuỗi trong nó.  
  
   1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
   2. Go to **Settings** > **Customizations** ([How do I get there?](http://go.microsoft.com/fwlink/p/?LinkId=525636))  
  
   3. Bấm vào **tùy chỉnh hệ thống** để thêm các nguồn tài nguyên web vào các giải pháp mặc định.  
  
   4. Trên trang **Giải pháp mặc định**, bấm vào **nguồn tài nguyên Web**, và sau đó nhấp vào **Mới**.  
  
   5. On the new web resource page, specify the name of the web resource, select **Data (XML)** as the type, **English** as the language, and then select your .xml file.  
  
   ![New web resource](../unified-service-desk/media/usd-new-web-resource.PNG "New web resource")  
  
   6.  Lưu và xuất bản tài nguyên web của bạn.  
  
4. Sau khi xuất bản tài nguyên web cho tập tin tài nguyên ngôn ngữ của bạn, thêm nguồn tài nguyên web vào kiểm soát tổ chức **trình quản lý chung** của bạn.  
  
   1. On the nav bar, choose **Settings** > **Unified Service Desk** > **Hosted Controls**.  
  
   2. Click **Dynamics 365 for Customer Engagement apps Global Manager** under the **Name** column, or select the record, and click **Edit** on the command bar.  
  
      > [!NOTE]
      > **Dynamics 365 for Customer Engagement apps Global Manager** is the name of the default **Global Manager** hosted control type in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Nếu bạn có kiểm soát tổ chức trình quản lý chung với tên khác, hãy chọn tên đó để thay thế.  
  
   3. On the **Dynamics 365 for Customer Engagement apps Global Manager** page, under the **Language Services** area, click **+** to add a language module record.  
  
   ![Add a language module](../unified-service-desk/media/usd-add-language-module.png "Add a language module")  
  
   4.  Trên trang **Mô đun ngôn ngữ mới**, hãy chỉ định tên, LCID, và tên của các nguồn tài nguyên web có chứa các tập tin bản dịch.  
  
        LCID nên được xác định với một giá trị đại diện cho ngôn ngữ đó đại diện cho tài nguyên này. [Xem danh sách ID các miền địa phương](https://msdn.microsoft.com/library/ms912047\(WinEmbedded.10\).aspx).  
  
   ![New language module](../unified-service-desk/media/usd-new-language-module.png "New language module")  
  
   > [!IMPORTANT]
   >  If you use language services, you should always configure language services for your base [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps language. Trong ví dụ này, cũng thêm một dịch vụ ngôn ngữ tiếng Anh. The base language translation file is always used if someone uses a language pack in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps that doesn’t have a translation file in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] language services.  
  
5. Bấm vào **Lưu**.  
  
## <a name="use-the-translated-text"></a>Sử dụng Văn bản Đã dịch  
 Để sử dụng văn bản dịch, tham khảo các mục bằng cách sử dụng một tham số thay thế, như được hiển thị ở đây.  
  
```xml  
[[$Resources.Welcome]]  
```  
  
 Điều này có thể được sử dụng bất cứ nơi nào mà bạn sử dụng một tham số thay thế và các tập tin bản dịch cũng có thể chứa tham số thay thế. Ngôn ngữ dịch sẽ được thay thế trước tiên và sau đó các thông số thay thế khác sẽ được áp dụng. Chúng có thể được sử dụng cho tên của các nút, các văn bản của các mã lệnh tổng đài viên hoặc bất cứ nơi nào bạn có thể sử dụng tham số thay thế.  
  
### <a name="see-also"></a>Xem thêm  
 [Trình quản lý chung (Kiểm soát tổ chức)](../unified-service-desk/global-manager-hosted-control.md)
