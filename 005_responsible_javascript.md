---
title: Responsible JavaScript
speaker: Jeremy Wagner <@malchata>
---

# Responsible JavaScript

A List Apart

> Sphexishness - (of animal behavior) deterministic; preprogrammed

Sphex: a genus of solitary wasp. These wasps are easily manipulated.

```
npm install react 

npm install react-dom 

npm install react-router 

npm install react-redux
```

10% of websites will send 1MB of JS (Transfer size)

Understanding constraints are what make us good programmers. The best video games were under a megabyte.

## Anti-Sphexishness

Paint the picture, not the frame (A11y & UX)

Do not subvert expectations by changing the appearance of external consistencies. We do this when we don't use semantic HTML.

A form should ALWAYS USE A `<form>` tag.

The browser gives us a lot for free stuff.

## The Tools Are Not Infallible

We would all benefit if we needed to transpile less.

Change babel `useBuiltIns` to `usage`;

`loose: true`

## Differential Serving

Serving different code depending on the browser.

```html
<script type="module" src="/js/app.mjs"></script>
<script nomodule defer src="/js/app.js"></script>
```

// TALK ABOUT DIFFERENTIAL SERVING AND THE USERBASE

Jeremy.Codes - A Less Risky Differential Serving Pattern

## Be Accommodating

When we deploy something to the web, we need to be a steward of that thing.

[The Unacceptable Persistence of the Digital Divide]

Pew Research found that 33% of Americans do not have an Internet access faster than dial-up in their homes.

**Client hints** (User Navigator)

- `rtt` - round trip time
- `downlink` - 
- `ect` - effective connection type

`Accept-CH: RTT, Downlink, ECT`

`Accept-CH-Lifetime: 86400`

```js
let ect = '4g';
if (req.headers['ect']) {
  ect = req.headers['ect'];
}
```

[Adapting to Users with Client Hints]

Figure Out What People Want -> And Work Backward From There

`People > Dev Experience`


