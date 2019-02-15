---
title: Define ribbon actions (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: 'Learn about defining the actions to be performed by a command bar or ribbon control in a <CommandDefinition> element together with rules that control whether the control is enabled or visible in the ribbon. '
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
- ribbon, control actions
ms.assetid: 350e6c40-d277-4aba-9619-5e007a67e477
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7bea4871ea768a94af270d93f1e66b34fb45753f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386660"
---
# <a name="define-ribbon-actions"></a><span data-ttu-id="75e3e-103">Define ribbon actions</span><span class="sxs-lookup"><span data-stu-id="75e3e-103">Define ribbon actions</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="75e3e-104">Define the actions to be performed by a command bar or ribbon control in a `<CommandDefinition>` element together with rules that control whether the control is enabled or visible in the ribbon.</span><span class="sxs-lookup"><span data-stu-id="75e3e-104">Define the actions to be performed by a command bar or ribbon control in a `<CommandDefinition>` element together with rules that control whether the control is enabled or visible in the ribbon.</span></span>  
  
 <span data-ttu-id="75e3e-105">A Ribbon control can perform two types actions and may include multiple actions:</span><span class="sxs-lookup"><span data-stu-id="75e3e-105">A Ribbon control can perform two types actions and may include multiple actions:</span></span>  
  
- <span data-ttu-id="75e3e-106">**JavaScript Functions**: A `<JavaScriptFunction>` element references a function defined in a Script Web resource.</span><span class="sxs-lookup"><span data-stu-id="75e3e-106">**JavaScript Functions**: A `<JavaScriptFunction>` element references a function defined in a Script Web resource.</span></span>  
  
- <span data-ttu-id="75e3e-107">**Open a URL**: The ribbon opens a URL using the value from an Address attribute in the `<Url>` element.</span><span class="sxs-lookup"><span data-stu-id="75e3e-107">**Open a URL**: The ribbon opens a URL using the value from an Address attribute in the `<Url>` element.</span></span> <span data-ttu-id="75e3e-108">Additional parameters can pass information about how what querystring parameters are passed and the mode in which the window opens.</span><span class="sxs-lookup"><span data-stu-id="75e3e-108">Additional parameters can pass information about how what querystring parameters are passed and the mode in which the window opens.</span></span>  
  
     <span data-ttu-id="75e3e-109">You have several options to pass parameters to a URL using the ribbon.</span><span class="sxs-lookup"><span data-stu-id="75e3e-109">You have several options to pass parameters to a URL using the ribbon.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="75e3e-110">[Passing Parameters to a URL using the Ribbon](pass-parameters-url-by-using-ribbon.md)</span><span class="sxs-lookup"><span data-stu-id="75e3e-110">[Passing Parameters to a URL using the Ribbon](pass-parameters-url-by-using-ribbon.md)</span></span>  
  
### <a name="passing-parameters-to-ribbon-actions"></a><span data-ttu-id="75e3e-111">Passing parameters to ribbon actions</span><span class="sxs-lookup"><span data-stu-id="75e3e-111">Passing parameters to ribbon actions</span></span>  
 <span data-ttu-id="75e3e-112">Use the following elements to define data to pass to your custom action:</span><span class="sxs-lookup"><span data-stu-id="75e3e-112">Use the following elements to define data to pass to your custom action:</span></span>  
  
 `<BoolParameter>`  
[!INCLUDE[ribbon_element_BoolParameter](../../includes/ribbon-element-boolparameter.md)]
  
 `<CrmParameter>`  
 [!INCLUDE[ribbon_element_CrmParameter](../../includes/ribbon-element-crmparameter.md)] <span data-ttu-id="75e3e-113">[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Pass Microsoft Dynamics 365 for Customer Engagement data from a page as a parameter to Ribbon Actions](pass-dynamics-365-data-page-parameter-ribbon-actions.md)</span><span class="sxs-lookup"><span data-stu-id="75e3e-113">[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Pass Microsoft Dynamics 365 for Customer Engagement data from a page as a parameter to Ribbon Actions](pass-dynamics-365-data-page-parameter-ribbon-actions.md)</span></span>  
  
 `<DecimalParameter>`  
 [!INCLUDE[ribbon_element_DecimalParameter](../../includes/ribbon-element-decimalparameter.md)]
  
 `<IntParameter>`  
 [!INCLUDE[ribbon_element_IntParameter](../../includes/ribbon-element-intparameter.md)]
  
 `<StringParameter>`  
 [!INCLUDE[ribbon_element_StringParameter](../../includes/ribbon-element-stringparameter.md)]
  
 <span data-ttu-id="75e3e-114">When parameters are passed to a `<Url>` element they are passed as a query string.</span><span class="sxs-lookup"><span data-stu-id="75e3e-114">When parameters are passed to a `<Url>` element they are passed as a query string.</span></span> <span data-ttu-id="75e3e-115">Therefore, they must include a name value to represent the ”key” in the query string key/value pair.</span><span class="sxs-lookup"><span data-stu-id="75e3e-115">Therefore, they must include a name value to represent the ”key” in the query string key/value pair.</span></span>  
  
 <span data-ttu-id="75e3e-116">Parameters passed to a `<JavaScriptFunction>` do not require a name but they must be included in the order expected by the function and be of the correct data type.</span><span class="sxs-lookup"><span data-stu-id="75e3e-116">Parameters passed to a `<JavaScriptFunction>` do not require a name but they must be included in the order expected by the function and be of the correct data type.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="75e3e-117">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="75e3e-117">See also</span></span>  
 <span data-ttu-id="75e3e-118">[Customize commands and the ribbon](customize-commands-ribbon.md) </span><span class="sxs-lookup"><span data-stu-id="75e3e-118">[Customize commands and the ribbon](customize-commands-ribbon.md) </span></span>  
 <span data-ttu-id="75e3e-119">[Define Ribbon Display Rules](define-ribbon-display-rules.md) </span><span class="sxs-lookup"><span data-stu-id="75e3e-119">[Define Ribbon Display Rules](define-ribbon-display-rules.md) </span></span>  
 [<span data-ttu-id="75e3e-120">Pass Microsoft Dynamics 365 for Customer Engagement data from a page as a parameter to Ribbon Actions</span><span class="sxs-lookup"><span data-stu-id="75e3e-120">Pass Microsoft Dynamics 365 for Customer Engagement data from a page as a parameter to Ribbon Actions</span></span>](pass-dynamics-365-data-page-parameter-ribbon-actions.md)
