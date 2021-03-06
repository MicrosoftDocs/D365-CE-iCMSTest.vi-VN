---
title: getResourceString (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 01/02/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: d5e51eac-ce0a-4f4a-b7b6-495433e3f8c1
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2909a7e6dae2eebec17075e3aa51176d15a77246
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386052"
---
# <a name="getresourcestring-client-api-reference"></a>getResourceString (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getResourceString-description.md](./includes/getResourceString-description.md)] 

## <a name="syntax"></a>Cú pháp

`Xrm.Utility.getResourceString(webResourceName,key)` 

## <a name="parameters"></a>Tham số

|Tên |Loại |Bắt buộc |Mô tả |
|---|---|---|---|
|webResourceName|Chuỗi|Có|The name of the web resource.|
|khóa|Chuỗi|Có|The key for the localized string.|

## <a name="return-value"></a>Return value

A localized string.

## <a name="remarks"></a>Chú thích

<!-- 
Content adapted from /developer/resx-web-resources 
If you change this, make sure that topic is in sync.
-->

When you create RESX web resources you must explicitly set the language value and include the locale identifier (LCID) for the appropriate language in the name of the web resource. For example, `new_/strings/MyAppResources.1033.resx` would contain resources for English language. See [Microsoft Locale ID Values](https://msdn.microsoft.com/library/ms912047(WinEmbedded.10).aspx) for a list of LCID values.

For example `Xrm.Utility.getResourceString("new_/strings/MyAppResources","hello")` will return the localized string value for the resource key `hello` within the `new_/strings/MyAppResources.1033.resx` web resource if the user’s preferred language is English. Notice that the function doesn’t refer to any specific language or full name of any RESX web resource. This functionality depends on the RESX web resource being associated to the calling JavaScript web resource as a dependency. More information: [Web resource dependencies](../../../web-resource-dependencies.md).

The appropriate string value will be determined by the individual user’s language preference and the languages available in the organization. If a localized string is not found that matches the user’s language preference, the localized string will automatically fallback to the base language for the organization. If no matching localized string is found for the organizations base language, a null value will be returned.

### <a name="related-topics"></a>Chủ đề liên quan

[Xrm.Utility](../xrm-utility.md)<br />
[String (RESX) web resources](../../../resx-web-resources.md)<br />
[Quan hệ phụ thuộc tài nguyên web](../../../web-resource-dependencies.md)



