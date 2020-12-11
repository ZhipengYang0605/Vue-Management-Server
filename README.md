#### 1.下载或clone代码到本地

#### 2.后端启动说明

1.1 安装‘连接数据库用的App’目录中的phpStudy.exe

1.2 安装成功后启动， 按照如下进行连接数据库

[img]http://chuantu.xyz/t6/741/1607692213x989559133.png[/img]

<img src=".\连接数据库用的App\1.png" alt="1" style="zoom:50%;" />



<img src=".\连接数据库用的App\2.png" />



![](.\连接数据库用的App\3.png)

下面这个界面过一会自己会关闭

<img src=".\连接数据库用的App\4.png" style="zoom:80%;" />

![](.\连接数据库用的App\5.png)

1.3 cd到目录vue_api_server

1.4 npm install 安装包

1.5 输入node app.js启动项目

#### 3.项目整体文件说明

- `config` 配置文件目录
  - `default.json` 默认配置文件（其中包含数据库配置，jwt配置）
- `dao` 数据访问层，存放对数据库的增删改查操作
  - `DAO.js` 提供的公共访问数据库的方法
- `models` 存放具体数据库 ORM 模型文件
- `modules` 当前项目模块
  - `authorization.js` API权限验证模块
  - `database.js` 数据库模块（数据库加载基于 nodejs-orm2 库加载）
  - `passport.js` 基于 passport 模块的登录搭建
  - `resextra.js` API 统一返回结果接口
- `node_modules` 项目依赖的第三方模块
- `routes` 统一路由
  - `api` 提供 api 接口
  - `mapp` 提供移动APP界面
  - `mweb` 提供移动web站点
- `services` 服务层，业务逻辑代码在这一层编写，通过不同的接口获取的数据转换成统一的前端所需要的数据
- `app.js` 主项目入口文件
- `package.json` 项目配置文件