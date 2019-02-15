---
title: How hierarchical security can be used to control access to entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Provides an additional, more granular security model for accessing records in a hierarchical organizational structure.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 61ec481c-c128-498b-a784-16fe11af424b
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 97352c1f0e86762f26d3de31f2f83f38cc65d992
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387874"
---
# <a name="how-hierarchical-security-can-be-used-to-control-access-to-entities"></a>How hierarchical security can be used to control access to entities

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

Hierarchy security offers a more granular access to records for an organization and helps to bring the maintenance costs down. Ví dụ, trong các tình huống phức tạp, bạn có thể bắt đầu với việc tạo ra một số đơn vị kinh doanh và sau đó thêm an ninh hệ thống phân cấp. Điều này sẽ đạt được một truy cập vào dữ liệu chi tiết hơn với ít chi phí bảo trì thấp hơn nhiều chi phí số lớn các đơn vị kinh doanh có thể yêu cầu. The hierarchy security model is an extension to the earlier security models that use business units, security roles, sharing, and teams. Nó có thể được sử dụng kết hợp với tất cả các mô hình bảo mật hiện tại.  
  
 Previously, implementing this kind of security often required developers to mimic this behavior using custom plug-ins. Now, with the hierarchy security model, that type of security is built into the  product. This removes the need to create and update custom plug-ins.  
  
 For a detailed description of the hierarchy security model, see [Security concepts for Microsoft Dynamics 365 for Customer Engagment apps](https://technet.microsoft.com/library/hh699698.aspx) in the [!INCLUDE[pn_crm_2015_ig](../../includes/pn-crm-2015-ig.md)] for Customer Engagement apps documentation.  
  
 [Video: Hierarchical Security Modelling in Microsoft Dynamics CRM 2015](http://youtu.be/kx5So32DrCo)  
  
## <a name="position-hierarchy"></a>hệ thống cấp bậc vị trí  
 Administrators can define various job positions in the organization and arrange them in the position hierarchy. You can add users to any given position or “tag” a user with a particular position. A user can be tagged only with one position in a given hierarchy; however, a position can be used for multiple users. Người dùng tại các vị trí cao hơn trong hệ thống có quyền truy cập vào dữ liệu của những người sử dụng tại các vị trí thấp hơn, trong đường dẫn tổ tiên trực tiếp. The direct higher positions have Read, Write, Update, Append, and AppendTo access to the lower positions’ data in the direct ancestor path. The non-direct higher positions have read-only access to the lower positions’ data in the direct ancestor path.  
  
 With the position hierarchy security, a user at a higher position has access to the records owned by a lower position user or by the team that a user is a member of, and to the records that are directly shared to the user or the team that a user is a member of. In addition to the position hierarchy security model, the users at a higher level must have at least the user level Read privilege on an entity to see the records that the users at the lower positions have access to. For example, if a user at a higher level doesn’t have the Read access to the `Case` entity, that user won’t be able to see the cases that the users at a lower positions have access to.  
  
 As a developer, you can implement a position hierarchy by using the **Position** entity.  
  
 Two new privileges have been added that are related to the position hierarchy feature as shown in the table below.  
  
|Đặc quyền|Mô tả|  
|---------------|-----------------|  
|prvAssignPosition|Assign a position to a system user.|  
|prvWriteHierarchicalSecurityConfiguration|Change hierarchy security settings.|  
  
 For more information about the `Position` entity and its messages, see [Position Entity](../entities/position.md).  
  
### <a name="see-also"></a>Xem thêm  
 [Video: Hierarchical Security Modelling in Microsoft Dynamics CRM 2015](http://youtu.be/kx5So32DrCo)   
 [The Security Model of Microsoft Dynamics 365 for Customer Engagement apps](security-model.md)   
 [Security concepts for Microsoft Dynamics 365 for Customer Engagement apps](https://technet.microsoft.com/library/hh699698.aspx) [Position Entity](../entities/position.md)
