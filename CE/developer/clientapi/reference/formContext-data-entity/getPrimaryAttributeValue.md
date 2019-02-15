---
title: getPrimaryAttributeValue (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: 861259cc24573c1ca5820106385e3b5c722d8e13
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386120"
---
# <a name="getprimaryattributevalue-client-api-reference"></a><span data-ttu-id="b7e79-102">getPrimaryAttributeValue (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="b7e79-102">getPrimaryAttributeValue (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getPrimaryAttributeValue-description.md](./includes/getPrimaryAttributeValue-description.md)]

## <a name="syntax"></a><span data-ttu-id="b7e79-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="b7e79-103">Syntax</span></span>

`formContext.data.entity.getPrimaryAttributeValue();`

## <a name="return-value"></a><span data-ttu-id="b7e79-104">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="b7e79-104">Return Value</span></span>

<span data-ttu-id="b7e79-105">**Type**: String.</span><span class="sxs-lookup"><span data-stu-id="b7e79-105">**Type**: String.</span></span>

<span data-ttu-id="b7e79-106">**Description**: The name of the entity.</span><span class="sxs-lookup"><span data-stu-id="b7e79-106">**Description**: The name of the entity.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7e79-107">Chú thích</span><span class="sxs-lookup"><span data-stu-id="b7e79-107">Remarks</span></span>

<span data-ttu-id="b7e79-108">Each entity has one string attribute that is designated as the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.PrimaryNameAttribute>.</span><span class="sxs-lookup"><span data-stu-id="b7e79-108">Each entity has one string attribute that is designated as the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.PrimaryNameAttribute>.</span></span> <span data-ttu-id="b7e79-109">The value for this attribute is used when links to the record are displayed.</span><span class="sxs-lookup"><span data-stu-id="b7e79-109">The value for this attribute is used when links to the record are displayed.</span></span>



