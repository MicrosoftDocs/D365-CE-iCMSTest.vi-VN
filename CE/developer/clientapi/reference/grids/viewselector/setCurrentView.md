---
title: setCurrentView (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: f5ee65bf-2964-49c9-9dd2-d81416353bf3
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2f4c8fa86003954a0583743367f901d4a6f7d24e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386054"
---
# <a name="setcurrentview-client-api-reference"></a>setCurrentView (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setCurrentView-description.md](./includes/setCurrentView-description.md)]

## <a name="grid-types-supported"></a>Grid types supported

Read-only grid

## <a name="syntax"></a>Cú pháp

`viewSelector.setCurrentView(object);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|đối tượng|Lookup object|Có|Specify the Lookup object that has the following attributes:<br/>- **entityType**: Number. The object type code for the SavedQuery (1039) or UserQuery (4230) that represents the view the user can select.<br/>- **id**: String. The Id for the view the user can select.<br/>- **name**: String. The name of the view the user can select.|

## <a name="remarks"></a>Chú thích

If the subgrid control is not configured to display the view selector, calling this method on the `viewSelector` object will throw an error.

To get the `viewSelector` object, see [ViewSelector](../viewselector.md).

## <a name="example"></a>Ví dụ

```JavaScript
function setView(executionContext) {
    var ContactsIFollow = {
        entityType: 1039, // SavedQuery
        id: "3A282DA1-5D90-E011-95AE-00155D9CFA02",
        name: "Contacts I Follow"
    }
    // Get the gridContext
    var formContext = executionContext.getFormContext();
    var gridContext = formContext.getControl("Contacts");

    // Set the view using ContactsIFollow
    gridContext.getViewSelector().setCurrentView(ContactsIFollow);
}
```

### <a name="related-topics"></a>Chủ đề liên quan

[ViewSelector](../viewselector.md)




