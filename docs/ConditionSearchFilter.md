# ApiMrdSdkJavascript.ConditionSearchFilter

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **String** | Text to search for. The value must not be empty and may contain only letters, numbers and whitespace. | 
**operator** | **String** | Comparison operator accepted by the Conditions search validator. | 
**condition** | **String** | Logical condition supplied with the filter. The property is required but may be an empty string. The current validator accepts an empty string, AND or OR. | 



## Enum: OperatorEnum


* `LIKE` (value: `"LIKE"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)





## Enum: ConditionEnum


* `empty` (value: `""`)

* `AND` (value: `"AND"`)

* `OR` (value: `"OR"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)




