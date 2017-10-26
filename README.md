# notif
# 新增功能说明
## 增加`css3`动画效果
+ 添加 `@keyframes`属性，`position`属性以及`animation`设置动画效果；利用 `background` 设置背景颜色 
+ 产生效果：在规定时间五秒内，相对原始位置进行轨迹为正方形的移动，五秒之后停在原始位置
## 示例
```css
@keyframes yidong/* 规定动画,0%开始，100%结束*/
{
 0%   {background:red; left:0px; top:0px;}
 25%  {background:yellow; left:200px; top:0px;}
 50%  {background:blue; left:200px; top:200px;}
 75%  {background:green; left:0px; top:200px;}
 100% {background:red; left:0px; top:0px;}
}
```
## 添加 `button` 关闭按钮
+ 在 `container`中添加一个 `button` 按钮
+ 给 `button` 关闭按钮 `display：block` 使其点击关闭后隐藏
## 示例
```js
const template = `<section id="notify-container"                   class="notify-container">
                 <button  class="close" type="button" 
                 onclick="document.getElementById('notify-container').style.display='none'">关闭</button>
                 <h3 class="notify-title"></h3>                      
                 <article class="notify-content"></article>
                 </section>` 
```
## 添加 `button` 收到按钮
+ 在 `body` 主体中添加一个收到按钮
+ 在`css`中应用 `display:none`属性使其隐藏
+ 在 `<script>` 标签中添加延时与清除函数，延时七秒之后显示按钮
+ 显示按钮，调用函数，点击确定之后隐藏按钮
```js
function appearance(){
     var div = document.getElementById("qwe");
     div.style.display="block";
     }  
     window.clearTimeout(time1);
     var time1 = window.setTimeout("appearance()",7000);
```
