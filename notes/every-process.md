---
id: 46gp5d41whxsw23pyk4ew03
title: Every Process
desc: ''
updated: 1691532356548
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