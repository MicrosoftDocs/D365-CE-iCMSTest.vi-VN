---
title: Use data driven adapters (DDAs) in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn how to use data-driven adapters (DDAs) in Unified Service Desk.
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
ms.assetid: 56bb1a8b-f988-467e-9b59-8951a8809570
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
ms.openlocfilehash: a4a1e970e586f993c3df9a3c9241d3f067ad89db
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386618"
---
# <a name="use-data-driven-adapters-ddas-in-unified-service-desk"></a>Use data driven adapters (DDAs) in Unified Service Desk
Bộ chuyển đổi định hướng dữ liệu (DDA) là các bộ chuyển đổi được tận dụng nói chung của [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)]. Các bộ chuyển đổi này là các cụm tổ hợp chung chỉ xử lý tương tác với UI và không chứa quy trình kinh doanh. SDK [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] đi kèm với DDA cung cấp một bộ chức năng chung cho phép bạn lưu trữ và truy cập vào một loạt ứng dụng. Tuy nhiên, bạn có thể yêu cầu các chức năng bổ sung tùy theo loại ứng dụng. Có các cách khác nhau để mở rộng chức năng hiện có, chẳng hạn như tạo DDA mới (và sử dụng trong DDA tổng hợp với DDA bên ngoài) và mở rộng DDA hiện có.  
  
