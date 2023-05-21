##  1.闭包

             一句话可以概括：闭包就是能够读取其他函数内部变量的函数，或者子函数在外调用，子函数所在的父函数的作用域不会被释放。
## 2. JS 的 new 操作符做了哪些事情 

        new 操作符新建了一个空对象，这个对象原型指向构造函数的 prototype，执行构造函数后返回这个对象。

## 3. 改变函数内部 this 指针的指向函数（bind，apply，call 的区别） 

        通过 apply 和 call 改变函数的 this 指向，他们两个函数的第一个参数都是一样的表示要改变指向的那个对象，第二个参数，apply 是数组，而 call 则是 arg1,arg2...这种形式。通过 bind 改变 this 作用域会返回一个新的函数，这个函数不会马上执行。

##    4.如何理解前端模块化 

        前端模块化就是复杂的文件编程一个一个独立的模块，比如 JS 文件等等，分成独立的
        模块有利于重用（复用性）和维护（版本迭代），这样会引来模块之间相互依赖的问
        题，所以有了 commonJS 规范，AMD，CMD 规范等等，以及用于 JS 打包（编译等处理）
        的工具 webpack

##    5.webpack 用来干什么的

        webpack 是一个现代 JavaScript 应用程序的静态模块打包器(module bundler)。当
        webpack 处理应用程序时，它会递归地构建一个依赖关系图(dependency graph)，其
        中包含应用程序需要的每个模块，然后将所有这些模块打包成一个或多个 bundle。   
##    6.深拷贝/浅拷贝

        深拷贝是指在拷贝一个对象时，会将该对象及其所有嵌套的子对象都完全拷贝一遍，生成一个新的副本。深拷贝后，原对象和拷贝后的对象是完全独立的，互不影响。

        浅拷贝是指在拷贝一个对象时，仅仅拷贝该对象本身及其所有一级属性，不拷贝该对象嵌套的子对象。对于原对象和拷贝后的对象，它们共享相同的子对象。
##    7.七种基本数据类型

        ①布尔值（Boolean），②null，③undefined，和 null ，③undefined，和 null ，⑤任意精度的整数 (BigInt) ，
        ⑥字符串（String），⑦代表（Symbol），⑧以及对象（Object）
##    8.mouseover 和 mouseenter 的区别    

             mouseover：当鼠标移入元素或其子元素都会触发事件，所以有一个重复触发，冒泡的过程。对应的移除事件是 mouseout 
             mouseenter：当鼠标移除元素本身（不包含元素的子元素）会触发事件，也就是不会
            冒泡，对应的移除事件是 mouseleave
##    9.两个嵌套的 div，position 都是 absolute，子 div 设置 top 属性，那么这个 top 是相对于父元素的哪个位置定位的。

        margin 的外边缘

##    10.line-height 和 height 的区别 

        line-height 一般是指布局里面一段文字上下行之间的高度，是针对字体来设置的，height 一般是指容器的整体高度。

##    11.addEventListener 参数

        addEventListener(event, function, useCapture) 其中，event 指定事件名；function 指定要事件触发时执行的函数；useCapture 指定事件是否在捕获或冒泡阶段执行
##     12.讲讲 304

        304：如果客户端发送了一个带条件的 GET 请求且该请求已被允许，而文档的内容（自上次访问以来或者根据请求的条件）并没有改变，则服务器应当返回这个 304 状态码
        
##        13.GET 和 POST 的区别

        get 参数通过 url 传递，post 放在 request body 中。
        get 请求在 url 中传递的参数是有长度限制的，而 post没有。
        get 比 post 更不安全，因为参数直接暴露在 url 中，所以不能用来传递敏感信息。
        get 请求只能进行 url 编码，而 post 支持多种编码方式

##        14.HTTP 支持的方法

       GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE, CONNECT
##      15.http 常见的请求方法

        get、post，这两个用的是最多的，还有很多比如 patch、delete、put、options 等等

##     16.说一下块元素和行元素

        块元素:独占一行，并且有自动填满父元素，可以设置 margin 和 pading 以及高度和宽度
        行元素:不会独占一行，width 和 height 会失效，并且在垂直方向的 padding 和margin 会失效。
##      17.用的最多的 css 属性是啥？
        用的目前来说最多的是 flex 属性，灵活但是兼容性方面不强。
##      18.事件代理在捕获阶段的实际应用
        可以在父元素层面阻止事件向子元素传播，也可代替子元素执行某些操作。
##      19.eval 是做什么的
        它的功能是将对应的字符串解析成 JS 并执行，应该避免使用 JS，因为非常消耗性能（2 次，一次解析成 JS，一次执行）
##      20.cache-control 的值有哪些
        cache-control 是一个通用消息头字段被用于 HTTP 请求和响应中，通过指定指令来实
        现缓存机制，这个缓存指令是单向的，常见的取值有 private、no-cache、max-age、
        must-revalidate 等，默认为 private。