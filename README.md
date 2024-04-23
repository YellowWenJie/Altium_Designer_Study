<center><h1>Altium_Designer_Study(Altium_Designer_21 学习笔记)</h1></center>

# 注意事项及规则

> #####  [PCB布线基本规则](https://www.ebyte.com/new-view-info.aspx?id=890)
>
> ##### [20h](https://murata.eetrend.com/article/2019-11/1003161.html)
>
> > ##### 20H原则，在PCB设计的时候，为了体现20H原则，我们一般在平面层分割的时候，将电源层比地层内缩1mm就可以了。然后在1mm的内缩带打上屏蔽地过孔，150mil一个
> >
> > ![233739not8pxyr3q77psx7](https://p.ipic.vip/01wf3e.png)
>
> ##### [规则界面介绍](https://blog.csdn.net/qq_43460476/article/details/123464180)
>
> ##### [3W：它指的是两个PCB走线它们的中心间距不小于3倍线宽](https://blog.csdn.net/weixin_42693097/article/details/129540539)
>
> > ##### 3W原则，在PCB设计中很容易体现，保证走线与走线的中心间距为3倍的线宽即可，如走线的线宽为4.5mil，那么为了满足3W原则，在AD设置线到线的规则为9mil即可，那么中心距是13.5mil
> >
> > ![233724pgkbrrkm90rz3trp](https://p.ipic.vip/xw9rlj.png)
>
> ##### 如果在布线的时候网络太多太乱，可以设置电源类并关闭电源类的网络线
>
> > ![截屏2024-04-21 10.37.33](https://p.ipic.vip/m8vc8x.png)
>
> 

# 软件名词

designator -> 丝印，位号

![IMG_4094](https://p.ipic.vip/75otn8.jpg)

> ![截屏2024-04-21 11.40.43](https://p.ipic.vip/7n0pyl.png)
>
> Arc：圆弧
> Track：走线
> SMD Pad：表贴焊盘
> TH Pad：通孔焊盘
> Via：过孔
> Fill：填充区块
> Poly：覆铜
> Region：逻辑区
> Text：文本
> Copper:铜皮
> Hole: 孔

# 软件配置

##### 交互选择对象

![截屏2024-04-18 21.09.36](https://p.ipic.vip/6wqqzz.png)

##### 关闭允许网络活动（可能造成软件卡顿）

![](https://p.ipic.vip/v575lk.png)

##### 自动保存

![截屏2024-04-18 21.18.25](https://p.ipic.vip/sv1n8z.png)

##### DRC

![](https://p.ipic.vip/bxgatd.png)



##### 实时高亮（鼠标放到元器件上会高亮）

![截屏2024-04-18 21.28.49](https://p.ipic.vip/tnnqpe.jpg)

##### 铜皮以及焊盘样式

![截屏2024-04-18 21.34.01](https://p.ipic.vip/9s1v3c.png)

##### DRC报错样式

![截屏2024-04-18 21.35.19](https://p.ipic.vip/tu3192.png)



##### 布线冲突方案（当前模式里可以切换方案）

![截屏2024-04-18 21.37.13](https://p.ipic.vip/1643hn.png)

##### 走线时设置宽度（shift + W）

![截屏2024-04-18 21.40.26](https://p.ipic.vip/kdafoc.png)

##### 设置布线最大宽度与最小宽度

![截屏2024-04-18 21.41.35](https://p.ipic.vip/aene6d.png)

##### 设置过孔

> ##### Solder Mask Expansion(阻焊外扩)

![截屏2024-04-18 21.44.43](https://p.ipic.vip/veyrkn.png)

##### 铺铜模式

> ##### Remove Islands Less Than 设置为 50
>
> ![截屏2024-04-18 21.51.18](https://p.ipic.vip/amtlzc.png)

##### 铺铜间隙

![截屏2024-04-18 21.54.52](https://p.ipic.vip/ju5c70.jpg)













# 键位（常用)

> 1. ##### 交互式布线：control + W
>
> 2. ##### 布线时切换线宽度：shift + W
>
> 3. ##### 放置过孔： P + V
>
> 4. ##### 铺铜：P + G
>
> 5. ##### 修割铜皮（多边形铺铜挖空）：7 | (以改键）
>
> 6. ##### 修整铜皮边缘：option + F1 | (以改键）
>
> 7. ##### 交换器件：F9 |（T + O -> 交换器件）(以改键）
>
> 8. ##### 在矩形区域内排列：F6 | I + L (以改键）
>
> 9. ##### XY轴偏移命令： E + M + X
>
> 10. ##### 线选：E + S + L
>
> 11. ##### 2D：2
>
> 12. ##### 3D：3
>
> 13. ##### 移动命令（跟随鼠标移动，不用一直按着）：4 |（M + S）(以改键）
>
> 14. ##### 差分布线：U + I
>
> 15. ##### 放置填充：P + F
>
> 16. ##### 元器件文本位置（元器件的位号）：E + G + P
>
> 17. ##### 对齐：选中器件  + A
>
> 18. ##### 删除线：delete
>
> 19. ##### 显示连接线： N
>
> 20. ##### 抓取到中心：shift + E
>
> 21. ##### 切换单位：Q
>
> 22. ##### PCB中选择器件：J + C
>
> 23. ##### 元器件切换层：L
>
> 24. ##### 设置：T + P
>
> 25. ##### 设计规则检查：T + D
>
> 26. ##### 改变布线走线的角度：shift + 空格
>

# 布局规则

## 交互式模块化布局规则

> 工具 -> 交叉选择模式

#### PCB 布局的各项要求

1. [DFM](https://zhuanlan.zhihu.com/p/461235700)

2. EMC、EMI、ESD、信号完整性、元器件散热

3. 满足热设计

   



#### 类Class

> ##### 设计 -> 类 -> Net Classes -> 添加类
>
> 1. ###### 将电源全部添加到一个 class 中
>
> > ![](https://p.ipic.vip/l2y84h.png)



# 布局布线注意事项

1. 元器件与跳线帽柱子至少保持 3cm 的距离
2. 电感和晶振下面不能走铜



# 网络 Class 及规则设置

> #####  信号线宽度一般 6mil 就能满足要求，电源线的宽度则需要满足它的载流

##### 参考文献

> ##### 间距规则设置
>
> > https://blog.csdn.net/luobeihai/article/details/123952325

##### 电源类加粗（选中 Width 右键添加新规则）

> ![截屏2024-04-21 10.48.20](https://p.ipic.vip/75fj2h.png)
>
> ###### 电源类首选 20mil，最小 10mil， 最大 100mil。
>
> ![截屏2024-04-22 21.48.55](https://p.ipic.vip/tzjkk6.png)

##### 间距规则（[3W原则&10W原则]()）

##### 3W原则

> ##### 3W原则，在PCB设计中很容易体现，保证走线与走线的中心间距为3倍的线宽即可，如走线的线宽为4.5mil，那么为了满足3W原则，在AD设置线到线的规则为9mil即可，那么中心距是13.5mil
>
> ![233724pgkbrrkm90rz3trp](https://p.ipic.vip/xw9rlj.png)

##### 布线冲突解决方案

> Interactive Routing 选项卡
> 走线设置是比较重要的设置
> 第一个区块为布线冲突解决方案：
> 1：Ignore Obstacles：忽略障碍物走线
> 2：Push Obstacles：推荐障碍物走线
> 3：Walkaround Obstacles：围绕障碍物走线
> 4：Stop At First Obstacle：遇到障碍物即停止走线
> 5：AutoRoute On Current Layer：自动布线时在当前层走线。
> 6：AutoRoute On Multiple Layer：自动布线时在表层或内层走线。（用途不大，可以取消勾选）
> 以上走线模式在布线时可以使用快捷键Shift + R进行切换
> 第二个区块Interactive Routing Options
> 1：Automatically Remove Loops：自动移除回路
> 2：Remove NET Antennas：移除Stub线头（不封闭连线，除了天线其余时候不应有。）
> 3：Allow Via Pushing：允许过孔的推挤。
> 4：Display Clearance Boundaries：走线保护边界显示
> 5：Reduce Clearance Display Area：减小保护边界的显示
> 第三个区块Dragging
> 1：Ignore Obstacles：拖动状态忽略障碍物
> Avoid Obstacles(Snap Grid)：按照格点躲避障碍物。
> 2：Unselected via/track-Move：对于没有选择的过孔和导线拖动时只进行移动。
> 3：Selected via/track-Drag：对于被选中了的过孔和导线拖动时进行拖拽和鼠标一起移动。
> 4：Component pushing-Ignore：元件拖动时忽略障碍物。

##### Room 使用（设置room后，在room区域内会按照room设计规则走线）

> ![截屏2024-04-22 21.37.56](https://p.ipic.vip/5rd04o.png)
>
> ##### 新建规则
>
> ![截屏2024-04-22 21.41.01](https://p.ipic.vip/dxo2mt.png)
>
> ##### 在输入框中输入 WithinRoom(‘创建room的名字’)
>
> ![截屏2024-04-22 21.43.09](https://p.ipic.vip/afeucv.png)

##### 过孔规则

> ##### 特别密：4/10
>
> ##### 如果比较密： 8/16±2（8/14 || 8/ 16  || 8/18）
>
> ##### 板子空间还好的： 10/20±2（10/18 || 10/20 || 10/22）
>
> ##### 板子空间特别稀疏：12/24±2（12/22 || 12/24 || 12/26）
>
> 

> ![截屏2024-04-22 22.00.34](https://p.ipic.vip/b5bct2.jpg)
>
> ##### 如果设置没效果则可以去设置里设置
>
> ![截屏2024-04-22 22.00.14](https://p.ipic.vip/3mm2kw.jpg)

##### 铺铜规则

> ![截屏2024-04-23 21.41.12](https://p.ipic.vip/uwcl4i.png)
>
> ![截屏2024-04-23 21.58.05](https://p.ipic.vip/ym53f3.png)

###### 如何铺铜

> ###### 使用 P + G 快捷键在需要铺铜的位置绘制区域,再使用取色笔选择需要赋予的网络，然后在点击 Repour
>
> ![截屏2024-04-23 21.46.13](https://p.ipic.vip/fft4fl.png)
>
> ###### 如果需要修改铜皮，则需要在修改完后使用快捷键 T + G + R
>
> ![截屏2024-04-23 21.53.12](https://p.ipic.vip/l2oaur.png)

###### 如何铺一个脚全连接一个脚十字连接

> ##### 首先在焊盘类中新建类，再把对应的元器件加入到类中
>
> ![截屏2024-04-23 22.07.15](https://p.ipic.vip/yclczm.png)
>
> ##### 然后在焊盘规则中新建规则
>
> ![截屏2024-04-23 22.08.31](https://p.ipic.vip/zpnbv3.png)
>
> ![截屏2024-04-23 22.10.34](https://p.ipic.vip/6bib17.png)















