---
title: getValue (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4d025f92-db16-440c-9f82-e40d71e09862
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: afcf35d43fdf48ba066e7698c2d4e030ff2bf797
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387554"
---
# <a name="getvalue-client-api-reference"></a><span data-ttu-id="e1207-102">getValue (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="e1207-102">getValue (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e1207-103">Gets the latest value in a control as the user types characters in a specific text or number field.</span><span class="sxs-lookup"><span data-stu-id="e1207-103">Gets the latest value in a control as the user types characters in a specific text or number field.</span></span> <span data-ttu-id="e1207-104">This method helps you to build interactive experiences by validating data and alerting users as they type characters in a control.</span><span class="sxs-lookup"><span data-stu-id="e1207-104">This method helps you to build interactive experiences by validating data and alerting users as they type characters in a control.</span></span>

<span data-ttu-id="e1207-105">The getValue method is different from the attribute [getValue](../attributes/getvalue.md) method because the control method retrieves the value from the control as the user is typing in the control as opposed to the attribute getValue method that retrieves the value after the user commits (saves) the field.</span><span class="sxs-lookup"><span data-stu-id="e1207-105">The getValue method is different from the attribute [getValue](../attributes/getvalue.md) method because the control method retrieves the value from the control as the user is typing in the control as opposed to the attribute getValue method that retrieves the value after the user commits (saves) the field.</span></span> 

## <a name="syntax"></a><span data-ttu-id="e1207-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="e1207-106">Syntax</span></span>

`formContext.getControl(arg).getValue();`

## <a name="return-value"></a><span data-ttu-id="e1207-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="e1207-107">Return Value</span></span>

<span data-ttu-id="e1207-108">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="e1207-108">**Type**: String</span></span>

<span data-ttu-id="e1207-109">**Description**:  The latest data value for a control.</span><span class="sxs-lookup"><span data-stu-id="e1207-109">**Description**:  The latest data value for a control.</span></span>

