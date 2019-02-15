---
title: getEntityTypes (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: c20ba958-821f-4168-a518-e39431603b28
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 98e1a172f5bb21f9b24c58bbe0a158ed22e940be
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387444"
---
# <a name="getentitytypes-client-api-reference"></a>getEntityTypes (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Gets the types of entities allowed in the lookup control. 

## <a name="control-types-supported"></a>Control types supported

Lookup control

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).getEntityTypes();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Array of String

**Description**: The logical names of the entities allowed in this control.

### <a name="related-topics"></a>Chủ đề liên quan

[setEntityTypes](setEntityTypes.md)
