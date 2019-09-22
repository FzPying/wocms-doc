## 目录描述

~~~
/ProjectDirectory       项目目录（或者子目录）
├─app                   应用目录（主要开发目录）
│   ├─Controller        控制器目录
│   ├─Exception         异常目录
│   ├─Listener          监管者目录（各种监听之类的，钩子）
│   ├─Model             模型
│   ├─Entity            实体（每个对应一个实体）
│   ├─Service           服务（各种数据服务）
│   ├─Logic             逻辑
│   └──...
├─config                 应用配置目录
│   ├── autoload                // 此文件夹内的配置文件会被配置组件自己加载，并以文件夹内的文件名作为第一个键值
│   │   ├── amqp.php            // 用于管理 AMQP 组件
│   │   ├── annotations.php     // 用于管理注解
│   │   ├── apollo.php          // 用于管理基于 Apollo 实现的配置中心
│   │   ├── aspects.php         // 用于管理 AOP 切面
│   │   ├── async_queue.php     // 用于管理基于 Redis 实现的简易队列服务
│   │   ├── cache.php           // 用于管理缓存组件
│   │   ├── commands.php        // 用于管理自定义命令
│   │   ├── consul.php          // 用于管理 Consul 客户端
│   │   ├── databases.php       // 用于管理数据库客户端
│   │   ├── devtool.php         // 用于管理开发者工具
│   │   ├── exceptions.php      // 用于管理异常处理器
│   │   ├── listeners.php       // 用于管理事件监听者
│   │   ├── logger.php          // 用于管理日志
│   │   ├── middlewares.php     // 用于管理中间件
│   │   ├── opentracing.php     // 用于管理调用链追踪
│   │   ├── processes.php       // 用于管理自定义进程
│   │   ├── redis.php           // 用于管理 Redis 客户端
│   │   └── server.php          // 用于管理 Server 服务
│   ├── config.php              // 用于管理用户或框架的配置，如配置相对独立亦可放于 autoload 文件夹内
│   ├── container.php           // 负责容器的初始化，作为一个配置文件运行并最终返回一个 Psr\Container\ContainerInterface 对象
│   ├── dependencies.php        // 用于管理 DI 的依赖关系和类对应关系
│   └── routes.php              // 用于管理路由
~~~