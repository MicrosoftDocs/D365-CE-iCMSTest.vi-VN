---
title: reflow (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 6833e4ea-70fc-4ee0-8aab-68cc55e21444
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 82b50e5d5fe2803c4115bb4658863caa72020779
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388592"
---
# <a name="reflow-client-api-reference"></a>reflow (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/reflow-description.md](./includes/reflow-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.ui.process.reflow(updateUI, parentStage, nextStage);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|updateUI|Boolean|Có|Specify **true** to update the UI of the process control; **false** otherwise.|
|parentStage|Chuỗi|Có|Specify the ID of the parent stage in the GUID format.|
|nextStage|Chuỗi|Có|Specify the ID of the next stage in the GUID format.|

### <a name="related-topics"></a>Chủ đề liên quan

[formContext.ui.process](../formContext-ui-process.md)



