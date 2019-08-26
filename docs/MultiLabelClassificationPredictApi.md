# nanonets.MultiLabelClassificationPredictApi

All URIs are relative to *https://app.nanonet.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**multi_label_classification_label_files_post**](MultiLabelClassificationPredictApi.md#multi_label_classification_label_files_post) | **POST** /MultiLabelClassification/Model/{model_id}/LabelFiles/ | Prediction for image File
[**multi_label_classification_post**](MultiLabelClassificationPredictApi.md#multi_label_classification_post) | **POST** /MultiLabelClassification/Model/{model_id}/LabelUrls/ | Prediction for image URLs

# **multi_label_classification_label_files_post**
> multi_label_classification_label_files_post(files, model_id)

Prediction for image File

Use the model to predict which one of the categories an image (given an image file) belongs to. You can specify multiple image files.

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
api_instance = nanonets.MultiLabelClassificationPredictApi(nanonets.ApiClient(configuration))
files = 'files_example' # file | 
model_id = 'model_id_example' # str | 

try:
    # Prediction for image File
    api_instance.multi_label_classification_label_files_post(files, model_id)
except ApiException as e:
    print("Exception when calling MultiLabelClassificationPredictApi->multi_label_classification_label_files_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **files** | **file**|  | 
 **model_id** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **multi_label_classification_post**
> multi_label_classification_post(urls, model_id)

Prediction for image URLs

Use the model to predict what all categories an image (given the image url) belongs to. You can specify multiple image urls.

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
api_instance = nanonets.MultiLabelClassificationPredictApi(nanonets.ApiClient(configuration))
urls = 'urls_example' # str | 
model_id = 'model_id_example' # str | 

try:
    # Prediction for image URLs
    api_instance.multi_label_classification_post(urls, model_id)
except ApiException as e:
    print("Exception when calling MultiLabelClassificationPredictApi->multi_label_classification_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **urls** | [**str**](.md)|  | 
 **model_id** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

