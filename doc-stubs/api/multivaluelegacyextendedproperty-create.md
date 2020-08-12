---
title: "Create multiValueLegacyExtendedProperty"
description: "Create a new multiValueLegacyExtendedProperty object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Create multiValueLegacyExtendedProperty
Namespace: microsoft.graph

Create a new [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) object.

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
POST /users/{usersId}/messages/{messageId}/multiValueExtendedProperties
POST /users/{usersId}/contacts/{contactId}/multiValueExtendedProperties
POST /users/{usersId}/messages/{messageId}/event/multiValueExtendedProperties
POST /users/{usersId}/mailFolders/{mailFolderId}/multiValueExtendedProperties
POST /users/{usersId}/contactFolders/{contactFolderId}/multiValueExtendedProperties
POST /users/{usersId}/messages/{messageId}/event/calendar/multiValueExtendedProperties
POST /users/{usersId}/outlook/taskGroups/{outlookTaskGroupId}/taskFolders/{outlookTaskFolderId}/multiValueExtendedProperties
POST /groups/{groupsId}/conversations/{conversationId}/threads/{conversationThreadId}/posts/{postId}/multiValueExtendedProperties
POST /users/{usersId}/outlook/taskGroups/{outlookTaskGroupId}/taskFolders/{outlookTaskFolderId}/tasks/{outlookTaskId}/multiValueExtendedProperties
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) object.

The following table shows the properties that are required when you create the [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|value|String collection|**TODO: Add Description**|



## Response

If successful, this method returns a `201 Created` response code and a [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "create_multivaluelegacyextendedproperty_from_"
}
-->
``` http
POST https://graph.microsoft.com/beta/users/{usersId}/messages/{messageId}/multiValueExtendedProperties
Content-Type: application/json
Content-length: 108

{
  "@odata.type": "#microsoft.graph.multiValueLegacyExtendedProperty",
  "value": [
    "String"
  ]
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.multiValueLegacyExtendedProperty"
}
-->
``` http
HTTP/1.1 201 Created

Content-Type: application/json
{
  "@odata.type": "#microsoft.graph.multiValueLegacyExtendedProperty",
  "id": "24e89013-9013-24e8-1390-e8241390e824",
  "value": [
    "String"
  ]
}
```
