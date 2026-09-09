# ApiMrdSdkJavascript.SearchFilter

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**keyword** | **String** | Optional keyword value to search. A non-empty value may contain letters, numbers, commas, spaces and hyphens and cannot consist only of whitespace. | [optional] 
**description** | **String** | Optional page-description value to search. A non-empty value may contain letters, numbers, commas, spaces and hyphens and cannot consist only of whitespace. | [optional] 
**operator** | **String** | Comparison operator used for searchable fields in this filter. | 
**condition** | **String** | Logical condition connecting this filter to another indexed filter. NOT is converted internally to AND NOT. The final filter should normally use an empty condition. | 



## Enum: OperatorEnum


* `EQUAL` (value: `"="`)

* `LIKE` (value: `"LIKE"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)





## Enum: ConditionEnum


* `empty` (value: `""`)

* `AND` (value: `"AND"`)

* `OR` (value: `"OR"`)

* `NOT` (value: `"NOT"`)

* `AND NOT` (value: `"AND NOT"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)




