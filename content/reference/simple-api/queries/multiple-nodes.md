---
alias: pa2aothaec
path: /docs/reference/simple-api/multiple-nodes
layout: REFERENCE
shorttitle: Querying multiple nodes
description: Query all nodes of a type and combine filter, order and pagination query arguments to exactly define what data you want to fetch.
simple_relay_twin: uu4ohnaih7
tags:
  - simple-api
  - queries
  - nodes
related:
  further:
    - xookaexai0
    - koo4eevun4
    - ua6eer7shu
    - vequoog7hu
    - ojie8dohju
  more:
    - cahzai2eur
    - tioghei9go
---

# Querying multiple nodes in the Simple API

The Simple API contains automatically generated queries to fetch all nodes of a certain [type](!alias-ij2choozae). For example, for the `Post` type the top-level query `allPosts` will be generated.

## Querying all nodes of a specific type

> Query all post nodes:

```graphql
---
endpoint: https://api.graph.cool/simple/v1/cixne4sn40c7m0122h8fabni1
disabled: false
---
query {
  allPosts {
    id
    title
    published
  }
}
---
{
  "data": {
    "allPosts": [
      {
        "id": "cixnen24p33lo0143bexvr52n",
        "title": "My biggest Adventure",
        "published": false
      },
      {
        "id": "cixnenqen38mb0134o0jp1svy",
        "title": "My latest Hobbies",
        "published": true
      },
      {
        "id": "cixneo7zp3cda0134h7t4klep",
        "title": "My great Vacation",
        "published": true
      }
    ]
  }
}
```

> A few examples for query names
* type name: `Post`, query name: `allPosts`
* type name: `Todo`, query name: `allTodoes`
* type name: `Hobby`, query name: `allHobbies`.

Note: The query name approximate the plural rules of the English language. If you are unsure about the actual query name, explore available queries in your [playground](!alias-uh8shohxie#playground).

## Modifying the query response

The query response of a query fetching multiple nodes can be further controlled by supplying different query arguments. The response can be

* [ordered by field](!alias-vequoog7hu)
* [filtered by multiple fields](!alias-xookaexai0)
* [paginated](!alias-ojie8dohju) into multiple pages by fixing one specific node and either seeking forwards or backwards

These query arguments can be combined to achieve very specific query responses.
