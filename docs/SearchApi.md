# ApiMrdSdkJavascript.SearchApi

All URIs are relative to *https://api-mrd.mydex.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**searchMrd**](SearchApi.md#searchMrd) | **GET** /search | Search MRD content



## searchMrd

> SearchMrd200Response searchMrd(xMrdScopes, filters, opts)

Search MRD content

Searches indexed MRD content using structured filters. Filter 0 must contain a keyword. Searchable fields are keyword and page description, using either &#x3D; or LIKE. Indexed filters can be connected using AND, OR, NOT or AND NOT, with NOT converted internally to AND NOT. Results are restricted according to the MRD scopes authorised for the request. By default results are paginated. Supplying the all query parameter disables pagination regardless of the parameter value.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.SearchApi();
let xMrdScopes = "aliss,conditions"; // String | MRD service scope or scopes to include in global search. Supply one or more OAuth-authorised MRD service scopes, comma-delimited or space-delimited.
let filters = [null]; // [SearchFilter] | Structured Search filters supplied using indexed bracket notation. Filter 0 must contain keyword, operator and condition. Additional filters must contain operator and condition and may contain keyword, description or both. For example: filters[0][operator]=LIKE&filters[0][keyword]=smoking&filters[0][condition]=AND&filters[1][operator]=LIKE&filters[1][description]=electronic cigarette&filters[1][condition]=. The final filter should normally use an empty condition.
let opts = {
  'page': 1, // Number | Page number used when pagination is enabled. The value is cast to an integer by the current implementation. If the resulting value is below 1, page 1 is used. The default is 1.
  'all': "true", // String | Disables pagination when this query parameter is present. The current implementation checks only whether the parameter exists; its value is ignored. all=true, all=false and an empty all parameter all enable unpaginated results. Omit the parameter to use pagination.
  'limit': 50 // Number | Requested number of results per page when pagination is enabled. The value is cast to an integer. Values above 100 are reduced to 100. The default is 50.
};
apiInstance.searchMrd(xMrdScopes, filters, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope or scopes to include in global search. Supply one or more OAuth-authorised MRD service scopes, comma-delimited or space-delimited. | [default to &#39;aliss&#39;]
 **filters** | [**[SearchFilter]**](SearchFilter.md)| Structured Search filters supplied using indexed bracket notation. Filter 0 must contain keyword, operator and condition. Additional filters must contain operator and condition and may contain keyword, description or both. For example: filters[0][operator]&#x3D;LIKE&amp;filters[0][keyword]&#x3D;smoking&amp;filters[0][condition]&#x3D;AND&amp;filters[1][operator]&#x3D;LIKE&amp;filters[1][description]&#x3D;electronic cigarette&amp;filters[1][condition]&#x3D;. The final filter should normally use an empty condition. | 
 **page** | **Number**| Page number used when pagination is enabled. The value is cast to an integer by the current implementation. If the resulting value is below 1, page 1 is used. The default is 1. | [optional] [default to 1]
 **all** | **String**| Disables pagination when this query parameter is present. The current implementation checks only whether the parameter exists; its value is ignored. all&#x3D;true, all&#x3D;false and an empty all parameter all enable unpaginated results. Omit the parameter to use pagination. | [optional] 
 **limit** | **Number**| Requested number of results per page when pagination is enabled. The value is cast to an integer. Values above 100 are reduced to 100. The default is 50. | [optional] [default to 50]

### Return type

[**SearchMrd200Response**](SearchMrd200Response.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

