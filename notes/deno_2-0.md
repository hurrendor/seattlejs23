---
id: 2jhzsq7dvp7cc2s80aanv0w
title: Deno_2 0
desc: ''
updated: 1692747893478
created: 1691513398262
---
## What to Know About Deno 2.0 - Kevin Whinnery (9:30)
[Deno Website](deno.io) |
[Talk on YouTube](https://www.youtube.com/watch?v=dipwQfcV0AU)
- Set up to use like a browser / models browser behavior
### Examples given: 
* Accesibility to test/experimental methods
* works with fetch api
* Ability to deploy applications
* Ability to render out individual JSX components to test against
* Import secure (https) resources - act like the browser
* Decentralized - modules live anywhere

Challenges Faced With HTTPS imports:
* Disappearing imports - if ther was an update (subtle), or the server hosting the resource goes down
* Possibility of duplicate dependencies - different version/server, inability to optimize on **semvar**

2.0 Provides a centralized package management platform
[Deno Registry](deno.land/r) 

[10 Things I Regret About Node.js - Ryan Dahl](rytalk.deno.dev)

Deno is marketed as faster, especially on network requests. The aim is to create code in a local environment 

[Fresh](https://fresh.deno.dev/) - Deno Framework: Reducing the dev steps needed. "Fresh embraces the tried and true design of server side rendering and progressive enhancement on the client side"