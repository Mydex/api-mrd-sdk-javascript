# ApiMrdSdkJavascript.PregnancyApi

All URIs are relative to *https://api-mrd.mydex.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getPregnancyLevelOne**](PregnancyApi.md#getPregnancyLevelOne) | **GET** /pregnancy/{param1} | Retrieve a Pregnancy page
[**getPregnancyLevelThree**](PregnancyApi.md#getPregnancyLevelThree) | **GET** /pregnancy/{param1}/{param2}/{param3} | Retrieve deeply nested Pregnancy content
[**getPregnancyLevelTwo**](PregnancyApi.md#getPregnancyLevelTwo) | **GET** /pregnancy/{param1}/{param2} | Retrieve a Pregnancy subpage
[**getPregnancyRoutes**](PregnancyApi.md#getPregnancyRoutes) | **GET** /pregnancy | Retrieve available Pregnancy routes
[**searchPregnancy**](PregnancyApi.md#searchPregnancy) | **GET** /pregnancy/search | Search Pregnancy content



## getPregnancyLevelOne

> GetPregnancyLevelOne200Response getPregnancyLevelOne(xMrdScopes, param1, opts)

Retrieve a Pregnancy page

Returns a first-level Pregnancy route. no_html&#x3D;true removes HTML markup, while nhs_links&#x3D;true rewrites eligible MRD API URLs to NHS website URLs. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.PregnancyApi();
let xMrdScopes = "pregnancy"; // String | MRD service scope required for Pregnancy endpoints.
let param1 = "keeping-well"; // String | First Pregnancy route segment, normally identifying a Pregnancy topic, category or section.
let opts = {
  'noHtml': "true", // String | When supplied, removes HTML markup from returned Pregnancy content. The only accepted value is 'true'. Omit the parameter to retain HTML.
  'nhsLinks': "true" // String | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.
};
apiInstance.getPregnancyLevelOne(xMrdScopes, param1, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Pregnancy endpoints. | [default to &#39;pregnancy&#39;]
 **param1** | **String**| First Pregnancy route segment, normally identifying a Pregnancy topic, category or section. | 
 **noHtml** | **String**| When supplied, removes HTML markup from returned Pregnancy content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] 
 **nhsLinks** | **String**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] 

### Return type

[**GetPregnancyLevelOne200Response**](GetPregnancyLevelOne200Response.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getPregnancyLevelThree

> GetPregnancyLevelOne200Response getPregnancyLevelThree(xMrdScopes, param1, param2, param3, opts)

Retrieve deeply nested Pregnancy content

Returns a third-level Pregnancy route. no_html&#x3D;true removes HTML markup, while nhs_links&#x3D;true rewrites eligible MRD API URLs to NHS website URLs. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.PregnancyApi();
let xMrdScopes = "pregnancy"; // String | MRD service scope required for Pregnancy endpoints.
let param1 = "keeping-well"; // String | First Pregnancy route segment, normally identifying a Pregnancy topic, category or section.
let param2 = "pregnancy-and-covid-19"; // String | Second Pregnancy route segment, normally identifying a page within a Pregnancy topic.
let param3 = "4-weeks"; // String | Third Pregnancy route segment identifying a deeply nested Pregnancy page, such as a specific pregnancy week or page within a nested category.
let opts = {
  'noHtml': "true", // String | When supplied, removes HTML markup from returned Pregnancy content. The only accepted value is 'true'. Omit the parameter to retain HTML.
  'nhsLinks': "true" // String | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.
};
apiInstance.getPregnancyLevelThree(xMrdScopes, param1, param2, param3, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Pregnancy endpoints. | [default to &#39;pregnancy&#39;]
 **param1** | **String**| First Pregnancy route segment, normally identifying a Pregnancy topic, category or section. | 
 **param2** | **String**| Second Pregnancy route segment, normally identifying a page within a Pregnancy topic. | 
 **param3** | **String**| Third Pregnancy route segment identifying a deeply nested Pregnancy page, such as a specific pregnancy week or page within a nested category. | 
 **noHtml** | **String**| When supplied, removes HTML markup from returned Pregnancy content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] 
 **nhsLinks** | **String**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] 

### Return type

[**GetPregnancyLevelOne200Response**](GetPregnancyLevelOne200Response.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getPregnancyLevelTwo

> GetPregnancyLevelOne200Response getPregnancyLevelTwo(xMrdScopes, param1, param2, opts)

Retrieve a Pregnancy subpage

Returns a second-level page within a Pregnancy topic. no_html&#x3D;true removes HTML markup, while nhs_links&#x3D;true rewrites eligible MRD API URLs to NHS website URLs. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.PregnancyApi();
let xMrdScopes = "pregnancy"; // String | MRD service scope required for Pregnancy endpoints.
let param1 = "keeping-well"; // String | First Pregnancy route segment, normally identifying a Pregnancy topic, category or section.
let param2 = "pregnancy-and-covid-19"; // String | Second Pregnancy route segment, normally identifying a page within a Pregnancy topic.
let opts = {
  'noHtml': "true", // String | When supplied, removes HTML markup from returned Pregnancy content. The only accepted value is 'true'. Omit the parameter to retain HTML.
  'nhsLinks': "true" // String | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.
};
apiInstance.getPregnancyLevelTwo(xMrdScopes, param1, param2, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Pregnancy endpoints. | [default to &#39;pregnancy&#39;]
 **param1** | **String**| First Pregnancy route segment, normally identifying a Pregnancy topic, category or section. | 
 **param2** | **String**| Second Pregnancy route segment, normally identifying a page within a Pregnancy topic. | 
 **noHtml** | **String**| When supplied, removes HTML markup from returned Pregnancy content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] 
 **nhsLinks** | **String**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] 

### Return type

[**GetPregnancyLevelOne200Response**](GetPregnancyLevelOne200Response.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getPregnancyRoutes

> PregnancyRoutesResponse getPregnancyRoutes(xMrdScopes)

Retrieve available Pregnancy routes

Returns the available routes within the NHS Pregnancy dataset.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.PregnancyApi();
let xMrdScopes = "pregnancy"; // String | MRD service scope required for Pregnancy endpoints.
apiInstance.getPregnancyRoutes(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Pregnancy endpoints. | [default to &#39;pregnancy&#39;]

### Return type

[**PregnancyRoutesResponse**](PregnancyRoutesResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## searchPregnancy

> [PregnancyData] searchPregnancy(xMrdScopes, filters, opts)

Search Pregnancy content

Searches the NHS Pregnancy dataset using structured filters. By default each filter searches the page description. When search_all&#x3D;true, the search additionally checks page-content text and expander-group content. no_html removes HTML markup from returned content and nhs_links rewrites eligible MRD API links to NHS website links.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.PregnancyApi();
let xMrdScopes = "pregnancy"; // String | MRD service scope required for Pregnancy endpoints.
let filters = [new ApiMrdSdkJavascript.PregnancySearchFilter()]; // [PregnancySearchFilter] | Structured Pregnancy search filters supplied using indexed bracket notation, for example filters[0][value]=antenatal appointments&filters[0][operator]=LIKE&filters[0][condition]=. Each filter must contain exactly value, operator and condition.
let opts = {
  'noHtml': "true", // String | When supplied, removes HTML markup from returned Pregnancy content. The only accepted value is 'true'. Omit the parameter to retain HTML.
  'nhsLinks': "true", // String | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.
  'searchAll': "true" // String | When supplied, the search also checks Pregnancy page-content text and expander-group content in addition to the page description. The only accepted value is 'true'. This parameter is only valid on the search endpoint.
};
apiInstance.searchPregnancy(xMrdScopes, filters, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Pregnancy endpoints. | [default to &#39;pregnancy&#39;]
 **filters** | [**[PregnancySearchFilter]**](PregnancySearchFilter.md)| Structured Pregnancy search filters supplied using indexed bracket notation, for example filters[0][value]&#x3D;antenatal appointments&amp;filters[0][operator]&#x3D;LIKE&amp;filters[0][condition]&#x3D;. Each filter must contain exactly value, operator and condition. | 
 **noHtml** | **String**| When supplied, removes HTML markup from returned Pregnancy content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] 
 **nhsLinks** | **String**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] 
 **searchAll** | **String**| When supplied, the search also checks Pregnancy page-content text and expander-group content in addition to the page description. The only accepted value is &#39;true&#39;. This parameter is only valid on the search endpoint. | [optional] 

### Return type

[**[PregnancyData]**](PregnancyData.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

