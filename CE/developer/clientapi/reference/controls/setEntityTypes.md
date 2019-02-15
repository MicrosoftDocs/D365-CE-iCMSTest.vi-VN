---
title: setEntityTypes (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 93154168-1e9f-4849-b4bb-be8804f86f81
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d27196d86060e348185bb242aef60994b319b9ec
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387522"
---
# <a name="setentitytypes-client-api-reference"></a>setEntityTypes (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Sets the types of entities allowed in the lookup control.

## <a name="control-types-supported"></a>Control types supported

Lookup control

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).setEntityTypes([entityLogicalNames]);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|entityLogicalNames|Array of String|Có|Specify the logical name of the entities allowed in the lookup control.|

### <a name="related-topics"></a>Chủ đề liên quan

[getEntityTypes](getEntityTypes.md)

 


