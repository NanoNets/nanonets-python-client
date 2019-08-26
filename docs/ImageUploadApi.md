# nanonets.ImageUploadApi

All URIs are relative to *https://app.nanonet.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**image_categorization_upload_file_post**](ImageUploadApi.md#image_categorization_upload_file_post) | **POST** /ImageCategorization/UploadFile/ | Upload training images by File
[**image_categorization_upload_urls_post**](ImageUploadApi.md#image_categorization_upload_urls_post) | **POST** /ImageCategorization/UploadUrls/ | Upload training images by Url

# **image_categorization_upload_file_post**
> image_categorization_upload_file_post(model_id, category, file)

Upload training images by File

You can use this endpoint to upload training images for a category (for the specified model) using locally stored files. You will receive model information along with total number of images per category on successful execution. <br>Note: Filename in Data must be the same as that of the uploaded image name.

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
api_instance = nanonets.ImageUploadApi(nanonets.ApiClient(configuration))
model_id = 'model_id_example' # str | 
category = 'category_example' # str | 
file = 'file_example' # file | 

try:
    # Upload training images by File
    api_instance.image_categorization_upload_file_post(model_id, category, file)
except ApiException as e:
    print("Exception when calling ImageUploadApi->image_categorization_upload_file_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_id** | [**str**](.md)|  | 
 **category** | [**str**](.md)|  | 
 **file** | **file**|  | 

### Return type

void (empty response body)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **image_categorization_upload_urls_post**
> image_categorization_upload_urls_post(model_id, category, urls)

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
api_instance = nanonets.ImageUploadApi(nanonets.ApiClient(configuration))
model_id = 'model_id_example' # str | 
category = 'category_example' # str | 
urls = 'urls_example' # str | 

try:
    # Upload training images by Url
    api_instance.image_categorization_upload_urls_post(model_id, category, urls)
except ApiException as e:
    print("Exception when calling ImageUploadApi->image_categorization_upload_urls_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_id** | [**str**](.md)|  | 
 **category** | [**str**](.md)|  | 
 **urls** | [**str**](.md)|  | 

### Return type

void (empty response body)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

