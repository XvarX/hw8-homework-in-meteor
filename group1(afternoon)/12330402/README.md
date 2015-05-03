# My Homework

一个简单的作业管理系统

## 测试账号

1. 学生
  * 用户名：test
  * 密码：123456
  * 注册了课程，提交了部分作业
2. 老师
  * 用户名：test2
  * 密码：123456
  * 注册了课程，批改了部分作业
3. 学生
  * 用户名：test3
  * 密码：123456
  * 注册了课程，提交了部分作业，漏交了部分作业

## 运行

在项目目录下运行 `meteor`, 访问`http://localhost:3000/`。
部分包在 Windows 下或者校园网下会下载/安装失败，放了替代品在 `packages` 文件夹内。

## 其他

新注册的用户需要在后台设置教师权限，在 `meteor mongo` 下

```
> db.users.find()  // 查看已有用户
> db.users.update({username: '需要更新的用户名'}, {$set: {isTeacher: true}})
```

新用户默认自动添加到“软件过程改进”课程