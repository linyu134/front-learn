## 问题

> 1. CSS 加载方式有几种？

*   三种
*   外部样式；内部样式；内联样式。
>
> 2. @charset有什么作用？

*   通过charset可以改变网页的编码格式，避免页面乱码等兼容问题。
>
> 3. @import有什么作用？如何使用？

*   import用于引入CSS。
*   使用格式：@import url('地址');
```
例如：@import 'custom.css';

```
>
> 4. id 选择器和 class 选择器的使用场景分别是什么？

*   id 选择器可以为标有特定 id 的 HTML 元素指定特定的样式。HTML元素以id属性来设置id选择器, CSS 中 id 选择器以"#" 来定义。
*   class 选择器用于描述一组元素的样式，class选择器有别于id选择器，class可以在多个元素中使用。class择器在HTML中以class属性表示, 在CSS 中，类选择器以一个点"."号显示：
>

> 5. CSS选择器常见的有几种？

*   三种
*   元素选择器；ID选择器；类选择器。
>

> 6. 伪类选择器有哪些？伪元素有哪些？

* 伪类选择器：
```
:link
:visited
:hover
:active
:first-child
:last-child
:not(p)
:not(.warning)
```
* 伪元素：
```
::after
::before
::selection
::backdrop
::first-letter
::first-line
::-webkit-input-placeholder
```
> 7. 以下选择器分别是什么意思?
>
>    1. ```css
>       #header{  
>       }
>       //id选择器的值为header的元素的样式
>
>       .header{ 
>       }
>       //class选择器的值为header的元素的样式
>
>       .header .logo{
>       }
>       //class选择器的值为header的元素的后代中的class选择器的值为logo的元素的样式
>
>       .header.mobile{
>       }
>       //class选择器的值包括header和mobile的元素的样式
>
>       .header p, .header h3{
>       }
>       //class选择器的值为header的后代p标签或者h3标签的样式
>
>       #header a:hover{
>       }
>       //id选择器的值为header的后代a标签在hover状态（鼠标悬停其上）下的样式
>
>       #header .logo~p{
>       }
>       //id选择器的值为header的后代中，class选择器的值为logo的元素之后的同级元素中的所有p标签的样式
>
>       #header .logo+p{
>       }
>       //id选择器的值为header的后代中，class选择器的值为logo的元素的下一相邻的元素的样式
>
>       #header .logo p{
>       }
>       //id选择器的值为header的后代中，class选择器的值为logo的元素的后代p标签的样式
>
>       #header .logo>p{
>       }
>       //id选择器的值为header的后代中，class选择器的值为logo的元素的直接子元素的样式
>
>       #header p.logo{
>       }
>       //id选择器的值为header的后代中，p标签的后代class选择器的值为logo的元素的样式
>
>       #header .logo.p{
>       }
>       //id选择器的值为header的后代中，class选择器的值包括logo和p的元素的样式
>
>       #header input[checked]{
>       }
>       //id选择器的值为header的后代中，input元素中存在checked的值的样式
>       ```
>
> 8. 选择器的优先级是如何计算的？

*   important>行内样式>ID选择器>类选择器>标签>通配符>继承>浏览器默认属性
>
> 9. 运行如下代码，并对结果做出解释
>
>    1. ```css
>        <style>
>        .box:first-child {
>         color: red;
>       }
>       .box:first-of-type {
>         background: blue;
>       }
>       .box :first-child {
>         font-size: 30px;
>       }
>       .box :first-of-type {
>         font-weight: bold;
>       }
>        </style>
>         <div class="container">
>           <div class="box">div.box</div>
>           <p class="box">p.box</p>
>           <div class="box">div.box</div>
>           <div class="box">
>             <div class="item">div.item</div>
>             <p class="item">p.item</p>
>           </div>
>           <p class="box"></p>
>         </div>
>       ```
```
.box:first-child {
  color: red; /* 满足class=box并且是父元素的第一个孩子的元素*/
}
.box:first-of-type {
  background: blue;/*满足class=box并且是父元素的后代中类型第一次出现的子元素*/
}
.box :first-child {
  font-size: 30px;/*满足class=box的后代中属于第一个孩子的元素*/
}
.box :first-of-type {
  font-weight: bold;/*满足class=box的后代中属于类型第一次出现的子元素*/
}

<div class="container">
    <div class="box">div.box</div> //满足.box:first-child;.box:first-of-type
    <p class="box">p.box</p>       // 满足.box:first-of-type
    <div class="box">div.box</div>
    <div class="box">
      <div class="item">div.item</div>  //满足.box :first-child; .box :first-of-type
      <p class="item">p.item</p>        //满足.box :first-of-type
    </div>
    <p class="box"></p>
  </div>

```

