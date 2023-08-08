---
id: 46gp5d41whxsw23pyk4ew03
title: Every Process
desc: ''
updated: 1691534541856
created: 1691527360934
---
# Every Process, Everywhere, All at Once - Luis Montes
[Slides](seattlejs23.netlify.app)
Luis Montes - @monteslu@fosstodon.org


## Decentralized web computing
Web APIs have provided lots of abilities since 2001.

Web 3 --> Decentralization
## Web 3 Browser APIs? Surprise - none!

Decentralization requires each peer to be both a client and a server.

## So how do we do that?

Electron is great for Direct TCP & UDP Networking
[Do you really need it though](https://youmightnotneedelectron.com/)

How to share local proxies - reverse proxies - ngrok, localtunnel, hsync 

## Put the proxy in a web page?
Reverse proxy in a web page to deliver content outside of a web server.
[Proxy in a Web Page](browserver.netlify.app)

## Use Node in the browser
[Actual Node in Browswer](expressnode.netlify.app)
Provdes `nodemon` and `npm` inside of an iframe inside of the web page. 
Native threading has been pushed by [StackBlitz](https://stackblitz.com/) to prevent blocking when multitudes of requests are present.

## Proxying more than http
Use WASM to allow Postgres within the server

Use Telnet to open up a TCP pipe to talk to a browser

## Web RTC Data Channels
Creating a direct connection between two mobile browsers

## Nesting the proxy server
Use wildcard certs on domains

## Is all of this decentralized or federated?
More federated

TCP and UDP sockets still need to happen in the browser.

# TL;DR 

If we can get full duplex packet transfers working between web browsers without any reverse proxying shennanigens it would be possible to implement a fully peer to peer system that doesn't rely on centralized authority. In some ways a system like this would be more resilient to bad corporate actors or, worse, hostile state actors. Google can't shut down a Nest device that doesn't rely on talking to Google servers to work, for example. As it stands there's some ambiguity on what levels of trust you will have to possess to impement a decentralized system based wholly on browser technology. Do we trust web browser vendors? Should we have to? Big questions!