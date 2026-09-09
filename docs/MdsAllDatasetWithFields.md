# ApiMrdSdkJavascript.MdsAllDatasetWithFields

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**datasetMachineName** | **String** |  | 
**datasetName** | **String** |  | 
**status** | **String** |  | 
**pdsFileType** | **String** |  | 
**environment** | **String** | Environment value derived by the endpoint from the dataset deployment flags. | 
**fields** | [**{String: MdsAllField}**](MdsAllField.md) | Object keyed dynamically by field machine name, containing extended MDS field information. | 



## Enum: PdsFileTypeEnum


* `SQLite` (value: `"SQLite"`)

* `JSON` (value: `"JSON"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)





## Enum: EnvironmentEnum


* `Production` (value: `"Production"`)

* `Dev` (value: `"Dev"`)

* `Sandbox` (value: `"Sandbox"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)




