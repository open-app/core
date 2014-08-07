# OpenApp.js

## principles

"I want programming computers to be like coloring with crayons and playing with duplo blocks." - [Ryan Dahl, creator of node.js](https://news.ycombinator.com/item?id=4310723)

[timoxley/best-practices](https://github.com/timoxley/best-practices)

- simple
- modular
- composable

## features

- resources are commonly understood entities (Linked Data vocabularies)
- holons (people and recursive groups) are identities
- identities are cryptographic keys
- each holon has a unique primary data service
- each service can be many micro data services
- services can have many different interfaces
- services describe their interfaces through hypermedia
- each primary data service can have many cached replicas
- primary data services publish changes to subscribed cached replicas
- cached replicas provide pipeline to submit changes to primary data services
- trust relationships between identities determine cross-service network topology
- resources transfer through services across trust relationships (CPU cycles, data storage, food, shelter, ...)
- transfer between services can employ many different patterns of conversation (request / response, publish / subscribe, push / pull, even more complex patterns like conversations of action)
- data services store transactions on state instead of state
- data services employ conflict resolution algorithms on transactions
- data is immutable and flows instead of changes (consequence of all the above)
- data services are de-coupled from views
- views are components that take in input events, render, and output events (one-directional like https://raynos.github.io/forwardjs2014-talk/)
- generic views can be generated from data and relevant hypermedia

## models

- describe data with an extended version of JSON-Schema
  - validation
  - coercion
  - format
  - serialization
  - deserialization
  - relations
  - Linked Data vocabulary
- composable with allOf, anyOf, oneOf, and not

## views

- use models to generate reactive views
- each page is a Linked Data query
- multiple ways to view result set (list, grid, graph)
- multiple ways to sort result set (A-Z, Z-A, ...)

## controllers

- autonomous micro-services
- support various forms of message-passing
  - conversation patterns
    - request / response
    - publish / subscribe
    - push / pull
  - interfaces
    - HTTP
    - WebSockets
    - libchan via [jschan](https://github.com/graftjs/jschan)
  - serialization
    - JSON
    - msgpack v5
  - transport
    - SPDY
    - WebSockets
  - formats
    - JSON-LD
  - hypermedia
    - Hydra
    - JSON API
- composable via chaining
