# Timer
multifunctional calculagraph

##Install

### Step 1: construct a new time object

```javascript

var time = new Timer();
 
```

### Step 2: set up your start time
It will be 0 as default, when start time set to 0, the decrease time will be stoped.

```javascript

time.set(20); // set start time to 20 second

```


### Step 3: bind timer
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
export the Timer constructor

## Example

### anticlockwise timing
```javascript
    
var time = new Timer();
time.set(30);
time.decrease(function(time){
    console.log(time);
}, 30, 500, function(){
    console.log('finishde');
});

```

### clockwise
``` javascript

var time = new Timer();
time.set(15);
time.increase(function(time){
    console.log(time);
}, 20, 1000, function(){
    console.log('finished');
});

```

## Who is using the plugin

* 阿里妈妈MUX:[http://mux.alimama.com/event/2015mothersday/index.html](http://mux.alimama.com/event/2015mothersday/index.html)





