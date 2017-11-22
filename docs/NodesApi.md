# io.spfs.NeutoSpfs.Api.NodesApi

All URIs are relative to *http://localhost:8082/sp*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CheckNodeUsingGET**](NodesApi.md#checknodeusingget) | **GET** /node/check | Check if the Storage Node is up and running.
[**GetNodeInfoUsingGET**](NodesApi.md#getnodeinfousingget) | **GET** /node/info | Get Storage Node Information


<a name="checknodeusingget"></a>
# **CheckNodeUsingGET**
> string CheckNodeUsingGET ()

Check if the Storage Node is up and running.

This endpoint is used to check if the P2P Storage Node instance is either alive or down.

### Example
```csharp
using System;
using System.Diagnostics;
using io.spfs.NeutoSpfs.Api;
using io.spfs.NeutoSpfs.Client;
using io.spfs.NeutoSpfs.Model;

namespace Example
{
    public class CheckNodeUsingGETExample
    {
        public void main()
        {
            var apiInstance = new NodesApi();

            try
            {
                // Check if the Storage Node is up and running.
                string result = apiInstance.CheckNodeUsingGET();
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling NodesApi.CheckNodeUsingGET: " + e.Message );
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
 - **Accept**: application/json

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
using io.spfs.NeutoSpfs.Api;
using io.spfs.NeutoSpfs.Client;
using io.spfs.NeutoSpfs.Model;

namespace Example
{
    public class GetNodeInfoUsingGETExample
    {
        public void main()
        {
            var apiInstance = new NodesApi();

            try
            {
                // Get Storage Node Information
                string result = apiInstance.GetNodeInfoUsingGET();
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling NodesApi.GetNodeInfoUsingGET: " + e.Message );
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
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

