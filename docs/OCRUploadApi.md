# nanonets.OCRUploadApi

All URIs are relative to *https://app.nanonet.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**o_cr_model_upload_file_by_model_id_post**](OCRUploadApi.md#o_cr_model_upload_file_by_model_id_post) | **POST** /OCR/Model/{model_id}/UploadFile/ | Upload training images by File
[**o_cr_model_upload_urls_by_model_id_post**](OCRUploadApi.md#o_cr_model_upload_urls_by_model_id_post) | **POST** /OCR/Model/{model_id}/UploadUrls/ | Upload training images by Url

# **o_cr_model_upload_file_by_model_id_post**
> o_cr_model_upload_file_by_model_id_post(data, file, model_id)

Upload training images by File

You can use this endpoint to upload training images for a category (for the specified model) using locally stored files. You will receive model information along with total number of images per category on successful execution. <br>Note: Filename in Data must be the same as that of the uploaded image name.

### Example
```python
from __future__ import print_function
import time
import nanonets
from nanonets.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = nanonets.OCRUploadApi()
data = 'data_example' # str | 
file = 'file_example' # file | 
model_id = 'model_id_example' # str | 

try:
    # Upload training images by File
    api_instance.o_cr_model_upload_file_by_model_id_post(data, file, model_id)
except ApiException as e:
    print("Exception when calling OCRUploadApi->o_cr_model_upload_file_by_model_id_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **data** | [**str**](.md)|  | 
 **file** | **file**|  | 
 **model_id** | **str**|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **o_cr_model_upload_urls_by_model_id_post**
> o_cr_model_upload_urls_by_model_id_post(body, content_type, model_id)

Upload training images by Url

You can use this endpoint to upload training images for a category (for the specified model) by image urls. You can upload multiple images in the same request by adding an array of urls. You will receive model information along with total number of images per category on successful execution.

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
api_instance = nanonets.OCRUploadApi(nanonets.ApiClient(configuration))
body = nanonets.UploadTrainingImagesByUrlrequest() # UploadTrainingImagesByUrlrequest | 
content_type = 'content_type_example' # str | 
model_id = 'model_id_example' # str | 

try:
    # Upload training images by Url
    api_instance.o_cr_model_upload_urls_by_model_id_post(body, content_type, model_id)
except ApiException as e:
    print("Exception when calling OCRUploadApi->o_cr_model_upload_urls_by_model_id_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**UploadTrainingImagesByUrlrequest**](UploadTrainingImagesByUrlrequest.md)|  | 
 **content_type** | **str**|  | 
 **model_id** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

