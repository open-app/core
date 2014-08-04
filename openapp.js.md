# OpenApp.js

## principles

"I want programming computers to be like coloring with crayons and playing with duplo blocks." - [Ryan Dahl, creator of node.js](https://news.ycombinator.com/item?id=4310723)

[timoxley/best-practices](https://github.com/timoxley/best-practices)

- simple
- modular
- composable

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
