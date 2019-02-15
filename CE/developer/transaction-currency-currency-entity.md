---
title: Transaction Currency (currency) entity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about transaction curreny, which is a multicurrency feature enabling users to perform financial transactions in multiple currencies. Multiple records in different transaction currencies can be aggregated, compared, or analyzed with regard to a single currency using the base currency.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- transaction currency (currency) entity, associating currency to specific records
- transaction currency properties, actions you can perform
- transaction currency, definition
- transaction currency (currency) entity, transaction currency
- transaction currency (currency) entity, multicurrency system
- transaction currency (currency) entity, supported entities
- multicurrency system, definition
- exchange rate, definition
- transaction currency (currency) entity, decimal precision
- multicurrency system, transaction currency (currency) entity
- transaction currency (currency) entity, introduction
- associating currency to specific records, transaction currency (currency) entity
- base currency, definition
ms.assetid: 9439baba-166c-4779-be3c-2c52833e01b0
caps.latest.revision: 16
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ea4e4aaa548e30aad7a6b65e7965a87d84c22be8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385878"
---
# <a name="transaction-currency-currency-entity"></a><span data-ttu-id="7abc6-104">Transaction Currency (currency) entity</span><span class="sxs-lookup"><span data-stu-id="7abc6-104">Transaction Currency (currency) entity</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] <span data-ttu-id="7abc6-105">là một hệ thống nhiều loại tiền tệ, trong đó mỗi bản ghi có thể được kết hợp với loại tiền tệ riêng của mình.</span><span class="sxs-lookup"><span data-stu-id="7abc6-105">is a multicurrency system, in which each record can be associated with its own currency.</span></span> <span data-ttu-id="7abc6-106">This currency is called the *transaction* currency.</span><span class="sxs-lookup"><span data-stu-id="7abc6-106">This currency is called the *transaction* currency.</span></span> <span data-ttu-id="7abc6-107">The multicurrency features enable users to perform financial transactions like opportunities, quotes, orders, and invoices in multiple currencies.</span><span class="sxs-lookup"><span data-stu-id="7abc6-107">The multicurrency features enable users to perform financial transactions like opportunities, quotes, orders, and invoices in multiple currencies.</span></span> <span data-ttu-id="7abc6-108">This feature also provides a currency choice to the end user when a financial transaction occurs.</span><span class="sxs-lookup"><span data-stu-id="7abc6-108">This feature also provides a currency choice to the end user when a financial transaction occurs.</span></span>  
  
 <span data-ttu-id="7abc6-109">Multiple records in different transaction currencies can be aggregated, compared, or analyzed with regard to a single currency, by using an exchange rate.</span><span class="sxs-lookup"><span data-stu-id="7abc6-109">Multiple records in different transaction currencies can be aggregated, compared, or analyzed with regard to a single currency, by using an exchange rate.</span></span> <span data-ttu-id="7abc6-110">This is known as the *base currency*.</span><span class="sxs-lookup"><span data-stu-id="7abc6-110">This is known as the *base currency*.</span></span> <span data-ttu-id="7abc6-111">You first define a base currency for the organization and then define exchange rates to associate the base currency with transaction currencies.</span><span class="sxs-lookup"><span data-stu-id="7abc6-111">You first define a base currency for the organization and then define exchange rates to associate the base currency with transaction currencies.</span></span> <span data-ttu-id="7abc6-112">The base currency is the currency in which other currencies are quoted.</span><span class="sxs-lookup"><span data-stu-id="7abc6-112">The base currency is the currency in which other currencies are quoted.</span></span> <span data-ttu-id="7abc6-113">The exchange rate is the value of a transaction currency equal to one base currency.</span><span class="sxs-lookup"><span data-stu-id="7abc6-113">The exchange rate is the value of a transaction currency equal to one base currency.</span></span>  
  
 <span data-ttu-id="7abc6-114">By using the transaction currency properties you can do the following:</span><span class="sxs-lookup"><span data-stu-id="7abc6-114">By using the transaction currency properties you can do the following:</span></span>  
  
