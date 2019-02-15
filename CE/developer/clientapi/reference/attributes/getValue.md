---
title: getValue (Client API reference)| MicrosoftDocs
ms.date: 10/16/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: acc78a1e-212a-4eef-88c5-8272f9ba3009
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9f25e7cc1b72c58dd02985652e533cc2c9c7bd5d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387229"
---
# <a name="getvalue-client-api-reference"></a>getValue (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Retrieves the data value for an attribute.

## <a name="attribute-types-supported"></a>Attribute types supported

Tất cả

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getValue()`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Depends on the type of attaribute. 

| Attribute Type | Return Type| 
|----|-----|
| boolean | [Boolean](https://msdn.microsoft.com/library/t7bkhaz6.aspx) |
| ngày giờ| [Date](https://msdn.microsoft.com/library/cd9w2te4.aspx)<br/> To get the string version of a date using the Microsoft Dynamics 365 for Customer Engagement app user’s locale preferences, use the [format](https://msdn.microsoft.com/library/bb384009.aspx) and [localeFormat](https://msdn.microsoft.com/library/bb383816.aspx) methods. Other methods will format dates using the operating system locale rather than the user’s Microsoft Dynamics 365 for Customer Engagement apps locale preferences. | 
| thập phân| [Number](https://msdn.microsoft.com/library/dwab3ed2.aspx)| 
| Gấp đôi | [Number](https://msdn.microsoft.com/library/dwab3ed2.aspx)| 
| số nguyên | [Number](https://msdn.microsoft.com/library/dwab3ed2.aspx)|
| lookup | [Mảng](https://msdn.microsoft.com/library/k4h76zbx.aspx) <br/>An array of lookup objects.<br/><br/>NOTE: Certain lookups allow for multiple records to be associated in a lookup, such as the To: field for an email entity record. Therefore, all lookup data values use an array of lookup objects – even when the lookup attribute does not support more than one record reference to be added. <br/><br/>Each lookup has the following properties:<br/>- *entityType*: String. The name of the entity displayed in the lookup.<br/>- *id*: String: The string representation of the GUID value for the record displayed in the lookup.<br/>- *name*: String: The text representing the record to be displayed in the lookup.|
| memo  | [Chuỗi](https://msdn.microsoft.com/library/ecczf11c.aspx)  |
| money| [Number](https://msdn.microsoft.com/library/dwab3ed2.aspx)  |
| optionset | [Number](https://msdn.microsoft.com/library/dwab3ed2.aspx)  |
| multiselectoptionset | Array of [Number](https://msdn.microsoft.com/library/dwab3ed2.aspx)  |
| chuỗi | [Chuỗi](https://msdn.microsoft.com/library/ecczf11c.aspx) |


### <a name="related-topic"></a>Related topic
[setValue (Client API reference)](setValue.md)
