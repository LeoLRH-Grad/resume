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