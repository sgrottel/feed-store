# Feed Store API Definition
The HTTP API offers the following routes:
* [`GET /feed`](#get-feed)
    * Gets a list of feeds in the store
* [`GET /feed/{ID}`](#get-feedid)
    * Gets meta data and entries of one specific feed
* [`GET /feed/{ID}/rss`](#get-feedidrss)
    * Gets meta data ane entries of one specific feed in RSS format
* [`POST /feed`](#post-feed)
    * Creates a new feed
* [`PATCH /feed/{ID}`](#patch-feedid)
    * Updates meta data of one specific feed
* [`POST /feed/{ID}`](#post-feedid)
    * Creates or overwrites entries in one specific feed
* [`DELETE /feed/{ID}`](#delete-feedid)
    * Deletes one specific feed and all entries
* [`DELETE /feed/{ID}/entry/{EID}`](#delete-feedidentryeid)
    * Deletes one specific entry from one specific feed
* [`OPTIONS /feed`](#options-feed)
    * Enable CORS access if configured accordingly
* [`OPTIONS /feed/{ID}`](#options-feedid)
    * Enable CORS access if configured accordingly
* [`OPTIONS /feed/{ID}/rss`](#options-feedidrss)
    * Enable CORS access if configured accordingly
* [`OPTIONS /feed/{ID}/entry/{EID}`](#options-feedidentryeid)
    * Enable CORS access if configured accordingly

Additional notes on: [Authorization and Authentication](#authentication-and-authentication)


## `GET /feed`
Gets a list of feeds in the store.

TODO


## `GET /feed/{ID}`
Gets meta data and entries of one specific feed.

TODO


## `GET /feed/{ID}/rss`
Gets meta data ane entries of one specific feed in RSS format.

TODO


## `POST /feed`
Creates a new feed.

TODO


## `PATCH /feed/{ID}`
Updates meta data of one specific feed.

TODO


## `POST /feed/{ID}`
Creates or overwrites entries in one specific feed.

TODO


## `DELETE /feed/{ID}`
Deletes one specific feed and all entries.

TODO


## `DELETE /feed/{ID}/entry/{EID}`
Deletes one specific entry from one specific feed.

TODO


## `OPTIONS /feed`
If the backend is implemented and configured to allow CORS this route should return `200` with empty body.


## `OPTIONS /feed/{ID}`
If the backend is implemented and configured to allow CORS this route should return `200` with empty body.


## `OPTIONS /feed/{ID}/rss`
If the backend is implemented and configured to allow CORS this route should return `200` with empty body.


## `OPTIONS /feed/{ID}/entry/{EID}`
If the backend is implemented and configured to allow CORS this route should return `200` with empty body.


## Authentication and Authentication
Authentication and authorization are handled in addition to this API definition.
Unless otherwise stated, e.g. cf. [`GET /feed/{ID}/rss`](#get-feedidrss), the authentication is handled via HTTP header fields.
The recommendation for any implementation is to use `Authorization: Bearer <token>`.
Authorization is also implementation dependent and beyond the scope of this API definition.
