---
title: "Update contact"
description: "Update the properties of a contact object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update contact
Namespace: microsoft.graph

Update the properties of a [contact](../resources/contact.md) object.

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
PATCH /users/{usersId}/contacts/{contactId}
PATCH /users/{usersId}/contactFolders/{contactFolderId}/contacts/{contactId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [contact](../resources/contact.md) object.

The following table shows the properties that are required when you create the [contact](../resources/contact.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|createdDateTime|DateTimeOffset|**TODO: Add Description** Inherited from [outlookItem](../resources/outlookitem.md)|
|lastModifiedDateTime|DateTimeOffset|**TODO: Add Description** Inherited from [outlookItem](../resources/outlookitem.md)|
|changeKey|String|**TODO: Add Description** Inherited from [outlookItem](../resources/outlookitem.md)|
|categories|String collection|**TODO: Add Description** Inherited from [outlookItem](../resources/outlookitem.md)|
|parentFolderId|String|**TODO: Add Description**|
|birthday|DateTimeOffset|**TODO: Add Description**|
|fileAs|String|**TODO: Add Description**|
|displayName|String|**TODO: Add Description**|
|givenName|String|**TODO: Add Description**|
|initials|String|**TODO: Add Description**|
|middleName|String|**TODO: Add Description**|
|nickName|String|**TODO: Add Description**|
|surname|String|**TODO: Add Description**|
|title|String|**TODO: Add Description**|
|yomiGivenName|String|**TODO: Add Description**|
|yomiSurname|String|**TODO: Add Description**|
|yomiCompanyName|String|**TODO: Add Description**|
|generation|String|**TODO: Add Description**|
|emailAddresses|[typedEmailAddress](../resources/typedemailaddress.md) collection|**TODO: Add Description**|
|websites|[website](../resources/website.md) collection|**TODO: Add Description**|
|imAddresses|String collection|**TODO: Add Description**|
|jobTitle|String|**TODO: Add Description**|
|companyName|String|**TODO: Add Description**|
|department|String|**TODO: Add Description**|
|officeLocation|String|**TODO: Add Description**|
|profession|String|**TODO: Add Description**|
|assistantName|String|**TODO: Add Description**|
|manager|String|**TODO: Add Description**|
|phones|[phone](../resources/phone.md) collection|**TODO: Add Description**|
|postalAddresses|[physicalAddress](../resources/physicaladdress.md) collection|**TODO: Add Description**|
|spouseName|String|**TODO: Add Description**|
|personalNotes|String|**TODO: Add Description**|
|children|String collection|**TODO: Add Description**|
|weddingAnniversary|Date|**TODO: Add Description**|
|gender|String|**TODO: Add Description**|
|isFavorite|Boolean|**TODO: Add Description**|
|flag|[followupFlag](../resources/followupflag.md)|**TODO: Add Description**|



## Response

If successful, this method returns a `200 OK` response code and an updated [contact](../resources/contact.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_contact"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/users/{usersId}/contacts/{contactId}
Content-Type: application/json
Content-length: 1346

{
  "@odata.type": "#microsoft.graph.contact",
  "changeKey": "String",
  "categories": [
    "String"
  ],
  "parentFolderId": "String",
  "birthday": "String (timestamp)",
  "fileAs": "String",
  "displayName": "String",
  "givenName": "String",
  "initials": "String",
  "middleName": "String",
  "nickName": "String",
  "surname": "String",
  "title": "String",
  "yomiGivenName": "String",
  "yomiSurname": "String",
  "yomiCompanyName": "String",
  "generation": "String",
  "emailAddresses": [
    {
      "@odata.type": "microsoft.graph.typedEmailAddress"
    }
  ],
  "websites": [
    {
      "@odata.type": "microsoft.graph.website"
    }
  ],
  "imAddresses": [
    "String"
  ],
  "jobTitle": "String",
  "companyName": "String",
  "department": "String",
  "officeLocation": "String",
  "profession": "String",
  "assistantName": "String",
  "manager": "String",
  "phones": [
    {
      "@odata.type": "microsoft.graph.phone"
    }
  ],
  "postalAddresses": [
    {
      "@odata.type": "microsoft.graph.physicalAddress"
    }
  ],
  "spouseName": "String",
  "personalNotes": "String",
  "children": [
    "String"
  ],
  "weddingAnniversary": "Date",
  "gender": "String",
  "isFavorite": "Boolean",
  "flag": {
    "@odata.type": "microsoft.graph.followupFlag"
  }
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
  "@odata.type": "#microsoft.graph.contact",
  "id": "9cad47e6-47e6-9cad-e647-ad9ce647ad9c",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "changeKey": "String",
  "categories": [
    "String"
  ],
  "parentFolderId": "String",
  "birthday": "String (timestamp)",
  "fileAs": "String",
  "displayName": "String",
  "givenName": "String",
  "initials": "String",
  "middleName": "String",
  "nickName": "String",
  "surname": "String",
  "title": "String",
  "yomiGivenName": "String",
  "yomiSurname": "String",
  "yomiCompanyName": "String",
  "generation": "String",
  "emailAddresses": [
    {
      "@odata.type": "microsoft.graph.typedEmailAddress"
    }
  ],
  "websites": [
    {
      "@odata.type": "microsoft.graph.website"
    }
  ],
  "imAddresses": [
    "String"
  ],
  "jobTitle": "String",
  "companyName": "String",
  "department": "String",
  "officeLocation": "String",
  "profession": "String",
  "assistantName": "String",
  "manager": "String",
  "phones": [
    {
      "@odata.type": "microsoft.graph.phone"
    }
  ],
  "postalAddresses": [
    {
      "@odata.type": "microsoft.graph.physicalAddress"
    }
  ],
  "spouseName": "String",
  "personalNotes": "String",
  "children": [
    "String"
  ],
  "weddingAnniversary": "Date",
  "gender": "String",
  "isFavorite": "Boolean",
  "flag": {
    "@odata.type": "microsoft.graph.followupFlag"
  }
}
```
