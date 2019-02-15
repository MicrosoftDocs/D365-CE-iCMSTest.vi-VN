---
title: getIsDirty (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 93908c95-c813-4f55-9d19-8fd27a0126d7
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 978dd3c54fa74fb23a4aaa59274d061331e8cefc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386119"
---
# <a name="getisdirty-client-api-reference"></a>getIsDirty (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getIsDirty-description.md](./includes/getIsDirty-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.data.entity.getIsDirty();`

## <a name="return-type"></a>Return Type

**Type**: Boolean

**Description**: true if any fields in the form have been changed; false otherwise.

### <a name="related-topics"></a>Chủ đề liên quan

[formContext.data.getIsDirty](../formContext-data/getIsDirty.md)

[formContext](../../clientapi-form-context.md)

