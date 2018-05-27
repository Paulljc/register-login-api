# register-login-api
注册和登录功能的相关中间件使用

最近在学restful接口方面的知识，并且接触到了一些第三方库。
考虑到在实际项目中，注册和登录功能是比较常见的，所以就学了一些登录验证之类的库。
用 node.js + express 写写代码练练手，大家也可以学习学习，说不定工作中能用上。

#### 涉及的第三方库

- body-parser	bodyParser.json() - 解析JSON格式  请求体解析后，解析值都会被放到req.body属性，内容为空时是一个{}空对象。
		        bodyParser.raw() - 解析二进制格式
		        bodyParser.text() - 解析文本格式
		        bodyParser.urlencoded() - 解析文本格式	extended - 当设置为false时，会使用querystring库解析URL编码的数据；
            当设置为true时，会使用qs库解析URL编码的数据。后没有指定编码时，使用此编码。默认为true
            
- validator 对用户输入的信息进行合法验证。有兴趣的顺便可以了解一下ES6的 class-validator 是可以通过使用装饰器进行编写。

- jsonwebtoken 生成token验证字符串，Token中的payload是通过base64url编码的。具体可以参考我简书写的文章(jwt)[https://www.jianshu.com/p/f7e7b056f43d]

- passport 是一个基于Nodejs的认证中间件。Passport目的只是为了“登陆认证”，因此，代码干净，易维护，可以方便地集成到其他的应用中。

- passport-jwt 验证生成的token字符串。

- gravatar 全球公认头像，Gravatar是一图像跟随著您到访过的网站，当您在博客中留言或发表文章，它将会出现在您的名称旁。

- bcrypt 用于密码加密。
