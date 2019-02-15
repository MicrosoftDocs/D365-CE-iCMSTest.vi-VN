---
title: getControlType (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 72d6c761-bcc7-4de6-b73f-5f2833297825
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3489f8ec12d193c3a20289fc4966e9189ab6e78b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387345"
---
# <a name="getcontroltype-client-api-reference"></a>getControlType (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getControlType-description.md](./includes/getControlType-description.md)]

## <a name="syntax"></a>Cú pháp

`quickViewControl.getControlType();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: String.

**Description**: For a quick view control, the method returns "quickform". 

For a constituent control in a quick view control, the method returns the actual category of the control. For more information about possible return values, see [getControlType](../controls/getControlType.md)..

### <a name="related-topics"></a>Chủ đề liên quan

[formContext.ui.quickForms](../formContext-ui-quickForms.md)
