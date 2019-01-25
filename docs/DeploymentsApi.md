# \DeploymentsApi

All URIs are relative to *https://api.bitbucket.org/2.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetDeploymentForRepository**](DeploymentsApi.md#GetDeploymentForRepository) | **Get** /repositories/{username}/{repo_slug}/deployments/{deployment_uuid} | 
[**GetDeploymentsForRepository**](DeploymentsApi.md#GetDeploymentsForRepository) | **Get** /repositories/{username}/{repo_slug}/deployments/ | 
[**GetEnvironmentForRepository**](DeploymentsApi.md#GetEnvironmentForRepository) | **Get** /repositories/{username}/{repo_slug}/environments/{environment_uuid} | 
[**GetEnvironmentsForRepository**](DeploymentsApi.md#GetEnvironmentsForRepository) | **Get** /repositories/{username}/{repo_slug}/environments/ | 
[**UpdateEnvironmentForRepository**](DeploymentsApi.md#UpdateEnvironmentForRepository) | **Post** /repositories/{username}/{repo_slug}/environments/{environment_uuid}/changes/ | 


# **GetDeploymentForRepository**
> Deployment GetDeploymentForRepository(ctx, username, repoSlug, deploymentUuid)


Retrieve a deployment

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| The account. | 
  **repoSlug** | **string**| The repository. | 
  **deploymentUuid** | **string**| The deployment UUID. | 

### Return type

[**Deployment**](deployment.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetDeploymentsForRepository**
> PaginatedDeployments GetDeploymentsForRepository(ctx, username, repoSlug)


Find deployments

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| The account. | 
  **repoSlug** | **string**| The repository. | 

### Return type

[**PaginatedDeployments**](paginated_deployments.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetEnvironmentForRepository**
> DeploymentEnvironment GetEnvironmentForRepository(ctx, username, repoSlug, environmentUuid)


Retrieve an environment

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| The account. | 
  **repoSlug** | **string**| The repository. | 
  **environmentUuid** | **string**| The environment UUID. | 

### Return type

[**DeploymentEnvironment**](deployment_environment.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetEnvironmentsForRepository**
> PaginatedEnvironments GetEnvironmentsForRepository(ctx, username, repoSlug)


Find environments

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| The account. | 
  **repoSlug** | **string**| The repository. | 

### Return type

[**PaginatedEnvironments**](paginated_environments.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateEnvironmentForRepository**
> UpdateEnvironmentForRepository(ctx, username, repoSlug, environmentUuid)


Update an environment

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| The account. | 
  **repoSlug** | **string**| The repository. | 
  **environmentUuid** | **string**| The environment UUID. | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

