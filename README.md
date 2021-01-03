# 使用CLion调试redis源码
# Using clion to debug redis source code to better understand how Redis works.

link：[https://github.com/andrewluooo/redis-3.0-annotated-cmake-in-clion]()

### 阅读和学习源码最好先将代码跑起来

## 参考

Reference: `https://github.com/htw0056/redis-3.0-annotated-cmake-in-clion` .

Add `CMakeList.txt` for Redis

`CLion`使用`CMake`来管理编译，而redis源码本身使用`make`，因此直接将redis源码导入`CLion`无法直接运行，需要配置`CMake`。

由于学习过程中参考的书籍为[《Redis 设计与实现》](http://redisbook.com/)，因此源码版本也跟本书保持一致。

## 步骤

### 下载源码

Download source code

```shell
git clone https://github.com/andrewluooo/redis-3.0-annotated-cmake-in-clion.git
```

### 设置断点
### Set Break Points

For examples, to debug reids command
```
set key value
```
you can find the function `void setCommand(redisClient *c)` and set a break point in it.

![image](https://github.com/andrewluooo/redis-3.0-annotated-cmake-in-clion/blob/main/IMG/clionDebugRedis_setCommand.png)

### 开启调试
### Start Debug Redis-Server

![image](https://github.com/andrewluooo/redis-3.0-annotated-cmake-in-clion/blob/main/IMG/clionDebugRedis01.png)

Service started successfully

![image](https://github.com/andrewluooo/redis-3.0-annotated-cmake-in-clion/blob/main/IMG/clionDebugRedis_startServer.png)

### 启动Redis-cli
### Start Redis-cli

Start the client in the file `cmake-build-debug` and input a command such as `set hello hi`

![image](https://github.com/andrewluooo/redis-3.0-annotated-cmake-in-clion/blob/main/IMG/clionDebugRedis_startClient.png)

Successfully stop at break point!

![image](https://github.com/andrewluooo/redis-3.0-annotated-cmake-in-clion/blob/main/IMG/clionDebugRedis_breakPoint.png)
