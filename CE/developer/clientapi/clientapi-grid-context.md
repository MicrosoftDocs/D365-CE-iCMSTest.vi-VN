---
title: Client API grid context in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 08/29/2018
ms.service: crm-online
ms.topic: conceptual
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: f884d7d4-31e6-4080-acd9-493e81e6b278
author: KumarVivek
ms.author: kvivek
manager: annbe
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 91d7bb9617398aa5d5973ca0b81e12545b7d08dd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388204"
---
# <a name="client-api-grid-context"></a>Client API grid context

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

Grids present data in a tabular format. Grids can span the entire form or can be one of the items on a form; the latter are called **subgrids**.

The Client API grid context object provides reference to a subgrid on a form against which the current code is executed. 

> [!NOTE]
> Getting the context of a grid (spanning the entire form) is only supported in ribbon commands. More information: [Form and grid context in ribbon actions](../customize-dev/pass-dynamics-365-data-page-parameter-ribbon-actions.md#form-and-grid-context-in-ribbon-actions)

Use the [formContext](clientapi-form-context.md) object to get an instance of the form where the code is executed, and then retrieve the subgrid control on the form. For example, when you know the name of a subgrid control (say **Contacts** subgrid in the default account form), you can access it using the following code:

```JavaScript
function doSomething(executionContext) {
   var formContext = executionContext.getFormContext(); // get the form Context
   var gridContext = formContext.getControl("Contacts"); // get the grid context

   // Perform operations on the subgrid
}
```

## <a name="related-topics"></a>Chủ đề liên quan

[Client API form context](clientapi-form-context.md)

[Client API execution context](clientapi-execution-context.md)

[Understand the Client API object model](understand-clientapi-object-model.md)

[Grids and subgrids](reference/grids.md)

 

