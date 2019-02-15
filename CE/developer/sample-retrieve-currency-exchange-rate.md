---
title: 'Sample: Retrieve currency exchange rate (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates how to create a new currency, and how to retrieve and display the currency exchange rate relative to the organization’s base currency.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d071fe46-4d71-4fd1-95b8-069bd4a96f8d
caps.latest.revision: 13
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7b2932256562bab29d60728fce55ca7cdd29ead5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386609"
---
# <a name="sample-retrieve-currency-exchange-rate"></a><span data-ttu-id="b7da7-103">Sample: Retrieve currency exchange rate</span><span class="sxs-lookup"><span data-stu-id="b7da7-103">Sample: Retrieve currency exchange rate</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b7da7-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="b7da7-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="b7da7-105">Download the complete sample here [Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span><span class="sxs-lookup"><span data-stu-id="b7da7-105">Download the complete sample here [Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="b7da7-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="b7da7-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="b7da7-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="b7da7-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="b7da7-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="b7da7-108">Demonstrates</span></span>  
 <span data-ttu-id="b7da7-109">This sample shows how to create a new currency, and how to retrieve and display the currency exchange rate relative to the organization’s base currency.</span><span class="sxs-lookup"><span data-stu-id="b7da7-109">This sample shows how to create a new currency, and how to retrieve and display the currency exchange rate relative to the organization’s base currency.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b7da7-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="b7da7-110">Example</span></span>  
 [!code-csharp[BusinessManagement#TransactionCurrencyExchangeRate](../snippets/csharp/CRMV8/businessmanagement/cs/transactioncurrencyexchangerate.cs#transactioncurrencyexchangerate)]  
  
### <a name="see-also"></a><span data-ttu-id="b7da7-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b7da7-111">See also</span></span>  
 <span data-ttu-id="b7da7-112">[Transaction Currency (Currency) Entity](transaction-currency-currency-entity.md) </span><span class="sxs-lookup"><span data-stu-id="b7da7-112">[Transaction Currency (Currency) Entity](transaction-currency-currency-entity.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveExchangeRateRequest>
