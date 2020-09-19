# API Design

We recommend that APIs be built with REST.  The exception may be services built sepecifically to be gateways that combine multiple APIs.

## Why

The face that REST is mature, proven, and ubiquious outweight the benefits that GraphQL can provide.  Talent is easy to find and tooling is extensive for REST.

## Benefits
### REST

- Familiarity, ease of learning
- Vast community and support, it has been a standard for eons
- Clearly defined operations
  - GET, PUT, POST, DELETE
  - Match the associated database concepts
- Can be implemented by a number of API tools, languages, etc
- Ubiquitous
- Lots of testing support libraries and tools including contract testing

### GraphQL

- Elinates over-fetching and under-fetching eliminating unneeded roundtrips and data transfer.
- Can defer decisions on data modelling
- Very effective for aggregating across multiple APIs
- Further decouples front and back ends, simplifying what the clients need to know to get data by collapsing everything down to one “source”
- Allow clients that need data define the query, rather than restrict via what’s offered by the API
- Trims data down to just what’s needed, streamlining calls across multiple surfaces required to assemble the ask
- Offers a playground UI that visualizes requests and supports testing
- Can deprecate individual nodes on the graph, informing users that they should move to the new source/node

## Negatives

### REST

- Versioning APIs – hard to get people to migrate from v1 to v2
- Tightly couples data shapes, and relationships between UI and API

### GraphQL

- The whole shape of the graph is always exposed.  Can request anything, but trying to without the correct permissions will generate an error
- Node deprecation is not easy to manage or implement
  - Nodes must have a unique name, so there’s no real advantage here over the API versioning
- Still new and unrefined.  Lots of great concepts, but execution / implementation often lacks or is difficult
  - Should probably never be used for a Tech Challenge
- No specification like there is for OpenAPI
- No contract to test
- Tough to cause failures to test for fault tolerance
- Newer technology means that there is less expertise
