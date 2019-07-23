### interview

---
写了一些针对前端面试的笔记。


// 
HTML
1.(必考) 你是如何理解HTML语义化的？
<<<<<<< HEAD
  举例：段落用 p，边栏用 aside，主要内容用 main 标签。
2. meta viewport 是做什么用的，怎么写？
  背：<meta name="viewport" content="width=device-width(宽度等于设备宽度),
  user-scalable=no(用户不准放大缩小),initial-scale=1.0(一开始的倍数),
  maximum-scale=1.0(最大倍数), minimum=1.0(最小倍数)">
  作用：控制页面在移动端不要缩小显示。
3. canvas 元素是干什么的？
  canvas 是 HTML5 新增的元素，可用于通过使用js中的脚本来绘制图形。
  自己做的 canvas 项目
=======
  - 根据内容选择合适的标签，便于阅读和书写，举例：段落用 p，边栏用 aside，主要内容用 main 标签。
2. meta viewport 是做什么用的，怎么写？
  - 背：meta name="viewport" content="width=device-width(宽度等于设备宽度),
  user-scalable=no(用户不准放大缩小),initial-scale=1.0(一开始的倍数),
  maximum-scale=1.0(最大倍数), minimum=1.0(最小倍数)"
  - 作用：控制页面在移动端不要缩小显示。
3. canvas 元素是干什么的？
  - canvas 是 HTML5 新增的元素，可用于通过使用js中的脚本来绘制图形。
  - 自己做的 canvas 项目
    先添加一个 canvas 标签，再用 getContext（'2d'） 中的属性和方法，还有我这个画板是移动端和网     页都可以使用的，移动端我监听的事件是 ontouch，网页的是 onmouse。
>>>>>>> 3d5bd5dc522c0008902833a0b2276208279b1c86

//
CSS
1.(必考) 说说盒模型
<<<<<<< HEAD
  content-box: width === 内容区宽度
  border-box：width === 内容区宽度 + padding + border
=======
  - content-box: width === 内容区宽度
  - border-box：width === 内容区宽度 + padding + border
>>>>>>> 3d5bd5dc522c0008902833a0b2276208279b1c86
2. css reset 和 normalize.css 有什么区别？
  - reset 重置，抛弃默认样式。
  - normalize 让所有浏览器的标签都跟标准规定的默认样式一致，
    各浏览器上的默认标签样式基本统一。
3.(必考) 如何居中？
<<<<<<< HEAD
  水平居中：
    内联元素：爸爸身上写 text-align；center；
    块级元素：margin-left：auto；margin-right：auto；
  垂直居中：
    -table 自带功能
    -把 div 装成 table (display: table)
=======
  display: flex;
  justify-content: center;
  align-items: center;
  水平居中：
    内联元素：爸爸身上写 text-align；center；
    块级元素：margin：0 auto；
  垂直居中：
>>>>>>> 3d5bd5dc522c0008902833a0b2276208279b1c86
    -父元素：display：flex；
     子元素：align-self：center；
    -display：inline-block；
     vertical-align：middle；
    -父元素：position：relative；
     子元素：position：absolute；
            top：50%；
            transform：translateY（-50%）；
4. 选择器优先级如何确定？
  -选择越具体，优先级越高。
  -同样优先级，写在后面的覆盖前面的。
  -！important 优先级最高。
5. BFC 是什么？
  -overflow：hidden；清除浮动/取消父子 margin 合并
