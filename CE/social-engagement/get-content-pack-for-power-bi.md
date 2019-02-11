---
title: Get the Social Engagement content pack | Microsoft Docs
description: Download the use the Social Engagement content pack for Power BI.
keywords: Power BI, content pack, engagement details
ms.date: 07/11/2018
ms.service: dynamics-365-marketing
ms.topic: article
ms.assetid: c82b4063-c86c-4922-99dd-1f5ddd18cb00
author: m-hartmann
ms.author: mhart
manager: sakudes
topic-status: Drafting
ms.custom:
- dyn365-socialengagement
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365SE
ms.openlocfilehash: eea1d5147f9a9f39babea06cb35e8459b2df6d67
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375596"
---
# <a name="get-the-includepnnetbreezelongincludespn-social-engagement-longmd-content-pack-for-power-bi"></a>Get the [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] content pack for Power BI
Engaging on social media by responding to posts is a core capability of [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)]. With this [!INCLUDE[pn_microsoft_power_bi](../includes/pn-microsoft-power-bi.md)] content pack, you can now get insights on how your organization, and your teams are engaging with KPIs such as volume of interactions and average response times.  
  
 This content pack is for organizations using [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] and can only be accessed via [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)]. You can use this content pack with both [the free and the pro versions of Power BI](https://powerbi.microsoft.com/).  
  
 Use this content pack as a starting point on [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] to create your own reports and dashboards that best meet your needs.  
  
## <a name="getting-started"></a>Getting Started  
 Connect to [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] from [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] with the [content pack for Microsoft Social Engagement](https://go.microsoft.com/fwlink/p/?linkid=846841).  
  
> [!NOTE]
>  Administrator or Manager permissions and access to [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]'s solution ID are required to connect.  For more information about the solution ID, see  [Troubleshooting](#troubleshooting).  
  
### <a name="how-to-connect"></a>How to connect  
  
1. Go to [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] and select **Get Data** at the bottom of the left navigation pane.  
  
   ![Get Data button in Power BI](media/content-pack-get-data.png "Get Data button in Power BI")  
  
2. In the **Services** box, select **Get**.  
  
   ![Get data from services to show in Power BI](media/content-pack-get-services.png "Get data from services to show in Power BI")  
  
3. Search for **[!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]**, select the content pack from the results, and then click **Get it now**.  
  
   ![Select Social Engagement from the list of content packs](media/content-pack-select-social-engagement.png "Select Social Engagement from the list of content packs")  
  
4. Provide the **Solution ID** (not the full URL) of the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] instance you want to connect to, choose the time frame you want to import and click **Next**.  For more information how to find the **Solution ID**, see [Troubleshooting](#troubleshooting).  
  
   ![Set the solution id and the time frame of the data](media/content-pack-solutionid.png "Set the solution id and the time frame of the data")  
  
   > [!IMPORTANT]
   >  Choose an appropriate time frame based on the interaction data volume in your [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution to avoid potentially long loading times. We recommend keeping the total number of posts with actions imported into [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] under 100,000.  
  
5. For **Authentication method**, select **oAuth2** and then click **Sign in**.  
  
   ![Select the oAuth2 authentication method](media/content-pack-select-oauth2.png "Select the oAuth2 authentication method")  
  
    The first time you connect, [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] may prompt you to allow read-only access to your account.  
  
    Select **Grant** to begin the import process. The import process can take a few minutes depending on the volume of data in your solution and will gather data for social posts that users of [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] interacted with.  
  
   ![Sign in to your Office 365 account](media/content-pack-office365-sign-in.png "Sign in to your Office 365 account")  
  
6. After [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] imports the data you will see a new dashboard, report, and dataset in the left navigation pane. New items are marked with a yellow asterisk *:  
  
   ![Sidebar in Power BI with highlighted controls](media/content-pack-sidebar-powerbi.png "Sidebar in Power BI with highlighted controls")  
  
7. Select the **[!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] Performance** dashboard. It may take a while initially to show the data.  
  
   ![Processing the data import in Power BI](media/content-pack-importing-data.png "Processing the data import in Power BI")  
  
    Once your data is imported you can see the default dashboard that [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] creates to display your data. You can modify this dashboard to display your data in any way you want.  
  
   ![Dashboard with Social Engagmeent data in Power BI](media/content-pack-social-engagement-dashboard.jpg "Dashboard with Social Engagement data in Power BI")  
  
### <a name="whats-next"></a>What's next?  
  
-   Try [asking a question in the Q & A box](https://docs.microsoft.com/power-bi/power-bi-tutorial-q-and-a) at the top of the dashboard.  
  
-   [Change the tiles](https://powerbi.microsoft.com/documentation/powerbi-service-edit-a-tile-in-a-dashboard/) in the dashboard.  
  
-   [Select a tile](https://powerbi.microsoft.com/documentation/powerbi-service-dashboard-tiles/) to open the underlying report.  
  
-   While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.  
  
-   See also:  
  
    -   [Get started with Power BI](https://powerbi.microsoft.com/documentation/powerbi-service-dashboard-tiles/)  
  
    -   [Get Data for Power BI](https://powerbi.microsoft.com/documentation/powerbi-service-get-data/)  
  
## <a name="whats-included"></a>What's included  
 At the core of this content pack is the term 'Action'. We describe Action as a single, specific interaction with a given social post. For example, assigning a post to a user or retweeting a tweet, etc.  
  
 Depending on the type of action, related information is shown. It’s critical to understand that only actions taken in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] are part of this dataset.  
  
 To get you started quickly, the content pack includes a dashboard based on three [reports](https://powerbi.microsoft.com/documentation/powerbi-service-reports/):  
  
- **Engagement Performance**: Get insights on how your organization is engaging on  social media with KPIs on actions and response times.  
  
- **Team Performance**: Get insights on how teams and individuals in your organization are engaging on social media with KPIs on actions and response times.  
  
- **Engagement Analytics**: Analyze your organization’s engagement on social media with KPIs based on location, authors, tags and sentiment.  
  
### <a name="action-types"></a>Action types  
 Contains the various types of actions that can be performed on social posts in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].  
  
- **Internal**: Actions that are directed at an internal audience.  
  
  - Assign  
  
  - Link to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)]  
  
  - Label  
  
- **External**: Actions that are directed at an external (public) audience.  
  
    -   Share  
  
    -   Like  
  
    -   Reply  
  
    -   Private message  
  
> [!NOTE]
>  This content pack contains only a subset of the available actions in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].  
  
### <a name="actions"></a>Actions  
 The Actions table provides the core details about the individual actions taken on posts.  
  
- **Post ID**: ID of the post the action was taken on.  
  
- **User ID**: ID of the user who took the action.  
  
- **Action Value**: Result or addressee of the action. For example: For Assign actions, this is the name of the user or user group. For Reply, this is the social profile used for the reply.  
  
- **Action Value Group**: Adds an additional layer of information regarding the Action Value. For example: For Assign actions, this describes if the action value is a user or a group. For Reply actions, this is the corresponding source.  
  
- **Action Value ID**: ID of the entity that was addressed by the action.  
  
- **Action Date**: Time stamp for the action.  
  
- **First Response Time**: Duration between Publication Date and Action Date.  
  
### <a name="action-modes"></a>Action modes  
 The Action Modes table contains information about the origin of actions.  
  
- **Manual**: Actions that were taken manually, in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] or Social Selling Assistant user interface.  
  
- **Auto**: Actions that were taken by the system for example by processing automation rules, or by un-assigning posts when a user is deleted in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].  
  
  The table below maps out the possible combination of values for Action Type Group, Action Type, Action Value and Action Value Group fields:  
  
| Action Type Group |                             Action Type                             |                                                                                                                                                                                                                       Action Value                                                                                                                                                                                                                        |                                                                            Action Value Group                                                                            |
|-------------------|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Internal      |                               Assign                                |                                                                                                                                                                                                               User name or User Group name                                                                                                                                                                                                                |                                                                            User or User Group                                                                            |
|     Internal      |                                Label                                |                                                                                                                                                                                                                        Label name                                                                                                                                                                                                                         |                                                                                  Label                                                                                   |
|     Internal      | Link to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] |                                                                                                                                                                                                                       Instance name                                                                                                                                                                                                                       |                                                                  Instance type (Online or On-premises)                                                                   |
|     External      |                                Reply                                |                                                                                                                                                                        Social profile in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] that was used.                                                                                                                                                                         |   Source ([!INCLUDE[tn_twitter](../includes/tn-twitter.md)], [!INCLUDE[tn_youtube](../includes/tn-youtube.md)] or [!INCLUDE[tn_facebook](../includes/tn-facebook.md)])   |
|     External      |                                Like                                 |                                                                                                                                                                        Social profile in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] that was used.                                                                                                                                                                         |  Source ([!INCLUDE[tn_twitter](../includes/tn-twitter.md)], [!INCLUDE[tn_youtube](../includes/tn-youtube.md)] or [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] )   |
|     External      |                                Share                                | Social profile in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] that was used in:<br /><br /> -   Retweet on [!INCLUDE[tn_twitter](../includes/tn-twitter.md)]<br />-   Share As on [!INCLUDE[tn_facebook](../includes/tn-facebook.md)]<br />-   Post Link for [!INCLUDE[tn_twitter](../includes/tn-twitter.md)], [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] and [!INCLUDE[pn_LinkedIn](../includes/pn-linkedin.md)] | Source ([!INCLUDE[tn_twitter](../includes/tn-twitter.md)], [!INCLUDE[tn_facebook](../includes/tn-facebook.md)], and [!INCLUDE[pn_LinkedIn](../includes/pn-linkedin.md)]) |
|     External      |                          Private messages                           |                                                                                                                                                                        Social profile in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] that was used.                                                                                                                                                                         |                            Source ([!INCLUDE[tn_twitter](../includes/tn-twitter.md)] or [!INCLUDE[tn_facebook](../includes/tn-facebook.md)])                             |
  
