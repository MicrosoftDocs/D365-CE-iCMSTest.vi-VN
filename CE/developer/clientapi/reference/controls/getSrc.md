---
title: getSrc (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: e003d21f-393a-4681-a6fc-256949167fcc
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a5e2893d5da10fef03122412dfbc3262479aa242
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385843"
---
# <a name="getsrc-client-api-reference"></a>getSrc (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns the current URL being displayed in an IFRAME or web resource. 

## <a name="control-types-supported"></a>Control types supported

iframe, webresource

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).getSrc();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: A URL representing the **src** property of the IFRAME or web resource.

### <a name="related-topics"></a>Chủ đề liên quan

[setSrc](setSrc.md)

