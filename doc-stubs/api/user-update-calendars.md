---
title: "Update calendars"
description: "Update the properties of a calendars object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update calendars
Namespace: microsoft.graph

Update the properties of a calendars object.

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
PATCH /users/{usersId}/calendars
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [calendar](../resources/calendar.md) object.

The following table shows the properties that are required when you create the [calendar](../resources/calendar.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|name|String|**TODO: Add Description**|
|color|calendarColor|**TODO: Add Description**. Possible values are: `lightBlue`, `lightGreen`, `lightOrange`, `lightGray`, `lightYellow`, `lightTeal`, `lightPink`, `lightBrown`, `lightRed`, `maxColor`, `auto`.|
|hexColor|String|**TODO: Add Description**|
|isDefaultCalendar|Boolean|**TODO: Add Description**|
|changeKey|String|**TODO: Add Description**|
|canShare|Boolean|**TODO: Add Description**|
|canViewPrivateItems|Boolean|**TODO: Add Description**|
|isShared|Boolean|**TODO: Add Description**|
|isSharedWithMe|Boolean|**TODO: Add Description**|
|canEdit|Boolean|**TODO: Add Description**|
|owner|[emailAddress](../resources/emailaddress.md)|**TODO: Add Description**|
|calendarGroupId|String|**TODO: Add Description**|
|allowedOnlineMeetingProviders|onlineMeetingProviderType collection|**TODO: Add Description**. Possible values are: `unknown`, `skypeForBusiness`, `skypeForConsumer`, `teamsForBusiness`.|
|defaultOnlineMeetingProvider|onlineMeetingProviderType|**TODO: Add Description**. Possible values are: `unknown`, `skypeForBusiness`, `skypeForConsumer`, `teamsForBusiness`.|
|isTallyingResponses|Boolean|**TODO: Add Description**|
|isRemovable|Boolean|**TODO: Add Description**|



## Response

If successful, this method returns a `200 OK` response code and an updated [calendar](../resources/calendar.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_calendars"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/users/{usersId}/calendars
Content-Type: application/json
Content-length: 597

{
  "@odata.type": "#microsoft.graph.calendar",
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
```
