---
title: close (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
ms.date: 12/04/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 1261a94d-4f5c-446d-8c29-a326e819696b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: bd5b03469ca5513c4052effffbbb5f3155b99c34
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386542"
---
# <a name="close-client-api-reference"></a>close (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/close-description.md](./includes/close-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.ui.close();`

## <a name="remarks"></a>Chú thích

The HTML **Window.close** method is suppressed. To close a form window, you must use this method. If there are any unsaved changes in the form, the user will be prompted whether they want to save their changes before the window closes.

For Microsoft Dynamics 365 for tablets, this method mimics the behavior of the back navigation button.

### <a name="related-topics"></a>Chủ đề liên quan

[formContext.ui](../formContext-ui.md)

[formContext](../../clientapi-form-context.md)

