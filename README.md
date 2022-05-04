# Hexo

## 1、Hexo安装
```bash
$ npm install hexo -g
```
## 2、Hexo升级
更新hexo到最新版

```bash
$ npm update hexo -g
```

## 3、Hexo初始化

```bash
$ hexo init <folder>
```
如果指定，便会在目前的资料夹建立一个名为的新文件夹；否则会在目前资料夹初始化。

## 4、Hexo生成网站

```bash
$ hexo g
```
## 5、Hexo启动本地服务

```bash
$ hexo s
```

启动服务后，就可以访问：http://localhost:4000/（port 预设为 4000，可在 _config.yml 设定）

## 6、HexoRSS订阅
命令行切换到hexo博客根目录，安装

```bash
$ hexo-generator-feed
```

```bash
$ npm install hexo-generator-feed --save
```

在博客目录的_config.yml中添加如下代码

```
## feed   
feed:
  type: atom
  path: atom.xml
  limit: 20
  hub:
  content:
```
## Hexositemap站点地图
命令行切换到hexo博客根目录，分别用下面两个命令来安装针对谷歌和百度的sitemap插件

```bash
    $ npm install hexo-generator-sitemap --save
    $ npm install hexo-generator-baidu-sitemap --save
```

在博客目录的_config.yml中添加如下代码

```
## sitemap
sitemap:
  path: sitemap.xml
baidusitemap:
  path: baidusitemap.xml
```

## 7、Hexo部署步骤
每次部署的步骤，可按以下三步来进行。

```bash
$ hexo clean
$ hexo generate
$ hexo deploy
```

## 8、Hexo一些常用命令：

```bash
$ hexo new "postName" #新建文章
$ hexo new page "pageName" #新建页面
$ hexo generate #生成静态页面至public目录
$ hexo server #开启预览访问端口（默认端口4000，'ctrl + c'关闭server）
$ hexo deploy #将.deploy目录部署到GitHub
$ hexo help  # 查看帮助
$ hexo version  #查看Hexo的版本
```