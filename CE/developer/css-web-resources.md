---
title: CSS web resources (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: 'Learn about using cascading style sheet (CSS) web resources to create style sheets for use in webpage web resources. '
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
- web resource, css
ms.assetid: 7794a5f1-2055-426b-985b-c9ad23fcd1ad
caps.latest.revision: 16
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 19017663ac3982ab6e10a4df744c5c216466d16f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385908"
---
# <a name="css-web-resources"></a>CSS web resources

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

Use cascading style sheet (CSS) web resources to create style sheets for use in webpage web resources.  
  
## <a name="capabilities-of-css-web-resources"></a>Capabilities of CSS web resources  
 With CSS web resources, you can manage the appearance of webpage web resources by linking them to a shared library of CSS styles.  
  
### <a name="limitations-of-css-web-resources"></a>Limitations of CSS web resources  
 Like all web resources, CSS web resources are only available in the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps security context. Only licensed [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps users who have the necessary privileges can access them.  
  
## <a name="referencing-a-style-sheet-web-resource-from-a-webpage-web-resource"></a>Referencing a style sheet web resource from a webpage web resource  
 All web resources can use relative URLs to reference each other. In the following example, for the webpage web resource `sample_/content/contentpage.htm` to reference the style sheet web resource `sample_/styles/styles.css`, add the following example to the head element of sample_/content/contentpage.htm:  
  
```html  
<link rel="stylesheet" type="text/css" href="../styles/styles.css" />  
```  
  
 To reference a style sheet from a different publisher, the path must include that solution publisher customization prefix. For example, for the `sample_/content/contentpage.htm` page to reference the `MyIsv_/styles/styles.css` page, the href parameter value should be `../../MyIsv_/styles/styles.css`.  
  
> [!NOTE]
>  References included in code between web resources aren’t tracked as solution dependencies.  
  
### <a name="see-also"></a>Xem thêm  
 [Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md)   
 [Using Web Page (HTML) Web Resources](webpage-html-web-resources.md)   
 [Using Script (JScript) Web Resources](script-jscript-web-resources.md)   
 [Using Data (XML) Web Resources](data-xml-web-resources.md)   
 [Using Image (JPG, PNG, GIF) Web Resources](image-web-resources.md)   
 [Using Silverlight (XAP) Web Resources](silverlight-xap-web-resources.md)   
 [Using Stylesheet (XSL) Web Resources](stylesheet-xsl-web-resources.md)   
 [WebResource Entity](entities/webresource.md)
