# nanonets.OCRTrainApi

All URIs are relative to *https://app.nanonet.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**o_cr_model_train_by_model_id_post**](OCRTrainApi.md#o_cr_model_train_by_model_id_post) | **POST** /OCR/Model/{model_id}/Train/ | Train Model

# **o_cr_model_train_by_model_id_post**
> o_cr_model_train_by_model_id_post(model_id)

Train Model

You can use this endpoint to train a model after uploading images for each category. You can use the same endpoint to retrain a model after uploading more images to improve the model.

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
api_instance = nanonets.OCRTrainApi(nanonets.ApiClient(configuration))
model_id = 'model_id_example' # str | 

try:
    # Train Model
    api_instance.o_cr_model_train_by_model_id_post(model_id)
except ApiException as e:
    print("Exception when calling OCRTrainApi->o_cr_model_train_by_model_id_post: %s\n" % e)
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

