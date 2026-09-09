# ApiMrdSdkJavascript.PregnancySearchFilter

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **String** | Text to search for. The value must not be empty and may contain only letters, numbers and whitespace. | 
**operator** | **String** | Comparison operator supported by the Pregnancy search. | 
**condition** | **String** | Logical condition accepted by the shared search validator. The property is required but may be empty. The Pregnancy search implementation currently combines generated search clauses using AND. | 



## Enum: OperatorEnum


* `LIKE` (value: `"LIKE"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)





## Enum: ConditionEnum


* `empty` (value: `""`)

* `AND` (value: `"AND"`)

* `OR` (value: `"OR"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)




