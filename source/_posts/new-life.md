---
title: new life
date: 2020-02-22 19:13:02
tags:
---

### new life

hexo迁移--使用分分支保存源文件

重装系统，由于没有备份hexo的资源文件，导致之前日志丢失，哭死。现采用如下方案，对资源进行备份

1. 克隆wanerness1.github.io仓库到本地（命名为wanerness1-hexo），删除项目中的所有文件，仅留下.git文件
2. 将hexo文件夹下所有文件拷贝进来
3. git checkout -b hexo 切除一个新分支
4. git add .
5. git commit -m "hexo 分支"
6. git push --set-upstream origin hexo 推送到wanerness1.github.io仓库
7. 之后写日志在wanerness1-hexo里写，即：在hexo分支上运行：

```
    hexo new "new blog"
    
    //写好后  先运行add commit push ，推送到hexo分支保存
    hexo add .
    hexo commit -m 'xxx'
    hexo push


    //之后运行 hexo clean,hexo g,hexo d 进行部署（部署时会更新master分支）
    hexo clean
    hexo g
    hexo d
```

8. 换电脑时，就直接把创建的分支克隆下来，npm install安装依赖，在hexo分支进行开发即可。
```
git clone -b hexo https://github.com/wanerness1/wanerness1.github.io.git

```
https://blog.csdn.net/wxl1555/article/details/79293159