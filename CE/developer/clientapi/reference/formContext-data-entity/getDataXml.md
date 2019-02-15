---
title: getDataXml (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 1a66f93d-a47c-4316-91f1-dcf5d09f9d19
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 12394437139dc00c23d5a4f55fd4eda45df42890
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385980"
---
# <a name="getdataxml-client-api-reference"></a><span data-ttu-id="91e12-102">getDataXml (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="91e12-102">getDataXml (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getDataXml-description.md](./includes/getDataXml-description.md)]

## <a name="syntax"></a><span data-ttu-id="91e12-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="91e12-103">Syntax</span></span>

`formContext.data.entity.getDataXml();`

## <a name="return-value"></a><span data-ttu-id="91e12-104">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="91e12-104">Return Value</span></span>

<span data-ttu-id="91e12-105">**Type**: String.</span><span class="sxs-lookup"><span data-stu-id="91e12-105">**Type**: String.</span></span>

<span data-ttu-id="91e12-106">**Description**: In this example, the following three fields for an account record were updated: name, accountnumber, telephone2.</span><span class="sxs-lookup"><span data-stu-id="91e12-106">**Description**: In this example, the following three fields for an account record were updated: name, accountnumber, telephone2.</span></span>

```"<account><name>Contoso</name><accountnumber>55555</accountnumber><telephone2>425 555-1234</telephone2></account>"```

## <a name="remarks"></a><span data-ttu-id="91e12-107">Chú thích</span><span class="sxs-lookup"><span data-stu-id="91e12-107">Remarks</span></span>

<span data-ttu-id="91e12-108">This method does not work with Microsoft Dynamics 365 for tablets.</span><span class="sxs-lookup"><span data-stu-id="91e12-108">This method does not work with Microsoft Dynamics 365 for tablets.</span></span>



