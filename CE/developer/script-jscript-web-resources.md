---
title: Script(JScript) web resources (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: 'Learn about using JavaScript web resources to create a library of JavaScript functions that can be accessed from anywhere. '
ms.custom: ''
ms.date: 03/02/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- web resource, Jscript
ms.assetid: 882565b5-aa86-475e-971a-b5123bbadcf9
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 432b07d6eba58f408ee5af0e1cc9aa9b9345d9c1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387207"
---
# <a name="scriptjscript-web-resources"></a>Script(JScript) web resources

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

Use Script(JScript) web resources to create a library of [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] functions that can be accessed from anywhere.  
  
<a name="BKMK_capabilities"></a>   
## <a name="capabilities-of-script-web-resources"></a>Capabilities of script web resources  
 With [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] web resources, you can more efficiently manage code used in form scripts, webpage (HTML) web resources, or ribbon commands by linking them to shared library of [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] functions.  
  
<a name="BKMK_limitations"></a>   
## <a name="limitations-of-script-web-resources"></a>Limitations of script web resources  
 Like all web resources, [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] web resources use the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] web application security context. Only licensed [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] users who have the necessary privileges can access them.  
  
> [!NOTE]
>  References included in code between web resources aren’t tracked as solution dependencies.  
  
<a name="BKMK_Using"></a>   
## <a name="using-javascript-libraries"></a>Using JavaScript libraries  
 For information about developing and testing [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] libraries as well as how to associate them with ribbon commands and form events, see [Client scripting in Customer Engagement using JavaScript](clientapi/client-scripting.md).  
  
<a name="BKMK_Referencing"></a>   
## <a name="referencing-a-script-web-resource-from-a-webpage-web-resource"></a>Referencing a script web resource from a webpage web resource  
 All web resources can use relative URLs to reference each other. In the following example, for the webpage web resource `new_/content/contentpage.htm` to reference the [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] web resource `new_/scripts/myScript.js`, add the following HTML code to the head element of `new_/content/contentpage.htm`.  
  
```html  
<script type="text/jscript" src="../scripts/myScript.js"></script>  
```  
  
 To reference a [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] from a different publisher, the path must include the customization prefix for that publisher. For example, for the `new_/content/contentpage.htm` page to reference the `MyIsv_/scripts/customscripts.js` page, the `src` attribute value should be `../../MyIsv_/scripts/customscripts.js`.  
  
### <a name="see-also"></a>Xem thêm  
 [Use JavaScript with Customer Engagement apps](use-javascript.md)   
 [Client scripting in Customer Engagement apps using JavaScript](clientapi/client-scripting.md)   
 [Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md)   
 [Using Web Page (HTML) Web Resources](webpage-html-web-resources.md)   
 [Using Style Sheet (CSS) Web Resources](css-web-resources.md)   
 [Using Data (XML) Web Resources](data-xml-web-resources.md)   
 [Using Image (JPG, PNG, GIF) Web Resources](image-web-resources.md)   
 [Using Silverlight (XAP) Web Resources](silverlight-xap-web-resources.md)   
 [Using Stylesheet (XSL) Web Resources](stylesheet-xsl-web-resources.md)   
 [Streamline web resource development using Fiddler AutoResponder](streamline-javascript-development-fiddler-autoresponder.md)    
