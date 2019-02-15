---
title: addCustomFilter (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 06/24/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: e359b-c4d9-48ac-a57b-367c2e6168c5
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6d0b10c1653c89a8597392c8a425e1e20da51bd4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387201"
---
# <a name="addcustomfilter-client-api-reference"></a>addCustomFilter (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Adds filters to the results displayed in the lookup. Each filter will be combined with any previously added filters as an “AND” condition.

> [!NOTE]
> Custom lookup filters are not supported in mobile offline. For information about the mobile offline feature, see [Configure mobile offline synchronization](../../../../mobile-app/configure-mobile-offline-synchronization-dynamics-365-phones-tablets.md)

## <a name="control-types-supported"></a>Control types supported

Tra cứu

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).addCustomFilter(filter, entityLogicaName)`

## <a name="parameters"></a>Tham số

- **filter**: String. The fetchXml filter element to apply. Ví dụ:

    ```xml
    <filter type="and">
      <condition attribute="address1_city" operator="eq" value="Redmond" />
    </filter>
    ```

- **entityLogicalName**: (Optional) String. If this is set, the filter only applies to that entity type. Otherwise, it applies to all types of entities returned.

## <a name="remarks"></a>Chú thích

This method can only be used in a function in an event handler for the [Lookup Control PreSearch Event](../events/presearch.md).

## <a name="example"></a>Ví dụ

The following code sample is for the Opportunity form **Account** (parentaccountid) lookup. When the **Sdk.setParentAccountIdFilter** function is set in the form **Onload** event handler, the **Sdk.filterCustomAccounts** function is added to the **PreSearch** event for that lookup. Remember to select the option to pass in the execution context when setting the function in the form **Onload** event handler. The result is that only accounts with the **Category** (accountcategorycode) value of **Preferred Customer** (1) will be returned.

```JavaScript
// A namespace defined for SDK sample code
// You should define a unique namespace for your libraries
var Sdk = window.Sdk || {};

// set 'Sdk.setParentAccountIdFilter' in the Opportunity form onload event handler
Sdk.setParentAccountIdFilter = function (executionContext) {

    // get the form context
    formContext = executionContext.getFormContext();
    formContext.getControl("parentaccountid").addPreSearch(Sdk.filterCustomerAccounts);
}

Sdk.filterCustomerAccounts = function () {

    // Only show accounts with the type 'Preferred Customer'
    var customerAccountFilter = "<filter type='and'><condition attribute='accountcategorycode' operator='eq' value='1'/></filter>";
    formContext.getControl("parentaccountid").addCustomFilter(customerAccountFilter, "account");
}
```
[addPreSearch](addPreSearch.md)

[formContext](../../clientapi-form-context.md)
