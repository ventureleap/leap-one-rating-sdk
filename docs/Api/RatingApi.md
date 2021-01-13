# VentureLeap\RatingService\RatingApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteRatingItem**](RatingApi.md#deleteratingitem) | **DELETE** /rating/ratings/{id} | Removes the Rating resource.
[**findAverageRatingRatingItem**](RatingApi.md#findaverageratingratingitem) | **GET** /rating/ratings/{productUuid}/average-rating/ | Retrieves a Rating resource.
[**getRatingCollection**](RatingApi.md#getratingcollection) | **GET** /rating/ratings | Retrieves the collection of Rating resources.
[**getRatingItem**](RatingApi.md#getratingitem) | **GET** /rating/ratings/{id} | Retrieves a Rating resource.
[**postRatingCollection**](RatingApi.md#postratingcollection) | **POST** /rating/ratings | Creates a Rating resource.
[**putRatingItem**](RatingApi.md#putratingitem) | **PUT** /rating/ratings/{id} | Replaces the Rating resource.

# **deleteRatingItem**
> deleteRatingItem($id)

Removes the Rating resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RatingService\Api\RatingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->deleteRatingItem($id);
} catch (Exception $e) {
    echo 'Exception when calling RatingApi->deleteRatingItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

void (empty response body)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findAverageRatingRatingItem**
> \VentureLeap\RatingService\Model\AverageRating findAverageRatingRatingItem($product_uuid)

Retrieves a Rating resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RatingService\Api\RatingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_uuid = "product_uuid_example"; // string | 

try {
    $result = $apiInstance->findAverageRatingRatingItem($product_uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RatingApi->findAverageRatingRatingItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_uuid** | **string**|  |

### Return type

[**\VentureLeap\RatingService\Model\AverageRating**](../Model/AverageRating.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRatingCollection**
> \VentureLeap\RatingService\Model\InlineResponse2001 getRatingCollection($product_uuid, $exists_review, $custom_data, $page)

Retrieves the collection of Rating resources.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RatingService\Api\RatingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_uuid = "product_uuid_example"; // string | 
$exists_review = true; // bool | 
$custom_data = "custom_data_example"; // string | 
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->getRatingCollection($product_uuid, $exists_review, $custom_data, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RatingApi->getRatingCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_uuid** | **string**|  | [optional]
 **exists_review** | **bool**|  | [optional]
 **custom_data** | **string**|  | [optional]
 **page** | **int**| The collection page number | [optional] [default to 1]

### Return type

[**\VentureLeap\RatingService\Model\InlineResponse2001**](../Model/InlineResponse2001.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRatingItem**
> \VentureLeap\RatingService\Model\RatingJsonldRatingRead getRatingItem($id)

Retrieves a Rating resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RatingService\Api\RatingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getRatingItem($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RatingApi->getRatingItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\VentureLeap\RatingService\Model\RatingJsonldRatingRead**](../Model/RatingJsonldRatingRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postRatingCollection**
> \VentureLeap\RatingService\Model\RatingJsonldRatingRead postRatingCollection($body)

Creates a Rating resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RatingService\Api\RatingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \VentureLeap\RatingService\Model\RatingJsonldRatingWrite(); // \VentureLeap\RatingService\Model\RatingJsonldRatingWrite | The new Rating resource

try {
    $result = $apiInstance->postRatingCollection($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RatingApi->postRatingCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\RatingService\Model\RatingJsonldRatingWrite**](../Model/RatingJsonldRatingWrite.md)| The new Rating resource | [optional]

### Return type

[**\VentureLeap\RatingService\Model\RatingJsonldRatingRead**](../Model/RatingJsonldRatingRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putRatingItem**
> \VentureLeap\RatingService\Model\RatingJsonldRatingRead putRatingItem($id, $body)

Replaces the Rating resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RatingService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RatingService\Api\RatingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$body = new \VentureLeap\RatingService\Model\RatingJsonldRatingWrite(); // \VentureLeap\RatingService\Model\RatingJsonldRatingWrite | The updated Rating resource

try {
    $result = $apiInstance->putRatingItem($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RatingApi->putRatingItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **body** | [**\VentureLeap\RatingService\Model\RatingJsonldRatingWrite**](../Model/RatingJsonldRatingWrite.md)| The updated Rating resource | [optional]

### Return type

[**\VentureLeap\RatingService\Model\RatingJsonldRatingRead**](../Model/RatingJsonldRatingRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

