# ApiMrdSdkJavascript.ConditionPage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**context** | **String** |  | 
**type** | **String** |  | 
**name** | **String** |  | 
**copyrightHolder** | [**ConditionOrganisation**](ConditionOrganisation.md) |  | [optional] 
**license** | **String** |  | [optional] 
**author** | [**ConditionOrganisation**](ConditionOrganisation.md) |  | [optional] 
**about** | [**ConditionAbout**](ConditionAbout.md) |  | [optional] 
**description** | **String** |  | 
**url** | **String** | MRD URL by default or the original NHS URL when nhs_links is enabled. | 
**genre** | **[String]** |  | [optional] 
**keywords** | [**ConditionKeywords**](ConditionKeywords.md) |  | [optional] 
**dateModified** | **Date** |  | [optional] 
**lastReviewed** | **[Date]** | The last review date followed by the next review-due date when supplied. | [optional] 
**breadcrumb** | [**ConditionBreadcrumb**](ConditionBreadcrumb.md) |  | [optional] 
**hasPart** | [**[ConditionHealthTopicContent]**](ConditionHealthTopicContent.md) |  | [optional] 
**relatedLink** | [**[ConditionRelatedLink]**](ConditionRelatedLink.md) |  | [optional] 
**contentSubTypes** | **[String]** |  | [optional] 
**headline** | **String** |  | [optional] 
**mainEntityOfPage** | [**[ConditionContentNode]**](ConditionContentNode.md) |  | [optional] 
**webpage** | **String** |  | [optional] 
**id** | **Number** |  | 
**routeMapping** | **String** |  | 



## Enum: TypeEnum


* `MedicalWebPage` (value: `"MedicalWebPage"`)

* `WebPage` (value: `"WebPage"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)




