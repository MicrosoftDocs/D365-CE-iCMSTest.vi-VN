---
title: AttributeMatchPath in Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: The topic explains about the <AttributeMatchPath> element that can be utilized by a web control configuration to find the desired control on the currently loaded HTML document using the controls attributes.
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
ms.assetid: d0fcd69d-b049-4dff-8a08-1add589d88f9
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
ms.openlocfilehash: 680817aa986c4e840727cdfcb7db98a695188bb5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385750"
---
# <a name="attributematchpath"></a><span data-ttu-id="03ad8-103">AttributeMatchPath</span><span class="sxs-lookup"><span data-stu-id="03ad8-103">AttributeMatchPath</span></span>
<span data-ttu-id="03ad8-104">Yếu tố `<AttributeMatchPath>` có thể được một cấu hình kiểm soát web sử dụng để tìm kiểm soát mong muốn trên tài liệu `HTML` hiện được tải bằng các thuộc tính kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="03ad8-104">The `<AttributeMatchPath>` element can be utilized by a web control configuration to find the desired control on the currently loaded `HTML` document using the controls attributes.</span></span> <span data-ttu-id="03ad8-105">The "match path" is an ordered list of key/value pairs that is applied by iterating through every element in the `HTML``Document Object Model (DOM)`, matching attributes along the nodes of the match path.</span><span class="sxs-lookup"><span data-stu-id="03ad8-105">The "match path" is an ordered list of key/value pairs that is applied by iterating through every element in the `HTML``Document Object Model (DOM)`, matching attributes along the nodes of the match path.</span></span> <span data-ttu-id="03ad8-106">Mỗi khóa đại diện cho tên của thuộc tính để khớp và giá trị được khớp với giá trị thuộc tính đã chỉ định trong tài liệu `HTML`.</span><span class="sxs-lookup"><span data-stu-id="03ad8-106">Each key represents the name of the attribute to match, and the value is matched with the assigned attribute value in the `HTML` document.</span></span> <span data-ttu-id="03ad8-107">Sau khi khớp một khóa/giá trị, cặp khóa/giá trị tiếp theo trong trình tự được sử dụng để so sánh với từng yếu tố trong `DOM`.</span><span class="sxs-lookup"><span data-stu-id="03ad8-107">After a key/value is matched, the next key/value pair in the sequence is used to compare to each element in the `DOM`.</span></span> <span data-ttu-id="03ad8-108">Lưu ý rằng khi **keyn+1 = keyn**, việc khớp với cặp khóa/giá trị mới bắt đầu bằng nút yếu tố tiếp theo trong `DOM`, không phải với nút hiện tại.</span><span class="sxs-lookup"><span data-stu-id="03ad8-108">Note that when **keyn+1 = keyn**, matching with the new key/value pair begins with the next element node in the `DOM`, not with the current node.</span></span>  
  
<a name="syntax"></a>   
## <a name="attributematchpath-syntax"></a><span data-ttu-id="03ad8-109">\<AttributeMatchPath> syntax</span><span class="sxs-lookup"><span data-stu-id="03ad8-109">\<AttributeMatchPath> syntax</span></span>  
 <span data-ttu-id="03ad8-110">Yếu tố `<AttributeMatchPath>` có thể được nhắm mục tiêu tại các khung cụ thể bên trong ứng dụng `HTML`.</span><span class="sxs-lookup"><span data-stu-id="03ad8-110">The `<AttributeMatchPath>` element can be targeted at specific frames within an `HTML` application.</span></span>  
  
```xml  
<AttributeMatchPath [framename=""|framesrc=""] [framematch="n"] [matchtype="equals|startswith|endswith|contains"]>  
  
<attributeName1 [matchtype= "equals|startswith|endswith|contains"]>  
attributeValueToMatch1  
</attributeName1>  
  
<attributeName2 [matchtype= "equals|startswith|endswith|contains"]>  
attributeValueToMatch2  
</attributeName2>  
  
…  
<attributeNamen [matchtype= "equals|startswith|endswith|contains"]>  
attributeValueToMatchn  
</attributeNamen>  
  
</AttributeMatchPath>  
  
```  
  
<a name="elements"></a>   
## <a name="attributematchpath-elements"></a><span data-ttu-id="03ad8-111">\<AttributeMatchPath> elements</span><span class="sxs-lookup"><span data-stu-id="03ad8-111">\<AttributeMatchPath> elements</span></span>  
 <span data-ttu-id="03ad8-112">Bảng sau mô tả các yếu tố của `<AttributeMatchPath>`</span><span class="sxs-lookup"><span data-stu-id="03ad8-112">The following table describes the elements of `<AttributeMatchPath>`</span></span>  
  
