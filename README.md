# Vue_learning
## 理解Vue设计思想
首先要理解的是vue的设计理念是怎样的？在我眼里，组件化是vue最为成功的一项涉及。组件化这个特性把一整个网站都打散成了很小的一个又一个部分。举个例子，看目前的目录下，有三个文件：整个项目目录下的index.htm，src目录下的App.vue，和components文件夹下的Hello.vue.

理解这三者的关系很重要，Index是一个最外层的网站框架，它其实什么都没有，有一个head，head里边可以定义一些CSS一类的，然后body部分完全是空的，它仅仅载入了一个名字叫做app的vue module.

## App.vue
### 1.App.vue在HTML中使用router-link标签来导航，默认被渲染成一个a标签，通过传入to属性指定链接：

![image](https://github.com/lqAsuna/Vue_learning/blob/master/image/result1.png)

### 2.渲染后：在main.js中配置路由导入Vue和VueRouter，并调用Vue.use(VueRouter)
定义组件：import子组件：

![image](https://github.com/lqAsuna/Vue_learning/blob/master/image/result2.png)

定义路由：每个路由映射一个组件：

![image](https://github.com/lqAsuna/Vue_learning/blob/master/image/result3.png)

创建router实例：传入routes配置：

![image](https://github.com/lqAsuna/Vue_learning/blob/master/image/result4.png)

创建和挂载根实例：通过router配置参数注入路由，从而让整个应用都有路由功能：

![image](https://github.com/lqAsuna/Vue_learning/blob/master/image/result5.png)

### 3.在App.vue中添加router-view（最顶层的出口，渲染最高级路由匹配到的组件），使用keep-alive，把切换出去的组件保存在内存中，保留它的状态或避免重新渲染：

![image](https://github.com/lqAsuna/Vue_learning/blob/master/image/result6.png)

### 4.引入data.json中的数据：

![image](https://github.com/lqAsuna/Vue_learning/blob/master/image/result7.png)
      
### 5.引入header组件，并将seller数据传给header组件在JS中import header组件，并在components中注册，在template模板中使用header：

![image](https://github.com/lqAsuna/Vue_learning/blob/master/image/result8.png)