- <span data-ttu-id="7abc6-115">Select the currency in which you want to define and transact opportunities, quotes, orders, and invoices.</span><span class="sxs-lookup"><span data-stu-id="7abc6-115">Select the currency in which you want to define and transact opportunities, quotes, orders, and invoices.</span></span>  
  
- <span data-ttu-id="7abc6-116">Define currency exchange rates relative to the base currency.</span><span class="sxs-lookup"><span data-stu-id="7abc6-116">Define currency exchange rates relative to the base currency.</span></span>  
  
- <span data-ttu-id="7abc6-117">Define transaction currencies and define an exchange rate to associate the base currency with the transaction currency.</span><span class="sxs-lookup"><span data-stu-id="7abc6-117">Define transaction currencies and define an exchange rate to associate the base currency with the transaction currency.</span></span>  
  
- <span data-ttu-id="7abc6-118">Capture the value of the transaction in the base currency and the transaction currency in all financial transactions.</span><span class="sxs-lookup"><span data-stu-id="7abc6-118">Capture the value of the transaction in the base currency and the transaction currency in all financial transactions.</span></span>  
  
- <span data-ttu-id="7abc6-119">Define product pricelists for each currency.</span><span class="sxs-lookup"><span data-stu-id="7abc6-119">Define product pricelists for each currency.</span></span>  
  
  <span data-ttu-id="7abc6-120">To use multiple currencies, the base currency must be defined for an organization during server installation and organization setup.</span><span class="sxs-lookup"><span data-stu-id="7abc6-120">To use multiple currencies, the base currency must be defined for an organization during server installation and organization setup.</span></span> <span data-ttu-id="7abc6-121">After the base currency is set for an organization, it cannot be changed.</span><span class="sxs-lookup"><span data-stu-id="7abc6-121">After the base currency is set for an organization, it cannot be changed.</span></span> <span data-ttu-id="7abc6-122">This value is stored in the `Organization.BaseCurrencyID` attribute.</span><span class="sxs-lookup"><span data-stu-id="7abc6-122">This value is stored in the `Organization.BaseCurrencyID` attribute.</span></span>  
  
  <span data-ttu-id="7abc6-123">Transaction currencies are defined as a part of the system settings.</span><span class="sxs-lookup"><span data-stu-id="7abc6-123">Transaction currencies are defined as a part of the system settings.</span></span> <span data-ttu-id="7abc6-124">An unlimited number of transaction currencies can be defined.</span><span class="sxs-lookup"><span data-stu-id="7abc6-124">An unlimited number of transaction currencies can be defined.</span></span> <span data-ttu-id="7abc6-125">Transaction currencies are related to the base currency with the definition of a currency exchange rate.</span><span class="sxs-lookup"><span data-stu-id="7abc6-125">Transaction currencies are related to the base currency with the definition of a currency exchange rate.</span></span>  
  
  <span data-ttu-id="7abc6-126">After the definition of base and transaction currencies, pricelists must be defined.</span><span class="sxs-lookup"><span data-stu-id="7abc6-126">After the definition of base and transaction currencies, pricelists must be defined.</span></span> <span data-ttu-id="7abc6-127">An organization can have multiple pricelists, which are also typically defined for a target geographical market in the local currency.</span><span class="sxs-lookup"><span data-stu-id="7abc6-127">An organization can have multiple pricelists, which are also typically defined for a target geographical market in the local currency.</span></span>  
  
  <span data-ttu-id="7abc6-128">All entities that are involved in financial transactions support transaction currency.</span><span class="sxs-lookup"><span data-stu-id="7abc6-128">All entities that are involved in financial transactions support transaction currency.</span></span> <span data-ttu-id="7abc6-129">The currency is typically inherited from the account, opportunity, and so on, but can be changed as needed.</span><span class="sxs-lookup"><span data-stu-id="7abc6-129">The currency is typically inherited from the account, opportunity, and so on, but can be changed as needed.</span></span>  
  
  <span data-ttu-id="7abc6-130">You can specify the decimal precision for the transaction currency by using the `TransactionCurrency.CurrencyPrecision` attribute.</span><span class="sxs-lookup"><span data-stu-id="7abc6-130">You can specify the decimal precision for the transaction currency by using the `TransactionCurrency.CurrencyPrecision` attribute.</span></span> <span data-ttu-id="7abc6-131">To specify the source of the precision for the attributes of type Money, use the <xref:Microsoft.Xrm.Sdk.Metadata.MoneyAttributeMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.MoneyAttributeMetadata.PrecisionSource></span><span class="sxs-lookup"><span data-stu-id="7abc6-131">To specify the source of the precision for the attributes of type Money, use the <xref:Microsoft.Xrm.Sdk.Metadata.MoneyAttributeMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.MoneyAttributeMetadata.PrecisionSource></span></span> <span data-ttu-id="7abc6-132">attribute.</span><span class="sxs-lookup"><span data-stu-id="7abc6-132">attribute.</span></span>  
  
  <span data-ttu-id="7abc6-133">All money properties in a record share the same transaction currency, for example, see the `Account.CreditLimit` attribute.</span><span class="sxs-lookup"><span data-stu-id="7abc6-133">All money properties in a record share the same transaction currency, for example, see the `Account.CreditLimit` attribute.</span></span> <span data-ttu-id="7abc6-134">For each money attribute in an entity, [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] automatically creates a corresponding read-only, system calculated, money attribute that is called the "base".</span><span class="sxs-lookup"><span data-stu-id="7abc6-134">For each money attribute in an entity, [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] automatically creates a corresponding read-only, system calculated, money attribute that is called the "base".</span></span> <span data-ttu-id="7abc6-135">This is a money attribute that stores the value of the corresponding attribute in a base currency equivalent, for example, see the `Account.CreditLimit_Base` attribute.</span><span class="sxs-lookup"><span data-stu-id="7abc6-135">This is a money attribute that stores the value of the corresponding attribute in a base currency equivalent, for example, see the `Account.CreditLimit_Base` attribute.</span></span>  
  
  <span data-ttu-id="7abc6-136">The following formula is used to calculate the base value:</span><span class="sxs-lookup"><span data-stu-id="7abc6-136">The following formula is used to calculate the base value:</span></span>  
  