<<<<<<< HEAD
  -.clearfix:after {
=======
  -.clearfix::after {
>>>>>>> 3d5bd5dc522c0008902833a0b2276208279b1c86
      content: "\0020";
      display: block;
      height: 0;
      clear: both;
  }
<<<<<<< HEAD
  .clearfix::after {
    content: '';
    diaplay: block;
    clear: both;
  }
6. 如何清除浮动？
  -overflow：hidden；清除浮动/取消父子 margin 合并
  -.clearfix:after {/* 写在父亲身上 */
      content: "";
      display: block;
=======
6. 如何清除浮动？
  -overflow：hidden；清除浮动/取消父子 margin 合并
  -.clearfix::after {/* 写在父亲身上 */
      content: "";
      display: block;// 可以设置宽高 并独占一行
>>>>>>> 3d5bd5dc522c0008902833a0b2276208279b1c86
      clear: both;
  }
   .clearfix{
       zoom: 1;/* 兼容IE*/
   }
<<<<<<< HEAD

=======
7.css3 动画
  - @keyframe XXX {
    from{} to{}}
    animation: XXX 3s;
  - transform 有 translate 和 rotate 等方法，
    transtion 变化和时间
    
>>>>>>> 3d5bd5dc522c0008902833a0b2276208279b1c86
//
JS
1. JS有哪些数据类型？
  string bool symbol number undefined null object
  object 包括 数组、函数、正则、日期等对象。
2.(必考)Promise 怎么使用？
  -then 的用法
  $.ajax().then(成功函数，失败函数)
  -链式 then
  $.ajax().then(成功函数，失败函数).then(成功函数2，失败函数2)
  -如何自己生成 Promise
  function xxx() {
      return new Promise(function(resolve, reject) {
          setTimeout(() => {
              resolve() 或者 reject()
          },3000)
      })
  }
  xxx().then()
<<<<<<< HEAD

  function XXX() {
    return new Promise(function(resolve, reject) {
      setTimeout(() => {
        resolve() 或者 reject（）
      }, 3000)
    })
  }
   xxx().then()
=======
>>>>>>> 3d5bd5dc522c0008902833a0b2276208279b1c86
3.(必考) ajax手写
  let xhr = new XMLHttpRequest()
  xhr.open(method, path, true)
  xhr.onreadystatechange = function() {
<<<<<<< HEAD
    if(xhr.readState === 4 && xhr.status === 200) {
      console.log(xhr.responseText)
    }
  }
  xhr.send(data)

  let xhr = new XMLHttpRequest()
  xhr.open(method, path, true)
  xhr.onreadystatechage = function() {
    if(xhr.readState === 4) &&
    xhr.status === 200) {
      console.log(xhr.responseText)
    }
=======
      if(xhr.readState === 4 && xhr.status === 200) {
          console.log(xhr.responseText)
      }
>>>>>>> 3d5bd5dc522c0008902833a0b2276208279b1c86
  }
  xhr.send(data)
4.(必考) 闭包是什么？
  函数 和 函数内部能访问到的变量 的总和，就是一个闭包。
  function createAdder() {
    var n = 0
    return function() {
        n += 1
    }
  }
  let adder = createAdder()
  adder()// n === 1
  adder()// n === 2
  console.log(n)// n is not defined
<<<<<<< HEAD

  function a() {
    var x = 0
    return function() {
      x += 1
    }
  }
  var n = a()
  n()// x === 1
  n()// x === 2
=======
>>>>>>> 3d5bd5dc522c0008902833a0b2276208279b1c86
5.(必考) 这段代码里的 this 是什么？
  -fn() 里面的 this 就是 window
  -fn() 是 strict mode，this 就是 undefined
  -a.fn() 里面的 this 就是 a
  -new fn() 里面的 this 就是新生成的实例
  -fn() => console.log(this) 里面的 this 就是外面的 this
6.(必考) 什么是立即执行函数，使用立即函数的目的是什么?
  (function(){}())
  造出一个函数作用域，防止污染全局变量//声明局部变量
  相当于 ES6 中新语法 {let name}
7. async/await 语法了解吗？目的是什么？
  function returnPromise() {
      return new Promise(function(resolve, reject){
          setTimeout(() => {
              resolve('resolved');
          },3000)
      })
  }
  //用 then
  returnPromise().then((result) => {
      result === 'resolved'
  })
  //用 await
  var result = await returnPromise()
  result === 'resolved'

  目的是把异步代码写成同步代码。
8. 如何实现深拷贝？
  -JSON 拷贝
  var a = {}//对象
  var b = JSON.parse(JSON.stringify(a))
  //把对象变成字符串 再从字符串中生成一个对象
  缺点：JSON 不支持 函数、引用、undefined..
  -递归拷贝

9. 如何实现数组去重
  -Set 去重
  Array.from(new Set(a))
10. 如何使用正则实现 string.trim()
  function trim(string) {
    return string.replace(/^\s+|\s+$/,'')
  }

11. JS原型是什么？
  一个对象 通过原型 获得了一个函数或者属性
  -var a = [1, 2, 3]
   只有 0 1 2 length 4 个 key
   但是却可以 a.push(4) 那么 push 是哪来的呢
   a.__proto__ === Array.prototype
   push 就是沿着 a.__proto__ 找到的，也就是 Array.prototype.push
   Array.prototype 就是 a 的原型(__proto__)
12. ES6 中的 class ?
  看 MDN

13. JS 如何实现继承?
  -原型链
  function Animal() {
    this.body = '肉体'
  }
  Animal.prototype.move = function() {
  }
  function Human(name) {
    Animal.apply(this, arguments)//自身属性的继承
    this.name = name
  }
  
  var f = function() {}//原型属性继承
  f.prototype = Animal.prototype
  Human.prototype = new f()

  Human.prototype.use = function(){}

  var lu = new Human()

  -extends 关键字
  class Animal{
    constructor(){
      this.body = '肉体'
    },
    move(){}
  }
  class Human extends Animal{
    constructor(name) {
      super()
      this.name = name
    },
    ues(){}
  }
  var lu = new Human()

//
DOM
1. DOM 事件模型是什么？
  -冒泡
  -捕获
  -一般是先捕获，后冒泡。
  -如果这个元素是被点击的元素，那么捕获不一定在冒泡之前，
   顺序是由监听顺序决定的。
  -以下是三种方法
  -myButtom.addEventListener('click', function() {alert('hello world')}, false//false 是冒泡，true 是捕获)
  -<buttom onclick="alert('hello world')">
  -myButtom.onclick = function(event) {alert('hello world')}
2. 移动端的触摸事件了解吗？
  -touchstart touchmove touchend touchcancel
<<<<<<< HEAD
  -模拟 swipe 事件：记录两次 touchmove 的位置差，如果后一次在前一次的右边，说明向右了。
=======
  -模拟 swipe 事件：记录两次 touchmove 的位置差，
   如果后一次在前一次的右边，说明向右划了。
>>>>>>> 3d5bd5dc522c0008902833a0b2276208279b1c86
3. 事件委托是什么？有什么好处？
  通过监听一个父元素，来得知触发事件的子元素或者是给不同的子元素绑定事件，这就是事件委托。
  -优点：
   可以监听动态生成的子元素。
   减少监听次数，从而提升速度。

//
HTTP
1. HTTP 状态码知道那些？
  -1** 信息，服务器收到请求，需要请求者继续执行操作。
   100 继续
   101 切换协议
  -2** 成功，操作成功接受并处理。
   200 请求成功
   201 已创建
   202 已接受
  -3** 重定向，需要进一步的操作以完成请求。
   301 永久重定向
   302 临时重定向
  -4** 客户端错误，请求包含语法错误或无法完成请求。
   400 语法错误
   401 用户的身份认证
  -5** 服务器错误，服务器在处理请求过程中发生了错误。
   500 服务器内部错误
   501 服务器不支持请求的功能
2. HTTP 缓存怎么做？
  Cache-Control：max-age=300
3. Cache-Control 和 Etag 有什么区别？
  Cache-Control 请求完成后 响应体会保存 max-age 的时间长度，
  时间一到，就会重新请求服务器去拿数据。
  Etag 会对比本地和服务器端 MD5 的返回值，若一致，则不需要重新加载响应体，
  若不一致，则重新下载，当数据没有变化时，也会发送请求。
4. Cookie 是什么？ Session 是什么？
  -Cookie
   HTTP 响应通过 Set-Cookie 设置 Cookie
   浏览器访问指定域名时必须要带上 Cookie 作为 Request Header
   Cookie 一般用来记录用户数据
  -Session
   Session 是服务器端的内存 (数据)
   Session 一般通过在 Cookie 里记录 SessionID 实现
   SessionID 一般是随机数
5. LocalStorage 和 Cookie 的区别是什么？
  -Cookie 会随请求被发到服务器上，而 LocalStorage 不会。
  -Cookie 一般大小 4kb 以下，LocalStorage 一般 5Mb 左右。
6.(必考) GET 和 POST 有什么区别？
  -GET 用来读数据，POST 用来写数据，POST 不幂等。
  -参数 GET 的参数放在 url 的查询参数里，POST 的参数(数据)放在请求消息体里面。
  -安全 GET 没有 POST 安全。
  -包 GET 请求只需要发一个包 POST 请求需要发两个以上。
7.(必考)怎么跨域？JSONP 是什么？CORS 是什么？postMessage 是什么？
  -JSONP 是 JSON 的一种"使用模式"，可以让网页从别的域名(网站)那获取资料，
   即跨域读取数据。
  -CORS 是一个 W3C 标准，全称是跨域资源共享。它允许浏览器像跨源服务器发出 XMLHttpRequest 请求，
   从而克服了 AJAX 只能同源使用的限制。
  -window.postMessage 方法可以安全的实现跨源通信。


//
Vue
1.(必考) Vue 有哪些生命周期钩子函数？
  -beforeCreate 在实例初始化之后，数据观测（data observer）和 event/watcher 事件配置之前被调用。
  -created 在实例创建完成后被立即调用。在这一步，实力已经完成以下配置：数据观测，属性和方法的运算，
   watch/event 事件回调。
   然而，挂载阶段还没开始，$el 属性目前不可见。
  -beforeMount 在挂载开始之前被调用：相关的 render 函数首次被调用。
   该钩子在服务器端渲染期间不被调用。
  -mounted el 被新创建的 vm.$el 替换，并挂载到实例上去之后调用该钩子。如果 root 实例挂载了一个文档内元素，
   当 mounted 被调用时 vm.$el 也在文档内。
  -beforeUpdate 数据更新时调用，发生在虚拟 DOM 打补丁之前。这里合适在更新之前访问现有的 DOM，
   比如手动移除已添加的事件监听器。
   该钩子只有在初次渲染会在服务端进行
  -updated 由于数据更新导致的虚拟 DOM 重新渲染和打补丁，在这之后会用到该钩子。
   该钩子在服务器端渲染期间不被调用。
  -activated keep-alive 组件激活时调用。
  -deactivated keep-alive 组件停用时调用。
  -beforeDestroy 实例销毁之前调用，在这一步，实例仍然完全可用。
  -destoryed Vue实例销毁后调用。调用后，Vue 实例指示的所有东西都会解绑定，
   所有的事件监听器都会被移除，所有的子实例也会被销毁。
  -新增 errorCaptured 当捕获一个来自子孙组件的错误时被调用。此钩子会收到三个参数：错误对象、
   发生错误的组件实例以及一个包含错误来源信息的字符串。此钩子可以返回 false 以阻止该错误继续向上传播。
2.(必考) Vue 如何实现组件通信？
<<<<<<< HEAD
  -父子通信 Prop 传递数据、v-on 绑定自定义事件
  -爷孙通信
  -非父子通信 new vue（） 作为 eventbus（）
=======
  -父子通信
  -爷孙通信
  -非父子通信
>>>>>>> 3d5bd5dc522c0008902833a0b2276208279b1c86

3. Vuex 的作用是什么？
  转为 Vue 应用程序开发的状态管理模式，它采用集中式储存管理应用的所有组件的状态，
  并以相应的规则保证状态以一种可以测的方式发生变化。
  (例如购物车页面)
4. VueRouter 路由是什么？
  Vue 的单页面应用是基于路由和组件的，路由用于设定访问路径，并将路径和组件映射起来。传统的页面应用，
  是用一些超链接来实现页面切换和跳转的，在 Vue-Router 单页面应用中，则是路径之间的切换，
  实际上就是组建的切换。路由就是 SPA(单页应用) 的路径管理器。
5. Vue 的双向绑定是如何实现的？有什么缺点？
<<<<<<< HEAD
  - v-model
  Vue 的双向绑定是语法糖

6. Computed 计算属性的用法？跟Methods 的区别。
  - methods 是非响应式的一种交互方法，需要人为出触发。methods 没有缓存，只会在每次调用的时候执行。
  - computed 是响应式的计算属性，在检测到 data 数据变化时自动触发的。而且 computed 是带缓存的，
  只有其引用的响应式属性发生改变时才会重新计算。
=======
  

6. Computed 计算属性的用法？跟Methods 的区别。
  -
  -区别 methods 是一种交互方法，需要人为出触发。methods 没有缓存，只会在每次调用的时候执行。
       computed 是在检测到 data 数据变化时自动触发的。而且 computed 是带缓存的，
       只有其引用的响应式属性发生改变时才会重新计算。
>>>>>>> 3d5bd5dc522c0008902833a0b2276208279b1c86
      

//
算法
1. 排序算法
  -冒泡排序
  -选择排序
  -技术排序
  -快速排序
  -插入排序
  -归并排序

2. 二分查找法
<<<<<<< HEAD
  前提是个有序数组
  var Arr = [...]
  function binary(find, arr, low, high){
    if(low <= high) {
      if(arr[low] === find) {
        return low
      }
      if(arr[high] === find) {
        return high
      }
      var min = Math.ceil((high + low) / 2)
      if(arr[mid] === find) {
        return mid
      } else if (arr[mid] > find) {
        return binary(find,arr,low,mid-1)
      } else {
        return binary(find,arr,mid+1,high)
      }
    }
    return -1
  }
  binary(X, Arr, 0, Arr.length-1)
=======
>>>>>>> 3d5bd5dc522c0008902833a0b2276208279b1c86

3. 反转二叉树
  暂时不会没关系


//
安全
1. 什么是 XSS　攻击？如何预防？
<<<<<<< HEAD
  通过对网页注入可执行的代码且成功的被浏览器执行，达到攻击的目的。
  预防方法使用字符过滤。

2. 什么是 CSRF 攻击？ 如何预防？
  比如用户登陆了网页qq，随后切换到了一个恶意网站，恶意网站向用户提出加好友的申请，用户在不知不觉中加了好友。
  预防方法有 验证 http referer字段
  或者在请求地址添加 token 并验证
=======

2. 什么是 CSRF 攻击？ 如何预防？

>>>>>>> 3d5bd5dc522c0008902833a0b2276208279b1c86

//
Webpack
1. 转译出的文件太大怎么办？
  -使用 code split
   写法 import('xxx').then(xxx => {console.log(xxx)})
   xxx 模块就是按需加载的。
2. 转移速度慢怎么办？

3. 写过 Webpack loader 吗？


//
1. 从输入 url 到页面展现之间发生了什么？
  -DNS 查询
   建立 TCP 链接 (三次握手：建立连接、服务器收到 SYN 报文段、客户端收到 SYN+ACK 报文段。)
   发送 HTTP 请求 (请求的四部分：请求行 request line、请求头部 header、空行和请求数据四部分。)
   后台处理请求
    监听 80 端口
    路由
    渲染 HTML 模板
    生成响应
   发送 HTTP 响应
   关闭 TCP 连接 (四次挥手)
   解析 HTML
   下载 CSS
   解析 CSS
   下载 JS
   解析 JS
   渲染 DOM 树
   渲染样式树
   执行 JS
2. 你遇到过最难的问题？

3. 你的缺点和优点？
