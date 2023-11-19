---
title: "Flow Field"
description: "A Coding Train challenge, converted to clojurescript."
date: 2023-11-19T17:39:10-05:00
draft: false
---

This is a more substantial project, where I've taken a Coding Train challenge and converted it to clojurescript. The original challenge can be found [here](https://thecodingtrain.com/CodingChallenges/024-perlinnoiseflowfield.html).

I found several challenges in converting this to clojurescript. The original Coding Train implementation made frequent use of Javascript's mutable data structures. For example, I had to represent particles as a map of properties, and the "physics engine" as a set of functions acting on those properties.

Using Quil as a wrapper around P5.js enabled me to use a React-like style of programming. I had the well-known `setup` and `draw` functions, of course, but without resorting to mutating state, I had to use Quil's `update` function to generate the next frame's drawing state.

The primary side effect of this style of programming is that the clojurescript implementation creates much more garbage than the original Javascript implementation.

{{< loadJS "f" >}}

<div id="app"></div>
