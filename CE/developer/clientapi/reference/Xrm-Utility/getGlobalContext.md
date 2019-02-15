---
title: getGlobalContext (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
ms.date: 01/23/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: d87e0614-f365-4ed1-992a-741575bb2b7e
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 58f59b22e7b3d3e54fa62c6381dfe749c3bce4cf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386782"
---
# <a name="getglobalcontext-client-api-reference"></a>getGlobalContext (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getGlobalContext-description.md](./includes/getGlobalContext-description.md)]
The method provides access to the global context without going through the form context. It contains an equivalent of all the methods available for the **Xrm.Page.context** object (now deprecated) to retrieve information specific to the client, organization or user.

> [!IMPORTANT]
> To access the global context information in a standalone HTML Web resource, you should include a reference to **ClientGlobalContext.js.aspx** in the web resource, and then use the **GetGlobalContext** function. More information: [GetGlobalContext function and ClientGlobalContext.js.aspx](../GetGlobalContext-ClientGlobalContext.js.aspx.md) 

## <a name="properties-of-global-context-getglobalcontext"></a>Properties of Global Context (getGlobalContext)

Use the following properties of global context to return information about the client, organization settings, or user settings:

|Thuộc tính |Mô tả | 
|---|---|
|[client](getGlobalContext/client.md) | Returns information about the client.|
|[organizationSettings](getGlobalContext/organizationSettings.md) | Returns information about the current organization settings.|
|[userSettings](getGlobalContext/userSettings.md) | Returns information about the current user settings.|


## <a name="methods-of-global-context-getglobalcontext"></a>Methods of Global Context (getGlobalContext)

|Phương pháp |Mô tả |
|---|---|
|[getAdvancedConfigSetting](getGlobalContext/getAdvancedConfigSetting.md) |Returns information about the advanced configuration settings for the organization.|
|[getClientUrl](getGlobalContext/getClientUrl.md) |Returns the base URL that was used to access the application.|
|[getCurrentAppName](getGlobalContext/getCurrentAppName.md) |Returns the name of the current business app in Customer Engagement.|
|[getCurrentAppProperties](getGlobalContext/getCurrentAppProperties.md) |Returns the properties of the current business app in Customer Engagement.|
|[getCurrentAppUrl](getGlobalContext/getCurrentAppUrl.md) |Returns the URL of the current business app in Customer Engagement.|
|[getVersion](getGlobalContext/getVersion.md) |Returns the version number of the Dynamics 365 for Customer Engagement apps instance.|
|[isOnPremises](getGlobalContext/isOnPremises.md) |Returns a boolean value indicating if the Customer Engagement instance is hosted on-premises or online.|
|[prependOrgName](getGlobalContext/prependOrgName.md) |Prefixes the current organization's unique name to a string, typically a URL path.|




 



