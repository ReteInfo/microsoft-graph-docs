---
title: "List calendars"
description: "Get a list of the calendar objects and their properties."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# List calendars
Namespace: microsoft.graph

Get a list of the [calendar](../resources/calendar.md) objects and their properties.

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
GET /users/{usersId}/calendars
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

If successful, this method returns a `200 OK` response code and a collection of [calendar](../resources/calendar.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "get_calendar"
}
-->
``` http
GET https://graph.microsoft.com/beta/users/{usersId}/calendars
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.calendar)"
}
-->
``` http
HTTP/1.1 200 OK

Content-Type: application/json
{
  "value": [
    {
      "@odata.type": "#microsoft.graph.calendar",
      "id": "32b4c718-c718-32b4-18c7-b43218c7b432",
      "name": "String",
      "color": "String",
      "hexColor": "String",
      "isDefaultCalendar": "Boolean",
      "changeKey": "String",
      "canShare": "Boolean",
      "canViewPrivateItems": "Boolean",
      "isShared": "Boolean",
      "isSharedWithMe": "Boolean",
      "canEdit": "Boolean",
      "owner": {
        "@odata.type": "microsoft.graph.emailAddress"
      },
      "calendarGroupId": "String",
      "allowedOnlineMeetingProviders": [
        "String"
      ],
      "defaultOnlineMeetingProvider": "String",
      "isTallyingResponses": "Boolean",
      "isRemovable": "Boolean"
    }
  ]
}
```
