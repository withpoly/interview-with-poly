
## The Problem

We would like you to write a web server in Node.js that utilizes wasm (WebAssembly) to execute computation. The catch is that your wasm binary runs on *both* the client and the server, and the client can decide dynamically whether to execute the computation locally or to contact the server for the result.

## Context

The most important link you need is [this](https://wasmedge.org/book/en/sdk/node.html), which is essentially a fully set up library to use WasmEdge from within Node.js. In their example, the client application has some task (solving a quadratic equation) and the client pings the server to solve the problem via a WasmEdge connector. You need to write a your own code compiled to wasm binaries that are run on both the client and the server. The client will of course need to include a way to contact the server (this could be native to the wasm code or external to it, i.e. either be via a Wasm Fetch API, or just by calling a javascript method in the containing code).

The goal is to have the same Wasm code be "write once, run anywhere", so do NOT write your method twice. Your client also gets to "decide" whether to run locally or run on the server, so you do not need to dynamically compile the runtime or anything. Just a statically compiled binary should work. Note that you might need two compilation targets even if the code is shared.

You can choose any language to write your wasm library in. We recommend Rust, but Python, C, etc. should all work. For a demo, your wasm application can just do something simple like echoing text, adding numbers, etc. 

## Some questions

1. How does your client "ask" the server to run the computation? Is there a way to do this without duplicating your libary SDK as an API?
2. How do you make the library non-blocking (this is potentially outside of scope, but still interesting)
3. What are the benefits and drawbacks of this way of separating compute between the client and server?

## What is WASM?

WebAssembly (WASM) is a way of executing code at near native performance inside a sandbox in various environments (starting with the web). It is now being used as a potential replacement for Docker containers! 

## What libraries should I use?

WasmEdge should have everything you need

## Extra credit questions

Can you have the client automatically decide when to use the server vs the client? What kinds of computations would need to be on one or the other?
Can you have the client manage some state as well, so that your client can be an MVC-style system and the server calls are just "internal" to the controller logic?
