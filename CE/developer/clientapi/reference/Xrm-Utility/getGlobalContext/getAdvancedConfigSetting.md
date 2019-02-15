---
title: getAdvancedConfigSetting (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: 6eceb6e623b9bba2d59eb9c6a8a1acd57a019e08
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388796"
---
# <a name="getadvancedconfigsetting-client-api-reference"></a>getAdvancedConfigSetting (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns information about the advanced configuration settings for the organization. 

## <a name="syntax"></a>Cú pháp

```JavaScript
var globalContext = Xrm.Utility.getGlobalContext();
globalContext.getAdvancedConfigSetting(setting);
```

## <a name="parameters"></a>Tham số

|Tên |Loại |Bắt buộc |Mô tả |
|---|---|---|---|
|setting |Chuỗi |Có |Name of the configuration setting. <br/>Only the following two configuration settings are supported: **"MaxChildIncidentNumber"** and **"MaxIncidentMergeNumber"** |

## <a name="return-value"></a>Giá trị trả lại

Returns the advanced configuration setting value.

### <a name="related-topics"></a>Chủ đề liên quan

[Xrm.Utility.getGlobalContext](../getGlobalContext.md)



