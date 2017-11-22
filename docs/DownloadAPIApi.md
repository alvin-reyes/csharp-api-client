# io.spfs.Api.DownloadAPIApi

All URIs are relative to *http://p2ptest1.smartproof.io:8082/sp*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DownloadFileUsingNemHashAndEncryptedHashUsingGET**](DownloadAPIApi.md#downloadfileusingnemhashandencryptedhashusingget) | **GET** /download/data/{nemhash} | Download resource/file using NEM Transaction Hash
[**DownloadFileUsingNemHashUsingGET**](DownloadAPIApi.md#downloadfileusingnemhashusingget) | **GET** /download/byte-array/{nemhash} | Download resource/file using NEM Transaction Hash
[**DownloadPlainMessageFileUsingNemHashUsingGET**](DownloadAPIApi.md#downloadplainmessagefileusingnemhashusingget) | **GET** /download/data/plain/{nemhash} | Download resource/file using NEM Transaction Hash
[**DownloadSecureMessageFileUsingNemHashUsingGET**](DownloadAPIApi.md#downloadsecuremessagefileusingnemhashusingget) | **GET** /download/data/secure/{nemhash} | Download resource/file using NEM Transaction Hash


<a name="downloadfileusingnemhashandencryptedhashusingget"></a>
# **DownloadFileUsingNemHashAndEncryptedHashUsingGET**
> ResponseEntity DownloadFileUsingNemHashAndEncryptedHashUsingGET (string nemhash, string xPubkey = null)

Download resource/file using NEM Transaction Hash

The endpoint returns the Transaction that has the message with the data hash.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.Api;
using io.spfs.Client;
using io.spfs.Model;

namespace Example
{
    public class DownloadFileUsingNemHashAndEncryptedHashUsingGETExample
    {
        public void main()
        {
            var apiInstance = new DownloadAPIApi();
            var nemhash = nemhash_example;  // string | The NEM Transaction Hash
            var xPubkey = xPubkey_example;  // string | The Sender or Receiver's Public Key (optional) 

            try
            {
                // Download resource/file using NEM Transaction Hash
                ResponseEntity result = apiInstance.DownloadFileUsingNemHashAndEncryptedHashUsingGET(nemhash, xPubkey);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DownloadAPIApi.DownloadFileUsingNemHashAndEncryptedHashUsingGET: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **nemhash** | **string**| The NEM Transaction Hash | 
 **xPubkey** | **string**| The Sender or Receiver&#39;s Public Key | [optional] 

### Return type

[**ResponseEntity**](ResponseEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="downloadfileusingnemhashusingget"></a>
# **DownloadFileUsingNemHashUsingGET**
> ResponseEntity DownloadFileUsingNemHashUsingGET (string nemhash, string xPvkey = null)

Download resource/file using NEM Transaction Hash

This endpoint returns either a byte array format of the actual file OR a JSON format GenericMessageResponse.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.Api;
using io.spfs.Client;
using io.spfs.Model;

namespace Example
{
    public class DownloadFileUsingNemHashUsingGETExample
    {
        public void main()
        {
            var apiInstance = new DownloadAPIApi();
            var nemhash = nemhash_example;  // string | The NEM Transaction Hash
            var xPvkey = xPvkey_example;  // string | The Sender or Receiver's Private Key (optional) 

            try
            {
                // Download resource/file using NEM Transaction Hash
                ResponseEntity result = apiInstance.DownloadFileUsingNemHashUsingGET(nemhash, xPvkey);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DownloadAPIApi.DownloadFileUsingNemHashUsingGET: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **nemhash** | **string**| The NEM Transaction Hash | 
 **xPvkey** | **string**| The Sender or Receiver&#39;s Private Key | [optional] 

### Return type

[**ResponseEntity**](ResponseEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="downloadplainmessagefileusingnemhashusingget"></a>
# **DownloadPlainMessageFileUsingNemHashUsingGET**
> ResponseEntity DownloadPlainMessageFileUsingNemHashUsingGET (string nemhash)

Download resource/file using NEM Transaction Hash

This endpoint returns either a byte array format of the actual file OR a JSON format GenericMessageResponse.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.Api;
using io.spfs.Client;
using io.spfs.Model;

namespace Example
{
    public class DownloadPlainMessageFileUsingNemHashUsingGETExample
    {
        public void main()
        {
            var apiInstance = new DownloadAPIApi();
            var nemhash = nemhash_example;  // string | The NEM Transaction Hash

            try
            {
                // Download resource/file using NEM Transaction Hash
                ResponseEntity result = apiInstance.DownloadPlainMessageFileUsingNemHashUsingGET(nemhash);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DownloadAPIApi.DownloadPlainMessageFileUsingNemHashUsingGET: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **nemhash** | **string**| The NEM Transaction Hash | 

### Return type

[**ResponseEntity**](ResponseEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="downloadsecuremessagefileusingnemhashusingget"></a>
# **DownloadSecureMessageFileUsingNemHashUsingGET**
> ResponseEntity DownloadSecureMessageFileUsingNemHashUsingGET (string nemhash, string xPvkey = null)

Download resource/file using NEM Transaction Hash

This endpoint returns either a byte array format of the actual file OR a JSON format GenericMessageResponse.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.Api;
using io.spfs.Client;
using io.spfs.Model;

namespace Example
{
    public class DownloadSecureMessageFileUsingNemHashUsingGETExample
    {
        public void main()
        {
            var apiInstance = new DownloadAPIApi();
            var nemhash = nemhash_example;  // string | The NEM Transaction Hash
            var xPvkey = xPvkey_example;  // string | The Sender or Receiver's Public Key (optional) 

            try
            {
                // Download resource/file using NEM Transaction Hash
                ResponseEntity result = apiInstance.DownloadSecureMessageFileUsingNemHashUsingGET(nemhash, xPvkey);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DownloadAPIApi.DownloadSecureMessageFileUsingNemHashUsingGET: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **nemhash** | **string**| The NEM Transaction Hash | 
 **xPvkey** | **string**| The Sender or Receiver&#39;s Public Key | [optional] 

### Return type

[**ResponseEntity**](ResponseEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

