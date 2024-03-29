# 网格动态暂停

服务器使用 [Concealment](https://torchapi.com/plugins/view/?guid=17f44521-b77a-4e85-810f-ee73311cf75d) 插件动态暂停一部分网格来降低服务器负载.

**被暂停的网格上的所有功能性(Functional Block)方块不会运作**, 包括但不限于编程块, 物流系统, 反应堆等. 因此一个被暂停的网格不会通过太阳能板充电, 反应堆也不会运作, 箱子里的矿也不会被精炼.

在目前的服务器设置中, 以下几个条件满足任意一个就可以使网格保持加载:

* 有玩家在 5 千米范围内(不分敌我)
* 是海盗网格
* 有生产设备(组装机等)
* 已被加载不到一分钟

被暂停的网格的物理系统不会被暂停, 即网格会保持应有的运动状态. 但是网格的方块破坏效果会被暂停, 网格上的方块不会在被暂停的状态下被破坏. 举例来说, 一个从地球轨道扔下的网格若在落地时为暂停状态, 则网格上的方块不会被砸毁.
