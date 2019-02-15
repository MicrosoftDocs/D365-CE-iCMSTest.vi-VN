---
title: Stylesheet (XSL) web resources (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about using Stylesheet (XSL) Web resources to transform XML data.
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
- web resource, xsl
ms.assetid: 35b82c28-943d-40aa-8c1d-70de5c7d0f98
caps.latest.revision: 17
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: bd252ca801650fbedc055072346c6e973fd66d00
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385915"
---
# <a name="stylesheet-xsl-web-resources"></a><span data-ttu-id="a5e73-103">Stylesheet (XSL) web resources</span><span class="sxs-lookup"><span data-stu-id="a5e73-103">Stylesheet (XSL) web resources</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a5e73-104">Use Stylesheet (XSL) Web resources to transform XML data.</span><span class="sxs-lookup"><span data-stu-id="a5e73-104">Use Stylesheet (XSL) Web resources to transform XML data.</span></span>  
  
## <a name="capabilities-of-xsl-web-resources"></a><span data-ttu-id="a5e73-105">Capabilities of XSL Web resources</span><span class="sxs-lookup"><span data-stu-id="a5e73-105">Capabilities of XSL Web resources</span></span>  
 <span data-ttu-id="a5e73-106">Use XSL Web resources to transform XML data used by your solution.</span><span class="sxs-lookup"><span data-stu-id="a5e73-106">Use XSL Web resources to transform XML data used by your solution.</span></span>  
  
 <span data-ttu-id="a5e73-107">The following Web resources work together to render a page that displays a table using the data in the XML Web resource.</span><span class="sxs-lookup"><span data-stu-id="a5e73-107">The following Web resources work together to render a page that displays a table using the data in the XML Web resource.</span></span> <span data-ttu-id="a5e73-108">The source files for these Web resources are part of the Import Web Resources sample under the **filestoimport** folder.</span><span class="sxs-lookup"><span data-stu-id="a5e73-108">The source files for these Web resources are part of the Import Web Resources sample under the **filestoimport** folder.</span></span> <span data-ttu-id="a5e73-109">Download the sample of [Import files as web resources](https://code.msdn.microsoft.com/Import-files-as-web-f84ad8dc).</span><span class="sxs-lookup"><span data-stu-id="a5e73-109">Download the sample of [Import files as web resources](https://code.msdn.microsoft.com/Import-files-as-web-f84ad8dc).</span></span>  
  
 <span data-ttu-id="a5e73-110">**HTML Web resource:** sample_/ImportWebResources/Content/ShowData.htm</span><span class="sxs-lookup"><span data-stu-id="a5e73-110">**HTML Web resource:** sample_/ImportWebResources/Content/ShowData.htm</span></span>  
 ```html  
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">  
<html>  
<head>  
 <title></title>  
 <script src="Script/Script.js" type="text/javascript"></script>  
 <link href="CSS/Styles.css" rel="stylesheet" type="text/css" />  
</head>  
<body onload="SDK.ImportWebResources.showData()">  
 <div id="results" />  
</body>  
</html>  
```  
  
 <span data-ttu-id="a5e73-111">**XSL Web resource:** sample_/ImportWebResources/XSL/Transform.xslt</span><span class="sxs-lookup"><span data-stu-id="a5e73-111">**XSL Web resource:** sample_/ImportWebResources/XSL/Transform.xslt</span></span>  
 ```xml  
<?xml version="1.0" encoding="utf-8"?>  
<xsl:stylesheet version="1.0"  
                xmlns:xsl="http://www.w3.org/1999/XSL/Transform"  
                xmlns:msxsl="urn:schemas-microsoft-com:xslt"  
                exclude-result-prefixes="msxsl"  
>  
 <xsl:output method="xml"  
             indent="yes"/>  
  
 <xsl:template match="@* | node()">  
  <xsl:copy>  
   <xsl:apply-templates select="@* | node()"/>  
  </xsl:copy>  
 </xsl:template>  
  
 <xsl:template match="people">  
  <xsl:element name="table">  
   <xsl:element name="thead">  
    <xsl:element name="tr">  
     <xsl:element name="th">  
      <xsl:text>First Name</xsl:text>  
     </xsl:element>  
     <xsl:element name="th">  
      <xsl:text>Last Name</xsl:text>  
     </xsl:element>  
    </xsl:element>  
   </xsl:element>  
   <xsl:element name="tbody">  
    <xsl:apply-templates />  
   </xsl:element>  
  </xsl:element>  
  
 </xsl:template>  
  
 <xsl:template match="person">  
  <xsl:element name="tr">  
   <xsl:element name="td">  
    <xsl:value-of select="@firstName"/>  
   </xsl:element>  
   <xsl:element name="td">  
    <xsl:value-of select="@lastName"/>  
   </xsl:element>  
  </xsl:element>  
  
 </xsl:template>  
  
</xsl:stylesheet>  
  
```  
  
 <span data-ttu-id="a5e73-112">**XML Web resource:** sample_/ImportWebResources/Data/Data.xml</span><span class="sxs-lookup"><span data-stu-id="a5e73-112">**XML Web resource:** sample_/ImportWebResources/Data/Data.xml</span></span>  
 ```xml  
<?xml version="1.0" encoding="utf-8" ?>  
<people>  
 <person firstName="Apurva"  
         lastName="Dalia" />  
 <person firstName="Ofer"  
         lastName="Daliot" />  
 <person firstName="Jim"  
         lastName="Daly" />  
 <person firstName="Ryan"  
         lastName="Danner" />  
 <person firstName="Mike"  
         lastName="Danseglio" />  
 <person firstName="Alex"  
         lastName="Darrow" />  
</people>  
```  
  
 <span data-ttu-id="a5e73-113">**Script Web resource:** sample_/ImportWebResources/Script/Script.js</span><span class="sxs-lookup"><span data-stu-id="a5e73-113">**Script Web resource:** sample_/ImportWebResources/Script/Script.js</span></span>  
 ```javascript  
//If the SDK namespace object is not defined, create it.  
if (typeof (SDK) == "undefined")  
{ SDK = {}; }  
// Create Namespace container for functions in this library;  
SDK.ImportWebResources = {  
 dataFile: "Data/Data.xml",  
 transformFile: "XSL/Transform.xslt",  
 showData: function () {  
  
  //Create an XML document from the Data.xml file  
  var dataXml = new ActiveXObject("Msxml2.DOMDocument.6.0");  
  dataXml.async = false;  
  dataXml.load(this.dataFile);  
  
  //Create an XML document from the Transform.xslt file  
  var transformXSLT = new ActiveXObject("Msxml2.DOMDocument.6.0");  
  transformXSLT.async = false;  
  transformXSLT.load(this.transformFile);  
  
  // Set the innerHTML of the results area to the output of the transformation.  
  var resultsArea = document.getElementById("results");  
  resultsArea.innerHTML = dataXml.transformNode(transformXSLT);  
 }  
  
}  
```  
  
 <span data-ttu-id="a5e73-114">**CSS Web resource:** sample_/ImportWebResources/CSS/Styles.css</span><span class="sxs-lookup"><span data-stu-id="a5e73-114">**CSS Web resource:** sample_/ImportWebResources/CSS/Styles.css</span></span>  
 ```css
body  
{  
    font-family: Calibri;  
}  
table  
{  
    border: 1px solid gray;  
    border-collapse: collapse;  
}  
th  
{  
    text-align: left;  
    border: 1px solid gray;  
}  
td  
{  
    border: 1px solid gray;  
}  
```  
  
### <a name="see-also"></a><span data-ttu-id="a5e73-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a5e73-115">See also</span></span>  
 <span data-ttu-id="a5e73-116">[Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="a5e73-116">[Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md) </span></span>  
 <span data-ttu-id="a5e73-117">[Using Web Page (HTML) Web Resources](webpage-html-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="a5e73-117">[Using Web Page (HTML) Web Resources](webpage-html-web-resources.md) </span></span>  
 <span data-ttu-id="a5e73-118">[Using Style Sheet (CSS) Web Resources](css-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="a5e73-118">[Using Style Sheet (CSS) Web Resources](css-web-resources.md) </span></span>  
 <span data-ttu-id="a5e73-119">[Using Script (JScript) Web Resources](script-jscript-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="a5e73-119">[Using Script (JScript) Web Resources](script-jscript-web-resources.md) </span></span>  
 <span data-ttu-id="a5e73-120">[Using Data (XML) Web Resources](data-xml-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="a5e73-120">[Using Data (XML) Web Resources](data-xml-web-resources.md) </span></span>  
 <span data-ttu-id="a5e73-121">[Using Image (JPG, PNG, GIF) Web Resources](image-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="a5e73-121">[Using Image (JPG, PNG, GIF) Web Resources](image-web-resources.md) </span></span>  
 [<span data-ttu-id="a5e73-122">Using Silverlight (XAP) Web Resources</span><span class="sxs-lookup"><span data-stu-id="a5e73-122">Using Silverlight (XAP) Web Resources</span></span>](silverlight-xap-web-resources.md)
