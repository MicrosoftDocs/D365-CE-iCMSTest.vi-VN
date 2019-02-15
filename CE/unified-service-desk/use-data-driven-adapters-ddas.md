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
# <a name="use-data-driven-adapters-ddas-in-unified-service-desk"></a><span data-ttu-id="46eb6-103">Use data driven adapters (DDAs) in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="46eb6-103">Use data driven adapters (DDAs) in Unified Service Desk</span></span>
<span data-ttu-id="46eb6-104">Bộ chuyển đổi định hướng dữ liệu (DDA) là các bộ chuyển đổi được tận dụng nói chung của [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)].</span><span class="sxs-lookup"><span data-stu-id="46eb6-104">Data-driven adapters (DDAs) are the adapters leveraged generally by the [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)].</span></span> <span data-ttu-id="46eb6-105">Các bộ chuyển đổi này là các cụm tổ hợp chung chỉ xử lý tương tác với UI và không chứa quy trình kinh doanh.</span><span class="sxs-lookup"><span data-stu-id="46eb6-105">These adapters are generic assemblies that handle only the interaction with the UI and do not contain business processes.</span></span> <span data-ttu-id="46eb6-106">SDK [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] đi kèm với DDA cung cấp một bộ chức năng chung cho phép bạn lưu trữ và truy cập vào một loạt ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="46eb6-106">The [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] SDK ships with a DDA that provides a common set of functions that allows you to host and access a wide range of applications.</span></span> <span data-ttu-id="46eb6-107">Tuy nhiên, bạn có thể yêu cầu các chức năng bổ sung tùy theo loại ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="46eb6-107">However, you might require additional functionality depending on the type of application.</span></span> <span data-ttu-id="46eb6-108">Có các cách khác nhau để mở rộng chức năng hiện có, chẳng hạn như tạo DDA mới (và sử dụng trong DDA tổng hợp với DDA bên ngoài) và mở rộng DDA hiện có.</span><span class="sxs-lookup"><span data-stu-id="46eb6-108">There are various ways of extending the existing functionality, such as creating a new DDA (and using it in a composite DDA with outer DDAs) and extending an existing DDA.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="46eb6-109">In This Section</span><span class="sxs-lookup"><span data-stu-id="46eb6-109">In This Section</span></span>  
 [<span data-ttu-id="46eb6-110">Các loại Bộ chuyển đổi Định hướng Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="46eb6-110">Types of Data Driven Adapters</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md#types)  
  
 [<span data-ttu-id="46eb6-111">Đang tạo DDA</span><span class="sxs-lookup"><span data-stu-id="46eb6-111">Creating a DDA</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md#create)  
  
 [<span data-ttu-id="46eb6-112">Mở rộng DDA hiện có</span><span class="sxs-lookup"><span data-stu-id="46eb6-112">Extending an existing DDA</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md#extend)  
  
 [<span data-ttu-id="46eb6-113">Liên kết</span><span class="sxs-lookup"><span data-stu-id="46eb6-113">Bindings</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md#bindings)  
  
 [<span data-ttu-id="46eb6-114">Sử dụng DDA trong các bộ chuyển đổi ứng dụng tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="46eb6-114">Using DDAs in custom application adapters</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md#custom)  
  
<a name="types"></a>   
## <a name="types-of-data-driven-adapters"></a><span data-ttu-id="46eb6-115">Các loại Bộ chuyển đổi Định hướng Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="46eb6-115">Types of Data Driven Adapters</span></span>  
 <span data-ttu-id="46eb6-116">Có bốn loại DDA:</span><span class="sxs-lookup"><span data-stu-id="46eb6-116">There are four types of DDAs:</span></span>  
  
-   [<span data-ttu-id="46eb6-117">WinDDA</span><span class="sxs-lookup"><span data-stu-id="46eb6-117">WinDDA</span></span>](../unified-service-desk/windda.md)  
  
-   [<span data-ttu-id="46eb6-118">WebDDA</span><span class="sxs-lookup"><span data-stu-id="46eb6-118">WebDDA</span></span>](../unified-service-desk/web-dda.md)  
  
-   [<span data-ttu-id="46eb6-119">UIADDA</span><span class="sxs-lookup"><span data-stu-id="46eb6-119">UIADDA</span></span>](../unified-service-desk/uiadda.md)  
  
-   [<span data-ttu-id="46eb6-120">JavaDDA</span><span class="sxs-lookup"><span data-stu-id="46eb6-120">JavaDDA</span></span>](../unified-service-desk/javadda.md)  
  
<a name="create"></a>   
## <a name="creating-a-dda"></a><span data-ttu-id="46eb6-121">Đang tạo DDA</span><span class="sxs-lookup"><span data-stu-id="46eb6-121">Creating a DDA</span></span>  
 <span data-ttu-id="46eb6-122">You can create a new DDA by simply inheriting the [DataDrivenAdapterBase](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.datadrivenadapterbase) class.</span><span class="sxs-lookup"><span data-stu-id="46eb6-122">You can create a new DDA by simply inheriting the [DataDrivenAdapterBase](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.datadrivenadapterbase) class.</span></span>  
  
 <span data-ttu-id="46eb6-123">Lớp này có hàm dựng có thể được quá tải.</span><span class="sxs-lookup"><span data-stu-id="46eb6-123">The class has the constructor which can be overloaded.</span></span>  
  
<a name="extend"></a>   
## <a name="extending-an-existing-dda"></a><span data-ttu-id="46eb6-124">Mở rộng DDA hiện có</span><span class="sxs-lookup"><span data-stu-id="46eb6-124">Extending an existing DDA</span></span>  
 <span data-ttu-id="46eb6-125">Trong phần trước chúng ta đã biết cách tạo DDA.</span><span class="sxs-lookup"><span data-stu-id="46eb6-125">In the previous section we saw how to create a DDA.</span></span> <span data-ttu-id="46eb6-126">Tuy nhiên, nếu tùy chỉnh của bạn là trên danh nghĩa, bạn có thể sử dụng DDA hiện có và mở rộng theo yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="46eb6-126">However, if your customization is nominal, you can use the existing DDA and extend it as per requirements.</span></span>  
  
 <span data-ttu-id="46eb6-127">Bạn có thể sử dụng các lớp sau để mở rộng DDA UII hiện có:</span><span class="sxs-lookup"><span data-stu-id="46eb6-127">You can use the following classes to extend the existing UII DDAs:</span></span>  
  
- <span data-ttu-id="46eb6-128">[WinDataDrivenAdapter](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.windatadrivenadapter): Creates an adapter based on the WinDDA.</span><span class="sxs-lookup"><span data-stu-id="46eb6-128">[WinDataDrivenAdapter](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.windatadrivenadapter): Creates an adapter based on the WinDDA.</span></span>  
  
- <span data-ttu-id="46eb6-129">[WebDataDrivenAdapter](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.webdatadrivenadapter): Creates an adapter based on the WebDDA.</span><span class="sxs-lookup"><span data-stu-id="46eb6-129">[WebDataDrivenAdapter](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.webdatadrivenadapter): Creates an adapter based on the WebDDA.</span></span>  
  
- <span data-ttu-id="46eb6-130">[JavaDataDrivenAdapter](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.javadatadrivenadapter): Creates an adapter based on the JavaDDA.</span><span class="sxs-lookup"><span data-stu-id="46eb6-130">[JavaDataDrivenAdapter](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.javadatadrivenadapter): Creates an adapter based on the JavaDDA.</span></span>  
  
- <span data-ttu-id="46eb6-131">[UIADataDrivenAdapter](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.uiadatadrivenadapter): Creates an adapter based on the UIADDA.</span><span class="sxs-lookup"><span data-stu-id="46eb6-131">[UIADataDrivenAdapter](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.uiadatadrivenadapter): Creates an adapter based on the UIADDA.</span></span>  
  
  <span data-ttu-id="46eb6-132">All the preceding classes derive from [DataDrivenAdapterBase](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.datadrivenadapterbase) class.</span><span class="sxs-lookup"><span data-stu-id="46eb6-132">All the preceding classes derive from [DataDrivenAdapterBase](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.datadrivenadapterbase) class.</span></span>  
  
<a name="bindings"></a>   
## <a name="bindings"></a><span data-ttu-id="46eb6-133">Liên kết</span><span class="sxs-lookup"><span data-stu-id="46eb6-133">Bindings</span></span>  
 <span data-ttu-id="46eb6-134">Bộ chuyển đổi định hướng dữ liệu, có tên là liên kết, để xác định cách bộ chuyển đổi xác định thành phần UI của ứng dụng được lưu trữ.</span><span class="sxs-lookup"><span data-stu-id="46eb6-134">A data-driven adapter uses data, named the bindings, to define the way that it identifies a UI component of a hosted application.</span></span> <span data-ttu-id="46eb6-135">Ví dụ: các liên kết có thể chứa đường dẫn Mô hình Đối tượng Tài liệu (DOM) để mô tả các yếu tố trên trang web.</span><span class="sxs-lookup"><span data-stu-id="46eb6-135">For example, the bindings may consist of Document Object Model (DOM) paths for describing elements on a webpage.</span></span> <span data-ttu-id="46eb6-136">Ví dụ sau cho thấy chuỗi khởi tạo ứng dụng với cây con liên kết DDA nhúng.</span><span class="sxs-lookup"><span data-stu-id="46eb6-136">The following example shows an application initialization string with an embedded DDA binding sub-tree.</span></span> <span data-ttu-id="46eb6-137">Đây là một ví dụ chung nhưng nó chỉ ra mô hình được sử dụng để thực hiện các kiểm soát `Acc` trong liên kết Windows.</span><span class="sxs-lookup"><span data-stu-id="46eb6-137">This is a general example, but it indicates the pattern used to implement `Acc` controls in Windows bindings.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="46eb6-138">Một số tham số cấu hình đã được xóa để cho rõ ràng.</span><span class="sxs-lookup"><span data-stu-id="46eb6-138">Some of the configuration parameters have been removed for clarity.</span></span>  
  
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
  
 <span data-ttu-id="46eb6-139">Nếu bạn đang sử dụng Nhà máy Phần mềm HAT, ứng dụng này sẽ tạo `InitString`.</span><span class="sxs-lookup"><span data-stu-id="46eb6-139">If you are using the HAT Software Factory, it will create the `InitString`.</span></span> <span data-ttu-id="46eb6-140">Ứng dụng này sau đó có thể được triển khai đến máy chủ từ nhà máy phần mềm.</span><span class="sxs-lookup"><span data-stu-id="46eb6-140">The application can then be deployed to the server from the software factory.</span></span>  
  
 <span data-ttu-id="46eb6-141">Nếu bạn đang thêm trực tiếp ứng dụng được lưu trữ bằng UI Quản trị, bạn không cần tạo `InitString` hoàn chỉnh.</span><span class="sxs-lookup"><span data-stu-id="46eb6-141">If you are directly adding a hosted application using the Admin UI, you do not need to create the complete `InitString`.</span></span> <span data-ttu-id="46eb6-142">Bạn chỉ cần chỉ định phần <`DataDrivenAdapterBindings`> và thêm phần đó vào tab `Automation Xml`.</span><span class="sxs-lookup"><span data-stu-id="46eb6-142">You only need to specify the <`DataDrivenAdapterBindings`> section and add it to the `Automation Xml` tab.</span></span>  
  
<a name="custom"></a>   
## <a name="using-ddas-in-custom-application-adapters"></a><span data-ttu-id="46eb6-143">Sử dụng DDA trong các bộ chuyển đổi ứng dụng tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="46eb6-143">Using DDAs in custom application adapters</span></span>  
 <span data-ttu-id="46eb6-144">Mặc dù DDA ban đầu được hình thành để hỗ trợ các quá trình tự động hóa bên trong [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)], các quá trình này cũng có thể được sử dụng bởi bộ chuyển đổi tùy chỉnh để đạt được kết quả thành công.</span><span class="sxs-lookup"><span data-stu-id="46eb6-144">Although DDAs were initially conceived to support automations within the [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)], they can also be used by custom adapters to achieve useful results.</span></span> <span data-ttu-id="46eb6-145">Mẫu mã sau đây, được lấy từ bộ chuyển đổi tùy chỉnh, mô phỏng cách bộ chuyển đổi tùy chỉnh có thể sử dụng DDA và mô phỏng các lợi ích chung của DDA.</span><span class="sxs-lookup"><span data-stu-id="46eb6-145">The following code sample, taken from a custom adapter, illustrates how custom adapters can use DDAs, and illustrates the general advantages of DDAs.</span></span> <span data-ttu-id="46eb6-146">Như mẫu minh họa, việc sử dụng DDA cho phép tách thông tin mã và cấu hình.</span><span class="sxs-lookup"><span data-stu-id="46eb6-146">As the sample illustrates, the use of DDAs allows a separation of code and configuration information.</span></span>  
  
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
  
 <span data-ttu-id="46eb6-147">Cấu hình DDA, được nhúng trong `InitString` của ứng dụng là XML như trong ví dụ sau.</span><span class="sxs-lookup"><span data-stu-id="46eb6-147">The DDA configuration, which is embedded in the application's `InitString`, is XML, as in the following example.</span></span>  
  
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
  
 <span data-ttu-id="46eb6-148">Yếu tố `<Type/>` hướng UII để tạo phiên bản theo cách động cho loại được chỉ định trong loại, định dạng cụm tổ hợp, do đó cho phép DDA tùy chỉnh được tải và sử dụng.</span><span class="sxs-lookup"><span data-stu-id="46eb6-148">The `<Type/>` element directs UII to dynamically instantiate the type specified in type, assembly format, thus allowing custom DDAs to be loaded and used.</span></span> <span data-ttu-id="46eb6-149">Yếu tố `<Controls/>` chứa danh sách các kiểm soát đã cấu hình, được chỉ định theo cách do DDA đã tải yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="46eb6-149">The `<Controls/>` element contains the list of configured controls, specified in a manner required by the loaded DDA.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="46eb6-150">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="46eb6-150">See also</span></span>  
 [<span data-ttu-id="46eb6-151">Work with HAT Software Factory</span><span class="sxs-lookup"><span data-stu-id="46eb6-151">Work with HAT Software Factory</span></span>](../unified-service-desk/work-with-hat-software-factory.md)
