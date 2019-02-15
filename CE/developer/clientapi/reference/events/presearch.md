---
title: Lookup Control PreSearch Event (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: ea4279bb31db6100205d072f59ec63e9049058ef
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387323"
---
# <a name="lookup-control-presearch-event-client-api-reference"></a>Lookup Control PreSearch Event (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

This event occurs just before the Lookup control launches a dialog to search for records. There is no UI to set event handlers for this event. You must use the [addPreSearch](../controls/addpresearch.md) and [removePreSearch](../controls/removepresearch.md) methods on the lookup control to add or remove event handlers for this event.

Use this event with other Lookup control methods to change the results displayed in a lookup based on the form data just before the lookup control shows search results for a user to choose from. 

## <a name="related-topics"></a>Chủ đề liên quan

[addCustomFilter](../controls/addCustomFilter.md)



