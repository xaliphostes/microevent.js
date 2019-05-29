

# MicroEvent in ES6+
Refactor of [MicroEvent](https://github.com/jeromeetienne/microevent.js) in JavaScript for ES6+

## Usage
See [this page](https://github.com/jeromeetienne/microevent.js)

## Example
```js
 import MicroEvent from 'MicroEvent'
 
 class Ticker {
     setInterval() {
         this.trigger( 'tick', new Date() )
     }, 1000)
 }
 MicroEvent.mixin(Ticker)
 
  
 const ticker = new Ticker()
 ticker.bind('tick', date => {
     console.log('notified date', date)
 })
  
 // And you will see this output every second:
 //   notified date Tue, 22 Mar 2019 14:43:41 GMT
 //   notified date Tue, 22 Mar 2019 14:43:42 GMT
 //   ...
```
