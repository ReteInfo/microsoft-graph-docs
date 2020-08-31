---
title: "Delete event"
description: "Deletes an event object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Delete event
Namespace: microsoft.graph

Deletes an [event](../resources/event.md) object.

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
DELETE /users/{usersId}/events/{eventId}
DELETE /groups/{groupsId}/events/{eventId}
DELETE /users/{usersId}/calendarView/{eventId}
DELETE /groups/{groupsId}/calendarView/{eventId}
DELETE /users/{usersId}/messages/{messageId}/event
DELETE /users/{usersId}/messages/{messageId}/event/instances/{eventId}
DELETE /users/{usersId}/messages/{messageId}/event/calendar/events/{eventId}
DELETE /users/{usersId}/messages/{messageId}/event/exceptionOccurrences/{eventId}
DELETE /users/{usersId}/messages/{messageId}/event/calendar/calendarView/{eventId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `204 No Content` response code.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "delete_event"
}
-->
``` http
DELETE https://graph.microsoft.com/beta/users/{usersId}/events/{eventId}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 204 No Content
```
