# nanonets.MultiLabelClassificationUploadApi

All URIs are relative to *https://app.nanonet.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**multi_label_classification_upload_files_post**](MultiLabelClassificationUploadApi.md#multi_label_classification_upload_files_post) | **POST** /MultiLabelClassification/Model/{model_id}/UploadFiles/ | Upload training images by File
[**multi_label_classification_upload_urls_post**](MultiLabelClassificationUploadApi.md#multi_label_classification_upload_urls_post) | **POST** /MultiLabelClassification/Model/{model_id}/UploadUrls/ | Upload training images by Urls

# **multi_label_classification_upload_files_post**
> multi_label_classification_upload_files_post(data, files, model_id)

Upload training images by File

You can use this endpoint to upload multiple training images using locally stored files and optionally send the corresponding annotations for the images. You will receive the upload status of each file in the response.

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
api_instance = nanonets.MultiLabelClassificationUploadApi(nanonets.ApiClient(configuration))
data = 'data_example' # str | 
files = 'files_example' # file | 
model_id = 'model_id_example' # str | 

try:
    # Upload training images by File
    api_instance.multi_label_classification_upload_files_post(data, files, model_id)
except ApiException as e:
    print("Exception when calling MultiLabelClassificationUploadApi->multi_label_classification_upload_files_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **data** | [**str**](.md)|  | 
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

# **multi_label_classification_upload_urls_post**
> multi_label_classification_upload_urls_post(data, urls, model_id)

Upload training images by Urls

You can use this endpoint to upload multiple training images using urls and optionally send the corresponding annotations for the images. You will receive the upload status of each url in the response.

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
api_instance = nanonets.MultiLabelClassificationUploadApi(nanonets.ApiClient(configuration))
data = 'data_example' # str | 
urls = 'urls_example' # str | 
model_id = 'model_id_example' # str | 

try:
    # Upload training images by Urls
    api_instance.multi_label_classification_upload_urls_post(data, urls, model_id)
except ApiException as e:
    print("Exception when calling MultiLabelClassificationUploadApi->multi_label_classification_upload_urls_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **data** | [**str**](.md)|  | 
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

