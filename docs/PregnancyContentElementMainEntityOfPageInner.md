# ApiMrdSdkJavascript.PregnancyContentElementMainEntityOfPageInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **String** |  | [optional] 
**name** | **String** |  | [optional] 
**identifier** | [**ConditionVideoObjectIdentifier**](ConditionVideoObjectIdentifier.md) |  | [optional] 
**position** | **Number** |  | [optional] 
**headline** | **String** | Element heading. Empty strings are valid. | [optional] 
**description** | **String** |  | [optional] 
**url** | **String** | Element URL. MRD API URLs are normally returned by default and NHS URLs are returned when nhs_links is enabled. | [optional] 
**text** | **String** | Element content. HTML is retained by default. When no_html is enabled, markup is removed and extracted links may be moved into links. | [optional] 
**caption** | **String** | Caption content when supplied by the source. This content is processed using the selected content formatter. | [optional] 
**credit** | **String** | Credit content when supplied by the source. This content is processed using the selected content formatter. | [optional] 
**links** | [**[PregnancyAnswerLinksInner]**](PregnancyAnswerLinksInner.md) | Links extracted while formatting text, caption, credit or nested content. | [optional] 
**acceptedAnswer** | [**PregnancyAnswer**](PregnancyAnswer.md) |  | [optional] 
**mainEntity** | [**PregnancyContentElementMainEntity**](PregnancyContentElementMainEntity.md) |  | [optional] 
**mainEntityOfPage** | [**[PregnancyContentElementMainEntityOfPageInner]**](PregnancyContentElementMainEntityOfPageInner.md) | Nested Pregnancy page content. | [optional] 
**hasPart** | [**[PregnancyContentElement]**](PregnancyContentElement.md) | Nested Pregnancy content. | [optional] 
**thumbnailUrl** | **String** |  | [optional] 
**uploadDate** | **String** |  | [optional] 
**contentUrl** | **String** |  | [optional] 
**embedUrl** | **String** |  | [optional] 


