# ApiMrdSdkJavascript.GetPregnancyLevelOne200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**context** | **String** |  | [optional] 
**type** | **String** |  | [optional] 
**name** | **String** |  | [optional] 
**copyrightHolder** | [**PregnancyCopyrightHolder**](PregnancyCopyrightHolder.md) |  | [optional] 
**license** | **String** |  | [optional] 
**author** | [**PregnancyAuthor**](PregnancyAuthor.md) |  | [optional] 
**about** | [**PregnancyAbout**](PregnancyAbout.md) |  | [optional] 
**description** | **String** |  | [optional] 
**url** | **String** | Canonical content URL. An MRD API URL is normally returned by default and is rewritten where applicable when nhs_links is enabled. | [optional] 
**genre** | **[String]** | Page genres. Pregnancy pages may return an empty array. | [optional] 
**keywords** | [**LivewellAboutAlternateName**](LivewellAboutAlternateName.md) |  | [optional] 
**dateModified** | **Date** |  | [optional] 
**lastReviewed** | **[String]** | Review date and review-due date when supplied by the source. | [optional] 
**hasPart** | [**[PregnancyHealthTopicContent]**](PregnancyHealthTopicContent.md) | Structured health-topic sections. Some category pages may return an empty array. | [optional] 
**breadcrumb** | [**PregnancyBreadcrumb**](PregnancyBreadcrumb.md) |  | [optional] 
**relatedLink** | [**[PregnancyRelatedLink]**](PregnancyRelatedLink.md) | Navigation links associated with the page when supplied by the source. | [optional] 
**headline** | **String** | Page headline. Empty strings are valid. | [optional] 
**contentSubTypes** | **[String]** |  | [optional] 
**mainEntityOfPage** | [**[PregnancyContentElement]**](PregnancyContentElement.md) | Top-level Pregnancy page content. The exact elements depend on the requested NHS page. | [optional] 
**expanderGroups** | [**[PregnancyExpanderGroup]**](PregnancyExpanderGroup.md) | Expandable content groups when supplied by the Pregnancy source data. | [optional] 
**webpage** | **String** | Original NHS webpage URL. | [optional] 
**id** | **Number** |  | [optional] 
**routeMapping** | **String** |  | [optional] 
**redirect** | **String** | Redirect value from the source dataset. Empty strings are valid. | [optional] 
**message** | **String** |  | 
**indexOfPregnancyRoutes** | **String** |  | 



## Enum: MessageEnum


* `the requested data does not exist` (value: `"the requested data does not exist"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)




