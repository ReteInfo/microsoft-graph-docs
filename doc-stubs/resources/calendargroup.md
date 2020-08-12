---
title: "calendarGroup resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# calendarGroup resource type

Namespace: microsoft.graph

**TODO: Add Description**


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List calendarGroups](../api/calendargroup-list.md)|[calendarGroup](../resources/calendargroup.md) collection|Get a list of the [calendarGroup](../resources/calendargroup.md) objects and their properties.|
|[Create calendarGroup](../api/calendargroup-create.md)|[calendarGroup](../resources/calendargroup.md)|Create a new [calendarGroup](../resources/calendargroup.md) object.|
|[Get calendarGroup](../api/calendargroup-get.md)|[calendarGroup](../resources/calendargroup.md)|Read the properties and relationships of a [calendarGroup](../resources/calendargroup.md) object.|
|[Update calendarGroup](../api/calendargroup-update.md)|[calendarGroup](../resources/calendargroup.md)|Update the properties of a [calendarGroup](../resources/calendargroup.md) object.|
|[Delete calendarGroup](../api/calendargroup-delete.md)|None|Deletes a [calendarGroup](../resources/calendargroup.md) object.|
|[List calendars](../api/calendargroup-list-calendars.md)|[calendar](../resources/calendar.md) collection|Get the calendars from the calendars navigation property.|
|[Create calendars](../api/calendargroup-post-calendars.md)|[calendar](../resources/calendar.md)|Create a new calendars object.|
|[Get calendars](../api/calendargroup-get-calendar.md)|[calendar](../resources/calendar.md)|Read the properties and relationships of a [calendar](../resources/calendar.md) object.|
|[Update calendars](../api/calendargroup-update-calendars.md)|[calendar](../resources/calendar.md)|Update the properties of a calendars object.|
|[Delete calendars](../api/calendargroup-delete-calendars.md)|None|Delete a [calendar](../resources/calendar.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|changeKey|String|**TODO: Add Description**|
|classId|Guid|**TODO: Add Description**|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|name|String|**TODO: Add Description**|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|calendars|[calendar](../resources/calendar.md) collection|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.calendarGroup",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.calendarGroup",
  "id": "String (identifier)",
  "name": "String",
  "classId": "Guid",
  "changeKey": "String"
}
```
