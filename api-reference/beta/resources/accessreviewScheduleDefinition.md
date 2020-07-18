---
title: "accessReviewScheduleDefinition resource type"
description: "In the Azure AD access reviews feature, the `accessReviewScheduleDefinition` represents an access review.  "
localization_priority: Normal
author: "raprakasMSFT"
ms.prod: "microsoft-identity-platform"
doc_type: resourcePageType
---

# accessReviewScheduleDefinition resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents an Azure AD [access review](accessreviews-root.md).  


## Methods

| Method		   | Return type	|Description|
|:---------------|:--------|:----------|
|[List accessReviews](../api/accessreview-list-v2.md) |	[accessReviewScheduleDefinition](accessreviewScheduleDefinition.md) collection |	Get a list of all access review definitions. |
|[Get accessReview](../api/accessreview-get-v2.md) |	[accessReviewScheduleDefinition](accessreviewScheduleDefinition.md) |	Get an access review deifintion with a specific ID. |

<!-- commented by raprakasMSFT on 7/17/2020
|[Create accessReview](../api/accessreview-create.md) |	[accessReview](accessreview.md) |	Create a new accessReview. |
|[Update accessReview](../api/accessreview-update.md) |	[accessReview](accessreview.md)	| Update an accessReview. |
|[Delete accessReview](../api/accessreview-delete.md) |	None.	| Delete an accessReview. |
|[List accessReview reviewers](../api/accessreview-listreviewers.md) |		[userIdentity](useridentity.md) collection|	Get the reviewers of an accessReview. |
|[Add accessReview reviewer](../api/accessreview-addreviewer.md) |		None.	|	Add a reviewer to an accessReview. |
|[Remove accessReview reviewer](../api/accessreview-removereviewer.md) | None.	|	Remove a reviewer from an accessReview. |
|[List accessReview decisions](../api/accessreview-listdecisions.md) |		[accessReviewDecision](accessreviewdecision.md) collection|	Get the decisions of an accessReview.|
|[List my accessReview decisions](../api/accessreview-listmydecisions.md) |		[accessReviewDecision](accessreviewdecision.md) collection|	As a reviewer, get my decisions of an accessReview.|
|[Send accessReview reminder](../api/accessreview-sendreminder.md) |		None.	|	Send a reminder to the reviewers of an accessReview. |
|[Stop accessReview](../api/accessreview-stop.md) |		None.	|	Stop an accessReview. |
|[Reset accessReview decisions](../api/accessreview-reset.md) |		None.	|	Reset the decisions in an in-progress accessReview.|
|[Apply accessReview decisions](../api/accessreview-apply.md) |		None.	|	Apply the decisions from a completed accessReview.|
-->

## Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
| `id`                      |`String`                                                        | The feature-assigned unique identifier of an access review. |
| `displayName`             |`String`                                                        | The access review name. Required on create. |
| `createdDateTime`           |`DateTimeOffset`                                                | The DateTime when the review was created. |
| `lastModifiedDateTime`           |`DateTimeOffset`                                                | The DateTime when the review was last modified. |
| `status`           |`String`                                                | Status of an accessReview(Read-only). This describes the phase that an access review is in : For ex: InProgress, Completed. The state transitions are as follows - Initializing -> NotStarted -> Starting -> InProgress -> Completing -> Completed -> AutoReviewing -> AutoReviewed |
| `descriptionForAdmins`           |`String`                                                | Description provided by review creators to provide more context of the review to admins |
| `descriptionForReviewers`           |`String`                                                | 	Description provided by review creators to provide more context of the review to reviewers. This string is displayed in the email that is sent to the reviewer. |
| `createdBy`               |[userIdentity](useridentity.md)                                 | The user who created this review. |
| `scope`               |accessReview <!--Scope-->                              | This is used to define what to include in scope of the review. The scope definition includes defining the query/url and the type of the scope such as MicrosoftGraph/ARM. Examples of URLs/queries include: /groups/{id}/members |
| `settings`                |`microsoft.graph.accessReviewSettings`             | The settings of an accessReview, see type definition below. |
| `reviewers`            |accessReviewScope collection                                                          | TThis collection of access review scopes is used to define who are the reviewers. The scope definition includes defining the query/url and the type of the scope such as MicrosoftGraph/ARM. | 



## Relationships




| Relationship | Type	|Description|
|:---------------|:--------|:----------|
| `instances`               |accessreviewInstance collection                     | Set of access reviews instance for this recurrent access review. |

