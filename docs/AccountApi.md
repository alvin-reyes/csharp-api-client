# io.spfs.NeutoSpfs.Api.AccountApi

All URIs are relative to *http://localhost:8082/sp*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GenerateAccountUsingGET**](AccountApi.md#generateaccountusingget) | **GET** /account/generate | Generate a new Address along with Public and Private Keys
[**GetNemAddressDetailsUsingGET**](AccountApi.md#getnemaddressdetailsusingget) | **GET** /account/get/{nemAddress} | Get the NEM Address Details


<a name="generateaccountusingget"></a>
# **GenerateAccountUsingGET**
> GeneratedAccount GenerateAccountUsingGET ()

Generate a new Address along with Public and Private Keys

This endpoint returns the newly generated Address from NEM Platform

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.NeutoSpfs.Api;
using io.spfs.NeutoSpfs.Client;
using io.spfs.NeutoSpfs.Model;

namespace Example
{
    public class GenerateAccountUsingGETExample
    {
        public void main()
        {
            var apiInstance = new AccountApi();

            try
            {
                // Generate a new Address along with Public and Private Keys
                GeneratedAccount result = apiInstance.GenerateAccountUsingGET();
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling AccountApi.GenerateAccountUsingGET: " + e.Message );
            }
        }
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**GeneratedAccount**](GeneratedAccount.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="getnemaddressdetailsusingget"></a>
# **GetNemAddressDetailsUsingGET**
> AccountMetaDataPair GetNemAddressDetailsUsingGET (string nemAddress)

Get the NEM Address Details

This endpoint returns the NEM Address/Account Information of a given address

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.NeutoSpfs.Api;
using io.spfs.NeutoSpfs.Client;
using io.spfs.NeutoSpfs.Model;

namespace Example
{
    public class GetNemAddressDetailsUsingGETExample
    {
        public void main()
        {
            var apiInstance = new AccountApi();
            var nemAddress = nemAddress_example;  // string | The NEM Address without the dash ('-')

            try
            {
                // Get the NEM Address Details
                AccountMetaDataPair result = apiInstance.GetNemAddressDetailsUsingGET(nemAddress);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling AccountApi.GetNemAddressDetailsUsingGET: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **nemAddress** | **string**| The NEM Address without the dash (&#39;-&#39;) | 

### Return type

[**AccountMetaDataPair**](AccountMetaDataPair.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

