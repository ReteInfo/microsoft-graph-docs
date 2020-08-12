---
title: "attachment: createUploadSession"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# attachment: createUploadSession
Namespace: microsoft.graph

**TODO: Add Description**

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
POST /users/{usersId}/messages/{messageId}/attachments/createUploadSession
POST /users/{usersId}/messages/{messageId}/event/attachments/createUploadSession
POST /groups/{groupsId}/conversations/{conversationId}/threads/{conversationThreadId}/posts/{postId}/attachments/createUploadSession
POST /users/{usersId}/outlook/taskGroups/{outlookTaskGroupId}/taskFolders/{outlookTaskFolderId}/tasks/{outlookTaskId}/attachments/createUploadSession
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply JSON representation of the parameters.

The following table shows the parameters that can be used with this action.

|Parameter|Type|Description|
|:---|:---|:---|
|AttachmentItem|[attachmentItem](../resources/attachmentitem.md)|**TODO: Add Description**|



## Response

If successful, this action returns a `200 OK` response code and a [uploadSession](../resources/uploadsession.md) in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "attachment_createuploadsession"
}
-->
``` http
POST https://graph.microsoft.com/beta/users/{usersId}/messages/{messageId}/attachments/createUploadSession

Content-Type: application/json
Content-length: 85

{
  "AttachmentItem": {
    "@odata.type": "microsoft.graph.attachmentItem"
  }
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.uploadSession"
}
-->
``` http
HTTP/1.1 200 OK

Content-Type: application/json
{
  "value": {
    "@odata.type": "microsoft.graph.uploadSession"
  }
}
```
