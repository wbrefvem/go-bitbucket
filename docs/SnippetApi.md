# \SnippetApi

All URIs are relative to *https://api.bitbucket.org/2.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**SnippetsUsernameEncodedIdFilesPathGet**](SnippetApi.md#SnippetsUsernameEncodedIdFilesPathGet) | **Get** /snippets/{username}/{encoded_id}/files/{path} | 


# **SnippetsUsernameEncodedIdFilesPathGet**
> SnippetsUsernameEncodedIdFilesPathGet(ctx, username, path, encodedId)


Convenience resource for getting to a snippet's raw files without the need for first having to retrieve the snippet itself and having to pull out the versioned file links.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**|  | 
  **path** | **string**|  | 
  **encodedId** | **string**|  | 

### Return type

 (empty response body)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

