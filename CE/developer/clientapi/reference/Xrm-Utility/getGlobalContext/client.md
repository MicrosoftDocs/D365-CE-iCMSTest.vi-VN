---
title: getGlobalContext.client (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 89123cde-7c66-4c7d-94e4-e287285019f8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 697ab7190ff4e131e40c3a5a09803fd333cd0883
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388715"
---
# <a name="getglobalcontextclient-client-api-reference"></a>getGlobalContext.client (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

Provides access to the methods to determine which client is being used, whether the client is connected to the server, and what kind of device is being used.

`var clientContext = Xrm.Utility.getGlobalContext().client`

The following methods are available for the client context.

## <a name="getclient"></a>getClient

Returns a value to indicate which client the script is executing in. 

### <a name="syntax"></a>Cú pháp

`clientContext.getClient()`

### <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: The values returned are:

Value |Máy khách | 
|---|---|
|Web |Web application|
|Web |Giao diện Hợp nhất|
|Outlook |Outlook |
|Di động |Ứng dụng di động |

## <a name="getclientstate"></a>getClientState

Returns a value to indicate the state of the client.

### <a name="syntax"></a>Cú pháp

`clientContext.getClientState()`

### <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: The values returned are:

Value |Máy khách | 
|---|---|
|Trực tuyến |Web application, Outlook, Mobile app, Unified Interface|
|Offline |Outlook, Mobile app|

## <a name="getformfactor"></a>getFormFactor

Returns information about the kind of device the user is using.

### <a name="syntax"></a>Cú pháp

`clientContext.getFormFactor()`

### <a name="return-value"></a>Giá trị trả lại

**Type**: Number

**Description**: The values returned are:

Value |Nhân tố biểu mẫu | 
|---|---|
|0 |Unknown|
|1 |Desktop|
|2 |Máy tính bảng |
|3 |Số điện thoại |

## <a name="isoffline"></a>isOffline

Returns information whether the server is online or offline.

### <a name="syntax"></a>Cú pháp

`clientContext.isOffline()`

### <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean

**Description**: **true** if the server is offline; **false** otherwise.

## <a name="related-topics"></a>Chủ đề liên quan

[Organization Settings](organizationSettings.md)

[Thiết đặt người dùng](userSettings.md)

[Xrm.Utility.getGlobalContext](../getGlobalContext.md)