<!--
Whether these relationships are present on an object, depends upon whether the object is a one-time access review, the series of a recurring access review, or an instance of a recurring access review.

| Scenario | Has reviewers? | Has decisions and myDecisions? | Has instances? |
|:---------|:---------------|:---------------|:---------------|
|One-time access review|Yes | Yes, once started | No |
| Recurring access review | Yes | No | Yes |
| Instance of a recurring access review | Yes | Yes, once started | No |
-->
## JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.accessReview"
}-->

```json
{
 "id": "string (identifier)",
 "displayName": "string",
 "startDateTime": "string (timestamp)",
 "endDateTime": "string (timestamp)",
 "status": "string",
 "description": "string",
 "businessFlowTemplateId": "string (identifier)",
 "reviewerType": "string",
 "createdBy": "microsoft.graph.userIdentity",
 "reviewedEntity": "microsoft.graph.identity",
 "settings": "microsoft.graph.accessReviewSettings",
 "reviewers": "Collection(microsoft.graph.userIdentity)"
}

```

## accessReviewSettings resource type

The **accessReviewSettings** resource type provides additional settings when creating an access review, to control the feature behavior when starting an access review. This type has the following properties. 

| Property                     | Type                      | Description |
| :--------------------------- | :------------------------ | :---------- |
| `mailNotificationsEnabled`|`Boolean`                | Flag to indicate whether sending mails to reviewers and the review creator is enabled.                |
| `remindersEnabled`|`Boolean`       | Flag to indicate whether sending reminder emails to reviewers are enabled.       |
| `justificationRequiredOnApproval`|`Boolean` | Flag to indicate whether reviewers are required to provide a justification when reviewing access.|
| `activityDurationInDays`|`Int64` | The number of days of user activities to show to reviewers. |
| `autoReviewEnabled`|`Boolean` | Flag to indicate whether the feature should set a decision if the reviewer did not supply one, for use with auto-apply, is enabled. |
| `autoReviewSettings`|`microsoft.graph.autoReviewSettings` | Detailed settings for how the feature should set the review decision, for use with auto-apply, described below. |
| `recurrenceSettings`|`microsoft.graph.accessReviewRecurrenceSettings` | Detailed settings for recurrence, described below. |
| `autoApplyReviewResultsEnabled`|`Boolean` | Flag to indicate whether auto-apply capability, to automatically change the target object access resource, is enabled.  If not enabled, a user must, after the review completes, apply the access review. |
| `accessRecommendationsEnabled`|`Boolean` | Flag to indicate whether showing recommendations to reviewers is enabled. |

## autoReviewSettings resource type

The **autoReviewSettings** resource type is embedded within the access review settings, and along with **autoReviewEnabled**, specifies the behavior for the feature when an access review completes. The resource has one property, **notReviewedResult**. If you don't want to have a review decision recorded unless the reviewer makes an explicit choice, set **autoReviewEnabled** to false. If you want to have the system provide a decision even if the reviewer does not make a choice, set **autoReviewEnabled** to `true` and include **autoReviewSettings** with the **notReviewedResult** property. Then, when a review completes, based on the **notReviewedResult** property, the decision will be recorded to either `Approve` or `Deny`.   

| Property                     | Type     | Description                          |
| :--------------------------- | :------  | :----------                          |
| `notReviewedResult`          |`String`  | Must be one of `Approve`, `Deny`, or `Recommendation`.  If `Recommendation`, then `accessRecommendationsEnabled` in the settings should also be set to true. |


## accessReviewRecurrenceSettings resource type

The **accessReviewRecurrenceSettings** resource type is embedded within the access review settings, and specifies that the access review recurs at regular intervals.  This type has the following properties.

| Property                     | Type                                                                                                          | Description |
| :--------------------------- | :------------------------------------------------------------------------------------------------------------ | :---------- |
| `recurrenceType`|`String`    | The recurrence interval, which must be one of `onetime`, `weekly`, `monthly`, `quarterly`, 'halfyearly' or `annual`.                                                                   |
| `recurrenceEndType`|`String` | How the recurrence ends. If it is `never`, then there is no explicit end of the recurrence series. If it is `endBy`, then the recurrence ends at a certain date. If it is `occurrences`, then the series ends after `recurrenceCount` instances of the review have completed. |
| `durationInDays`|`Int32`     | The duration in days for recurrence.                                                                              |
| `recurrenceCount`|`Int32`    | The count of recurrences, if the value of `recurrenceEndType` is `occurrences`, or 0 otherwise.                                                        |


<!--
{
  "type": "#page.annotation",
  "description": "accessReview resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->