
### 1.用css创建一个三角形 [例子Demo](http://jsrun.pro/EwbKp)
> 创建一个div，宽高都为0，实现效果如下，发现border的四个边都是一个三角形，要实现三角形只需将其中几个边background设置为transparent，即可得到三角形
```
> html
<div class='rect'>
</div>
<div class='triangle'>
</div>
```

```
> css
.rect {
  width: 0;
  height: 0;
  background-color: #fff;
  border-right: 100px solid rgb(34, 230, 220);
  border-left: 100px solid rgb(202, 146, 25);
  border-top: 100px solid rgb(29, 156, 194);
  border-bottom: 100px solid rgb(16, 204, 101);
}

.triangle {
  width: 0;
  height: 0;
  background-color: transparent;
  border-right: 100px solid transparent;
  border-left: 100px solid transparent;
  border-top: 100px solid rgb(29, 156, 194);
  border-bottom: 100px solid transparent;
}

```

### 2.css圣杯布局

1.第一种方法 [例子Demo](http://jsrun.pro/dIbKp)
```
> html
<div id="container">
  <div id="center" class="column">111122223334444111122223334444111122223334444111122223334444</div>
  <div id="left" class="column"></div>
  <div id="right" class="column"></div>
</div>
```
```
> css
body {
  min-width: 550px;
}

#container {
  padding-left: 200px; 
  padding-right: 150px;
}

#container .column {
  float: left;
  height:200px;
}

#center {
  width: 100%;
  background:#ffee33;
  word-break:break-all;
}

#left {
  width: 200px; 
  margin-left: -100%;
  position: relative;
  right: 200px;
  background:#2233dd;
}

#right {
  width: 150px; 
  margin-right: -150px; 
  background:#55eeee;
  position:relative;
}
```

2.第二种方法 [例子Demo](http://jsrun.pro/FIbKp)

```
> html
<div id="container">
  <div id="center" class="column">111122223334444111122223334444111122223334444111122223334444</div>
  <div id="left" class="column"></div>
  <div id="right" class="column"></div>
</div>
```

```
> css
body {
  min-width: 550px;
}

#container {
  padding-left: 200px; 
  padding-right: 150px;
}

#container .column {
  float: left;
  height:200px;
}

#center {
  width: 100%;
  background:#ffee33;
  word-break:break-all;
}

#left {
  width: 200px; 
  margin-left: -100%;
  position: relative;
  right: 200px;
  background:#2233dd;
}

#right {
  width: 150px; 
  margin-right: -150px; 
  background:#55eeee;
}
```
