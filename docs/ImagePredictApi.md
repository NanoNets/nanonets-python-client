# nanonets.ImagePredictApi

All URIs are relative to *https://app.nanonet.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**image_categorization_label_file_post**](ImagePredictApi.md#image_categorization_label_file_post) | **POST** /ImageCategorization/LabelFile/ | Prediction for image File
[**image_categorization_label_urls_post2**](ImagePredictApi.md#image_categorization_label_urls_post2) | **POST** /ImageCategorization/LabelUrls/ | Prediction for image URLs

# **image_categorization_label_file_post**
> image_categorization_label_file_post(model_id, file)

Prediction for image File

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
api_instance = nanonets.ImagePredictApi(nanonets.ApiClient(configuration))
model_id = 'model_id_example' # str | 
file = 'file_example' # file | 

try:
    # Prediction for image File
    api_instance.image_categorization_label_file_post(model_id, file)
except ApiException as e:
    print("Exception when calling ImagePredictApi->image_categorization_label_file_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_id** | [**str**](.md)|  | 
 **file** | **file**|  | 

### Return type

void (empty response body)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **image_categorization_label_urls_post2**
> image_categorization_label_urls_post2(model_id, urls)

Prediction for image URLs

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
api_instance = nanonets.ImagePredictApi(nanonets.ApiClient(configuration))
model_id = 'model_id_example' # str | 
urls = 'urls_example' # str | 

try:
    # Prediction for image URLs
    api_instance.image_categorization_label_urls_post2(model_id, urls)
except ApiException as e:
    print("Exception when calling ImagePredictApi->image_categorization_label_urls_post2: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_id** | [**str**](.md)|  | 
 **urls** | [**str**](.md)|  | 

### Return type

void (empty response body)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

