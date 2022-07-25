# Documentation for Feed Store

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *http://localhost*

| Class | Method | HTTP request | Description |
|------------ | ------------- | ------------- | -------------|
| *DefaultApi* | [**deleteFeed**](Apis/DefaultApi.md#deletefeed) | **DELETE** /feed/{fid} | Deletes a feed |
*DefaultApi* | [**deleteFeedEntry**](Apis/DefaultApi.md#deletefeedentry) | **DELETE** /feed/{fid}/entry/{eid} | Deletes a specific entry |
*DefaultApi* | [**getFeed**](Apis/DefaultApi.md#getfeed) | **GET** /feed/{fid} | Get a feed object |
*DefaultApi* | [**getFeedAsRss**](Apis/DefaultApi.md#getfeedasrss) | **GET** /feed/{fid}/rss | Get feed and entries as RSS/XML document |
*DefaultApi* | [**getFeedEntries**](Apis/DefaultApi.md#getfeedentries) | **GET** /feed/{fid}/entry | Gets the entries of the feed sorted by date (newest to oldest). |
*DefaultApi* | [**getFeedEntry**](Apis/DefaultApi.md#getfeedentry) | **GET** /feed/{fid}/entry/{eid} | Gets a specific entry |
*DefaultApi* | [**getFeeds**](Apis/DefaultApi.md#getfeeds) | **GET** /feed | Get list of all feeds |
*DefaultApi* | [**patchFeed**](Apis/DefaultApi.md#patchfeed) | **PATCH** /feed/{fid} | Change a feed meta data |
*DefaultApi* | [**patchFeedEntry**](Apis/DefaultApi.md#patchfeedentry) | **PATCH** /feed/{fid}/entry/{eid} | Updates a specific entry |
*DefaultApi* | [**postFeed**](Apis/DefaultApi.md#postfeed) | **POST** /feed | Create new feed |
*DefaultApi* | [**postFeedEntries**](Apis/DefaultApi.md#postfeedentries) | **POST** /feed/{fid}/entry | posts entries into the feed |


<a name="documentation-for-models"></a>
## Documentation for Models

 - [feedEntry](./Models/feedEntry.md)
 - [feedEntryWithId](./Models/feedEntryWithId.md)
 - [feedMetaData](./Models/feedMetaData.md)
 - [feedMetaDataWithId](./Models/feedMetaDataWithId.md)


<a name="documentation-for-authorization"></a>
## Documentation for Authorization

<a name="BasicAuth"></a>
### BasicAuth

- **Type**: HTTP basic authentication

<a name="BearerAuth"></a>
### BearerAuth

- **Type**: HTTP basic authentication

