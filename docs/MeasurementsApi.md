# ApiMrdSdkJavascript.MeasurementsApi

All URIs are relative to *https://api-mrd.mydex.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getActivityType**](MeasurementsApi.md#getActivityType) | **GET** /measurements/activity-type/{id} | Retrieve an activity type by ID
[**getActivityTypes**](MeasurementsApi.md#getActivityTypes) | **GET** /measurements/activity-type | Retrieve all activity types
[**getBloodPressureMeasurement**](MeasurementsApi.md#getBloodPressureMeasurement) | **GET** /measurements/blood-pressure-measurement/{id} | Retrieve a blood pressure measurement type by ID
[**getBloodPressureMeasurements**](MeasurementsApi.md#getBloodPressureMeasurements) | **GET** /measurements/blood-pressure-measurement | Retrieve all blood pressure measurement types
[**getBloodSpecimenSource**](MeasurementsApi.md#getBloodSpecimenSource) | **GET** /measurements/blood-specimen-source/{id} | Retrieve a blood specimen source by ID
[**getBloodSpecimenSources**](MeasurementsApi.md#getBloodSpecimenSources) | **GET** /measurements/blood-specimen-source | Retrieve all blood specimen sources
[**getBodyPosition**](MeasurementsApi.md#getBodyPosition) | **GET** /measurements/body-position/{id} | Retrieve a body position by ID
[**getBodyPositions**](MeasurementsApi.md#getBodyPositions) | **GET** /measurements/body-position | Retrieve all body positions
[**getBodyTemperatureLocation**](MeasurementsApi.md#getBodyTemperatureLocation) | **GET** /measurements/body-temperature-location/{id} | Retrieve a body temperature location by ID
[**getBodyTemperatureLocations**](MeasurementsApi.md#getBodyTemperatureLocations) | **GET** /measurements/body-temperature-location | Retrieve all body temperature locations
[**getCervicalDilation**](MeasurementsApi.md#getCervicalDilation) | **GET** /measurements/cervical-dilation/{id} | Retrieve a cervical dilation by ID
[**getCervicalDilations**](MeasurementsApi.md#getCervicalDilations) | **GET** /measurements/cervical-dilation | Retrieve all cervical dilations
[**getCervicalFirmness**](MeasurementsApi.md#getCervicalFirmness) | **GET** /measurements/cervical-firmness/{id} | Retrieve a cervical firmness value by ID
[**getCervicalFirmnessValues**](MeasurementsApi.md#getCervicalFirmnessValues) | **GET** /measurements/cervical-firmness | Retrieve all cervical firmness values
[**getCervicalMucusAmount**](MeasurementsApi.md#getCervicalMucusAmount) | **GET** /measurements/cervical-mucus-amount/{id} | Retrieve a cervical mucus amount by ID
[**getCervicalMucusAmounts**](MeasurementsApi.md#getCervicalMucusAmounts) | **GET** /measurements/cervical-mucus-amount | Retrieve all cervical mucus amounts
[**getCervicalMucusTexture**](MeasurementsApi.md#getCervicalMucusTexture) | **GET** /measurements/cervical-mucus-texture/{id} | Retrieve a cervical mucus texture by ID
[**getCervicalMucusTextures**](MeasurementsApi.md#getCervicalMucusTextures) | **GET** /measurements/cervical-mucus-texture | Retrieve all cervical mucus textures
[**getCervicalPosition**](MeasurementsApi.md#getCervicalPosition) | **GET** /measurements/cervical-position/{id} | Retrieve a cervical position by ID
[**getCervicalPositions**](MeasurementsApi.md#getCervicalPositions) | **GET** /measurements/cervical-position | Retrieve all cervical positions
[**getExerciseTypeByName**](MeasurementsApi.md#getExerciseTypeByName) | **GET** /measurements/exercise-type/{exercise_type_name} | Retrieve an exercise type by name
[**getExerciseTypes**](MeasurementsApi.md#getExerciseTypes) | **GET** /measurements/exercise-type | Retrieve all exercise types
[**getMealType**](MeasurementsApi.md#getMealType) | **GET** /measurements/meal-type/{id} | Retrieve a meal type by ID
[**getMealTypes**](MeasurementsApi.md#getMealTypes) | **GET** /measurements/meal-type | Retrieve all meal types
[**getMeasurementGroup**](MeasurementsApi.md#getMeasurementGroup) | **GET** /measurements/groups/{id} | Retrieve a measurement group by ID
[**getMeasurementGroups**](MeasurementsApi.md#getMeasurementGroups) | **GET** /measurements/groups | Retrieve all measurement groups
[**getMeasurementType**](MeasurementsApi.md#getMeasurementType) | **GET** /measurements/types/{id} | Retrieve a measurement type by ID
[**getMeasurementTypes**](MeasurementsApi.md#getMeasurementTypes) | **GET** /measurements/types | Retrieve all measurement types
[**getMeasurementUnit**](MeasurementsApi.md#getMeasurementUnit) | **GET** /measurements/units/{id} | Retrieve a unit of measure by ID
[**getMeasurementUnits**](MeasurementsApi.md#getMeasurementUnits) | **GET** /measurements/units | Retrieve all units of measure
[**getResistanceType**](MeasurementsApi.md#getResistanceType) | **GET** /measurements/resistance-type/{id} | Retrieve a resistance type by ID
[**getResistanceTypes**](MeasurementsApi.md#getResistanceTypes) | **GET** /measurements/resistance-type | Retrieve all resistance types
[**getSleepSegmentType**](MeasurementsApi.md#getSleepSegmentType) | **GET** /measurements/sleep-segment-type/{id} | Retrieve a sleep segment type by ID
[**getSleepSegmentTypes**](MeasurementsApi.md#getSleepSegmentTypes) | **GET** /measurements/sleep-segment-type | Retrieve all sleep segment types
[**getTemporalRelationToMeal**](MeasurementsApi.md#getTemporalRelationToMeal) | **GET** /measurements/temporal-relation-to-meal/{id} | Retrieve a temporal relation to meals by ID
[**getTemporalRelationToSleep**](MeasurementsApi.md#getTemporalRelationToSleep) | **GET** /measurements/temporal-relation-to-sleep/{id} | Retrieve a temporal relation to sleep by ID
[**getTemporalRelationsToMeal**](MeasurementsApi.md#getTemporalRelationsToMeal) | **GET** /measurements/temporal-relation-to-meal | Retrieve all temporal relations to meals
[**getTemporalRelationsToSleep**](MeasurementsApi.md#getTemporalRelationsToSleep) | **GET** /measurements/temporal-relation-to-sleep | Retrieve all temporal relations to sleep



## getActivityType

> MeasurementActivityTypeResult getActivityType(xMrdScopes, id)

Retrieve an activity type by ID

Returns the activity type matching the supplied activity_type_id.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getActivityType(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementActivityTypeResult**](MeasurementActivityTypeResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getActivityTypes

> MeasurementActivityTypesResult getActivityTypes(xMrdScopes)

Retrieve all activity types

Returns activity types including the database record ID, activity type ID and description.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getActivityTypes(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementActivityTypesResult**](MeasurementActivityTypesResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getBloodPressureMeasurement

> MeasurementBloodPressureMeasurementResult getBloodPressureMeasurement(xMrdScopes, id)

Retrieve a blood pressure measurement type by ID

Returns the blood pressure measurement type matching the supplied blood_pressure_measurement_id.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getBloodPressureMeasurement(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementBloodPressureMeasurementResult**](MeasurementBloodPressureMeasurementResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getBloodPressureMeasurements

> MeasurementBloodPressureMeasurementsResult getBloodPressureMeasurements(xMrdScopes)

Retrieve all blood pressure measurement types

Returns blood pressure measurement types including the database record ID, blood pressure measurement ID and description.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getBloodPressureMeasurements(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementBloodPressureMeasurementsResult**](MeasurementBloodPressureMeasurementsResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getBloodSpecimenSource

> MeasurementBloodSpecimenSourceResult getBloodSpecimenSource(xMrdScopes, id)

Retrieve a blood specimen source by ID

Returns the blood specimen source matching the supplied blood_specimen_source_id.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getBloodSpecimenSource(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementBloodSpecimenSourceResult**](MeasurementBloodSpecimenSourceResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getBloodSpecimenSources

> MeasurementBloodSpecimenSourcesResult getBloodSpecimenSources(xMrdScopes)

Retrieve all blood specimen sources

Returns blood specimen sources including the database record ID, blood specimen source ID and description.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getBloodSpecimenSources(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementBloodSpecimenSourcesResult**](MeasurementBloodSpecimenSourcesResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getBodyPosition

> MeasurementBodyPositionResult getBodyPosition(xMrdScopes, id)

Retrieve a body position by ID

Returns the body position matching the supplied body_position_id.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getBodyPosition(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementBodyPositionResult**](MeasurementBodyPositionResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getBodyPositions

> MeasurementBodyPositionsResult getBodyPositions(xMrdScopes)

Retrieve all body positions

Returns body positions including the database record ID, body position ID and description.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getBodyPositions(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementBodyPositionsResult**](MeasurementBodyPositionsResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getBodyTemperatureLocation

> MeasurementBodyTemperatureLocationResult getBodyTemperatureLocation(xMrdScopes, id)

Retrieve a body temperature location by ID

Returns the body temperature location matching the supplied body_temperature_location_id.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getBodyTemperatureLocation(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementBodyTemperatureLocationResult**](MeasurementBodyTemperatureLocationResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getBodyTemperatureLocations

> MeasurementBodyTemperatureLocationsResult getBodyTemperatureLocations(xMrdScopes)

Retrieve all body temperature locations

Returns body temperature locations including the database record ID, body temperature location ID and description.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getBodyTemperatureLocations(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementBodyTemperatureLocationsResult**](MeasurementBodyTemperatureLocationsResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getCervicalDilation

> MeasurementCervicalDilationResult getCervicalDilation(xMrdScopes, id)

Retrieve a cervical dilation by ID

Returns the cervical dilation matching the supplied cervical_dilation_id.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getCervicalDilation(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementCervicalDilationResult**](MeasurementCervicalDilationResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getCervicalDilations

> MeasurementCervicalDilationsResult getCervicalDilations(xMrdScopes)

Retrieve all cervical dilations

Returns cervical dilations including the database record ID, cervical dilation ID and description.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getCervicalDilations(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementCervicalDilationsResult**](MeasurementCervicalDilationsResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getCervicalFirmness

> MeasurementCervicalFirmnessResult getCervicalFirmness(xMrdScopes, id)

Retrieve a cervical firmness value by ID

Returns the cervical firmness value matching the supplied cervical_firmness_id.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getCervicalFirmness(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementCervicalFirmnessResult**](MeasurementCervicalFirmnessResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getCervicalFirmnessValues

> MeasurementCervicalFirmnessValuesResult getCervicalFirmnessValues(xMrdScopes)

Retrieve all cervical firmness values

Returns cervical firmness values including the database record ID, cervical firmness ID and description.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getCervicalFirmnessValues(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementCervicalFirmnessValuesResult**](MeasurementCervicalFirmnessValuesResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getCervicalMucusAmount

> MeasurementCervicalMucusAmountResult getCervicalMucusAmount(xMrdScopes, id)

Retrieve a cervical mucus amount by ID

Returns the cervical mucus amount matching the supplied cervical_mucus_amount_id.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getCervicalMucusAmount(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementCervicalMucusAmountResult**](MeasurementCervicalMucusAmountResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getCervicalMucusAmounts

> MeasurementCervicalMucusAmountsResult getCervicalMucusAmounts(xMrdScopes)

Retrieve all cervical mucus amounts

Returns cervical mucus amounts including the database record ID, cervical mucus amount ID and description.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getCervicalMucusAmounts(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementCervicalMucusAmountsResult**](MeasurementCervicalMucusAmountsResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getCervicalMucusTexture

> MeasurementCervicalMucusTextureResult getCervicalMucusTexture(xMrdScopes, id)

Retrieve a cervical mucus texture by ID

Returns the cervical mucus texture matching the supplied cervical_mucus_texture_id.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getCervicalMucusTexture(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementCervicalMucusTextureResult**](MeasurementCervicalMucusTextureResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getCervicalMucusTextures

> MeasurementCervicalMucusTexturesResult getCervicalMucusTextures(xMrdScopes)

Retrieve all cervical mucus textures

Returns cervical mucus textures including the database record ID, cervical mucus texture ID and description.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getCervicalMucusTextures(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementCervicalMucusTexturesResult**](MeasurementCervicalMucusTexturesResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getCervicalPosition

> MeasurementCervicalPositionResult getCervicalPosition(xMrdScopes, id)

Retrieve a cervical position by ID

Returns the cervical position matching the supplied cervical_position_id.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getCervicalPosition(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementCervicalPositionResult**](MeasurementCervicalPositionResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getCervicalPositions

> MeasurementCervicalPositionsResult getCervicalPositions(xMrdScopes)

Retrieve all cervical positions

Returns cervical positions including the database record ID, cervical position ID and description.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getCervicalPositions(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementCervicalPositionsResult**](MeasurementCervicalPositionsResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getExerciseTypeByName

> MeasurementExerciseTypeResult getExerciseTypeByName(xMrdScopes, exerciseTypeName)

Retrieve an exercise type by name

Returns the exercise type matching the supplied exercise_type_name.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let exerciseTypeName = "Running"; // String | Exercise type name used to retrieve a specific exercise-type record.
apiInstance.getExerciseTypeByName(xMrdScopes, exerciseTypeName, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **exerciseTypeName** | **String**| Exercise type name used to retrieve a specific exercise-type record. | 

### Return type

[**MeasurementExerciseTypeResult**](MeasurementExerciseTypeResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getExerciseTypes

> MeasurementExerciseTypesResult getExerciseTypes(xMrdScopes)

Retrieve all exercise types

Returns exercise types including the database record ID, exercise type name and description.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getExerciseTypes(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementExerciseTypesResult**](MeasurementExerciseTypesResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getMealType

> MeasurementMealTypeResult getMealType(xMrdScopes, id)

Retrieve a meal type by ID

Returns the meal type matching the supplied meal_type_id.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getMealType(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementMealTypeResult**](MeasurementMealTypeResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getMealTypes

> MeasurementMealTypesResult getMealTypes(xMrdScopes)

Retrieve all meal types

Returns meal types including the database record ID, meal type ID and description.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getMealTypes(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementMealTypesResult**](MeasurementMealTypesResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getMeasurementGroup

> MeasurementGroupResult getMeasurementGroup(xMrdScopes, id)

Retrieve a measurement group by ID

Returns the measurement group matching the supplied database record ID.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getMeasurementGroup(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementGroupResult**](MeasurementGroupResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getMeasurementGroups

> MeasurementGroupsResult getMeasurementGroups(xMrdScopes)

Retrieve all measurement groups

Returns the available measurement groups and their definitions.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getMeasurementGroups(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementGroupsResult**](MeasurementGroupsResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getMeasurementType

> MeasurementTypeResult getMeasurementType(xMrdScopes, id)

Retrieve a measurement type by ID

Returns the measurement definition matching the supplied measurement ID.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getMeasurementType(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementTypeResult**](MeasurementTypeResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getMeasurementTypes

> MeasurementTypesResult getMeasurementTypes(xMrdScopes)

Retrieve all measurement types

Returns measurement definitions including the measurement name, group and unit.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getMeasurementTypes(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementTypesResult**](MeasurementTypesResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getMeasurementUnit

> MeasurementUnitResult getMeasurementUnit(xMrdScopes, id)

Retrieve a unit of measure by ID

Returns the unit of measure matching the supplied database record ID.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getMeasurementUnit(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementUnitResult**](MeasurementUnitResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getMeasurementUnits

> MeasurementUnitsResult getMeasurementUnits(xMrdScopes)

Retrieve all units of measure

Returns available measurement units and their definitions.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getMeasurementUnits(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementUnitsResult**](MeasurementUnitsResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getResistanceType

> MeasurementResistanceTypeResult getResistanceType(xMrdScopes, id)

Retrieve a resistance type by ID

Returns the resistance type matching the supplied resistance_type_id.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getResistanceType(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementResistanceTypeResult**](MeasurementResistanceTypeResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getResistanceTypes

> MeasurementResistanceTypesResult getResistanceTypes(xMrdScopes)

Retrieve all resistance types

Returns resistance types including the database record ID, resistance type ID and description.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getResistanceTypes(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementResistanceTypesResult**](MeasurementResistanceTypesResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getSleepSegmentType

> MeasurementSleepSegmentTypeResult getSleepSegmentType(xMrdScopes, id)

Retrieve a sleep segment type by ID

Returns the sleep segment type matching the supplied sleep_segment_type_id.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getSleepSegmentType(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementSleepSegmentTypeResult**](MeasurementSleepSegmentTypeResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getSleepSegmentTypes

> MeasurementSleepSegmentTypesResult getSleepSegmentTypes(xMrdScopes)

Retrieve all sleep segment types

Returns sleep segment types including the database record ID, sleep segment type ID and description.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getSleepSegmentTypes(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementSleepSegmentTypesResult**](MeasurementSleepSegmentTypesResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTemporalRelationToMeal

> MeasurementTemporalRelationToMealResult getTemporalRelationToMeal(xMrdScopes, id)

Retrieve a temporal relation to meals by ID

Returns the temporal relation to meal matching the supplied temporal_relation_to_meal_id.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getTemporalRelationToMeal(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementTemporalRelationToMealResult**](MeasurementTemporalRelationToMealResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTemporalRelationToSleep

> MeasurementTemporalRelationToSleepResult getTemporalRelationToSleep(xMrdScopes, id)

Retrieve a temporal relation to sleep by ID

Returns the temporal relation to sleep matching the supplied temporal_relation_to_sleep_id.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
let id = 1; // Number | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.
apiInstance.getTemporalRelationToSleep(xMrdScopes, id, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]
 **id** | **Number**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | 

### Return type

[**MeasurementTemporalRelationToSleepResult**](MeasurementTemporalRelationToSleepResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTemporalRelationsToMeal

> MeasurementTemporalRelationsToMealResult getTemporalRelationsToMeal(xMrdScopes)

Retrieve all temporal relations to meals

Returns temporal relations to meals including the database record ID, relation ID and description.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getTemporalRelationsToMeal(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementTemporalRelationsToMealResult**](MeasurementTemporalRelationsToMealResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTemporalRelationsToSleep

> MeasurementTemporalRelationsToSleepResult getTemporalRelationsToSleep(xMrdScopes)

Retrieve all temporal relations to sleep

Returns temporal relations to sleep including the database record ID, relation ID and description.

### Example

```javascript
import ApiMrdSdkJavascript from 'api-mrd-sdk-javascript';
let defaultClient = ApiMrdSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiMrdSdkJavascript.MeasurementsApi();
let xMrdScopes = "measurements"; // String | MRD service scope required for Measurements endpoints.
apiInstance.getTemporalRelationsToSleep(xMrdScopes, (error, data, response) => {
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
 **xMrdScopes** | **String**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;]

### Return type

[**MeasurementTemporalRelationsToSleepResult**](MeasurementTemporalRelationsToSleepResult.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

