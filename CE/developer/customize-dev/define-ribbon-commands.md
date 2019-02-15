---
title: Define ribbon commands (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: A Ribbon command creates a reusable definition that can be referenced by ribbon control elements.
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
- ribbon, commands
ms.assetid: 7c6c4d14-428d-4b96-9fe3-5260c3a6ae36
caps.latest.revision: 17
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c66adad64a6100886215440780b139f3a10eab53
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386092"
---
# <a name="define-ribbon-commands"></a><span data-ttu-id="ef40d-103">Define ribbon commands</span><span class="sxs-lookup"><span data-stu-id="ef40d-103">Define ribbon commands</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ef40d-104">A *Ribbon* command creates a reusable definition that can be referenced by ribbon control elements.</span><span class="sxs-lookup"><span data-stu-id="ef40d-104">A *Ribbon* command creates a reusable definition that can be referenced by ribbon control elements.</span></span>  
  
## <a name="ribbon-command-elements"></a><span data-ttu-id="ef40d-105">Ribbon command elements</span><span class="sxs-lookup"><span data-stu-id="ef40d-105">Ribbon command elements</span></span>  
 <span data-ttu-id="ef40d-106">The `<CommandDefinition>` element defines a command in the ribbon.</span><span class="sxs-lookup"><span data-stu-id="ef40d-106">The `<CommandDefinition>` element defines a command in the ribbon.</span></span> <span data-ttu-id="ef40d-107">The `Id` attribute specifies a unique identifier for the command that can be referenced by ribbon control elements by using the `Command` parameter.</span><span class="sxs-lookup"><span data-stu-id="ef40d-107">The `Id` attribute specifies a unique identifier for the command that can be referenced by ribbon control elements by using the `Command` parameter.</span></span>  
  
 <span data-ttu-id="ef40d-108">A ribbon command defines three things:</span><span class="sxs-lookup"><span data-stu-id="ef40d-108">A ribbon command defines three things:</span></span>  
  
- <span data-ttu-id="ef40d-109">**Enable Rules**: Specifies when a specific ribbon control is enabled.</span><span class="sxs-lookup"><span data-stu-id="ef40d-109">**Enable Rules**: Specifies when a specific ribbon control is enabled.</span></span>  
  
- <span data-ttu-id="ef40d-110">**Display Rules**: Specifies when a specific ribbon element is visible.</span><span class="sxs-lookup"><span data-stu-id="ef40d-110">**Display Rules**: Specifies when a specific ribbon element is visible.</span></span>  
  
- <span data-ttu-id="ef40d-111">**Actions**: Specifies what code executes when a ribbon control is used.</span><span class="sxs-lookup"><span data-stu-id="ef40d-111">**Actions**: Specifies what code executes when a ribbon control is used.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="ef40d-112">All command definitions are downloaded to a user's computer so that they can be evaluated at run time.</span><span class="sxs-lookup"><span data-stu-id="ef40d-112">All command definitions are downloaded to a user's computer so that they can be evaluated at run time.</span></span> <span data-ttu-id="ef40d-113">This means that a user without the privileges to see a particular control in the ribbon can use the browser **View Source** command, review the code, and determine that a control exists that isn’t displayed to them in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="ef40d-113">This means that a user without the privileges to see a particular control in the ribbon can use the browser **View Source** command, review the code, and determine that a control exists that isn’t displayed to them in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ef40d-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ef40d-114">See also</span></span>  
 <span data-ttu-id="ef40d-115">[Customize commands and the ribbon](customize-commands-ribbon.md) </span><span class="sxs-lookup"><span data-stu-id="ef40d-115">[Customize commands and the ribbon](customize-commands-ribbon.md) </span></span>  
 <span data-ttu-id="ef40d-116">[Use Localized Labels with Ribbons](use-localized-labels-ribbons.md) </span><span class="sxs-lookup"><span data-stu-id="ef40d-116">[Use Localized Labels with Ribbons](use-localized-labels-ribbons.md) </span></span>  
 [<span data-ttu-id="ef40d-117">Define Ribbon Enable Rules</span><span class="sxs-lookup"><span data-stu-id="ef40d-117">Define Ribbon Enable Rules</span></span>](define-ribbon-enable-rules.md)
