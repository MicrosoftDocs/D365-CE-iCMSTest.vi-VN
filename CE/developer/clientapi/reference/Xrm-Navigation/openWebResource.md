---
title: openWebResource (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 07/13/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 798dc921-1e80-42bc-b8ca-2056728bcba4
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6221dcf64ee624f0ba6f2def70f46c9898489ffb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386843"
---
# <a name="openwebresource-client-api-reference"></a>openWebResource (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/openWebResource-description.md](./includes/openWebResource-description.md)]

## <a name="syntax"></a>Cú pháp

`Xrm.Navigation.openWebResource(webResourceName,windowOptions,data)`

## <a name="parameters"></a>Tham số

|Tên |Loại |Bắt buộc |Mô tả |
|---|---|---|---|
|webResourceName|Chuỗi|Có|Name of the HTML web resource to open.|
|windowOptions|Đối tượng|Không|Window options for opening the web resource. The object contains the following attributes:<br/>- **height**: (Optional) Number. Height of the window to open in pixels.<br/>- **width**: (Optional) Number. Width of the window to open in pixels.|
|dữ liệu|Chuỗi|Không|Data to be passed into the data parameter.|

## <a name="remarks"></a>Chú thích

You must use this method to display web resources instead of the deprecated [Xrm.Utility.openWebResource](https://msdn.microsoft.com/library/jj602956.aspx#BKMK_OpenWebResource) method.

An HTML web resource can accept the parameter values described in [Pass parameters to HTML web resources](../../../webpage-html-web-resources.md#BKMK_PassingParametersToWebResources). This function only provides for passing in the optional data parameter. To pass values for the other valid parameters, you must append them to the `webResourceName` parameter.

> [!NOTE]
> The **Xrm** object isn’t available in HTML web resources. Therefore, scripts containing `Xrm.*` methods aren’t supported in HTML web resources. `parent.Xrm.*` will work if the HTML web resource is loaded in a form container. However, for other places, such as loading an HTML web resource as part of the SiteMap, `parent.Xrm.*` also won’t work. More information: [GetGlobalContext function and ClientGlobalContext.js.aspx](../GetGlobalContext-ClientGlobalContext.js.aspx.md)



## <a name="examples"></a>Ví dụ

- Open an HTML web resource named “new_webResource.htm”:
   
   `Xrm.Navigation.openWebResource("new_webResource.htm");`

- Open an HTML web resource, setting the windowOptions:

  ```
  var windowOptions = { height: 400, width: 400 }
  Xrm.Navigation.openWebResource("new_webResource.htm",windowOptions);
  ```

- Open an HTML web resource including a single item of data for the `data` parameter

  `Xrm.Navigation.openWebResource("new_webResource.htm",null,"dataItemValue");`

  ### <a name="related-topics"></a>Chủ đề liên quan

[Xrm.Navigation](../xrm-navigation.md)

