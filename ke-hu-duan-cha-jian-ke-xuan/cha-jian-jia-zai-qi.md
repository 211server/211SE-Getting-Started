# 插件加载器

创意工坊链接: [https://steamcommunity.com/sharedfiles/filedetails/?id=2407984968](https://steamcommunity.com/sharedfiles/filedetails/?id=2407984968)

这个插件允许轻松安装和加载来自多种不同来源的客户端插件. 插件基本上是一个不受限制的 MOD, 可以做任何它想做的事情. 这显然伴随着更大的风险, 但它也可以允许一些奇妙的通常不可能的事情. 由于插件是不受限制的, 你应该**只安装来自你绝对信任的来源和作者的插件**. 就像任何软件一样, 不要在没有验证它是否安全的情况下随意去安装你找到的任何插件. 然而, 也要知道, 创意工坊的每一个插件都是经过检查和白名单的, 然后才允许与这个加载器一起工作. GitHub 插件每次更新都必须手动检查, 但其他插件可能只被检查一次.

插件可以从太空工程师的主菜单中使用插件按钮进行配置. 在这个菜单中点击一个插件, 会在右侧显示其信息. 另外, 在启动过程中按住 escape 键将允许你暂时禁用所有插件. 请注意, 这个插件在游戏的闪屏期间做了很多操作. 这意味着, 当有很多插件加载时, 游戏可能需要额外的几秒钟来启动.

## 服务器

**插件加载器只安装客户端的插件**. 安装在客户端的插件在游戏开始后不管发生了什么, 也不管你加入了什么世界, 都会加载. 请向插件作者询问关于在服务器上安装他们的插件的说明.

## 安装

### 创意工坊

要安装, 请订阅这个物品, 并将这一整行添加到你的[启动选项](https://support.steampowered.com/kb\_article.php?ref=1040-JWMT-2947)中:

```
-plugin "..\..\..\workshop\content\244850\2407984968\RunPluginLoader"
```

(译者注: 参数的值指向你的 steam 文件夹中的工坊物品, 可能与你的游戏所在的磁盘分区不同)

你可以把这个准确的字符串粘贴到你的启动选项中, 包括路径周围的引号. 如果添加启动选项后游戏崩溃, 很可能是你的steam安装没有自动下载一些创意工坊物品. 你可能需要将加载器临时添加到一个世界, 或者使用手动安装说明.

### 手动

要不通过创意工坊安装, 必须手动将文件复制到游戏文件夹中. 详见 [github 页面](https://github.com/sepluginloader/PluginLoader)上的说明并下载.

## 卸载

要卸载插件加载器, 请从启动选项中删除该插件. 从磁盘中删除文件或在没有删除启动选项的情况下取消订阅, 会使游戏崩溃.

## 来源

### Mods

这种类型的 "插件" 并不是真正的插件. 这些是普通的MOD, 插件加载器会告诉游戏去加载.

### GitHub

这些插件不需要你订阅任何东西. 只要启用它们, 重新启动后, 它们就会被下载和安装.

### 创意工坊

你将在插件列表中找到你所订阅的创意工坊物品. 安装会自动进行! 如果一个插件有 GitHub 的源代码, 请使用它而不是创意工坊的源代码.

### SEPluginManager

你会在列表中发现 [SEPM](https://steamcommunity.com/sharedfiles/filedetails/?id=1973745637) 项目, 就像其他创意工坊插件一样. 对这些东西要小心, 因为大多数已经过时了.

### 本地

你可以在游戏插件目录下安装本地插件: steamapps/common/SpaceEngineers/Bin64/Plugins

警告: 本地插件会绕过白名单!

## 插件列表

下面是一些可用的插件的列表:

[**Block Picker** by avaness](https://steamcommunity.com/linkfilter/?url=https://github.com/austinvaness/BlockPicker)\[github.com]\
[**Camera LCD \[WIP\]** by avaness](https://steamcommunity.com/linkfilter/?url=https://github.com/austinvaness/CameraLCD)\[github.com]\
[**Custom Loading Backgrounds** by WesternGamer](https://steamcommunity.com/linkfilter/?url=https://github.com/WesternGamer/CustomLoadingBackgrounds)\[github.com]\
[**Disable Analytics** by avaness](https://steamcommunity.com/linkfilter/?url=https://github.com/austinvaness/DisableAnalytics)\[github.com]\
[**Discord Rich Presence** by Math0424](https://steamcommunity.com/linkfilter/?url=https://github.com/Math0424/SERichPresence)\[github.com]\
[**GridFilter** by Xo](https://steamcommunity.com/workshop/filedetails/?id=1937528740)\
[**Hide Version String** by WesternGamer](https://steamcommunity.com/linkfilter/?url=https://github.com/WesternGamer/HideVersionString)\[github.com]\
[**Image to LCD** by avaness](https://steamcommunity.com/linkfilter/?url=https://github.com/austinvaness/LcdImagePlugin)\[github.com]\
[**In Game Exit** by WesternGamer](https://steamcommunity.com/linkfilter/?url=https://github.com/WesternGamer/InGameExit)\[github.com]\
[**Jump Selector** by dude](https://steamcommunity.com/linkfilter/?url=https://github.com/Allen-Wrench/JumpSelector)\[github.com]\
[**Large Planets** by Klime](https://steamcommunity.com/linkfilter/?url=https://github.com/KlimeSE/LargePlanets)\[github.com]\
[**More PP Settings** by Math0424](https://steamcommunity.com/linkfilter/?url=https://github.com/Math0424/MorePPSettings)\[github.com]\
[**Multigrid Projector** by Viktor](https://steamcommunity.com/workshop/filedetails/?id=2415983416)\
[**No Armor Edges** by avaness](https://steamcommunity.com/linkfilter/?url=https://github.com/austinvaness/NoArmorEdges)\[github.com]\
[**No News Plugin** by WesternGamer](https://steamcommunity.com/linkfilter/?url=https://github.com/WesternGamer/No-News-Plugin)\[github.com]\
[**Password Cache** by avaness](https://steamcommunity.com/linkfilter/?url=https://github.com/austinvaness/PasswordCachePlugin)\[github.com]\
[**Remove Intro Video Plugin** by WesternGamer](https://steamcommunity.com/linkfilter/?url=https://github.com/WesternGamer/RemoveIntroVideoPlugin)\[github.com]\
[**Scrollable FOV** by Math0424](https://steamcommunity.com/linkfilter/?url=https://github.com/Math0424/ScrollableFOV)\[github.com]\
[**SE VR** by Klime](https://steamcommunity.com/linkfilter/?url=https://github.com/KlimeSE/SEVR)\[github.com]\
[**Seamless Client Plugin** by Casimir](https://steamcommunity.com/linkfilter/?url=https://github.com/Casimir255/SeamlessClientPlugin)\[github.com]\
[**SEWorldGenPlugin** by thorwin99](https://steamcommunity.com/workshop/filedetails/?id=2413918072)\
[**SteamWorkshopFix** by Klime](https://steamcommunity.com/workshop/filedetails/?id=2413859055)\
[**Tool Switcher** by avaness](https://steamcommunity.com/linkfilter/?url=https://github.com/austinvaness/ToolSwitcherPlugin)\[github.com]\
[**WL Analog Script Input and Throttle** by Wolfe](https://steamcommunity.com/linkfilter/?url=https://github.com/wolfe-labs/SE-AnalogThrottlePlugin)\[github.com]

以及更多...

如果你可以阅读 XML, [这](https://github.com/sepluginloader/PluginHub/tree/main/Plugins)有一份可以找到的插件清单.

## 社区

有关支持, 插件开发和所有插件的事情, 请加入discord服务器: [https://discord.gg/VJGjzdgnjf](https://discord.gg/VJGjzdgnjf)

## 常见问题

我已经完全按照这里显示的方式输入了启动选项, 但是游戏一开始就崩溃了! 这到底是怎么回事?&#x20;

试着导航到你放在启动选项里面的文件夹. 有时steam并不像它应该的那样下载插件加载器. 如果你找不到这个文件夹, 试着把插件加载器暂时添加到一个世界里, 这样游戏就可以强制 steam 下载它.

请[投票](https://support.keenswh.com/spaceengineers/pc/topic/23269-plugins-please-check-if-they-exist-before-loading)修复这个问题, 这样它就不会使游戏崩溃.

当我加载一个世界时, 我得到了一堆关于模组的错误!

你在你的模组列表中添加了一个插件. 不要这样做. 插件通常不应该被放在世界的模组列表中.

当我做<事情>时, 我的游戏崩溃了!?

你是刚刚启用了一个插件, 还是有一个插件刚刚更新? 试着禁用那个插件, 或者随机禁用插件, 直到问题得到解决. (就像你的世界里有一个坏的模组一样!）注意, 所有的插件都可以在启动时按住 escape 键暂时禁用. 如果你找到了坏的插件, 把游戏的日志文件发给该插件的作者.

对于这里没有涉及的任何问题的支持, 请加入上面链接的 discord 服务器社区.

## 源代码

你可以在 github 上找到[这个插件](https://github.com/sepluginloader/PluginLoader)的源代码.

## 开发者

如果你想为插件加载器开发一个插件, 请加入上面链接的 discord 服务器社区.

### 捐助

想要支持我的工作, 你可以用 [Paypal](https://steamcommunity.com/linkfilter/?url=https://www.paypal.com/donate/?business=9V2RMEADM4AAW\&no\_recurring=0\&currency\_code=USD)\[www.paypal.com] 或者 [Patreon](https://steamcommunity.com/linkfilter/?url=https://www.patreon.com/user?u=52357162)\[www.patreon.com]
