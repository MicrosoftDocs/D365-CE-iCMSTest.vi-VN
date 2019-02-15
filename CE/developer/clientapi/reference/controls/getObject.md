---
title: getObject (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: ad68d177-3715-468e-b4af-8cf9b3c77799
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6070da231c4042ff403dfea5c8a5e4e96bbe6929
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385960"
---
# <a name="getobject-client-api-reference"></a><span data-ttu-id="7a00b-102">getObject (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="7a00b-102">getObject (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="7a00b-103">Returns the object in the form that represents an IFRAME or web resource.</span><span class="sxs-lookup"><span data-stu-id="7a00b-103">Returns the object in the form that represents an IFRAME or web resource.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="7a00b-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="7a00b-104">Control types supported</span></span>

<span data-ttu-id="7a00b-105">iframe, webresource</span><span class="sxs-lookup"><span data-stu-id="7a00b-105">iframe, webresource</span></span>

## <a name="syntax"></a><span data-ttu-id="7a00b-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="7a00b-106">Syntax</span></span>

`formContext.getControl(arg).getObject();`

## <a name="return-value"></a><span data-ttu-id="7a00b-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="7a00b-107">Return Value</span></span>

<span data-ttu-id="7a00b-108">**Type**: Object</span><span class="sxs-lookup"><span data-stu-id="7a00b-108">**Type**: Object</span></span>

<span data-ttu-id="7a00b-109">**Description**: Object depends on the type of control:</span><span class="sxs-lookup"><span data-stu-id="7a00b-109">**Description**: Object depends on the type of control:</span></span>
- <span data-ttu-id="7a00b-110">An IFRAME returns the [IFrame](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe) element from the Document Object Model (DOM).</span><span class="sxs-lookup"><span data-stu-id="7a00b-110">An IFRAME returns the [IFrame](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe) element from the Document Object Model (DOM).</span></span>
- <span data-ttu-id="7a00b-111">A Silverlight web resource will return the [Object](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/object) element from the DOM that represents the embedded Silverlight plug-in.</span><span class="sxs-lookup"><span data-stu-id="7a00b-111">A Silverlight web resource will return the [Object](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/object) element from the DOM that represents the embedded Silverlight plug-in.</span></span>



