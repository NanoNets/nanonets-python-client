# nanonets.OCRPredictApi

All URIs are relative to *https://app.nanonet.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**o_cr_model_label_file_by_model_id_post**](OCRPredictApi.md#o_cr_model_label_file_by_model_id_post) | **POST** /OCR/Model/{model_id}/LabelFile/ | Prediction for image file
[**o_cr_model_label_urls_by_model_id_post**](OCRPredictApi.md#o_cr_model_label_urls_by_model_id_post) | **POST** /OCR/Model/{model_id}/LabelUrls/ | Prediction for image url

# **o_cr_model_label_file_by_model_id_post**
> o_cr_model_label_file_by_model_id_post(file, model_id)

Prediction for image file

Use the model to predict which one of the categories an image (given an image file) belongs to.

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
api_instance = nanonets.OCRPredictApi(nanonets.ApiClient(configuration))
file = 'file_example' # file | 
model_id = 'model_id_example' # str | 

try:
    # Prediction for image file
    api_instance.o_cr_model_label_file_by_model_id_post(file, model_id)
except ApiException as e:
    print("Exception when calling OCRPredictApi->o_cr_model_label_file_by_model_id_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **file**|  | 
 **model_id** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **o_cr_model_label_urls_by_model_id_post**
> o_cr_model_label_urls_by_model_id_post(urls, model_id)

Prediction for image url

Use the model to predict which one of the categories an image (given the image url) belongs to. You can specify multiple image urls.

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
api_instance = nanonets.OCRPredictApi(nanonets.ApiClient(configuration))
urls = 'urls_example' # str | 
model_id = 'model_id_example' # str | 

try:
    # Prediction for image url
    api_instance.o_cr_model_label_urls_by_model_id_post(urls, model_id)
except ApiException as e:
    print("Exception when calling OCRPredictApi->o_cr_model_label_urls_by_model_id_post: %s\n" % e)
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

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

