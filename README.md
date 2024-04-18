<center><h1>Altium_Designer_Study(Altium_Designer_21 学习笔记)</h1></center>

# 注意事项及规则

> #####  [PCB布线基本规则](https://www.ebyte.com/new-view-info.aspx?id=890)
>
> ##### [20h](https://murata.eetrend.com/article/2019-11/1003161.html)

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
> 5. ##### 交换器件：F9 |（T + O -> 交换器件）(以改键）
>
> 6. ##### 在矩形区域内排列：F6 | I + L (以改键）
>
> 7. ##### XY轴偏移命令：1（字母上面的数字）| (E + M + X ) (以改键）
>
> 8. ##### 线选：E + S + L
>
> 9. ##### 2D：2
>
> 10. ##### 3D：3
>
> 11. ##### 移动命令（跟随鼠标移动，不用一直按着）：4 |（M + S）(以改键）
>
> 12. ##### 差分布线：U + I
>
> 13. ##### 修割铜皮（多边形铺铜挖空）：7 | (以改键）
>
> 14. ##### 修整铜皮边缘：option + F1 | (以改键）
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





