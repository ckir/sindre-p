# sindre-p 
---


All Promise Utils functions from github.com/sindresorhus bundled together!

## Installation
---

```sh
npm install github:ckir/sindre-p --save
```

## Usage
---

```javascript
const p = require('sindre-p')

/*
    That's it!, now you can call any of his functions :)
*/

p.delay(1000)
 .then(() => console.log('I waited 1000 milliseconds to send this message! :D'))

```

## Information
---

One important thing is that due to not all of the packages being legal variable names in JavaScript (for example the package `p-map` would be interpreted as `p - map`, like it would be a math equation)

Due to this, the keys in the object that represent the function will follow this naming convention:

1. If the module does not start with `p-`, it will be temporary be added to the module name, like this `require('delay')` -> `require('p-delay')`
2. `p-` will now be removed from the key name, due to the recommended variable the `require('sindre-p')` being assigned to is `p` or `P`, like the example above!
3. If the module name has hyphens (`-`) in it, it will get removed, and the following character will be capitalized, like this `require('do-whilst')` -> `require('doWhilst')`
4. Now the module name will get added to the object that this module is exporting, for example like this:
    ```javascript
    const p = {
        doWhilst: require('p-do-whilst')
    }
    ```

## Documentation
---
##### `require('sindre-p')`

Returns an object with all the Promise util functions!

They will be mapped just like this:

