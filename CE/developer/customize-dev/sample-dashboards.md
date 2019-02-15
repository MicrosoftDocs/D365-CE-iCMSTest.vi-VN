---
title: Sample dashboards | MicrosoftDocs
description: 'The topic contains sample dashboards along with the respective FormXML strings. You can specify the FormXML string for a dashboard using the SystemForm.FormXml attribute for an organization-owned dashboard or UserForm.FormXml for a user-owned dashboard. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 4ac5886d-a521-498c-b063-831113b507bc
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 589669057dbc98ae571b0c3c9e1863f18408fd70
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388029"
---
# <a name="sample-dashboards"></a><span data-ttu-id="9523b-104">Sample dashboards</span><span class="sxs-lookup"><span data-stu-id="9523b-104">Sample dashboards</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="9523b-105">This topic contains sample dashboards along with the respective FormXML strings.</span><span class="sxs-lookup"><span data-stu-id="9523b-105">This topic contains sample dashboards along with the respective FormXML strings.</span></span> <span data-ttu-id="9523b-106">You can specify the FormXML string for a dashboard using the `SystemForm.FormXml` attribute for an organization-owned dashboard or `UserForm.FormXml` for a user-owned dashboard.</span><span class="sxs-lookup"><span data-stu-id="9523b-106">You can specify the FormXML string for a dashboard using the `SystemForm.FormXml` attribute for an organization-owned dashboard or `UserForm.FormXml` for a user-owned dashboard.</span></span>  
  
<a name="Sample1"></a>   
## <a name="dashboard-with-charts-and-grids"></a><span data-ttu-id="9523b-107">Dashboard with charts and grids</span><span class="sxs-lookup"><span data-stu-id="9523b-107">Dashboard with charts and grids</span></span>  
 <span data-ttu-id="9523b-108">The following is a sample dashboard that has four components: three charts and a grid.</span><span class="sxs-lookup"><span data-stu-id="9523b-108">The following is a sample dashboard that has four components: three charts and a grid.</span></span> <span data-ttu-id="9523b-109">This is one of the default organization-owned dashboards, **Microsoft Dynamics 365 for Customer Engagement Overview**, available in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="9523b-109">This is one of the default organization-owned dashboards, **Microsoft Dynamics 365 for Customer Engagement Overview**, available in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement.</span></span>  
  
 <span data-ttu-id="9523b-110">![Sample dashboard: Microsoft Dynamics 365 for Customer Engagement Overview](../media/dashboard-sample.png "Sample dashboard: Microsoft Dynamics 365 for Customer Engagement Overview")</span><span class="sxs-lookup"><span data-stu-id="9523b-110">![Sample dashboard: Microsoft Dynamics 365 for Customer Engagement Overview](../media/dashboard-sample.png "Sample dashboard: Microsoft Dynamics 365 for Customer Engagement Overview")</span></span>  
  
### <a name="formxml"></a><span data-ttu-id="9523b-111">FormXML</span><span class="sxs-lookup"><span data-stu-id="9523b-111">FormXML</span></span>  
 <span data-ttu-id="9523b-112">The following sample shows the FormXML for this dashboard.</span><span class="sxs-lookup"><span data-stu-id="9523b-112">The following sample shows the FormXML for this dashboard.</span></span>  
  
