#技术选型规范
##数据库选型
###mysql 
  https://dev.mysql.com/downloads/mysql/ </br>
  版本>5.7.10 <8.0.0</br>
###redis
 版本 >3.2.0  <4.0.0</br>
##数据库安全和事物
1.原子性必须保证
2.事务性必须保证
 
#后端开发语言
1.对外提供接口开发语言选rust  网络协议http 对外传输数据格式提供json 主要和小程序的交互</br>
2.数据库ORM https://github.com/diesel-rs/diesel   </br>
3.数据库连接池 https://github.com/diesel-rs/r2d2-diesel</br>
4.web 框架选择sapper </br>
5.mvc</br>
6.</br>

#内部服务器通讯
交互传输格式 protobuf > 3.3  </br>
网络协议选http (是否2.0再议) </br>
解析库https://github.com/stepancheg/rust-protobuf </br>


##内部系统 
包括提供给商户的pc端部分 </br>
前端选 https://ant.design 前端代理nodejs > 7.10 版本 </br>
nodejs只提供代理不做业务逻辑，但提供拼接数据转protobuf到json和接口的缓存功能避免无限制请求后端接口 </br>
和后端rust语言交互传输格式 protobuf </br>
网络协议http  </br>


#JavaScript语法规范
必须基于es6  包括node  ant.design

#小程序规范
官方规范

#rust语法规范
官方规范

#原型图设计
Axure > 8.0

#程序发布
统一基于docker环境</br>
mysql 拉取官方镜像 数据保存和配置文件必须落在宿主机</br>
redis 拉取官方镜像 数据保存和配置文件必须落于宿主机 必须开启aof </br>
自己的二进制 rust二进制的docker环境只能包含最终编译出来的二进制文件 基于 alpine 打包  对外只能提供一个访问端口 和 配置文件必须从宿主机读取 日志文件必须落到宿主机</br>
前端打包webpack  其他的规范和ant.design一致</br>


#代码提交规范
基于github的流程</br>
1.fork  2.修改 提交通过request方式  提交前必须基于原始库master rebase一次</br>
2.开发功能基于git工作流规范 </br>
3.code review ...</br>





 
