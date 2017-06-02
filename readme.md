
# 数据库选型
## mysql 
* 版本 5.7.10 ~ 8.0.0
## redis
* 版本 >3.2.0  <4.0.0
## 数据库安全和事物
* 原子性必须保证
* 事务性必须保证

# 开发语言选型
## Rust
* 版本 最新稳定版
## JavaScript
* 版本 ES6


# 前端选型
## 小程序
* 官方原型
## 管理后台
* https://ant.design

# 运行环境选型
## 服务器 
* 版本 Centos 7.2
## docker
* 版本 最新稳定版

# 传输协议选型
* http
* websocket (再议)

# 传输数据格式选型
* json
* protobuf

# 原型图工具
## Axure 
* 版本 > 8.0


# rust技术选型
* 对外提供接口开发语言选rust  网络协议http 对外传输数据格式提供json 主要和小程序的交互
* mysql数据库ORM https://github.com/diesel-rs/diesel   
* mysql数据库连接池 https://github.com/diesel-rs/r2d2-diesel
* redis连接库 https://github.com/mitsuhiko/redis-rs
* redis连接池 https://github.com/sorccu/r2d2-redis
* web 框架选择sapper 
* mvc


# 内部服务通讯规范
* 交互传输格式 protobuf >= 3.3  
* 网络协议选http (是否2.0再议) 
* 解析库https://github.com/stepancheg/rust-protobuf 


# 内部系统规范 -管理后台 -商户后台 
* 前端选 https://ant.design 
* 传输数据格式 json
* 网络协议 http 
* 后端走rust规范


# rust语法规范
* 官方规范

# JavaScript代码规范
* 必须基于es6 

# 小程序代码规范
* 官方规范

# 架构设计规范
## 微服务
 * 服务之间保持独立性
## 水平扩展
 * 最差情况能通过增加配置来支撑系统增长
## mvc
 * 前后端完全分离


# 程序发布规范
统一基于docker环境
* mysql 
拉取官方镜像 数据保存和配置文件必须落在宿主机
* redis 
拉取官方镜像 数据保存和配置文件必须落于宿主机 必须开启aof 
* 服务二进制 
rust二进制的docker环境只能包含最终编译出来的二进制文件 基于 alpine 打包  对外只能提供一个访问端口 和 配置文件必须从宿主机读取 日志文件必须落到宿主机
* 前端打包webpack  
其他的规范和ant.design一致


# 代码提交规范
基于github的流程
* 1.fork  2.修改 提交通过request方式  提交前必须基于原始库master rebase一次
* 开发功能基于git工作流规范 
* code review ...





 
