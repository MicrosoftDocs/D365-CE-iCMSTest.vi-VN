---
title: getEntityReference (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: 8b690ae0208fbdd4234d11dc6aec36a68b9de456
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387216"
---
# <a name="getentityreference-client-api-reference"></a><span data-ttu-id="80c5e-102">getEntityReference (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="80c5e-102">getEntityReference (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getEntityReference-description.md](./includes/getEntityReference-description.md)]

## <a name="syntax"></a><span data-ttu-id="80c5e-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="80c5e-103">Syntax</span></span>

`formContext.data.entity.getEntityReference();`

## <a name="return-value"></a><span data-ttu-id="80c5e-104">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="80c5e-104">Return Value</span></span>

<span data-ttu-id="80c5e-105">**Type**: Lookup object.</span><span class="sxs-lookup"><span data-stu-id="80c5e-105">**Type**: Lookup object.</span></span>

<span data-ttu-id="80c5e-106">**Description**: The returned object has following three attributes:</span><span class="sxs-lookup"><span data-stu-id="80c5e-106">**Description**: The returned object has following three attributes:</span></span>

- <span data-ttu-id="80c5e-107">**entityType**: String.</span><span class="sxs-lookup"><span data-stu-id="80c5e-107">**entityType**: String.</span></span> <span data-ttu-id="80c5e-108">Logical name of the entity record.</span><span class="sxs-lookup"><span data-stu-id="80c5e-108">Logical name of the entity record.</span></span> <span data-ttu-id="80c5e-109">For example, "account".</span><span class="sxs-lookup"><span data-stu-id="80c5e-109">For example, "account".</span></span>
- <span data-ttu-id="80c5e-110">**id**: String.</span><span class="sxs-lookup"><span data-stu-id="80c5e-110">**id**: String.</span></span> <span data-ttu-id="80c5e-111">GUID value of the entity record.</span><span class="sxs-lookup"><span data-stu-id="80c5e-111">GUID value of the entity record.</span></span>
- <span data-ttu-id="80c5e-112">**name**: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="80c5e-112">**name**: (Optional) String.</span></span> <span data-ttu-id="80c5e-113">Name of the entity record.</span><span class="sxs-lookup"><span data-stu-id="80c5e-113">Name of the entity record.</span></span> 



