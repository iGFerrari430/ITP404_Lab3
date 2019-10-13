# ITP404_Lab3

## 1
JSON:API is a specification for how a client should request that resources be fetched or modified, and how a server should respond to those requests.
It is designed to minimize both the number of requests and the amount of data transmitted between clients and server. It’s efficient and meanwhile not compromising readability, flexibiliy or discoverability.

## 2
Alternatives to JSON:API includes: RESTful API and GraphQL.

## 3
### Pros:
1. excellent request efficiency. A single request sufficient for most needs.<br/>
2.operations are simple. works out of the box with CDNs and reverse proxies. no client-side libraries needed.<br/>
3. also excellent in terms of writing data. how writes are handled is clearly defined by the specs.

### Cons: 
1. Documentation is limited and schemas are limited to only generic schema. reliable field-level shcema is not yet available.<br/>
2. Interactivity is limited. Developers need to ovserve available fields and links in its reponses to enable the exploration of API, which is less ideal compared to GraphQL.

## 4
{
  "type": "articles",
  "id": "1",
  "attributes": {
    "title": "Rails is Omakase"
  },
  "relationships": {
    "author": {
      "links": {
        "self": "/articles/1/relationships/author",
        "related": "/articles/1/author"
      },
      "data": { "type": "people", "id": "9" }
    }
  }
}
