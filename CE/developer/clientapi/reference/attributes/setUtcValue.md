---
title: setUtcValue (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: e7f770ac-ee19-46dd-babb-44127c299411
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 475a48599ce1913e20db61ff244daef658e6d0ff
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386712"
---
# <a name="setutcvalue-client-api-reference"></a>setUtcValue (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Sets a UTC date and time value for a **datetime** type of attribute. UTC stands for Coordinated Universal Time.

> [!NOTE]
> Attributes on quick create forms won't save values set using this method. 

## <a name="attribute-types-supported"></a>Attribute types supported

ngày giờ

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).setUtcValue(value)`

## <a name="parameters"></a>Tham số

**Type**: datetime. 

**Description**: The UTC date and time value.

### <a name="related-topic"></a>Related topic
[getUtcValue (Client API reference)](getUtcValue.md)

