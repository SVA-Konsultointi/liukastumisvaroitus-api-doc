---
title: API Reference

toc_footers:
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the documentation for api.liukastumisvaroitus.fi! You can use our endpoints to access
the warnings given by our system.

# Authentication

Our API has no authentication, you are free to use it straight away. Please be mindful of the
load your application puts on our server to keep it running smoothly for everyone!

# URL parameters

> Example parameters

```text
http://api.liukastumisvaroitus.fi/api/v1/warnings?filter=city:Helsinki
http://api.liukastumisvaroitus.fi/api/v1/warnings?order=created_at:desc
```

Parameter | Description
--------- | -----------
filter | Filters resources by field and value
order | Orders resources according to the field and direction given

# Warnings

## Get all warnings

> Example response

```json
[
  {
    "id":1,
    "city":"Helsinki",
    "created_at":"2013-12-01 06:49:00",
    "updated_at":"2013-12-01 06:49:00"
  },
  {
    "id":2,
    "city":"Helsinki",
    "created_at":"2013-12-11 10:37:00",
    "updated_at":"2013-12-11 10:37:00"
  }
]
```

This endpoint retrieves all warnings.

### HTTP request

`POST http://api.liukastumisvaroitus.fi/api/v1/warnings`

## Get a specific warning

> Example response

```json
{
    "id":1,
    "city":"Helsinki",
    "created_at":"2013-12-01 06:49:00",
    "updated_at":"2013-12-01 06:49:00"
}
```

This endpoint retrieves a specific warning.

### HTTP request

`GET http://api.liukastumisvaroitus.fi/api/v1/warnings/<ID>`

### Query parameters

Parameter | Description
--------- | -----------
ID | The ID of the warning to retrieve
