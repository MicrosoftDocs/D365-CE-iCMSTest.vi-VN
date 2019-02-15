---
title: save (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 03e970ee-7ed3-4df2-9670-222d76a479fd
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 30d37713624e3d3c8338697650867fb6e34a4016
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386155"
---
# <a name="save-client-api-reference"></a>save (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/save-description.md](./includes/save-description.md)]

You can also set an object to control how appointment, recurring appointment, or service activity records are processed.

## <a name="syntax"></a>Cú pháp

`formContext.data.save(saveOptions).then(successCallback, errorCallback);`

## <a name="parameters"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|saveOptions|Đối tượng|Không|An object for specifying options for saving the record. Đối tượng có các thuộc tính sau đây:<br/><br/>- **saveMode**: (Optional) Number. Specify a value indicating how the save event was initiated. For a list of supported values, see the return value of the [getSaveMode](../save-event-arguments/getsavemode.md) method. Note that setting the **saveMode** does not actually take the corresponding action; it is just to provide information to the **OnSave** event handlers about the reason for the save operation.<br/><br/>- **useSchedulingEngine**: (Optional) Boolean. Indicate whether to use the **Book** or **Reschedule** messages rather than the **Create** or **Update** messages. This option is only applicable when used with appointment, recurring appointment, or service activity records.|
|successCallback|Hàm|Không|A function to call when the operation succeeds.|
|errorCallback|Hàm|Không|A function to call when the operation fails. An object with the following properties will be passed:<br/><br/>- **errorCode**: Number. The error code.<br/><br/>- **message**: String. A localized error message.|


### <a name="related-topics"></a>Chủ đề liên quan

[formContext.data.entity.save](../formContext-data-entity/save.md)

[formContext](../../clientapi-form-context.md)

