---
title: Xrm.WebApi.offline (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 12/18/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 848c277b-bd44-4388-852a-0f59a3a15538
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d03873221ef485fb4edebbed694c8ffee0bedd39
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386417"
---
# <a name="xrmwebapioffline-client-api-reference"></a>Xrm.WebApi.offline (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/offline-description.md](./includes/offline-description.md)] 

For information about the mobile offline feature, see [Configure mobile offline synchronization to allow users to work in offline mode on their mobile device](../../../../mobile-app/configure-mobile-offline-synchronization-dynamics-365-phones-tablets.md)

`var offlineWebApi = Xrm.WebApi.offline;`

> [!NOTE]
> Use **Xrm.WebApi.offline** instead of the [deprecated](/dynamics365/get-started/whats-new/customer-engagement/important-changes-coming#some-client-apis-are-deprecated) **Xrm.Mobile.Offline** namespace to create and manage records in the mobile clients while working in the offline mode.

The **offlineWebApi** object provides the following methods. When in the offline mode, these methods will work only for entities that are enabled for mobile offline synchronization and available in current user’s mobile offline profile.

- [createRecord](createRecord.md)
- [deleteRecord](deleteRecord.md)
- [isAvailableOffline](isAvailableOffline.md)
- [retrieveRecord](retrieveRecord.md)
- [retrieveMultipleRecords](retrieveMultipleRecords.md)
- [updateRecord](updateRecord.md)

> [!IMPORTANT]
> While creating or updating record in the offline mode, only basic validation is performed on the input data. Basic validation includes things such as ensuring that the entity attribute name specified is in lower case and does exist for an entity, checking for data type mismatch for the specified attribute value, preventing records getting created with the same GUID value, checking whether the related entity is offline enabled when retrieving related entity records, and validating if the record that you want to retrieve, update, or delete actually exists in the offline data store. Business-level validations happen only when you are connected to the server and the data is synchronized. A record is created or updated only if the input data is completely valid.

### <a name="related-topics"></a>Chủ đề liên quan

[Xrm.WebApi.online](online.md)

[Xrm.WebApi](../xrm-webapi.md)



