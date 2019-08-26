# nanonets.ObjectModelApi

All URIs are relative to *https://app.nanonet.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**object_detection_model_by_model_id_get**](ObjectModelApi.md#object_detection_model_by_model_id_get) | **GET** /ObjectDetection/Model/{model_id} | Get Model by Id
[**object_detection_model_post**](ObjectModelApi.md#object_detection_model_post) | **POST** /ObjectDetection/Model/ | Create New Model
[**object_detection_models_get**](ObjectModelApi.md#object_detection_models_get) | **GET** /OCR/Model/ | Get All Models
[**object_detection_models_get_0**](ObjectModelApi.md#object_detection_models_get_0) | **GET** /ObjectDetection/Models/ | Get All Models

# **object_detection_model_by_model_id_get**
> object_detection_model_by_model_id_get(model_id)

Get Model by Id

This endpoint retrieves a specific model's details given it's id.

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
api_instance = nanonets.ObjectModelApi(nanonets.ApiClient(configuration))
model_id = 'model_id_example' # str | 

try:
    # Get Model by Id
    api_instance.object_detection_model_by_model_id_get(model_id)
except ApiException as e:
    print("Exception when calling ObjectModelApi->object_detection_model_by_model_id_get: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_id** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **object_detection_model_post**
> object_detection_model_post(body, content_type)

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
api_instance = nanonets.ObjectModelApi(nanonets.ApiClient(configuration))
body = nanonets.CreateNewModelrequest() # CreateNewModelrequest | 
content_type = 'content_type_example' # str | 

try:
    # Create New Model
    api_instance.object_detection_model_post(body, content_type)
except ApiException as e:
    print("Exception when calling ObjectModelApi->object_detection_model_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**CreateNewModelrequest**](CreateNewModelrequest.md)|  | 
 **content_type** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **object_detection_models_get**
> object_detection_models_get()

Get All Models

This endpoint returns information of all models created by user.

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
api_instance = nanonets.ObjectModelApi(nanonets.ApiClient(configuration))

try:
    # Get All Models
    api_instance.object_detection_models_get()
except ApiException as e:
    print("Exception when calling ObjectModelApi->object_detection_models_get: %s\n" % e)
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

# **object_detection_models_get_0**
> object_detection_models_get_0()

Get All Models

This endpoint returns information of all models created by user.

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
api_instance = nanonets.ObjectModelApi(nanonets.ApiClient(configuration))

try:
    # Get All Models
    api_instance.object_detection_models_get_0()
except ApiException as e:
    print("Exception when calling ObjectModelApi->object_detection_models_get_0: %s\n" % e)
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

