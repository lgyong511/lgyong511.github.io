# [戚家山成人学校报名服务平台](https://codeup.aliyun.com/650031d2a42f1442323e2e64/registration-qjs.git)

----
这是前后端部署说明。部署使用helm chart包
----

## 部署环境要求
----
1、必须有一个MySQL，数据库名称：exam。
2、必须有一个minio公开的桶，桶名称：exam。
3、必须有redis、rabbitmq中间件。
4、安装heml3工具
----

## 添加helm仓库
```
helm repo add qjs https://lgyong511.github.io/charts
```

## 部署后端
```
helm install edu-qjs qjs/edu-qjs
```

## 部署前端
```
helm install web-qjs qjs/web-qjs
```

## 注意事项
----
1、前端部署时注意修改后端和minio地址和端口号。
2、后端没有做配置分离，部署时要确认好mysql、中间件等信息（地址、端口号、账号等）。
----