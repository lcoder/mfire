## 自定义事件处理器，模拟jquery的事件绑定

支持amd，cmd，commonjs调用

使用方法:
```javascript
var event = require( 'mfire' ) ;
event.on( 'event_click' , function() {
    console.log( 'event_click_trigger' ) ;
} ) ;
setTimeout(function(){
    event.fire( 'event_click' ) ;   // 1秒后，自动触发绑定的事件,控制台输出：'event_click_trigger'
},1000);
```

> 直接使用也可以，不过，多用于自定义的对象，继承这个mfire父类；
    ```javascript
    // 伪代码
    var children = {} ,
        mfire = require( 'mfire' ) ;
    }
    children.extend( mfire );

    children.on( 'event_something' , doSomething ) ;

    // someth times trigger event_something;
    children.fire( event_something ) ;

    ```