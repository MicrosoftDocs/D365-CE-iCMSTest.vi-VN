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
# <a name="xrmwebapioffline-client-api-reference"></a><span data-ttu-id="a310b-102">Xrm.WebApi.offline (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="a310b-102">Xrm.WebApi.offline (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/offline-description.md](./includes/offline-description.md)] 

<span data-ttu-id="a310b-103">For information about the mobile offline feature, see [Configure mobile offline synchronization to allow users to work in offline mode on their mobile device](../../../../mobile-app/configure-mobile-offline-synchronization-dynamics-365-phones-tablets.md)</span><span class="sxs-lookup"><span data-stu-id="a310b-103">For information about the mobile offline feature, see [Configure mobile offline synchronization to allow users to work in offline mode on their mobile device](../../../../mobile-app/configure-mobile-offline-synchronization-dynamics-365-phones-tablets.md)</span></span>

`var offlineWebApi = Xrm.WebApi.offline;`

> [!NOTE]
> <span data-ttu-id="a310b-104">Use **Xrm.WebApi.offline** instead of the [deprecated](/dynamics365/get-started/whats-new/customer-engagement/important-changes-coming#some-client-apis-are-deprecated) **Xrm.Mobile.Offline** namespace to create and manage records in the mobile clients while working in the offline mode.</span><span class="sxs-lookup"><span data-stu-id="a310b-104">Use **Xrm.WebApi.offline** instead of the [deprecated](/dynamics365/get-started/whats-new/customer-engagement/important-changes-coming#some-client-apis-are-deprecated) **Xrm.Mobile.Offline** namespace to create and manage records in the mobile clients while working in the offline mode.</span></span>

<span data-ttu-id="a310b-105">The **offlineWebApi** object provides the following methods.</span><span class="sxs-lookup"><span data-stu-id="a310b-105">The **offlineWebApi** object provides the following methods.</span></span> <span data-ttu-id="a310b-106">When in the offline mode, these methods will work only for entities that are enabled for mobile offline synchronization and available in current user’s mobile offline profile.</span><span class="sxs-lookup"><span data-stu-id="a310b-106">When in the offline mode, these methods will work only for entities that are enabled for mobile offline synchronization and available in current user’s mobile offline profile.</span></span>

- [<span data-ttu-id="a310b-107">createRecord</span><span class="sxs-lookup"><span data-stu-id="a310b-107">createRecord</span></span>](createRecord.md)
- [<span data-ttu-id="a310b-108">deleteRecord</span><span class="sxs-lookup"><span data-stu-id="a310b-108">deleteRecord</span></span>](deleteRecord.md)
- [<span data-ttu-id="a310b-109">isAvailableOffline</span><span class="sxs-lookup"><span data-stu-id="a310b-109">isAvailableOffline</span></span>](isAvailableOffline.md)
- [<span data-ttu-id="a310b-110">retrieveRecord</span><span class="sxs-lookup"><span data-stu-id="a310b-110">retrieveRecord</span></span>](retrieveRecord.md)
- [<span data-ttu-id="a310b-111">retrieveMultipleRecords</span><span class="sxs-lookup"><span data-stu-id="a310b-111">retrieveMultipleRecords</span></span>](retrieveMultipleRecords.md)
- [<span data-ttu-id="a310b-112">updateRecord</span><span class="sxs-lookup"><span data-stu-id="a310b-112">updateRecord</span></span>](updateRecord.md)

> [!IMPORTANT]
> <span data-ttu-id="a310b-113">While creating or updating record in the offline mode, only basic validation is performed on the input data.</span><span class="sxs-lookup"><span data-stu-id="a310b-113">While creating or updating record in the offline mode, only basic validation is performed on the input data.</span></span> <span data-ttu-id="a310b-114">Basic validation includes things such as ensuring that the entity attribute name specified is in lower case and does exist for an entity, checking for data type mismatch for the specified attribute value, preventing records getting created with the same GUID value, checking whether the related entity is offline enabled when retrieving related entity records, and validating if the record that you want to retrieve, update, or delete actually exists in the offline data store.</span><span class="sxs-lookup"><span data-stu-id="a310b-114">Basic validation includes things such as ensuring that the entity attribute name specified is in lower case and does exist for an entity, checking for data type mismatch for the specified attribute value, preventing records getting created with the same GUID value, checking whether the related entity is offline enabled when retrieving related entity records, and validating if the record that you want to retrieve, update, or delete actually exists in the offline data store.</span></span> <span data-ttu-id="a310b-115">Business-level validations happen only when you are connected to the server and the data is synchronized.</span><span class="sxs-lookup"><span data-stu-id="a310b-115">Business-level validations happen only when you are connected to the server and the data is synchronized.</span></span> <span data-ttu-id="a310b-116">A record is created or updated only if the input data is completely valid.</span><span class="sxs-lookup"><span data-stu-id="a310b-116">A record is created or updated only if the input data is completely valid.</span></span>

### <a name="related-topics"></a><span data-ttu-id="a310b-117">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="a310b-117">Related topics</span></span>

[<span data-ttu-id="a310b-118">Xrm.WebApi.online</span><span class="sxs-lookup"><span data-stu-id="a310b-118">Xrm.WebApi.online</span></span>](online.md)

[<span data-ttu-id="a310b-119">Xrm.WebApi</span><span class="sxs-lookup"><span data-stu-id="a310b-119">Xrm.WebApi</span></span>](../xrm-webapi.md)



