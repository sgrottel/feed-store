# DefaultApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteFeed**](DefaultApi.md#deleteFeed) | **DELETE** /feed/{fid} | Deletes a feed |
| [**deleteFeedEntry**](DefaultApi.md#deleteFeedEntry) | **DELETE** /feed/{fid}/entry/{eid} | Deletes a specific entry |
| [**getFeed**](DefaultApi.md#getFeed) | **GET** /feed/{fid} | Get a feed object |
| [**getFeedAsRss**](DefaultApi.md#getFeedAsRss) | **GET** /feed/{fid}/rss | Get feed and entries as RSS/XML document |
| [**getFeedEntries**](DefaultApi.md#getFeedEntries) | **GET** /feed/{fid}/entry | Gets the entries of the feed sorted by date (newest to oldest). |
| [**getFeedEntry**](DefaultApi.md#getFeedEntry) | **GET** /feed/{fid}/entry/{eid} | Gets a specific entry |
| [**getFeeds**](DefaultApi.md#getFeeds) | **GET** /feed | Get list of all feeds |
| [**patchFeed**](DefaultApi.md#patchFeed) | **PATCH** /feed/{fid} | Change a feed meta data |
| [**patchFeedEntry**](DefaultApi.md#patchFeedEntry) | **PATCH** /feed/{fid}/entry/{eid} | Updates a specific entry |
| [**postFeed**](DefaultApi.md#postFeed) | **POST** /feed | Create new feed |
| [**postFeedEntries**](DefaultApi.md#postFeedEntries) | **POST** /feed/{fid}/entry | posts entries into the feed |


<a name="deleteFeed"></a>
# **deleteFeed**
> deleteFeed(fid)

Deletes a feed

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **fid** | **String**| Id of a specific feed | [default to null] |

### Return type

null (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="deleteFeedEntry"></a>
# **deleteFeedEntry**
> deleteFeedEntry(fid, eid)

Deletes a specific entry

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **fid** | **String**| Id of a specific feed | [default to null] |
| **eid** | **String**| Id of a specific entry | [default to null] |

### Return type

null (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="getFeed"></a>
# **getFeed**
> feedMetaDataWithId getFeed(fid)

Get a feed object

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **fid** | **String**| Id of a specific feed | [default to null] |

### Return type

[**feedMetaDataWithId**](../Models/feedMetaDataWithId.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getFeedAsRss"></a>
# **getFeedAsRss**
> String getFeedAsRss(fid, limit)

Get feed and entries as RSS/XML document

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **fid** | **String**| Id of a specific feed | [default to null] |
| **limit** | **Integer**| Limits the number of elements in the returned answer Used together with &#x60;minFeedId&#x60; or &#x60;maxDate&#x60; for paginated results.  | [optional] [default to null] |

### Return type

**String**

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/xml

<a name="getFeedEntries"></a>
# **getFeedEntries**
> List getFeedEntries(fid, limit, max-date)

Gets the entries of the feed sorted by date (newest to oldest).

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **fid** | **String**| Id of a specific feed | [default to null] |
| **limit** | **Integer**| Limits the number of elements in the returned answer Used together with &#x60;minFeedId&#x60; or &#x60;maxDate&#x60; for paginated results.  | [optional] [default to null] |
| **max-date** | **Date**| Only returns entries with date values equal or older to the specified value. Used together with &#x60;limit&#x60; for paginated results.  | [optional] [default to null] |

### Return type

[**List**](../Models/feedEntryWithId.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getFeedEntry"></a>
# **getFeedEntry**
> feedEntryWithId getFeedEntry(fid, eid)

Gets a specific entry

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **fid** | **String**| Id of a specific feed | [default to null] |
| **eid** | **String**| Id of a specific entry | [default to null] |

### Return type

[**feedEntryWithId**](../Models/feedEntryWithId.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getFeeds"></a>
# **getFeeds**
> List getFeeds(limit, min-feed-id, link-match)

Get list of all feeds

    Lists all stored feeds, sorted by their feed id (ascending).

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **limit** | **Integer**| Limits the number of elements in the returned answer Used together with &#x60;minFeedId&#x60; or &#x60;maxDate&#x60; for paginated results.  | [optional] [default to null] |
| **min-feed-id** | **String**| Only returns feeds with feed id values equal or larger to the specified value. Used together with &#x60;limit&#x60; for paginated results.  | [optional] [default to null] |
| **link-match** | **String**| Limits the return list to elements which links matching the specified value.  | [optional] [default to null] |

### Return type

[**List**](../Models/feedMetaDataWithId.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="patchFeed"></a>
# **patchFeed**
> feedMetaDataWithId patchFeed(fid, feedMetaData)

Change a feed meta data

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **fid** | **String**| Id of a specific feed | [default to null] |
| **feedMetaData** | [**feedMetaData**](../Models/feedMetaData.md)|  | [optional] |

### Return type

[**feedMetaDataWithId**](../Models/feedMetaDataWithId.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="patchFeedEntry"></a>
# **patchFeedEntry**
> feedEntryWithId patchFeedEntry(fid, eid, feedEntry)

Updates a specific entry

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **fid** | **String**| Id of a specific feed | [default to null] |
| **eid** | **String**| Id of a specific entry | [default to null] |
| **feedEntry** | [**feedEntry**](../Models/feedEntry.md)|  | [optional] |

### Return type

[**feedEntryWithId**](../Models/feedEntryWithId.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="postFeed"></a>
# **postFeed**
> feedMetaDataWithId postFeed(feedMetaData)

Create new feed

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **feedMetaData** | [**feedMetaData**](../Models/feedMetaData.md)|  | [optional] |

### Return type

[**feedMetaDataWithId**](../Models/feedMetaDataWithId.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="postFeedEntries"></a>
# **postFeedEntries**
> List postFeedEntries(fid, feedEntry)

posts entries into the feed

    If an entry to be posted has a non-empty guid field: - if an entry already stored in the feed has the same non-empty guid value, the content of that entry is updated. - if no entry with that non-empty guid value exists, the entry is added to the feed. 

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **fid** | **String**| Id of a specific feed | [default to null] |
| **feedEntry** | [**List**](../Models/feedEntry.md)|  | [optional] |

### Return type

[**List**](../Models/feedEntryWithId.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

