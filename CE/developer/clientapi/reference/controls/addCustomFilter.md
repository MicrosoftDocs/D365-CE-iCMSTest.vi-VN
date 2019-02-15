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
# <a name="addcustomfilter-client-api-reference"></a><span data-ttu-id="672b4-102">addCustomFilter (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="672b4-102">addCustomFilter (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="672b4-103">Adds filters to the results displayed in the lookup.</span><span class="sxs-lookup"><span data-stu-id="672b4-103">Adds filters to the results displayed in the lookup.</span></span> <span data-ttu-id="672b4-104">Each filter will be combined with any previously added filters as an “AND” condition.</span><span class="sxs-lookup"><span data-stu-id="672b4-104">Each filter will be combined with any previously added filters as an “AND” condition.</span></span>

> [!NOTE]
> <span data-ttu-id="672b4-105">Custom lookup filters are not supported in mobile offline.</span><span class="sxs-lookup"><span data-stu-id="672b4-105">Custom lookup filters are not supported in mobile offline.</span></span> <span data-ttu-id="672b4-106">For information about the mobile offline feature, see [Configure mobile offline synchronization](../../../../mobile-app/configure-mobile-offline-synchronization-dynamics-365-phones-tablets.md)</span><span class="sxs-lookup"><span data-stu-id="672b4-106">For information about the mobile offline feature, see [Configure mobile offline synchronization](../../../../mobile-app/configure-mobile-offline-synchronization-dynamics-365-phones-tablets.md)</span></span>

## <a name="control-types-supported"></a><span data-ttu-id="672b4-107">Control types supported</span><span class="sxs-lookup"><span data-stu-id="672b4-107">Control types supported</span></span>

<span data-ttu-id="672b4-108">Tra cứu</span><span class="sxs-lookup"><span data-stu-id="672b4-108">Lookup</span></span>

## <a name="syntax"></a><span data-ttu-id="672b4-109">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="672b4-109">Syntax</span></span>

`formContext.getControl(arg).addCustomFilter(filter, entityLogicaName)`

## <a name="parameters"></a><span data-ttu-id="672b4-110">Tham số</span><span class="sxs-lookup"><span data-stu-id="672b4-110">Parameters</span></span>

- <span data-ttu-id="672b4-111">**filter**: String.</span><span class="sxs-lookup"><span data-stu-id="672b4-111">**filter**: String.</span></span> <span data-ttu-id="672b4-112">The fetchXml filter element to apply.</span><span class="sxs-lookup"><span data-stu-id="672b4-112">The fetchXml filter element to apply.</span></span> <span data-ttu-id="672b4-113">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="672b4-113">For example:</span></span>

    ```xml
    <filter type="and">
      <condition attribute="address1_city" operator="eq" value="Redmond" />
    </filter>
    ```

- <span data-ttu-id="672b4-114">**entityLogicalName**: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="672b4-114">**entityLogicalName**: (Optional) String.</span></span> <span data-ttu-id="672b4-115">If this is set, the filter only applies to that entity type.</span><span class="sxs-lookup"><span data-stu-id="672b4-115">If this is set, the filter only applies to that entity type.</span></span> <span data-ttu-id="672b4-116">Otherwise, it applies to all types of entities returned.</span><span class="sxs-lookup"><span data-stu-id="672b4-116">Otherwise, it applies to all types of entities returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="672b4-117">Chú thích</span><span class="sxs-lookup"><span data-stu-id="672b4-117">Remarks</span></span>

<span data-ttu-id="672b4-118">This method can only be used in a function in an event handler for the [Lookup Control PreSearch Event](../events/presearch.md).</span><span class="sxs-lookup"><span data-stu-id="672b4-118">This method can only be used in a function in an event handler for the [Lookup Control PreSearch Event](../events/presearch.md).</span></span>

## <a name="example"></a><span data-ttu-id="672b4-119">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="672b4-119">Example</span></span>

<span data-ttu-id="672b4-120">The following code sample is for the Opportunity form **Account** (parentaccountid) lookup.</span><span class="sxs-lookup"><span data-stu-id="672b4-120">The following code sample is for the Opportunity form **Account** (parentaccountid) lookup.</span></span> <span data-ttu-id="672b4-121">When the **Sdk.setParentAccountIdFilter** function is set in the form **Onload** event handler, the **Sdk.filterCustomAccounts** function is added to the **PreSearch** event for that lookup.</span><span class="sxs-lookup"><span data-stu-id="672b4-121">When the **Sdk.setParentAccountIdFilter** function is set in the form **Onload** event handler, the **Sdk.filterCustomAccounts** function is added to the **PreSearch** event for that lookup.</span></span> <span data-ttu-id="672b4-122">Remember to select the option to pass in the execution context when setting the function in the form **Onload** event handler.</span><span class="sxs-lookup"><span data-stu-id="672b4-122">Remember to select the option to pass in the execution context when setting the function in the form **Onload** event handler.</span></span> <span data-ttu-id="672b4-123">The result is that only accounts with the **Category** (accountcategorycode) value of **Preferred Customer** (1) will be returned.</span><span class="sxs-lookup"><span data-stu-id="672b4-123">The result is that only accounts with the **Category** (accountcategorycode) value of **Preferred Customer** (1) will be returned.</span></span>

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
[<span data-ttu-id="672b4-124">addPreSearch</span><span class="sxs-lookup"><span data-stu-id="672b4-124">addPreSearch</span></span>](addPreSearch.md)

[<span data-ttu-id="672b4-125">formContext</span><span class="sxs-lookup"><span data-stu-id="672b4-125">formContext</span></span>](../../clientapi-form-context.md)
