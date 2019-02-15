---
title: getActiveProcess (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: a977a250-b79f-4c88-a6af-776350b110f7
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7f8266d7beb146fe0c452b135b44bd2174e0fbbb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386392"
---
# <a name="getactiveprocess-client-api-reference"></a>getActiveProcess (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getActiveProcess-description.md](./includes/getActiveProcess-description.md)]

## <a name="syntax"></a>Cú pháp

`var activeProcess = formContext.data.process.getActiveProcess();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Process. 

**Description**: The currently active process. See [Process methods](../../formContext-data-process.md#process-methods) for the methods to access the properties of the process returned.

### <a name="related-topics"></a>Chủ đề liên quan

[setActiveProcess)](setActiveProcess.md)

[formContext.data.process](../../formContext-data-process.md)
 


