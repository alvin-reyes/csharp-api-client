# io.spfs.NeutoSpfs.Api.PublishApi

All URIs are relative to *http://localhost:8082/sp*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AnnounceRequestPublishDataSignatureReturnHashOnlyUsingPOST**](PublishApi.md#announcerequestpublishdatasignaturereturnhashonlyusingpost) | **POST** /publish/announce/return-hash-only | Announce the DataHash to NEM/P2P Storage and P2P Database and only returns the Nem Transaction Hash
[**AnnounceRequestPublishDataSignatureUsingPOST**](PublishApi.md#announcerequestpublishdatasignatureusingpost) | **POST** /publish/announce | Announce the DataHash to NEM/P2P Storage and P2P Database
[**PublishAndSendMultipleFilesToAddressUsingPOST**](PublishApi.md#publishandsendmultiplefilestoaddressusingpost) | **POST** /publish/multi/to/{address} | Store multiple files that can only be access by the given address
[**PublishAndSendSingleFileToAddressUsingPOST**](PublishApi.md#publishandsendsinglefiletoaddressusingpost) | **POST** /publish/single/to/{address} | Store a single file that can only be access by the given address
[**PublishAndSendSingleFileToAddressesUsingPOST**](PublishApi.md#publishandsendsinglefiletoaddressesusingpost) | **POST** /publish/single/to/addresses | Store a single file that can only be access by the given addresses


<a name="announcerequestpublishdatasignaturereturnhashonlyusingpost"></a>
# **AnnounceRequestPublishDataSignatureReturnHashOnlyUsingPOST**
> string AnnounceRequestPublishDataSignatureReturnHashOnlyUsingPOST (RequestAnnounceDataSignature requestAnnounceDataSignature = null)

Announce the DataHash to NEM/P2P Storage and P2P Database and only returns the Nem Transaction Hash

Endpoint that can be use to announce the data hash transaction. This will grab the signed BinaryTransaferTransaction and create the P2P Database Entry for the specific data hash / transaction.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.NeutoSpfs.Api;
using io.spfs.NeutoSpfs.Client;
using io.spfs.NeutoSpfs.Model;

namespace Example
{
    public class AnnounceRequestPublishDataSignatureReturnHashOnlyUsingPOSTExample
    {
        public void main()
        {
            var apiInstance = new PublishApi();
            var requestAnnounceDataSignature = new RequestAnnounceDataSignature(); // RequestAnnounceDataSignature | The Request Announce Data Signature Json Format (optional) 

            try
            {
                // Announce the DataHash to NEM/P2P Storage and P2P Database and only returns the Nem Transaction Hash
                string result = apiInstance.AnnounceRequestPublishDataSignatureReturnHashOnlyUsingPOST(requestAnnounceDataSignature);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PublishApi.AnnounceRequestPublishDataSignatureReturnHashOnlyUsingPOST: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestAnnounceDataSignature** | [**RequestAnnounceDataSignature**](RequestAnnounceDataSignature.md)| The Request Announce Data Signature Json Format | [optional] 

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="announcerequestpublishdatasignatureusingpost"></a>
# **AnnounceRequestPublishDataSignatureUsingPOST**
> ResponseEntity AnnounceRequestPublishDataSignatureUsingPOST (RequestAnnounceDataSignature requestAnnounceDataSignature = null)

Announce the DataHash to NEM/P2P Storage and P2P Database

Endpoint that can be use to announce the data hash transaction. This will grab the signed BinaryTransaferTransaction and create the P2P Database Entry for the specific data hash / transaction.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.NeutoSpfs.Api;
using io.spfs.NeutoSpfs.Client;
using io.spfs.NeutoSpfs.Model;

namespace Example
{
    public class AnnounceRequestPublishDataSignatureUsingPOSTExample
    {
        public void main()
        {
            var apiInstance = new PublishApi();
            var requestAnnounceDataSignature = new RequestAnnounceDataSignature(); // RequestAnnounceDataSignature | The Request Announce Data Signature Json Format (optional) 

            try
            {
                // Announce the DataHash to NEM/P2P Storage and P2P Database
                ResponseEntity result = apiInstance.AnnounceRequestPublishDataSignatureUsingPOST(requestAnnounceDataSignature);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PublishApi.AnnounceRequestPublishDataSignatureUsingPOST: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestAnnounceDataSignature** | [**RequestAnnounceDataSignature**](RequestAnnounceDataSignature.md)| The Request Announce Data Signature Json Format | [optional] 

### Return type

[**ResponseEntity**](ResponseEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="publishandsendmultiplefilestoaddressusingpost"></a>
# **PublishAndSendMultipleFilesToAddressUsingPOST**
> ResponseEntity PublishAndSendMultipleFilesToAddressUsingPOST (string address, string xPvkey = null, string messageType = null, List<System.IO.Stream> files = null)

Store multiple files that can only be access by the given address

This endpoint can be used to share multiple files to a specific address only. Note that multiple files in this context will create multiple transaction (1 transaction = 1 file).

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.NeutoSpfs.Api;
using io.spfs.NeutoSpfs.Client;
using io.spfs.NeutoSpfs.Model;

namespace Example
{
    public class PublishAndSendMultipleFilesToAddressUsingPOSTExample
    {
        public void main()
        {
            var apiInstance = new PublishApi();
            var address = address_example;  // string | The Receiver's Address without dash ('-')
            var xPvkey = xPvkey_example;  // string | The Sender's Private Key (optional) 
            var messageType = messageType_example;  // string | Message Type ( PLAIN or SECURE ) (optional) 
            var files = new List<System.IO.Stream>(); // List<System.IO.Stream> | The List of Multipart File (optional) 

            try
            {
                // Store multiple files that can only be access by the given address
                ResponseEntity result = apiInstance.PublishAndSendMultipleFilesToAddressUsingPOST(address, xPvkey, messageType, files);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PublishApi.PublishAndSendMultipleFilesToAddressUsingPOST: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string**| The Receiver&#39;s Address without dash (&#39;-&#39;) | 
 **xPvkey** | **string**| The Sender&#39;s Private Key | [optional] 
 **messageType** | **string**| Message Type ( PLAIN or SECURE ) | [optional] 
 **files** | [**List&lt;System.IO.Stream&gt;**](System.IO.Stream.md)| The List of Multipart File | [optional] 

### Return type

[**ResponseEntity**](ResponseEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="publishandsendsinglefiletoaddressusingpost"></a>
# **PublishAndSendSingleFileToAddressUsingPOST**
> ResponseEntity PublishAndSendSingleFileToAddressUsingPOST (string address, string xPvkey = null, string messageType = null, System.IO.Stream file = null)

Store a single file that can only be access by the given address

This endpoint can be used to share a file to a specific address only.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.NeutoSpfs.Api;
using io.spfs.NeutoSpfs.Client;
using io.spfs.NeutoSpfs.Model;

namespace Example
{
    public class PublishAndSendSingleFileToAddressUsingPOSTExample
    {
        public void main()
        {
            var apiInstance = new PublishApi();
            var address = address_example;  // string | The Receiver's Address without dash ('-')
            var xPvkey = xPvkey_example;  // string | The Sender's Private Key (optional) 
            var messageType = messageType_example;  // string | Message Type ( PLAIN or SECURE ) (optional) 
            var file = new System.IO.Stream(); // System.IO.Stream | The Multipart File (optional) 

            try
            {
                // Store a single file that can only be access by the given address
                ResponseEntity result = apiInstance.PublishAndSendSingleFileToAddressUsingPOST(address, xPvkey, messageType, file);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PublishApi.PublishAndSendSingleFileToAddressUsingPOST: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string**| The Receiver&#39;s Address without dash (&#39;-&#39;) | 
 **xPvkey** | **string**| The Sender&#39;s Private Key | [optional] 
 **messageType** | **string**| Message Type ( PLAIN or SECURE ) | [optional] 
 **file** | **System.IO.Stream**| The Multipart File | [optional] 

### Return type

[**ResponseEntity**](ResponseEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="publishandsendsinglefiletoaddressesusingpost"></a>
# **PublishAndSendSingleFileToAddressesUsingPOST**
> ResponseEntity PublishAndSendSingleFileToAddressesUsingPOST (string xPvkey = null, List<string> addresses = null, string messageType = null, System.IO.Stream file = null)

Store a single file that can only be access by the given addresses

This endpoint can be used to exclusively share files across a set of given addresses. This means that the file that's published here can only be viewed or downloaded by the given addresses including the uploader.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.NeutoSpfs.Api;
using io.spfs.NeutoSpfs.Client;
using io.spfs.NeutoSpfs.Model;

namespace Example
{
    public class PublishAndSendSingleFileToAddressesUsingPOSTExample
    {
        public void main()
        {
            var apiInstance = new PublishApi();
            var xPvkey = xPvkey_example;  // string | The Sender's Private Key (optional) 
            var addresses = new List<string>(); // List<string> | The List of receiving Addresses without dash ('-') (optional) 
            var messageType = messageType_example;  // string | Message Type ( PLAIN or SECURE ) (optional) 
            var file = new System.IO.Stream(); // System.IO.Stream | The Multipart File (optional) 

            try
            {
                // Store a single file that can only be access by the given addresses
                ResponseEntity result = apiInstance.PublishAndSendSingleFileToAddressesUsingPOST(xPvkey, addresses, messageType, file);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PublishApi.PublishAndSendSingleFileToAddressesUsingPOST: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xPvkey** | **string**| The Sender&#39;s Private Key | [optional] 
 **addresses** | [**List&lt;string&gt;**](string.md)| The List of receiving Addresses without dash (&#39;-&#39;) | [optional] 
 **messageType** | **string**| Message Type ( PLAIN or SECURE ) | [optional] 
 **file** | **System.IO.Stream**| The Multipart File | [optional] 

### Return type

[**ResponseEntity**](ResponseEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

