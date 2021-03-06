---
title: lookupObjects (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 89123cde-7c66-4c7d-94e4-e287285019f8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6458207f70426a4a501b002be7b4b0a5f0bfda53
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385783"
---
# <a name="lookupobjects-client-api-reference"></a>lookupObjects (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/lookupObjects-description.md](./includes/lookupObjects-description.md)] 

## <a name="syntax"></a>Cú pháp

`Xrm.Utility.lookupObjects(lookupOptions).then(successCallback, cancelCallback)`

## <a name="parameters"></a>Tham số

**lookupOptions**: Object. Defines the options for opening the lookup dialog. Has the following properties:

|Property Name |Loại |Bắt buộc |Mô tả |
|---|---|---|---|
|allowMultiSelect|Boolean|Không|Indicates whether the lookup allows more than one item to be selected.|
|defaultEntityType|Chuỗi|Không|The default entity type to use.|
|defaultViewId|Chuỗi|Không|The default view to use.|
|entityTypes|Mảng|Không|The entity types to display.|
|showBarcodeScanner|Boolean|Không|Indicates whether the lookup control should show the barcode scanner in mobile clients.|
|viewIds|Mảng|Không|The views to be available in the view picker. Only system views are supported.|
|successCallback |Hàm |Có |A function to call when the lookup control is invoked. An object with the following properties is passed:<br/>- **entityType**: String. Entity type of the record selected in the lookup control.<br/>- **id**: String. ID of the record selected in the lookup control.<br/>- **name**: String. Name of the record selected in the lookup control.|
|errorCallback |Hàm |Có |A function to call when you cancel the lookup control or the operation fails.  |


### <a name="related-topics"></a>Chủ đề liên quan

[Xrm.Utility](../xrm-utility.md)
