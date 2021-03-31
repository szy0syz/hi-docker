# hi-docker

## 基础

### 实现资源隔离

- `Docker`内部怎么实现资源隔离的？证明它！
  - `Namespace`
  - `Docker`并不是什么新技术，只是把 `linux` 的系统调用封装的很好用而已，就像资源隔离。
  - 原来用`Docker`时，真的是蹑手蹑脚的，理解了上面这句话后，豁然开朗了。

### 实现资源限制

- `Docker`内部用什么实现资源限制？如何证明？
  - `cgrounps`

### Docker镜像的特性

- Docker镜像具备了应用运行所需要的所有依赖
- 一次构建，处处运行
- Docker镜像的存储时基于 checksum 的去重存储，大大降低存储空间

## 动手开发自己的Docker

> 用`Golang`开发一个 `Jerry-Docker`
