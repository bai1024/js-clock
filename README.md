## 效果图
![](http://ok7n02kz6.bkt.clouddn.com/FsAOXtMY6-TXn8kXsPQtwaeNWVOg.gif)

## 关键点
1. 表盘上指针的样式：旋转的效果
2. 获取实时的时间
3. 每一秒改变一次指针状态

## CSS部分
这次主要运用了一下几个特性：
1.  `transform-orgin`,用来调整指针的初始位置以及旋转的轴点。
2.  `transform:rotate()`,用来控制指针旋转的角度。
3.  `transiton-time-function`,用来设置过渡的动画效果，为了表现出时钟“滴答滴答”的感觉

## js部分
1. 创建setData()方法，获取当前的时间。
2. 根据时间计算各指针的角度。
`const secondsDegree = ((seconds / 60) * 360) + 90`
3. 利用定时器更新当前的指针显示位置
`setInterval(setDate, 1000)`
这样每隔1000毫秒就更新一次指针的位置，从而实现了指针转动的效果。
