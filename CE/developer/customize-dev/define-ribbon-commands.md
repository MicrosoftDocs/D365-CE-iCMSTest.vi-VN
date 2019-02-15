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
# <a name="define-ribbon-commands"></a>Define ribbon commands

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

A *Ribbon* command creates a reusable definition that can be referenced by ribbon control elements.  
  
## <a name="ribbon-command-elements"></a>Ribbon command elements  
 The `<CommandDefinition>` element defines a command in the ribbon. The `Id` attribute specifies a unique identifier for the command that can be referenced by ribbon control elements by using the `Command` parameter.  
  
 A ribbon command defines three things:  
  
- **Enable Rules**: Specifies when a specific ribbon control is enabled.  
  
- **Display Rules**: Specifies when a specific ribbon element is visible.  
  
- **Actions**: Specifies what code executes when a ribbon control is used.  
  
> [!IMPORTANT]
>  All command definitions are downloaded to a user's computer so that they can be evaluated at run time. This means that a user without the privileges to see a particular control in the ribbon can use the browser **View Source** command, review the code, and determine that a control exists that isn’t displayed to them in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement.  
  
### <a name="see-also"></a>Xem thêm  
 [Customize commands and the ribbon](customize-commands-ribbon.md)   
 [Use Localized Labels with Ribbons](use-localized-labels-ribbons.md)   
 [Define Ribbon Enable Rules](define-ribbon-enable-rules.md)