|<span data-ttu-id="03ad8-113">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="03ad8-113">Element</span></span>|<span data-ttu-id="03ad8-114">Mô tả</span><span class="sxs-lookup"><span data-stu-id="03ad8-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="03ad8-115">Framename</span><span class="sxs-lookup"><span data-stu-id="03ad8-115">Framename</span></span>|<span data-ttu-id="03ad8-116">Khớp tên khung của IFrame.</span><span class="sxs-lookup"><span data-stu-id="03ad8-116">Matches the frame name of the IFrame.</span></span>|  
|<span data-ttu-id="03ad8-117">Framesrc</span><span class="sxs-lookup"><span data-stu-id="03ad8-117">Framesrc</span></span>|<span data-ttu-id="03ad8-118">Khớp nguồn của IFrame.</span><span class="sxs-lookup"><span data-stu-id="03ad8-118">Matches the source of the IFrame.</span></span>|  
|<span data-ttu-id="03ad8-119">Framematch</span><span class="sxs-lookup"><span data-stu-id="03ad8-119">Framematch</span></span>|<span data-ttu-id="03ad8-120">Khớp vị trí thứ n của khung đã chỉ định, mặc định là `1`.</span><span class="sxs-lookup"><span data-stu-id="03ad8-120">Matches the nth one of the specified frame; default is `1`.</span></span>|  
|<span data-ttu-id="03ad8-121">Matchtype</span><span class="sxs-lookup"><span data-stu-id="03ad8-121">Matchtype</span></span>|<span data-ttu-id="03ad8-122">Chỉ định cách kết hợp chú thích.</span><span class="sxs-lookup"><span data-stu-id="03ad8-122">Specifies how the caption should be matched.</span></span> <span data-ttu-id="03ad8-123">Các giá trị có thể là `equals`, `startswith`, `endswith` hoặc `contains`; bất kỳ giá trị nào khác sẽ thêm ngoại lệ.</span><span class="sxs-lookup"><span data-stu-id="03ad8-123">Possible values are `equals`, `startswith`, `endswith`, or `contains`; any other value will throw an exception.</span></span>|  
  
 <span data-ttu-id="03ad8-124">Ví dụ, nếu một ứng dụng web có nhiều hơn một khung với một tên, bạn có thể chỉ định để tìm kiếm khung thứ hai hoặc thứ ba của tên đó.</span><span class="sxs-lookup"><span data-stu-id="03ad8-124">For example, if a web application has more than one frame with a given name, you can specify to search for the second or third frame of that name.</span></span> <span data-ttu-id="03ad8-125">Thuộc tính `framematch` là không bắt buộc, tuy nhiên được giả định là 1 trừ khi được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="03ad8-125">The `framematch` attribute is not mandatory however is assumed to be 1 unless specified.</span></span> <span data-ttu-id="03ad8-126">Nếu `framematch` được chỉ định, `framename` hoặc `framesrc` phải được xác định; Nếu không, một ngoại lệ "Khung không tìm thấy" sẽ được thêm.</span><span class="sxs-lookup"><span data-stu-id="03ad8-126">If `framematch` is specified, `framename` or `framesrc` must be specified; otherwise, a "Frame not found" exception will be thrown.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="03ad8-127">Nếu không thuộc tính nào trong số các thuộc tính `AttributeMatchPath` được cung cấp, thao tác sẽ diễn ra trong cửa sổ cấp đầu tiên như thể nó là một khung.</span><span class="sxs-lookup"><span data-stu-id="03ad8-127">If none of the `AttributeMatchPath` attributes are supplied, the operation will take place in the top-level window as if it were a frame.</span></span> <span data-ttu-id="03ad8-128">Nếu cả hai `framename` và `framesrc` được chỉ định, `framesrc` được ưu tiên.</span><span class="sxs-lookup"><span data-stu-id="03ad8-128">If both `framename` and `framesrc` are specified, `framesrc` has precedence.</span></span>  
  
 <span data-ttu-id="03ad8-129">Trong ví dụ sau đây, các `matchtype` được sử dụng trên `attributeValueToMatch`.</span><span class="sxs-lookup"><span data-stu-id="03ad8-129">In the following example, the `matchtype` is used on the `attributeValueToMatch`.</span></span>  
  
```xml  
<AttributeMatchPath>  
<key1>val1</key1>  
<key2>val2</key2>  
<key3[matchtype="equals|startswith|endswith|contains"]>attributeValueToMatch</key3>  
  .  
<keyn>valn</keyn>  
</AttributeMatchPath>  
  
```  
  
 <span data-ttu-id="03ad8-130">Ví dụ sau cho thấy một đường dẫn phù hợp thuộc tính cho thẻ `Test`.</span><span class="sxs-lookup"><span data-stu-id="03ad8-130">The following example shows a full attribute match path for a `Test` tag.</span></span>  
  
```xml  
Page code:    
<Test FirstName='John' LastName='Smith'/>  
  
Match path used in control description:    
<AttributeMatchPath>  
<FirstName>John</FirstName>  
<LastName>Smith</LastName>  
</AttributeMatchPath>  
  
```  
  
> [!NOTE]
>  <span data-ttu-id="03ad8-131">Chúng tôi khuyến khách bạn chỉ sử dụng ID và/hoặc tên là thuộc tính dự án.</span><span class="sxs-lookup"><span data-stu-id="03ad8-131">It is highly recommended that you use only ID and/or name as search attributes.</span></span> <span data-ttu-id="03ad8-132">Các thuộc tính khác sẽ có tác động tiêu cực đến hiệu suất.</span><span class="sxs-lookup"><span data-stu-id="03ad8-132">The other attributes will have a negative impact on the performance.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="03ad8-133">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="03ad8-133">See also</span></span>  
 <span data-ttu-id="03ad8-134">[WebDDA](../unified-service-desk/web-dda.md) </span><span class="sxs-lookup"><span data-stu-id="03ad8-134">[WebDDA](../unified-service-desk/web-dda.md) </span></span>  
 [<span data-ttu-id="03ad8-135">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="03ad8-135">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
