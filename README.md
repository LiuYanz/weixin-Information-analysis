# weixin-Information-analysis
### 通过itchat来获取微信好友详细信息，然后进行分析
#### 首先，在终端安装一下 itchat 包。安装完成后导入包，再登陆自己的微信。过程中会生产一个登陆二维码，扫码之后即可登陆。

#### 仔细观察了一下返回的数据结构，发现”性别“是存放在一个字典里面的，key 是”Sex“，男性值为 1，女性为 2，其他是不明性别的(就是没有填的)。可以写个循环获取想要的性别数据，得到自己微信好友的性别比例。在使用pyecharts时会出现地图显示不全或只显示南海诸岛问题

#### 再仔细观察 friends 列表，发现里面还包含了好友昵称、省份、城市、个人简介等等的数据，刚好可以用来分析好友城市分布，最好的方式是定义一个函数把数据都爬下来，存到数据框里，再进行分析。

#### 自己微信好友个性签名的自定义词云图。之前已经爬下了每个好友的个性签名，刚好可以分析一下大伙儿个性签名时使用的高频词语是什么，顺便可以做个词云图。



### pyecharts地图显示不全或只显示南海诸岛问题解决
#### 官网给的解释如下：

##### 自从 0.3.2 开始，为了缩减项目本身的体积以及维持 pyecharts 项目的轻量化运行，pyecharts 将不再自带地图 js 文件。如用户需要用到地图图表，可自行安装对应的地图文件包。下面介绍如何安装。

##### 全球国家地图: echarts-countries-pypkg (1.9MB): 世界地图和 213 个国家，包括中国地图
##### 中国省级地图: echarts-china-provinces-pypkg (730KB)：23 个省，5 个自治区
##### 中国市级地图: echarts-china-cities-pypkg (3.8MB)：370 个中国城市
#### 需要这些地图的朋友，可以装 pip 命令行:

##### pip install echarts-countries-pypkg
##### pip install echarts-china-provinces-pypkg
##### pip install echarts-china-cities-pypkg
#### 特别注明，中国地图在 echarts-countries-pypkg 里。


## 以下来自不同微信号的分析图，感谢微信号的提供者！
### 微信好友区域分布图
weixin-Information-analysis/img/微信好友区域分布图.png
### 省份分布柱状图
weixin-Information-analysis/img/省份分布柱状图.png
### 微信好友签名词云图
weixin-Information-analysis/img/微信好友签名词云图.png
性别比例图
### weixin-Information-analysis/img/性别比例图.png






