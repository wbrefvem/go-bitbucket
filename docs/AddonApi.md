# \AddonApi

All URIs are relative to *https://api.bitbucket.org/2.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddonDelete**](AddonApi.md#AddonDelete) | **Delete** /addon | 
[**AddonLinkersGet**](AddonApi.md#AddonLinkersGet) | **Get** /addon/linkers | 
[**AddonLinkersLinkerKeyGet**](AddonApi.md#AddonLinkersLinkerKeyGet) | **Get** /addon/linkers/{linker_key} | 
[**AddonLinkersLinkerKeyValuesDelete**](AddonApi.md#AddonLinkersLinkerKeyValuesDelete) | **Delete** /addon/linkers/{linker_key}/values | 
[**AddonLinkersLinkerKeyValuesDelete_0**](AddonApi.md#AddonLinkersLinkerKeyValuesDelete_0) | **Delete** /addon/linkers/{linker_key}/values/ | 
[**AddonLinkersLinkerKeyValuesGet**](AddonApi.md#AddonLinkersLinkerKeyValuesGet) | **Get** /addon/linkers/{linker_key}/values | 
[**AddonLinkersLinkerKeyValuesGet_0**](AddonApi.md#AddonLinkersLinkerKeyValuesGet_0) | **Get** /addon/linkers/{linker_key}/values/ | 
[**AddonLinkersLinkerKeyValuesPost**](AddonApi.md#AddonLinkersLinkerKeyValuesPost) | **Post** /addon/linkers/{linker_key}/values | 
[**AddonLinkersLinkerKeyValuesPut**](AddonApi.md#AddonLinkersLinkerKeyValuesPut) | **Put** /addon/linkers/{linker_key}/values | 
[**AddonPut**](AddonApi.md#AddonPut) | **Put** /addon | 
[**AddonUsersTargetUserEventsEventKeyPost**](AddonApi.md#AddonUsersTargetUserEventsEventKeyPost) | **Post** /addon/users/{target_user}/events/{event_key} | 


# **AddonDelete**
> ModelError AddonDelete(ctx, )




### Required Parameters
This endpoint does not need any parameter.

### Return type

[**ModelError**](error.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **AddonLinkersGet**
> ModelError AddonLinkersGet(ctx, )




### Required Parameters
This endpoint does not need any parameter.

### Return type

[**ModelError**](error.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **AddonLinkersLinkerKeyGet**
> ModelError AddonLinkersLinkerKeyGet(ctx, linkerKey)




### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **linkerKey** | **string**|  | 

### Return type

[**ModelError**](error.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **AddonLinkersLinkerKeyValuesDelete**
> ModelError AddonLinkersLinkerKeyValuesDelete(ctx, linkerKey)




### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **linkerKey** | **string**|  | 

### Return type

[**ModelError**](error.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **AddonLinkersLinkerKeyValuesDelete_0**
> ModelError AddonLinkersLinkerKeyValuesDelete_0(ctx, linkerKey)




### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **linkerKey** | **string**|  | 

### Return type

[**ModelError**](error.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **AddonLinkersLinkerKeyValuesGet**
> ModelError AddonLinkersLinkerKeyValuesGet(ctx, linkerKey)




### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **linkerKey** | **string**|  | 

### Return type

[**ModelError**](error.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **AddonLinkersLinkerKeyValuesGet_0**
> ModelError AddonLinkersLinkerKeyValuesGet_0(ctx, linkerKey)




### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **linkerKey** | **string**|  | 

### Return type

[**ModelError**](error.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **AddonLinkersLinkerKeyValuesPost**
> ModelError AddonLinkersLinkerKeyValuesPost(ctx, linkerKey)




### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **linkerKey** | **string**|  | 

### Return type

[**ModelError**](error.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **AddonLinkersLinkerKeyValuesPut**
> ModelError AddonLinkersLinkerKeyValuesPut(ctx, linkerKey)




### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **linkerKey** | **string**|  | 

### Return type

[**ModelError**](error.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **AddonPut**
> ModelError AddonPut(ctx, )




### Required Parameters
This endpoint does not need any parameter.

### Return type

[**ModelError**](error.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **AddonUsersTargetUserEventsEventKeyPost**
> AddonUsersTargetUserEventsEventKeyPost(ctx, targetUser, eventKey)


POST a new custom event.  The data within the event body will be hydrated by Bitbucket. For example, the following event submission would result in subscribers for the event receiving the full repository object corresponding to the UUID.  ``` $ curl -X POST -H \"Content-Type: application/json\" -d '{     \"mynumdata\": \"12345\",     \"repository\": {         \"type\": \"repository\",         \"uuid\": \"{be95aa1f-c0b2-47f6-99d1-bf5d3a0f850f}\" }}' https://api.bitbucket.org/2.0/addon/users/myuser/events/com.example.app%3Amyevent ```  Use the optional `fields` property of the custom event Connect module where the event is defined to add additional fields to the expanded payload sent to listeners.  For example, the `customEvents` module in the app descriptor for the previous example would look like this:  ``` 'modules': {     'customEvents': {         'com.example.app:myevent': {             'schema': {                 'properties': {                     'mynumdata': {'type': 'number'},                     'repository': {'$ref': '#/definitions/repository'}                 }             },             'fields': ['repository.owner']         }     } } ```  By specifying fields as above, the repository owner will also be sent to subscribers of the event.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **targetUser** | **string**| The account the app is installed in.  This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
  **eventKey** | **string**| The key of the event, which corresponds to an event defined in the connect app descriptor.  | 

### Return type

 (empty response body)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