### <a name="authors"></a>Authors  
 Contains the authors of all posts in the data set. If available, it also contains the author location. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [See the locations for the posts](analytics-location.md)  
  
### <a name="dynamics-365-for-customer-engagement-connections"></a>Dynamics 365 for Customer Engagement connections  
 Contains the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] connections that posts were linked to using the Link to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] action and the instance type (online or on-premises).  
  
### <a name="labels"></a>Labels  
 Contains the labels that posts were labelled with using the Label action. Since users can change these values, it is a snapshot of the labels assigned to the posts at the time of the data refresh.  
  
### <a name="posts"></a>Posts  
 Contains the acquisition date, publication date, meta data such as sentiment, reach, and location of all the posts that have at least oneaction performed in the timeframe imported in the [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] data set.  
  
### <a name="users"></a>Users  
 The User table contains information about all users in the connected [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution.  
  
### <a name="active-users"></a>Active users  
 A subset of the Users table containing users and groups that have at least one action associated with them.  
  
### <a name="assignee"></a>Assignee  
 A subset of the Users table containing users or groups that were assigned posts. Since users can change these values, it is a snapshot of the assignments at the time of the data refresh.  
  
### <a name="search-topics"></a>Search topics  
 Contains the name of all search topics  in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution.  
  
### <a name="search-topic-categories"></a>Search topic categories  
 Contains the name of all search topic categories  in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution.  
  
### <a name="social-profiles"></a>Social profiles  
 Contains all social profiles in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution.  
  
### <a name="solution"></a>Solution  
 Contains the information used for reference in the Reports pages along with the total number of posts in the selected import time frame. Only posts with an action associated are imported to [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)].  
  
### <a name="sources"></a>Sources  
 Contains all available sources in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution from which the data was imported.  
  
### <a name="tags"></a>Tags  
 Contains all available tags in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution from which the data was imported. Since users can change these values, it is a snapshot of the tags assigned to the posts at the time of the data refresh.  
  
<a name="troubleshooting"></a>   
## <a name="troubleshooting"></a>Troubleshooting  
 If data is not showing up in [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)], check to make sure that you are using the correct Solution ID and that you have the required permissions to view the data.  
  
 If you are not already an admin in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)], please contact your administrator to make sure you have rights to view the collected data.  
  
 The **Solution ID** of your [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution can be found in the URL. The URL can be found in the browser’s address bar after [signing in to Social Engagement](https://social.dynamics.com/login).  
  
 The Solution URL is also shown on alerts or other email notifications you receive from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]. For example: 1 is the Solution ID in the Solution URL [https://listening-prod.dynamics.com/app/1/](https://www.microsoft.com). 
  
  
### <a name="see-also"></a>See Also  
 [Engage on social networks](engage-on-social-networks.md)   
 [Publish and react to posts](publish-react-posts.md)   
 [View posts and conversations in Social Engagement](posts-conversations.md)   
 [Work with posts](work-with-posts.md)
