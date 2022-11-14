# [Grasscutter](https://github.com/Grasscutters/Grasscutter)文档

## 工具

> 命令文档
>
> https://github.com/Grasscutters/Grasscutter/wiki/Commands

- [本地命令工具](https://github.com/jie65535/GrasscutterCommandGenerator)([服务端安装插件](https://github.com/jie65535/gc-opencommand-plugin))

- [网页命令工具](https://wmn1525.github.io/grasscutterTools/dist/index.html#/start/commuse)
- [网页控制工具](https://liujiaqi7998.github.io/GrasscuttersWebDashboard/)

## 部署

> 相关文档
>
> https://mihoyo-is-in.icu/
>
> 博客
>
> https://www.eula.club/%E4%BD%BF%E7%94%A8Grasscutter%E6%9C%8D%E5%8A%A1%E7%AB%AF%E6%90%AD%E5%BB%BA%E5%8E%9F%E7%A5%9E%E7%A7%81%E6%9C%8D.html
>
> https://www.rainkavik.com/archives/254/
>
> https://blog.tomys.top/2022-04/GenshinTJ/
>
> https://memorz.top/archives/112
>
> https://telegra.ph/Grasscutter-CN-04-21
>
> https://blog.otoo.top/Blog/Genshin2-6-Grasscutters/
>
> https://www.autive.cn/archives/116.html
>
> https://www.autive.cn/archives/113.html
>
> https://www.xiaoweigod.com/network/2403.html
>
> https://moeyy.cn/2050
>
> https://blog.dsrkafuu.net/post/2022/genshin-grasscutter/
>
> https://ybbs.fun/959.html
>
> https://ybbs.fun/1983.html
>
> https://ybbs.fun/2152.html
>
> https://www.chr0nix.xyz/genshintj/
>
> https://blog.tomys.top/2022-07/GenshinLauncher/

### 配置环境

####  MongoDB 数据库

https://www.mongodb.com/try/download/community

#### JDK 17

https://jdk.java.net/archive/

#### 运行服务器

拉取资源

```bash
git clone https://github.com/Koko-boya/Grasscutter_Resources.git
```

移动`Grasscutter_Resources`文件夹中`Resources`文件夹到Grasscutter根目录

```bash
mv Grasscutter_Resources/Resources ./resources
```

Grasscutter服务端资源目录结构

```yaml
grasscutter-1.4.4-dev.jar  #服务端
resources				   #服务端资源
keystore.p12			   #代理加密证书
```

启动项目

> 启动后会自动生成资源文件

```bash
java -jar grasscutter.jar
```

> 注意：
>
> 如果需要在非本地部署服务，需要修改Grasscutter生成的`config.json`其中127.0.0.1修改为服务端IP，同时端口也需要修改。

## 启动游戏

### Windows

补丁(启动器)

https://github.com/gc-toolkit/GenshinLauncher

#### 任选其一

1. 启动器

   - https://github.com/Grasscutters/Cultivation

   - https://github.com/Coooookies/OceanLauncher

   - https://github.com/efojug/Grasssummoner (推荐这个)

   - https://github.com/KL-kirito/CelestiaLauncher

   

2. 代理([安装证书教程](https://blog.csdn.net/feiyu68/article/details/119665869))

运行`proxy.py`

> 每次更换服务端IP都需要重新安装证书http://mitm.it/

```bash
mitmdump -s proxy.py -k --set block_global=false
```

系统连接代理

### Android

代理

https://github.com/577fkj/GenshinProxy