# Flex布局

```css
.box {
    display: flex;
}

.box {
    display: inline-flex; //行内元素的flex布局
}
```

## 基本概念
![flex](../resource/flex/flex.png)

- main axis 主轴
- cross axis 交叉轴
- main start 主轴的开始位置
- main end 主轴的结束位置
- cross start 交叉轴的开始位置
- cross end 交叉轴的结束位置
- main size 单个项目占据主轴的空间
- cross size 单个项目占据交叉轴的空间

## 容器属性
- flex-direction 决定主轴的方向 (**row** | row-reverse | column | column-reverse)
- flex-wrap 一条轴线排不下，如何换行(**nowrap** | wrap | wrap-reverse)
- flex-flow 上面两个属性的简写，默认值(row nowrap)
- justify-content 定义了项目在主轴上的对齐方式 (**flex-start** | flex-end | center | space-between | space-around)
- align-items 项目在交叉轴上如何对齐 (flex-start | flex-end | center | base-line | **stretch**)
- align-content 多跟轴线的对齐方式 (flex-start | flex-end | center | space-around | **stretch**)

## 项目属性
- order 项目的排列顺序，越小越靠前，默认为0
- flex-grow 项目的放大比例，默认为0
- flex-shrink 项目的缩小比例,默认为1
- flex-basis 项目占据的主轴空间(**auto** | 固定大小)
- flex 上面三个的属性的简写(0 1 auto)
- align-self 允许单个项目的对齐方式和其他项目不一样(auto | flex-start | flex-end | center | base-line | stretch)