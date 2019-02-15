---
title: showProgressIndicator (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 36e17a06-e381-4efd-b3a6-62391377b613
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 13a0367cf963552731f3ac0924328acab9bfe73f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385782"
---
# <a name="showprogressindicator-client-api-reference"></a>showProgressIndicator (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/showProgressIndicator-description.md](./includes/showProgressIndicator-description.md)]

Any subsequent call to this method will update the displayed message in the existing progress dialog with the message specified in the latest method call.

>[!WARNING]
>The progress dialog blocks the UI until it is closed using the [closeProgressIndicator](closeProgressIndicator.md) method. So, you must use this method with caution.

## <a name="syntax"></a>Cú pháp

`Xrm.Utility.showProgressIndicator(message)`

## <a name="parameters"></a>Tham số 

|Tên |Loại |Bắt buộc |Mô tả |
|---|---|---|---|
|message|Chuỗi|Có|The message to be displayed in the progress dialog.|



### <a name="related-topics"></a>Chủ đề liên quan

[closeProgressIndicator](closeProgressIndicator.md)

[Xrm.Utility](../xrm-utility.md)  



