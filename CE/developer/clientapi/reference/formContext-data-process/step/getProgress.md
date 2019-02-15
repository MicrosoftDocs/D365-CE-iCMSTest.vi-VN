---
title: getProgress (Client API reference) in Dynamics 365 for Customer Engagement apps| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 56502c8b-af23-40d1-ad97-e780bb757d6d
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 680b559cee804c3be60b5677897f85908a8572f1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386161"
---
# <a name="getprogress-client-api-reference"></a>getProgress (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getProgress-description.md](./includes/getProgress-description.md)]

## <a name="syntax"></a>Cú pháp

`var stepProgress = stepObj.getProgress();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Number. 

**Description**: Returns one of the following values:

|Value |Mô tả|
|--|--|
|0|Không có|
|1|Processing|
|2|Đã hoàn thành|
|3|Failure|
|4|Invalid|

## <a name="remarks"></a>Chú thích

This method is supported only for the action steps; not for the data steps. Action steps are buttons on the business process stages that users can click to trigger an on-demand workflow or action. Action step is a preview feature introduced in the [!INCLUDE[pn_crm_9_0_0_online](../../../../../includes/pn-crm-9-0-0-online.md)] release. More information: See the **Business Process Flow automation with Action Steps** section in [Blog: New automation and visualization features for Business Process Flows (public preview)](https://blogs.msdn.microsoft.com/crm/2017/10/25/new-automation-and-visualization-features-for-business-process-flows-public-preview/)

### <a name="related-topics"></a>Chủ đề liên quan

[setProgress](setprogress.md)

[formContext.data.process](../../formContext-data-process.md)