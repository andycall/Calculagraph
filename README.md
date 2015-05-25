# Timer
多功能计时器





##安装

```bash
npm install Timer
```



## 使用

### 准备

+ Node.js
    ```javascript
    var Timer = require('timer');
    ```

+ Browser Global
    ```javascript
    console.log(Timer);
    ```
+ RequireJS
    ```javascript
    define(['Timer'], function(Timer){
        console.log(Timer);
    });
    ```
    
### Step 1: 构建time对象

```javascript

var time = new Timer();
 
```

### Step 2: 设置起始时间
如果没有设置， 则默认为0。 当起始时间为0的时候， 逆时计时会自动停止。

```javascript

time.set(20); // 设置起始时间为20秒

```


### Step 3: 绑定计时器
可以看下面的例子


### API

**increase**
递增计时绑定

+ 参数： 
    - callback 每一个时刻触发的回调函数
    - interval 总运行时间
    - tick     每一个时刻的时间间隔
    - finish   完成之后触发的回调函数

**descrease**
递减计时绑定

+ 参数： 
    - callback 每一个时刻触发的回调函数
    - interval 总运行时间
    - tick     每一个时刻的时间间隔
    - finish   完成之后触发的回调函数


**set**
设置起始的时间， 需要在调用decrease或者increase时运行
+ 参数:
    - time : 设置的时间， 单位是秒
    
**stop**
停止计时， 同时清空计时状态。

**parse**
暂停计时， 保留计时状态

**restore**
恢复上一次暂停时的计时状态

**restart**
重启计时，如果之前设置了起始时间， 则从起始时间开始运行。


## AMD 加载器支持
若检测到AMD加载器，暴露Timer构造函数，且不再将Timer暴露到全局下

## Example

### 逆时计时
```javascript
    
var time = new Timer();
time.set(30);
time.decrease(function(time){
    console.log(time);
}, 30, 500, function(){
    console.log('finishde');
});

```

### 顺时计时
``` javascript

var time = new Timer();
time.set(15);
time.increase(function(time){
    console.log(time);
}, 20, 1000, function(){
    console.log('finished');
});

```

## 当前用户

* 阿里妈妈MUX:[http://mux.alimama.com/event/2015mothersday/index.html](http://mux.alimama.com/event/2015mothersday/index.html)





