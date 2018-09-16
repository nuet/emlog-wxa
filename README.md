# emlog小程序版客户端

该小程序主要有文章列表，文章详情，板块展示，博客信息展示等功能。

## 更新

- 2018年5月1日
	- 将评论功能去除，只留评论列表（个人账号不能做评论，审核不通过）
	- 将登录功能去除，因为不用添加评论，就不用调用用户信息
	- 将wxParse去除，换用官方的rich-text组件，修复文章不显示的bug
	- 将首页的博客信息改成由api调用，不用手动修改代码了。
	- 将获取文章列表由获取某一个分类下的文章，改成获取所有的文章。

- 2018年9月16日
  - 将博客的接口对接到了emlog的一个插件上
  - 重新规划功能，将首页去除，直接显示文章列表。
  - 文章列表对无图/单图/多图的文章自动适应。
  - api插件获取：`http://emapi.zhangziheng.com/`

## 部署

部署该小程序， 需要进行以下几个步骤的修改

0. 在微信小程序开发工具中导入该项目，填入appid等信息。
1. 修改utils/api.js中的API根域名 `domain` 为自己emlog博客的域名地址。
2. 在`http://emapi.zhangziheng.com/`中下载api插件，里面是一个`api.php`文件，将该文件放到自己博客的根目录即可。(注意:跟别的插件安装方式不一样)
3. 通过微信小程序开发工具， 上传并在后台审核

> 需要注意的是，小程序要求接口必须是https协议。要上线的话，必须给博客加https

## API文档地址

http://emapi.zhangziheng.com/

文档尚在更新中，如有不完善的地方可以联系我.