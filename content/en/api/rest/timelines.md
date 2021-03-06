---
title: Timelines
menu:
  docs:
    parent: rest-api
    weight: 10
---

## GET /api/v1/timelines/home

Statuses from accounts the user follows.

Returns array of [Status]({{< relref "entities.md#status" >}})

### Resource information

{{< api_method_info auth="Yes" user="Yes" scope="read read:statuses" version="0.0.0" >}}

### Parameters

|Name|Description|Required|Default|
|----|-----------|:------:|:-----:|
| `max_id` | Return results older than ID | Optional ||
| `since_id` | Return results newer than ID | Optional ||
| `min_id` | Return results immediately newer than ID | Optional ||
| `limit` | Maximum number of results | Optional | 20 |


## GET /api/v1/conversations

Conversations for an account

Returns array of [Conversation]({{< relref "entities.md#conversation" >}})

### Resource information

{{< api_method_info auth="Yes" user="Yes" scope="read read:statuses" version="2.6.0" >}}

### Parameters

|Name|Description|Required|Default|
|----|-----------|:------:|:-----:|
| `max_id` | Return results older than ID | Optional ||
| `since_id` | Return results newer than ID | Optional ||
| `min_id` | Return results immediately newer than ID | Optional ||
| `limit` | Maximum number of results | Optional | 20 |

### Pagination

{{< api_dynamic_pagination >}}

## GET /api/v1/timelines/public

Public statuses known to the server.

Returns array of [Status]({{< relref "entities.md#status" >}})

### Resource information

{{< api_method_info auth="No" user="No" scope="read read:statuses" version="0.0.0" >}}

### Parameters

|Name|Description|Required|Default|
|----|-----------|:------:|:-----:|
| `local` | Only local statuses | Optional |false|
| `only_media` | Only statuses with media attachments | Optional |false|
| `max_id` | Return results older than ID | Optional ||
| `since_id` | Return results newer than ID | Optional ||
| `min_id` | Return results immediately newer than ID | Optional ||
| `limit` | Maximum number of results | Optional | 20 |

### Pagination

{{< api_dynamic_pagination >}}

## GET /api/v1/timelines/tag/:hashtag

Public statuses known to the server marked with a given hashtag.

Returns array of [Status]({{< relref "entities.md#status" >}})

### Resource information

{{< api_method_info auth="No" user="No" scope="read read:statuses" version="0.0.0" >}}

### Parameters

|Name|Description|Required|Default|
|----|-----------|:------:|:-----:|
| `local` | Only local statuses | Optional |false|
| `only_media` | Only statuses with media attachments | Optional |false|
| `max_id` | Return results older than ID | Optional ||
| `since_id` | Return results newer than ID | Optional ||
| `min_id` | Return results immediately newer than ID | Optional ||
| `limit` | Maximum number of results | Optional | 20 |

### Pagination

{{< api_dynamic_pagination >}}

## GET /api/v1/timelines/list/:list_id

Statuses from accounts on a given list.

Returns array of [Status]({{< relref "entities.md#status" >}})

### Resource information

{{< api_method_info auth="Yes" user="Yes" scope="read read:statuses" version="2.1.0" >}}

### Parameters

|Name|Description|Required|Default|
|----|-----------|:------:|:-----:|
| `max_id` | Return results older than ID | Optional ||
| `since_id` | Return results newer than ID | Optional ||
| `min_id` | Return results immediately newer than ID | Optional ||
| `limit` | Maximum number of results | Optional | 20 |

### Pagination

{{< api_dynamic_pagination >}}
