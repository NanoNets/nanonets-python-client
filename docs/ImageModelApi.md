# nanonets.ImageModelApi

All URIs are relative to *https://app.nanonet.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**image_categorization_model_get**](ImageModelApi.md#image_categorization_model_get) | **GET** /ImageCategorization/Model | Get Model by Id
[**image_categorization_model_post**](ImageModelApi.md#image_categorization_model_post) | **POST** /ImageCategorization/Model/ | Create New Model
[**image_categorization_models_get**](ImageModelApi.md#image_categorization_models_get) | **GET** /ImageCategorization/Models/ | Get All Models

# **image_categorization_model_get**
> image_categorization_model_get(id)

Get Model by Id

This endpoint retrieves a specific model's details given it's id

### Example
```python
from __future__ import print_function
import time
import nanonets
from nanonets.rest import ApiException
from pprint import pprint
# Configure HTTP basic authorization: ApiKey
configuration = nanonets.Configuration()
configuration.username = 'YOUR_USERNAME'
configuration.password = 'YOUR_PASSWORD'

# create an instance of the API class
api_instance = nanonets.ImageModelApi(nanonets.ApiClient(configuration))
id = 'id_example' # str | 

try:
    # Get Model by Id
    api_instance.image_categorization_model_get(id)
except ApiException as e:
    print("Exception when calling ImageModelApi->image_categorization_model_get: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **image_categorization_model_post**
> image_categorization_model_post(categories)

Create New Model

You can create a new model using this endpoint. A successful API call will return the json structure of the newly created model. You can then use the model's id to upload images for each category and then retrain the model.

### Example
```python
from __future__ import print_function
import time
import nanonets
from nanonets.rest import ApiException
from pprint import pprint
# Configure HTTP basic authorization: ApiKey
configuration = nanonets.Configuration()
configuration.username = 'YOUR_USERNAME'
configuration.password = 'YOUR_PASSWORD'

# create an instance of the API class
api_instance = nanonets.ImageModelApi(nanonets.ApiClient(configuration))
categories = 'categories_example' # str | 

try:
    # Create New Model
    api_instance.image_categorization_model_post(categories)
except ApiException as e:
    print("Exception when calling ImageModelApi->image_categorization_model_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **categories** | [**str**](.md)|  | 

### Return type

void (empty response body)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **image_categorization_models_get**
> image_categorization_models_get()

Get All Models

This endpoint returns information of all models created by user

### Example
```python
from __future__ import print_function
import time
import nanonets
from nanonets.rest import ApiException
from pprint import pprint
# Configure HTTP basic authorization: ApiKey
configuration = nanonets.Configuration()
configuration.username = 'YOUR_USERNAME'
configuration.password = 'YOUR_PASSWORD'

# create an instance of the API class
api_instance = nanonets.ImageModelApi(nanonets.ApiClient(configuration))

try:
    # Get All Models
    api_instance.image_categorization_models_get()
except ApiException as e:
    print("Exception when calling ImageModelApi->image_categorization_models_get: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

