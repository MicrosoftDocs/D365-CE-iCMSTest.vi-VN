---
title: getGlobalContext.userSettings (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 44296667-f1cd-49be-a300-7259bc3b41e0
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c5c897730b0247272335bec52eadacff1fe51787
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387237"
---
# <a name="getglobalcontextusersettings-client-api-reference"></a>getGlobalContext.userSettings (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns information about the current user settings.

`var userSettings = Xrm.Utility.getGlobalContext().userSettings`

The **userSettings** object provides following properties and a method.

## <a name="dateformattinginfo"></a>dateFormattingInfo 

Returns the date formatting information for the current user.

### <a name="syntax"></a>Cú pháp

`userSettings.dateFormattingInfo`

### <a name="return-value"></a>Giá trị trả lại

**Type**: Object

**Description**: An object with information about date formatting such as **FirstDayOfWeek**, **LongDatePattern**, **MonthDayPattern**, **TimeSeparator**, and so on.

## <a name="defaultdashboardid"></a>defaultDashboardId 

Returns the ID of the default dashboard for the current user.

### <a name="syntax"></a>Cú pháp

`userSettings.defaultDashboardId`

### <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: ID of the default dashboard. 

## <a name="isguidedhelpenabled"></a>isGuidedHelpEnabled 

Indicates whether guided help is enabled for the current user.

### <a name="syntax"></a>Cú pháp

`userSettings.isGuidedHelpEnabled`

### <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean

**Description**: true if enabled; false otherwise. 

## <a name="ishighcontrastenabled"></a>isHighContrastEnabled 

Indicates whether high contrast is enabled for the current user.

### <a name="syntax"></a>Cú pháp

`userSettings.isHighContrastEnabled`

### <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean

**Description**: true if enabled; false otherwise.

## <a name="isrtl"></a>isRTL 

Indicates whether the language for the current user is a right-to-left (RTL) language.

### <a name="syntax"></a>Cú pháp

`userSettings.isRTL`

### <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean

**Description**: true if it is RTL; false otherwise.

## <a name="languageid"></a>languageId 

Returns the language ID for the current user.

### <a name="syntax"></a>Cú pháp

`userSettings.languageId`

### <a name="return-value"></a>Giá trị trả lại

**Type**: Number

**Description**: Language ID.

## <a name="securityroleprivileges"></a>securityRolePrivileges 

Returns an array of strings that represent the GUID values of each of the security role privilege that the user is associated with or any teams that the user is associated with.

### <a name="syntax"></a>Cú pháp

`userSettings.securityRolePrivileges`

### <a name="return-value"></a>Giá trị trả lại

**Type**: Array

**Description**: GUID values of each of the security role privilege.

## <a name="securityroles"></a>securityRoles 

Returns an array of strings that represent the GUID values of each of the security role that the user is associated with or any teams that the user is associated with.

### <a name="syntax"></a>Cú pháp

`userSettings.securityRoles`

### <a name="return-value"></a>Giá trị trả lại

**Type**: Array

**Description**: GUID values of each of the security role. Ví dụ:

`["0d3dd20a-17a6-e711-a94e-000d3a1a7a9b", "ff42d20a-17a6-e711-a94e-000d3a1a7a9b"]`

## <a name="transactioncurrencyid"></a>transactionCurrencyId 

Returns the transaction currency ID for the current user.

### <a name="syntax"></a>Cú pháp

`userSettings.transactionCurrencyId`

### <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: Transaction currency ID.

## <a name="userid"></a>userId 

Returns the GUID of the **SystemUser.Id** value for the current user.

### <a name="syntax"></a>Cú pháp

`userSettings.userId`

### <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: The ID of the user. Ví dụ:

`"{75B5BA27-FD41-4D45-8E3A-C8446C95F0CC}"`

## <a name="username"></a>userName 

Returns the name of the current user.

### <a name="syntax"></a>Cú pháp

`userSettings.userName`

### <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: Name of the current user.

## <a name="gettimezoneoffsetminutes-method"></a>getTimeZoneOffsetMinutes method

Returns the difference in minutes between the local time and Coordinated Universal Time (UTC).

### <a name="syntax"></a>Cú pháp

`userSettings.getTimeZoneOffsetMinutes()`

### <a name="return-value"></a>Giá trị trả lại

**Type**: number

**Description**: Time zone offset in minutes.

## <a name="related-topics"></a>Chủ đề liên quan

[Client context](client.md)

[Organization settings](organizationSettings.md)

[Xrm.Utility.getGlobalContext](../getGlobalContext.md)

