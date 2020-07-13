# 常用命令

服务器使用了不少插件来提供额外功能, 从而使玩家能更好的进行游戏, 如果想要使用这些额外功能, 就必须使用对应的命令.

游戏客户端通过在聊天栏\(按一下 Enter 键来呼出\)中输入对应的语句来键入命令. \`方向键上\` 可以切换出上一次输入的内容.

通常, 插件命令以 "!" 开头, 注意, 此符号为半角符号, 即俗称的英文符号, 如果使用了输入法, 请将输入法切换到半角模式/英文标点模式, 或者关闭输入法.

一些命令具有参数, 如果参数包含空格, 请用引号包裹, 例如一个命令为

!command testing 123

则 testing 与 123 会被解析为两个参数.

!command "testing 123"

则只输入了一个参数.

## 基础命令

!longhelp

显示所有命令与帮助文本.

!motd

查看今日消息\(进服时看到的消息\).

!grids list

显示自己拥有的所有网格的坐标值\(在 Dialog 中\), 并为自己添加它们的 GPS 坐标.

!fixship

若飞船出现 bug\(不受控的移动或无法停止\), 屏幕准心对准飞船\(不要坐在驾驶座上\)使用此命令来尝试修复此网格.

!fixme

人物死亡后不弹出重生点选择页面时使用此命令, 可能需要盲打. 执行成功后客户端可能崩溃或与服务器断开连接, 重新进服后即可继续正常游戏.

!entities refresh

当出现客户端与服务端数据不同步时使用, 有几率使客户端崩溃.

## GlobalMarket

此插件提供玩家间交易物品的功能

!market inventory

显示当前身上所有物品的名字, 如果对准一个箱子\(需手持工具, 并使物流口高亮显示\)使用还将列出箱子中的物品名.

!market sell &lt;itemName&gt; &lt;amount&gt; &lt;price&gt;

以某价格卖出某数量的某物品. 其中 itemName 从上一个命令的返回结果中取得, 可以是缩写, 例如 "MyObjectBuilder\_Ore/Ice" 缩写为 "Ice"\(如果两个物品缩写一样则必须填写完全限定名\). 例子: "!market sell ice 5 100" - 以 100 的价格卖出 5 个冰.

!market search \[itemName\]

搜索市场上的订单, 若 itemName 为空则列出所有.

!market longsearch \[itemName\]

作用与上一个命令相同, 但是在 Dialog 中显示, 可以很好地查看大量订单.

!market my

列出我的订单

!market buy \[orderNumber\]

购买对应的订单. 其中 orderNumber 是订单号, 例如: !market buy 54d2c1

## Hangar

此插件提供船坞功能, 用于存储网格, 也提供船只交易功能.

每个玩家至多手动保存八个网格, 每次存取船插件都会判断周围是否有敌人.

过久不上线的玩家的网格会被自动存储到船坞, 请用指令取出.

#### 存取网格与出售网格

!hangar save

鼠标准心对准一个网格使用来保存此网格\(不要坐在驾驶座上\). 保存船只需要花费金钱, 请确保有足够的钱. 若出现确认提示请再输入一次此命令. 若飞船上绝大部分功能性方块不是自己的, 或者有敌人在周围一定距离内则无法存船, 详见此命令的返回提示.

!hangar list

查看自己的船坞, 每一条目最前面为网格序号.

!hangar info &lt;gridNameOrNumber&gt;

查看自己船坞中的一个网格的详情, 参数为此网格的名称或其序号. 例如: !hangar info 1

!hangar load \[gridNameOrEntityId\]

从自己的船坞中加载网格到身旁, 例如: "!hangar load 1" - 加载自己船坞中的第一个网格. 注意, 根据游戏自身的算法, 加载出的网格会被投放到身边的安全区域, 可能并不在眼前, 尤其是当自己周围有小行星或身处安全区中时. 若无法视觉确认请用 !grids list 命令查看自己的所有网格坐标. 特别注意, 具有子网格的飞船不保证正确加载. 严重警告, 重力圈内放出网格可能导致网格损坏.

!hangar sell &lt;gridNameOrNumber&gt; &lt;price&gt; &lt;description&gt;

出售自己船坞中的网格, 例如: "!hangar sell 1 100000 这艘船超强" - 以 100000 的价格卖出自己船坞中的第一个网格.

#### 购买网格

在 G 键菜单中, 左侧找到 "飞船市场" 分类, 此分类中只有一个方块, 其模型为原版的 ConsoleBlock. 建造此方块并为他供电. 打开此方块的 UI\(ControlTerminal\) 滚动到下方. 所有玩家卖出的网格会在此处的列表被显示. 点击一个条目会在右边显示此正在被出售的网格的详情. 下方的 预览选中的网格 按钮可以将此网格的物理模型\(投影\)展示在飞船市场方块上方. 点击 购买选中的网格 即可购买. 购买完成后, 目标网格会被放入自己的船坞. 取船指令详见前文.

## LagGridBroadcaster

此插件用于统计玩家的网格耗时并通告超标网格给所有玩家. 网格耗时为游戏中的网格占用的服务器 cpu 计算时长\(每 tick\), 设计不良的物流系统以及氢氧机和活塞装置等会显著增加网格耗时. 该插件每半小时运行一次, 运行结束后将通过聊天栏告知每个玩家其所在阵营耗时最大的三个网格\(用于及时整改\), 并播报超标网格给所有玩家\(所有玩家都会被新增一个紫色 GPS\).

注意, 某些 mod 具有非常大的耗时, 例如纳米机.

常用单位换算:

1s=1000ms 1ms=1000us 1us=1000ns

!laggrids list

列出上一次测算中的所有网格的耗时\(不加载或耗时太低的网格不会被显示\).

!laggrids get

当人物坐在驾驶座上时使用, 用于显示当前控制的网格在上一次测算中的耗时.

## Bounty

此插件提供通缉功能, 可让玩家对其他玩家发布击杀悬赏. 自杀或友好阵营击杀或通缉发布者击杀不会结束通缉.

通缉被发布时将发送消息给所有玩家. 通缉结束时\(目标被敌对阵营击杀\)也会发送消息给所有玩家.

!bounty add &lt;playerNameOrId&gt; &lt;rewardAmount&gt;

对其他玩家发布悬赏, 例如 "!bounty add czp 1000000" - 对 czp 发布一张价值一百万的悬赏. 悬赏金额至少十万, 悬赏发布时从悬赏人账户上扣除.

!bounty list

查看所有通缉令.


