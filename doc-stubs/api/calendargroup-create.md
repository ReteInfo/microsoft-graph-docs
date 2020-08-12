---
title: "Create calendarGroup"
description: "Create a new calendarGroup object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Create calendarGroup
Namespace: microsoft.graph

Create a new [calendarGroup](../resources/calendargroup.md) object.

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
POST /users/{usersId}/calendarGroups
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [calendarGroup](../resources/calendargroup.md) object.

The following table shows the properties that are required when you create the [calendarGroup](../resources/calendargroup.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|name|String|**TODO: Add Description**|
|classId|Guid|**TODO: Add Description**|
|changeKey|String|**TODO: Add Description**|



## Response

If successful, this method returns a `201 Created` response code and a [calendarGroup](../resources/calendargroup.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "create_calendargroup_from_"
}
-->
``` http
POST https://graph.microsoft.com/beta/users/{usersId}/calendarGroups
Content-Type: application/json
Content-length: 124

{
  "@odata.type": "#microsoft.graph.calendarGroup",
  "name": "String",
  "classId": "Guid",
  "changeKey": "String"
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendarGroup"
}
-->
``` http
HTTP/1.1 201 Created

Content-Type: application/json
{
  "@odata.type": "#microsoft.graph.calendarGroup",
  "id": "be2bb1d5-b1d5-be2b-d5b1-2bbed5b12bbe",
  "name": "String",
  "classId": "Guid",
  "changeKey": "String"
}
```
