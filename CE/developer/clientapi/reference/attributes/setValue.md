---
title: setValue (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 1324b465-6012-47d4-bf35-837df82014cb
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9de9789077e9b64d3ff34327c9771e11a6b47174
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385535"
---
# <a name="setvalue-client-api-reference"></a>setValue (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Sets the data value for an attribute. 

## <a name="attribute-types-supported"></a>Attribute types supported

Tất cả

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).setValue(value)`

# <a name="parameters"></a>Tham số
Depends on the type of attribute.

| Attribute Type|Parameters Type|
-------|------|
| boolean| [Boolean](https://msdn.microsoft.com/library/t7bkhaz6.aspx) |
| ngày giờ|[Date](https://msdn.microsoft.com/library/cd9w2te4.aspx)|
| thập phân| [Number](https://msdn.microsoft.com/library/dwab3ed2.aspx)|
| double| [Number](https://msdn.microsoft.com/library/dwab3ed2.aspx) |
| Số nguyên|[Number](https://msdn.microsoft.com/library/dwab3ed2.aspx)|
| lookup  | [Array](https://msdn.microsoft.com/library/k4h76zbx.aspx) An array of lookup objects. <br/><br/>Certain lookups, known as ‘partylist’ lookups, allow for multiple records to be associated in a lookup, such as the **To:** field for an email entity record. Therefore, all lookup data values use an array of lookup objects – even when the lookup attribute does not support more than one record reference to be added.<br/><br/>Each lookup has the following properties:<br/>- *entityType*: String. The name of the entity displayed in the lookup.<br/>- *id*: String: The string representation of the GUID value for the record displayed in the lookup. The value should match the following format: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}<br/>- *name*: String: The text representing the record to be displayed in the lookup.|
| memo  | [Chuỗi](https://msdn.microsoft.com/library/ecczf11c.aspx)  |
| money| [Number](https://msdn.microsoft.com/library/dwab3ed2.aspx)  |
| optionset | [Number](https://msdn.microsoft.com/library/dwab3ed2.aspx)  |
| chuỗi | [Chuỗi](https://msdn.microsoft.com/library/ecczf11c.aspx)|
| memo | [Chuỗi](https://msdn.microsoft.com/library/ecczf11c.aspx)|
| money|[Number](https://msdn.microsoft.com/library/dwab3ed2.aspx)|
| optionset, multiselectoptionset|[Number](https://msdn.microsoft.com/library/dwab3ed2.aspx)<br/><br/>The [getOptions](getOptions.md) method returns option values as strings. You must use [parseInt](https://msdn.microsoft.com/library/x53yedee.aspx) to convert them to numbers before you can use those values to set the value of an optionset attribute. Valid statuscode (Status Reason) options depend on the current statecode of the record. The statecode (Status) field cannot be set in form scripts. To understand which statecode values are valid, refer to the metadata for the attributes. <!-- See [Default status and status reason values](../../../customize/default-status-and-status-reason-values.md) for a list of default values for system entities. --> For custom entities use the Entity Metadata browser. Finally, also consider any custom state transitions that have been applied to the field. More information: [Define status reason transitions](../../../../customize/define-status-reason-transitions.md).| 
| Chuỗi| [Chuỗi](https://msdn.microsoft.com/library/ecczf11c.aspx) <br/><br/> A String field with the email format requires that the string represents a valid email address.|


> [!NOTE]
> Updating an attribute using **setValue** will not cause the **OnChange** event handlers to run. If you want the **OnChange** event handlers to run you must use [fireOnChange](../attributes/fireOnChange.md) in addition to **setValue**. <br/><br/>
When Microsoft Dynamics 365 for Customer Engagement  apps for tablets is not connected to the server, **setValue** will not work.<br/><br/>You cannot set the value of composite attributes. More information: [Write scripts for composite attributes](../composite-attributes.md).

### <a name="related-topic"></a>Related topic
[getValue (Client API reference)](getValue.md)
