# ApiMrdSdkJavascript.ConditionsApi

All URIs are relative to *https://api-mrd.mydex.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getConditionLevelOne**](ConditionsApi.md#getConditionLevelOne) | **GET** /conditions/{param1} | Retrieve a first-level Conditions page
[**getConditionLevelThree**](ConditionsApi.md#getConditionLevelThree) | **GET** /conditions/{param1}/{param2}/{param3} | Retrieve a third-level Conditions page
[**getConditionLevelTwo**](ConditionsApi.md#getConditionLevelTwo) | **GET** /conditions/{param1}/{param2} | Retrieve a second-level Conditions page
[**getConditionRoutes**](ConditionsApi.md#getConditionRoutes) | **GET** /conditions | Retrieve available Conditions routes
[**searchConditions**](ConditionsApi.md#searchConditions) | **GET** /conditions/search | Search Conditions content



## getConditionLevelOne

> ConditionResponse getConditionLevelOne(xMrdScopes, param1, opts)

Retrieve a first-level Conditions page

Returns a Conditions page identified by one route segment. The response may contain HTML by default. Use no_html to return processed plain text and nhs_links to return eligible original NHS URLs.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.ConditionsApi();
let xMrdScopes = "conditions"; // String | MRD service scope required for Conditions endpoints.
let param1 = "adhd-adults"; // String | First Conditions route segment.
let opts = {
  'noHtml': "true", // String | Removes HTML markup from returned content. When supplied, this parameter must be set to 'true'.
  'nhsLinks': "true" // String | Replaces eligible MRD URLs with their NHS website equivalents. When supplied, this parameter must be set to 'true'.
};
apiInstance.getConditionLevelOne(xMrdScopes, param1, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Conditions endpoints. | [default to &#39;conditions&#39;]
 **param1** | **String**| First Conditions route segment. | 
 **noHtml** | **String**| Removes HTML markup from returned content. When supplied, this parameter must be set to &#39;true&#39;. | [optional] 
 **nhsLinks** | **String**| Replaces eligible MRD URLs with their NHS website equivalents. When supplied, this parameter must be set to &#39;true&#39;. | [optional] 

### Return type

[**ConditionResponse**](ConditionResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getConditionLevelThree

> ConditionResponse getConditionLevelThree(xMrdScopes, param1, param2, param3, opts)

Retrieve a third-level Conditions page

Returns a Conditions page identified by three route segments. Responses may contain recursively nested web-page elements and video objects.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.ConditionsApi();
let xMrdScopes = "conditions"; // String | MRD service scope required for Conditions endpoints.
let param1 = "adhd-adults"; // String | First Conditions route segment.
let param2 = "help-and-support"; // String | Second Conditions route segment.
let param3 = "help-for-families"; // String | Third Conditions route segment.
let opts = {
  'noHtml': "true", // String | Removes HTML markup from returned content. When supplied, this parameter must be set to 'true'.
  'nhsLinks': "true" // String | Replaces eligible MRD URLs with their NHS website equivalents. When supplied, this parameter must be set to 'true'.
};
apiInstance.getConditionLevelThree(xMrdScopes, param1, param2, param3, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Conditions endpoints. | [default to &#39;conditions&#39;]
 **param1** | **String**| First Conditions route segment. | 
 **param2** | **String**| Second Conditions route segment. | 
 **param3** | **String**| Third Conditions route segment. | 
 **noHtml** | **String**| Removes HTML markup from returned content. When supplied, this parameter must be set to &#39;true&#39;. | [optional] 
 **nhsLinks** | **String**| Replaces eligible MRD URLs with their NHS website equivalents. When supplied, this parameter must be set to &#39;true&#39;. | [optional] 

### Return type

[**ConditionResponse**](ConditionResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getConditionLevelTwo

> ConditionResponse getConditionLevelTwo(xMrdScopes, param1, param2, opts)

Retrieve a second-level Conditions page

Returns a Conditions page identified by two route segments. The no_html and nhs_links parameters can be used separately or together.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.ConditionsApi();
let xMrdScopes = "conditions"; // String | MRD service scope required for Conditions endpoints.
let param1 = "adhd-adults"; // String | First Conditions route segment.
let param2 = "help-and-support"; // String | Second Conditions route segment.
let opts = {
  'noHtml': "true", // String | Removes HTML markup from returned content. When supplied, this parameter must be set to 'true'.
  'nhsLinks': "true" // String | Replaces eligible MRD URLs with their NHS website equivalents. When supplied, this parameter must be set to 'true'.
};
apiInstance.getConditionLevelTwo(xMrdScopes, param1, param2, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Conditions endpoints. | [default to &#39;conditions&#39;]
 **param1** | **String**| First Conditions route segment. | 
 **param2** | **String**| Second Conditions route segment. | 
 **noHtml** | **String**| Removes HTML markup from returned content. When supplied, this parameter must be set to &#39;true&#39;. | [optional] 
 **nhsLinks** | **String**| Replaces eligible MRD URLs with their NHS website equivalents. When supplied, this parameter must be set to &#39;true&#39;. | [optional] 

### Return type

[**ConditionResponse**](ConditionResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getConditionRoutes

> ConditionsRouteListResponse getConditionRoutes(xMrdScopes)

Retrieve available Conditions routes

Returns absolute URLs for the routes available in the NHS Conditions dataset.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.ConditionsApi();
let xMrdScopes = "conditions"; // String | MRD service scope required for Conditions endpoints.
apiInstance.getConditionRoutes(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Conditions endpoints. | [default to &#39;conditions&#39;]

### Return type

[**ConditionsRouteListResponse**](ConditionsRouteListResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## searchConditions

> ConditionsSearchResponse searchConditions(xMrdScopes, filters, opts)

Search Conditions content

Searches the NHS Conditions dataset. By default the search is performed against page descriptions. When search_all is enabled, page text and expander content are also searched. The no_html option removes HTML from textual content and nhs_links changes eligible MRD URLs to original NHS URLs.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.ConditionsApi();
let xMrdScopes = "conditions"; // String | MRD service scope required for Conditions endpoints.
let filters = [new ApiMrdSdkJavascript.ConditionSearchFilter()]; // [ConditionSearchFilter] | Structured Conditions search filters supplied using indexed bracket notation, for example filters[0][operator]=LIKE&filters[0][value]=cancer&filters[0][condition]=AND&filters[1][operator]=LIKE&filters[1][value]=treatment&filters[1][condition]=. Each filter must contain exactly value, operator and condition.
let opts = {
  'noHtml': "true", // String | Removes HTML markup from returned content. When supplied, this parameter must be set to 'true'.
  'nhsLinks': "true", // String | Replaces eligible MRD URLs with their NHS website equivalents. When supplied, this parameter must be set to 'true'.
  'searchAll': "true" // String | Extends Conditions search to page-content text and expander content in addition to the default page description. When supplied, this parameter must be set to 'true'. This parameter is only valid on the search endpoint.
};
apiInstance.searchConditions(xMrdScopes, filters, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Conditions endpoints. | [default to &#39;conditions&#39;]
 **filters** | [**[ConditionSearchFilter]**](ConditionSearchFilter.md)| Structured Conditions search filters supplied using indexed bracket notation, for example filters[0][operator]&#x3D;LIKE&amp;filters[0][value]&#x3D;cancer&amp;filters[0][condition]&#x3D;AND&amp;filters[1][operator]&#x3D;LIKE&amp;filters[1][value]&#x3D;treatment&amp;filters[1][condition]&#x3D;. Each filter must contain exactly value, operator and condition. | 
 **noHtml** | **String**| Removes HTML markup from returned content. When supplied, this parameter must be set to &#39;true&#39;. | [optional] 
 **nhsLinks** | **String**| Replaces eligible MRD URLs with their NHS website equivalents. When supplied, this parameter must be set to &#39;true&#39;. | [optional] 
 **searchAll** | **String**| Extends Conditions search to page-content text and expander content in addition to the default page description. When supplied, this parameter must be set to &#39;true&#39;. This parameter is only valid on the search endpoint. | [optional] 

### Return type

[**ConditionsSearchResponse**](ConditionsSearchResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

