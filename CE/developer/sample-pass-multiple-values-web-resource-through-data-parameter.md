---
title: 'Sample: Pass multiple values to a  web resource through the data parameter (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: The sample represents a technique to pass the additional values within a single parameter and then process them within your web resource.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- web resource, use the data parameter
ms.assetid: 132dc96c-6c02-4caa-a2a9-b27e61f96de3
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8ee37f5f4872d6bce83b85b028240e15a0daea3e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386754"
---
# <a name="sample-pass-multiple-values-to-a--web-resource-through-the-data-parameter"></a><span data-ttu-id="990ca-103">Sample: Pass multiple values to a  web resource through the data parameter</span><span class="sxs-lookup"><span data-stu-id="990ca-103">Sample: Pass multiple values to a  web resource through the data parameter</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="990ca-104">An (HTML) web resource page can only accept a single custom parameter called `data`.</span><span class="sxs-lookup"><span data-stu-id="990ca-104">An (HTML) web resource page can only accept a single custom parameter called `data`.</span></span> <span data-ttu-id="990ca-105">To pass more than one value in the data parameter, you need to encode the parameters and decode the parameters in your page.</span><span class="sxs-lookup"><span data-stu-id="990ca-105">To pass more than one value in the data parameter, you need to encode the parameters and decode the parameters in your page.</span></span>  
  
 <span data-ttu-id="990ca-106">The page here represents a technique to pass the additional values within a single parameter and then process them within your web resource.</span><span class="sxs-lookup"><span data-stu-id="990ca-106">The page here represents a technique to pass the additional values within a single parameter and then process them within your web resource.</span></span> 
  
## <a name="sample-html-web-resource"></a><span data-ttu-id="990ca-107">Sample HTML web resource</span><span class="sxs-lookup"><span data-stu-id="990ca-107">Sample HTML web resource</span></span>  
 <span data-ttu-id="990ca-108">The HTML code below represents a webpage (HTML) web resource that includes a script that defines three functions:</span><span class="sxs-lookup"><span data-stu-id="990ca-108">The HTML code below represents a webpage (HTML) web resource that includes a script that defines three functions:</span></span>  
  
- <span data-ttu-id="990ca-109">**getDataParam**: Called from the `body.onload` event, this function retrieves any query string parameters passed to the page and locates one named `data`.</span><span class="sxs-lookup"><span data-stu-id="990ca-109">**getDataParam**: Called from the `body.onload` event, this function retrieves any query string parameters passed to the page and locates one named `data`.</span></span>  
  
