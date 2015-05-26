# Calculagraph
multifunctional calculagraph

##Install

```bash
npm install calculagraph
```

## How to Use

### Prepare

+ Node.js

    ```javascript
    var Calculagraph = require('calculagraph');
    ```

+ Browser Global
    
    ```javascript
    console.log(Calculagraph);
    ```

+ RequireJS

    ```javascript
    define(['Calculagraph'], function(Calculagraph){
        console.log(Calculagraph);
    });
    ```

### Step 1: setup a new time object

```javascript

var time = new Calculagraph();
 
```

### Step 2: config your start time
It will be 0 as default, when start time set to 0, the decrease time will be stoped.

```javascript

time.set(20); // set start time to 20 second

```


### Step 3: start your calculagraph

here are some examples

### API

**increase**
clockwise timing

+ params： 
    - callback(**Function**) : the callback triggered every tick 
    - interval(**Number**):  total running time
    - tick (**Number**):     custom the tick time, default to 1000 ms
    - finish (**Function**):   the callback when all done

**descrease**
anticlosewise timing

 
+ params： 
    - callback(**Function**) : the callback triggered every tick 
    - interval(**Number**):  total running time
    - tick (**Number**):     custom the tick time, default to 1000 ms
    - finish (**Function**):   the callback when all done


**set**
set up start time, set before call decrease or increase function
+ param:
    - time(**Number**): start time
    
**stop**
stop timing and clear time status

**parse**
parse timing and storage time status

**restore**
restore last time status when parsed

**restart**
restart timing, and set time to start time.

## Support for AMD loader
export the Calculagraph constructor

## Example

### anticlockwise timing
```javascript
    
var time = new Calculagraph();
time.set(30);
time.decrease(function(time){
    console.log(time);
}, 30, 500, function(){
    console.log('finishde');
});

```

### clockwise
``` javascript

var time = new Calculagraph();
time.set(15);
time.increase(function(time){
    console.log(time);
}, 20, 1000, function(){
    console.log('finished');
});

```

## Who is using the plugin

* 阿里妈妈MUX:[http://mux.alimama.com/event/2015mothersday/index.html](http://mux.alimama.com/event/2015mothersday/index.html)





