---
title: NextRole Tag Unified Service Desk for Dynamics 365 for Customer Engagement apps Customer Enagagement| MicrosoftDocs
description: " Mẫu sau đây tìm thấy một kiểm soát cách một vị trí sau kiểm soát thứ hai với vai trò nút nhấn. "
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
ms.assetid: a76c84f2-fee6-4fd8-bbd2-0720b50b46ad
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
ms.openlocfilehash: ec3bd6c9ed59634d32e45ec6faef31fe3c040358
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387623"
---
# <a name="nextrole-tag-unified-service-desk"></a>NextRole Tag Unified Service Desk
Thẻ `<NextRole>` hoạt động như thẻ `<Next>` nhưng áp dụng cho vai trò khả năng tiếp cận của kiểm soát. Các thuộc tính của thẻ này giống như thẻ `<Next>`. The following sample finds a control one position after the second control with a push button role.  
  
```xml  
<JAccControl name="TestButton">  
<Path>  
<NextRole match="2"offset="1">push button</NextRole>  
</Path>  
</JAccControl>  
  
```  
  
### <a name="see-also"></a>Xem thêm  
 [JavaDDA](../unified-service-desk/javadda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
