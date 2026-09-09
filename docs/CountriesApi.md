# ApiMrdSdkJavascript.CountriesApi

All URIs are relative to *https://api-mrd.mydex.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getAllCountries**](CountriesApi.md#getAllCountries) | **GET** /countries | Retrieve all countries
[**getCountryByCca2**](CountriesApi.md#getCountryByCca2) | **GET** /countries/{cca2} | Retrieve a country by CCA2 code



## getAllCountries

> GetAllCountries200Response getAllCountries(xMrdScopes, opts)

Retrieve all countries

Returns all available countries. Without filters, the model returns the complete country list inside an additional outer array. When filters are supplied, the response is the filtered country list directly.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.CountriesApi();
let xMrdScopes = "countries"; // String | MRD service scope required for Countries endpoints.
let opts = {
  'filters': ["null"] // [String] | Country fields to include in the response. The API accepts comma-separated values such as filters=region,subregion,idd and PHP-style array values such as filters[]=capital&filters[]=maps. Duplicate filters are removed.
};
apiInstance.getAllCountries(xMrdScopes, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Countries endpoints. | [default to &#39;countries&#39;]
 **filters** | [**[String]**](String.md)| Country fields to include in the response. The API accepts comma-separated values such as filters&#x3D;region,subregion,idd and PHP-style array values such as filters[]&#x3D;capital&amp;filters[]&#x3D;maps. Duplicate filters are removed. | [optional] 

### Return type

[**GetAllCountries200Response**](GetAllCountries200Response.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getCountryByCca2

> GetCountryByCca2200Response getCountryByCca2(xMrdScopes, cca2, opts)

Retrieve a country by CCA2 code

Returns the country matching the supplied lookup value. The value is converted to uppercase before lookup. Without filters, a matching country is returned inside an array. With filters, the filtered country object is returned directly. An unknown value returns an empty array.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.CountriesApi();
let xMrdScopes = "countries"; // String | MRD service scope required for Countries endpoints.
let cca2 = "ad"; // String | Country CCA2 lookup value. The supplied value is converted to uppercase before the database lookup. For example, ad is looked up as AD.
let opts = {
  'filters': ["null"] // [String] | Country fields to include in the response. The API accepts comma-separated values such as filters=region,subregion,idd and PHP-style array values such as filters[]=capital&filters[]=maps. Duplicate filters are removed.
};
apiInstance.getCountryByCca2(xMrdScopes, cca2, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Countries endpoints. | [default to &#39;countries&#39;]
 **cca2** | **String**| Country CCA2 lookup value. The supplied value is converted to uppercase before the database lookup. For example, ad is looked up as AD. | 
 **filters** | [**[String]**](String.md)| Country fields to include in the response. The API accepts comma-separated values such as filters&#x3D;region,subregion,idd and PHP-style array values such as filters[]&#x3D;capital&amp;filters[]&#x3D;maps. Duplicate filters are removed. | [optional] 

### Return type

[**GetCountryByCca2200Response**](GetCountryByCca2200Response.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

