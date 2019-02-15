---
title: Image web resources (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: 'Learn about using image web resources to make images available for use in Dynamics 365 for Customer Engagement apps. '
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
- images
- web resource, image
ms.assetid: dfa3f3e2-471e-4295-be47-ab6936189340
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a2d4a93a266ae2702904846d0b9c35e88ea1d8c4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388063"
---
# <a name="image-web-resources"></a>Image web resources

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

Use image web resources to make images available for use in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

There are 5 types of image web resources: 
* PNG Format
* JPG Format
* GIF Format
* ICO Format
* Vector Format (SVG)

> [!NOTE]
> Vector Format (SVG) web resources were added with the [!INCLUDE[../includes/pn-crm-9-0-0-online.md](../includes/pn-crm-9-0-0-online.md)].

  
<a name="BKMK_Capabilities"></a>   
## <a name="capabilities-of-image-web-resources"></a>Capabilities of image web resources  
 With image web resources you can add images where you need them. Common uses include the following:  
  
- Biểu tượng thực thể tùy chỉnh  
- Icons for custom Ribbon controls and `SiteMap` subareas  
- Decorative graphics for entity forms and webpage web resources.  
- Background images that are used by CSS web resources.  

Use Vector Format (SVG) web resources for any icon presented in the application. Hình ảnh véc-tơ được định nghĩa là Đồ họa Véc tơ Có thể thay đổi quy mô (SVG), một định dạng hình ảnh véc-tơ dựa trên XML. So với các tài nguyên web hình ảnh khác, hình ảnh véc-tơ có lợi thế đó là khả năng mở rộng. Bạn có thể xác định một hình ảnh véc-tơ và tái sử dụng nó, chứ không phải cung cấp nhiều kích cỡ hình ảnh. You will use these in with a new <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IconVectorName> property to define the icon for a custom entity instead of the `IconLargeName`, `IconMediumName`, or `IconSmallName` properties.
  
<a name="BKMK_Limitations"></a>   
## <a name="limitations-of-image-web-resources"></a>Limitations of image web resources  
 Like all web resources, image web resources use the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] security context. Only licensed [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] users who have the necessary privileges can access them.  
 
  
<a name="BKMK_ReferenceFromWebPageWebResource"></a>   
## <a name="reference-an-image-web-resource-from-a-webpage-web-resource"></a>Reference an image web resource from a webpage web resource  
 All web resources can use relative URLs to reference each other. In the following example, for the webpage (HTML) web resource new_/content/contentpage.htm to reference the image web resource new_/Images/image1.png, add the following HTML code to new_/content/contentpage.htm:  
  
```html  
<img src="../Images/image1.png" />  
```  
  
<a name="BKMK_ReferenceFromForm"></a>   
## <a name="reference-an-image-web-resource-from-a-dynamics-365-for-customer-engagement-apps-form"></a>Reference an image web resource from a Dynamics 365 for Customer Engagement apps form  
  
#### <a name="add-an-image-to-an-entity-form"></a>Add an image to an entity form  
  
1.  Navigate to the form editor for an entity.  
  
2.  Select where you want to add the image in the form.  
  
3.  On the **Insert tab**, click **Web Resource**.  
  
4.  On the **General** tab, select the web resource image that you want to add.  
  
5.  Specify a name for the web resource. You can also specify a label and alternative text.  
  
6.  On the **Formatting** tab, you can define:  
  
    -   The number of columns the images should use.  
  
    -   The number of rows the images should use, or if it should automatically expand to use available space.  
  
    -   The size of the image using the following options:  
  
        - **Stretch to fit**  
  
        - **Stretch to fit (maintain aspect ratio)**  
  
        - **Original**  
  
        - **Specific**  
  
    -   If you select “Specific,” you can enter the desired height and width in pixels.  
  
7.  Bấm **OK**.  
  
8.  You must save your changes and publish the form before users can see the image in the form.  
  
<a name="BKMK_ReferenceWithWebResourcedirective"></a>   
## <a name="reference-an-image-web-resource-from-a-ribbon-element-or-from-the-site-map-subarea"></a>Reference an image web resource from a ribbon element or from the Site Map subarea  
 Use the `$webresource:` directive to specify a web resource image to use as an icon in the ribbon or in the application navigation using Site Map. The following sample shows how to specify icons for a button in the ribbon.  
  
```xml  
<Button Id="MyISV.opportunity.form.actions.FlyoutAnchor.Button.1" Image16by16="$webresource:new_/icons/oneIcon16.png" Image32by32="$webresource:new_/icons/oneIcon32.png"/>  
```  
  
> [!NOTE]
>  Using the `$webresource:` directive adds a solution dependency that prevents the referenced image web resources from being deleted as long as they are used by another solution component.  
  
### <a name="see-also"></a>Xem thêm  
 [Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md)   
 [Using Web Page (HTML) Web Resources](webpage-html-web-resources.md)   
 [Using Style Sheet (CSS) Web Resources](css-web-resources.md)   
 [Using Script (JScript) Web Resources](script-jscript-web-resources.md)   
 [Using Data (XML) Web Resources](data-xml-web-resources.md)   
 [Using Silverlight (XAP) Web Resources](silverlight-xap-web-resources.md)   
 [Using Stylesheet (XSL) Web Resources](stylesheet-xsl-web-resources.md)