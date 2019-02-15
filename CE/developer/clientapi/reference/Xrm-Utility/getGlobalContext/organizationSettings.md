---
title: getGlobalContext.organizationSettings (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: badf4f82-cb47-4864-aa43-bb777d04de4d
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 33e1eb7088e5c592b1824cab5275f8299c86bc96
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387530"
---
# <a name="getglobalcontextorganizationsettings-client-api-reference"></a>getGlobalContext.organizationSettings (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns information about the current organization settings. 

`var organizationSettings = Xrm.Utility.getGlobalContext().organizationSettings`

The **organizationSettings** object provides following properties.

## <a name="attributes"></a>attributes

Returns attributes and their values as `key:value` pairs that are available for the organization entity. Additional values will be available as attributes if they are specified as attribute dependencies in the web resource dependency list. The `key` will be the attribute logical name.

### <a name="syntax"></a>Cú pháp

`organizationSettings.attributes`

### <a name="return-value"></a>Giá trị trả lại

**Type**: Object

**Description**: An object with attributes and their values.

## <a name="basecurrencyid"></a>baseCurrencyId 

Returns the ID of the base currency for the current organization.

### <a name="syntax"></a>Cú pháp

`organizationSettings.baseCurrencyId`

### <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: ID of the base currency.

## <a name="defaultcountrycode"></a>defaultCountryCode 

Returns the default country/region code for phone numbers for the current organization.

### <a name="syntax"></a>Cú pháp

`organizationSettings.defaultCountryCode`

### <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: Default country/region code for phone numbers.

## <a name="isautosaveenabled"></a>isAutoSaveEnabled 

Indicates whether the auto-save option is enabled for the current organization.

### <a name="syntax"></a>Cú pháp

`organizationSettings.isAutoSaveEnabled`

### <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean

**Description**: **true** if enabled; **false** otherwise.

## <a name="languageid"></a>languageId 

Returns the preferred language ID for the current organization.

### <a name="syntax"></a>Cú pháp

`organizationSettings.languageId`

### <a name="return-value"></a>Giá trị trả lại

**Type**: Number

**Description**: Preferred Language ID. Ví dụ:

`1033`

## <a name="organizationid"></a>organizationId 

Returns the ID of the current organization.

### <a name="syntax"></a>Cú pháp

`organizationSettings.organizationId`

### <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: Id of the current organization.

## <a name="uniquename"></a>uniqueName 

Returns the unique name of the current organization.

### <a name="syntax"></a>Cú pháp

`organizationSettings.uniqueName`

### <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: Unique name of the current organization.

## <a name="useskypeprotocol"></a>useSkypeProtocol 

Indicates whether the Skype protocol is used for the current organization.

### <a name="syntax"></a>Cú pháp

`organizationSettings.useSkypeProtocol`

### <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean

**Description**: **true** if Skype protocol is used; **false** otherwise.


## <a name="related-topics"></a>Chủ đề liên quan

[Client context](client.md)

[Cài đặt người dùng](userSettings.md)

[Xrm.Utility.getGlobalContext](../getGlobalContext.md)
