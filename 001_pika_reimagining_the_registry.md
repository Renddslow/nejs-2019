---
title: Pika: Reimagining the Registry
speaker: Fred K Schott <@fredkschott>
---

# Pika

Tl;dr: Compiling is slow.

[pika.dev](https://pika.dev)

> We are not Java developers. Why are we waiting for compilers?

## Why do we NEED web bundlers?
Npm

### 2009

Back in 2009 frontend was a bunch of `<script src="" />`'s and Node (Common.js) was `require("")`;

Enter Browserify. Everyone could do `require`'s.

The **web** added **tooling** to access **npm**.

This was not the web and Node entering a shared ecosystem. This was Node inviting the web into its ecosystem.

### 2019

ESM: all browsers support it.

Node.js still doesn't support it. NPM is Node's ecosystem.

We still need to handle Commonjs for the near future.

```
// 1. Bad Sup Dependencies
import 'modern-package-cjs'
// 2. Bad imports (package name, incomplete
import { cart } from 'cart-libary'
// 3. Bad Node-isms
import url from 'url'
```

### Pika Web

`@pika/web`

```
import { render, Component, createElement } from '/web_modules/preact.js'; 
```

When every dependency is a single file, you don't have to worry about dependency trees.

**Unbundled vs. Unbuilt**

```
// no build
import { cart } from '/web_modules/cart';

// Pika + Babel
import { cart } from 'cart';
```

For the first time, you don't **need** a bundler.

There is a growing divide in the frontend community: JS "only" devs and everything else devs.
