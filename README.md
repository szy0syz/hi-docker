# hi-docker

## 基础

### 实现资源隔离

- `Docker`内部怎么实现资源隔离的？证明它！
  - `Namespace`
  - Docker 并不是什么新技术，只是把 `linux` 的系统调用封装的很好用而已，就像资源隔离。

### 实现资源限制

- `Docker`内部用什么实现资源限制？如何证明？
  - `cgrounps`
