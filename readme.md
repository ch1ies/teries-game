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