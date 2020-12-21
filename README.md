# SwaggerClient-php
No description provided (generated by Swagger Codegen https://github.com/swagger-api/swagger-codegen)

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/ventureleap/leap-one-rating-sdk.git"
    }
  ],
  "require": {
    "ventureleap/leap-one-rating-sdk": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: apiKey
$config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RatingService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->deleteConfigurationEntryItem($id);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->deleteConfigurationEntryItem: ', $e->getMessage(), PHP_EOL;
}

// Configure API key authorization: apiKey
$config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RatingService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$key = "key_example"; // string | 
$sub_key = "sub_key_example"; // string | 
$value = "value_example"; // string | 
$application_id = "application_id_example"; // string | 
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->getConfigurationEntryCollection($key, $sub_key, $value, $application_id, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->getConfigurationEntryCollection: ', $e->getMessage(), PHP_EOL;
}

// Configure API key authorization: apiKey
$config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RatingService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getConfigurationEntryItem($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->getConfigurationEntryItem: ', $e->getMessage(), PHP_EOL;
}

// Configure API key authorization: apiKey
$config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RatingService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \VentureLeap\RatingService\Model\ConfigurationEntryJsonldConfigurationWrite(); // \VentureLeap\RatingService\Model\ConfigurationEntryJsonldConfigurationWrite | The new ConfigurationEntry resource

try {
    $result = $apiInstance->postConfigurationEntryCollection($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->postConfigurationEntryCollection: ', $e->getMessage(), PHP_EOL;
}

// Configure API key authorization: apiKey
$config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RatingService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$body = new \VentureLeap\RatingService\Model\ConfigurationEntryJsonldConfigurationWrite(); // \VentureLeap\RatingService\Model\ConfigurationEntryJsonldConfigurationWrite | The updated ConfigurationEntry resource

try {
    $result = $apiInstance->putConfigurationEntryItem($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->putConfigurationEntryItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

## Documentation for API Endpoints

All URIs are relative to */*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ConfigurationEntryApi* | [**deleteConfigurationEntryItem**](docs/Api/ConfigurationEntryApi.md#deleteconfigurationentryitem) | **DELETE** /rating/configuration_entries/{id} | Removes the ConfigurationEntry resource.
*ConfigurationEntryApi* | [**getConfigurationEntryCollection**](docs/Api/ConfigurationEntryApi.md#getconfigurationentrycollection) | **GET** /rating/configuration_entries | Retrieves the collection of ConfigurationEntry resources.
*ConfigurationEntryApi* | [**getConfigurationEntryItem**](docs/Api/ConfigurationEntryApi.md#getconfigurationentryitem) | **GET** /rating/configuration_entries/{id} | Retrieves a ConfigurationEntry resource.
*ConfigurationEntryApi* | [**postConfigurationEntryCollection**](docs/Api/ConfigurationEntryApi.md#postconfigurationentrycollection) | **POST** /rating/configuration_entries | Creates a ConfigurationEntry resource.
*ConfigurationEntryApi* | [**putConfigurationEntryItem**](docs/Api/ConfigurationEntryApi.md#putconfigurationentryitem) | **PUT** /rating/configuration_entries/{id} | Replaces the ConfigurationEntry resource.
*RatingApi* | [**deleteRatingItem**](docs/Api/RatingApi.md#deleteratingitem) | **DELETE** /rating/ratings/{id} | Removes the Rating resource.
*RatingApi* | [**findAverageRatingRatingItem**](docs/Api/RatingApi.md#findaverageratingratingitem) | **GET** /rating/ratings/{productUuid}/average-rating/ | Retrieves a Rating resource.
*RatingApi* | [**getRatingCollection**](docs/Api/RatingApi.md#getratingcollection) | **GET** /rating/ratings | Retrieves the collection of Rating resources.
*RatingApi* | [**getRatingItem**](docs/Api/RatingApi.md#getratingitem) | **GET** /rating/ratings/{id} | Retrieves a Rating resource.
*RatingApi* | [**postRatingCollection**](docs/Api/RatingApi.md#postratingcollection) | **POST** /rating/ratings | Creates a Rating resource.
*RatingApi* | [**putRatingItem**](docs/Api/RatingApi.md#putratingitem) | **PUT** /rating/ratings/{id} | Replaces the Rating resource.

## Documentation For Models

 - [AverageRating](docs/Model/AverageRating.md)
 - [ConfigurationEntryJsonldConfigurationRead](docs/Model/ConfigurationEntryJsonldConfigurationRead.md)
 - [ConfigurationEntryJsonldConfigurationWrite](docs/Model/ConfigurationEntryJsonldConfigurationWrite.md)
 - [InlineResponse200](docs/Model/InlineResponse200.md)
 - [InlineResponse2001](docs/Model/InlineResponse2001.md)
 - [InlineResponse200Hydrasearch](docs/Model/InlineResponse200Hydrasearch.md)
 - [InlineResponse200HydrasearchHydramapping](docs/Model/InlineResponse200HydrasearchHydramapping.md)
 - [InlineResponse200Hydraview](docs/Model/InlineResponse200Hydraview.md)
 - [RatingJsonldRatingRead](docs/Model/RatingJsonldRatingRead.md)
 - [RatingJsonldRatingWrite](docs/Model/RatingJsonldRatingWrite.md)

## Documentation For Authorization


## apiKey

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


## Author


