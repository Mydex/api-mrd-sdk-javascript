# ApiMrdSdkJavascript.MedicineContentElement

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **String** |  | [optional] 
**name** | **String** |  | [optional] 
**identifier** | [**ConditionVideoObjectIdentifier**](ConditionVideoObjectIdentifier.md) |  | [optional] 
**position** | **Number** |  | [optional] 
**headline** | **String** |  | [optional] 
**description** | **String** |  | [optional] 
**url** | **String** |  | [optional] 
**text** | **String** | Content or question text. HTML is retained by default and removed when no_html is enabled. | [optional] 
**caption** | **String** | Caption content when supplied by the source. This is processed by the same content formatter as text. | [optional] 
**credit** | **String** | Credit content when supplied by the source. This is processed by the same content formatter as text. | [optional] 
**links** | [**[MedicineAnswerLinksInner]**](MedicineAnswerLinksInner.md) |  | [optional] 
**acceptedAnswer** | [**MedicineAnswer**](MedicineAnswer.md) |  | [optional] 
**mainEntity** | [**MedicineContentElementMainEntity**](MedicineContentElementMainEntity.md) |  | [optional] 
**mainEntityOfPage** | [**[MedicineContentElement]**](MedicineContentElement.md) | Nested page elements. | [optional] 
**hasPart** | [**[MedicineContentElement]**](MedicineContentElement.md) | Nested content elements duplicated or grouped under hasPart by the source data. | [optional] 


