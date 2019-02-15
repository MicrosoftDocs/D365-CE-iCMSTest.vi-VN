---
title: 'Sample: Retrieve field permissions (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample shows how to retrieve secured fields for a user according to the steps outlined in Field security entities.
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- field security entities sample, enabling
- enabling field security, sample
ms.assetid: acb20fc8-4b62-4e92-b105-7d832c56d007
caps.latest.revision: 20
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 27dd9cf089e9adb1880e69d5d90ba263a0ee8156
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386900"
---
# <a name="sample-retrieve-field-permissions"></a><span data-ttu-id="605ec-103">Sample: Retrieve field permissions</span><span class="sxs-lookup"><span data-stu-id="605ec-103">Sample: Retrieve field permissions</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="605ec-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="605ec-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="605ec-105">Download the complete sample here [Work with Field security entities](https://code.msdn.microsoft.com/Work-with-Field-Security-a18489bf).</span><span class="sxs-lookup"><span data-stu-id="605ec-105">Download the complete sample here [Work with Field security entities](https://code.msdn.microsoft.com/Work-with-Field-Security-a18489bf).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="605ec-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="605ec-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="605ec-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="605ec-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="605ec-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="605ec-108">Demonstrates</span></span>  
 <span data-ttu-id="605ec-109">This sample shows how to retrieve secured fields for a user according to the steps outlined in [Field security entities](field-security-entities.md).</span><span class="sxs-lookup"><span data-stu-id="605ec-109">This sample shows how to retrieve secured fields for a user according to the steps outlined in [Field security entities](field-security-entities.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="605ec-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="605ec-110">Example</span></span>  
 [!code-csharp[FieldSecurity#RetrieveSecuredFieldsForAUser1](../snippets/csharp/CRMV8/fieldsecurity/cs/retrievesecuredfieldsforauser1.cs#retrievesecuredfieldsforauser1)]  
  
### <a name="see-also"></a><span data-ttu-id="605ec-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="605ec-111">See also</span></span>  
 <span data-ttu-id="605ec-112">[How Field Security Can Be Used to Control Access to Field Values In Dynamics 365 for Customer Engagement apps](security-dev/use-field-security-control-access-field-values.md) </span><span class="sxs-lookup"><span data-stu-id="605ec-112">[How Field Security Can Be Used to Control Access to Field Values In Dynamics 365 for Customer Engagement apps](security-dev/use-field-security-control-access-field-values.md) </span></span>  
 <span data-ttu-id="605ec-113">[Field Security Entities](field-security-entities.md) </span><span class="sxs-lookup"><span data-stu-id="605ec-113">[Field Security Entities](field-security-entities.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>
