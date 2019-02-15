---
title: Pass Dynamics 365 URL to widget library| Microsoft Docs
description: Read how you can pass the URL of your Dynamics 365 instance to the widget library inside your widget iframe to be able to use CIF's APIs.
keywords: ''
ms.date: 12/10/2018
ms.service:
- dynamics-365-cross-app
ms.custom:
- dyn365-a11y
- dyn365-developer
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement Version 9.x
ms.assetid: CBA9588C-5CF7-4FE5-A92E-6091FD8940EC
author: susikka
ms.author: susikka
manager: shujoshi
ms.openlocfilehash: b8f811aded75b3dd348136a39d094dae8f7505cf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387926"
---
# <a name="pass-a-dynamics-365-url-to-a-widget-library"></a><span data-ttu-id="752a7-103">Pass a Dynamics 365 URL to a widget library</span><span class="sxs-lookup"><span data-stu-id="752a7-103">Pass a Dynamics 365 URL to a widget library</span></span>

<span data-ttu-id="752a7-104">To access the Dynamics 365 Channel Integration Framework (CIF) APIs, you need to load the `msdyn_cilibrary.js` file inside your communication widget.</span><span class="sxs-lookup"><span data-stu-id="752a7-104">To access the Dynamics 365 Channel Integration Framework (CIF) APIs, you need to load the `msdyn_cilibrary.js` file inside your communication widget.</span></span> <span data-ttu-id="752a7-105">Since the widget is in a different domain, this library needs to know what Dynamics 365 domain it should talk to.</span><span class="sxs-lookup"><span data-stu-id="752a7-105">Since the widget is in a different domain, this library needs to know what Dynamics 365 domain it should talk to.</span></span> <span data-ttu-id="752a7-106">For this reason you need to pass your Dynamics 365 instance URL to the widget library.</span><span class="sxs-lookup"><span data-stu-id="752a7-106">For this reason you need to pass your Dynamics 365 instance URL to the widget library.</span></span>

<span data-ttu-id="752a7-107">There are two ways to pass a Dynamics 365 URL to a widget library.</span><span class="sxs-lookup"><span data-stu-id="752a7-107">There are two ways to pass a Dynamics 365 URL to a widget library.</span></span>

## <a name="1-add-attributes-to-the-script-tag"></a><span data-ttu-id="752a7-108">1. Add attributes to the script tag</span><span class="sxs-lookup"><span data-stu-id="752a7-108">1. Add attributes to the script tag</span></span>

<span data-ttu-id="752a7-109">The widget provider has to add the following attributes to the script tag that loads `msdyn_cilibrary.js` to pass the Dynamics 365 domain:</span><span class="sxs-lookup"><span data-stu-id="752a7-109">The widget provider has to add the following attributes to the script tag that loads `msdyn_cilibrary.js` to pass the Dynamics 365 domain:</span></span>

`data-cifid: CIFMainLibrary` <br />
`data-crmurl: <CRM domain name>`

### <a name="example"></a><span data-ttu-id="752a7-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="752a7-110">Example</span></span>

```html
<script type="text/javascript" src="https://crmorg.crm.dynamics.com/webresources/Widget/msdyn_ciLibrary.js" onload="ciLoadDone();" data-crmurl="https://crmorg.crm.dynamics.com" data-cifid="CIFMainLibrary">
</script>
```

## <a name="2-add-a-url-parameter"></a><span data-ttu-id="752a7-111">2. Add a URL parameter</span><span class="sxs-lookup"><span data-stu-id="752a7-111">2. Add a URL parameter</span></span>

<span data-ttu-id="752a7-112">Another method is to pass a `ucilib` parameter in the landing URL, like `ucilib=https://crmorg.crm.dynamics.com/webresources/Widget/msdyn_ciLibrary.js`.</span><span class="sxs-lookup"><span data-stu-id="752a7-112">Another method is to pass a `ucilib` parameter in the landing URL, like `ucilib=https://crmorg.crm.dynamics.com/webresources/Widget/msdyn_ciLibrary.js`.</span></span>

### <a name="example"></a><span data-ttu-id="752a7-113">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="752a7-113">Example</span></span>

`https://widget.domain.com?ucilib=https://crmorg.crm.dynamics.com/webresources/Widget/msdyn_ciLibrary.js`

## <a name="see-also"></a><span data-ttu-id="752a7-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="752a7-114">See also</span></span>

[<span data-ttu-id="752a7-115">Configure a channel provider for your Dynamics 365 organization</span><span class="sxs-lookup"><span data-stu-id="752a7-115">Configure a channel provider for your Dynamics 365 organization</span></span>](configure-channel-provider-channel-integration-framework.md)<br />
[<span data-ttu-id="752a7-116">Enable outbound communication (ClickToAct)</span><span class="sxs-lookup"><span data-stu-id="752a7-116">Enable outbound communication (ClickToAct)</span></span>](enable-outbound-communication-clicktoact.md)<br />
[<span data-ttu-id="752a7-117">Add a Channel Integration Framework solution as a dependent solution</span><span class="sxs-lookup"><span data-stu-id="752a7-117">Add a Channel Integration Framework solution as a dependent solution</span></span>](add-cif-solution-dependent-solution.md)<br />
[<span data-ttu-id="752a7-118">Authenticate channel users to the channel (widget)</span><span class="sxs-lookup"><span data-stu-id="752a7-118">Authenticate channel users to the channel (widget)</span></span>](authenticate-channel-users.md)
