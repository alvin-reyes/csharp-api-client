# io.spfs.Api.SearchAPIApi

All URIs are relative to *http://p2ptest1.smartproof.io:8082/sp*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GrabPlainMessageTransactionUsingGET**](SearchAPIApi.md#grabplainmessagetransactionusingget) | **GET** /search/transaction/plain/{nemhash} | NEM Transaction Hash based file lookup.
[**GrabSsecureMessageTransactionUsingGET**](SearchAPIApi.md#grabssecuremessagetransactionusingget) | **GET** /search/transaction/secure/{nemhash} | NEM Transaction Hash based file lookup.
[**GrabTransactionUsingGET**](SearchAPIApi.md#grabtransactionusingget) | **GET** /search/transaction/{nemhash} | NEM Transaction Hash based file lookup.
[**SearchAssetWithKeyUsingGET**](SearchAPIApi.md#searchassetwithkeyusingget) | **GET** /search/text/{searchKey} | Key/Text-based search of available files.
[**SearchAssetWithNemHashUsingGET**](SearchAPIApi.md#searchassetwithnemhashusingget) | **GET** /search/data/{nemhash} | NEM Transaction Hash based file lookup.


<a name="grabplainmessagetransactionusingget"></a>
# **GrabPlainMessageTransactionUsingGET**
> BinaryTransactionEncryptedMessage GrabPlainMessageTransactionUsingGET (string nemhash)

NEM Transaction Hash based file lookup.

This endpoint can be used to grab the actual Signed and Confirmed TransferTransaction structure that can then be cast to the object. It has the Encrypted and Encoded Payload.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.Api;
using io.spfs.Client;
using io.spfs.Model;

namespace Example
{
    public class GrabPlainMessageTransactionUsingGETExample
    {
        public void main()
        {
            var apiInstance = new SearchAPIApi();
            var nemhash = nemhash_example;  // string | The NEM Transaction Hash

            try
            {
                // NEM Transaction Hash based file lookup.
                BinaryTransactionEncryptedMessage result = apiInstance.GrabPlainMessageTransactionUsingGET(nemhash);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling SearchAPIApi.GrabPlainMessageTransactionUsingGET: " + e.Message );
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

[**BinaryTransactionEncryptedMessage**](BinaryTransactionEncryptedMessage.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="grabssecuremessagetransactionusingget"></a>
# **GrabSsecureMessageTransactionUsingGET**
> BinaryTransactionEncryptedMessage GrabSsecureMessageTransactionUsingGET (string nemhash, string xPvkey = null)

NEM Transaction Hash based file lookup.

This endpoint can be used to grab the actual Signed and Confirmed TransferTransaction structure that can then be cast to the object. It has the Encrypted and Encoded Payload.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.Api;
using io.spfs.Client;
using io.spfs.Model;

namespace Example
{
    public class GrabSsecureMessageTransactionUsingGETExample
    {
        public void main()
        {
            var apiInstance = new SearchAPIApi();
            var nemhash = nemhash_example;  // string | The NEM Transaction Hash
            var xPvkey = xPvkey_example;  // string | The Sender or Receiver's Private Key (optional) 

            try
            {
                // NEM Transaction Hash based file lookup.
                BinaryTransactionEncryptedMessage result = apiInstance.GrabSsecureMessageTransactionUsingGET(nemhash, xPvkey);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling SearchAPIApi.GrabSsecureMessageTransactionUsingGET: " + e.Message );
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

[**BinaryTransactionEncryptedMessage**](BinaryTransactionEncryptedMessage.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="grabtransactionusingget"></a>
# **GrabTransactionUsingGET**
> string GrabTransactionUsingGET (string nemhash, string xPubkey = null)

NEM Transaction Hash based file lookup.

This endpoint can be used to grab the actual Signed and Confirmed TransferTransaction structure that can then be cast to the object. It has the Encrypted and Encoded Payload.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.Api;
using io.spfs.Client;
using io.spfs.Model;

namespace Example
{
    public class GrabTransactionUsingGETExample
    {
        public void main()
        {
            var apiInstance = new SearchAPIApi();
            var nemhash = nemhash_example;  // string | The NEM Transaction Hash
            var xPubkey = xPubkey_example;  // string | The Sender or Receiver's Public Key (optional) 

            try
            {
                // NEM Transaction Hash based file lookup.
                string result = apiInstance.GrabTransactionUsingGET(nemhash, xPubkey);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling SearchAPIApi.GrabTransactionUsingGET: " + e.Message );
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

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="searchassetwithkeyusingget"></a>
# **SearchAssetWithKeyUsingGET**
> string SearchAssetWithKeyUsingGET (string searchKey, string xPubkey = null)

Key/Text-based search of available files.

This endpoint can be used to exclusively search for all files that are associated to the public key specified.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.Api;
using io.spfs.Client;
using io.spfs.Model;

namespace Example
{
    public class SearchAssetWithKeyUsingGETExample
    {
        public void main()
        {
            var apiInstance = new SearchAPIApi();
            var searchKey = searchKey_example;  // string | The Search Key
            var xPubkey = xPubkey_example;  // string | The Sender or Receiver's Public Key (optional) 

            try
            {
                // Key/Text-based search of available files.
                string result = apiInstance.SearchAssetWithKeyUsingGET(searchKey, xPubkey);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling SearchAPIApi.SearchAssetWithKeyUsingGET: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **searchKey** | **string**| The Search Key | 
 **xPubkey** | **string**| The Sender or Receiver&#39;s Public Key | [optional] 

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="searchassetwithnemhashusingget"></a>
# **SearchAssetWithNemHashUsingGET**
> string SearchAssetWithNemHashUsingGET (string nemhash, string xPubkey = null)

NEM Transaction Hash based file lookup.

This endpoint can be use to lookup a specific upload/store entry using the NEM Transaction Hash. Given this, only the owner or intended receiver can only access the entry using the public key

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.Api;
using io.spfs.Client;
using io.spfs.Model;

namespace Example
{
    public class SearchAssetWithNemHashUsingGETExample
    {
        public void main()
        {
            var apiInstance = new SearchAPIApi();
            var nemhash = nemhash_example;  // string | The NEM Transaction Hash
            var xPubkey = xPubkey_example;  // string | The Sender or Receiver's Public Key (optional) 

            try
            {
                // NEM Transaction Hash based file lookup.
                string result = apiInstance.SearchAssetWithNemHashUsingGET(nemhash, xPubkey);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling SearchAPIApi.SearchAssetWithNemHashUsingGET: " + e.Message );
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

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

