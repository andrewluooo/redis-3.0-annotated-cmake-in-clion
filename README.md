# 使用CLion调试redis源码
# Using clion to debug redis source code to better understand how Redis works.

## 参考

Reference: `https://github.com/htw0056/redis-3.0-annotated-cmake-in-clion` .
Add `CMakeList.txt` for Redis

`CLion`使用`CMake`来管理编译，而redis源码本身使用`make`，因此直接将redis源码导入`CLion`无法直接运行，需要配置`CMake`。

由于学习过程中参考的书籍为[《Redis 设计与实现》](http://redisbook.com/)，因此源码版本也跟本书保持一致。

## 步骤

### 下载源码

```shell
git clone https://github.com/andrewluooo/redis-3.0-annotated-cmake-in-clion.git
```
