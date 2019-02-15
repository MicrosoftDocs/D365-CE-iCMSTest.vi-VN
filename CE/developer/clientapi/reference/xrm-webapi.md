---
title: Xrm.WebApi (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
ms.date: 12/18/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: a6646fc8-c2e4-43fe-95f1-51483de38688
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: dd3dcd2d733ac79c532f56df82edcd626c485bfb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388356"
---
# <a name="xrmwebapi-client-api-reference"></a><span data-ttu-id="b8b54-102">Xrm.WebApi (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="b8b54-102">Xrm.WebApi (Client API reference)</span></span>

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b8b54-103">Provides properties and methods to use Web API to create and manage records and execute Web API actions and functions in Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="b8b54-103">Provides properties and methods to use Web API to create and manage records and execute Web API actions and functions in Customer Engagement.</span></span> 

## <a name="properties"></a><span data-ttu-id="b8b54-104">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="b8b54-104">Properties</span></span>

|             <span data-ttu-id="b8b54-105">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="b8b54-105">Property</span></span>             |                                            <span data-ttu-id="b8b54-106">Mô tả</span><span class="sxs-lookup"><span data-stu-id="b8b54-106">Description</span></span>                                             |
|----------------------------------|----------------------------------------------------------------------------------------------------|
|  [<span data-ttu-id="b8b54-107">trực tuyến</span><span class="sxs-lookup"><span data-stu-id="b8b54-107">online</span></span>](xrm-webapi/online.md)  |  [!INCLUDE[xrm-webapi/includes/online-description.md](xrm-webapi/includes/online-description.md)]  |
| [<span data-ttu-id="b8b54-108">offline</span><span class="sxs-lookup"><span data-stu-id="b8b54-108">offline</span></span>](xrm-webapi/offline.md) | [!INCLUDE[xrm-webapi/includes/offline-description.md](xrm-webapi/includes/offline-description.md)] |

## <a name="methods"></a><span data-ttu-id="b8b54-109">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="b8b54-109">Methods</span></span>

|                              <span data-ttu-id="b8b54-110">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="b8b54-110">Method</span></span>                              |                                                            <span data-ttu-id="b8b54-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="b8b54-111">Description</span></span>                                                             |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
|            [<span data-ttu-id="b8b54-112">createRecord</span><span class="sxs-lookup"><span data-stu-id="b8b54-112">createRecord</span></span>](xrm-webapi/createRecord.md)            |            [!INCLUDE[xrm-webapi/includes/createRecord-description.md](xrm-webapi/includes/createRecord-description.md)]            |
|            [<span data-ttu-id="b8b54-113">deleteRecord</span><span class="sxs-lookup"><span data-stu-id="b8b54-113">deleteRecord</span></span>](xrm-webapi/deleteRecord.md)            |            [!INCLUDE[xrm-webapi/includes/deleteRecord-description.md](xrm-webapi/includes/deleteRecord-description.md)]            |
|          [<span data-ttu-id="b8b54-114">retrieveRecord</span><span class="sxs-lookup"><span data-stu-id="b8b54-114">retrieveRecord</span></span>](xrm-webapi/retrieveRecord.md)          |          [!INCLUDE[xrm-webapi/includes/retrieveRecord-description.md](xrm-webapi/includes/retrieveRecord-description.md)]          |
| [<span data-ttu-id="b8b54-115">retrieveMultipleRecords</span><span class="sxs-lookup"><span data-stu-id="b8b54-115">retrieveMultipleRecords</span></span>](xrm-webapi/retrieveMultipleRecords.md) | [!INCLUDE[xrm-webapi/includes/retrieveMultipleRecords-description.md](xrm-webapi/includes/retrieveMultipleRecords-description.md)] |
|            [<span data-ttu-id="b8b54-116">updateRecord</span><span class="sxs-lookup"><span data-stu-id="b8b54-116">updateRecord</span></span>](xrm-webapi/updateRecord.md)            |            [!INCLUDE[xrm-webapi/includes/updateRecord-description.md](xrm-webapi/includes/updateRecord-description.md)]            |
|      [<span data-ttu-id="b8b54-117">isAvailableOffline</span><span class="sxs-lookup"><span data-stu-id="b8b54-117">isAvailableOffline</span></span>](xrm-webapi/isAvailableOffline.md)      |      [!INCLUDE[xrm-webapi/includes/isAvailableOffline-description.md](xrm-webapi/includes/isAvailableOffline-description.md)]      |
|                 [<span data-ttu-id="b8b54-118">thực thi</span><span class="sxs-lookup"><span data-stu-id="b8b54-118">execute</span></span>](xrm-webapi/online/execute.md)                 |                 [!INCLUDE[xrm-webapi/includes/execute-description.md](xrm-webapi/includes/execute-description.md)] <span data-ttu-id="b8b54-119">Supported only for the online mode ([Xrm.WebApi.online](xrm-webapi/online.md)).</span><span class="sxs-lookup"><span data-stu-id="b8b54-119">Supported only for the online mode ([Xrm.WebApi.online](xrm-webapi/online.md)).</span></span>                |
|         [<span data-ttu-id="b8b54-120">executeMultiple</span><span class="sxs-lookup"><span data-stu-id="b8b54-120">executeMultiple</span></span>](xrm-webapi/online/executeMultiple.md)         |         [!INCLUDE[xrm-webapi/includes/executeMultiple-description.md](xrm-webapi/includes/executeMultiple-description.md)] <span data-ttu-id="b8b54-121">Supported only for the online mode ([Xrm.WebApi.online](xrm-webapi/online.md)).</span><span class="sxs-lookup"><span data-stu-id="b8b54-121">Supported only for the online mode ([Xrm.WebApi.online](xrm-webapi/online.md)).</span></span>        |

### <a name="related-topics"></a><span data-ttu-id="b8b54-122">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="b8b54-122">Related topics</span></span>

[<span data-ttu-id="b8b54-123">Use the Dynamics 365 for Customer Engagement Web API</span><span class="sxs-lookup"><span data-stu-id="b8b54-123">Use the Dynamics 365 for Customer Engagement Web API</span></span>](../../use-microsoft-dynamics-365-web-api.md)

[<span data-ttu-id="b8b54-124">Client API Xrm object</span><span class="sxs-lookup"><span data-stu-id="b8b54-124">Client API Xrm object</span></span>](../clientapi-xrm.md)
