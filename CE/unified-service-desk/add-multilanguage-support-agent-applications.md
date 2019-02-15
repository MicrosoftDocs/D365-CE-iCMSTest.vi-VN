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
# <a name="add-and-manage-multilanguage-support-localized-resources-for-your-agent-applications"></a><span data-ttu-id="f6197-105">Add and manage multilanguage support (localized resources) for your agent applications</span><span class="sxs-lookup"><span data-stu-id="f6197-105">Add and manage multilanguage support (localized resources) for your agent applications</span></span>
[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]<span data-ttu-id="f6197-106">cho phép bạn bó trong chuỗi bản địa hóa cho giao diện kiểm sát của bạn để chúng xuất hiện trong ngôn ngữ dựa trên các thiết lập miền địa phương của máy tính của người dùng.</span><span class="sxs-lookup"><span data-stu-id="f6197-106">enables you to bundle in localized strings for your controls interface so that they appear in the language based on the locale settings of the user’s computer.</span></span> <span data-ttu-id="f6197-107">Hỗ trợ đa ngôn ngữ có sẵn cho tất cả các thành phần ngoại trừ những người đó thiết đặt thông qua [!INCLUDE[pn_customer_care_accelerator](../includes/pn-customer-care-accelerator.md)], mà không hỗ trợ kịch bản đa ngôn ngữ.</span><span class="sxs-lookup"><span data-stu-id="f6197-107">The multi-language support is available for all the components except for those that are surfaced through [!INCLUDE[pn_customer_care_accelerator](../includes/pn-customer-care-accelerator.md)], which doesn’t support multi-language scenarios.</span></span> <span data-ttu-id="f6197-108">Điều này bao gồm tên tab tổ chức kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="f6197-108">This includes the hosted control tab names.</span></span>  
  
 <span data-ttu-id="f6197-109">Để cung cấp tài nguyên bản địa hóa cho thành phần của bạn:</span><span class="sxs-lookup"><span data-stu-id="f6197-109">To provide localized resources for your component:</span></span>  
  
1. <span data-ttu-id="f6197-110">Start by creating an XML file using the [!INCLUDE[pn_ASP.NET_short](../includes/pn-asp-net-short.md)]resx formatting.</span><span class="sxs-lookup"><span data-stu-id="f6197-110">Start by creating an XML file using the [!INCLUDE[pn_ASP.NET_short](../includes/pn-asp-net-short.md)]resx formatting.</span></span> <span data-ttu-id="f6197-111">Đây là một ví dụ về định dạng này.</span><span class="sxs-lookup"><span data-stu-id="f6197-111">Here’s an example of this format.</span></span>  
  
   ```xml  
   <root>  
     <data name="Welcome">  
       <value>My Translated Welcome</value>   
     </data>  
   </root>  
   ```  
  
    <span data-ttu-id="f6197-112">Mỗi cụm từ mà bạn muốn cung cấp bản dịch cho phải được bao gồm trong một phần tử dữ liệu với một tên và giá trị phụ với các bản dịch.</span><span class="sxs-lookup"><span data-stu-id="f6197-112">Each term that you want to provide a translation for must be included in a data element with a name and a value child with the translation.</span></span>  
  
2. <span data-ttu-id="f6197-113">Lưu tệp này với các định danh ngôn ngữ trong tên tập tin.</span><span class="sxs-lookup"><span data-stu-id="f6197-113">Save the file with the language identifier in the file name.</span></span> <span data-ttu-id="f6197-114">For example, if you have Spanish resources, you can save the file with the name “TranslationResource.es.xml.”</span><span class="sxs-lookup"><span data-stu-id="f6197-114">For example, if you have Spanish resources, you can save the file with the name “TranslationResource.es.xml.”</span></span>  
  
