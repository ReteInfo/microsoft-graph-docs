---
title: "List calendarSharingMessages"
description: "Get a list of the calendarSharingMessage objects and their properties."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# List calendarSharingMessages
Namespace: microsoft.graph

Get a list of the [calendarSharingMessage](../resources/calendarsharingmessage.md) objects and their properties.

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
GET ** Collection URI for microsoft.graph.calendarSharingMessage not found
```

## Optional query parameters
This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [calendarSharingMessage](../resources/calendarsharingmessage.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "get_calendarsharingmessage"
}
-->
``` http
GET https://graph.microsoft.com/beta** Collection URI for microsoft.graph.calendarSharingMessage not found
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.calendarSharingMessage)"
}
-->
``` http
HTTP/1.1 200 OK

Content-Type: application/json
{
  "value": [
    {
      "@odata.type": "#microsoft.graph.calendarSharingMessage",
      "id": "094dc5e1-c5e1-094d-e1c5-4d09e1c54d09",
      "createdDateTime": "String (timestamp)",
      "lastModifiedDateTime": "String (timestamp)",
      "changeKey": "String",
      "categories": [
        "String"
      ],
      "receivedDateTime": "String (timestamp)",
      "sentDateTime": "String (timestamp)",
      "hasAttachments": "Boolean",
      "internetMessageId": "String",
      "internetMessageHeaders": [
        {
          "@odata.type": "microsoft.graph.internetMessageHeader"
        }
      ],
      "subject": "String",
      "body": {
        "@odata.type": "microsoft.graph.itemBody"
      },
      "bodyPreview": "String",
      "importance": "String",
      "parentFolderId": "String",
      "sender": {
        "@odata.type": "microsoft.graph.recipient"
      },
      "from": {
        "@odata.type": "microsoft.graph.recipient"
      },
      "toRecipients": [
        {
          "@odata.type": "microsoft.graph.recipient"
        }
      ],
      "ccRecipients": [
        {
          "@odata.type": "microsoft.graph.recipient"
        }
      ],
      "bccRecipients": [
        {
          "@odata.type": "microsoft.graph.recipient"
        }
      ],
      "replyTo": [
        {
          "@odata.type": "microsoft.graph.recipient"
        }
      ],
      "conversationId": "String",
      "conversationIndex": "Binary",
      "uniqueBody": {
        "@odata.type": "microsoft.graph.itemBody"
      },
      "isDeliveryReceiptRequested": "Boolean",
      "isReadReceiptRequested": "Boolean",
      "isRead": "Boolean",
      "isDraft": "Boolean",
      "webLink": "String",
      "mentionsPreview": {
        "@odata.type": "microsoft.graph.mentionsPreview"
      },
      "inferenceClassification": "String",
      "unsubscribeData": [
        "String"
      ],
      "unsubscribeEnabled": "Boolean",
      "flag": {
        "@odata.type": "microsoft.graph.followupFlag"
      },
      "canAccept": "Boolean",
      "suggestedCalendarName": "String",
      "sharingMessageAction": {
        "@odata.type": "microsoft.graph.calendarSharingMessageAction"
      },
      "sharingMessageActions": [
        {
          "@odata.type": "microsoft.graph.calendarSharingMessageAction"
        }
      ]
    }
  ]
}
```
