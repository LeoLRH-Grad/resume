这份模板是可编辑的了。

所有的文字栏目都是可以随意编辑的：

![1-2.2-1](https://doc.shiyanlou.com/document-uid8834labid2084timestamp1472193804571.png)

点击图片可以通过图片的url地址替换：

![1-2.2-2](https://doc.shiyanlou.com/document-uid8834labid2084timestamp1472193923263.png)

替换后：

![1-2.2-3](https://doc.shiyanlou.com/document-uid8834labid2084timestamp1472193962395.png)

微信号不想留就把整个栏目删掉：

![1-2.2-4](https://doc.shiyanlou.com/document-uid8834labid2084timestamp1472194078738.png)

可增加新的条目：

![1-2.2-5](https://doc.shiyanlou.com/document-uid8834labid2084timestamp1472194174398.png)

可通过点击编辑进度条：

![1-2.2-6](https://doc.shiyanlou.com/document-uid8834labid2084timestamp1472194207572.png)

注意敏感信息不要发布在页面上，我们仅在需要打印简历时用到这些信息：

![1-2.2-7](https://doc.shiyanlou.com/document-uid8834labid2084timestamp1472195222729.png)

注意简历的内容不要超出背景的高度。

编辑完自己的简历以后，就把修改后的代码复制下来，替换掉原`index.html`里的代码。

Firefox 下：

打开查看器：

![1-2.2-8](https://doc.shiyanlou.com/document-uid8834labid2084timestamp1472743591122.png)

复制 html 标签的外部 HTML：

![1-2.2-9](https://doc.shiyanlou.com/document-uid8834labid2084timestamp1472743628808.png)

然后将`index.html`中的 html 标签的所有内容（包括 html 标签）替换掉即可。

我的本意是发布后的简历页面仍是可编辑的，这方便我日后直接在上面编辑手机等个人信息后保存打印。

不喜欢这样子的同学可以修改`static/js`下的`script.js`文件，操作非常简单，删除该文件下的所有内容，然后加上下面这一句。

```
$(document).ready(function($){
    $("*").removeAttr('contenteditable');        
})
```









接着在自己电脑上github上写一个项目然后用Settings里面的github pages选择一下master

Github Pages 支持托管的页面分两类，个人/组织页面 与 项目页面，其主要区别就是托管位置的区别。如下表所示（这里略去组织，它跟个人是差不多的）：

| 类型     | 页面域名 & 托管位置              | 页面源文件所在的分支                               |
| -------- | -------------------------------- | -------------------------------------------------- |
| 个人主页 | `username.github.io`             | `master`                                           |
| 项目主页 | `username.github.io/projectname` | `master`、`gh-pages` 、或是在`master`的`doc`目录下 |

如果想使用个人主页，那么就创建一个名为 `username.github.io` （username需要替换为你的用户名）的库，在主分支`master`上托管你的页面代码。

如果是使用项目主页，那么可以选择将代码托管在`master`、`gh-pages`、或者`master`的`doc`目录下，其中`gh-pages`是默认的页面托管分支，如果想使用`master`，可在项目页面的设置栏中进行切换。

![1-2.3-1](https://doc.shiyanlou.com/document-uid8834labid2084timestamp1472195842571.png)

无论使用哪一种页面操作都是差不多的，这里就用项目页面来做演示了，由于我们所有的代码就只有页面代码而已，那么就直接在`master`分支上进行托管吧。

先在本地仓库做一次代码提交：

```
$ git add .
$ git commit -m 'commit my cv'
```

在项目页面找到你的仓库地址后输入：

```
$ git remote add origin 你的远程仓库地址
$ git push -u origin master
```

代码提交到远程仓库后，在项目页面设置 Github Pages 使用的托管源。

![1-2.3-3](https://doc.shiyanlou.com/document-uid8834labid2084timestamp1472195989896.png)

现在你可以访问`https://LeoLRH-Grad.github.io/resume/`这个地址了，恭喜，简历页面已成功部署在了 Github Pages 上。



这个方法太麻烦还不如直接就在简历网上直接写就好啦（超级简历）这个我更建议写成项目经历和项目过程记录文档

这个还可以去尝试加入防一个pdf会是什么样？这个下次进行尝试

