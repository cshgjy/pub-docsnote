## gitbook套件
[![](https://i.loli.net/2019/06/12/5d00c41e49dd542918.jpg)](https://www.lanzous.com/i4jhgja)
[![](https://i.loli.net/2019/06/12/5d00c4b5da92788640.jpg
)](https://darrenliuwei.com)
**bili视频教程：**
[1-什么是gitbook](https://www.bilibili.com/video/av26443858/?spm_id_from=333.788.videocard.3)
[2-安装使用gitbook](https://www.bilibili.com/video/av26450301?from=search&seid=11973058513650996244)
[3-简单书写](https://www.bilibili.com/video/av26457728/?spm_id_from=333.788.videocard.2)
[4-gitbook插件](https://www.bilibili.com/video/av26462561/?spm_id_from=333.788.videocard.1)
[5-部署到GitHub](https://www.bilibili.com/video/av26479800/?spm_id_from=333.788.videocard.2)
## 安装gitbook步骤及检测：

**1、安装“[node-v12.4.0-x64.msi](https://nodejs.org/en/)”（全部下一步就行）检验是否安装成功如下：**
```gitbook
$ node -v
v7.7.1
```
**2、安装gitbook，复制以下代码到运行里（win+R/cmd），再回车，自动安装完成**。[（npm的安装参考）](https://www.cnblogs.com/goldlong/p/8027997.html)
```gitbook
$ npm install gitbook-cli -g
```
**3、安装“[Git-2.22.0-64-bit.exe](https://git-scm.com/downloads)”（下一步下一步就自动完成），检验是否安装成功如下：**

```gitbook
$ gitbook -V
CLI version: 2.3.2
GitBook version: 3.2.3
```
4、复制以下代码创建book.json文件放到文件夹的根目录（或用自带的book.json文件）
```json
{
    "plugins": [
    "chapter-fold","-lunr","-sharing","expandable-chapters","page-treeview", "-search", "search-pro","splitter","ancre-navigation","popup","page-toc-button","back-to-top-button"
    ],
    "pluginsConfig": {
        "page-toc-button": {
            "maxTocDepth": 2,
            "minTocSize": 2
           },
           "expandable-chapters":{},
           "page-treeview": {
            "copyright": "Copyright &#169; aleen42",
            "minHeaderCount": "2",
            "minHeaderDeep": "2"
        }
    }
}
```
## 初始化文件夹
```gitbook
$ gitbook init
```
## 运行插件
```gitbook
gitbook install
```
## 生成网页
```gitbook
执行 gitbook build 或 gitbook serve 命令后会自动生成静态网页
```
