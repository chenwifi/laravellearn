### laravel的一些问题

1. 在你的中间件上调用 terminate 调用时，Laravel 会从 服务容器 中解析出一个新的中间件实例。如果要在调用 handle 和 terminate 方法时使用同一个中间件实例，就使用容器的 singleton 方法向容器注册中间件。(如何理解中间件中的这句话)
2. 容器的实例化是如何实现的？也就是make方法的实现。
3. helpers的文件是什么时候引入的？
4. router的实例已经有路径的内容，是何时如何放进去的？（我猜测是路由提供者那里，到时候看一下）。