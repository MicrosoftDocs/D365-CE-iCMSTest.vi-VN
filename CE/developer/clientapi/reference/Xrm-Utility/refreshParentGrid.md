---
title: refreshParentGrid (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: 57d2bdf660937baa83d3bbc6a59ba2ddcef10732
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386430"
---
# <a name="refreshparentgrid-client-api-reference"></a>refreshParentGrid (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/refreshParentGrid-description.md](./includes/refreshParentGrid-description.md)] 

## <a name="syntax"></a>Cú pháp

`Xrm.Utility.refreshParentGrid(lookupOptions)`

## <a name="parameters"></a>Tham số

**lookupOptions**: An object with the following properties to specify the record:

|Property Name |Loại |Bắt buộc  |Mô tả |
|---|---|---|---|
|entityType|Chuỗi|Có |Entity type of the record.|
|ID|Chuỗi|Có |ID of the record.|
|tên|Chuỗi|Không |Name of the record.|

### <a name="related-topics"></a>Chủ đề liên quan

[Xrm.Utility](../xrm-utility.md)