```csharp  
creditlimit_base = creditlimit / exchangerate  
```  
  
 <span data-ttu-id="7abc6-137">The following are the entities for which the transaction currency can be defined.</span><span class="sxs-lookup"><span data-stu-id="7abc6-137">The following are the entities for which the transaction currency can be defined.</span></span>  
  
-   <span data-ttu-id="7abc6-138">Khách hàng</span><span class="sxs-lookup"><span data-stu-id="7abc6-138">Account</span></span>  
  
-   <span data-ttu-id="7abc6-139">AnnualFiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="7abc6-139">AnnualFiscalCalendar</span></span>  
  
-   <span data-ttu-id="7abc6-140">Chiến dịch</span><span class="sxs-lookup"><span data-stu-id="7abc6-140">Campaign</span></span>  
  
-   <span data-ttu-id="7abc6-141">CampaignActivity</span><span class="sxs-lookup"><span data-stu-id="7abc6-141">CampaignActivity</span></span>  
  
-   <span data-ttu-id="7abc6-142">Đối thủ cạnh tranh</span><span class="sxs-lookup"><span data-stu-id="7abc6-142">Competitor</span></span>  
  
-   <span data-ttu-id="7abc6-143">người liên hệ</span><span class="sxs-lookup"><span data-stu-id="7abc6-143">Contact</span></span>  
  
-   <span data-ttu-id="7abc6-144">Hợp đồng</span><span class="sxs-lookup"><span data-stu-id="7abc6-144">Contract</span></span>  
  
-   <span data-ttu-id="7abc6-145">ContractDetail</span><span class="sxs-lookup"><span data-stu-id="7abc6-145">ContractDetail</span></span>  
  
-   <span data-ttu-id="7abc6-146">Giảm giá</span><span class="sxs-lookup"><span data-stu-id="7abc6-146">Discount</span></span>  
  
-   <span data-ttu-id="7abc6-147">DiscountType</span><span class="sxs-lookup"><span data-stu-id="7abc6-147">DiscountType</span></span>  
  