3. <span data-ttu-id="f6197-115">Upload the file as a web resource to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="f6197-115">Upload the file as a web resource to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span> <span data-ttu-id="f6197-116">Đặt tên tài nguyên web do đó bạn có thể xác định ngôn ngữ của các nguồn tài nguyên chuỗi trong nó.</span><span class="sxs-lookup"><span data-stu-id="f6197-116">Name the web resource so that you can identify the language of the string resources in it.</span></span>  
  
   1. <span data-ttu-id="f6197-117">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="f6197-117">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
   2. <span data-ttu-id="f6197-118">Go to **Settings** > **Customizations** ([How do I get there?](http://go.microsoft.com/fwlink/p/?LinkId=525636))</span><span class="sxs-lookup"><span data-stu-id="f6197-118">Go to **Settings** > **Customizations** ([How do I get there?](http://go.microsoft.com/fwlink/p/?LinkId=525636))</span></span>  
  
   3. <span data-ttu-id="f6197-119">Bấm vào **tùy chỉnh hệ thống** để thêm các nguồn tài nguyên web vào các giải pháp mặc định.</span><span class="sxs-lookup"><span data-stu-id="f6197-119">Click **Customize the System** to add the web resources to the default solution.</span></span>  
  
   4. <span data-ttu-id="f6197-120">Trên trang **Giải pháp mặc định**, bấm vào **nguồn tài nguyên Web**, và sau đó nhấp vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="f6197-120">On the **Default Solution** page, click **Web Resources**, and then click **New**.</span></span>  
  
   5. <span data-ttu-id="f6197-121">On the new web resource page, specify the name of the web resource, select **Data (XML)** as the type, **English** as the language, and then select your .xml file.</span><span class="sxs-lookup"><span data-stu-id="f6197-121">On the new web resource page, specify the name of the web resource, select **Data (XML)** as the type, **English** as the language, and then select your .xml file.</span></span>  
  
   <span data-ttu-id="f6197-122">![New web resource](../unified-service-desk/media/usd-new-web-resource.PNG "New web resource")</span><span class="sxs-lookup"><span data-stu-id="f6197-122">![New web resource](../unified-service-desk/media/usd-new-web-resource.PNG "New web resource")</span></span>  
  
   6.  <span data-ttu-id="f6197-123">Lưu và xuất bản tài nguyên web của bạn.</span><span class="sxs-lookup"><span data-stu-id="f6197-123">Save and publish the web resource.</span></span>  
  
4. <span data-ttu-id="f6197-124">Sau khi xuất bản tài nguyên web cho tập tin tài nguyên ngôn ngữ của bạn, thêm nguồn tài nguyên web vào kiểm soát tổ chức **trình quản lý chung** của bạn.</span><span class="sxs-lookup"><span data-stu-id="f6197-124">After publishing the web resource for your language resource file, add the web resource to your **Global Manager** hosted control.</span></span>  
  
   1. <span data-ttu-id="f6197-125">On the nav bar, choose **Settings** > **Unified Service Desk** > **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="f6197-125">On the nav bar, choose **Settings** > **Unified Service Desk** > **Hosted Controls**.</span></span>  
  
   2. <span data-ttu-id="f6197-126">Click **Dynamics 365 for Customer Engagement apps Global Manager** under the **Name** column, or select the record, and click **Edit** on the command bar.</span><span class="sxs-lookup"><span data-stu-id="f6197-126">Click **Dynamics 365 for Customer Engagement apps Global Manager** under the **Name** column, or select the record, and click **Edit** on the command bar.</span></span>  
  
      > [!NOTE]
      > <span data-ttu-id="f6197-127">**Dynamics 365 for Customer Engagement apps Global Manager** is the name of the default **Global Manager** hosted control type in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="f6197-127">**Dynamics 365 for Customer Engagement apps Global Manager** is the name of the default **Global Manager** hosted control type in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="f6197-128">Nếu bạn có kiểm soát tổ chức trình quản lý chung với tên khác, hãy chọn tên đó để thay thế.</span><span class="sxs-lookup"><span data-stu-id="f6197-128">If you have a Global Manager hosted control with different name, select it instead.</span></span>  
  
   3. <span data-ttu-id="f6197-129">On the **Dynamics 365 for Customer Engagement apps Global Manager** page, under the **Language Services** area, click **+** to add a language module record.</span><span class="sxs-lookup"><span data-stu-id="f6197-129">On the **Dynamics 365 for Customer Engagement apps Global Manager** page, under the **Language Services** area, click **+** to add a language module record.</span></span>  
  
   <span data-ttu-id="f6197-130">![Add a language module](../unified-service-desk/media/usd-add-language-module.png "Add a language module")</span><span class="sxs-lookup"><span data-stu-id="f6197-130">![Add a language module](../unified-service-desk/media/usd-add-language-module.png "Add a language module")</span></span>  
  
   4.  <span data-ttu-id="f6197-131">Trên trang **Mô đun ngôn ngữ mới**, hãy chỉ định tên, LCID, và tên của các nguồn tài nguyên web có chứa các tập tin bản dịch.</span><span class="sxs-lookup"><span data-stu-id="f6197-131">On the **New Language Module** page, specify the name, LCID, and the name of the web resource that contains the translation file.</span></span>  
  
        <span data-ttu-id="f6197-132">LCID nên được xác định với một giá trị đại diện cho ngôn ngữ đó đại diện cho tài nguyên này.</span><span class="sxs-lookup"><span data-stu-id="f6197-132">The LCID should be populated with a value that represents the language that this resource represents.</span></span> <span data-ttu-id="f6197-133">[Xem danh sách ID các miền địa phương](https://msdn.microsoft.com/library/ms912047\(WinEmbedded.10\).aspx).</span><span class="sxs-lookup"><span data-stu-id="f6197-133">[View the list of locale IDs](https://msdn.microsoft.com/library/ms912047\(WinEmbedded.10\).aspx).</span></span>  
  
   <span data-ttu-id="f6197-134">![New language module](../unified-service-desk/media/usd-new-language-module.png "New language module")</span><span class="sxs-lookup"><span data-stu-id="f6197-134">![New language module](../unified-service-desk/media/usd-new-language-module.png "New language module")</span></span>  
  
   > [!IMPORTANT]
   >  <span data-ttu-id="f6197-135">If you use language services, you should always configure language services for your base [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps language.</span><span class="sxs-lookup"><span data-stu-id="f6197-135">If you use language services, you should always configure language services for your base [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps language.</span></span> <span data-ttu-id="f6197-136">Trong ví dụ này, cũng thêm một dịch vụ ngôn ngữ tiếng Anh.</span><span class="sxs-lookup"><span data-stu-id="f6197-136">In this example, add an English language service as well.</span></span> <span data-ttu-id="f6197-137">The base language translation file is always used if someone uses a language pack in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps that doesn’t have a translation file in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] language services.</span><span class="sxs-lookup"><span data-stu-id="f6197-137">The base language translation file is always used if someone uses a language pack in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps that doesn’t have a translation file in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] language services.</span></span>  
  
5. <span data-ttu-id="f6197-138">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="f6197-138">Click **Save**.</span></span>  
  
## <a name="use-the-translated-text"></a><span data-ttu-id="f6197-139">Sử dụng Văn bản Đã dịch</span><span class="sxs-lookup"><span data-stu-id="f6197-139">Use the translated text</span></span>  
 <span data-ttu-id="f6197-140">Để sử dụng văn bản dịch, tham khảo các mục bằng cách sử dụng một tham số thay thế, như được hiển thị ở đây.</span><span class="sxs-lookup"><span data-stu-id="f6197-140">To use the translated text, refer to the entry using a replacement parameter as shown here.</span></span>  
  
```xml  
[[$Resources.Welcome]]  
```  
  
 <span data-ttu-id="f6197-141">Điều này có thể được sử dụng bất cứ nơi nào mà bạn sử dụng một tham số thay thế và các tập tin bản dịch cũng có thể chứa tham số thay thế.</span><span class="sxs-lookup"><span data-stu-id="f6197-141">This can be used anywhere that you use a replacement parameter and the translation file may contain other replacement parameter as well.</span></span> <span data-ttu-id="f6197-142">Ngôn ngữ dịch sẽ được thay thế trước tiên và sau đó các thông số thay thế khác sẽ được áp dụng.</span><span class="sxs-lookup"><span data-stu-id="f6197-142">The language translation will be substituted first and then the other replacement parameters will be applied.</span></span> <span data-ttu-id="f6197-143">Chúng có thể được sử dụng cho tên của các nút, các văn bản của các mã lệnh tổng đài viên hoặc bất cứ nơi nào bạn có thể sử dụng tham số thay thế.</span><span class="sxs-lookup"><span data-stu-id="f6197-143">These can be used for names of buttons, text of agent scripts, or wherever you can use replacement parameters.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f6197-144">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="f6197-144">See also</span></span>  
 [<span data-ttu-id="f6197-145">Trình quản lý chung (Kiểm soát tổ chức)</span><span class="sxs-lookup"><span data-stu-id="f6197-145">Global Manager (Hosted Control)</span></span>](../unified-service-desk/global-manager-hosted-control.md)
