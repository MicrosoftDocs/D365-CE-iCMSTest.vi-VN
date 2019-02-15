---
title: getParent (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 6d77db1b-18b4-410f-b91b-d2b65b369946
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: dbbd7df380c002fdf2ab637401b8ea16ca54b575
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387011"
---
# <a name="getparent-client-api-reference"></a>getParent (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns the `formContext.data.entity` object that is the parent to all attributes. 

## <a name="attribute-types-supported"></a>Attribute types supported

Tất cả

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getParent()`

## <a name="return-value"></a>Giá trị trả lại

**Type**: `formContext.data.entity` object. 

**Description**: The parent object.

