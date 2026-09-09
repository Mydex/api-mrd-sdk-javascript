# ApiMrdSdkJavascript.LivewellApi

All URIs are relative to *https://api-mrd.mydex.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getLivewellLevelOne**](LivewellApi.md#getLivewellLevelOne) | **GET** /live-well/{param-1} | Retrieve a first-level Live Well page
[**getLivewellLevelThree**](LivewellApi.md#getLivewellLevelThree) | **GET** /live-well/{param-1}/{param-2}/{param-3} | Retrieve a third-level Live Well page
[**getLivewellLevelTwo**](LivewellApi.md#getLivewellLevelTwo) | **GET** /live-well/{param-1}/{param-2} | Retrieve a second-level Live Well page
[**getLivewellRoutes**](LivewellApi.md#getLivewellRoutes) | **GET** /live-well | Retrieve available Live Well routes
[**searchLivewell**](LivewellApi.md#searchLivewell) | **GET** /live-well/search | Search Live Well content



## getLivewellLevelOne

> GetLivewellLevelOne200Response getLivewellLevelOne(xMrdScopes, param1, opts)

Retrieve a first-level Live Well page

Returns a first-level Live Well route. no_html removes HTML markup and nhs_links rewrites eligible MRD links to NHS website links. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.LivewellApi();
let xMrdScopes = "live-well"; // String | MRD service scope required for Live Well endpoints.
let param1 = "eat-well"; // String | First Live Well route segment, normally identifying a top-level topic or category.
let opts = {
  'noHtml': "true", // String | Removes HTML markup from returned Live Well content. When supplied, this parameter must be set to 'true'.
  'nhsLinks': "true" // String | Replaces eligible MRD API links with their NHS website equivalents. When supplied, this parameter must be set to 'true'.
};
apiInstance.getLivewellLevelOne(xMrdScopes, param1, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Live Well endpoints. | [default to &#39;live-well&#39;]
 **param1** | **String**| First Live Well route segment, normally identifying a top-level topic or category. | 
 **noHtml** | **String**| Removes HTML markup from returned Live Well content. When supplied, this parameter must be set to &#39;true&#39;. | [optional] 
 **nhsLinks** | **String**| Replaces eligible MRD API links with their NHS website equivalents. When supplied, this parameter must be set to &#39;true&#39;. | [optional] 

### Return type

[**GetLivewellLevelOne200Response**](GetLivewellLevelOne200Response.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getLivewellLevelThree

> GetLivewellLevelOne200Response getLivewellLevelThree(xMrdScopes, param1, param2, param3, opts)

Retrieve a third-level Live Well page

Returns deeply nested Live Well content. The response uses the same flexible NHS page structure as first-level and second-level routes. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.LivewellApi();
let xMrdScopes = "live-well"; // String | MRD service scope required for Live Well endpoints.
let param1 = "eat-well"; // String | First Live Well route segment, normally identifying a top-level topic or category.
let param2 = "food-types"; // String | Second Live Well route segment, normally identifying a category or page within a top-level topic.
let param3 = "milk-and-dairy-nutrition"; // String | Third Live Well route segment, normally identifying a deeply nested page within a Live Well category.
let opts = {
  'noHtml': "true", // String | Removes HTML markup from returned Live Well content. When supplied, this parameter must be set to 'true'.
  'nhsLinks': "true" // String | Replaces eligible MRD API links with their NHS website equivalents. When supplied, this parameter must be set to 'true'.
};
apiInstance.getLivewellLevelThree(xMrdScopes, param1, param2, param3, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Live Well endpoints. | [default to &#39;live-well&#39;]
 **param1** | **String**| First Live Well route segment, normally identifying a top-level topic or category. | 
 **param2** | **String**| Second Live Well route segment, normally identifying a category or page within a top-level topic. | 
 **param3** | **String**| Third Live Well route segment, normally identifying a deeply nested page within a Live Well category. | 
 **noHtml** | **String**| Removes HTML markup from returned Live Well content. When supplied, this parameter must be set to &#39;true&#39;. | [optional] 
 **nhsLinks** | **String**| Replaces eligible MRD API links with their NHS website equivalents. When supplied, this parameter must be set to &#39;true&#39;. | [optional] 

### Return type

[**GetLivewellLevelOne200Response**](GetLivewellLevelOne200Response.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getLivewellLevelTwo

> GetLivewellLevelOne200Response getLivewellLevelTwo(xMrdScopes, param1, param2, opts)

Retrieve a second-level Live Well page

Returns a second-level page or category within a Live Well topic. HTML and link behaviour can be controlled using no_html and nhs_links. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.LivewellApi();
let xMrdScopes = "live-well"; // String | MRD service scope required for Live Well endpoints.
let param1 = "eat-well"; // String | First Live Well route segment, normally identifying a top-level topic or category.
let param2 = "food-types"; // String | Second Live Well route segment, normally identifying a category or page within a top-level topic.
let opts = {
  'noHtml': "true", // String | Removes HTML markup from returned Live Well content. When supplied, this parameter must be set to 'true'.
  'nhsLinks': "true" // String | Replaces eligible MRD API links with their NHS website equivalents. When supplied, this parameter must be set to 'true'.
};
apiInstance.getLivewellLevelTwo(xMrdScopes, param1, param2, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Live Well endpoints. | [default to &#39;live-well&#39;]
 **param1** | **String**| First Live Well route segment, normally identifying a top-level topic or category. | 
 **param2** | **String**| Second Live Well route segment, normally identifying a category or page within a top-level topic. | 
 **noHtml** | **String**| Removes HTML markup from returned Live Well content. When supplied, this parameter must be set to &#39;true&#39;. | [optional] 
 **nhsLinks** | **String**| Replaces eligible MRD API links with their NHS website equivalents. When supplied, this parameter must be set to &#39;true&#39;. | [optional] 

### Return type

[**GetLivewellLevelOne200Response**](GetLivewellLevelOne200Response.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getLivewellRoutes

> LivewellRoutesResponse getLivewellRoutes(xMrdScopes)

Retrieve available Live Well routes

Returns the available routes within the NHS Live Well dataset.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.LivewellApi();
let xMrdScopes = "live-well"; // String | MRD service scope required for Live Well endpoints.
apiInstance.getLivewellRoutes(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Live Well endpoints. | [default to &#39;live-well&#39;]

### Return type

[**LivewellRoutesResponse**](LivewellRoutesResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## searchLivewell

> [LivewellData] searchLivewell(xMrdScopes, filters, opts)

Search Live Well content

Searches the NHS Live Well dataset using structured filters. By default filters search page descriptions. When search_all is enabled, page-content text is also searched.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.LivewellApi();
let xMrdScopes = "live-well"; // String | MRD service scope required for Live Well endpoints.
let filters = [new ApiMrdSdkJavascript.LivewellSearchFilter()]; // [LivewellSearchFilter] | Structured Live Well search filters supplied using indexed bracket notation, for example filters[0][operator]=LIKE&filters[0][value]=healthy eating&filters[0][condition]=AND&filters[1][operator]=LIKE&filters[1][value]=diet&filters[1][condition]=. Each filter must contain exactly value, operator and condition.
let opts = {
  'noHtml': "true", // String | Removes HTML markup from returned Live Well content. When supplied, this parameter must be set to 'true'.
  'nhsLinks': "true", // String | Replaces eligible MRD API links with their NHS website equivalents. When supplied, this parameter must be set to 'true'.
  'searchAll': "true" // String | Extends Live Well search to page-content text in addition to the default page description. When supplied, this parameter must be set to 'true'. This parameter is only valid on the search endpoint.
};
apiInstance.searchLivewell(xMrdScopes, filters, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Live Well endpoints. | [default to &#39;live-well&#39;]
 **filters** | [**[LivewellSearchFilter]**](LivewellSearchFilter.md)| Structured Live Well search filters supplied using indexed bracket notation, for example filters[0][operator]&#x3D;LIKE&amp;filters[0][value]&#x3D;healthy eating&amp;filters[0][condition]&#x3D;AND&amp;filters[1][operator]&#x3D;LIKE&amp;filters[1][value]&#x3D;diet&amp;filters[1][condition]&#x3D;. Each filter must contain exactly value, operator and condition. | 
 **noHtml** | **String**| Removes HTML markup from returned Live Well content. When supplied, this parameter must be set to &#39;true&#39;. | [optional] 
 **nhsLinks** | **String**| Replaces eligible MRD API links with their NHS website equivalents. When supplied, this parameter must be set to &#39;true&#39;. | [optional] 
 **searchAll** | **String**| Extends Live Well search to page-content text in addition to the default page description. When supplied, this parameter must be set to &#39;true&#39;. This parameter is only valid on the search endpoint. | [optional] 

### Return type

[**[LivewellData]**](LivewellData.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