-   <span data-ttu-id="7abc6-148">FixedMonthlyFiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="7abc6-148">FixedMonthlyFiscalCalendar</span></span>  
  
-   <span data-ttu-id="7abc6-149">Hóa đơn</span><span class="sxs-lookup"><span data-stu-id="7abc6-149">Invoice</span></span>  
  
-   <span data-ttu-id="7abc6-150">InvoiceDetail</span><span class="sxs-lookup"><span data-stu-id="7abc6-150">InvoiceDetail</span></span>  
  
-   <span data-ttu-id="7abc6-151">Khách hàng tiềm năng</span><span class="sxs-lookup"><span data-stu-id="7abc6-151">Lead</span></span>  
  
-   <span data-ttu-id="7abc6-152">Danh sách</span><span class="sxs-lookup"><span data-stu-id="7abc6-152">List</span></span>  
  
-   <span data-ttu-id="7abc6-153">MonthlyFiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="7abc6-153">MonthlyFiscalCalendar</span></span>  
  
-   <span data-ttu-id="7abc6-154">Cơ hội</span><span class="sxs-lookup"><span data-stu-id="7abc6-154">Opportunity</span></span>  
  
-   <span data-ttu-id="7abc6-155">OpportunityClose</span><span class="sxs-lookup"><span data-stu-id="7abc6-155">OpportunityClose</span></span>  
  
-   <span data-ttu-id="7abc6-156">OpportunityProduct</span><span class="sxs-lookup"><span data-stu-id="7abc6-156">OpportunityProduct</span></span>  
  
-   <span data-ttu-id="7abc6-157">PriceLevel</span><span class="sxs-lookup"><span data-stu-id="7abc6-157">PriceLevel</span></span>  
  
-   <span data-ttu-id="7abc6-158">Sản phẩm</span><span class="sxs-lookup"><span data-stu-id="7abc6-158">Product</span></span>  
  
-   <span data-ttu-id="7abc6-159">ProductPriceLevel</span><span class="sxs-lookup"><span data-stu-id="7abc6-159">ProductPriceLevel</span></span>  
  
-   <span data-ttu-id="7abc6-160">QuarterlyFiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="7abc6-160">QuarterlyFiscalCalendar</span></span>  
  
-   <span data-ttu-id="7abc6-161">Báo giá</span><span class="sxs-lookup"><span data-stu-id="7abc6-161">Quote</span></span>  
  
-   <span data-ttu-id="7abc6-162">QuoteDetail</span><span class="sxs-lookup"><span data-stu-id="7abc6-162">QuoteDetail</span></span>  
  
-   <span data-ttu-id="7abc6-163">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="7abc6-163">SalesOrder</span></span>  
  
-   <span data-ttu-id="7abc6-164">SalesOrderDetail</span><span class="sxs-lookup"><span data-stu-id="7abc6-164">SalesOrderDetail</span></span>  
  
-   <span data-ttu-id="7abc6-165">SemiAnnualFiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="7abc6-165">SemiAnnualFiscalCalendar</span></span>  
  
-   <span data-ttu-id="7abc6-166">UserSettings</span><span class="sxs-lookup"><span data-stu-id="7abc6-166">UserSettings</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="7abc6-167">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="7abc6-167">See also</span></span>  
 <span data-ttu-id="7abc6-168">[TransactionCurrency Entity](entities/transactioncurrency.md) </span><span class="sxs-lookup"><span data-stu-id="7abc6-168">[TransactionCurrency Entity](entities/transactioncurrency.md) </span></span>  
 <span data-ttu-id="7abc6-169">[Sample: Retrieve Currency Exchange Rate](sample-retrieve-currency-exchange-rate.md) </span><span class="sxs-lookup"><span data-stu-id="7abc6-169">[Sample: Retrieve Currency Exchange Rate](sample-retrieve-currency-exchange-rate.md) </span></span>  
 [<span data-ttu-id="7abc6-170">Business Management Entities</span><span class="sxs-lookup"><span data-stu-id="7abc6-170">Business Management Entities</span></span>](business-management-entities.md)