## <a name="in-this-section"></a>In This Section  
 [Các loại Bộ chuyển đổi Định hướng Dữ liệu](../unified-service-desk/use-data-driven-adapters-ddas.md#types)  
  
 [Đang tạo DDA](../unified-service-desk/use-data-driven-adapters-ddas.md#create)  
  
 [Mở rộng DDA hiện có](../unified-service-desk/use-data-driven-adapters-ddas.md#extend)  
  
 [Liên kết](../unified-service-desk/use-data-driven-adapters-ddas.md#bindings)  
  
 [Sử dụng DDA trong các bộ chuyển đổi ứng dụng tùy chỉnh](../unified-service-desk/use-data-driven-adapters-ddas.md#custom)  
  
<a name="types"></a>   
## <a name="types-of-data-driven-adapters"></a>Các loại Bộ chuyển đổi Định hướng Dữ liệu  
 Có bốn loại DDA:  
  
-   [WinDDA](../unified-service-desk/windda.md)  
  
-   [WebDDA](../unified-service-desk/web-dda.md)  
  
-   [UIADDA](../unified-service-desk/uiadda.md)  
  
-   [JavaDDA](../unified-service-desk/javadda.md)  
  
<a name="create"></a>   
## <a name="creating-a-dda"></a>Đang tạo DDA  
 You can create a new DDA by simply inheriting the [DataDrivenAdapterBase](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.datadrivenadapterbase) class.  
  
 Lớp này có hàm dựng có thể được quá tải.  
  
<a name="extend"></a>   
## <a name="extending-an-existing-dda"></a>Mở rộng DDA hiện có  
 Trong phần trước chúng ta đã biết cách tạo DDA. Tuy nhiên, nếu tùy chỉnh của bạn là trên danh nghĩa, bạn có thể sử dụng DDA hiện có và mở rộng theo yêu cầu.  
  
 Bạn có thể sử dụng các lớp sau để mở rộng DDA UII hiện có:  
  
- [WinDataDrivenAdapter](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.windatadrivenadapter): Creates an adapter based on the WinDDA.  
  
- [WebDataDrivenAdapter](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.webdatadrivenadapter): Creates an adapter based on the WebDDA.  
  
- [JavaDataDrivenAdapter](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.javadatadrivenadapter): Creates an adapter based on the JavaDDA.  
  
- [UIADataDrivenAdapter](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.uiadatadrivenadapter): Creates an adapter based on the UIADDA.  
  
  All the preceding classes derive from [DataDrivenAdapterBase](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.datadrivenadapterbase) class.  
  
<a name="bindings"></a>   
## <a name="bindings"></a>Liên kết  
 Bộ chuyển đổi định hướng dữ liệu, có tên là liên kết, để xác định cách bộ chuyển đổi xác định thành phần UI của ứng dụng được lưu trữ. Ví dụ: các liên kết có thể chứa đường dẫn Mô hình Đối tượng Tài liệu (DOM) để mô tả các yếu tố trên trang web. Ví dụ sau cho thấy chuỗi khởi tạo ứng dụng với cây con liên kết DDA nhúng. Đây là một ví dụ chung nhưng nó chỉ ra mô hình được sử dụng để thực hiện các kiểm soát `Acc` trong liên kết Windows.  
  
> [!NOTE]
>  Một số tham số cấu hình đã được xóa để cho rõ ràng.  
  
```xml  
<initstring>  
    <interopAssembly>  
      <URL>path to executable</URL>  
      <Arguments>test argument</Arguments>  
      <WorkingDirectory>c:\</WorkingDirectory>  
      <hostInside/>  
    </interopAssembly>  
<!—- notice there is no custom application adapter specified here-->  
    <displayGroup>None</displayGroup>  
    <optimumSize x="800" y="600"/>  
    <minimumSize x="640" y="480"/>  
    <DataDrivenAdapterBindings>  
      <Type>typeName, assemblyName</Type>  
      <Controls>  
        <AccControl name="combobox1">  
          <Path>  
            <FindWindow>  
              <ControlID>1003</ControlID>  
            </FindWindow>  
          </Path>  
        </AccControl>  
</Controls>  
    </DataDrivenAdapterBindings>  
</initstring>  
  
```  
  
 Nếu bạn đang sử dụng Nhà máy Phần mềm HAT, ứng dụng này sẽ tạo `InitString`. Ứng dụng này sau đó có thể được triển khai đến máy chủ từ nhà máy phần mềm.  
  
 Nếu bạn đang thêm trực tiếp ứng dụng được lưu trữ bằng UI Quản trị, bạn không cần tạo `InitString` hoàn chỉnh. Bạn chỉ cần chỉ định phần <`DataDrivenAdapterBindings`> và thêm phần đó vào tab `Automation Xml`.  
  
<a name="custom"></a>   
## <a name="using-ddas-in-custom-application-adapters"></a>Sử dụng DDA trong các bộ chuyển đổi ứng dụng tùy chỉnh  
 Mặc dù DDA ban đầu được hình thành để hỗ trợ các quá trình tự động hóa bên trong [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)], các quá trình này cũng có thể được sử dụng bởi bộ chuyển đổi tùy chỉnh để đạt được kết quả thành công. Mẫu mã sau đây, được lấy từ bộ chuyển đổi tùy chỉnh, mô phỏng cách bộ chuyển đổi tùy chỉnh có thể sử dụng DDA và mô phỏng các lợi ích chung của DDA. Như mẫu minh họa, việc sử dụng DDA cho phép tách thông tin mã và cấu hình.  
  
```csharp  
DataDrivenAdapter Dda;  
public overrIDe bool Initialize()  
{  
   Dda=DataDrivenAdapter.CreateInstance(ApplicationInitString,ApplicationObject);  
   return (Dda != null);  
}  
public overrIDe bool DoAction(Action action, ref string data)  
{  
if (action.Name == "AddToHistory")  
   {  
   Dda.ExecuteControlAction("combobox1");  
   Dda.SetControlValue("textbox1", data);  
   Dda.ExecuteControlAction("button1");  
   }  
}  
  
```  
  
 Cấu hình DDA, được nhúng trong `InitString` của ứng dụng là XML như trong ví dụ sau.  
  
```xml  
<DataDrivenAdapterBindings>  
<Type> Microsoft.UII.HostedApplicationToolkit.DataDrivenAdapter.WinDataDrivenAdapter, Microsoft.UII.HostedApplicationToolkit.DataDrivenAdapter</Type>  
  <Controls>  
    <AccControl name="combobox1">  
      <Path>  
        <FindWindow>  
          <ControlID>1003</ControlID>  
        </FindWindow>  
      </Path>  
    </AccControl>  
    <AccControl name="textbox1">  
      <Path>  
        <FindWindow>  
          <ControlID>1001</ControlID>  
        </FindWindow>  
      </Path>  
    </AccControl>  
    <AccControl name="button1">  
      <Path>  
        <FindWindow>  
          <ControlID>1002</ControlID>  
        </FindWindow>  
      </Path>  
    </AccControl>  
  </Controls>  
</DataDrivenAdapterBindings>  
  
```  
  
 Yếu tố `<Type/>` hướng UII để tạo phiên bản theo cách động cho loại được chỉ định trong loại, định dạng cụm tổ hợp, do đó cho phép DDA tùy chỉnh được tải và sử dụng. Yếu tố `<Controls/>` chứa danh sách các kiểm soát đã cấu hình, được chỉ định theo cách do DDA đã tải yêu cầu.  
  
### <a name="see-also"></a>Xem thêm  
 [Work with HAT Software Factory](../unified-service-desk/work-with-hat-software-factory.md)
