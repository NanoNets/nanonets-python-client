# nanonets.ImageTrainApi

All URIs are relative to *https://app.nanonet.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**image_categorization_train_post**](ImageTrainApi.md#image_categorization_train_post) | **POST** /ImageCategorization/Train/ | Train Model

# **image_categorization_train_post**
> image_categorization_train_post(model_id)

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
api_instance = nanonets.ImageTrainApi(nanonets.ApiClient(configuration))
model_id = 'model_id_example' # str | 

try:
    # Train Model
    api_instance.image_categorization_train_post(model_id)
except ApiException as e:
    print("Exception when calling ImageTrainApi->image_categorization_train_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_id** | [**str**](.md)|  | 

### Return type

void (empty response body)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

