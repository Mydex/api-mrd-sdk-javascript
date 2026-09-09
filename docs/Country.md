# ApiMrdSdkJavascript.Country

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | [**CountryName**](CountryName.md) |  | 
**cca2** | **String** |  | 
**cca3** | **String** |  | 
**ccn3** | **String** |  | 
**independent** | **Number** | Whether the country is independent. The current database response serializes this as 0 or 1. | 
**status** | **String** |  | 
**unMember** | **Number** | Whether the country is a United Nations member. The current database response serializes this as 0 or 1. | 
**capital** | **[String]** |  | 
**altSpellings** | **[String]** |  | 
**region** | **String** |  | 
**subregion** | **String** |  | 
**languages** | **{String: String}** | Language codes mapped to language names. | 
**landlocked** | **Number** | Whether the country is landlocked. The current database response serializes this as 0 or 1. | 
**area** | **Number** |  | 
**demonyms** | [**{String: CountryDemonym}**](CountryDemonym.md) |  | 
**translations** | [**{String: CountryTranslation}**](CountryTranslation.md) |  | 
**flag** | **String** |  | 
**maps** | [**CountryMaps**](CountryMaps.md) |  | 
**population** | **Number** |  | 
**gini** | **{String: Number}** | Gini coefficient values keyed by year. Countries without Gini data return an empty object. | 
**fifa** | **String** | FIFA country code. The source may also return an empty string. | 
**car** | [**CountryCar**](CountryCar.md) |  | 
**timezones** | **[String]** |  | 
**continents** | **[String]** |  | 
**flags** | [**CountryFlags**](CountryFlags.md) |  | 
**coatOfArms** | [**CountryCoatOfArms**](CountryCoatOfArms.md) |  | 
**startOfWeek** | **String** |  | 
**capitalInfo** | [**CountryCapitalInfo**](CountryCapitalInfo.md) |  | 
**postalCode** | [**CountryPostalCode**](CountryPostalCode.md) |  | 
**currencies** | [**{String: CountryCurrency}**](CountryCurrency.md) |  | 
**idd** | [**CountryIdd**](CountryIdd.md) |  | 



## Enum: IndependentEnum


* `0` (value: `0`)

* `1` (value: `1`)

* `unknown_default_open_api` (value: `11184809`)





## Enum: UnMemberEnum


* `0` (value: `0`)

* `1` (value: `1`)

* `unknown_default_open_api` (value: `11184809`)





## Enum: LandlockedEnum


* `0` (value: `0`)

* `1` (value: `1`)

* `unknown_default_open_api` (value: `11184809`)




