---
title: WebDDA Events in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about using Web data-driven adapter (WebDDA) events that can be used in automations in Unified Service Desk.
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
ms.assetid: 2ecac8dc-d423-405b-bc4e-23b1b05e1d0e
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
ms.openlocfilehash: 564773386817c644c0cd54969193ac9adf76fcd2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385710"
---
# <a name="webdda-events"></a>Sự kiện WebDDA
Bộ chuyển đổi định hướng dữ liệu web (WebDDA) cung cấp một tập hợp sự kiện có thể được sử dụng trong quá trình tự động hóa. Các sự kiện có thể được chia thành sự kiện trang và sự kiện kiểm soát. Chúng ánh xạ cho cùng tên sự kiện được sử dụng trong DOM. Để biết thêm thông tin về các sự kiện, hãy xem [Sự kiện](https://msdn.microsoft.com/library/aa768400.aspx)  
  
 When registering Action for page events the control parameter in the `RegisterActionForEvent`(For more information, see [Automate hosted applications using HAT automation activities](../unified-service-desk/automate-hosted-applications-using-hat-automation-activities.md)) activity is ignored. Đối với sự kiện kiểm soát, tham số `ControlName` phải chứa tên kiểm soát được chỉ định trong liên kết.  
  
 Một số sự kiện cũng cung cấp dữ liệu bổ sung về sự kiện này. Dữ liệu này có thể được truy cập thông qua hoạt động `GetActionData`. (For more information, see [Automate hosted applications using HAT automation activities](../unified-service-desk/automate-hosted-applications-using-hat-automation-activities.md)) The following example shows the format they’re provided in.  
  
```xml  
<EventArgs[flags] [frame] [headers ] [navigationcontext] [postdata] [url] [urlcontext] [cancel] [type] [key][button]>  
  
```  
  
 Các đối số cung cấp tùy chọn bổ sung cho sự kiện:  
  
|Đối số|Mô tả|  
|--------------|-----------------|  
|`flags`|Một hằng số hoặc giá trị chỉ định tổ hợp các giá trị được xác định bởi liệt kê `BrowserNavConstants`.|  
|`frame`|Biểu thức chuỗi phân biệt chữ hoa chữ thường đánh giá tên khung để hiển thị tài nguyên. Đó là `NULL`, nếu không có khung được đặt tên nhắm mục tiêu cho tài nguyên.|  
|`headers`|A string that contains additional HTTP headers to send to the server. Các tiêu đề này được thêm vào trình duyệt web. This parameter is ignored if the URL isn’t an HTTP URL.|  
|`navigationcontext`|Cờ được sử dụng khi mở cửa sổ mới. Những giá trị này được sử dụng để xác định liệu một cửa sổ bật lên có được hiển thị không.|  
|`postdata`|Data that is sent to the server as part of an HTTPPOST transaction. A POST transaction is typically used to send data gathered by an HTML form. If this parameter doesn’t specify any post data, this method issues an HTTP`GET` transaction. This parameter is ignored if the URL is not an HTTP URL.|  
|`url`|Đã điều hướng tới URL của trang tới sự kiện đó.|  
|`urlcontext`|URL of the page that is opening the new window. Tham số này là một phần của sự kiện `NewWindow` của trình duyệt web.|  
|`cancel`|Quá trình tạo trang đã bị hủy (`True`) hoặc đã hoàn tất (`False`).|  
|`type`|Loại sự kiện, thường giống như chính sự kiện.|  
|`key`|Nút chuột đã được bấm vào tại sự kiện (1=trái, 2=phải, v.v).|  
|`button`|Mã của nút đã được nhấn (ví dụ: mã phím Enter là 13).|  
  
<a name="BKMK_Control"></a>   
## <a name="control-events"></a>Sự kiện Kiểm soát  
 Sự kiện kiểm soát là các sự kiện được liên kết với một kiểm soát.  
  
 Bảng sau liệt kê các sự kiện kiểm soát có sẵn với các tham số tương ứng:  
  
|||  
|-|-|  
|`Element`|`Description`|  
|BeforeNavigate|`flags`, `frame`, `headers`, `navigationcontext`, `postdata`, `url`|  
|onBlur|loại|  
|onchange|loại|  
|onclick|loại, nút|  
|ondblclick|loại, nút|  
|onfocus|loại|  
|onkeydown|loại, phím|  
|onmousedown|loại, nút|  
|onreset|loại|  
|onsubmit|loại|  
  
<a name="BKMK_pageevents"></a>   
## <a name="page-events"></a>Sự kiện Trang  
 Khi đăng ký hành động cho sự kiện trang, tham số kiểm soát trong hoạt động `RegisterActionForEvent` bị bỏ qua. (For more information, see [Automate hosted applications using HAT automation activities](../unified-service-desk/automate-hosted-applications-using-hat-automation-activities.md))  
  
 Bảng sau liệt kê các sự kiện trang có sẵn với các tham số tương ứng:  
  
|||  
|-|-|  
|**Yếu tố**|**Mô tả**|  
|BeforeNavigate|`flags`, `frame`, `headers`, `navigationcontext`, `postdata`, `url`|  
|BeforeNewWindow|`flags`, `url`, `urlcontext`|  
|DocumentCompleted|`Notification`, `flag`, `url`|  
|DownloadStarted|`Notification`, `flag`, `url`|  
|DownloadCompleted|`Notification`, `flag`, `url`|  
|NewWindow2|`Cancel`|  
|NewWindow3|`flags`, `url`, `urlcontext`, `cancel`|  
  
### <a name="see-also"></a>Xem thêm  
 [WebDDA](../unified-service-desk/web-dda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
