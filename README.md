![avatar]()


## 介绍

前台功能:

- 登录、注册
- 商品浏览
- 下订单、购买

商户后台功能:

- 商户管理
- 团购商品管理
- 商户入驻管理

总后台功能:

- 用户、商户管理
- 团购商品管理
- 订单管理
- 推荐位管理



## 安装教程

环境要求:

- PHP >= 5.5.9

## 步骤

步骤一  
先导入根目录下的o2o.sql数据库文件

步骤二  
配置数据库，打开 application/database.php 文件，修改下面的内容：

```
  'type'           => 'mysql',
    // 服务器地址
    'hostname'       => 'localhost',
    // 数据库名
    'database'       => 'o2o',
    // 用户名
    'username'       => 'root',
    // 密码
    'password'       => 'root',
    // 端口
    'hostport'       => '3306',
```




步骤1  
设置 public/upload 目录和 runtime  权限为 777

```
chmod -R  777 public/upload
chmod -R  777 runtime 
````

步骤2  
配置伪静态并设置 meedu 的运行目录为 public 。

伪静态规则（Nginx）：

```
location / {
	try_files $uri $uri/ /index.php$is_args$query_string;
}
```


步骤3  
到这里，网站可以正常访问了。

后台登录地址：http://youdomain.com/admin/Index/index  
超级管理员账号: admin  密码:admin
