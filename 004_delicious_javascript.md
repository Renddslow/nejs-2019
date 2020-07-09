---
title: Delicious JavScript: Delectable Explanations of the Power of JS
speaker: Adrienne Tacke <adriennetacke>
---

# Delicious JavScript: Delectable Explanations of the Power of JS

- JavaScript is hard
- JavaScript is complicated
- JavaScript is confusing...

## `filter()`

`Array.prototype.filter`

```js
const food = ['🍩', '🍪', '🍪', '🍣'];

const onlyCookies = food.filter((x) => x === '🍪');
// => ['🍪', '🍪']
```

## `map()`

`Array.prototype.map`

```js
const bagOfMarshmallows = [
  'marshmallow',
  'marshMallow',
  'marshMALLOW',
  'MARSHmallow',
  '☁️',
];

const filteredJumboMarshmallows = bagOfMarshmallows
  .filter((m) => m !== '☁️')
  .map((m) => m.toUpperCase());
// => ['MARSHMALLOW', 'MARSHMALLOW', 'MARSHMALLOW', 'MARSHMALLOW']
```

## `reduce()`

`Array.prototype.reduce`

```js
const donutLog = [
  { day: 'Monday', totalEaten: 2 },
  { day: 'Tuesday', totalEaten: 3 },
  { day: 'Wednesday', totalEaten: 1 },
  { day: 'Thursday', totalEaten: 5 },
  { day: 'Friday', totalEaten: 4 },
];

const caloriesConsumed =  donutLog.reduce((acc, val) => {
  acc += val.totalEaten * 278;
  return acc;
}, 0);
// => 4170
```

