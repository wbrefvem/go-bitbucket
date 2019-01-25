# \RefsApi

All URIs are relative to *https://api.bitbucket.org/2.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**RepositoriesUsernameRepoSlugRefsBranchesGet**](RefsApi.md#RepositoriesUsernameRepoSlugRefsBranchesGet) | **Get** /repositories/{username}/{repo_slug}/refs/branches | 
[**RepositoriesUsernameRepoSlugRefsBranchesNameDelete**](RefsApi.md#RepositoriesUsernameRepoSlugRefsBranchesNameDelete) | **Delete** /repositories/{username}/{repo_slug}/refs/branches/{name} | 
[**RepositoriesUsernameRepoSlugRefsBranchesNameGet**](RefsApi.md#RepositoriesUsernameRepoSlugRefsBranchesNameGet) | **Get** /repositories/{username}/{repo_slug}/refs/branches/{name} | 
[**RepositoriesUsernameRepoSlugRefsBranchesPost**](RefsApi.md#RepositoriesUsernameRepoSlugRefsBranchesPost) | **Post** /repositories/{username}/{repo_slug}/refs/branches | 
[**RepositoriesUsernameRepoSlugRefsGet**](RefsApi.md#RepositoriesUsernameRepoSlugRefsGet) | **Get** /repositories/{username}/{repo_slug}/refs | 
[**RepositoriesUsernameRepoSlugRefsTagsGet**](RefsApi.md#RepositoriesUsernameRepoSlugRefsTagsGet) | **Get** /repositories/{username}/{repo_slug}/refs/tags | 
[**RepositoriesUsernameRepoSlugRefsTagsNameDelete**](RefsApi.md#RepositoriesUsernameRepoSlugRefsTagsNameDelete) | **Delete** /repositories/{username}/{repo_slug}/refs/tags/{name} | 
[**RepositoriesUsernameRepoSlugRefsTagsNameGet**](RefsApi.md#RepositoriesUsernameRepoSlugRefsTagsNameGet) | **Get** /repositories/{username}/{repo_slug}/refs/tags/{name} | 
[**RepositoriesUsernameRepoSlugRefsTagsPost**](RefsApi.md#RepositoriesUsernameRepoSlugRefsTagsPost) | **Post** /repositories/{username}/{repo_slug}/refs/tags | 


# **RepositoriesUsernameRepoSlugRefsBranchesGet**
> PaginatedBranches RepositoriesUsernameRepoSlugRefsBranchesGet(ctx, username, repoSlug, optional)


Returns a list of all open branches within the specified repository. Results will be in the order the source control manager returns them.  ``` $ curl -s https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/refs/branches | jq . {   \"pagelen\": 10,   \"values\": [     {       \"heads\": [         {           \"hash\": \"f1a0933ce59e809f190602655e22ae6ec107c397\",           \"type\": \"commit\",           \"links\": {             \"self\": {               \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/f1a0933ce59e809f190602655e22ae6ec107c397\"             },             \"html\": {               \"href\": \"https://bitbucket.org/seanfarley/mercurial/commits/f1a0933ce59e809f190602655e22ae6ec107c397\"             }           }         }       ],       \"type\": \"named_branch\",       \"name\": \"default\",       \"links\": {         \"commits\": {           \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commits/default\"         },         \"self\": {           \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/refs/branches/default\"         },         \"html\": {           \"href\": \"https://bitbucket.org/seanfarley/mercurial/branch/default\"         }       },       \"target\": {         \"hash\": \"f1a0933ce59e809f190602655e22ae6ec107c397\",         \"repository\": {           \"links\": {             \"self\": {               \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial\"             },             \"html\": {               \"href\": \"https://bitbucket.org/seanfarley/mercurial\"             },             \"avatar\": {               \"href\": \"https://bitbucket.org/seanfarley/mercurial/avatar/32/\"             }           },           \"type\": \"repository\",           \"name\": \"mercurial\",           \"full_name\": \"seanfarley/mercurial\",           \"uuid\": \"{73dcbd61-e506-4fc1-9ecd-31be2b6d6031}\"         },         \"links\": {           \"self\": {             \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/f1a0933ce59e809f190602655e22ae6ec107c397\"           },           \"comments\": {             \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/f1a0933ce59e809f190602655e22ae6ec107c397/comments\"           },           \"patch\": {             \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/patch/f1a0933ce59e809f190602655e22ae6ec107c397\"           },           \"html\": {             \"href\": \"https://bitbucket.org/seanfarley/mercurial/commits/f1a0933ce59e809f190602655e22ae6ec107c397\"           },           \"diff\": {             \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/diff/f1a0933ce59e809f190602655e22ae6ec107c397\"           },           \"approve\": {             \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/f1a0933ce59e809f190602655e22ae6ec107c397/approve\"           },           \"statuses\": {             \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/f1a0933ce59e809f190602655e22ae6ec107c397/statuses\"           }         },         \"author\": {           \"raw\": \"Martin von Zweigbergk <martinvonz@google.com>\",           \"type\": \"author\",           \"user\": {             \"username\": \"martinvonz\",             \"nickname\": \"martinvonz\",             \"display_name\": \"Martin von Zweigbergk\",             \"type\": \"user\",             \"uuid\": \"{fdb0e657-3ade-4fad-a136-95f1ffe4a5ac}\",             \"links\": {               \"self\": {                 \"href\": \"https://api.bitbucket.org/2.0/users/martinvonz\"               },               \"html\": {                 \"href\": \"https://bitbucket.org/martinvonz/\"               },               \"avatar\": {                 \"href\": \"https://bitbucket.org/account/martinvonz/avatar/32/\"               }             }           }         },         \"parents\": [           {             \"hash\": \"5523aabb85c30ebc2b8e29aadcaf5e13fa92b375\",             \"type\": \"commit\",             \"links\": {               \"self\": {                 \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/5523aabb85c30ebc2b8e29aadcaf5e13fa92b375\"               },               \"html\": {                 \"href\": \"https://bitbucket.org/seanfarley/mercurial/commits/5523aabb85c30ebc2b8e29aadcaf5e13fa92b375\"               }             }           }         ],         \"date\": \"2018-02-01T18:44:49+00:00\",         \"message\": \"config: replace a for-else by any()\",         \"type\": \"commit\"       }     },     {       \"heads\": [         {           \"hash\": \"1d60ad093792706e1dc7a52b20942593f2c19655\",           \"type\": \"commit\",           \"links\": {             \"self\": {               \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/1d60ad093792706e1dc7a52b20942593f2c19655\"             },             \"html\": {               \"href\": \"https://bitbucket.org/seanfarley/mercurial/commits/1d60ad093792706e1dc7a52b20942593f2c19655\"             }           }         }       ],       \"type\": \"named_branch\",       \"name\": \"stable\",       \"links\": {         \"commits\": {           \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commits/stable\"         },         \"self\": {           \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/refs/branches/stable\"         },         \"html\": {           \"href\": \"https://bitbucket.org/seanfarley/mercurial/branch/stable\"         }       },       \"target\": {         \"hash\": \"1d60ad093792706e1dc7a52b20942593f2c19655\",         \"repository\": {           \"links\": {             \"self\": {               \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial\"             },             \"html\": {               \"href\": \"https://bitbucket.org/seanfarley/mercurial\"             },             \"avatar\": {               \"href\": \"https://bitbucket.org/seanfarley/mercurial/avatar/32/\"             }           },           \"type\": \"repository\",           \"name\": \"mercurial\",           \"full_name\": \"seanfarley/mercurial\",           \"uuid\": \"{73dcbd61-e506-4fc1-9ecd-31be2b6d6031}\"         },         \"links\": {           \"self\": {             \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/1d60ad093792706e1dc7a52b20942593f2c19655\"           },           \"comments\": {             \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/1d60ad093792706e1dc7a52b20942593f2c19655/comments\"           },           \"patch\": {             \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/patch/1d60ad093792706e1dc7a52b20942593f2c19655\"           },           \"html\": {             \"href\": \"https://bitbucket.org/seanfarley/mercurial/commits/1d60ad093792706e1dc7a52b20942593f2c19655\"           },           \"diff\": {             \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/diff/1d60ad093792706e1dc7a52b20942593f2c19655\"           },           \"approve\": {             \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/1d60ad093792706e1dc7a52b20942593f2c19655/approve\"           },           \"statuses\": {             \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/1d60ad093792706e1dc7a52b20942593f2c19655/statuses\"           }         },         \"author\": {           \"raw\": \"Augie Fackler <raf@durin42.com>\",           \"type\": \"author\",           \"user\": {             \"username\": \"durin42\",             \"nickname\": \"durin42\",             \"display_name\": \"Augie Fackler\",             \"type\": \"user\",             \"uuid\": \"{e07dc61f-bb05-4218-b43a-d991f26be65a}\",             \"links\": {               \"self\": {                 \"href\": \"https://api.bitbucket.org/2.0/users/durin42\"               },               \"html\": {                 \"href\": \"https://bitbucket.org/durin42/\"               },               \"avatar\": {                 \"href\": \"https://bitbucket.org/account/durin42/avatar/32/\"               }             }           }         },         \"parents\": [           {             \"hash\": \"56a0da11bde519d79168e890df4bcf0da62f0a7b\",             \"type\": \"commit\",             \"links\": {               \"self\": {                 \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/56a0da11bde519d79168e890df4bcf0da62f0a7b\"               },               \"html\": {                 \"href\": \"https://bitbucket.org/seanfarley/mercurial/commits/56a0da11bde519d79168e890df4bcf0da62f0a7b\"               }             }           }         ],         \"date\": \"2018-02-01T19:13:41+00:00\",         \"message\": \"Added signature for changeset d334afc585e2\",         \"type\": \"commit\"       }     }   ],   \"page\": 1,   \"size\": 2 } ```  Branches support [filtering and sorting](../../../../../meta/filtering) that can be used to search for specific branches. For instance, to find all branches that have \"stab\" in their name:  ``` curl -s https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/refs/branches -G --data-urlencode 'q=name ~ \"stab\"' ```  By default, results will be in the order the underlying source control system returns them and identical to the ordering one sees when running \"$ hg branches\" or \"$ git branch --list\". Note that this follows simple lexical ordering of the ref names.  This can be undesirable as it does apply any natural sorting semantics, meaning for instance that tags are sorted [\"v10\", \"v11\", \"v9\"] instead of [\"v9\", \"v10\", \"v11\"].  Sorting can be changed using the ?q= query parameter. When using ?q=name to explicitly sort on ref name, Bitbucket will apply natural sorting and interpret numerical values as numbers instead of strings.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**|  This can either be the username or the UUID of the user, surrounded by curly-braces, for example: &#x60;{user UUID}&#x60;.  | 
  **repoSlug** | **string**|  This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **string**|  This can either be the username or the UUID of the user, surrounded by curly-braces, for example: &#x60;{user UUID}&#x60;.  | 
 **repoSlug** | **string**|  This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 
 **q** | **string**|  Query string to narrow down the response as per [filtering and sorting](../../../../../../meta/filtering). | 
 **sort** | **string**|  Field by which the results should be sorted as per [filtering and sorting](../../../../../../meta/filtering). The &#x60;name&#x60; field is handled specially for branches in that, if specified as the sort field, it uses a natural sort order instead of the default lexicographical sort order. For example, it will return [&#39;branch1&#39;, &#39;branch2&#39;, &#39;branch10&#39;] instead of [&#39;branch1&#39;, &#39;branch10&#39;, &#39;branch2&#39;]. | 

### Return type

[**PaginatedBranches**](paginated_branches.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RepositoriesUsernameRepoSlugRefsBranchesNameDelete**
> RepositoriesUsernameRepoSlugRefsBranchesNameDelete(ctx, username, name, repoSlug)


Delete a branch in the specified repository.  The main branch is not allowed to be deleted and will return a 400 response.  For Git, the branch name should not include any prefixes (e.g. refs/heads). For Mercurial, this closes all open heads on the branch, sets the author of the commit to the authenticated caller, and changes the date to the datetime of the call.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
  **name** | **string**| The name of the branch. | 
  **repoSlug** | **string**| This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 

### Return type

 (empty response body)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RepositoriesUsernameRepoSlugRefsBranchesNameGet**
> Branch RepositoriesUsernameRepoSlugRefsBranchesNameGet(ctx, username, name, repoSlug)


Returns a branch object within the specified repository.  ``` $ curl -s https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/refs/branches/default | jq . {   \"heads\": [     {       \"hash\": \"f1a0933ce59e809f190602655e22ae6ec107c397\",       \"type\": \"commit\",       \"links\": {         \"self\": {           \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/f1a0933ce59e809f190602655e22ae6ec107c397\"         },         \"html\": {           \"href\": \"https://bitbucket.org/seanfarley/mercurial/commits/f1a0933ce59e809f190602655e22ae6ec107c397\"         }       }     }   ],   \"type\": \"named_branch\",   \"name\": \"default\",   \"links\": {     \"commits\": {       \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commits/default\"     },     \"self\": {       \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/refs/branches/default\"     },     \"html\": {       \"href\": \"https://bitbucket.org/seanfarley/mercurial/branch/default\"     }   },   \"target\": {     \"hash\": \"f1a0933ce59e809f190602655e22ae6ec107c397\",     \"repository\": {       \"links\": {         \"self\": {           \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial\"         },         \"html\": {           \"href\": \"https://bitbucket.org/seanfarley/mercurial\"         },         \"avatar\": {           \"href\": \"https://bitbucket.org/seanfarley/mercurial/avatar/32/\"         }       },       \"type\": \"repository\",       \"name\": \"mercurial\",       \"full_name\": \"seanfarley/mercurial\",       \"uuid\": \"{73dcbd61-e506-4fc1-9ecd-31be2b6d6031}\"     },     \"links\": {       \"self\": {         \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/f1a0933ce59e809f190602655e22ae6ec107c397\"       },       \"comments\": {         \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/f1a0933ce59e809f190602655e22ae6ec107c397/comments\"       },       \"patch\": {         \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/patch/f1a0933ce59e809f190602655e22ae6ec107c397\"       },       \"html\": {         \"href\": \"https://bitbucket.org/seanfarley/mercurial/commits/f1a0933ce59e809f190602655e22ae6ec107c397\"       },       \"diff\": {         \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/diff/f1a0933ce59e809f190602655e22ae6ec107c397\"       },       \"approve\": {         \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/f1a0933ce59e809f190602655e22ae6ec107c397/approve\"       },       \"statuses\": {         \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/f1a0933ce59e809f190602655e22ae6ec107c397/statuses\"       }     },     \"author\": {       \"raw\": \"Martin von Zweigbergk <martinvonz@google.com>\",       \"type\": \"author\",       \"user\": {         \"username\": \"martinvonz\",         \"nickname\": \"martinvonz\",         \"display_name\": \"Martin von Zweigbergk\",         \"type\": \"user\",         \"uuid\": \"{fdb0e657-3ade-4fad-a136-95f1ffe4a5ac}\",         \"links\": {           \"self\": {             \"href\": \"https://api.bitbucket.org/2.0/users/martinvonz\"           },           \"html\": {             \"href\": \"https://bitbucket.org/martinvonz/\"           },           \"avatar\": {             \"href\": \"https://bitbucket.org/account/martinvonz/avatar/32/\"           }         }       }     },     \"parents\": [       {         \"hash\": \"5523aabb85c30ebc2b8e29aadcaf5e13fa92b375\",         \"type\": \"commit\",         \"links\": {           \"self\": {             \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/mercurial/commit/5523aabb85c30ebc2b8e29aadcaf5e13fa92b375\"           },           \"html\": {             \"href\": \"https://bitbucket.org/seanfarley/mercurial/commits/5523aabb85c30ebc2b8e29aadcaf5e13fa92b375\"           }         }       }     ],     \"date\": \"2018-02-01T18:44:49+00:00\",     \"message\": \"config: replace a for-else by any()\",     \"type\": \"commit\"   } } ```  This call requires authentication. Private repositories require the caller to authenticate with an account that has appropriate authorization.  For Git, the branch name should not include any prefixes (e.g. refs/heads).  For Mercurial, the response will include an additional field that lists the open heads.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
  **name** | **string**| The name of the branch. | 
  **repoSlug** | **string**| This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 

### Return type

[**Branch**](branch.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RepositoriesUsernameRepoSlugRefsBranchesPost**
> Branch RepositoriesUsernameRepoSlugRefsBranchesPost(ctx, username, repoSlug)


Creates a new branch in the specified repository.  The payload of the POST should consist of a JSON document that contains the name of the tag and the target hash.  ``` curl https://api.bitbucket.org/2.0/repositories/seanfarley/hg/refs/branches \\ -s -u seanfarley -X POST -H \"Content-Type: application/json\" \\ -d '{     \"name\" : \"smf/create-feature\",     \"target\" : {         \"hash\" : \"default\",     } }' ```  This call requires authentication. Private repositories require the caller to authenticate with an account that has appropriate authorization.  For Git, the branch name should not include any prefixes (e.g. refs/heads). This endpoint does support using short hash prefixes for the commit hash, but it may return a 400 response if the provided prefix is ambiguous. Using a full commit hash is the preferred approach.  For Mercurial, the authenticated user making this call is the author of the new branch commit and the date is current datetime of the call.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
  **repoSlug** | **string**| This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 

### Return type

[**Branch**](branch.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RepositoriesUsernameRepoSlugRefsGet**
> PaginatedRefs RepositoriesUsernameRepoSlugRefsGet(ctx, username, repoSlug, optional)


Returns the branches and tags in the repository.  By default, results will be in the order the underlying source control system returns them and identical to the ordering one sees when running \"$ git show-ref\". Note that this follows simple lexical ordering of the ref names.  This can be undesirable as it does apply any natural sorting semantics, meaning for instance that refs are sorted [\"branch1\", \"branch10\", \"branch2\", \"v10\", \"v11\", \"v9\"] instead of [\"branch1\", \"branch2\", \"branch10\", \"v9\", \"v10\", \"v11\"].  Sorting can be changed using the ?sort= query parameter. When using ?sort=name to explicitly sort on ref name, Bitbucket will apply natural sorting and interpret numerical values as numbers instead of strings.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**|  This can either be the username or the UUID of the user, surrounded by curly-braces, for example: &#x60;{user UUID}&#x60;.  | 
  **repoSlug** | **string**|  This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **string**|  This can either be the username or the UUID of the user, surrounded by curly-braces, for example: &#x60;{user UUID}&#x60;.  | 
 **repoSlug** | **string**|  This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 
 **q** | **string**|  Query string to narrow down the response as per [filtering and sorting](../../../../../../meta/filtering). | 
 **sort** | **string**|  Field by which the results should be sorted as per [filtering and sorting](../../../../../../meta/filtering). The &#x60;name&#x60; field is handled specially for refs in that, if specified as the sort field, it uses a natural sort order instead of the default lexicographical sort order. For example, it will return [&#39;1.1&#39;, &#39;1.2&#39;, &#39;1.10&#39;] instead of [&#39;1.1&#39;, &#39;1.10&#39;, &#39;1.2&#39;]. | 

### Return type

[**PaginatedRefs**](paginated_refs.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RepositoriesUsernameRepoSlugRefsTagsGet**
> PaginatedTags RepositoriesUsernameRepoSlugRefsTagsGet(ctx, username, repoSlug, optional)


Returns the tags in the repository.  By default, results will be in the order the underlying source control system returns them and identical to the ordering one sees when running \"$ hg tags\" or \"$ git tag --list\". Note that this follows simple lexical ordering of the ref names.  This can be undesirable as it does apply any natural sorting semantics, meaning for instance that tags are sorted [\"v10\", \"v11\", \"v9\"] instead of [\"v9\", \"v10\", \"v11\"].  Sorting can be changed using the ?sort= query parameter. When using ?sort=name to explicitly sort on ref name, Bitbucket will apply natural sorting and interpret numerical values as numbers instead of strings.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**|  This can either be the username or the UUID of the user, surrounded by curly-braces, for example: &#x60;{user UUID}&#x60;.  | 
  **repoSlug** | **string**|  This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **string**|  This can either be the username or the UUID of the user, surrounded by curly-braces, for example: &#x60;{user UUID}&#x60;.  | 
 **repoSlug** | **string**|  This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 
 **q** | **string**|  Query string to narrow down the response as per [filtering and sorting](../../../../../../meta/filtering). | 
 **sort** | **string**|  Field by which the results should be sorted as per [filtering and sorting](../../../../../../meta/filtering). The &#x60;name&#x60; field is handled specially for tags in that, if specified as the sort field, it uses a natural sort order instead of the default lexicographical sort order. For example, it will return [&#39;1.1&#39;, &#39;1.2&#39;, &#39;1.10&#39;] instead of [&#39;1.1&#39;, &#39;1.10&#39;, &#39;1.2&#39;]. | 

### Return type

[**PaginatedTags**](paginated_tags.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RepositoriesUsernameRepoSlugRefsTagsNameDelete**
> RepositoriesUsernameRepoSlugRefsTagsNameDelete(ctx, username, name, repoSlug)


Delete a tag in the specified repository.  For Git, the tag name should not include any prefixes (e.g. refs/tags). For Mercurial, this adds a commit to the main branch that removes the specified tag.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
  **name** | **string**| The name of the tag. | 
  **repoSlug** | **string**| This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 

### Return type

 (empty response body)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RepositoriesUsernameRepoSlugRefsTagsNameGet**
> Tag RepositoriesUsernameRepoSlugRefsTagsNameGet(ctx, username, name, repoSlug)


Returns the specified tag.  ``` $ curl -s https://api.bitbucket.org/2.0/repositories/seanfarley/hg/refs/tags/3.8 -G | jq . {   \"name\": \"3.8\",   \"links\": {     \"commits\": {       \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/hg/commits/3.8\"     },     \"self\": {       \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/hg/refs/tags/3.8\"     },     \"html\": {       \"href\": \"https://bitbucket.org/seanfarley/hg/commits/tag/3.8\"     }   },   \"tagger\": {     \"raw\": \"Matt Mackall <mpm@selenic.com>\",     \"type\": \"author\",     \"user\": {       \"username\": \"mpmselenic\",       \"nickname\": \"mpmselenic\",       \"display_name\": \"Matt Mackall\",       \"type\": \"user\",       \"uuid\": \"{a4934530-db4c-419c-a478-9ab4964c2ee7}\",       \"links\": {         \"self\": {           \"href\": \"https://api.bitbucket.org/2.0/users/mpmselenic\"         },         \"html\": {           \"href\": \"https://bitbucket.org/mpmselenic/\"         },         \"avatar\": {           \"href\": \"https://bitbucket.org/account/mpmselenic/avatar/32/\"         }       }     }   },   \"date\": \"2016-05-01T18:52:25+00:00\",   \"message\": \"Added tag 3.8 for changeset f85de28eae32\",   \"type\": \"tag\",   \"target\": {     \"hash\": \"f85de28eae32e7d3064b1a1321309071bbaaa069\",     \"repository\": {       \"links\": {         \"self\": {           \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/hg\"         },         \"html\": {           \"href\": \"https://bitbucket.org/seanfarley/hg\"         },         \"avatar\": {           \"href\": \"https://bitbucket.org/seanfarley/hg/avatar/32/\"         }       },       \"type\": \"repository\",       \"name\": \"hg\",       \"full_name\": \"seanfarley/hg\",       \"uuid\": \"{c75687fb-e99d-4579-9087-190dbd406d30}\"     },     \"links\": {       \"self\": {         \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/hg/commit/f85de28eae32e7d3064b1a1321309071bbaaa069\"       },       \"comments\": {         \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/hg/commit/f85de28eae32e7d3064b1a1321309071bbaaa069/comments\"       },       \"patch\": {         \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/hg/patch/f85de28eae32e7d3064b1a1321309071bbaaa069\"       },       \"html\": {         \"href\": \"https://bitbucket.org/seanfarley/hg/commits/f85de28eae32e7d3064b1a1321309071bbaaa069\"       },       \"diff\": {         \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/hg/diff/f85de28eae32e7d3064b1a1321309071bbaaa069\"       },       \"approve\": {         \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/hg/commit/f85de28eae32e7d3064b1a1321309071bbaaa069/approve\"       },       \"statuses\": {         \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/hg/commit/f85de28eae32e7d3064b1a1321309071bbaaa069/statuses\"       }     },     \"author\": {       \"raw\": \"Sean Farley <sean@farley.io>\",       \"type\": \"author\",       \"user\": {         \"username\": \"seanfarley\",         \"nickname\": \"seanfarley\",         \"display_name\": \"Sean Farley\",         \"type\": \"user\",         \"uuid\": \"{a295f8a8-5876-4d43-89b5-3ad8c6c3c51d}\",         \"links\": {           \"self\": {             \"href\": \"https://api.bitbucket.org/2.0/users/seanfarley\"           },           \"html\": {             \"href\": \"https://bitbucket.org/seanfarley/\"           },           \"avatar\": {             \"href\": \"https://bitbucket.org/account/seanfarley/avatar/32/\"           }         }       }     },     \"parents\": [       {         \"hash\": \"9a98d0e5b07fc60887f9d3d34d9ac7d536f470d2\",         \"type\": \"commit\",         \"links\": {           \"self\": {             \"href\": \"https://api.bitbucket.org/2.0/repositories/seanfarley/hg/commit/9a98d0e5b07fc60887f9d3d34d9ac7d536f470d2\"           },           \"html\": {             \"href\": \"https://bitbucket.org/seanfarley/hg/commits/9a98d0e5b07fc60887f9d3d34d9ac7d536f470d2\"           }         }       }     ],     \"date\": \"2016-05-01T04:21:17+00:00\",     \"message\": \"debian: alphabetize build deps\",     \"type\": \"commit\"   } } ```

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
  **name** | **string**| The name of the tag. | 
  **repoSlug** | **string**| This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 

### Return type

[**Tag**](tag.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RepositoriesUsernameRepoSlugRefsTagsPost**
> Tag RepositoriesUsernameRepoSlugRefsTagsPost(ctx, username, repoSlug, body)


Creates a new tag in the specified repository.  The payload of the POST should consist of a JSON document that contains the name of the tag and the target hash.  ``` curl https://api.bitbucket.org/2.0/repositories/jdoe/myrepo/refs/tags \\ -s -u jdoe -X POST -H \"Content-Type: application/json\" \\ -d '{     \"name\" : \"new-tag-name\",     \"target\" : {         \"hash\" : \"a1b2c3d4e5f6\",     } }' ```  This endpoint does support using short hash prefixes for the commit hash, but it may return a 400 response if the provided prefix is ambiguous. Using a full commit hash is the preferred approach.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **username** | **string**| This can either be the username or the UUID of the account, surrounded by curly-braces, for example: &#x60;{account UUID}&#x60;. An account is either a team or user.  | 
  **repoSlug** | **string**| This can either be the repository slug or the UUID of the repository, surrounded by curly-braces, for example: &#x60;{repository UUID}&#x60;.  | 
  **body** | [**Tag**](Tag.md)|  | 

### Return type

[**Tag**](tag.md)

### Authorization

[api_key](../README.md#api_key), [basic](../README.md#basic), [oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

