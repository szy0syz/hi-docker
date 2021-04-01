# hi-docker

## 基础

### 实现资源隔离

- `Docker`内部怎么实现资源隔离的？证明它！
  - `Namespace`
  - `Docker`并不是什么新技术，只是把 `linux` 的系统调用封装的很好用而已，就像资源隔离。
  - 原来用`Docker`时，真的是蹑手蹑脚的，理解了上面这句话后，豁然开朗了。

`Namespace` 是 Linux 内核的一个特性，该特性可以实现在同一主机系统中，对进程 ID、主机名、用户 ID、文件名、网络和进程间通信等资源的隔离。`Docker` 利用 `Linux` 内核的 `Namespace` 特性，实现了每个容器的资源相互隔离，从而保证容器内部只能访问到自己 `Namespace` 的资源。

目前 `Linux5.6` 内核中共有8种类型的 `Namespace`，但最新版的 `Docker` 中只使用了其中的6中，分别为： 

- `Mount Namespace` 隔离挂载点
- `PID Namespace` 隔离进程ID
- `Net Namespace` 隔离网络设备、端口号等
- `IPC Namespace` 隔离 System V IPC 和 POSIX message queues
- `UTS Namespace` 隔离主机名和域名
- `User Namespace` 隔离用户和用户组

### 实现资源限制

- `Docker`内部用什么实现资源限制？如何证明？
  - `cgrounps`

## 开发自己的Docker

> 用`Golang`开发一个 `Jerry-Docker`