- <span data-ttu-id="990ca-110">**parseDataValue**: Receives the data parameter from `getDataParam` and builds a DHTML table to display any values passed within the `data` parameter.</span><span class="sxs-lookup"><span data-stu-id="990ca-110">**parseDataValue**: Receives the data parameter from `getDataParam` and builds a DHTML table to display any values passed within the `data` parameter.</span></span>  
  
  > [!NOTE]
  >  <span data-ttu-id="990ca-111">All characters included in the query string will be encoded using the [encodeURIComponent method](https://msdn.microsoft.com/library/xh9be5xc\(v=VS.85\).aspx).</span><span class="sxs-lookup"><span data-stu-id="990ca-111">All characters included in the query string will be encoded using the [encodeURIComponent method](https://msdn.microsoft.com/library/xh9be5xc\(v=VS.85\).aspx).</span></span> <span data-ttu-id="990ca-112">This function uses the [!INCLUDE[pn_JScript](../includes/pn-jscript.md)][decodeURIComponent method](https://msdn.microsoft.com/library/91b80x6x\(VS.85\).aspx) to decode the values passed.</span><span class="sxs-lookup"><span data-stu-id="990ca-112">This function uses the [!INCLUDE[pn_JScript](../includes/pn-jscript.md)][decodeURIComponent method](https://msdn.microsoft.com/library/91b80x6x\(VS.85\).aspx) to decode the values passed.</span></span>  
  
- <span data-ttu-id="990ca-113">**noParams**: Displays a message when no parameters are passed to the page.</span><span class="sxs-lookup"><span data-stu-id="990ca-113">**noParams**: Displays a message when no parameters are passed to the page.</span></span>  
  
```html  
<!DOCTYPE html >  
<html lang="en-us">  
<head>  
 <title>Show Data Parameters Page</title>  
 <style type="text/css">  
  body  
  {  
   font-family: Segoe UI, Tahoma, Arial;  
   background-color: #d6e8ff;  
  }  
  tbody  
  {  
   background-color: white;  
  }  
  th  
  {  
   background-color: black;  
   color: White;  
  }  
 </style>  
 <script type="text/javascript">  
  document.onreadystatechange = function () {  
   if (document.readyState == "complete") {  
    getDataParam();  
   }  
  }  
  
  function getDataParam() {  
   //Get the any query string parameters and load them  
   //into the vals array  
  
   var vals = new Array();  
   if (location.search != "") {  
    vals = location.search.substr(1).split("&");  
    for (var i in vals) {  
     vals[i] = vals[i].replace(/\+/g, " ").split("=");  
    }  
    //look for the parameter named 'data'  
    var found = false;  
    for (var i in vals) {  
     if (vals[i][0].toLowerCase() == "data") {  
      parseDataValue(vals[i][1]);  
      found = true;  
      break;  
     }  
    }  
    if (!found)  
    { noParams(); }  
   }  
   else {  
    noParams();  
   }  
  }  
  
  function parseDataValue(datavalue) {  
   if (datavalue != "") {  
    var vals = new Array();  
  
    var message = document.createElement("p");  
    setText(message, "These are the data parameters values that were passed to this page:");  
    document.body.appendChild(message);  
  
    vals = decodeURIComponent(datavalue).split("&");  
    for (var i in vals) {  
     vals[i] = vals[i].replace(/\+/g, " ").split("=");  
    }  
  
    //Create a table and header using the DOM  
    var oTable = document.createElement("table");  
    var oTHead = document.createElement("thead");  
    var oTHeadTR = document.createElement("tr");  
    var oTHeadTRTH1 = document.createElement("th");  
    setText(oTHeadTRTH1, "Parameter");  
    var oTHeadTRTH2 = document.createElement("th");  
    setText(oTHeadTRTH2, "Value");  
    oTHeadTR.appendChild(oTHeadTRTH1);  
    oTHeadTR.appendChild(oTHeadTRTH2);  
    oTHead.appendChild(oTHeadTR);  
    oTable.appendChild(oTHead);  
    var oTBody = document.createElement("tbody");  
    //Loop through vals and create rows for the table  
    for (var i in vals) {  
     var oTRow = document.createElement("tr");  
     var oTRowTD1 = document.createElement("td");  
     setText(oTRowTD1, vals[i][0]);  
     var oTRowTD2 = document.createElement("td");  
     setText(oTRowTD2, vals[i][1]);  
  
     oTRow.appendChild(oTRowTD1);  
     oTRow.appendChild(oTRowTD2);  
     oTBody.appendChild(oTRow);  
    }  
  
    oTable.appendChild(oTBody);  
    document.body.appendChild(oTable);  
   }  
   else {  
    noParams();  
   }  
  }  
  
  function noParams() {  
   var message = document.createElement("p");  
   setText(message, "No data parameter was passed to this page");  
  
   document.body.appendChild(message);  
  }  
  //Added for cross browser support.  
  function setText(element, text) {  
   if (typeof element.innerText != "undefined") {  
    element.innerText = text;  
   }  
   else {  
    element.textContent = text;  
   }  
  
  }  
 </script>  
</head>  
<body>  
</body>  
</html>  
  
```  
  
#### <a name="using-this-page"></a><span data-ttu-id="990ca-114">Using this page</span><span class="sxs-lookup"><span data-stu-id="990ca-114">Using this page</span></span>  
  
1.  <span data-ttu-id="990ca-115">Create a webpage web resource called "new_/ShowDataParams.htm" using the sample code.</span><span class="sxs-lookup"><span data-stu-id="990ca-115">Create a webpage web resource called "new_/ShowDataParams.htm" using the sample code.</span></span>  
  
     <span data-ttu-id="990ca-116">The parameters you want to pass are: `first=First Value&second=Second Value&third=Third Value`</span><span class="sxs-lookup"><span data-stu-id="990ca-116">The parameters you want to pass are: `first=First Value&second=Second Value&third=Third Value`</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="990ca-117">If you’re adding static parameters using the Web Resource Properties dialog box from the form editor, you can simply paste the parameters without encoding them into the **Custom Parameter(data)** field.</span><span class="sxs-lookup"><span data-stu-id="990ca-117">If you’re adding static parameters using the Web Resource Properties dialog box from the form editor, you can simply paste the parameters without encoding them into the **Custom Parameter(data)** field.</span></span> <span data-ttu-id="990ca-118">These values will be encoded for you, but you’ll still need to decode them and extract the values in your page.</span><span class="sxs-lookup"><span data-stu-id="990ca-118">These values will be encoded for you, but you’ll still need to decode them and extract the values in your page.</span></span>  
  
2.  <span data-ttu-id="990ca-119">For dynamic values generated in code, use the `encodeURIComponent` method on the parameters.</span><span class="sxs-lookup"><span data-stu-id="990ca-119">For dynamic values generated in code, use the `encodeURIComponent` method on the parameters.</span></span> <span data-ttu-id="990ca-120">The encoded values should be:</span><span class="sxs-lookup"><span data-stu-id="990ca-120">The encoded values should be:</span></span>  
  
     `first%3DFirst%20Value%26second%3DSecond%20Value%26third%3DThird%20Value`  
  
     <span data-ttu-id="990ca-121">Open the page passing the encoded parameters as the value of the data parameter:</span><span class="sxs-lookup"><span data-stu-id="990ca-121">Open the page passing the encoded parameters as the value of the data parameter:</span></span>  
  
    ```  
    http://<server name>/WebResources/new_/ShowDataParams.htm?Data=first%3DFirst%20Value%26second%3DSecond%20Value%26third%3DThird%20Value  
    ```  
  
    > [!NOTE]
    >  <span data-ttu-id="990ca-122">If you have added the web resource to a form and have pasted the un-encoded parameters into the **Custom Parameters(data)** field, you can just preview the form.</span><span class="sxs-lookup"><span data-stu-id="990ca-122">If you have added the web resource to a form and have pasted the un-encoded parameters into the **Custom Parameters(data)** field, you can just preview the form.</span></span>  
  
3.  <span data-ttu-id="990ca-123">The `new_/ShowDataParams.htm` will display a dynamically generated table:</span><span class="sxs-lookup"><span data-stu-id="990ca-123">The `new_/ShowDataParams.htm` will display a dynamically generated table:</span></span>  
  
    |<span data-ttu-id="990ca-124">Tham số</span><span class="sxs-lookup"><span data-stu-id="990ca-124">Parameter</span></span>|<span data-ttu-id="990ca-125">Value</span><span class="sxs-lookup"><span data-stu-id="990ca-125">Value</span></span>|  
    |---------------|-----------|  
    |<span data-ttu-id="990ca-126">đầu tiên</span><span class="sxs-lookup"><span data-stu-id="990ca-126">first</span></span>|<span data-ttu-id="990ca-127">First Value</span><span class="sxs-lookup"><span data-stu-id="990ca-127">First Value</span></span>|  
    |<span data-ttu-id="990ca-128">second</span><span class="sxs-lookup"><span data-stu-id="990ca-128">second</span></span>|<span data-ttu-id="990ca-129">Second Value</span><span class="sxs-lookup"><span data-stu-id="990ca-129">Second Value</span></span>|  
    |<span data-ttu-id="990ca-130">third</span><span class="sxs-lookup"><span data-stu-id="990ca-130">third</span></span>|<span data-ttu-id="990ca-131">Third Value</span><span class="sxs-lookup"><span data-stu-id="990ca-131">Third Value</span></span>|  
  
### <a name="how-it-works"></a><span data-ttu-id="990ca-132">Cách hoạt động</span><span class="sxs-lookup"><span data-stu-id="990ca-132">How it works</span></span>  
 <span data-ttu-id="990ca-133">To access the values embedded within the data query string parameter value, in your webpage web resource you can extract the value of the data parameter and then use code to split the string into an array so you can access each name value pair individually.</span><span class="sxs-lookup"><span data-stu-id="990ca-133">To access the values embedded within the data query string parameter value, in your webpage web resource you can extract the value of the data parameter and then use code to split the string into an array so you can access each name value pair individually.</span></span>  
  
 <span data-ttu-id="990ca-134">When the page loads the `getDataParam` function is called.</span><span class="sxs-lookup"><span data-stu-id="990ca-134">When the page loads the `getDataParam` function is called.</span></span> <span data-ttu-id="990ca-135">This function simply identifies the data parameter and passes the value to the `ParseDataValue` function.</span><span class="sxs-lookup"><span data-stu-id="990ca-135">This function simply identifies the data parameter and passes the value to the `ParseDataValue` function.</span></span> <span data-ttu-id="990ca-136">If no data parameter is found the `noParams` function will add a message to the page in place of the table.</span><span class="sxs-lookup"><span data-stu-id="990ca-136">If no data parameter is found the `noParams` function will add a message to the page in place of the table.</span></span>  
  
 <span data-ttu-id="990ca-137">The `ParseDataValue` function uses similar logic found in `getDataParam` to locate the custom parameter delimiters to create an array of name value pairs.</span><span class="sxs-lookup"><span data-stu-id="990ca-137">The `ParseDataValue` function uses similar logic found in `getDataParam` to locate the custom parameter delimiters to create an array of name value pairs.</span></span> <span data-ttu-id="990ca-138">Then it generates a table and appends it to the otherwise empty document.body.</span><span class="sxs-lookup"><span data-stu-id="990ca-138">Then it generates a table and appends it to the otherwise empty document.body.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="990ca-139">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="990ca-139">See also</span></span>  
 <span data-ttu-id="990ca-140">[Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="990ca-140">[Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md) </span></span>  
 <span data-ttu-id="990ca-141">[Sample: Import Files as Web Resources](sample-import-files-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="990ca-141">[Sample: Import Files as Web Resources](sample-import-files-web-resources.md) </span></span>  
 <span data-ttu-id="990ca-142">[Web Page (HTML) Web Resources](webpage-html-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="990ca-142">[Web Page (HTML) Web Resources](webpage-html-web-resources.md) </span></span>  
 [<span data-ttu-id="990ca-143">Silverlight (XAP) Web Resources</span><span class="sxs-lookup"><span data-stu-id="990ca-143">Silverlight (XAP) Web Resources</span></span>](silverlight-xap-web-resources.md)
