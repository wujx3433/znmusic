zn music配置文件
====
# 概览
Zn Music是我创建的一个wiki站。众所周知，wiki站的基础建设比较复杂，所以我同步一部分源码到Git，方便以后调用。

内容解释
----
下面解释一下各个文件是干什么的。


# LocalSetting.php

这个文件是用来储存你的wiki的全站配置的，你的wiki要加载哪些extension、各个extension的参数配置都在这里填写。这个文件在根目录里。

# interwiki.sql

一看sql就知道这是一张数据库的表。interwiki中文翻译成“跨维基”，你可以理解成浏览器地址栏的搜索功能，只不过通配符从`%s`换成了`$1`。
以前wiki上编辑interwiki可以直接在`Special:Interwiki`编辑，只要你有相应权限就没问题；至少在1.31是可以的。不过我用的是1.34，这个功能的实现只能改表了。就很难受。

# DefaultSettings.php

这个文件保存的是全站的一些配置，位于`wiki根目录/includes`文件夹内。就如同我注释说的，你只需要关注947行即可。

947行的`$wgFileExtensions`控制着你能在`Special:Upload`里上传的文件类型。

另外，有问题请尽量先去[mediawiki官网](https://www.mediawiki.org/)扒拉一下，百度很难出有参考价值的内容，这些事情还是参考官方手册比较好。

再不济，去请教几位wiki站长。
