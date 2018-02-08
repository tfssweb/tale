# theme-handsome for tale
[handsome](https://www.ihewro.com/ 'handsome') 是由 [友人c](https://www.ihewro.com/ '友人c') 设计的一套基于 Typecho 的主题，在此感谢作者授权给 tale

> 主题说明

主题采用全站 Ajax 无刷新交互方式构建，在原版基础上删除了一些不必要的模块

增加颜文字和自定义表情的导入

使用方法请参考[主题使用说明](https://github.com/otale/tale.git '主题使用说明')

下载完主题之后请修改文件，为了解决分类页面下无法进行分页的BUG

`resources/templates/comm/macros.html`

原代码
```
#for(navIndex : pageInfo.navPageNums)
<li #if(pageInfo.pageNum== navIndex) class="current" #end><a href="/page/${navIndex}">${navIndex}</a></li>
#end
```

替换后
```
#for(navIndex : pageInfo.navPageNums)
#if(pageInfo.hasNextPage)
<li #if(pageInfo.pageNum== navIndex) class="current" #end><a href="/${prefix}/${navIndex}">${navIndex}</a></li>
#else
<li #if(pageInfo.pageNum== navIndex) class="current" #end><a href="/page/${navIndex}">${navIndex}</a></li>
#end
#end
```


> 已知问题

* 目前存在唯一的缺陷是评论无法回复，该功能后续会尽快添加
* 搜索好像并没有什么作用（与主题无关）
* 调用随机文章会出现系统错误（与主题无关）
* 无法正确获取文章的评论数量（与主题无关）

> 预览

![](https://i.loli.net/2017/09/04/59ad24b668cd3.png)

![](https://i.loli.net/2017/09/04/59ad24b1d2620.png)

![](https://i.loli.net/2017/09/04/59ad24b54d70d.png)

![](https://i.loli.net/2017/09/04/59ad24b51e16d.png)

![](https://i.loli.net/2017/09/04/59ad24b268ea9.png)

![](https://i.loli.net/2017/09/04/59ad24aecf52c.png)

![](https://i.loli.net/2017/09/04/59ad24aecefaf.png)

![](https://i.loli.net/2017/09/04/59ad24aecee7d.png)