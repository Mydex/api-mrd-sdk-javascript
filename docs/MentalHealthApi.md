# ApiMrdSdkJavascript.MentalHealthApi

All URIs are relative to *https://api-mrd.mydex.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getMentalHealthLevelFour**](MentalHealthApi.md#getMentalHealthLevelFour) | **GET** /mental-health/{param1}/{param2}/{param3}/{param4} | Retrieve deeply nested Mental Health content
[**getMentalHealthLevelOne**](MentalHealthApi.md#getMentalHealthLevelOne) | **GET** /mental-health/{param1} | Retrieve a Mental Health page
[**getMentalHealthLevelThree**](MentalHealthApi.md#getMentalHealthLevelThree) | **GET** /mental-health/{param1}/{param2}/{param3} | Retrieve nested Mental Health content
[**getMentalHealthLevelTwo**](MentalHealthApi.md#getMentalHealthLevelTwo) | **GET** /mental-health/{param1}/{param2} | Retrieve a Mental Health subcategory
[**getMentalHealthRoutes**](MentalHealthApi.md#getMentalHealthRoutes) | **GET** /mental-health | Retrieve available Mental Health routes
[**searchMentalHealth**](MentalHealthApi.md#searchMentalHealth) | **GET** /mental-health/search | Search Mental Health content



## getMentalHealthLevelFour

> GetMentalHealthLevelOne200Response getMentalHealthLevelFour(xMrdScopes, param1, param2, param3, param4, opts)

Retrieve deeply nested Mental Health content

Returns a fourth-level Mental Health route. no_html&#x3D;true removes HTML markup and nhs_links&#x3D;true rewrites eligible MRD API links to NHS website links. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MentalHealthApi();
let xMrdScopes = "mental-health"; // String | MRD service scope required for Mental Health endpoints.
let param1 = "feelings-symptoms-behaviours"; // String | First Mental Health route segment, normally identifying a Mental Health topic, category or section.
let param2 = "feelings-and-symptoms"; // String | Second Mental Health route segment, normally identifying a category or page within a Mental Health topic.
let param3 = "stress"; // String | Third Mental Health route segment identifying a nested Mental Health page.
let param4 = "getting-help"; // String | Fourth Mental Health route segment identifying deeply nested Mental Health content.
let opts = {
  'noHtml': "true", // String | When supplied, removes HTML markup from returned Mental Health content. The only accepted value is 'true'. Omit the parameter to retain HTML.
  'nhsLinks': "true" // String | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.
};
apiInstance.getMentalHealthLevelFour(xMrdScopes, param1, param2, param3, param4, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Mental Health endpoints. | [default to &#39;mental-health&#39;]
 **param1** | **String**| First Mental Health route segment, normally identifying a Mental Health topic, category or section. | 
 **param2** | **String**| Second Mental Health route segment, normally identifying a category or page within a Mental Health topic. | 
 **param3** | **String**| Third Mental Health route segment identifying a nested Mental Health page. | 
 **param4** | **String**| Fourth Mental Health route segment identifying deeply nested Mental Health content. | 
 **noHtml** | **String**| When supplied, removes HTML markup from returned Mental Health content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] 
 **nhsLinks** | **String**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] 

### Return type

[**GetMentalHealthLevelOne200Response**](GetMentalHealthLevelOne200Response.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getMentalHealthLevelOne

> GetMentalHealthLevelOne200Response getMentalHealthLevelOne(xMrdScopes, param1, opts)

Retrieve a Mental Health page

Returns a first-level Mental Health route. no_html&#x3D;true removes HTML markup and nhs_links&#x3D;true rewrites eligible MRD API links to NHS website links. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MentalHealthApi();
let xMrdScopes = "mental-health"; // String | MRD service scope required for Mental Health endpoints.
let param1 = "feelings-symptoms-behaviours"; // String | First Mental Health route segment, normally identifying a Mental Health topic, category or section.
let opts = {
  'noHtml': "true", // String | When supplied, removes HTML markup from returned Mental Health content. The only accepted value is 'true'. Omit the parameter to retain HTML.
  'nhsLinks': "true" // String | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.
};
apiInstance.getMentalHealthLevelOne(xMrdScopes, param1, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Mental Health endpoints. | [default to &#39;mental-health&#39;]
 **param1** | **String**| First Mental Health route segment, normally identifying a Mental Health topic, category or section. | 
 **noHtml** | **String**| When supplied, removes HTML markup from returned Mental Health content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] 
 **nhsLinks** | **String**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] 

### Return type

[**GetMentalHealthLevelOne200Response**](GetMentalHealthLevelOne200Response.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getMentalHealthLevelThree

> GetMentalHealthLevelOne200Response getMentalHealthLevelThree(xMrdScopes, param1, param2, param3, opts)

Retrieve nested Mental Health content

Returns a third-level Mental Health page. no_html&#x3D;true removes HTML markup and nhs_links&#x3D;true rewrites eligible MRD API links to NHS website links. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MentalHealthApi();
let xMrdScopes = "mental-health"; // String | MRD service scope required for Mental Health endpoints.
let param1 = "feelings-symptoms-behaviours"; // String | First Mental Health route segment, normally identifying a Mental Health topic, category or section.
let param2 = "feelings-and-symptoms"; // String | Second Mental Health route segment, normally identifying a category or page within a Mental Health topic.
let param3 = "stress"; // String | Third Mental Health route segment identifying a nested Mental Health page.
let opts = {
  'noHtml': "true", // String | When supplied, removes HTML markup from returned Mental Health content. The only accepted value is 'true'. Omit the parameter to retain HTML.
  'nhsLinks': "true" // String | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.
};
apiInstance.getMentalHealthLevelThree(xMrdScopes, param1, param2, param3, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Mental Health endpoints. | [default to &#39;mental-health&#39;]
 **param1** | **String**| First Mental Health route segment, normally identifying a Mental Health topic, category or section. | 
 **param2** | **String**| Second Mental Health route segment, normally identifying a category or page within a Mental Health topic. | 
 **param3** | **String**| Third Mental Health route segment identifying a nested Mental Health page. | 
 **noHtml** | **String**| When supplied, removes HTML markup from returned Mental Health content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] 
 **nhsLinks** | **String**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] 

### Return type

[**GetMentalHealthLevelOne200Response**](GetMentalHealthLevelOne200Response.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getMentalHealthLevelTwo

> GetMentalHealthLevelOne200Response getMentalHealthLevelTwo(xMrdScopes, param1, param2, opts)

Retrieve a Mental Health subcategory

Returns a second-level Mental Health route. no_html&#x3D;true removes HTML markup and nhs_links&#x3D;true rewrites eligible MRD API links to NHS website links. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MentalHealthApi();
let xMrdScopes = "mental-health"; // String | MRD service scope required for Mental Health endpoints.
let param1 = "feelings-symptoms-behaviours"; // String | First Mental Health route segment, normally identifying a Mental Health topic, category or section.
let param2 = "feelings-and-symptoms"; // String | Second Mental Health route segment, normally identifying a category or page within a Mental Health topic.
let opts = {
  'noHtml': "true", // String | When supplied, removes HTML markup from returned Mental Health content. The only accepted value is 'true'. Omit the parameter to retain HTML.
  'nhsLinks': "true" // String | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.
};
apiInstance.getMentalHealthLevelTwo(xMrdScopes, param1, param2, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Mental Health endpoints. | [default to &#39;mental-health&#39;]
 **param1** | **String**| First Mental Health route segment, normally identifying a Mental Health topic, category or section. | 
 **param2** | **String**| Second Mental Health route segment, normally identifying a category or page within a Mental Health topic. | 
 **noHtml** | **String**| When supplied, removes HTML markup from returned Mental Health content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] 
 **nhsLinks** | **String**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] 

### Return type

[**GetMentalHealthLevelOne200Response**](GetMentalHealthLevelOne200Response.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getMentalHealthRoutes

> MentalHealthRoutesResponse getMentalHealthRoutes(xMrdScopes)

Retrieve available Mental Health routes

Returns the available routes within the NHS Mental Health dataset.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MentalHealthApi();
let xMrdScopes = "mental-health"; // String | MRD service scope required for Mental Health endpoints.
apiInstance.getMentalHealthRoutes(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Mental Health endpoints. | [default to &#39;mental-health&#39;]

### Return type

[**MentalHealthRoutesResponse**](MentalHealthRoutesResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## searchMentalHealth

> [MentalHealthData] searchMentalHealth(xMrdScopes, filters, opts)

Search Mental Health content

Searches the NHS Mental Health dataset using structured filters. By default filters search the page description. search_all&#x3D;true additionally searches page-content text and expander-group content.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MentalHealthApi();
let xMrdScopes = "mental-health"; // String | MRD service scope required for Mental Health endpoints.
let filters = [new ApiMrdSdkJavascript.MentalHealthSearchFilter()]; // [MentalHealthSearchFilter] | Structured Mental Health search filters supplied using indexed bracket notation, for example filters[0][value]=depression&filters[0][operator]=LIKE&filters[0][condition]=. Each filter must contain value, operator and condition. By default the search checks the page description. search_all=true additionally searches page-content text and expander-group content.
let opts = {
  'noHtml': "true", // String | When supplied, removes HTML markup from returned Mental Health content. The only accepted value is 'true'. Omit the parameter to retain HTML.
  'nhsLinks': "true", // String | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.
  'searchAll': "true" // String | When supplied, the search also checks page-content text and expander-group content in addition to the page description. The only accepted value is 'true'. This parameter is only valid on the search endpoint.
};
apiInstance.searchMentalHealth(xMrdScopes, filters, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Mental Health endpoints. | [default to &#39;mental-health&#39;]
 **filters** | [**[MentalHealthSearchFilter]**](MentalHealthSearchFilter.md)| Structured Mental Health search filters supplied using indexed bracket notation, for example filters[0][value]&#x3D;depression&amp;filters[0][operator]&#x3D;LIKE&amp;filters[0][condition]&#x3D;. Each filter must contain value, operator and condition. By default the search checks the page description. search_all&#x3D;true additionally searches page-content text and expander-group content. | 
 **noHtml** | **String**| When supplied, removes HTML markup from returned Mental Health content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] 
 **nhsLinks** | **String**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] 
 **searchAll** | **String**| When supplied, the search also checks page-content text and expander-group content in addition to the page description. The only accepted value is &#39;true&#39;. This parameter is only valid on the search endpoint. | [optional] 

### Return type

[**[MentalHealthData]**](MentalHealthData.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

