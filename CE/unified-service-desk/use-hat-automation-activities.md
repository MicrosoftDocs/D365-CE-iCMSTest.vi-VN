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
# <a name="use-hat-automation-activities-in-unified-service-desk"></a>Use HAT automation activities in Unified Service Desk
[!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)] cung cấp cho bạn một loạt các hoạt động tự động hóa mà bạn có thể sử dụng để tự động hóa ứng dụng được lưu trữ của mình. Để xem các hoạt động tự động hóa [!INCLUDE[pn_hat](../includes/pn-hat.md)] trong [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)]:  
  
1. Bắt đầu [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] và tạo Thư viện Hoạt động của Quy trình hoặc mở dự án Thư viện Hoạt động của Quy trình. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Cách: Tạo Thư viện Hoạt động](https://msdn.microsoft.com/library/dd489393\(v=vs.110\).aspx)  
  
2. Nếu **Hộp công cụ** không hiển thị trong khu vực không gian làm việc, từ menu **Xem**, chọn **Hộp công cụ** để hiển thị.  
  
3. Trong **Hộp công cụ**, bấm chuột phải và chọn **Chọn Mục**.  
  
   ![Select Choose Items in Toolbox](../unified-service-desk/media/usd-view-hat-activities-1.png "Select Choose Items in Toolbox")  
  
4. In the **Choose Toolbox Items** dialog box, on the **System.Activities Components** tab, click **Browse** to locate and select the Microsoft.UII.HostedApplicationToolkit.Activity.dll file. The file is available in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client installation directory (typically, C:\Program Files\Microsoft Dynamics CRM USD\USD) or in the *<UII_SDK_Extracted_Folder>* \UII\Bin folder.  
  
5. After you select the Microsoft.UII.HostedApplicationToolkit.Activity.dll file, the [!INCLUDE[pn_hat](../includes/pn-hat.md)] automation activities appear selected in the **Choose Toolbox Items** dialog box. Chọn **OK** để hiển thị chúng trong **Hộp công cụ**.  
  
   ![HAT automation activities](../unified-service-desk/media/usd-hat-automation-activities-selected.png "HAT automation activities")  
  
6. Sử dụng các hoạt động tự động hóa [!INCLUDE[pn_hat](../includes/pn-hat.md)] từ **Thanh công cụ** để thiết kế quy trình làm việc của bạn.  
  
   ![HAT automation activities in Toolbox](../unified-service-desk/media/usd-hat-automation-activities-toolbox.png "HAT automation activities in Toolbox")  
  
### <a name="see-also"></a>Xem thêm  
 [Automate hosted applications using HAT automation activities](../unified-service-desk/automate-hosted-applications-using-hat-automation-activities.md)   
 [Types of HAT automation activities](../unified-service-desk/types-of-hat-automation-activities.md)
