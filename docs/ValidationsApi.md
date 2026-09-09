# ApiMrdSdkJavascript.ValidationsApi

All URIs are relative to *https://api-mrd.mydex.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getValidationLookupValues**](ValidationsApi.md#getValidationLookupValues) | **GET** /validations/lookup/{field_name} | Retrieve allowed values for a lookup field
[**getValidationMdsAllDatasetsAndFields**](ValidationsApi.md#getValidationMdsAllDatasetsAndFields) | **GET** /validations/mds/all-datasets-and-fields | Retrieve all MDS datasets with extended field information
[**getValidationMdsDatasetFieldTypes**](ValidationsApi.md#getValidationMdsDatasetFieldTypes) | **GET** /validations/mds/dataset/{dataset}/fieldtypes | Retrieve field types for an MDS dataset
[**getValidationMdsDatasetFields**](ValidationsApi.md#getValidationMdsDatasetFields) | **GET** /validations/mds/dataset/{dataset} | Retrieve full field definitions for an MDS dataset
[**getValidationMdsDatasets**](ValidationsApi.md#getValidationMdsDatasets) | **GET** /validations/mds/datasets | Retrieve MDS datasets
[**getValidationMdsDatasetsAndFields**](ValidationsApi.md#getValidationMdsDatasetsAndFields) | **GET** /validations/mds/datasets-and-fields | Retrieve MDS datasets and basic field information
[**getValidationMdsDatasetsByOneStatus**](ValidationsApi.md#getValidationMdsDatasetsByOneStatus) | **GET** /validations/mds/datasets/{status1} | Retrieve MDS datasets by one status
[**getValidationMdsDatasetsByThreeStatuses**](ValidationsApi.md#getValidationMdsDatasetsByThreeStatuses) | **GET** /validations/mds/datasets/{status1}/{status2}/{status3} | Retrieve MDS datasets by three statuses
[**getValidationMdsDatasetsByTwoStatuses**](ValidationsApi.md#getValidationMdsDatasetsByTwoStatuses) | **GET** /validations/mds/datasets/{status1}/{status2} | Retrieve MDS datasets by two statuses
[**getValidationMdsDatasetsByType**](ValidationsApi.md#getValidationMdsDatasetsByType) | **GET** /validations/mds/datasets/type/{type} | Retrieve MDS datasets by type
[**getValidationMdsFieldType**](ValidationsApi.md#getValidationMdsFieldType) | **GET** /validations/mds/field/type/{field} | Retrieve an MDS field&#39;s data type
[**getValidationMdsSummary**](ValidationsApi.md#getValidationMdsSummary) | **GET** /validations/mds/summary | Retrieve an MDS summary
[**getValidationMtsFeatureByName**](ValidationsApi.md#getValidationMtsFeatureByName) | **GET** /validations/mts/features/{feature} | Retrieve an MTS feature by name
[**getValidationMtsFeatures**](ValidationsApi.md#getValidationMtsFeatures) | **GET** /validations/mts/features | Retrieve all MTS features
[**getValidationMtsFeaturesByGroup**](ValidationsApi.md#getValidationMtsFeaturesByGroup) | **GET** /validations/mts/features/group/{group} | Retrieve MTS features by group
[**getValidationMtsTemplateByModule**](ValidationsApi.md#getValidationMtsTemplateByModule) | **GET** /validations/mts/templates/{template}/{module} | Retrieve an MTS template module
[**getValidationMtsTemplateByName**](ValidationsApi.md#getValidationMtsTemplateByName) | **GET** /validations/mts/templates/{template} | Retrieve MTS template records by template name
[**getValidationMtsTemplateBySubsection**](ValidationsApi.md#getValidationMtsTemplateBySubsection) | **GET** /validations/mts/templates/{template}/{module}/{subsection} | Retrieve an MTS template subsection
[**getValidationMtsTemplates**](ValidationsApi.md#getValidationMtsTemplates) | **GET** /validations/mts/templates | Retrieve all MTS template records
[**searchValidationMdsFields**](ValidationsApi.md#searchValidationMdsFields) | **GET** /validations/mds/search/{search} | Search MDS field names
[**validateLookupValue**](ValidationsApi.md#validateLookupValue) | **GET** /validations/lookup/{field_name}/{user_input} | Validate a value against a lookup field



## getValidationLookupValues

> LookupAllowedValuesResponse getValidationLookupValues(fieldName)

Retrieve allowed values for a lookup field

Returns allowed values from the requested validation lookup. Most lookup tables return an array of strings. Structured lookup tables such as race_ethnicity return an array of objects. The field name must map to a supported lu_&lt;field_name&gt; lookup table; country is additionally supported from the Countries database.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
let fieldName = "gender"; // String | Supported validation lookup field. Only lookup datasets currently intended to provide useful values through the Validations API are exposed here.
apiInstance.getValidationLookupValues(fieldName, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fieldName** | **String**| Supported validation lookup field. Only lookup datasets currently intended to provide useful values through the Validations API are exposed here. | 

### Return type

[**LookupAllowedValuesResponse**](LookupAllowedValuesResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMdsAllDatasetsAndFields

> {String: Array} getValidationMdsAllDatasetsAndFields()

Retrieve all MDS datasets with extended field information

Returns all published datasets grouped dynamically by dataset status. Each dataset includes its PDS file type, derived deployment environment and extended information for its published fields.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
apiInstance.getValidationMdsAllDatasetsAndFields((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

**{String: Array}**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMdsDatasetFieldTypes

> {String: MdsFieldType} getValidationMdsDatasetFieldTypes(dataset)

Retrieve field types for an MDS dataset

Returns an object keyed by field machine name containing the field name, display name and data type for fields belonging to the requested dataset.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
let dataset = "ds_employment"; // String | MDS dataset machine name.
apiInstance.getValidationMdsDatasetFieldTypes(dataset, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dataset** | **String**| MDS dataset machine name. | 

### Return type

[**{String: MdsFieldType}**](MdsFieldType.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMdsDatasetFields

> {String: MdsFieldDetails} getValidationMdsDatasetFields(dataset)

Retrieve full field definitions for an MDS dataset

Returns an object keyed by field machine name containing extended definitions for published fields belonging to the requested dataset.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
let dataset = "ds_employment"; // String | MDS dataset machine name.
apiInstance.getValidationMdsDatasetFields(dataset, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dataset** | **String**| MDS dataset machine name. | 

### Return type

[**{String: MdsFieldDetails}**](MdsFieldDetails.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMdsDatasets

> [MdsDatasetSummary] getValidationMdsDatasets()

Retrieve MDS datasets

Returns published MDS datasets including their machine name, display name and status.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
apiInstance.getValidationMdsDatasets((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**[MdsDatasetSummary]**](MdsDatasetSummary.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMdsDatasetsAndFields

> {String: Array} getValidationMdsDatasetsAndFields()

Retrieve MDS datasets and basic field information

Returns published datasets grouped dynamically by dataset status. Each dataset contains its machine name, display name, status, PDS file type and a map of published fields containing field name, display name and data type.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
apiInstance.getValidationMdsDatasetsAndFields((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

**{String: Array}**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMdsDatasetsByOneStatus

> [MdsDatasetSummary] getValidationMdsDatasetsByOneStatus(status1)

Retrieve MDS datasets by one status

Returns published datasets matching the supplied dataset status.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
let status1 = "Live"; // String | First MDS dataset status to include.
apiInstance.getValidationMdsDatasetsByOneStatus(status1, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status1** | **String**| First MDS dataset status to include. | 

### Return type

[**[MdsDatasetSummary]**](MdsDatasetSummary.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMdsDatasetsByThreeStatuses

> [MdsDatasetSummary] getValidationMdsDatasetsByThreeStatuses(status1, status2, status3)

Retrieve MDS datasets by three statuses

Returns published datasets matching any of the supplied dataset statuses.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
let status1 = "Live"; // String | First MDS dataset status to include.
let status2 = "Implement"; // String | Second MDS dataset status to include.
let status3 = "Hold"; // String | Third MDS dataset status to include.
apiInstance.getValidationMdsDatasetsByThreeStatuses(status1, status2, status3, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status1** | **String**| First MDS dataset status to include. | 
 **status2** | **String**| Second MDS dataset status to include. | 
 **status3** | **String**| Third MDS dataset status to include. | 

### Return type

[**[MdsDatasetSummary]**](MdsDatasetSummary.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMdsDatasetsByTwoStatuses

> [MdsDatasetSummary] getValidationMdsDatasetsByTwoStatuses(status1, status2)

Retrieve MDS datasets by two statuses

Returns published datasets matching either of the supplied dataset statuses.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
let status1 = "Live"; // String | First MDS dataset status to include.
let status2 = "Implement"; // String | Second MDS dataset status to include.
apiInstance.getValidationMdsDatasetsByTwoStatuses(status1, status2, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status1** | **String**| First MDS dataset status to include. | 
 **status2** | **String**| Second MDS dataset status to include. | 

### Return type

[**[MdsDatasetSummary]**](MdsDatasetSummary.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMdsDatasetsByType

> [MdsDatasetSummary] getValidationMdsDatasetsByType(type)

Retrieve MDS datasets by type

Returns published datasets belonging to the requested public dataset type. metadata is mapped internally to JSON and transactional is mapped internally to SQLite.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
let type = "transactional"; // String | Public dataset type. metadata maps to JSON-backed datasets and transactional maps to SQLite-backed datasets.
apiInstance.getValidationMdsDatasetsByType(type, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **type** | **String**| Public dataset type. metadata maps to JSON-backed datasets and transactional maps to SQLite-backed datasets. | 

### Return type

[**[MdsDatasetSummary]**](MdsDatasetSummary.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMdsFieldType

> MdsFieldTypeResponse getValidationMdsFieldType(field)

Retrieve an MDS field&#39;s data type

Returns the field machine name, display name and data type for the requested MDS field.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
let field = "field_country"; // String | MDS field machine name.
apiInstance.getValidationMdsFieldType(field, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **field** | **String**| MDS field machine name. | 

### Return type

[**MdsFieldTypeResponse**](MdsFieldTypeResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMdsSummary

> MdsSummaryResponse getValidationMdsSummary()

Retrieve an MDS summary

Returns counts of published datasets, published live datasets and published fields. The current API serializes these database count values as strings.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
apiInstance.getValidationMdsSummary((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**MdsSummaryResponse**](MdsSummaryResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMtsFeatureByName

> [MtsFeatureRecord] getValidationMtsFeatureByName(feature)

Retrieve an MTS feature by name

Returns records whose feature_name matches the supplied feature name.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
let feature = "View Measurements"; // String | Mydex Template System feature name. The endpoint matches this value against feature_name.
apiInstance.getValidationMtsFeatureByName(feature, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **feature** | **String**| Mydex Template System feature name. The endpoint matches this value against feature_name. | 

### Return type

[**[MtsFeatureRecord]**](MtsFeatureRecord.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMtsFeatures

> [MtsFeatureRecord] getValidationMtsFeatures()

Retrieve all MTS features

Returns all Mydex Template System feature records.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
apiInstance.getValidationMtsFeatures((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**[MtsFeatureRecord]**](MtsFeatureRecord.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMtsFeaturesByGroup

> [MtsFeatureRecord] getValidationMtsFeaturesByGroup(group)

Retrieve MTS features by group

Returns records whose feature_group matches the supplied feature group name.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
let group = "Measurements"; // String | Mydex Template System feature group name. The endpoint matches this value against feature_group.
apiInstance.getValidationMtsFeaturesByGroup(group, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **group** | **String**| Mydex Template System feature group name. The endpoint matches this value against feature_group. | 

### Return type

[**[MtsFeatureRecord]**](MtsFeatureRecord.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMtsTemplateByModule

> [MtsTemplateRecord] getValidationMtsTemplateByModule(template, module)

Retrieve an MTS template module

Returns records whose template_name and module_name match the supplied values.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
let template = "About Me"; // String | Mydex Template System template name. The endpoint matches this value against template_name.
let module = "This is Me"; // String | Mydex Template System module name. The endpoint matches this value against module_name.
apiInstance.getValidationMtsTemplateByModule(template, module, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **template** | **String**| Mydex Template System template name. The endpoint matches this value against template_name. | 
 **module** | **String**| Mydex Template System module name. The endpoint matches this value against module_name. | 

### Return type

[**[MtsTemplateRecord]**](MtsTemplateRecord.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMtsTemplateByName

> [MtsTemplateRecord] getValidationMtsTemplateByName(template)

Retrieve MTS template records by template name

Returns records whose template_name matches the supplied template name.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
let template = "About Me"; // String | Mydex Template System template name. The endpoint matches this value against template_name.
apiInstance.getValidationMtsTemplateByName(template, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **template** | **String**| Mydex Template System template name. The endpoint matches this value against template_name. | 

### Return type

[**[MtsTemplateRecord]**](MtsTemplateRecord.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMtsTemplateBySubsection

> [MtsTemplateRecord] getValidationMtsTemplateBySubsection(template, module, subsection)

Retrieve an MTS template subsection

Returns records whose template_name, module_name and module_subsection match the supplied values.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
let template = "About Me"; // String | Mydex Template System template name. The endpoint matches this value against template_name.
let module = "This is Me"; // String | Mydex Template System module name. The endpoint matches this value against module_name.
let subsection = "Personal Details"; // String | Mydex Template System module subsection name. The endpoint matches this value against module_subsection.
apiInstance.getValidationMtsTemplateBySubsection(template, module, subsection, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **template** | **String**| Mydex Template System template name. The endpoint matches this value against template_name. | 
 **module** | **String**| Mydex Template System module name. The endpoint matches this value against module_name. | 
 **subsection** | **String**| Mydex Template System module subsection name. The endpoint matches this value against module_subsection. | 

### Return type

[**[MtsTemplateRecord]**](MtsTemplateRecord.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getValidationMtsTemplates

> [MtsTemplateRecord] getValidationMtsTemplates()

Retrieve all MTS template records

Returns all records from the Mydex Template System templates_features table, including template, module, subsection and route information.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
apiInstance.getValidationMtsTemplates((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**[MtsTemplateRecord]**](MtsTemplateRecord.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## searchValidationMdsFields

> MdsFieldSearchResponse searchValidationMdsFields(search)

Search MDS field names

Searches published MDS field machine names for values containing the supplied search term.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
let search = "birth"; // String | Partial field machine name used to search published MDS fields.
apiInstance.searchValidationMdsFields(search, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **search** | **String**| Partial field machine name used to search published MDS fields. | 

### Return type

[**MdsFieldSearchResponse**](MdsFieldSearchResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## validateLookupValue

> LookupValidationResponse validateLookupValue(fieldName, userInput)

Validate a value against a lookup field

Checks whether the supplied value matches an allowed value associated with the requested lookup. Matching is case-insensitive because the endpoint converts both stored values and the supplied value to uppercase. The result is returned as the string true or false.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';

let apiInstance = new ApiMrdSdkJavascript.ValidationsApi();
let fieldName = "gender"; // String | Supported validation lookup field. Only lookup datasets currently intended to provide useful values through the Validations API are exposed here.
let userInput = "Female"; // String | Value to validate against the allowed values associated with the requested lookup.
apiInstance.validateLookupValue(fieldName, userInput, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fieldName** | **String**| Supported validation lookup field. Only lookup datasets currently intended to provide useful values through the Validations API are exposed here. | 
 **userInput** | **String**| Value to validate against the allowed values associated with the requested lookup. | 

### Return type

[**LookupValidationResponse**](LookupValidationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

