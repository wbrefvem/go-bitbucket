# \SearchApi

All URIs are relative to *https://api.bitbucket.org/2.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**SearchAccount**](SearchApi.md#SearchAccount) | **Get** /teams/{username}/search/code | Search for code in the repositories of the specified team
[**SearchAccount_0**](SearchApi.md#SearchAccount_0) | **Get** /users/{username}/search/code | Search for code in the repositories of the specified user


# **SearchAccount**
> SearchResultPage SearchAccount(ctx, username, searchQuery, optional)
Search for code in the repositories of the specified team

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| The account to search in; either the username or the UUID in curly braces | 
  **searchQuery** | **string**| The search query | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **string**| The account to search in; either the username or the UUID in curly braces | 
 **searchQuery** | **string**| The search query | 
 **page** | **int32**| Which page of the search results to retrieve | [default to 1]
 **pagelen** | **int32**| How many search results to retrieve per page | [default to 10]

### Return type

[**SearchResultPage**](search_result_page.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **SearchAccount_0**
> SearchResultPage SearchAccount_0(ctx, username, searchQuery, optional)
Search for code in the repositories of the specified user

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| The account to search in; either the username or the UUID in curly braces | 
  **searchQuery** | **string**| The search query | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **string**| The account to search in; either the username or the UUID in curly braces | 
 **searchQuery** | **string**| The search query | 
 **page** | **int32**| Which page of the search results to retrieve | [default to 1]
 **pagelen** | **int32**| How many search results to retrieve per page | [default to 10]

### Return type

[**SearchResultPage**](search_result_page.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

