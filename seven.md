## 问题



http://js.jirengu.com/?html,output

在这个地址写需要效果的代码，答案附上链接就可以了

> 1. 什么是 CSS 继承?哪些属性能继承，哪些不能？

*   CSS继承可定义为特定的css属性向下传递到子孙元素，就是指被包在内部的标签将拥有外部标签的样式，即子元素可以继承父元素的属性。
*   能继承的属性：
    1. 字体系列属性:font、font-family、font-weight、font-size、font-style;
    2. 文本系列属性:  
        （1）内联元素：color、line-height、word-spacing、letter-spacing、text-transform;
        （2）块级元素：text-indent、text-align;
    3. 元素可见性：visibility
    4. 表格布局属性：caption-side、border-collapse、border-spacing、empty-cells、table-layout;
    5. 列表布局属性：list-style
    6. 生成内容属性：quotes
    7. 光标属性：cursor
    8. 页面样式属性：page、page-break-inside、windows、orphans;
    9. 声音样式属性：speak、speech-rate、volume、voice-family、pitch、stress、elevation;
*   不能继承的属性：
    1. display：规定元素应该生成的框的类型；
    2. 文本属性：vertical-align、text-decoration;
    3. 盒子模型的属性：width、height、margin 、border、padding;
    4. 背景属性：background、background-color、background-image;
    5. 定位属性：float、clear、position、top、right、bottom、left、min-width、min-height、max-width、max-height、overflow、clip;
    6. 生成内容属性：content、counter-reset、counter-increment;
    7. 轮廓样式属性：outline-style、outline-width、outline-color、outline;
    8. 页面样式属性：size、page-break-before、page-break-after;
    9. 声音样式属性：pause、cue、play-during;

>
> 2. 块级元素和行内元素分别有哪些？

*   块级元素：
    1. address - 地址
    2. blockquote - 块引用
    3. center - 居中对齐块
    4. dir - 目录列表
    5. div - 常用块级元素
    6. dl - 定义列表
    7. fieldset - form控制组
    8. form - 交互表单
    9. h1 - 标题
    10. hr - 水平分隔线
    11. menu - 菜单列表
    12. ol - 排序表单
    13. p - 段落
    14. pre - 格式化文本
    15. table - 表格
    16. ul - 非排序列表

*   行内元素： 

&ensp;&ensp;&ensp;&ensp;*  a - 锚点  
　　* abbr - 缩写  
　　* acronym - 首字  
　　* b - 粗体(不推荐)  
　　* bdo - bidi override  
　　* big - 大字体  
　　* br - 换行  
　　* cite - 引用  
　　* code - 计算机代码(在引用源码的时候需要)  
　　* dfn - 定义字段  
　　* em - 强调  
　　* font - 字体设定(不推荐)  
　　* i - 斜体  
　　* img - 图片  
　　* input - 输入框  
　　* kbd - 定义键盘文本  
　　* label - 表格标签  
　　* q - 短引用  
　　* s - 中划线(不推荐)  
　　* samp - 定义范例计算机代码  
　　* select - 项目选择  
　　* small - 小字体文本  
　　* span - 常用内联容器，定义文本内区块  
　　* strike - 中划线  
　　* strong - 粗体强调  
　　* sub - 下标  
　　* sup - 上标  
　　* textarea - 多行文本输入框  
　　* tt - 电传文本  
　　* u - 下划线  
　　* var - 定义变量  

*   可变元素素列表--可变元素为根据上下文语境决定该元素为块元素或者行内元素
    1. button按钮
    2. del	定义文档中已被删除的文本
    3. iframe	创建包含另外一个文档的内联框架（即行内框架）
    4. ins	标签定义已经被插入文档中的文本
    5. map	客户端图像映射（即热区）
    6. object	object对象
    7. script	客户端脚本
>
> 3. 如何让块级元素水平居中？如何让行内元素水平居中?如何让 inline-block 元素水平居中？

*   块级元素水平居中：margin:0 auto;

*   行内元素水平居中：父容器设置text-align:center;

*   inline-block元素水平居中：父容器设置text-align:center;
>
> 4. 单行文本溢出加 ...如何实现?

*   white-space:nowrap      不折行
*   overflow:hidden         溢出之后隐藏
*   text-overflow:ellipsis  显示三个点
>
> 5. px, em, rem,vw 有什么区别

*   px：像素，绝对单位
*   em：1em = 默认字体大小的倍数(比如不设置时是字体是20px，那2em 就是40px)
*   rem：1rem = 根元素(html 节点)字体大小的倍数。IE8 及以下不支持 rem.
*   vw：相对于父元素宽度的百分比，1vw = 1%*父元素width
>
> 6. 解释下面代码的作用? 字体里\5b8b\4f53代表什么?
>
```
body{
    font: 12px/1.5 tahoma,arial,'Hiragino Sans GB','\5b8b\4f53',sans-serif;
}
```

*   设置body元素中字体大小为12px，行高为字体大小的1.5倍，字体优先级依次为tahoma、arial、‘Hiragino Sans GB’、黑体、scans-serif；
*   '\5b8b\4f53'代表汉字“黑体”。

> 7. 实现如下效果
>
>    1. http://js.jirengu.com/siyowirubu
>
*   效果代码：http://js.jirengu.com/nodojenivi/11/edit
>
> 8. 实现如下效果
>
>    ![img](http://cloud.hunger-valley.com/17-10-12/36694508.jpg)
>
>    
>
>    效果线上[预览地址](http://book.jirengu.com/jrg-team/frontend-knowledge-ppt/code/hunger-ui/button.html)

*   效果代码：http://js.jirengu.com/zadegunoca/2/edit
>
> 9. 实现如下两个表格效果
>
>    ![img](http://cloud.hunger-valley.com/17-10-12/86785917.jpg)
>
>    
>
>    [线上预览地址](http://book.jirengu.com/jrg-team/frontend-knowledge-ppt/code/hunger-ui/table.html)

*   效果代码：http://js.jirengu.com/guwobovuba/2/edit
>
> 10. 实现如下三角形
>
>     
>
>     ![img](https://static.xiedaimala.com/xdml/image/b9807bae-0127-4b33-8530-56e42fd15104/2018-12-7-13-49-32.pic.jpg)

*   效果代码：http://js.jirengu.com/hibilirajo/8/edit
>
> 