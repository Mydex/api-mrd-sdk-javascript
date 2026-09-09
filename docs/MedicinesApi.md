# ApiMrdSdkJavascript.MedicinesApi

All URIs are relative to *https://api-mrd.mydex.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getMedicineLevelOne**](MedicinesApi.md#getMedicineLevelOne) | **GET** /medicines/{param1} | Retrieve a Medicine page
[**getMedicineLevelThree**](MedicinesApi.md#getMedicineLevelThree) | **GET** /medicines/{param1}/{param2}/{param3} | Retrieve a page within a nested Medicine
[**getMedicineLevelTwo**](MedicinesApi.md#getMedicineLevelTwo) | **GET** /medicines/{param1}/{param2} | Retrieve a Medicine subpage or nested medicine
[**getMedicinesRoutes**](MedicinesApi.md#getMedicinesRoutes) | **GET** /medicines | Retrieve available Medicines routes
[**searchMedicines**](MedicinesApi.md#searchMedicines) | **GET** /medicines/search | Search Medicines content



## getMedicineLevelOne

> GetMedicineLevelOne200Response getMedicineLevelOne(xMrdScopes, param1, opts)

Retrieve a Medicine page

Returns a first-level Medicines page. HTML content is returned by default. no_html removes markup, while nhs_links rewrites eligible MRD links to NHS website links. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MedicinesApi();
let xMrdScopes = "medicines"; // String | MRD service scope required for Medicines endpoints.
let param1 = "insulin"; // String | First Medicines route segment, normally identifying a medicine, medicine category or medicine family.
let opts = {
  'noHtml': "true", // String | When supplied, removes HTML markup from content text. The only accepted value is 'true'. Omit the parameter to leave HTML unchanged.
  'nhsLinks': "true" // String | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.
};
apiInstance.getMedicineLevelOne(xMrdScopes, param1, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Medicines endpoints. | [default to &#39;medicines&#39;]
 **param1** | **String**| First Medicines route segment, normally identifying a medicine, medicine category or medicine family. | 
 **noHtml** | **String**| When supplied, removes HTML markup from content text. The only accepted value is &#39;true&#39;. Omit the parameter to leave HTML unchanged. | [optional] 
 **nhsLinks** | **String**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] 

### Return type

[**GetMedicineLevelOne200Response**](GetMedicineLevelOne200Response.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getMedicineLevelThree

> GetMedicineLevelOne200Response getMedicineLevelThree(xMrdScopes, param1, param2, param3, opts)

Retrieve a page within a nested Medicine

Returns a third-level Medicines route. These responses use the same flexible NHS page structure as other Medicines routes and may include nested question and answer content. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MedicinesApi();
let xMrdScopes = "medicines"; // String | MRD service scope required for Medicines endpoints.
let param1 = "insulin"; // String | First Medicines route segment, normally identifying a medicine, medicine category or medicine family.
let param2 = "rapid-acting-insulin"; // String | Second Medicines route segment, normally identifying a medicine page or a medicine within a broader medicine family.
let param3 = "common-questions-about-rapid-acting-insulin"; // String | Third Medicines route segment identifying a page within a nested medicine, such as common questions, dosage, side effects or interactions.
let opts = {
  'noHtml': "true", // String | When supplied, removes HTML markup from content text. The only accepted value is 'true'. Omit the parameter to leave HTML unchanged.
  'nhsLinks': "true" // String | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.
};
apiInstance.getMedicineLevelThree(xMrdScopes, param1, param2, param3, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Medicines endpoints. | [default to &#39;medicines&#39;]
 **param1** | **String**| First Medicines route segment, normally identifying a medicine, medicine category or medicine family. | 
 **param2** | **String**| Second Medicines route segment, normally identifying a medicine page or a medicine within a broader medicine family. | 
 **param3** | **String**| Third Medicines route segment identifying a page within a nested medicine, such as common questions, dosage, side effects or interactions. | 
 **noHtml** | **String**| When supplied, removes HTML markup from content text. The only accepted value is &#39;true&#39;. Omit the parameter to leave HTML unchanged. | [optional] 
 **nhsLinks** | **String**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] 

### Return type

[**GetMedicineLevelOne200Response**](GetMedicineLevelOne200Response.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getMedicineLevelTwo

> GetMedicineLevelOne200Response getMedicineLevelTwo(xMrdScopes, param1, param2, opts)

Retrieve a Medicine subpage or nested medicine

Returns a specific page within a medicine, or a medicine nested within a broader medicine family. HTML and link behaviour can be controlled using no_html and nhs_links. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MedicinesApi();
let xMrdScopes = "medicines"; // String | MRD service scope required for Medicines endpoints.
let param1 = "insulin"; // String | First Medicines route segment, normally identifying a medicine, medicine category or medicine family.
let param2 = "rapid-acting-insulin"; // String | Second Medicines route segment, normally identifying a medicine page or a medicine within a broader medicine family.
let opts = {
  'noHtml': "true", // String | When supplied, removes HTML markup from content text. The only accepted value is 'true'. Omit the parameter to leave HTML unchanged.
  'nhsLinks': "true" // String | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.
};
apiInstance.getMedicineLevelTwo(xMrdScopes, param1, param2, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Medicines endpoints. | [default to &#39;medicines&#39;]
 **param1** | **String**| First Medicines route segment, normally identifying a medicine, medicine category or medicine family. | 
 **param2** | **String**| Second Medicines route segment, normally identifying a medicine page or a medicine within a broader medicine family. | 
 **noHtml** | **String**| When supplied, removes HTML markup from content text. The only accepted value is &#39;true&#39;. Omit the parameter to leave HTML unchanged. | [optional] 
 **nhsLinks** | **String**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] 

### Return type

[**GetMedicineLevelOne200Response**](GetMedicineLevelOne200Response.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getMedicinesRoutes

> MedicinesRoutesResponse getMedicinesRoutes(xMrdScopes)

Retrieve available Medicines routes

Returns the available routes within the NHS Medicines dataset.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MedicinesApi();
let xMrdScopes = "medicines"; // String | MRD service scope required for Medicines endpoints.
apiInstance.getMedicinesRoutes(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Medicines endpoints. | [default to &#39;medicines&#39;]

### Return type

[**MedicinesRoutesResponse**](MedicinesRoutesResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## searchMedicines

> [MedicineData] searchMedicines(xMrdScopes, filters, opts)

Search Medicines content

Searches the NHS Medicines dataset using structured filters. By default filters search medicine descriptions. When search_all is enabled, additional searchable page content is included. no_html and nhs_links control content and link formatting.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MedicinesApi();
let xMrdScopes = "medicines"; // String | MRD service scope required for Medicines endpoints.
let filters = [new ApiMrdSdkJavascript.MedicinesSearchFilter()]; // [MedicinesSearchFilter] | Structured Medicines search filters supplied using indexed bracket notation, for example filters[0][operator]=LIKE&filters[0][value]=rapid acting insulin&filters[0][condition]=AND&filters[1][operator]=LIKE&filters[1][value]=diabetes&filters[1][condition]=. Each filter must contain exactly value, operator and condition.
let opts = {
  'noHtml': "true", // String | When supplied, removes HTML markup from content text. The only accepted value is 'true'. Omit the parameter to leave HTML unchanged.
  'nhsLinks': "true", // String | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.
  'searchAll': "true" // String | When supplied, the search also checks additional Medicines page content in addition to medicine descriptions. The only accepted value is 'true'. This parameter is only valid on the search endpoint.
};
apiInstance.searchMedicines(xMrdScopes, filters, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Medicines endpoints. | [default to &#39;medicines&#39;]
 **filters** | [**[MedicinesSearchFilter]**](MedicinesSearchFilter.md)| Structured Medicines search filters supplied using indexed bracket notation, for example filters[0][operator]&#x3D;LIKE&amp;filters[0][value]&#x3D;rapid acting insulin&amp;filters[0][condition]&#x3D;AND&amp;filters[1][operator]&#x3D;LIKE&amp;filters[1][value]&#x3D;diabetes&amp;filters[1][condition]&#x3D;. Each filter must contain exactly value, operator and condition. | 
 **noHtml** | **String**| When supplied, removes HTML markup from content text. The only accepted value is &#39;true&#39;. Omit the parameter to leave HTML unchanged. | [optional] 
 **nhsLinks** | **String**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] 
 **searchAll** | **String**| When supplied, the search also checks additional Medicines page content in addition to medicine descriptions. The only accepted value is &#39;true&#39;. This parameter is only valid on the search endpoint. | [optional] 

### Return type

[**[MedicineData]**](MedicineData.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

