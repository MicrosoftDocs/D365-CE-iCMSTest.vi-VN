---
title: Use HAT automation activities in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn how to use HAT automation activities to automate your hosted applications in Unified Service Desk.
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
ms.assetid: c9f6c498-68c8-4c67-9b89-c44ce39d6da1
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
ms.openlocfilehash: 38c8ce029e454f64afb393485950b1d561dc6f47
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385990"
---
# <a name="use-hat-automation-activities-in-unified-service-desk"></a><span data-ttu-id="7eb6d-103">Use HAT automation activities in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="7eb6d-103">Use HAT automation activities in Unified Service Desk</span></span>
<span data-ttu-id="7eb6d-104">[!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)] cung cấp cho bạn một loạt các hoạt động tự động hóa mà bạn có thể sử dụng để tự động hóa ứng dụng được lưu trữ của mình.</span><span class="sxs-lookup"><span data-stu-id="7eb6d-104">The [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)] provides you with a bunch of automation activities that you can use to automate your hosted applications.</span></span> <span data-ttu-id="7eb6d-105">Để xem các hoạt động tự động hóa [!INCLUDE[pn_hat](../includes/pn-hat.md)] trong [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)]:</span><span class="sxs-lookup"><span data-stu-id="7eb6d-105">To view the [!INCLUDE[pn_hat](../includes/pn-hat.md)] automation activities in [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)]:</span></span>  
  
1. <span data-ttu-id="7eb6d-106">Bắt đầu [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] và tạo Thư viện Hoạt động của Quy trình hoặc mở dự án Thư viện Hoạt động của Quy trình.</span><span class="sxs-lookup"><span data-stu-id="7eb6d-106">Start [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)], and create a Workflow Activity Library or open a Workflow Activity Library project.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="7eb6d-107">[Cách: Tạo Thư viện Hoạt động](https://msdn.microsoft.com/library/dd489393\(v=vs.110\).aspx)</span><span class="sxs-lookup"><span data-stu-id="7eb6d-107">[How to: Create an Activity Library](https://msdn.microsoft.com/library/dd489393\(v=vs.110\).aspx)</span></span>  
  
2. <span data-ttu-id="7eb6d-108">Nếu **Hộp công cụ** không hiển thị trong khu vực không gian làm việc, từ menu **Xem**, chọn **Hộp công cụ** để hiển thị.</span><span class="sxs-lookup"><span data-stu-id="7eb6d-108">If **Toolbox** is not visible in the workspace area, from the **View** menu, choose **Toolbox** to display it.</span></span>  
  
3. <span data-ttu-id="7eb6d-109">Trong **Hộp công cụ**, bấm chuột phải và chọn **Chọn Mục**.</span><span class="sxs-lookup"><span data-stu-id="7eb6d-109">In **Toolbox**, right-click and select **Choose Items**.</span></span>  
  
   <span data-ttu-id="7eb6d-110">![Select Choose Items in Toolbox](../unified-service-desk/media/usd-view-hat-activities-1.png "Select Choose Items in Toolbox")</span><span class="sxs-lookup"><span data-stu-id="7eb6d-110">![Select Choose Items in Toolbox](../unified-service-desk/media/usd-view-hat-activities-1.png "Select Choose Items in Toolbox")</span></span>  
  
4. <span data-ttu-id="7eb6d-111">In the **Choose Toolbox Items** dialog box, on the **System.Activities Components** tab, click **Browse** to locate and select the Microsoft.UII.HostedApplicationToolkit.Activity.dll file.</span><span class="sxs-lookup"><span data-stu-id="7eb6d-111">In the **Choose Toolbox Items** dialog box, on the **System.Activities Components** tab, click **Browse** to locate and select the Microsoft.UII.HostedApplicationToolkit.Activity.dll file.</span></span> <span data-ttu-id="7eb6d-112">The file is available in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client installation directory (typically, C:\Program Files\Microsoft Dynamics CRM USD\USD) or in the *<UII_SDK_Extracted_Folder>* \UII\Bin folder.</span><span class="sxs-lookup"><span data-stu-id="7eb6d-112">The file is available in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client installation directory (typically, C:\Program Files\Microsoft Dynamics CRM USD\USD) or in the *<UII_SDK_Extracted_Folder>* \UII\Bin folder.</span></span>  
  
5. <span data-ttu-id="7eb6d-113">After you select the Microsoft.UII.HostedApplicationToolkit.Activity.dll file, the [!INCLUDE[pn_hat](../includes/pn-hat.md)] automation activities appear selected in the **Choose Toolbox Items** dialog box.</span><span class="sxs-lookup"><span data-stu-id="7eb6d-113">After you select the Microsoft.UII.HostedApplicationToolkit.Activity.dll file, the [!INCLUDE[pn_hat](../includes/pn-hat.md)] automation activities appear selected in the **Choose Toolbox Items** dialog box.</span></span> <span data-ttu-id="7eb6d-114">Chọn **OK** để hiển thị chúng trong **Hộp công cụ**.</span><span class="sxs-lookup"><span data-stu-id="7eb6d-114">Choose **OK** to display them in **Toolbox**.</span></span>  
  
   <span data-ttu-id="7eb6d-115">![HAT automation activities](../unified-service-desk/media/usd-hat-automation-activities-selected.png "HAT automation activities")</span><span class="sxs-lookup"><span data-stu-id="7eb6d-115">![HAT automation activities](../unified-service-desk/media/usd-hat-automation-activities-selected.png "HAT automation activities")</span></span>  
  
6. <span data-ttu-id="7eb6d-116">Sử dụng các hoạt động tự động hóa [!INCLUDE[pn_hat](../includes/pn-hat.md)] từ **Thanh công cụ** để thiết kế quy trình làm việc của bạn.</span><span class="sxs-lookup"><span data-stu-id="7eb6d-116">Use the [!INCLUDE[pn_hat](../includes/pn-hat.md)] automation activities from **Toolbox** to design your workflow.</span></span>  
  
   <span data-ttu-id="7eb6d-117">![HAT automation activities in Toolbox](../unified-service-desk/media/usd-hat-automation-activities-toolbox.png "HAT automation activities in Toolbox")</span><span class="sxs-lookup"><span data-stu-id="7eb6d-117">![HAT automation activities in Toolbox](../unified-service-desk/media/usd-hat-automation-activities-toolbox.png "HAT automation activities in Toolbox")</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="7eb6d-118">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="7eb6d-118">See also</span></span>  
 <span data-ttu-id="7eb6d-119">[Automate hosted applications using HAT automation activities](../unified-service-desk/automate-hosted-applications-using-hat-automation-activities.md) </span><span class="sxs-lookup"><span data-stu-id="7eb6d-119">[Automate hosted applications using HAT automation activities](../unified-service-desk/automate-hosted-applications-using-hat-automation-activities.md) </span></span>  
 [<span data-ttu-id="7eb6d-120">Types of HAT automation activities</span><span class="sxs-lookup"><span data-stu-id="7eb6d-120">Types of HAT automation activities</span></span>](../unified-service-desk/types-of-hat-automation-activities.md)
