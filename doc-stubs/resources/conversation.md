---
title: "conversation resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# conversation resource type

Namespace: microsoft.graph

**TODO: Add Description**


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List conversations](../api/group-list-conversations.md)|[conversation](../resources/conversation.md) collection|Get the conversations from the conversations navigation property.|
|[Create conversations](../api/group-post-conversations.md)|[conversation](../resources/conversation.md)|Create a new conversations object.|
|[Update conversations](../api/group-update-conversations.md)|[conversation](../resources/conversation.md)|Update the properties of a conversations object.|
|[Get conversations](../api/group-get-conversation.md)|[conversation](../resources/conversation.md)|Read the properties and relationships of a [conversation](../resources/conversation.md) object.|
|[Delete conversations](../api/group-delete-conversations.md)|None|Delete a [conversation](../resources/conversation.md) object.|
|[List conversations](../api/conversation-list.md)|[conversation](../resources/conversation.md) collection|Get a list of the [conversation](../resources/conversation.md) objects and their properties.|
|[Create conversation](../api/conversation-create.md)|[conversation](../resources/conversation.md)|Create a new [conversation](../resources/conversation.md) object.|
|[Get conversation](../api/conversation-get.md)|[conversation](../resources/conversation.md)|Read the properties and relationships of a [conversation](../resources/conversation.md) object.|
|[Update conversation](../api/conversation-update.md)|[conversation](../resources/conversation.md)|Update the properties of a [conversation](../resources/conversation.md) object.|
|[Delete conversation](../api/conversation-delete.md)|None|Deletes a [conversation](../resources/conversation.md) object.|
|[List threads](../api/conversation-list-threads.md)|[conversationThread](../resources/conversationthread.md) collection|Get the conversationThreads from the threads navigation property.|
|[Create threads](../api/conversation-post-threads.md)|[conversationThread](../resources/conversationthread.md)|Create a new threads object.|
|[Get threads](../api/conversation-get-conversationthread.md)|[conversationThread](../resources/conversationthread.md)|Read the properties and relationships of a [conversationThread](../resources/conversationthread.md) object.|
|[Update threads](../api/conversation-update-threads.md)|[conversationThread](../resources/conversationthread.md)|Update the properties of a threads object.|
|[Delete threads](../api/conversation-delete-threads.md)|None|Delete a [conversationThread](../resources/conversationthread.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|hasAttachments|Boolean|**TODO: Add Description**|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|lastDeliveredDateTime|DateTimeOffset|**TODO: Add Description**|
|preview|String|**TODO: Add Description**|
|topic|String|**TODO: Add Description**|
|uniqueSenders|String collection|**TODO: Add Description**|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|threads|[conversationThread](../resources/conversationthread.md) collection|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.conversation",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.conversation",
  "id": "String (identifier)",
  "topic": "String",
  "hasAttachments": "Boolean",
  "lastDeliveredDateTime": "String (timestamp)",
  "uniqueSenders": [
    "String"
  ],
  "preview": "String"
}
```
