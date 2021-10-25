---
description: Defense Shields
---

# 防御护盾

工坊链接 [https://steamcommunity.com/sharedfiles/filedetails/?id=1365616918](https://steamcommunity.com/sharedfiles/filedetails/?id=1365616918)

[武器核心](wu-qi-he-xin.md)兼容的护盾.

编程块 API: [https://steamcommunity.com/linkfilter/?url=https://github.com/sstixrud/DefenseShields/blob/Production/Data/Scripts/DefenseShields/API/PbApiWrapper.cs](https://steamcommunity.com/linkfilter/?url=https://github.com/sstixrud/DefenseShields/blob/Production/Data/Scripts/DefenseShields/API/PbApiWrapper.cs)

## 独特之处

与其他模组不同的是, 我决定采取一种不同的方式, 即一艘飞船/空间站在任何时间每种方块只能有一个处于激活状态, 所有多余的方块将在激活的方块被摧毁时作为备份. 另一个独特之处是这个模组中的所有方块都可以互相通讯并为彼此增加额外功能. 最后, 不像其他模组那样, 本模组中的方块耗电量与方块数量无关, 而是与可用能源量以及能源被配置为如何使用有关.

## 多人游戏与性能

这个模组的设计是高效且性能友好的, 在任何时候都能在屏幕上显示 1000 个护盾. 这个模组还为运行着超过一千个激活的护盾的大型服务器专门设计并优化了多人游戏体验. 这是可以做到的, 因为有特殊的代码被设计用来当护盾不再与世界互动时休眠它们并在它们周围没有玩家或者移动的实体时完全卸载它们. 此外本模组是极致多线程的, 在测试中的 16 核心处理器上有很好的分布式效能.

## 防御护盾(Defense Shield)基础: 哪些组件做了什么

//TODO
