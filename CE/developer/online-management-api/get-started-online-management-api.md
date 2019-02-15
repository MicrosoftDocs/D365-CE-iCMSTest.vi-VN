---
title: Get started with Online Management API for Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Provides basic information to help you get started with the Online Admin API for Customer Engagement.
ms.date: 11/16/2018
ms.service: crm-online
ms.topic: conceptual
ms.assetid: c292c148-01f0-41f6-a2fe-7ed05a01a733
author: KumarVivek
ms.author: kvivek
manager: annbe
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8f10d0d562b7ef11bc42f558e9c1a52eeb8c5159
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387893"
---
# <a name="get-started-with-online-management-api"></a>Get started with Online Management API 

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This topic provides basic information to help you get started with the Online Admin API for Customer Engagement.

## <a name="office-365-admin-roles"></a>Office 365 Admin roles

To use the Online Management API, you must have one of the following admin roles assigned to you in your Office 365 tenant:

- Global administrator
- Service administrator

For information about these roles, see [About Office 365 admin roles](https://support.office.com/en-us/article/About-Office-365-admin-roles-da585eea-f576-4f55-a1e0-87090b6aaa9d)

## <a name="service-url"></a>Service URL

The service URL defines the endpoint address for accessing REST API. To perform any operation using the Online Management API, you need to specify the request URL in the following format:

`{ServiceUrl}/api/v1.1/{resource}`

For example, you can pass in the following URL with a **GET** request to retrieve the instances in your Office 365 tenant in North America:

`https://admin.services.crm.dynamics.com/api/v1.1/instances`


The following table lists the service URL of Online Management API for worldwide Office 365 data centers.

|Location | Service URL |
|---------|-------------|
|Bắc Mỹ | https://admin.services.crm.dynamics.com |
|Bắc Mỹ 2 | https://admin.services.crm9.dynamics.com |
|Châu Âu, Trung Đông và Châu Phi (EMEA) | https://admin.services.crm4.dynamics.com |
|Asia Pacific (APAC) | https://admin.services.crm5.dynamics.com |
|Châu Đại Dương | https://admin.services.crm6.dynamics.com |
|Nhật Bản (JPN) | https://admin.services.crm7.dynamics.com |
|Nam Mỹ | https://admin.services.crm2.dynamics.com |
|Ấn Độ (IND) | https://admin.services.crm8.dynamics.com |
|Canada | https://admin.services.crm3.dynamics.com |
|Vương quốc Anh (UK) | https://admin.services.crm11.dynamics.com |


## <a name="standard-headers"></a>Standard headers

The Online Management API has following standard request and response headers.   

### <a name="request-headers"></a>Request headers

| Dòng đầu trang | Loại | Mô tả  |
|--------|------|--------------|
|**Accept-Language**|Chuỗi|Specifies the preferred language for the response. More information about the header: [Accept-Language (MDN web docs)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Accept-Language)|
|**Authorization**|Chuỗi|Specifies the credentials to authenticate a user with the Online Management API service. More information about the header: [Authorization (MDN web docs)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Authorization)|

See [Authenticate to use the Online Management API](authentication.md) to know about setting these headers in your request.

### <a name="response-headers"></a>Response headers

| Dòng đầu trang | Mô tả  |
|--------|--------------|
|**Operation-Location**|For long-running operations, specifies the location of the operation query to check its status. Ví dụ:<br />`https://admin.services.crm.dynamics.com/operations/{operationid}`|
|**Retry-After**|For long-running operations, specifies the recommended period in seconds after which to query the operation status again. For example: **30**|
    
### <a name="related-topics"></a>Related Topics  

[Authenticate to use Online Management API](authentication.md)

[Operations supported by Online Management API](operations-supported.md)

[Online Management API Reference](/rest/api/admin.services.crm.dynamics.com)
