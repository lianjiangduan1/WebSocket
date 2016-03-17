WebSocket简介
谈到Web实时推送，就不得不说WebSocket。在WebSocket出现之前，很多网站为了实现实时推送技术，通常采用的方案是轮询技术的改进，Comet又可细分为两种实现方式，一种是长轮询机制，一种称为流技术，这两种方式实际上是对轮询技术的改进，这些方案带来很明显的缺点，需要由浏览器对服务器发出HTTP request，大量消耗服务器带宽和资源。面对这种状况，HTML5定义了WebSocket协议，能更好的节省服务器资源和带宽并实现真正意义上的实时推送。
WwbSocket协议本质上是一个基于TCP的协议，它由通信协议和编程API组成，WebSocket能够在浏览器和服务器之间建立双向链接，以基于事件的方式，赋予浏览器实时通信能力，既然是双向通信，就意味着服务器和客户端可以同时发送并响应请求，二不再像HTTP的请求和响应。
为了建立一个WebSocket连接，客户端浏览器首先要向服务器发起一个HTTP请求，这个请求和通常的HTTP请求不同，包含了一些附加头信息，其中附加头信息”Upgrade:WebSocket“表明这是一个申请协议升级的HTTP请求，服务器端解析这些附加的头信息然后返回给客户端，客户端和服务器端的WebSocket连接就建立起来了，双方就可以通过这个连接通道自由的传递信息，并且这个连接会持续存在直到客户端或者服务器端的某一方主动的关闭连接。
搭建WebSocket服务端
1、新建一个名为 package.json的文件
2、接下来使用npm命令安装express和socket.io
npm install --save express
npm install --save socket.io
3、编写服务端代码index.js
4、命令行运行 node index.js
5、编写客户端代码index.html(包含一些css、js)