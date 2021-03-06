# nanonets.MultiLabelClassificationModelApi

All URIs are relative to *https://app.nanonet.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**multi_label_classification_by_model_id_get**](MultiLabelClassificationModelApi.md#multi_label_classification_by_model_id_get) | **GET** /MultiLabelClassification/Model/{model_id} | Get Model by Id
[**multi_label_image_classification_post**](MultiLabelClassificationModelApi.md#multi_label_image_classification_post) | **POST** /MultiLabelClassification/Model/ | Create New Model

# **multi_label_classification_by_model_id_get**
> multi_label_classification_by_model_id_get(model_id)

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
api_instance = nanonets.MultiLabelClassificationModelApi(nanonets.ApiClient(configuration))
model_id = 'model_id_example' # str | 

try:
    # Get Model by Id
    api_instance.multi_label_classification_by_model_id_get(model_id)
except ApiException as e:
    print("Exception when calling MultiLabelClassificationModelApi->multi_label_classification_by_model_id_get: %s\n" % e)
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

# **multi_label_image_classification_post**
> multi_label_image_classification_post(body, content_type)

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
api_instance = nanonets.MultiLabelClassificationModelApi(nanonets.ApiClient(configuration))
body = nanonets.CreateNewModelrequest() # CreateNewModelrequest | 
content_type = 'content_type_example' # str | 

try:
    # Create New Model
    api_instance.multi_label_image_classification_post(body, content_type)
except ApiException as e:
    print("Exception when calling MultiLabelClassificationModelApi->multi_label_image_classification_post: %s\n" % e)
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

