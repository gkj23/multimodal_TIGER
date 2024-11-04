### 一些灵感

#### visual encoder
AutoEncoder ResNet U-Net

#### modal fusion
##### fusion position
去年的一篇发现，视觉信息频繁地加入会反而对听觉信息的质量作出稀释，所以可以实验验证什么时候插入效果最好（或者在fuse路径上加softmax/gate）
##### fusion 方式
1.先都encoding，之后视觉信息上采样与听觉信息concat+1*1Conv( 1**1conv真的合适吗)
2.视觉encoding信息作为attention模块的Q
3.能否视听信息信息相互辅助encoding

#### Adaptive