---
title: getOption (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: e334d2d9-91c0-4953-956d-444a84dc9da2
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4d26daf4ea2b97841924c6bf4ee2ca9a646e41c6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387878"
---
# <a name="getoption-client-api-reference"></a>getOption (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns an option object with the value matching the argument (label or enumeration value) passed to the method. 

## <a name="attribute-types-supported"></a>Attribute types supported

OptionSet, MultiSelectOptionSet

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getOption(value)`

## <a name="parameters"></a>Tham số

**String** (label of the option) or **Number** (enumeration value of the option).

## <a name="return-value"></a>Giá trị trả lại

**Type**: Option object. 

**Description**: The logical name of the attribute.

