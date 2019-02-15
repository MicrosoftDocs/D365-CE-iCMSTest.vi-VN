---
title: getIsDirty (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 5f75ecae-a946-47a0-b748-96525b556f31
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7152fd5cd6f0e792d5df1f30ed1d6ff5c7535979
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386739"
---
# <a name="getisdirty-client-api-reference"></a>getIsDirty (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns a Boolean value indicating if there are unsaved changes to the attribute value. 

## <a name="attribute-types-supported"></a>Attribute types supported

Tất cả

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getIsDirty()`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean. 

**Description**: True if there are unsaved changes, otherwise false.
