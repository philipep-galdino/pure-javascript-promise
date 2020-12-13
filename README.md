_This whole Promise work-out idea and explanation comes from Roger Melo video on Promises as it's in pure Javascript._

Click below to be redirected to the video in portuguese-brazilian - there's no english version.

[Video](https://www.youtube.com/watch?v=wTGPhsGJ0sw "Video Link")
# Promises

A promise is an object that represents the success or the error of a asynchronous operation.

## Asynchronous Operations

When executing a asynchronous operation - a request, for example - Javascript pulls out a new thread to resolve the request separatedely while the main thread flows on with it's functioning.


## How does a Promise works?

Promises normally receives two functions for it's callbacks, a resolve and a reject function. These functions are invokeds as it's needed to resolve or reject some operation/value.

---

A promise usually is chained by other promises inside of it, as it happens on the example below:

```js
const aPromise = new Promise((resolve, reject) => {
    const aNUmber = 37

    //resolve(aNumber) // resolve returns the value
    reject(aNumber)
})

aPromise
    .then(value => value)
    .then(value => {
        console.log(value)
    })
    .catch(rejectValue => {
        // catch is only invoked as an
        // error handler for the promise
        console.log(rejectValue)
    })
```    
---

The example above is not an asynchronous operation, but shows off how does a Promise works by it's syntax. 

If you want to check out a asynchronous operation working with a Promise, go to the [promise.js](https://github.com/philipep-galdino/pure-javascript-promise/blob/main/promise.js) file.

There you'll see how to we do a request to an API, where each request returns a random dog image for us, and we handle this operation with a Promise.
