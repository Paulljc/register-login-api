# register-login-api
注册和登录功能的相关中间件使用

最近在学restful接口方面的知识，并且接触到了一些第三方库。
考虑到在实际项目中，注册和登录功能是比较常见的，所以就学了一些登录验证之类的库。
用 node.js + express 写写代码练练手，大家也可以学习学习，说不定工作中能用上。

#### 项目用到的第三方库

- jsonwebtoken 生成token验证字符串，Token中的payload是通过base64url编码的。具体可以参考我简书写的文章[jsonwebtoken](https://www.jianshu.com/p/f7e7b056f43d) (附中文文档)。
 
- validator 对用户输入的信息进行合法验证。有兴趣的顺便可以了解一下ES6的 [class-validator](https://www.npmjs.com/package/class-validator) 是可以通过使用装饰器进行编写。

- passport 是一个基于Nodejs的认证中间件。Passport目的只是为了“登陆认证”，因此，代码干净，易维护，可以方便地集成到其他的应用中。

- passport-jwt 验证生成的token字符串。

- gravatar 全球公认头像，Gravatar是一图像跟随著您到访过的网站，当您在博客中留言或发表文章，它将会出现在您的名称旁。

- bcrypt 用于密码加密。

---
#### 使用


`npm/cnpm install ` 安装依赖

`npm run start`	  启动项目  /  `npm run server` 使用nodemon启动项目(热更新)，注意需要全局安装该模块。

---
#### 测试
###### 使用postman对注册登录以及私有接口进行测试

注册 post / register

![register](testImg/register.PNG)

登录 post / login

![login](testImg/login.PNG)

当前用户 get / current (注意验证jwt需要把token放在请求头中的Authorization中)

![current](testImg/current.PNG)
