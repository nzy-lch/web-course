# Homework-03
### Google Material Icon fixed布局
实现左侧固定的侧边栏导航，侧边栏中基于网络提供的Icon图标实现     
Google Material Icon，是Google设计提供的一套免费开源的图标库   
学习使用方法及国内镜像：http://micon.dxbtech.cn/   
正确引入css后，通过文字，声明展示对应的图标   

![result](https://github.com/bwhyman/web-course/blob/master/homeworks/homework-03/screen-01.gif)

### 原理与思路
布局   
声明全局容器    
声明导航容器   
导航容器中，声明放置图标的item容器   
item容器中声明超链接，超链接内容为icon   
声明复制若干item容器   
声明主容器   
主容器中声明段落   

样式   
全局box计算模式   
全局弹性容器，即将导航与主内容容器横向并列   
左导航容器，显式声明宽度，窗口高度，固定。即，当内容长度超过一屏可滚动时，左导航不动   
右侧主区域容器，占用除左导航外的最大
- 由于左侧导航按固定布局，因此，在计算尺寸时不会计算。
即，此时弹性容器计算尺寸时，内部仅有一个主容器。
因此，主区域容器布局时，用margin据左计算出左导航的距离，从而避免导航压住内容区域   

item容器，中内容居中，即超链接居中   
超链接导航，内边距撑开，可点击范围为全部item等   
Google图标，为Google图标创建一个自定义样式类，声明图标的颜色/尺寸样式   
Google图标库基于文本声明，因此图标的颜色/尺寸等是基于文本的属性   
当悬浮在item，item向上移动5px，添加渐进效果。即，当悬浮时，有图标向上跳一下的效果   