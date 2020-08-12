---
title: "Update threads"
description: "Update the properties of a threads object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update threads
Namespace: microsoft.graph

Update the properties of a threads object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /groups/{groupsId}/conversations/{conversationId}/threads
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [conversationThread](../resources/conversationthread.md) object.

The following table shows the properties that are required when you create the [conversationThread](../resources/conversationthread.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|toRecipients|[recipient](../resources/recipient.md) collection|**TODO: Add Description**|
|topic|String|**TODO: Add Description**|
|hasAttachments|Boolean|**TODO: Add Description**|
|lastDeliveredDateTime|DateTimeOffset|**TODO: Add Description**|
|uniqueSenders|String collection|**TODO: Add Description**|
|ccRecipients|[recipient](../resources/recipient.md) collection|**TODO: Add Description**|
|preview|String|**TODO: Add Description**|
|isLocked|Boolean|**TODO: Add Description**|



## Response

If successful, this method returns a `200 OK` response code and an updated [conversationThread](../resources/conversationthread.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_threads"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/groups/{groupsId}/conversations/{conversationId}/threads
Content-Type: application/json
Content-length: 438

{
  "@odata.type": "#microsoft.graph.conversationThread",
  "toRecipients": [
    {
      "@odata.type": "microsoft.graph.recipient"
    }
  ],
  "topic": "String",
  "hasAttachments": "Boolean",
  "lastDeliveredDateTime": "String (timestamp)",
  "uniqueSenders": [
    "String"
  ],
  "ccRecipients": [
    {
      "@odata.type": "microsoft.graph.recipient"
    }
  ],
  "preview": "String",
  "isLocked": "Boolean"
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 200 OK

Content-Type: application/json
{
  "@odata.type": "#microsoft.graph.conversationThread",
  "id": "107cecb7-ecb7-107c-b7ec-7c10b7ec7c10",
  "toRecipients": [
    {
      "@odata.type": "microsoft.graph.recipient"
    }
  ],
  "topic": "String",
  "hasAttachments": "Boolean",
  "lastDeliveredDateTime": "String (timestamp)",
  "uniqueSenders": [
    "String"
  ],
  "ccRecipients": [
    {
      "@odata.type": "microsoft.graph.recipient"
    }
  ],
  "preview": "String",
  "isLocked": "Boolean"
}
```
