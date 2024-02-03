# Links All-in-one

<p align="center"><img src="https://s2.loli.net/2024/02/03/LJGQCqSPUgtbIaM.png" width="100" alt="linksaio logo"></p>

<p align="center">
  <a href="https://zh.wikipedia.org/wiki/%E6%98%93%E8%AF%AD%E8%A8%80" target="_blank"><img src="https://img.shields.io/badge/Language-%E6%98%93%E8%AF%AD%E8%A8%80-green"></a>
  <img src="https://img.shields.io/badge/Version-1.0-blue">
  <img src="https://img.shields.io/badge/LinksJSON-20240126-blue">
  <img src="https://img.shields.io/github/license/yzl3014/LinksAIO">
  <br>
  <a href="https://linksaio-dl.yuanzj.top/"><img src="https://img.shields.io/badge/%E7%AB%8B%E5%8D%B3%E4%B8%8B%E8%BD%BD-8A2BE2"></a>
</p>

LinksAIO 是一个用易语言开发的链接工具箱，支持在 Windows 7 及以上系统使用（Windows XP可以运行但效果不佳）。

因易语言文件无法使用git进行管理，目前并不开源主程序，但是链接列表`links.json`开源。也就是说，您可以定制自己的链接列表，添加自己常用的链接，让LinksAIO更易用。

# 链接列表(links.json)

“链接列表”是一个JSON文件，**LinksAIO将在这个列表中寻找输入的搜索词**。首次运行软件时，它会向注册表中添加数据，以便修改和再次读取，链接地址也包括在内。

您可以在 https://yzl3014.github.io/LinksAIO 找到更多链接地址。如果没有想要的，也可以在本地自行制作。

> 作者在开发v1.0时制作了快速生成工具，虽然界面简陋，但是可以完成快速生成JSON文件的需求：
> https://github.com/yzl3014/LinksAIO/tools/LinksTool.exe

links.json格式如下，id不可重复。请注意格式不要出错。

```JSON
{
    "version": "20240126(版本号，格式为yyyyMMdd)",
    "data": [
        {
            "id": "1",
            "title": "标题",
            "link": "链接(可不带https协议头)",
            "abbr": "短码(缩写或拼音，若link中已出现可不写)"
        },
        {
            "id": "2",
            "title": "163邮箱网页版",
            "link": "mail.163.com",
            "abbr": "163yx.mail"
        }
    ]
}
```

**导入方式**：将链接列表写入`links.json`，然后(任选其一)：

- 将其放在软件运行目录下，运行软件即可自动读取。
- 上传至服务器，将链接写在`操作-设置-搜索-Links链接`中，不要使用从html页面跳转出来的链接。然后打开软件，点击`操作-更换Links列表`即可导入。

**读取顺序**：软件将首先读取运行目录下的links文件，其次时临时目录中的，最后是从链接获取。

# 备注

默认列表链接：`https://cdn.jsdelivr.net/gh/yzl3014/LinksAIO@gh-pages/links.json`

临时目录：`%temp%\LinksAIO_temp`

注册表：`HKEY_CURRENT_USER\Software\LinksAIO`

LOGO制作素材：
- `https://icon-icons.com/icon/folder-blue/92960`
- `https://uxwing.com/internet-access-icon/`
