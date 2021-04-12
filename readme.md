# 游戏开发
单一职能原则： 每个类只做一件它相关的事
开闭原则：系统中的每个类，应该对扩展开放，对修改关闭

基于以上原则，系统中使用如下模式
数据-界面分离模式

传统面向对象语言，书写类的属性时，往往会进行如下操作
1. 所有的属性全部私有化
2. 使用公开的方法提供对属性的访问

## 开发小方块类

小方块类： 处理自己的数据，知道什么时候显示，但不知道怎么显示

react,  核心逻辑，跟界面无关，响应式，怎么生成vnode ,怎么对比
react-dom ， 怎么显示 
react-native

## 小方块的显示类
作用：用于显示一个小方块到页面上

## 方块的组合类
组合类中的属性：
- 小方块的数组
思考： 该数组的组合能不能发生变化
回答： 不能发生变化，是只读数组

思考： 该数组的每一项从何而来

一个方块的组合取决于 **组合的形状**
形状是什么？
一组相对坐标的组合，该组合中有一个特殊的坐标，表示形状的坐标

如果知道了： 形状，中心点坐标（在面板中的坐标）, 颜色，就可设置小方块的数组

- 形状的属性




## 俄罗斯方块的生产（形状）类

## 俄罗斯方块的规则类

## 开发旋转功能
旋转的本质 -- 改变形状 根据当前的形状 ---> 新的形状
- 有些方块是不旋转的
- 有些方块旋转时只有两种状态
    先顺时针在逆时针
- 选装不能超出边界

rotate 有一种特定实现，但是不同的情况下会有不同的实现
    将square 作为父类， 其他的方块都是他的子类，子类可以重写父类的方法


思考： 旋转对于程序结构的影响
      为什么要书写子类？


## 开发游戏类（组合功能）
数据类， 只控制数据
Game 类清楚， 什么时候进行显示的切换，但不知道如何显示

## 触底处理
触底： 当前方块到达最底部
什么时候可能发生触底？（什么时候调用函数的问题）
 1. 自由下落
 2. 玩家控制
触底之后做什么？ （函数如何编写）
- 切换方块
- 保存以落下的方块
- 游戏是否结束的判断
- 消除方块的处理

新的问题
1. 当触底后，如何保存已落下的方块
2. 如何根据以保存的方块，判断当前方块是否可以移动

## 消除方块
消除时做哪些事？
1. 界面上移除
2. 从exists数组中移除
3. 改变y 坐标 + 1

## 游戏是否结束

## 积分

## 完成游戏界面


## 项目总结
为什么要学面向对象
1. 面向对象带来了新的开发方式
面向对象开发已经非常成熟，特别善于解决复杂问题
2. TypeScript 某些语法专门为面向对象准备的
    - 访问修饰符
    - 抽象类 abstract
3. 为了学习一些设计模式
    - 单例
    - 接口
 为什么选择做游戏？
1. 游戏特别容易使用面向对象的思维
2. 锻炼抽象的思维方式

整体的思维
 - 划分类
 - 一个类就是最小的功能单元，每个类只做一件事
 - 类与类之间的边界很清晰
 - 开发 高内聚（同一个类的功能做完）， 低耦合（类与类之间的联系越少越好） 
 - 类比模块化开发，高内聚（同一个模块的功能做完），低耦合（模块之间的联系越小越好）
 

 
