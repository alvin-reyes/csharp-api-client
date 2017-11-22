# io.spfs.Api.DataHashAPIApi

All URIs are relative to *http://p2ptest1.smartproof.io:8082/sp*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GenerateByteArrayDataHashOnlyUsingPOST**](DataHashAPIApi.md#generatebytearraydatahashonlyusingpost) | **POST** /datahash/byte-array/hashonly | Gets the encrypted datahash of a file (in the form of byte array) only.
[**GenerateDataHashOnlyUsingPOST**](DataHashAPIApi.md#generatedatahashonlyusingpost) | **POST** /datahash/hashonly | Gets the encrypted datahash of a file only.
[**GenerateHashAndExposeByteArrayFileToNetworkUsingPOST**](DataHashAPIApi.md#generatehashandexposebytearrayfiletonetworkusingpost) | **POST** /datahash/generate/byte-array | Gets the encrypted datahash and uploads the file (in the form of byte array) in the process.
[**GenerateHashAndExposeFileToNetworkUsingPOST**](DataHashAPIApi.md#generatehashandexposefiletonetworkusingpost) | **POST** /datahash/generate | Gets the encrypted datahash and uploads the file in the process.
[**GenerateHashExposeFileToNetworkBuildAndSignUsingPOST**](DataHashAPIApi.md#generatehashexposefiletonetworkbuildandsignusingpost) | **POST** /datahash/generate-sign | This endpoint can be used to generate the transaction along with the data hash with the private key signature.


<a name="generatebytearraydatahashonlyusingpost"></a>
# **GenerateByteArrayDataHashOnlyUsingPOST**
> string GenerateByteArrayDataHashOnlyUsingPOST (string fileName = null, byte[] byteArrayFile = null)

Gets the encrypted datahash of a file (in the form of byte array) only.

The endpoint can be used to get the datahash of the file without pinning the file on the P2P Network

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.Api;
using io.spfs.Client;
using io.spfs.Model;

namespace Example
{
    public class GenerateByteArrayDataHashOnlyUsingPOSTExample
    {
        public void main()
        {
            var apiInstance = new DataHashAPIApi();
            var fileName = fileName_example;  // string | File name (optional) 
            var byteArrayFile = byteArrayFile_example;  // byte[] | The Byte Array File (optional) 

            try
            {
                // Gets the encrypted datahash of a file (in the form of byte array) only.
                string result = apiInstance.GenerateByteArrayDataHashOnlyUsingPOST(fileName, byteArrayFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DataHashAPIApi.GenerateByteArrayDataHashOnlyUsingPOST: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fileName** | **string**| File name | [optional] 
 **byteArrayFile** | **byte[]**| The Byte Array File | [optional] 

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="generatedatahashonlyusingpost"></a>
# **GenerateDataHashOnlyUsingPOST**
> string GenerateDataHashOnlyUsingPOST (System.IO.Stream file = null)

Gets the encrypted datahash of a file only.

The endpoint can be used to get the datahash of the file without pinning the file on the P2P Network

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.Api;
using io.spfs.Client;
using io.spfs.Model;

namespace Example
{
    public class GenerateDataHashOnlyUsingPOSTExample
    {
        public void main()
        {
            var apiInstance = new DataHashAPIApi();
            var file = new System.IO.Stream(); // System.IO.Stream | The Multipart File (optional) 

            try
            {
                // Gets the encrypted datahash of a file only.
                string result = apiInstance.GenerateDataHashOnlyUsingPOST(file);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DataHashAPIApi.GenerateDataHashOnlyUsingPOST: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **System.IO.Stream**| The Multipart File | [optional] 

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="generatehashandexposebytearrayfiletonetworkusingpost"></a>
# **GenerateHashAndExposeByteArrayFileToNetworkUsingPOST**
> string GenerateHashAndExposeByteArrayFileToNetworkUsingPOST (string fileName = null, byte[] byteArrayFile = null)

Gets the encrypted datahash and uploads the file (in the form of byte array) in the process.

The endpoint that can be used to expose and generate the data hash of a given file. The data hash can then be used to create a secured message, that can then be signed by the SPFS Java Client App. Limit: 900MB.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.Api;
using io.spfs.Client;
using io.spfs.Model;

namespace Example
{
    public class GenerateHashAndExposeByteArrayFileToNetworkUsingPOSTExample
    {
        public void main()
        {
            var apiInstance = new DataHashAPIApi();
            var fileName = fileName_example;  // string | File name (optional) 
            var byteArrayFile = byteArrayFile_example;  // byte[] | The Byte Array File (optional) 

            try
            {
                // Gets the encrypted datahash and uploads the file (in the form of byte array) in the process.
                string result = apiInstance.GenerateHashAndExposeByteArrayFileToNetworkUsingPOST(fileName, byteArrayFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DataHashAPIApi.GenerateHashAndExposeByteArrayFileToNetworkUsingPOST: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fileName** | **string**| File name | [optional] 
 **byteArrayFile** | **byte[]**| The Byte Array File | [optional] 

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="generatehashandexposefiletonetworkusingpost"></a>
# **GenerateHashAndExposeFileToNetworkUsingPOST**
> string GenerateHashAndExposeFileToNetworkUsingPOST (System.IO.Stream file = null)

Gets the encrypted datahash and uploads the file in the process.

This endpoint can be used to generate the transaction along with the data hash with the private key signature.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.Api;
using io.spfs.Client;
using io.spfs.Model;

namespace Example
{
    public class GenerateHashAndExposeFileToNetworkUsingPOSTExample
    {
        public void main()
        {
            var apiInstance = new DataHashAPIApi();
            var file = new System.IO.Stream(); // System.IO.Stream | The Multipart File (optional) 

            try
            {
                // Gets the encrypted datahash and uploads the file in the process.
                string result = apiInstance.GenerateHashAndExposeFileToNetworkUsingPOST(file);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DataHashAPIApi.GenerateHashAndExposeFileToNetworkUsingPOST: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **System.IO.Stream**| The Multipart File | [optional] 

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="generatehashexposefiletonetworkbuildandsignusingpost"></a>
# **GenerateHashExposeFileToNetworkBuildAndSignUsingPOST**
> RequestAnnounceDataSignature GenerateHashExposeFileToNetworkBuildAndSignUsingPOST (string xPvkey = null, string xPubkey = null, string messageType = null, System.IO.Stream file = null)

This endpoint can be used to generate the transaction along with the data hash with the private key signature.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.Api;
using io.spfs.Client;
using io.spfs.Model;

namespace Example
{
    public class GenerateHashExposeFileToNetworkBuildAndSignUsingPOSTExample
    {
        public void main()
        {
            var apiInstance = new DataHashAPIApi();
            var xPvkey = xPvkey_example;  // string | Sender Private Key (optional) 
            var xPubkey = xPubkey_example;  // string | Receiver Public Key (optional) 
            var messageType = messageType_example;  // string | Message Type ( PLAIN or SECURE ) (optional) 
            var file = new System.IO.Stream(); // System.IO.Stream | The Multipart File (optional) 

            try
            {
                // This endpoint can be used to generate the transaction along with the data hash with the private key signature.
                RequestAnnounceDataSignature result = apiInstance.GenerateHashExposeFileToNetworkBuildAndSignUsingPOST(xPvkey, xPubkey, messageType, file);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DataHashAPIApi.GenerateHashExposeFileToNetworkBuildAndSignUsingPOST: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xPvkey** | **string**| Sender Private Key | [optional] 
 **xPubkey** | **string**| Receiver Public Key | [optional] 
 **messageType** | **string**| Message Type ( PLAIN or SECURE ) | [optional] 
 **file** | **System.IO.Stream**| The Multipart File | [optional] 

### Return type

[**RequestAnnounceDataSignature**](RequestAnnounceDataSignature.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

