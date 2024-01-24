
## The Problem

We would like you to write a web server (in any language) that utilizes wasm (WebAssembly) to execute computation. The catch is that your wasm code can be built to run on *either* the client and the server, and the client can decide dynamically whether to execute the computation locally or to contact the server for the result. The goal is to "write once, run anywhere" for your code, so you will need to minimize duplication of implementation, and use a wasm toolchain that can build for multiple environments.

## Context

In the future, powerful client environments will have the ability to execute complex computation. This might include GPU tasks, file or image processing, etc. However, we currently still live in a world of client-server communication. There are good reasons for the server to be seen as a source of truth, but we might also want to push computation to the edge for many reasons, such as cost, latency, etc. However, traditionally, edge compute has required a separate codebase since the embedded environment is so different from the server. Examples include iOS, Raspberry Pi, etc. What we want to do is explore how to drastically improve the developer experience of this kind of architecture by sharing and reusing code as much as feasible and possible.

We want you to explore this possibility in a miniature way. You can choose any language to write your wasm library in. We recommend Rust, but Python, C, etc. should all work. For a demo, your wasm application can just do something simple like echoing text, adding numbers, etc. 

The first problem is creating a development environment (toolchain, binary, etc.) that allows for this kind of cross-compilation and cross-deployment. The second problem is the devising a set of abstractions and APIs that can make use of these capabilities.

## Some questions

1. How does your client "ask" the server to run the computation? Is there a way to do this without duplicating your libary SDK as an API? For example, can it be invisible to the front-end developer as to "where" the computation is run?
2. How do you make the library non-blocking on the client?
3. What are the benefits and drawbacks of this way of separating compute between the client and server? Where is this a very good or very bad idea?
4. How do you ensure consistency of your data in a scenario where the client and server are disconnected?

## What is WASM?

WebAssembly (WASM) is a way of executing code at near native performance inside a sandbox in various environments (starting with the web). It is now being used as a potential replacement for Docker containers! 

## What libraries should I use?

WasmEdge should be a good starting place, but there are now a variety of systems that try to do this in different ways. One big decision you get to make is what language you want to implement these things in. 

## Extra credit questions

Can you have the client automatically decide when to use the server vs the client? What kinds of computations would need to be on one or the other?
Can you have the client manage some state as well, so that your client can be an MVC-style system and the server calls are just "internal" to the controller logic? How is that state maintained in the face of network partitions?
Can you do a more meaningful computation that bundles a larger library? Examples might be to render JXL images, generate a fractal, etc. Being able to manage/wrangle with the dependency chain is a great show of expertise!
