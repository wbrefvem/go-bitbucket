# \DefaultApi

All URIs are relative to *https://api.bitbucket.org/2.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**RepositoriesUsernameRepoSlugDiffstatSpecGet**](DefaultApi.md#RepositoriesUsernameRepoSlugDiffstatSpecGet) | **Get** /repositories/{username}/{repo_slug}/diffstat/{spec} | 
[**RepositoriesUsernameRepoSlugIssuesExportPost**](DefaultApi.md#RepositoriesUsernameRepoSlugIssuesExportPost) | **Post** /repositories/{username}/{repo_slug}/issues/export | 
[**RepositoriesUsernameRepoSlugIssuesExportRepoNameIssuesTaskIdZipGet**](DefaultApi.md#RepositoriesUsernameRepoSlugIssuesExportRepoNameIssuesTaskIdZipGet) | **Get** /repositories/{username}/{repo_slug}/issues/export/{repo_name}-issues-{task_id}.zip | 
[**RepositoriesUsernameRepoSlugIssuesImportGet**](DefaultApi.md#RepositoriesUsernameRepoSlugIssuesImportGet) | **Get** /repositories/{username}/{repo_slug}/issues/import | 
[**RepositoriesUsernameRepoSlugIssuesImportPost**](DefaultApi.md#RepositoriesUsernameRepoSlugIssuesImportPost) | **Post** /repositories/{username}/{repo_slug}/issues/import | 
[**RepositoriesUsernameRepoSlugPropertiesAppKeyPropertyNameDelete**](DefaultApi.md#RepositoriesUsernameRepoSlugPropertiesAppKeyPropertyNameDelete) | **Delete** /repositories/{username}/{repo_slug}/properties/{app_key}/{property_name} | 
[**RepositoriesUsernameRepoSlugPropertiesAppKeyPropertyNameGet**](DefaultApi.md#RepositoriesUsernameRepoSlugPropertiesAppKeyPropertyNameGet) | **Get** /repositories/{username}/{repo_slug}/properties/{app_key}/{property_name} | 
[**RepositoriesUsernameRepoSlugPropertiesAppKeyPropertyNamePut**](DefaultApi.md#RepositoriesUsernameRepoSlugPropertiesAppKeyPropertyNamePut) | **Put** /repositories/{username}/{repo_slug}/properties/{app_key}/{property_name} | 
[**TeamsUsernamePermissionsGet**](DefaultApi.md#TeamsUsernamePermissionsGet) | **Get** /teams/{username}/permissions | 
[**TeamsUsernamePermissionsRepositoriesGet**](DefaultApi.md#TeamsUsernamePermissionsRepositoriesGet) | **Get** /teams/{username}/permissions/repositories | 
[**UserPermissionsTeamsGet**](DefaultApi.md#UserPermissionsTeamsGet) | **Get** /user/permissions/teams | 


# **RepositoriesUsernameRepoSlugDiffstatSpecGet**
> PaginatedDiffstats RepositoriesUsernameRepoSlugDiffstatSpecGet(ctx, username, repoSlug, spec, optional)


Returns the diff stat for the specified commit.  Diff stat responses contain a record for every path modified by the commit and lists the number of lines added and removed for each file.   Example: ``` curl https://api.bitbucket.org/2.0/repositories/bitbucket/geordi/diffstat/d222fa2..e174964 {     \"pagelen\": 500,     \"values\": [         {             \"type\": \"diffstat\",             \"status\": \"modified\",             \"lines_removed\": 1,             \"lines_added\": 2,             \"old\": {                 \"path\": \"setup.py\",                 \"type\": \"commit_file\",                 \"links\": {                     \"self\": {                         \"href\": \"https://api.bitbucket.org/2.0/repositories/bitbucket/geordi/src/e1749643d655d7c7014001a6c0f58abaf42ad850/setup.py\"                     }                 }             },             \"new\": {                 \"path\": \"setup.py\",                 \"type\": \"commit_file\",                 \"links\": {                     \"self\": {                         \"href\": \"https://api.bitbucket.org/2.0/repositories/bitbucket/geordi/src/d222fa235229c55dad20b190b0b571adf737d5a6/setup.py\"                     }                 }             }         }     ],     \"page\": 1,     \"size\": 1 } ```

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
  **repoSlug** | **string**| This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 
  **spec** | **string**| A commit SHA (e.g. &#x60;3a8b42&#x60;) or a commit range using double dot notation (e.g. &#x60;3a8b42..9ff173&#x60;).  | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **string**| This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
 **repoSlug** | **string**| This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 
 **spec** | **string**| A commit SHA (e.g. &#x60;3a8b42&#x60;) or a commit range using double dot notation (e.g. &#x60;3a8b42..9ff173&#x60;).  | 
 **ignoreWhitespace** | **bool**| Generate diffs that ignore whitespace | 

### Return type

[**PaginatedDiffstats**](paginated_diffstats.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RepositoriesUsernameRepoSlugIssuesExportPost**
> RepositoriesUsernameRepoSlugIssuesExportPost(ctx, username, repoSlug)


A POST request to this endpoint initiates a new background celery task that archives the repo's issues.  For example, you can run:  curl -u <username> -X POST http://api.bitbucket.org/2.0/repositories/<owner_username>/<repo_slug>/ issues/export  When the job has been accepted, it will return a 202 (Accepted) along with a unique url to this job in the 'Location' response header. This url is the endpoint for where the user can obtain their zip files.\"

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
  **repoSlug** | **string**| This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 

### Return type

 (empty response body)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RepositoriesUsernameRepoSlugIssuesExportRepoNameIssuesTaskIdZipGet**
> IssueJobStatus RepositoriesUsernameRepoSlugIssuesExportRepoNameIssuesTaskIdZipGet(ctx, username, repoSlug, repoName, taskId)


This endpoint is used to poll for the progress of an issue export job and return the zip file after the job is complete. As long as the job is running, this will return a 200 response with in the response body a description of the current status.  After the job has been scheduled, but before it starts executing, this endpoint's response is:  {  \"type\": \"issue_job_status\",  \"status\": \"ACCEPTED\",  \"phase\": \"Initializing\",  \"total\": 0,  \"count\": 0,  \"pct\": 0 }   Then once it starts running, it becomes:  {  \"type\": \"issue_job_status\",  \"status\": \"STARTED\",  \"phase\": \"Attachments\",  \"total\": 15,  \"count\": 11,  \"pct\": 73 }  Once the job has successfully completed, it returns a stream of the zip file.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
  **repoSlug** | **string**| This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 
  **repoName** | **string**| The name of the repo | 
  **taskId** | **string**| The ID of the export task | 

### Return type

[**IssueJobStatus**](issue_job_status.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RepositoriesUsernameRepoSlugIssuesImportGet**
> IssueJobStatus RepositoriesUsernameRepoSlugIssuesImportGet(ctx, username, repoSlug)


When using GET, this endpoint reports the status of the current import task. Request example:  ``` $ curl -u <username> -X GET https://api.bitbucket.org/2.0/repositories/<owner_username>/<repo_slug>/issues/import ```  After the job has been scheduled, but before it starts executing, this endpoint's response is:  ``` < HTTP/1.1 202 Accepted {     \"type\": \"issue_job_status\",     \"status\": \"PENDING\",     \"phase\": \"Attachments\",     \"total\": 15,     \"count\": 0,     \"percent\": 0 } ```  Once it starts running, it is a 202 response with status STARTED and progress filled.  After it is finished, it becomes a 200 response with status SUCCESS or FAILURE.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
  **repoSlug** | **string**| This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 

### Return type

[**IssueJobStatus**](issue_job_status.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RepositoriesUsernameRepoSlugIssuesImportPost**
> IssueJobStatus RepositoriesUsernameRepoSlugIssuesImportPost(ctx, username, repoSlug)


A POST request to this endpoint will import the zip file given by the archive parameter into the repository. All existing issues will be deleted and replaced by the contents of the imported zip file.  Imports are done through a multipart/form-data POST. There is one valid and required form field, with the name \"archive,\" which needs to be a file field:  ``` $ curl -u <username> -X POST -F archive=@/path/to/file.zip https://api.bitbucket.org/2.0/repositories/<owner_username>/<repo_slug>/issues/import ```  When the import job is accepted, here is example output:  ``` < HTTP/1.1 202 Accepted  {     \"type\": \"issue_job_status\",     \"status\": \"ACCEPTED\",     \"phase\": \"Attachments\",     \"total\": 15,     \"count\": 0,     \"percent\": 0 } ```

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
  **repoSlug** | **string**| This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 

### Return type

[**IssueJobStatus**](issue_job_status.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RepositoriesUsernameRepoSlugPropertiesAppKeyPropertyNameDelete**
> RepositoriesUsernameRepoSlugPropertiesAppKeyPropertyNameDelete(ctx, )


### Required Parameters
This endpoint does not need any parameter.

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RepositoriesUsernameRepoSlugPropertiesAppKeyPropertyNameGet**
> RepositoriesUsernameRepoSlugPropertiesAppKeyPropertyNameGet(ctx, )


### Required Parameters
This endpoint does not need any parameter.

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RepositoriesUsernameRepoSlugPropertiesAppKeyPropertyNamePut**
> RepositoriesUsernameRepoSlugPropertiesAppKeyPropertyNamePut(ctx, )


### Required Parameters
This endpoint does not need any parameter.

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **TeamsUsernamePermissionsGet**
> PaginatedTeamPermissions TeamsUsernamePermissionsGet(ctx, username, optional)


Returns an object for each team permission a user on the team has.  Permissions returned are effective permissions — if a user is a member of multiple groups with distinct roles, only the highest level is returned.  Permissions can be:  * `admin` * `collaborator`  Only users with admin permission for the team may access this resource.  Example:  ``` $ curl https://api.bitbucket.org/2.0/teams/atlassian_tutorial/permissions  {   \"pagelen\": 10,   \"values\": [     {       \"permission\": \"admin\",       \"type\": \"team_permission\",       \"user\": {         \"type\": \"user\",         \"username\": \"evzijst\",         \"nickname\": \"evzijst\",         \"display_name\": \"Erik van Zijst\",         \"uuid\": \"{d301aafa-d676-4ee0-88be-962be7417567}\"       },       \"team\": {         \"username\": \"bitbucket\",         \"display_name\": \"Atlassian Bitbucket\",         \"uuid\": \"{4cc6108a-a241-4db0-96a5-64347ac04f87}\"       }     },     {       \"permission\": \"collaborator\",       \"type\": \"team_permission\",       \"user\": {         \"type\": \"user\",         \"username\": \"seanaty\",         \"nickname\": \"seanaty\",         \"display_name\": \"Sean Conaty\",         \"uuid\": \"{504c3b62-8120-4f0c-a7bc-87800b9d6f70}\"       },       \"team\": {         \"username\": \"bitbucket\",         \"display_name\": \"Atlassian Bitbucket\",         \"uuid\": \"{4cc6108a-a241-4db0-96a5-64347ac04f87}\"       }     }   ],   \"page\": 1,   \"size\": 2 } ```  Results may be further [filtered or sorted](../../../meta/filtering) by team, user, or permission by adding the following query string parameters:  * `q=user.username=\"evzijst\"` or `q=permission=\"admin\"` * `sort=team.display_name`  Note that the query parameter values need to be URL escaped so that `=` would become `%3D`.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **string**| This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
 **q** | **string**|  Query string to narrow down the response as per [filtering and sorting](../../../meta/filtering). | 
 **sort** | **string**|  Name of a response property sort the result by as per [filtering and sorting](../../../meta/filtering#query-sort).  | 

### Return type

[**PaginatedTeamPermissions**](paginated_team_permissions.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **TeamsUsernamePermissionsRepositoriesGet**
> PaginatedRepositoryPermissions TeamsUsernamePermissionsRepositoriesGet(ctx, username, optional)


Returns an object for each repository permission for all of a team’s repositories.  If the username URL parameter refers to a user account instead of a team account, an object containing the repository permissions of all the username's repositories will be returned.  Permissions returned are effective permissions — the highest level of permission the user has. This does not include public repositories that users are not granted any specific permission in, and does not distinguish between direct and indirect privileges.  Only users with admin permission for the team may access this resource.  Permissions can be:  * `admin` * `write` * `read`  Example:  ``` $ curl https://api.bitbucket.org/2.0/teams/atlassian_tutorial/permissions/repositories  {   \"pagelen\": 10,   \"values\": [     {       \"type\": \"repository_permission\",       \"user\": {         \"type\": \"user\",         \"username\": \"evzijst\",         \"display_name\": \"Erik van Zijst\",         \"uuid\": \"{d301aafa-d676-4ee0-88be-962be7417567}\"       },       \"repository\": {         \"type\": \"repository\",         \"name\": \"geordi\",         \"full_name\": \"bitbucket/geordi\",         \"uuid\": \"{85d08b4e-571d-44e9-a507-fa476535aa98}\"       },       \"permission\": \"admin\"     },     {       \"type\": \"repository_permission\",       \"user\": {         \"type\": \"user\",         \"username\": \"seanaty\",         \"display_name\": \"Sean Conaty\",         \"uuid\": \"{504c3b62-8120-4f0c-a7bc-87800b9d6f70}\"       },       \"repository\": {         \"type\": \"repository\",         \"name\": \"geordi\",         \"full_name\": \"bitbucket/geordi\",         \"uuid\": \"{85d08b4e-571d-44e9-a507-fa476535aa98}\"       },       \"permission\": \"write\"     }   ],   \"page\": 1,   \"size\": 2 } ```  Results may be further [filtered or sorted](../../../../meta/filtering) by repository, user, or permission by adding the following query string parameters:  * `q=repository.name=\"geordi\"` or `q=permission>\"read\"` * `sort=user.display_name`  Note that the query parameter values need to be URL escaped so that `=` would become `%3D`.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **string**| This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
 **q** | **string**|  Query string to narrow down the response as per [filtering and sorting](../../../../meta/filtering). | 
 **sort** | **string**|  Name of a response property sort the result by as per [filtering and sorting](../../../../meta/filtering#query-sort).  | 

### Return type

[**PaginatedRepositoryPermissions**](paginated_repository_permissions.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UserPermissionsTeamsGet**
> PaginatedTeamPermissions UserPermissionsTeamsGet(ctx, optional)


Returns an object for each team the caller is a member of, and their effective role — the highest level of privilege the caller has. If a user is a member of multiple groups with distinct roles, only the highest level is returned.  Permissions can be:  * `admin` * `collaborator`  Example:  ``` $ curl https://api.bitbucket.org/2.0/user/permissions/teams  {   \"pagelen\": 10,   \"values\": [     {       \"permission\": \"admin\",       \"type\": \"team_permission\",       \"user\": {         \"type\": \"user\",         \"username\": \"evzijst\",         \"nickname\": \"evzijst\",         \"display_name\": \"Erik van Zijst\",         \"uuid\": \"{d301aafa-d676-4ee0-88be-962be7417567}\"       },       \"team\": {         \"username\": \"bitbucket\",         \"display_name\": \"Atlassian Bitbucket\",         \"uuid\": \"{4cc6108a-a241-4db0-96a5-64347ac04f87}\"       }     }   ],   \"page\": 1,   \"size\": 1 } ```  Results may be further [filtered or sorted](../../../meta/filtering) by team or permission by adding the following query string parameters:  * `q=team.username=\"bitbucket\"` or `q=permission=\"admin\"` * `sort=team.display_name`  Note that the query parameter values need to be URL escaped so that `=` would become `%3D`.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **q** | **string**|  Query string to narrow down the response as per [filtering and sorting](../../../meta/filtering). | 
 **sort** | **string**|  Name of a response property sort the result by as per [filtering and sorting](../../../meta/filtering#query-sort).  | 

### Return type

[**PaginatedTeamPermissions**](paginated_team_permissions.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