```xml  
<form>  
 <tabs>  
  <tab showlabel="true"  
       verticallayout="true"  
       id="{4e5d00ec-6b2a-447a-afdf-235e6c5d4599}"  
       name="{4e5d00ec-6b2a-447a-afdf-235e6c5d4599}"  
       locklevel="0"  
       expanded="true">  
   <columns>  
    <column width="100%">  
     <sections>  
      <section showlabel="false"  
               showbar="false"  
               columns="111"  
               id="{7f7bbdb7-15d6-4664-bda7-6060d0cd3105}"  
               name="{7f7bbdb7-15d6-4664-bda7-6060d0cd3105}">  
       <rows>  
        <row>  
         <cell colspan="1"  
               rowspan="12"  
               showlabel="false"  
               id="{cfa8b70b-b0f0-4b91-9cf3-c4e29925186f}"  
               auto="false">  
          <control id="Chart1"  
                   classid="{E7A81278-8635-4d9e-8D4D-59480B391C5B}">  
           <parameters>  
            <TargetEntityType>opportunity</TargetEntityType>  
            <ChartGridMode>Chart</ChartGridMode>  
            <EnableQuickFind>true</EnableQuickFind>  
            <EnableViewPicker>false</EnableViewPicker>  
            <EnableJumpBar>true</EnableJumpBar>  
            <RecordsPerPage>12</RecordsPerPage>  
            <ViewId>{00000000-0000-0000-00AA-000010003001}</ViewId>  
            <IsUserView>false</IsUserView>  
            <ViewIds></ViewIds>  
            <AutoExpand>Fixed</AutoExpand>  
            <VisualizationId>{87293554-2482-DE11-9FF3-00155DA3B012}</VisualizationId>  
            <IsUserChart>false</IsUserChart>  
            <EnableChartPicker>false</EnableChartPicker>  
            <RelationshipName></RelationshipName>  
           </parameters>  
          </control>  
         </cell>  
         <cell colspan="1"  
               rowspan="12"  
               showlabel="false"  
               id="{5fc07b79-9f15-4396-9a66-c8ca4a13cac3}"  
               auto="false">  
          <control id="Chart2"  
                   classid="{E7A81278-8635-4d9e-8D4D-59480B391C5B}">  
           <parameters>  
            <TargetEntityType>lead</TargetEntityType>  
            <ChartGridMode>Chart</ChartGridMode>  
            <EnableQuickFind>true</EnableQuickFind>  
            <EnableViewPicker>false</EnableViewPicker>  
            <EnableJumpBar>true</EnableJumpBar>  
            <RecordsPerPage>12</RecordsPerPage>  
            <ViewId>{5A926B99-3A5F-DF11-AE90-00155D2E3002}</ViewId>  
            <IsUserView>false</IsUserView>  
            <ViewIds></ViewIds>  
            <AutoExpand>Fixed</AutoExpand>  
            <VisualizationId>{3ED18B7C-5693-DE11-97D4-00155DA3B01E}</VisualizationId>  
            <IsUserChart>false</IsUserChart>  
            <EnableChartPicker>false</EnableChartPicker>  
            <RelationshipName></RelationshipName>  
           </parameters>  
          </control>  
         </cell>  
         <cell colspan="1"  
               rowspan="12"  
               showlabel="false"  
               id="{378521f2-889b-4e56-ae46-0b69e87dd0b8}"  
               auto="false">  
          <control id="Chart3"  
                   classid="{E7A81278-8635-4d9e-8D4D-59480B391C5B}">  
           <parameters>  
            <TargetEntityType>incident</TargetEntityType>  
            <ChartGridMode>Chart</ChartGridMode>  
            <EnableQuickFind>true</EnableQuickFind>  
            <EnableViewPicker>false</EnableViewPicker>  
            <EnableJumpBar>true</EnableJumpBar>  
            <RecordsPerPage>12</RecordsPerPage>  
            <ViewId>{00000000-0000-0000-00AA-000010001032}</ViewId>  
            <IsUserView>false</IsUserView>  
            <ViewIds></ViewIds>  
            <AutoExpand>Fixed</AutoExpand>  
            <VisualizationId>{DF31B045-1D63-DF11-AE90-00155D2E3002}</VisualizationId>  
            <IsUserChart>false</IsUserChart>  
            <EnableChartPicker>false</EnableChartPicker>  
            <RelationshipName></RelationshipName>  
           </parameters>  
          </control>  
         </cell>  
        </row>  
        <row></row>  
        <row></row>  
        <row></row>  
        <row></row>  
        <row></row>  
        <row></row>  
        <row></row>  
        <row></row>  
        <row></row>  
        <row></row>  
        <row></row>  
       </rows>  
      </section>  
     </sections>  
    </column>  
   </columns>  
  </tab>  
  <tab showlabel="true"  
       verticallayout="true"  
       id="{3fb82356-c884-44b6-b11e-d3292776dfb8}"  
       name="{3fb82356-c884-44b6-b11e-d3292776dfb8}"  
       locklevel="0"  
       expanded="true">  
   <columns>  
    <column width="100%">  
     <sections>  
      <section showlabel="false"  
               showbar="false"  
               columns="111"  
               id="{02aab82b-167e-4f61-8d10-9b5a3fab3d76}"  
               name="{02aab82b-167e-4f61-8d10-9b5a3fab3d76}">  
       <rows>  
        <row>  
         <cell colspan="3"  
               rowspan="12"  
               showlabel="false"  
               id="{f0114d8b-f5c9-41b2-9b59-07ff839ef176}"  
               auto="false">  
          <control id="Grid1"  
                   classid="{E7A81278-8635-4d9e-8D4D-59480B391C5B}">  
           <parameters>  
            <TargetEntityType>activitypointer</TargetEntityType>  
            <ChartGridMode>All</ChartGridMode>  
            <EnableQuickFind>false</EnableQuickFind>  
            <EnableViewPicker>true</EnableViewPicker>  
            <EnableJumpBar>true</EnableJumpBar>  
            <RecordsPerPage>8</RecordsPerPage>  
            <ViewId>{00000000-0000-0000-00AA-000010001899}</ViewId>  
            <IsUserView>false</IsUserView>  
            <ViewIds></ViewIds>  
            <AutoExpand>Fixed</AutoExpand>  
            <VisualizationId>{EDF35649-5293-DE11-97D4-00155DA3B01E}</VisualizationId>  
            <IsUserChart>false</IsUserChart>  
            <EnableChartPicker>false</EnableChartPicker>  
            <RelationshipName></RelationshipName>  
           </parameters>  
          </control>  
         </cell>  
        </row>  
        <row></row>  
        <row></row>  
        <row></row>  
        <row></row>  
        <row></row>  
        <row></row>  
        <row></row>  
        <row></row>  
        <row></row>  
        <row></row>  
        <row></row>  
       </rows>  
      </section>  
     </sections>  
    </column>  
   </columns>  
  </tab>  
 </tabs>  
</form>  
```  
  
### <a name="see-also"></a><span data-ttu-id="9523b-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="9523b-113">See also</span></span>  
 <span data-ttu-id="9523b-114">[Dashboards for Microsoft Dynamics 365 for Customer Engagement](analyze-data-with-dashboards.md) </span><span class="sxs-lookup"><span data-stu-id="9523b-114">[Dashboards for Microsoft Dynamics 365 for Customer Engagement](analyze-data-with-dashboards.md) </span></span>  
 [<span data-ttu-id="9523b-115">Dashboard Entities</span><span class="sxs-lookup"><span data-stu-id="9523b-115">Dashboard Entities</span></span>](dashboard-entities.md)
