# ApiMrdSdkJavascript.MdsFieldDetails

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fieldName** | **String** |  | 
**displayName** | **String** |  | 
**dataType** | **String** |  | 
**notNull** | **String** | Whether the field is marked not-null. The API serializes this value as the string true or false. | 
**_default** | **String** |  | 
**fieldDescription** | **String** |  | 
**fieldExample** | **Object** | Example value associated with the field. The returned value type depends on the field definition. | 
**fieldOrder** | **String** | Field ordering value as serialized by the current API. | 
**length** | **String** | Maximum field length when applicable, serialized by the current API as a string. | 
**status** | **String** |  | 



## Enum: NotNullEnum


* `true` (value: `"true"`)

* `false` (value: `"false"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)




