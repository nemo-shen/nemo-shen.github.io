# vertical-align属性

> 用来指定行内元素(inline)或表格单元格(table-cell)元素的垂直对齐方式

## 行内元素的值

### 相对父元素

```css
vertical-align: baseline; /*使元素的基线和父元素的基线对齐*/
vertical-align: sub; /*使元素的基线和父元素的下标基线对齐*/
vertical-align: super; /*使元素的基线与父元素的上标基线对齐*/
vertical-align: text-top; /*使元素的顶部与父元素的字体顶部对齐*/
vertical-align: text-bottom; /*使元素的底部与父元素的字体底部对齐*/
vertical-align: middle; /*使元素的中部与父元素的基线加上父元素高度的一半对齐*/
vertical-align: 10px; /*使元素的基线对齐到父元素的基线之上的给定长度(可以是负数)*/
vertical-align: 15%; /*使元素的基线对齐到父元素的基线之上的给定百分比(可以是负数)*/
```

### 相对行

```css
vertical-align: top; /*使元素及其后代元素的顶部与整行的顶部对齐*/
vertical-align: bottom; /*使元素及其后代的元素的底部与整行的底部对齐*/
```

## 表格单元格的值

```css
vertical-align: baseline;
vertical-align: sub;
vertical-align: super;
vertical-align: text-top;
vertical-align: text-bottom;
vertical-align: 5px;
vertical-align: 10%;
vertical-align: top;
vertical-align: middle;
vertical-align: bottom;
```



## 相关问题

### 1. 什么是基线？

