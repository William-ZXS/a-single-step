#cookie&sessionStorage&localStorage

## 三者区别

**1）存储大小**

cookie：一般不超过4K（因为每次http请求都会携带cookie、所以cookie只适合保存很小的数据，如会话标识）

sessionStorage：5M或者更大

localStorage：5M或者更大

**2）数据有效期**

cookie：一般由服务器生成，可以设置失效时间；若没有设置时间，关闭浏览器cookie失效，若设置了时间，cookie就会存放在硬盘里，过期才失效

sessionStorage：仅在当前浏览器窗口关闭之前有效，关闭页面或者浏览器会被清除

localStorage：永久有效，窗口或者浏览器关闭也会一直保存，除非手动永久清除，因此用作持久数据

**3）作用域**

cookie：在所有同源窗口中都是共享的

sessionStorage：在同一个浏览器窗口是共享的（不同浏览器、同一个页面也是不共享的）

localStorage：在所有同源窗口中都是共享的

**4）通信**

ccokie：十种携带在同源的http请求中，即使不需要，故cookie在浏览器和服务器之间来回传递；如果使用cookie保存过多数据会造成性能问题

sessionStorage：仅在客户端（即浏览器）中保存，不参与和服务器的通信；不会自动把数据发送给服务器，仅在本地保存

localStorage：仅在客户端（即浏览器）中保存，不参与和服务器的通信；不会自动把数据发送给服务器，仅在本地保存

**5）易用性**

cookie：需要自己进行封装，原生的cookie接口不够友好

sessionStorage：原生接口可以接受，可以封装来对Object和Array有更好的支持

localStorage：原生接口可以接受，可以封装来对Object和Array有更好的支持

 

## 应用场景

cookie：判断用户是否登录过网站，以便实现下次自动登录或记住密码；保存事件信息等

sessionStorage：敏感账号一次性登录；单页面用的较多（sessionStorage 可以保证打开页面时 sessionStorage 的数据为空）

localStorage：常用于长期登录（判断用户是否已登录），适合长期保存在本地的数据