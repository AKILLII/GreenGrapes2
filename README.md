# GreenGrapes2
一款有科技感颗粒、自定义头像的、功能丰富的、好看的标签云的typecho绿色主题
修改自[https://github.com/hongweipeng/GreenGrapes](https://github.com/hongweipeng/GreenGrapes "https://github.com/hongweipeng/GreenGrapes")

![](http://i.imgur.com/dD8mg7T.png)

## 使用方法 ##
1. 下载Typecho主题，得到一个文件夹
2. 重命名整个文件夹为`GreenGrapes2`并上传至`usr/themes/`目录下
3. 登陆自己的博客后台，在“控制台”的下拉菜单中选择“外观”选项进入已安装主题列表
4. 在相应的主题点击“启用”即可使用

**注意：在主题目录下请注意一个权限足够的名为`avatarCache`的目录，用来存放头像缓存。
所谓权限足够就是PHP有足够的权限写入文件，一般也就是www:www/755或者干脆777**

## 增加的功能与特色 ##
* 增加了分享功能（插件来自于[river](https://github.com/revir/need-more-share2)）
* 页面和文章访问量统计（不需要插件）
* 改变协议为CC-BY-NC-SA4.0
* 去除页面最下方的备案信息、改成动态的颜文字
* 增加`meta theme color`使Chrome变色
* 增加侧边后台管理
* 启用侧边分类
* 启用页脚加载耗时
* 启用页脚运行时间
* 增加编辑按钮
* 增加字数统计
* 增加最后更新时间
* 增加文章数量统计
* 增加评论框特效（可以在主题中设置是否启用）
* 增加网站运行时间
* 评论头像QQ邮箱和Gravatar同时启用：优先QQ头像，然后是Gravatar，再之后是默认。已经启用了gravatar和QQ头像的缓存策略，所以基本上不会对网站速度有太大影响
* 主题增加设置缓存时间、设置建站日期
* 随机缩略图（分辨率为300*169）：如果文中包含图片的话，将会显示第一张图片作为背景；否则随机选择。请注意：只有在Typecho中添加的图片才会显示，如果是插入的外部图片，将被视为没有图片。
* 增加了404页面的动画选择
* 增加页面加载动画
* 新文章使用new标签（魔术棒）
* 评论区可以设置显示UA、不显示UA、显示带图UA、为博主显示UA和图片。默认为为博主显示UA和图片
* 可选隐藏侧边博主回复
* 增加面包屑导航功能
* 两种新的markdown语法支持：拼音、高亮：不知为何在某些环境版本上的Typecho，默认markdown引擎对于`~~删除线~~`的渲染会失败，所以主题暂时不开启渲染删除线而使用自带的引擎渲染。
* 站点统计功能，可以从百度统计等出粘贴代码，当然，不要粘贴进去自己想说的话，那样页面顶端会出现一些奇怪的东西。
* 三个杂项功能：平滑滚动效果、链接以新标签页形式打开、引用 Pangu.js 实现中英文间自动添加空格
* 页脚社交网络、自定义版权信息
* 主题增加自带表情（可以与similies共存）、侧边和代码等细节优化
* 增加灯箱支持（使用的是功能更强大更简洁的slimbox2）
* 主题内嵌支持友情链接并可选显示友链的favicon：使用A标签添加即可，如果Links插件存在那此项则无效。**注意，如果切换到其他主题，将会导致此项设置丢失，请谨慎选择。**
* 侧边文章存档
* 添加网易云音乐的支持，只需要在文章页面使用`{{音乐id}}`即可，默认不自动播放。
* 集成notice（来路判断）插件
* 集成kiana插件：移动版默认不加载（二级目录需要手动修改`bga.min.js`为正确的路径）
* 集成snow插件（移动版和文章内容包含视频的时候将会默认禁用）
* 集成代码高亮SyntaxHighlighter插件，使用方法，使用PHP、Bash、Python、CPP等指定渲染模式，如不填写则使用`plain text`模式渲染高亮。
* 可以开启访客天气预报：根据访客IP获取，缓存时间内第一次运行性能上会增加100ms-800ms不等的PHP运行时间。
* 支持动态格言
* 增加打赏功能
* 支持回复可见功能
* HTML代码压缩功能
* 复制版权提示

## To do ##
- [ ] 点赞：暂时不打算添加
- [x] 集成各种插件：目前已经集成或实现kiana、notice、Links、similies、Snow灯箱、SyntaxHighlighter
- [x] 404页面的加载动图问题：已修复
- [x] 优化天气预报性能：使用cookies
- [x] 评论区代码高亮无视语言指令，总是渲染成plain模式

## Q&A ##
1. Q：文章底部版权信息的范例
A：如下，这里支持全部HTML语法，尽管如此，但是在这里加JS可能不太好，JS请加到上面的站点统计上。
```
文章版权归 <a href='{{homepage}}'>{{name}}</a> 所有，
本站默认采用 <a class="alert-link" target="_blank" href="https://creativecommons.org/licenses/by-nc-sa/4.0/">CC-BY-NC-SA 4.0</a>授权，
转载必须包含本声明，并以超链接形式注明原作者和本文原始地址：
<a href='{{link}}'>《{{title}}》</a>
```
2. Q：有的时候设置不生效是咋回事？
A：由于Typecho的一些限制，需要先切换到其他主题，然后再切换回本主题。注意，这样操作将会导致你**丢失全部自定义配置**。

3. Q：如何恢复初始配置？
A：如上，切换到其他主题、再切换回来即可。

4. Q：主题自动更新检查是个啥？
A：就是会和GitHub上的版本号进行比对，如果是新版本会有提示，仅仅是提示而已

5. Q：SNS数量太少了/图标不好看
A：嗯……以后可以考虑可以加上国内的微信、QQ什么的吧；图标来自`fontawesone`，那里没有的我基本上也就不会加了。

6. Q:OwO表情插入之后不显示啊，已经允许`img`标签了
![](http://i.imgur.com/8Ddj9BK.png)
A：这个问题曾经让我一度头疼，在我本地Apache+PHP+MySQL的环境下，`Typecho 1.0 (14.10.10)`没有出现这个问题，但是在服务器上Nginx+PHP+MySQL就出现了这个问题。我的解决方法是升级到`Typecho开发版1.1 (17.4.24)`（2017年5月25日）或者重装Typecho，可能由于某些原因你修改了Typecho的代码、或者是稳定版中存在的bug导致这个问题。

7. Q:评论如何设置允许markdown语法？
A:设置-评论-在评论中使用markdown语法，允许使用的内容和标签，如下内容即可：
`<blockquote><pre><code class=""><strong><em><h3><h4><h5><h6><a href title><table><thead><tr><th><tbody><td><img src="">`

8. Q:最好的更新方式是什么？
A:建议`git clone`本仓库，每次收到更新只要切换到对应的主题目录，运行`git pull`就会是最新版本了。

## 更新历史 ##
我可没工夫写这玩意，直接看Git就得了。

## 演示 ##
[奔跑的蜗牛壳](https://www.tougetu.com)

## 更多说明 ##

[戳我](https://www.bennythink.com/greengrapes2.html)来获得更多说明

## 许可证 ##
已与原作者沟通确认使用 Apache License 2.0，感谢[原作者](https://github.com/hongweipeng/GreenGrapes) 的设计！
