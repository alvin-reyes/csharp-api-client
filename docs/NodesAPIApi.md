# io.spfs.Api.NodesAPIApi

All URIs are relative to *http://p2ptest1.smartproof.io:8082/sp*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CheckNodeUsingGET**](NodesAPIApi.md#checknodeusingget) | **GET** /node/check | Check if the Storage Node is up and running.
[**GetNodeInfoUsingGET**](NodesAPIApi.md#getnodeinfousingget) | **GET** /node/info | Get Storage Node Information


<a name="checknodeusingget"></a>
# **CheckNodeUsingGET**
> string CheckNodeUsingGET ()

Check if the Storage Node is up and running.

This endpoint is used to check if the P2P Storage Node instance is either alive or down.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.Api;
using io.spfs.Client;
using io.spfs.Model;

namespace Example
{
    public class CheckNodeUsingGETExample
    {
        public void main()
        {
            var apiInstance = new NodesAPIApi();

            try
            {
                // Check if the Storage Node is up and running.
                string result = apiInstance.CheckNodeUsingGET();
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling NodesAPIApi.CheckNodeUsingGET: " + e.Message );
            }
        }
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="getnodeinfousingget"></a>
# **GetNodeInfoUsingGET**
> string GetNodeInfoUsingGET ()

Get Storage Node Information

This endpoint returns the information of the P2P Storage Node

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.Api;
using io.spfs.Client;
using io.spfs.Model;

namespace Example
{
    public class GetNodeInfoUsingGETExample
    {
        public void main()
        {
            var apiInstance = new NodesAPIApi();

            try
            {
                // Get Storage Node Information
                string result = apiInstance.GetNodeInfoUsingGET();
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling NodesAPIApi.GetNodeInfoUsingGET: " + e.Message );
            }
        }
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

