---
title: addCustomView (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 482b8cd4-e643-48ea-8a54-d8601271ec81
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: def8d71f5f6e7f67faf3bbbebe853e3cd5866379
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387582"
---
# <a name="addcustomview-client-api-reference"></a>addCustomView (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Adds a new view for the lookup dialog box. 

## <a name="control-types-supported"></a>Control types supported

Tra cứu

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).addCustomView(viewId, entityName, viewDisplayName, fetchXml, layoutXml, isDefault)`

## <a name="parameters"></a>Tham số

- **viewId**: String. The string representation of a GUID for a view.
    > [!NOTE]
    > This value is never saved and only needs to be unique among the other available views for the lookup. A string for a non-valid GUID will work, for example “{00000000-0000-0000-0000-000000000001}”. It’s recommended that you use a tool like **guidgen.exe** to generate a valid GUID.  

- **entityName**: String. The name of the entity.
- **viewDisplayName**: String. The name of the view.
- **fetchXml**: String. The fetchXml query for the view.
- **layoutXml**: String. The XML that defines the layout of the view.
- **isDefault**: Boolean: Indicates whether the view should be the default view.

## <a name="remarks"></a>Chú thích

This method doesn’t work with **Owner** lookups. Owner lookups are used to assign user-owned records.
