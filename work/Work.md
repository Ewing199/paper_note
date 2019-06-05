<attachment contentEditable="false" data-atts="%5B%5D" data-aid=".atts-ec27514d-9c39-4a9d-a10a-54ef4d87d99a"></attachment>
## 团队和沟通、责任
团队合作的重要性
适应团队，改变沟通模式，主动沟通
## 职业规划
[TOC]
# HDMI02_EAS模块
## 1.网管页面
**首先需要在背板开启ATSC模式才会显示该模块**
在EAS参数模块，需要对应设置与EAS的多播端口，并且勾选相应的需要垫播的频道
![](/uploads/share_project/images/m_a76e537280fd6621563625fd9c9d8559_r.png)

## 2.代码实现
![](/uploads/share_project/images/m_527704a7a9e1eddc5168bd43aa97ce92_r.png)
### 2.1 写垫播复用表
将EAS自带的流信息：流号（默认写为1），VideoPID,AudioPID,PCRPID，改为需要垫播通路的相关信息，其中需要特别注意PCRPID信息。
#### PCRPID由于存在两种模式：
1.PCRPID与VIDEOPID共用（PCRPID:103,VIDEOPID:103）
2.PCRPID与VIDEOPID共用（PCRPID:104,VIDEOPID:103）
