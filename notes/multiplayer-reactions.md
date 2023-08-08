---
id: 2zx52ri4d5pvccbz6uvfwmc
title: Multiplayer Reactions
desc: ''
updated: 1691530693911
created: 1691527316699
---
# Building a Real-Time Multiplayer Reactions Component - John Pham
[Slides](https://live-reactions-slides.vercel.app/)
[Reactions](dub.sh/reactions)

John Pham - @JohnPhamous

## Building a component

- Multiplayer, accessible, reactive

Creating a multiplayer application presents a series of issues:
* Learning sockets
* Scaling servers
* **TODO: Add more from slides**
LiveBlocks provides the ability 

## Accesibility
* Role attributes
Group items inside of this component. These items are related to a common thing, described in the aria-label.
* Aria-labels

Provide relevant naming in aria-labels to provide clarity for accesibility.
Rendering something like emojis non-stop to the screen overloads screen-readers

Roles control what is announced or given attention to screen readers. By providing options for visual users and screen readers, user experience can be increased for both.

Reactive for multiple people in the same room
Using LiveBlocks
- provides room clients to gather responses from people within that 'room'

Subscribing to published events
- LiveBlocks provides a useBroadcastEvent() hook to subscribe to events happening in the client room. Setting up a `broadcast` event will allow others to also see the data being broadcast.

Receiving messages from broadcast
- LiveBlocks event listener hook `useEventListener`
Using separate clients can be used to separate responses received from local and remote levels.