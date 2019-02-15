---
title: Add a UII action to a hosted control | MicrosoftDocs
description: Learn about adding User Interface Integration (UII) actions to a hosted control type to provide new functionality.
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
ms.assetid: 0e082c56-76b8-405e-98ae-1d33802a19d0
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
ms.openlocfilehash: 9b36280b998feee417cae704d1738eb37a51b6ec
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386936"
---
# <a name="add-a-uii-action-to-a-hosted-control"></a>Add a UII action to a hosted control
Khi phiên bản mới của [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] được phát triển, các hành động [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] mới có thể được thêm vào loại kiểm soát tổ chức để cung cấp chức năng mới. Tuy nhiên, các hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] mới cho loại tổ chức kiểm soát sẽ chỉ khả dụng ngay mà không cần kích hoạt cho các phiên bản mới của loại kiểm soát tổ chức. Nếu bạn có các phiên bản hiện có của loại kiểm soát được lưu trữ trong cấu hình của bạn, hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] mới sẽ không khả dụng theo mặc định. Bạn sẽ phải thêm hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] theo cách thủ công vào hồ sơ kiểm soát tổ chức (phiên bản) để có thể sử dụng hành động trong cuộc gọi hành động của bạn.  
  
> [!NOTE]
>  Bạn phải thêm theo cách thủ công hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] vào phiên bản kiểm soát tổ chức chỉ khi hành động đó được hỗ trợ cho loại phiên bản kiểm soát tổ chức. Nếu không, hành động sẽ không hoạt động cho phiên bản kiểm soát tổ chức.  
  
 Để thêm một hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] vào phiên bản kiểm soát tổ chức hiện có:  
  
1. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
2. Bấm **Kiểm soát Tổ chức**.  
  
3. Tìm kiếm hồ sơ kiểm soát tổ chức mà bạn muốn thêm hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] vào đó, sau đó bấm vào tên kiểm soát tổ chức để mở định nghĩa.  
  
4. Trên trang định nghĩa kiểm soát tổ chức, bấm vào mũi tên bên cạnh tên kiểm soát tổ chức, rồi bấm vào **Hành động UII**.  
  
5. Bấm vào **Thêm Hoạt động UII mới**.  
  
6. Trên trang **Hành động UII Mới**, chỉ định tên của hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] trong trường **Tên** rồi bấm vào **Lưu và Đóng**. Bạn không phải chỉ định bất kỳ giá trị nào khác trên trang này.  
  
   ![Add a UII action to a hosted control](../unified-service-desk/media/usd-new-uii-action-hc.png "Add a UII action to a hosted control")  
  
    Hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] mới được thêm vào phiên bản kiểm soát tổ chức và có thể được sử dụng trong các cuộc gọi hành động của bạn.  
  
### <a name="see-also"></a>Xem thêm  
 [Create an action call for a UII action](../unified-service-desk/create-action-call-uii-action.md)   
 [Manage hosted controls, actions, and events](../unified-service-desk/manage-hosted-controls-actions-events.md)
