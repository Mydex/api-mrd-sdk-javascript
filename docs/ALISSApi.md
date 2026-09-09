# ApiMrdSdkJavascript.ALISSApi

All URIs are relative to *https://api-mrd.mydex.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**countAlissServices**](ALISSApi.md#countAlissServices) | **GET** /aliss/get-services/search/count | Count matching ALISS services
[**getAlissAccessibilityFeatures**](ALISSApi.md#getAlissAccessibilityFeatures) | **GET** /aliss/accessibility-features | Retrieve ALISS accessibility features
[**getAlissCategories**](ALISSApi.md#getAlissCategories) | **GET** /aliss/categories | Retrieve ALISS categories
[**getAlissCommunityGroups**](ALISSApi.md#getAlissCommunityGroups) | **GET** /aliss/community-groups | Retrieve ALISS community groups
[**getAlissOrganisations**](ALISSApi.md#getAlissOrganisations) | **GET** /aliss/organisations | Retrieve ALISS organisations
[**getAlissServiceAreas**](ALISSApi.md#getAlissServiceAreas) | **GET** /aliss/service-areas | Retrieve ALISS service areas
[**getAlissServicesByIds**](ALISSApi.md#getAlissServicesByIds) | **GET** /aliss/get-services/{service-ids} | Retrieve ALISS services by ID
[**searchAlissServices**](ALISSApi.md#searchAlissServices) | **GET** /aliss/get-services/search | Search ALISS services



## countAlissServices

> [AlissServiceCount] countAlissServices(xMrdScopes, opts)

Count matching ALISS services

Returns the number of distinct ALISS services matching the supplied structured filters.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.ALISSApi();
let xMrdScopes = "aliss"; // String | MRD service scope required for ALISS endpoints.
let opts = {
  'filters': new ApiMrdSdkJavascript.SearchAlissServicesFiltersParameter() // SearchAlissServicesFiltersParameter | Structured filters used to search ALISS services. Supported datasets are services, organisations, categories, service_areas, locations, accessibility_features and community_groups. Each filter requires field, value and operator. Every filter except the final filter must also contain condition.
};
apiInstance.countAlissServices(xMrdScopes, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for ALISS endpoints. | [default to &#39;aliss&#39;]
 **filters** | [**SearchAlissServicesFiltersParameter**](.md)| Structured filters used to search ALISS services. Supported datasets are services, organisations, categories, service_areas, locations, accessibility_features and community_groups. Each filter requires field, value and operator. Every filter except the final filter must also contain condition. | [optional] 

### Return type

[**[AlissServiceCount]**](AlissServiceCount.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAlissAccessibilityFeatures

> [AlissNamedSlugItem] getAlissAccessibilityFeatures(xMrdScopes)

Retrieve ALISS accessibility features

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.ALISSApi();
let xMrdScopes = "aliss"; // String | MRD service scope required for ALISS endpoints.
apiInstance.getAlissAccessibilityFeatures(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for ALISS endpoints. | [default to &#39;aliss&#39;]

### Return type

[**[AlissNamedSlugItem]**](AlissNamedSlugItem.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAlissCategories

> [AlissNamedSlugItem] getAlissCategories(xMrdScopes)

Retrieve ALISS categories

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.ALISSApi();
let xMrdScopes = "aliss"; // String | MRD service scope required for ALISS endpoints.
apiInstance.getAlissCategories(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for ALISS endpoints. | [default to &#39;aliss&#39;]

### Return type

[**[AlissNamedSlugItem]**](AlissNamedSlugItem.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAlissCommunityGroups

> [AlissNamedSlugItem] getAlissCommunityGroups(xMrdScopes)

Retrieve ALISS community groups

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.ALISSApi();
let xMrdScopes = "aliss"; // String | MRD service scope required for ALISS endpoints.
apiInstance.getAlissCommunityGroups(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for ALISS endpoints. | [default to &#39;aliss&#39;]

### Return type

[**[AlissNamedSlugItem]**](AlissNamedSlugItem.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAlissOrganisations

> [AlissNamedSlugItem] getAlissOrganisations(xMrdScopes)

Retrieve ALISS organisations

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.ALISSApi();
let xMrdScopes = "aliss"; // String | MRD service scope required for ALISS endpoints.
apiInstance.getAlissOrganisations(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for ALISS endpoints. | [default to &#39;aliss&#39;]

### Return type

[**[AlissNamedSlugItem]**](AlissNamedSlugItem.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAlissServiceAreas

> [AlissServiceAreaReference] getAlissServiceAreas(xMrdScopes)

Retrieve ALISS service areas

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.ALISSApi();
let xMrdScopes = "aliss"; // String | MRD service scope required for ALISS endpoints.
apiInstance.getAlissServiceAreas(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for ALISS endpoints. | [default to &#39;aliss&#39;]

### Return type

[**[AlissServiceAreaReference]**](AlissServiceAreaReference.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAlissServicesByIds

> [AlissService] getAlissServicesByIds(xMrdScopes, serviceIds, opts)

Retrieve ALISS services by ID

Retrieves one or more services using a comma-separated list of service IDs.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.ALISSApi();
let xMrdScopes = "aliss"; // String | MRD service scope required for ALISS endpoints.
let serviceIds = "123,456"; // String | One or more comma-separated ALISS service IDs.
let opts = {
  'orderBy': "services.name", // String | Field used to order matching services.
  'order': "ASC", // String | Direction used to order matching services.
  'geojson': false, // Boolean | Controls whether GeoJSON is included with service-area data. The API accepts true or false case-insensitively.
  'format': "JSON" // String | Response format.
};
apiInstance.getAlissServicesByIds(xMrdScopes, serviceIds, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for ALISS endpoints. | [default to &#39;aliss&#39;]
 **serviceIds** | **String**| One or more comma-separated ALISS service IDs. | 
 **orderBy** | **String**| Field used to order matching services. | [optional] [default to &#39;services.id&#39;]
 **order** | **String**| Direction used to order matching services. | [optional] [default to &#39;ASC&#39;]
 **geojson** | **Boolean**| Controls whether GeoJSON is included with service-area data. The API accepts true or false case-insensitively. | [optional] [default to false]
 **format** | **String**| Response format. | [optional] [default to &#39;JSON&#39;]

### Return type

[**[AlissService]**](AlissService.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/xml, application/json


## searchAlissServices

> [AlissService] searchAlissServices(xMrdScopes, opts)

Search ALISS services

Searches ALISS services using structured filters, ordering and keyset pagination.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.ALISSApi();
let xMrdScopes = "aliss"; // String | MRD service scope required for ALISS endpoints.
let opts = {
  'filters': new ApiMrdSdkJavascript.SearchAlissServicesFiltersParameter(), // SearchAlissServicesFiltersParameter | Structured filters used to search ALISS services. Supported datasets are services, organisations, categories, service_areas, locations, accessibility_features and community_groups. Each filter requires field, value and operator. Every filter except the final filter must also contain condition.
  'orderBy': "services.name", // String | Field used to order matching services.
  'order': "ASC", // String | Direction used to order matching services.
  'limit': 20, // Number | Maximum number of services to return. The API defaults to 20 and rejects values greater than 100.
  'after': "123", // String | Keyset pagination value used to retrieve records after the supplied position. Only alphanumeric characters, commas, hyphens, underscores and spaces are accepted.
  'before': "456", // String | Keyset pagination value used to retrieve records before the supplied position. Only alphanumeric characters, commas, hyphens, underscores and spaces are accepted.
  'geojson': false, // Boolean | Controls whether GeoJSON is included with service-area data. The API accepts true or false case-insensitively.
  'format': "JSON" // String | Response format.
};
apiInstance.searchAlissServices(xMrdScopes, opts, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for ALISS endpoints. | [default to &#39;aliss&#39;]
 **filters** | [**SearchAlissServicesFiltersParameter**](.md)| Structured filters used to search ALISS services. Supported datasets are services, organisations, categories, service_areas, locations, accessibility_features and community_groups. Each filter requires field, value and operator. Every filter except the final filter must also contain condition. | [optional] 
 **orderBy** | **String**| Field used to order matching services. | [optional] [default to &#39;services.id&#39;]
 **order** | **String**| Direction used to order matching services. | [optional] [default to &#39;ASC&#39;]
 **limit** | **Number**| Maximum number of services to return. The API defaults to 20 and rejects values greater than 100. | [optional] [default to 20]
 **after** | **String**| Keyset pagination value used to retrieve records after the supplied position. Only alphanumeric characters, commas, hyphens, underscores and spaces are accepted. | [optional] 
 **before** | **String**| Keyset pagination value used to retrieve records before the supplied position. Only alphanumeric characters, commas, hyphens, underscores and spaces are accepted. | [optional] 
 **geojson** | **Boolean**| Controls whether GeoJSON is included with service-area data. The API accepts true or false case-insensitively. | [optional] [default to false]
 **format** | **String**| Response format. | [optional] [default to &#39;JSON&#39;]

### Return type

[**[AlissService]**](AlissService.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/xml, application/json