- `all` -> [`require('p-all')`](https://github.com/sindresorhus/p-all): Run promise-returning &amp; async functions concurrently with optional limited concurrency
- `any` -> [`require('p-any')`](https://github.com/sindresorhus/p-any): Wait for any promise to be fulfilled
- `break` -> [`require('p-break')`](https://github.com/sindresorhus/p-break): Break out of a promise chain
- `cancelable` -> [`require('p-cancelable')`](https://github.com/sindresorhus/p-cancelable): Create a promise that can be canceled
- `catchIf` -> [`require('p-catch-if')`](https://github.com/sindresorhus/p-catch-if): Conditional promise catch handler
- `debounce` -> [`require('p-debounce')`](https://github.com/sindresorhus/p-debounce): Debounce promise-returning &amp; async functions
- `defer` -> [`require('p-defer')`](https://github.com/sindresorhus/p-defer): Create a deferred promise
- `delay` -> [`require('delay')`](https://github.com/sindresorhus/delay): Delay a promise a specified amount of time
- `doWhilst` -> [`require('p-do-whilst')`](https://github.com/sindresorhus/p-do-whilst): Calls a function repeatedly while a condition returns true and then resolves the promise
- `eachSeries` -> [`require('p-each-series')`](https://github.com/sindresorhus/p-each-series): Iterate over promises serially
- `event` -> [`require('p-event')`](https://github.com/sindresorhus/p-event): Promisify an event by waiting for it to be emitted
- `every` -> [`require('p-every')`](https://github.com/kevva/p-every): Test whether all promises passes a testing function
- `filter` -> [`require('p-filter')`](https://github.com/sindresorhus/p-filter): Filter promises concurrently
- `forever` -> [`require('p-forever')`](https://github.com/sindresorhus/p-forever): Run promise-returning &amp; async functions repeatedly until you end it
- `hardRejection` -> [`require('hard-rejection')`](https://github.com/sindresorhus/hard-rejection): Make unhandled promise rejections fail hard right away instead of the default silent fail
- `if` -> [`require('p-if')`](https://github.com/sindresorhus/p-if): Conditional promise chains
- `immediate` -> [`require('p-immediate')`](https://github.com/sindresorhus/p-immediate): Returns a promise resolved in the next event loop - think `setImmediate()`
- `isPromise` -> [`require('p-is-promise')`](https://github.com/sindresorhus/p-is-promise): Check if something is a promise
- `lazy` -> [`require('p-lazy')`](https://github.com/sindresorhus/p-lazy): Create a lazy promise that defers execution until `.then()` or `.catch()` is called
- `limit` -> [`require('p-limit')`](https://github.com/sindresorhus/p-limit): Run multiple promise-returning &amp; async functions with limited concurrency
- `locate` -> [`require('p-locate')`](https://github.com/sindresorhus/p-locate): Get the first fulfilled promise that satisfies the provided testing function
- `log` -> [`require('p-log')`](https://github.com/sindresorhus/p-log): Log the value/error of a promise
- `loudRejection` -> [`require('loud-rejection')`](https://github.com/sindresorhus/loud-rejection): Make unhandled promise rejections fail loudly instead of the default silent fail
- `map` -> [`require('p-map')`](https://github.com/sindresorhus/p-map): Map over promises concurrently
- `mapSeries` -> [`require('p-map-series')`](https://github.com/sindresorhus/p-map-series): Map over promises serially
- `memoize` -> [`require('p-memoize')`](https://github.com/sindresorhus/p-memoize): Memoize promise-returning &amp; async functions
- `minDelay` -> [`require('p-min-delay')`](https://github.com/sindresorhus/p-min-delay): Delay a promise a minimum amount of time
- `one` -> [`require('p-one')`](https://github.com/kevva/p-one): Test whether some promise passes a testing function
- `pify` -> [`require('pify')`](https://github.com/sindresorhus/pify): Promisify a callback-style function
- `pipe` -> [`require('p-pipe')`](https://github.com/sindresorhus/p-pipe): Compose promise-returning &amp; async functions into a reusable pipeline
- `progress` -> [`require('p-progress')`](https://github.com/sindresorhus/p-progress): Create a promise that reports progress
- `props` -> [`require('p-props')`](https://github.com/sindresorhus/p-props): Like `Promise.all()` but for `Map` and `Object`
- `queue` -> [`require('p-queue')`](https://github.com/sindresorhus/p-queue): Promise queue with concurrency control
- `race` -> [`require('p-race')`](https://github.com/sindresorhus/p-race): A better `Promise.race()`
- `reduce` -> [`require('p-reduce')`](https://github.com/sindresorhus/p-reduce): Reduce a list of values using promises into a promise for a value
- `reflect` -> [`require('p-reflect')`](https://github.com/sindresorhus/p-reflect): Make a promise always fulfill with its actual fulfillment value or rejection reason
- `retry` -> [`require('p-retry')`](https://github.com/sindresorhus/p-retry): Retry a promise-returning or async function
- `series` -> [`require('p-series')`](https://github.com/sindresorhus/p-series): Run promise-returning &amp; async functions in series
- `settle` -> [`require('p-settle')`](https://github.com/sindresorhus/p-settle): Settle promises concurrently and get their fulfillment value or rejection reason
- `some` -> [`require('p-some')`](https://github.com/sindresorhus/p-some): Wait for a specified number of promises to be fulfilled
- `tap` -> [`require('p-tap')`](https://github.com/sindresorhus/p-tap): Tap into a promise chain without affecting its value or state
- `throttle` -> [`require('p-throttle')`](https://github.com/sindresorhus/p-throttle): Throttle promise-returning &amp; async functions
- `time` -> [`require('p-time')`](https://github.com/sindresorhus/p-time): Measure the time a promise takes to resolve
- `timeout` -> [`require('p-timeout')`](https://github.com/sindresorhus/p-timeout): Timeout a promise after a specified amount of time
- `times` -> [`require('p-times')`](https://github.com/sindresorhus/p-times): Run promise-returning &amp; async functions a specific number of times concurrently
- `try` -> [`require('p-try')`](https://github.com/sindresorhus/p-try): `Promise#try()` ponyfill - Starts a promise chain
- `waitFor` -> [`require('p-wait-for')`](https://github.com/sindresorhus/p-wait-for): Wait for a condition to be true
- `waterfall` -> [`require('p-waterfall')`](https://github.com/sindresorhus/p-waterfall): Run promise-returning &amp; async functions in series, each passing its result to the next
- `whilst` -> [`require('p-whilst')`](https://github.com/sindresorhus/p-whilst): Calls a function repeatedly while a condition returns true and then resolves the promise

## License

MIT
