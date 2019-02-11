---
title: JSON objects reference from Social Engagement | Microsoft Docs
description: Review the full list of properties and object in the Social Engagement payload for Event Hubs.
keywords: JSON, payload, metadata, event hubs, reference
ms.date: 08/22/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: 29a876d1-1915-3517-7ff0-cc357a156dec
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
ms.openlocfilehash: 9226f382ca154b72086a04d9370c3db28ea65d04
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375645"
---
# <a name="json-reference-for-events-from-includepnnetbreezeshortincludespn-social-engagement-shortmd"></a>JSON reference for events from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]
This topic applies to version 2.1 of the JSON payload for social posts streamed to [!INCLUDE[pn_microsoft_azure_event_hubs](../includes/pn-microsoft-azure-event-hubs.md)] from [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)].  

Latest version of the payload: Version 2.1  

> [!NOTE]
> New objects and properties can get added to the payload without increasing the version number.

For more information about getting a connection between [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] and [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)] up and running, see [Stream data from Social Engagement to Microsoft Azure Event Hubs](stream-data-to-event-hubs.md).  

<a name="overview"></a>   
## <a name="overview"></a>Overview  
When [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] streams events to [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)], a JSON payload is generated. A single social post in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] is a single event in the event hub. The JSON payload contains information about a single social post that matches the defined filters and action on the automation rules that generated the payload. Additional properties that you define in your automation rules are part of the [metadata object](#metadataProperties). The main content is part of the [post object](#documentProperties).  

<a name="metadataProperties"></a>   
### <a name="metadata-object-elements"></a>metadata object elements  
Use this table to get a quick link to metadata object properties.  


|                            JSON element                             |                                                           Description                                                            |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
|             [Metadata JSON payload objects](#metadata)              | JSON object describing the metadata for the payload sent to [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)]. |
|           [metadata.matchedRules](#metadata.matchedrules)           |                                        Array of automation rules that matched this post.                                         |
|        [metadata.matchedRules.id](#metadata.matchedrules.id)        |                           ID of the automation rule that triggered the creation of this JSON payload.                            |
|      [metadata.matchedRules.name](#metadata.matchedrules.name)      |                          Name of the automation rule that triggered the creation of this JSON payload.                           |
|             [metadata.properties](#metadata.properties)             |    Array of key-value pairs defined in the additional properties of the "Stream to Event Hubs" action in an automation rule.     |
|         [metadata.properties.key](#metadata.properties.key)         |                         Key of a key-value pair provided in additional properties of an automation rule.                         |
|       [metadata.properties.value](#metadata.properties.value)       |                        Value of a key-value pair provided in additional properties of an automation rule.                        |
| [metadata.properties.matchedrule](#metadata.properties.matchedrule) |                                ID of the automation rule that contains the additional properties                                 |

Back to [top](#overview)  

<a name="metadata_sample_payload"></a>   
#### <a name="metadata-sample-payload"></a>metadata sample payload  

```json  
{  
  "metadata": {  
    "matchedRules": [  
      {  
        "id": 12345,  
        "name": "Support Requests"  
      },  
      {  
        "id": 54321,  
        "name": "Company News"  
      }  
    ],  
    "properties": [  
      {  
        "key": "customKey_1",  
        "value": "Some custom value.",  
        "matchedRule": 12345  
        },  

      {  
        "key": "customKey_2",  
        "value": "Some other custom value.",  
        "matchedRule": 54321  
      }  
    ]  
  }  

```  

Back to [top](#overview)  

<a name="documentProperties"></a>   
### <a name="post-object-elements"></a>post object elements  
Use this table to get a quick link to post object properties.  


|                        JSON element                        |                                                                     Description                                                                      |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|                  [post.id](#document.id)                   |                The unique post ID in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution database.                |
|         [post.contentType](#document.contentType)          |                                                            The type of content in a post.                                                            |
|            [post.postType](#document.postType)             |                                                 The type of the post in its conversational context.                                                  |
|                 [post.uri](#document.uri)                  |                                                The post's URI—a  backlink to the post's original URI.                                                |
|               [post.title](#document.title)                |                                                The title as delivered from a post's meta information.                                                |
|     [post.acquisitionDate](#document.acquisitionDate)      |       Timestamp when the post was acquired in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] (in ISO 8601 format).        |
|    [post.modificationDate](#document.modificationDate)     |     Timestamp when  the post was last updated in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] (in ISO 8601 format).     |
|     [post.publicationDate](#document.publicationDate)      |                                      Timestamp when the post was published on the source (in ISO 8601 format).                                       |
|             [post.profile](#document.profile)              |                                           JSON object describing the social profile of the post's author.                                            |
|              [post.source](#document.source)               |                                               JSON object describing on which source a post was found.                                               |
|             [post.content](#document.content)              |                                                    JSON object describing the content of a post.                                                     |
|            [post.language](#document.language)             |                                                    JSON object describing the language of a post.                                                    |
|        [post.abstractText](#document.abstractText)         |                                                              Short excerpt of the post.                                                              |
|               [post.score](#document.score)                |               JSON object describing the source specific score of the post or score of the author at the time the post was published.                |
|      [post.referencedPost](#document.referencedPost)       |                                       Information about the post that this post is a reply to, or a share of.                                        |
|           [post.sentiment](#document.sentiment)            |                                                   JSON object describing the sentiment of a post.                                                    |
|                [post.tags](#document.tags)                 | Array of JSON objects representing tags on a post that were added through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]. |
|          [post.externalId](#document.externalId)           |                                                            ID of the post on the source.                                                             |
|        [post.postLocation](#document.postLocation)         |                                          JSON object describing the location on which a post was published.                                          |
|   [post.fullContentLength](#document.fullContentLenght)    |                                                    Length in characters of a post's text content.                                                    |
|              [post.origin](#document.origin)               |                     JSON object describing the origin of a content. For example: Facebook page on which the post was published.                      |
| [post.matchingSearchTopics](#document.matchingSeachTopics) |                                      Array of JSON objects describing the list of search topics a post matches.                                      |
|  [post.externalCategories](#document.externalCategories)   |                                                Array of categories as delivered by the data provider.                                                |
|        [post.contributors](#document.contributors)         |                                Array of names of those who contributed to the post as provided by the data provider.                                 |
|               [post.media](#document.media)                |                                                Array of JSON objects describing the media in a post.                                                 |
|      [post.externalTopics](#document.externalTopics)       |                                            Array of topics in this post as defined by the data provider.                                             |
|  [post.contributorSummary](#document.contributorSummary)   |                              Short description about the contributor for this post as delivered by external providers.                               |

Back to [top](#overview)  

<a name="document_sample_payload"></a>   
#### <a name="post-sample-payload"></a>post sample payload  

<a name="sampleTwitterReply"></a>   
##### <a name="sample-twitter-reply"></a>Sample Twitter reply  
This is a sample post payload for a [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] reply acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]. We've made up some values to anonymize the sample.  

```json  
  "post": {  
    "id": "1234567",  
    "contentType": "POST",  
    "postType": "reply",  
    "uri": "http://twitter.com/externalHandle/status/1234567890",  
    "publicationDate": "2016-01-23T12:34:56.789+0000",  
    "acquisitionDate": "2016-01-23T12:34:56.789+0000",  
    "modificationDate": "2016-01-23T12:34:56.789+0000",  
    "profile": {  
      "name": "Display Name @chosenUserName",  
      "id": "mse-tw://#12345678",
      "uri": "mse-tw://#12345678",  
      "profileIcon": "https://path/to/the/profileIcon.png",  
      "externalHandle": "chosenUserName",  
      "displayName": "Display Name",  
      "externalId": "7654321"  
    },  
    "source": {  
      "name": "Microblogs",  
      "id": "18",  
      "param": "Twitter"  
    },  
    "content": {  
      "text": "Main text content of the tweet."  
    },  
    "language": {  
      "name": "English",  
      "code": "en"  
    },  
    "abstractText": "Main text content of the tweet.",  
    "score": {  
      "normalScore": 3,  
      "providerScore": 29.0,  
      "provider": "KLOUT"  
    },  
    "referencedPost": {  
      "profile": {  
        "displayName": "Referenced Display Name",  
        "id": "987654321"  
      },  
      "externalId": "123456789",  
    },  
    "sentiment": {  
      "polarity": "negative",  
      "value": -0.46005836  
    },  
        "tags": [  
          {  
            "probability": 0.8339088,  
            "type": "system",  
            "tag": {  
              "name": "Information request",  
              "id": "2473",  
              "parentId": "2470"  
            }  
          }  
        ],  
    "externalId": "12345ab54321",  
    "fullContentLength": 137,  
    "matchingSearchTopics": [  
      {  
        "id": "1234567",  
        "name": "Contoso search topic",  
        "parentId": "7654321"  
      }  
    ],  
  }  
}  

```  

Back to [top](#overview)  

<a name="sampleTwitterRetweet"></a>   
##### <a name="sample-twitter-retweet"></a>Sample Twitter retweet  
This is a sample post payload for a [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] retweet acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]. We've made up some values to anonymize the sample.  

```json  
  "post": {  
    "id": "5786261",  
    "contentType": "POST",  
    "postType": "share",  
    "uri": "http://twitter.com/externalHandle/statuses/1234567890",  
    "publicationDate": "2016-01-23T12:34:56-07:00",  
    "acquisitionDate": "2016-01-23T12:34:56-07:00",  
    "modificationDate": "2016-01-23T12:34:56-07:00",  
    "profile": {  
      "name": "Display Name @chosenUserName",  
      "id": "mse-tw://#12345678",
      "uri": "mse-tw://#12345678",  
      "profileIcon": "https://path/to/the/profileIcon.png",  
      "externalHandle": "chosenUserName",  
      "displayName": "Display Name",  
      "externalId": "7654321"  
    },  
    "source": {  
      "name": "Microblogs",  
      "id": "18",  
      "param": "Twitter"  
    },  
    "content": {  
      "text": "Main text of the tweet."  
    },  
    "language": {  
      "name": "English",  
      "code": "en"  
    },  
    "abstractText": "Main text of the tweet.",  
    "score": {  
      "normalScore": 4,  
      "providerScore": 46.0,  
      "provider": "KLOUT"  
    },  
    "referencedPost": {  
      "profile": {  
        "name": "Display Name of retweeted profile @anotherChosenUserName",  
        "profileIcon": "https://path/to/the/profileIcon.png",  
        "externalHandle": "anotherChosenUserName",  
        "displayName": "Display Name of retweeted profile"  
      },  
      "externalId": "123456789"  
    },  
    "sentiment": {  
      "polarity": "negative",  
      "value": -0.6864638  
    },  
    "tags": [  
      {  
        "probability": 0.8339088,  
        "type": "system",  
        "tag": {  
          "name": "Information request",  
          "id": "2473",  
          "parentId": "2470"  
        }  
      }  
    ],  
    "externalId": "12345ab54321",  
    "fullContentLength": 139,  
    "matchingSearchTopics": [  
      {  
        "name": "Contoso search topic",  
        "id": "12345",  
        "parentId": "54321"  
      }  
    ]  
  }  
}  

```  

Back to [top](#overview)  

<a name="sampleFacebookReply"></a>   
##### <a name="sample-facebook-reply"></a>Sample Facebook reply  
This is a sample post payload for a [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] reply acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]. We've made up some values to anonymize the sample.  

```json  
  "post": {  
    "id": "1234567",  
    "contentType": "POST",  
    "postType": "reply",  
    "uri": "http://www.facebook.com/123456789/posts/987654321?comment_id=123123123",  
    "publicationDate": "2016-01-23T12:34:56-07:00",  
    "acquisitionDate": "2016-01-23T12:34:56-07:00",  
    "modificationDate": "2016-01-23T12:34:56-07:00",  
    "profile": {  
      "name": "Name of the profile",  
      "id": "mse-fb://#109826384650057",
      "uri": "mse-fb://#109826384650057",  
      "profileIcon": "http://graph.facebook.com/123456789/picture?type=square",  
      "externalId": "123456789"  
    },  
    "source": {  
      "name": "Facebook Posts",  
      "id": "16",  
      "param": "Facebook"  
    },  
    "content": {  
      "text": "Text as provided for the reply. This is usually a text that contains several sentences. This example highlights the difference between post.content and post.abstractText."  
    },  
    "language": {  
      "name": "English",  
      "code": "en"  
    },  
    "abstractText": "Text as provided for the reply. This is usually a",  
    "referencedPost": {  
      "externalId": "987654321"  
    },  
    "sentiment": {  
      "polarity": "neutral",  
      "value": -0.0023945  
    },  
    "externalId": "321321321",  
    "fullContentLength": 227,  
    "origin": {  
      "id": "12345",  
      "externalId": "123456789"  
    },  
    "matchingSearchTopics": [  
      {  
        "name": "Contoso search topic",  
        "id": "12345",  
        "parentId": "54321"  
      }  
    ]  
  }  
}  

```  

Back to [top](#overview)  

<a name="sampleVideoPost"></a>   
##### <a name="sample-video-post"></a>Sample video post  
This is a sample post payload for a video post acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]. We've made up some values to anonymize the sample.  

```json  
  "post": {  
    "id": "1234567",  
    "contentType": "VIDEO",  
    "postType": "post",  
    "uri": "http://www.youtube.com/watch?v=videoId",  
    "title": "Title of the video",  
    "publicationDate": "2016-01-23T12:34:56-07:00",  
    "acquisitionDate": "2016-01-23T12:34:56-07:00",  
    "modificationDate": "2016-01-23T12:34:56-07:00",  
    "profile": {  
      "name": "Name of the profile",  
      "id": "mse-vd://#UUFSerfsZZt-sdER", 
      "uri": "mse-vd://#UUFSerfsZZt-sdER", 
      "externalId": "98765abc4321"  
    },  
    "source": {  
      "name": "Youtube Videos",  
      "id": "19",  
      "param": "YoutubeVideos"  
    },  
    "content": {  
      "text": "Text description as provided for the video. This is usually a text that contains several sentences. This example highlights the difference between post.content and post.abstractText."  
    },  
    "language": {  
      "name": "English",  
      "code": "en"  
    },  
    "abstractText": "Text description as provided for the video. This is usually a",  
    "embeddedMedia": "http://www.youtube.com/embed/videoId",  
    "media": [  
      {  
        "type": "VIDEO",  
        "embedUrl": "http://www.youtube.com/embed/videoId"  
      }  
    ],  
    "sentiment": {  
      "polarity": "neutral",  
      "value": -0.07142752  
    },  
    "fullContentLength": 358,  
    "matchingSearchTopics": [  
      {  
        "name": "Contoso search topic",  
        "id": "12345",  
        "parentId": "54321"  
      }  
    ]  
  }  
}  

```  

Back to [top](#overview)  

<a name="sampleBlogPost"></a>   
##### <a name="sample-blog-post"></a>Sample blog post  
This is a sample post payload for a blog post acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]. We've made up some values to anonymize the sample.  

```json  
  "post": {  
    "id": "1234567",  
    "contentType": "POST",  
    "postType": "post",  
    "uri": "http://someblog.tld/path/to/post",  
    "title": "Heading of this blog",  
    "acquisitionDate": "2016-01-23T12:34:56.789+0000",  
    "modificationDate": "2016-01-23T12:34:56.789+0000",  
    "publicationDate": "2016-01-23T12:34:56.789+0000",  
    "profile": {  
      "name": "Name of the profile",  
      "id": "mse-bl://contoso-blog.tumblr.com#1234567", 
      "uri": "mse-bl://contoso-blog.tumblr.com#1234567", 
      "externalId": "987654321"  
    },  
    "source": {  
      "name": "Blogs",  
      "id": "14",  
      "param": "Blogs"  
    },  
    "content": {  
      "text": "Main text content of the blog post. This is usually a text that contains several sentences. This example highlights the difference between post.content.text and post.abstractText."  
    },  
    "language": {  
      "name": "English",  
      "code": "en"  
    },  
    "abstractText": "Main text content of the blog post. This is usually a text that",  
    "sentiment": {  
      "polarity": "positive",  
      "value": 0.3150851  
    },  
    "externalId":"123456789abcd987654321",  
    "fullContentLength": 119,  
    "matchingSearchTopics": [  
      {  
        "id": "1234567",  
        "name": "Contoso search topic",  
        "parentId": "7654321"  
      }  
    ]  
  }  
}  

```  

Back to [top](#overview)  

<a name="sampleForumPost"></a>   
##### <a name="sample-forum-post"></a>Sample forum post  
This is a sample post payload for a forum post acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]. We've made up some values to anonymize the sample.  

```json  
  "post": {  
    "id": "1234567",  
    "contentType": "POST",  
    "postType": "reply",  
    "uri": "http://forumdomain.tld/path/to/the/forum",  
    "publicationDate": "2016-01-23T12:34:56.789+0000",  
    "acquisitionDate": "2016-01-23T12:34:56.789+0000",  
    "modificationDate": "2016-01-23T12:34:56.789+0000",  
    "profile": {  
      "name": "Name of the profile",  
      "id": "mse-bd://forumdomain.tld#someuser", 
      "uri": "mse-bd://forumdomain.tld#someuser", 
      "displayName": "Name of the profile",  
      "externalHandle": "Name of the profile",  
      "externalId": "987654321"  
    },  
    "source": {  
      "name": "Board",  
      "id": "15",  
      "param": "Board"  
    },  
    "content": {  
      "text": "Main text content of the forum post."  
    },  
    "language": {  
      "name": "English",  
      "code": "en"  
    },  
    "abstractText": "Abstract text of the forum post.",  
    "referencedPost": {  
      "externalId":"123456789abcd987654321",  
    },  
    "sentiment": {  
      "polarity": "positive",  
      "value": 0.3773585  
    },  
    "externalId":"123456789abcd987654321",  
    "fullContentLength": 398,  
    "origin": {  
      "externalId":"123ab321",  
      "name":"Title of the forum",  
    },  
    "matchingSearchTopics": [  
      {  
        "id": "1234567",  
        "name": "Contoso search topic",  
        "parentId": "7654321"  
      }  
    ],  
  }  
}  

```  

Back to [top](#overview)  

<a name="metadata"></a>   
## <a name="metadata-json-payload-objects"></a>Metadata JSON payload objects  
Read up on the fields currently supported in the metadata JSON payload.  

<a name="metadata.matchedrules"></a>   
### <a name="metadatamatchedrules"></a>metadata.matchedRules  
Array describing the automation rules that match this post.  

 Property Value Type: object  

 Parent: *metadata*  

 Sample: [metadata sample payload](#metadata_sample_payload)  

 Back to [top](#overview)  

<a name="metadata.matchedrules.id"></a>   
#### <a name="metadatamatchedrulesid"></a>metadata.matchedRules.id  
ID of the automation rule that triggered the creation of this JSON payload.  

 Property Value Type: number (integer)  

 Parent: *metadata.matchedRules*  

 Sample: [metadata sample payload](#metadata_sample_payload)  

<a name="metadata.matchedrules.name"></a>   
#### <a name="metadatamatchedrulesname"></a>metadata.matchedRules.name  
Name of the automation rule that triggered the creation of this JSON payload.  

 Property Value Type: string  

 Parent: *metadata.matchedRules*  

 Sample: [metadata sample payload](#metadata_sample_payload)  

<a name="metadata.properties"></a>   
### <a name="metadataproperties"></a>metadata.properties  
Array of key-value pairs defined in the additional properties of the "Stream to Event Hubs" action in an automation rule.  

 Property Value Type: object  

 Parent: *metadata*  

 Sample: [metadata sample payload](#metadata_sample_payload)  

Back to [top](#overview)  

<a name="metadata.properties.key"></a>   
#### <a name="metadatapropertieskey"></a>metadata.properties.key  
Key of a key-value pair provided in additional properties of an automation rule.  

 Property Value Type: number (integer)  

 Parent: *metadata.properties*  

 Sample: [metadata sample payload](#metadata_sample_payload)  

<a name="metadata.properties.value"></a>   
#### <a name="metadatapropertiesvalue"></a>metadata.properties.value  
Value of a key-value pair provided in additional properties of an automation rule.  

 Property Value Type: string  

 Parent: *metadata.properties*  

 Sample: [metadata sample payload](#metadata_sample_payload)  

<a name="metadata.properties.matchedrule"></a>   
#### <a name="metadatapropertiesmatchedrule"></a>metadata.properties.matchedrule  
ID of the automation rule that contains the additional properties.  

 Property Value Type: string  

 Parent: *metadata.properties*  

 Sample: [metadata sample payload](#metadata_sample_payload)  

<a name="referenceTop"></a>   
## <a name="post-json-payload-objects"></a>Post JSON payload objects  
Read up on the fields currently supported in the post JSON payload.  

<a name="document.id"></a>   
### <a name="postid"></a>post.id  
The unique post ID in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution database.  

 Property Value Type: number (integer)  

 Parent: *post*  

 Sample: [post sample payload](#document_sample_payload)  

 Back to [top](#overview)  

<a name="document.contentType"></a>   
### <a name="postcontenttype"></a>post.contentType  
The type of content in a post.  

 Property Value Type: enum  

 Property Values:  

- POST: The main content is text.  

- IMAGE: The main content is a picture.  

- VIDEO: The main content is a video.  

- LINK: The main content is a hyperlink.  

  Parent: *post*  

  Sample: [post sample payload](#document_sample_payload)  

  Back to [top](#overview)  

<a name="document.postType"></a>   
### <a name="postposttype"></a>post.postType  
The type of post in its conversational context.  

 Property Value Type: enum  

 Property Values:  

- post: An original post, that other posts are related to. Think of the start of a conversation.  

- reply: A reply or a comment to an original post.  

- share: A share or retweet of an original post.  

- privatemessage: A private conversation between two (or more) profiles.  

  Parent: *post*  

  Sample: [post sample payload](#document_sample_payload)  

  Back to [top](#overview)  

<a name="document.uri"></a>   
### <a name="posturi"></a>post.uri  
A backlink to the post's original URI.  

> [!NOTE]
>  The URI of news posts can't be used to link back to the original article.  

 Property Value Type: string  

 Parent: *post*  

 Sample: [post sample payload](#document_sample_payload)  

 Back to [top](#overview)  

<a name="document.title"></a>   
### <a name="posttitle"></a>post.title  
The title as delivered from a post's meta information.  

> [!NOTE]
>  Not all posts have a title.  

 Property Value Type: string  

 Parent: *post*  

 Sample: [post sample payload](#document_sample_payload)  

 Back to [top](#overview)  

<a name="document.acquisitionDate"></a>   
### <a name="postacquisitiondate"></a>post.acquisitionDate  
Timestamp when the post was acquired in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] (in ISO 8601 format).  

 Property Value Type: date-time  

 Parent: *post*  

 Sample: [post sample payload](#document_sample_payload)  

 Back to [top](#overview)  

<a name="document.modificationDate"></a>   
### <a name="postmodificationdate"></a>post.modificationDate  
Timestamp when  the post was last updated in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] (in ISO 8601 format).  

 Property Value Type: date-time  

 Parent: *post*  

 Sample: [post sample payload](#document_sample_payload)  

 Back to [top](#overview)  

<a name="document.publicationDate"></a>   
### <a name="postpublicationdate"></a>post.publicationDate  
Timestamp when the post was published on the source (in ISO 8601 format).  

 Property Value Type: date-time  

 Parent: *post*  

 Sample: [post sample payload](#document_sample_payload)  

 Back to [top](#overview)  

<a name="document.profile"></a>   
### <a name="postprofile"></a>post.profile  
JSON object describing the social profile of the post's author.  

In the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] user interface, this is referred to as an "author". More information: [Find out what people are talking about](analytics-conversations.md), [See author details](author-details.md)  

 Property Value Type: object  


|                           JSON element                            |                                                          Description                                                          |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
|             [post.profile.uri](#document.profile.uri)             | Unique URI of the profile in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution database. |
|     [post.profile.profileIcon](#document.profile.profileIcon)     |                                                URI to public profile picture.                                                 |
| [post.profile.profileLocation](#document.profile.profileLocation) |                     JSON object describing the author's location information as specified by the author.                      |
|  [post.profile.externalHandle](#document.profile.externalHandle)  |                                                 Alias or handle of a profile.                                                 |
|     [post.profile.displayName](#document.profile.displayName)     |                                     Display name of a profile as provided on the source.                                      |
|      [post.profile.externalId](#document.profile.externalId)      |                                               ID of the profile on the source.                                                |
|            [post.profile.name](#document.profile.name)            |     Name for the profile in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] user interface.     |

 Parent: *post*  

 Sample:  

```json  
"profile": {  
  "name": "Display Name @externalHandle",  
  "uri": "mse-tw://#12345678",
  "profileIcon": "https://path/to/the/profileIcon.png" ,  
  "profileLocation": {  
    "locality": "Boston",  
    "adminDistrict": "Massachusetts",  
    "countryRegion": "United States",  
    "coordinates": {  
      "latitude": 42.156028747558594,  
      "longitude": -71.56590270996094  
    },  
    "quadKey": "030233212221101333012"  
  },  
  "displayName": "Display Name ",  
  "externalId": "1234567"  
  },  

```  

Back to [top](#overview)  

<a name="document.profile.uri"></a>   
#### <a name="postprofileuri"></a>post.profile.uri  
Unique URI of the profile in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution database.

> [!NOTE]
> **post.profile.uri** replaced **post.profile.id** in June 2018. You can find more details in [this blog post](https://blogs.msdn.microsoft.com/crm/2017/11/27/deprecation-of-post-profile-id-object-in-social-engagement-json-payload/). 

 Property Value Type: string  

 Parent: *post.profile*  

 Sample: [post.profile](#document.profile)  

<a name="document.profile.profileIcon"></a>   
#### <a name="postprofileprofileicon"></a>post.profile.profileIcon  
URI to public profile picture.  

 Property Value Type: string  

 Parent: *post.profile*  

 Sample: [post.profile](#document.profile)  

<a name="document.profile.profileLocation"></a>   
#### <a name="postprofileprofilelocation"></a>post.profile.profileLocation  
JSON object describing the author's location information as specified by the author.  

For some sources, profile owners can provide their location information. This is shown in the user interface as author location, as opposed to the post location, which specifies from where the post was published. For the post location, see [post.postLocation](#document.postLocation)  

 Property Value Type: object  

|JSON element|Description|  
|------------------|-----------------|  
|[post.profile.profileLocation.locality](#document.profile.profileLocation.locality)|Represents the name of a city.|  
|[post.profile.profileLocation.adminDistrict](#document.profile.profileLocation.adminDistrict)|Represents the name of an administrative division, for example a federal state or a province.|  
|[post.profile.profileLocation.countryRegion](#document.profile.profileLocation.countryRegion)|Represents the name of a country or region.|  
|[post.profile.profileLocation.coordinates](#document.profile.profileLocation.coordinates)|JSON object describing the coordinates of a social profile with latitude and longitude.|  
|[post.profile.profileLocation.coordinates.latitude](#document.profile.profileLocation.coordinates.latitude)|Geographic latitude.|  
|[post.profile.profileLocation.coordinates.longitude](#document.profile.profileLocation.coordinates.longitude)|Geographic longitude.|  
|[post.profile.profileLocation.quadkey](#document.profile.profileLocation.quadkey)|Quadtree key of a location, or “quadkey” for short. Identifies a single tile at a particular level of detail on a map.|  

 Parent: *post.profile*  

 Sample:  

```json  
"profileLocation": {  
  "locality": "Boston",  
  "adminDistrict": "Massachusetts",  
  "countryRegion": "United States",  
  "coordinates": {  
    "latitude": 42.156028747558594,  
    "longitude": -71.56590270996094  
  },  
  "quadKey": "030233212221101333012"  
},  
```  

<a name="document.profile.profileLocation.locality"></a>   
##### <a name="postprofileprofilelocationlocality"></a>post.profile.profileLocation.locality  
Represents the name of a city.  

 Property Value Type: string  

 Parent: *post.profile*  

 Sample: [post.profile.profileLocation](#document.profile.profileLocation)  

<a name="document.profile.profileLocation.adminDistrict"></a>   
##### <a name="postprofileprofilelocationadmindistrict"></a>post.profile.profileLocation.adminDistrict  
Represents the name of an administrative division, for example a federal state or a province.  

 Property Value Type: string  

 Parent: *post.profile*  

 Sample: [post.profile.profileLocation](#document.profile.profileLocation)  

<a name="document.profile.profileLocation.countryRegion"></a>   
##### <a name="postprofileprofilelocationcountryregion"></a>post.profile.profileLocation.countryRegion  
Represents the name of a country or region.  

 Property Value Type: string  

 Parent: *post.profile*  

 Sample: [post.profile.profileLocation](#document.profile.profileLocation)  

<a name="document.profile.profileLocation.coordinates"></a>   
##### <a name="postprofileprofilelocationcoordinates"></a>post.profile.profileLocation.coordinates  
JSON object describing the coordinates of a social profile with latitude and longitude.  

 Sample:  

```json  
"coordinates": {  
  "latitude": 42.156028747558594,  
  "longitude": -71.56590270996094  
},  
```  

<a name="document.profile.profileLocation.coordinates.latitude"></a>   
###### <a name="postprofileprofilelocationcoordinateslatitude"></a>post.profile.profileLocation.coordinates.latitude  
Geographic latitude.  

 Property Value Type: number (floating point)  

 Parent: *post.profile.profileLocation.coordinates*  

 Sample: [post.profile.profileLocation.coordinates](#document.profile.profileLocation.coordinates)  

<a name="document.profile.profileLocation.coordinates.longitude"></a>   
###### <a name="postprofileprofilelocationcoordinateslongitude"></a>post.profile.profileLocation.coordinates.longitude  
Geographic longitude.  

 Property Value Type: number (floating point)  

 Parent: *post.profile.profileLocation.coordinates*  

 Sample: [post.profile.profileLocation.coordinates](#document.profile.profileLocation.coordinates)  

<a name="document.profile.profileLocation.quadkey"></a>   
##### <a name="postprofileprofilelocationquadkey"></a>post.profile.profileLocation.quadkey  
Quadtree key of a location, or “quadkey” for short. Identifies a single tile at a particular level of detail on a map. More information: [MSDN: Bing Maps Tile System](https://msdn.microsoft.com/library/bb259689.aspx)  

 Property Value Type: string  

 Parent: *post.profile.profileLocation*  

 Sample: [post.profile.profileLocation](#document.profile.profileLocation)  

<a name="document.profile.externalHandle"></a>   
#### <a name="postprofileexternalhandle"></a>post.profile.externalHandle  
Alias or handle of a profile.  

 Property Value Type: string  

 Parent: *post.profile*  

 Sample: [post.profile](#document.profile)  

<a name="document.profile.displayName"></a>   
#### <a name="postprofiledisplayname"></a>post.profile.displayName  
Display name of a profile as provided on the source.  

 Property Value Type: string  

 Parent: *post.profile*  

 Sample: [post.profile](#document.profile)  

<a name="document.profile.externalId"></a>   
#### <a name="postprofileexternalid"></a>post.profile.externalId  
ID of the profile on the source.  

 Property Value Type: string  

 Parent: *post.profile*  

 Sample: [post.profile](#document.profile)  

<a name="document.profile.name"></a>   
#### <a name="postprofilename"></a>post.profile.name  
Representation in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] for the name for the profile.  

 Property Value Type: string  

 Parent: *post.profile*  

 Sample: [post.profile](#document.profile)  

<a name="document.source"></a>   
### <a name="postsource"></a>post.source  
JSON object describing on which source a post was found.  

 Sample:  

```json  
"source": {  
  "name": "Microblogs",  
  "id": "18",  
  "param": "Twitter"  
}  

```  

Back to [top](#overview)  

<a name="document.source.id"></a>   
#### <a name="postsourceid"></a>post.source.id  
Represents the internal ID of the source that a post was found on.  

 Property Value Type: string  

 Parent: *post.source*  

 Sample: [post.source](#document.source)  

 Back to [top](#overview)  

<a name="document.source.name"></a>   
#### <a name="postsourcename"></a>post.source.name  
Represents the name of the source that a post was found on.  

 Property Value Type: string  

 Parent: *post.source*  

 Sample: [post.source](#document.source)  

 Back to [top](#overview)  

<a name="document.source.param"></a>   
#### <a name="postsourceparam"></a>post.source.param  
Describes on which source a post was found.  

 Property Value Type: enum  

 The sources availablility extends over time. For an up-to-date list, check back often and follow the release announcements.  

 Parent: *post.source*  

 Sample: [post.source](#document.source)  

 Back to [top](#overview)  

<a name="document.content"></a>   
### <a name="postcontent"></a>post.content  
JSON object describing the text content of a post.  

 Property Value Type: object  

 Parent: *post*  

 Sample:  

```json  
{  
    “post” {  
        "content": {  
            "text": "Lorem ispum dolor sit amet...",  
            "metaText": "Lorem, dolor, amet",  
        }  
    }  
}  
```  

Back to [top](#overview)  

<a name="document.content.text"></a>   
#### <a name="postcontenttext"></a>post.content.text  
Text content of the post.  

 Property Value Type: string  

 Parent: *post.content*  

 Sample: [post.content](#document.content)  

<a name="document.content.metaText"></a>   
#### <a name="postcontentmetatext"></a>post.content.metaText  
Meta text of the post.  

 Property Value Type: string  

 Parent: *post.content*  

 Sample: [post.content](#document.content)  

<a name="document.language"></a>   
### <a name="postlanguage"></a>post.language  
JSON object describing the language of a post.  

 Property Value Type: object  

|JSON element|Description|  
|------------------|-----------------|  
|[post.language.name](#document.language.name)|The localized language name in the locale chosen in Global Settings.|  
|[post.language.code](#document.language.code)|Language code (in ISO 639-1 format) for the post.|  

 Parent: *post*  

 Sample:  

```json  
{  
    “post” {  
        "language": {  
            "name": "Finnish",  
            "code": "fi",  
        }  
    }  
}  
```  

Back to [top](#overview)  

<a name="document.language.name"></a>   
#### <a name="postlanguagename"></a>post.language.name  
The localized language name in the locale chosen in Global Settings.  

 Property Value Type: string  

 Parent: *post.language*  

 Sample: [post.language](#document.language)  

<a name="document.language.code"></a>   
#### <a name="postlanguagecode"></a>post.language.code  
 Language code (in ISO 639-1 format) for the post.  

 Property Value Type: string  

 Parent: *post.language*  

 Sample: [post.language](#document.language)  

<a name="document.abstractText"></a>   
### <a name="postabstracttext"></a>post.abstractText  
Short excerpt of the post.  

 Property Value Type: string  

 Parent: *post*  

 Sample: [post sample payload](#document_sample_payload)  

 Back to [top](#overview)  

<a name="document.score"></a>   
### <a name="postscore"></a>post.score  
JSON object describing the source-specific score of the post or score of the author at the time the post was published.  

 Property Value Type: object  

 Parent: *post*  

 Sample:  

```json  
"score": {  
  "normalScore": 3,  
  "providerScore": 29.0,  
  "provider": "KLOUT"  
}  

```  

Back to [top](#overview)  

<a name="document.score.normalScore"></a>   
#### <a name="postscorenormalscore"></a>post.score.normalScore  
Normalized score, from 1 (lowest) to 5 (highest).  

 Property Value Type: number (integer)  

 Parent: *post.score*  

 Sample: [post.score](#document.score)  

<a name="document.score.providerScore"></a>   
#### <a name="postscoreproviderscore"></a>post.score.providerScore  
Non-normalized score as given by the score provider.  

 Property Value Type: number (floating point)  

 Parent: *post.score*  

 Sample: [post.score](#document.score)  

<a name="document.score.provider"></a>   
#### <a name="postscoreprovider"></a>post.score.provider  
Scoring service the score is provided from.  

 Parent: *post.score*  

 Sample: [post.score](#document.score)  

<a name="document.referencedPost"></a>   
### <a name="postreferencedpost"></a>post.referencedPost  
Information about the post that this post is a reply to, or a share of. referencedPost has the same structure as the parent post, although only a subset of its fields contain data.  

 Property Value Type: object  

 Parent: *post*  

 Sample:  

```json  
{  
    “post” {  
        "referencedPost": {  
            "id": "123456789",  
            "externalId": "654321",  
            "profile": {  
                "id": "123456",  
                "name": "Microsoft"  
            }  
        }  
    }  
}  
```  

 Back to [top](#overview)  

<a name="document.sentiment"></a>   
### <a name="postsentiment"></a>post.sentiment  
JSON object describing the sentiment of a post.  

 Property Value Type: object  

 Parent: *post*  

 Sample:  

```json  
"sentiment": {  
  "polarity": "negative",  
  "value": -0.46005836  
}  
```  

Back to [top](#overview)  

<a name="document.sentiment.polarity"></a>   
#### <a name="postsentimentpolarity"></a>post.sentiment.polarity  
Sentiment value of a post. More information: [Adaptive learning based on changes to organization’s sentiment values](adaptive-learning.md), [Understand the public perception using sentiment analysis](analytics-sentiment.md)  

 Property Value Type: enum  

 Property Values:  

- Positive: Post has a positive sentiment value.  

- Negative: Post has a negative sentiment value.  

- Neutral: Post has neither a positive nor a negative sentiment value.  

  Parent: *post.sentiment*  

  Sample: [post.sentiment](#document.sentiment)  

<a name="document.sentiment.value"></a>   
#### <a name="postsentimentvalue"></a>post.sentiment.value  
Sentiment value as a decimal value between -1 and 1.  

 Property Value Type: number  

 Parent: *post.sentiment*  

 Sample: [post.sentiment](#document.sentiment)  

<a name="document.tags"></a>   
### <a name="posttags"></a>post.tags  
Array of JSON objects representing tags on a post that were added through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].  

 Property Value Type: object  

|JSON element|Description|  
|------------------|-----------------|  
|[post.tags.probability](#document.tags.probability)|Probability provided by the machine learning model with which a system tag applies to a post.|  
|[post.tags.type](#document.tags.type)|Describes how  the tag was assigned to a post.|  
|[post.tags.tag](#document.tags.tag)|JSON object describing the tag.|  
|[post.tags.tag.id](#document.tags.tag.id)|Internal ID of the tag.|  
|[post.tags.tag.name](#document.tags.tag.name)|Name of the tag. Intentions are localized in the locale chosen in Global Settings.|  
|[post.tags.tag.parentId](#document.tags.tag.parentId)|ID of the group containing the tag.|  

 Parent: *post*  

 Sample:  

```json  
"tags": [ {  
  "probability": 0.7554345,  
  "type": "system",  
  "tag": {  
    "id": "12345",  
    "name": "Support request",  
    "parentId": "54321"  
  }, {...} ]  

```  

Back to [top](#overview)  

<a name="document.tags.probability"></a>   
#### <a name="posttagsprobability"></a>post.tags.probability  
 Probability provided by the machine learning model with which a system tag applies to a post.  

 Property Value Type: number  

 Parent: *post.tags*  

 Sample: [post.tags](#document.tags)  

<a name="document.tags.type"></a>   
#### <a name="posttagstype"></a>post.tags.type  
Describes how  the tag was assigned to a post.  

> [!NOTE]
>  Since automation rules pick up the posts before users can manually confirm or add tags to posts, this property usually has the value "system".  

 Property Value Type: enum  

 Property Values:  

- system: [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] added the tag to the post.  

- user: A user manually  added the tag to the post.  

- confirmed: A user confirmed a tag that was added by [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].  

  Parent: *post.tags*  

  Sample: [post.tags](#document.tags)  

<a name="document.tags.tag"></a>   
#### <a name="posttagstag"></a>post.tags.tag  
JSON object describing the tag.  

 Property Value Type: object  

 Parent: *post.tags*  

 Sample:  

```json  
"tag": {  
  "id": "12345",  
  "name": "Support request",  
  "parentId": "54321"  
},  
```  

<a name="document.tags.tag.id"></a>   
##### <a name="posttagstagid"></a>post.tags.tag.id  
Internal ID of the tag.  

 Property Value Type: string  

 Parent: *post.tags.tag*  

 Sample: [post.tags.tag](#document.tags.tag)  

<a name="document.tags.tag.name"></a>   
##### <a name="posttagstagname"></a>post.tags.tag.name  
Name of the tag. Intentions are localized in the locale chosen in Global Settings. More information: [Understand an author's intent using intention analysis](tags.md)  

 Property Value Type: string  

 Parent: *post.tags.tag*  

 Sample: [post.tags.tag](#document.tags.tag)  

<a name="document.tags.tag.parentId"></a>   
##### <a name="posttagstagparentid"></a>post.tags.tag.parentId  
ID of the group containing the tag.  

 Property Value Type: string  

 Parent: *post.tags.tag*  

 Sample: [post.tags.tag](#document.tags.tag)  

<a name="document.externalId"></a>   
### <a name="postexternalid"></a>post.externalId  
ID of the post on the source.  

 Property Value Type: string  

 Parent: *post*  

 Sample: [post sample payload](#document_sample_payload)  

 Back to [top](#overview)  

<a name="document.postLocation"></a>   
### <a name="postpostlocation"></a>post.postLocation  
JSON object describing the location from which a post was published.  

 Property Value Type: object  

|JSON element|Description|  
|------------------|-----------------|  
|[post.postLocation.locality](#document.postLocation.locality)|Represents the name of a city.|  
|[post.postLocation.adminDistrict](#document.postLocation.adminDistrict)|Represents the name of an administrative division, for example a federal state or a province.|  
|[post.postLocation.countryRegion](#document.postLocation.countryRegion)|Represents the name of a country or region.|  
|[post.postLocation.coordinates](#document.postLocation.coordinates)|JSON object describing the coordinates of a post as defined by the author with latitude and longitude.|  
|[post.postLocation.coordinates.latitude](#document.postLocation.coordinates.latitude)|Geographic latitude.|  
|[post.postLocation.coordinates.longitude](#document.postLocation.coordinates.longitude)|Geographic longitude.|  
|[post.postLocation.quadkey](#document.postLocation.quadkey)|Quadtree key of a location, or “quadkey” for short. Identifies a single tile at a particular level of detail on a map.|  

 Parent: *post*  

 Sample:  

```json  
"postLocation": {  
  "adminDistrict": "Massachusetts",  
  "countryRegion": "United States",  
  "coordinates": {  
    "latitude": 42.156028747558594,  
    "longitude": -71.56590270996094  
  },  
  "quadKey": "030233212221101333012"  
},  
```  

 Back to [top](#overview)  

<a name="document.postLocation.locality"></a>   
#### <a name="postpostlocationlocality"></a>post.postLocation.locality  
Represents the name of a city.  

 Property Value Type: string  

 Parent: *post.postLocation*  

 Sample: [post.postLocation](#document.postLocation)  

<a name="document.postLocation.adminDistrict"></a>   
#### <a name="postpostlocationadmindistrict"></a>post.postLocation.adminDistrict  
Represents the name of an administrative division, for example a federal state or a province.  

 Property Value Type: string  

 Parent: *post.postLocation*  

 Sample: [post.postLocation](#document.postLocation)  

<a name="document.postLocation.countryRegion"></a>   
#### <a name="postpostlocationcountryregion"></a>post.postLocation.countryRegion  
Represents the name of a country or region.  

 Property Value Type: string  

 Parent: *post.postLocation*  

 Sample: [post.postLocation](#document.postLocation)  

<a name="document.postLocation.coordinates"></a>   
#### <a name="postpostlocationcoordinates"></a>post.postLocation.coordinates  
JSON object describing the coordinates of a post as defined by the author with latitude and longitude.  

 Property Value Type: object  

 Parent: *post.postLocation*  

 Sample:  

```json  
"coordinates": {  
  "latitude": 42.156028747558594,  
  "longitude": -71.56590270996094  
},  
```  

<a name="document.postLocation.coordinates.latitude"></a>   
##### <a name="postpostlocationcoordinateslatitude"></a>post.postLocation.coordinates.latitude  
Geographic latitude.  

 Property Value Type: number (floating point)  

 Parent: *post.profile.profileLocation.coordinates*  

 Sample: [post.postLocation.coordinates](#document.postLocation.coordinates)  

<a name="document.postLocation.coordinates.longitude"></a>   
##### <a name="postpostlocationcoordinateslongitude"></a>post.postLocation.coordinates.longitude  
Geographic longitude.  

 Property Value Type: number (floating point)  

 Parent: *post.postLocation.coordinates*  

 Sample: [post.postLocation.coordinates](#document.postLocation.coordinates)  

<a name="document.postLocation.quadkey"></a>   
#### <a name="postpostlocationquadkey"></a>post.postLocation.quadkey  
Quadtree key of a location, or “quadkey” for short. Identifies a single tile at a particular level of detail on a map. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [MSDN: Bing Maps Tile System](https://msdn.microsoft.com/library/bb259689.aspx)  

 Property Value Type: string  

 Parent: *post.postLocation*  

 Sample: [post.postLocation](#document.postLocation)  

 Back to [top](#overview)  

<a name="document.fullContentLenght"></a>   
### <a name="postfullcontentlength"></a>post.fullContentLength  
Length in characters of the text-only content in a post.  

 Property Value Type: number (integer)  

 Parent: *post*  

 Sample: [post sample payload](#document_sample_payload)  

 Back to [top](#overview)  

<a name="document.origin"></a>   
### <a name="postorigin"></a>post.origin  
JSON object describing the origin of the post on the source. This is different from the post.source object.  For example: A specific Facebook page on the Facebook source.  

 Property Value Type: object  

 Parent: *post*  

 Sample:  

```json  
"origin": {  
  "id": "12345",  
  "externalId": "54321",  
  "name": "Microsoft Facebook Page",  
},  
```  

Back to [top](#overview)  

<a name="document.origin.id"></a>   
#### <a name="postoriginid"></a>post.origin.id  
ID of the internal representation in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] for the origin of a post.  

 Property Value Type: string  

 Parent: *post.origin*  

 Sample: [post.origin](#document.origin)  

<a name="document.origin.externalId"></a>   
#### <a name="postoriginexternalid"></a>post.origin.externalId  
ID of the origin for the original source of a post.  

 Property Value Type: string  

 Parent: *post.origin*  

 Sample: [post.origin](#document.origin)  

<a name="document.origin.forumName"></a>   
#### <a name="postoriginname"></a>post.origin.name  
Name of the origin of the post on the source.  

 Property Value Type: string  

 Parent: *post.origin*  

 Sample: [post.origin](#document.origin)  

<a name="document.matchingSeachTopics"></a>   
### <a name="postmatchingsearchtopics"></a>post.matchingSearchTopics  
Array of JSON objects describing the list of search topics a post matches.  

 Property Value Type: object  

 Parent: *post*  

 Sample:  

```json  
        "matchingSearchTopics": [{  
          "name": "Contoso Brand Mentions",  
          "id": "12345",  
          "parentId": "54321",  
        },  
{...}]  
```  

Back to [top](#overview)  

<a name="document.matchingSeachTopics.name"></a>   
#### <a name="postmatchingsearchtopicsname"></a>post.matchingSearchTopics.name  
Name of the search topic as defined in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Set up searches to listen to social media conversations](set-up-searches.md)  

 Property Value Type: string  

 Parent: *post.matchingSearchTopics*  

 Sample: [post.matchingSearchTopics](#document.matchingSeachTopics)  

<a name="document.matchingSeachTopics.id"></a>   
#### <a name="postmatchingsearchtopicsid"></a>post.matchingSearchTopics.id  
ID of the search topic.  

 Property Value Type: string  

 Parent: *post.matchingSearchTopics*  

 Sample: [post.matchingSearchTopics](#document.matchingSeachTopics)  

<a name="document.matchingSeachTopics.parentId"></a>   
#### <a name="postmatchingsearchtopicsparentid"></a>post.matchingSearchTopics.parentId  
ID of the search topics's category.  

 Property Value Type: string  

 Parent: *post.matchingSearchTopics*  

 Sample: [post.matchingSearchTopics](#document.matchingSeachTopics)  

<a name="document.externalCategories"></a>   
### <a name="postexternalcategories"></a>post.externalCategories  
Array of categories as delivered by external providers.  

> [!NOTE]
>  This property is only available for News posts.  

 Property Value Type: array of strings  

 Parent: *post*  

 Sample: [post sample payload](#document_sample_payload)  

 Back to [top](#overview)  

<a name="document.contributors"></a>   
### <a name="postcontributors"></a>post.contributors  
Array of names of those who contributed to the post as provided by the data provider.  

> [!NOTE]
>  This property is only available for News posts.  

 Property Value Type: array of strings  

 Parent: *post*  

 Sample: [post sample payload](#document_sample_payload)  

 Back to [top](#overview)  

<a name="document.media"></a>   
### <a name="postmedia"></a>post.media  
Array of JSON objects describing the media in a post.  

 Property Value Type: objects  

|JSON element|Description|  
|------------------|-----------------|  
|[post.media.type](#document.media.type)|The type of media content.|  
|[post.media.embedUrl](#document.media.embedUrl)|URL embedding the media file.|  

 Parent: *post*  

 Sample:  

```json  
"media": {  
  "type": "VIDEO",  
  "embedUrl": "http://www.youtube.com/embed/1dWKf8d8zfg"  
},  
```  

Back to [top](#overview)  

<a name="document.media.type"></a>   
#### <a name="postmediatype"></a>post.media.type  
The type of media content.  

 Property Value Type: enum  

 Property Values:  

- POST: The main media content is text.  

- IMAGE: The main media content is a picture.  

- VIDEO: The main media content is a video.  

- LINK: The main media content is a hyperlink.  

  Parent: *post.media*  

  Sample: [post.media](#document.media)  

<a name="document.media.embedUrl"></a>   
#### <a name="postmediaembedurl"></a>post.media.embedUrl  
URL embedding the media file.  

 Property Value Type: string  

 Parent: *post.media*  

 Sample: [post.media](#document.media)  

<a name="document.externalTopics"></a>   
### <a name="postexternaltopics"></a>post.externalTopics  
Array of topics in this post as delivered by external providers.  

 Property Value Type: array of strings  

 Parent: *post*  

 Sample: [post sample payload](#document_sample_payload)  

 Back to [top](#overview)  

<a name="document.contributorSummary"></a>   
### <a name="postcontributorsummary"></a>post.contributorSummary  
Short description about the contributor for this post as delivered by external providers.  

 Property Value Type: string  

 Parent: *post*  

 Sample: [post sample payload](#document_sample_payload)  

Back to [top](#overview)

### <a name="see-also"></a>See Also  
[Manage connections in Social Engagement](manage-connections.md)   
[Stream data from Social Engagement to Microsoft Azure Event Hubs](stream-data-to-event-hubs.md)   
[Work with events from social posts in Azure Event Hubs](work-with-event-hubs.md)
