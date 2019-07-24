
## 问题

> 1. post 和 get 方式提交数据有什么区别？

*   表象不同，get把提交的数据url可以看到，post看不到.
*   原理不同，get 是拼接 url， post 是放入http 请求体中.
*   提交数据量不同，get最多提交1k数据，浏览器的限制。post理论上无限制，受服务器限制.
*   get提交的数据在浏览器历史记录中，安全性不好.
*   场景不同，get 重在 "要", post 重在"给".

> 2. 在input里，name 有什么作用？

*   name 属性规定 input 元素的名称.
*	name会作为表单的一部分提交给后台
```
<input name="user" type="text" value="aaa" >//会提交{user：aaa}
```

> 3. radio 如何分组？

*   设置 name 属性，相同的为一组.

> 4. placeholder 属性有什么作用？

*  placeholder 属性提供可描述输入字段预期值的提示信息（hint）。
    该提示会在输入字段为空时显示，并会在字段获得焦点时消失。

> 5. CSRF 攻击是什么？如何防范？

*   其原理是攻击者构造网站后台某个功能接口的请求地址，诱导用户去点击或者用特殊方法让该请求地址自动加载。用     户在登录状态下这个请求被服务端接收后会被误以为是用户合法的操作。

>防范：

*   验证 HTTP Referer 字段.
*   使用验证码.
*   在请求地址中添加token并验证.
*   在HTTP 头中自定义属性并验证.


> 6. type=hidden隐藏域有什么作用? 举例说明

```
1、隐藏域在页面中对于用户是不可见的，在表单中插入隐藏域的目的在于收集或发送信息，以利于被处理表单的程序所使用。浏览者单击发送按钮发送表单的时候，隐藏域的信息也被一起发送到服务器。
2、有些时候我们要给用户一信息，让他在提交表单时提交上来以确定用户身份，如sessionkey，等等．当然这些东西也能用cookie实现，但使用隐藏域就简单的多了．而且不会有浏览器不支持，用户禁用cookie的烦恼。
3、有些时候一个form里有多个提交按钮，怎样使程序能够分清楚到底用户是按那一个按钮提交上来的呢？我们就可以写一个隐藏域，然后在每一个按钮处加上 onclick="document.form.command.value="xx""然后我们接到数据后先检查command的值就会知道用户是按的那个按钮提交上来的。
4、有时候一个网页中有多个form，我们知道多个form是不能同时提交的，但有时这些form确实相互作用，我们就可以在form中添加隐藏域来使它们联系起来。
5、javascript不支持全局变量，但有时我们必须用全局变量，我们就可以把值先存在隐藏域里，它的值就不会丢失了。
6、还有个例子，比如按一个按钮弹出四个小窗口，当点击其中的一个小窗口时其他三个自动关闭．可是IE不支持小窗口相互调用，所以只有在父窗口写个隐藏域，当小窗口看到那个隐藏域的值是close时就自己关掉。
如：
1.<input type=hidden name=coun value=<%=cc%>>
这里的隐藏域名为coun，值为<%=cc%>，假设前面cc=100的话，即值为100；
2.递交表单<form action=xx.asp>到新页面xx.asp；
3.在xx.asp页中，使用request.write request.form("coun")，则在页面中显示的值就是100。
```


> 7. 实现如下表单,附上预览地址。其中性别和取向是单选，爱好是多选
>    ![](http://cdn.jscode.me/6f0fa6d8-beb1-44ab-b8ea-5368a0d2d67b)
```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>表单</title>
	</head>
	<body>
		<form name="input" action="">
			姓名：<input type="text" value="用户名" name="a" /><br />
			密码：<input type="password"  name="b" /><br />
			性别：<input type="radio"  name="sex" />男
                             <input type="radio"  name="sex" />女<br />
			取向：<input type="radio"  name="sex1" />男
			     <input type="radio"  name="sex1" />女<br />
			爱好：<input type="checkbox" value="data" name="hobby"  />data
			     <input type="checkbox" value="travel" name="hobby"  />旅游
			     <input type="checkbox" value="pet" name="hobby"  />宠物<br />
			评论：<textarea rows="10" cols="30"></textarea><br />
			我的car：
				<select name="cars">
				<option value="张三">张三</option>
				<option value="李四">李四</option>
				<option value="王五">王五</option>
				<option value="燕六">燕六</option>
				</select>
				<input type="submit" value="提交" />
		</form>
		
	</body>
	
</html>
```

> 8. label 有什么作用？如何使用？

*   label标签来定义表单控制间的关系,当用户选择该标签时，浏览器会自动将焦点转到和标签相关的表单控件上。

```
<label for="Name">Number:</label> <input type=“text“name="Name" id="Name"/>

<label>Date:<input type="text" name="B" /></label>
```

> 9. 以下input有何作用？

>    ```html
>    <input type="submit" value="提交">
>    ```

*   表单的提交按钮


> 10. bing或者 google 搜索：“stackoverflow http get length”，找到第一条检索结果，大致翻译得票最高的答案

*   HTTP GET请求的长度限制取决于服务器和使用的客户端（如果适用，还取决于服务器或客户端使用的代理）。

    大多数Web服务器的限制为8192字节（8KB），通常可在服务器配置中的某处进行配置。

*   如果在浏览器或服务器中超出限制，大多数将仅截断限制之外的字符而不发出任何警告。但是，某些服务器可能会发     送HTTP 414错误。

> js在线编辑器：[https://jsfiddle.net/](https://jsfiddle.net/)

##CSRF攻击文章：

> CSRF攻击文章：
>
> 先从一个故事说起（故事纯属虚构，恶意模仿后果自负）：
>
> 小谷最近遭遇电信诈骗被骗的倾家荡产，于是他想到了报复社会。在知乎上狂点800个没有帮助1000个举报后，他决定做点正事干票捞钱的生意。
> 「很多视频网站都有赠送礼品的功能，假如所有人都赠送我个礼物，我再转卖掉，不就发财啦」小谷寻思着。
> 说干就敢，经过一番折腾测试，小谷发现视频网站赠送礼物的接口是:
>
> ```
> https://xxxx.com/gift/send?target=someone&giftId=ab231 
> ```
>
> ， 原来只要用户在登录状态下请求这个地址，就能给名为someone的用户赠送礼品ab231。
> 那如何才能让其他用户请求这个接口呢？其实只要用户点击就行，「色诱是最好的陷阱」回想起自己被骗的经过，小谷猥琐狠狠的打了一行文字 ——「想要的都在这里，今夜注定让你无眠~~ [饥人谷-最有爱的前端学习社区](http://jirengu.com/)」，然后在各个群组里回复。
> 经过一天等待，有几个上钩的，但远远达不到预期，「有没有更自动的办法，让用户只要看到即使不点也能上钩呢？」。小谷开始对整个网站功能逐一过滤，突然他眼前一亮，在用户评论编辑框内看到了上传外链图片的功能。「如果把这个 url 作为图片填进去，上传后会在评论区创建一个img 标签，src 对应的就是这个地址。当用户打开页面后这个 img 就会自动加载图片也就是发送这个请求，这样一来凡是打开这个页面的人不论是不是点击这个链接都会给赠送礼物，perfect!」 小谷为自己的聪明才智惊叹。
> 又过了一天，果然源源不断的礼物送了过来。这个时候小谷隐隐有些担心起来，虽然礼物送的都很小，但赠送都是有历史记录的，用户查看历史记录肯定会起疑心，能不能帮用户删除这条赠送记录呢？经过测试，发现删除赠送记录的接口地址是
>
> ```
> https://xxxx.com/gift/deleteRecord
> ```
>
> ， 接口类型为POST，请求参数为 { giftId:"ab231"}。 用户无法通过点击一个链接在不知情的情况下发送 POST 请求，怎么办呢？于是，小谷构造了一个页面：
>
> ```html
> <form action="https://xxxx.com/gift/deleteRecord" id="form" method="post" target="hiddenIframe">
> 
> </form>
> <script>
>     document.getElementById('form').submit();
>     location.href = "http://xxxx.com";
> </script>
> ```
>
> 当用户点开这个页面的链接后，会自动发送 POST 请求，然后跳转到原始首页。这样用户既在不知情的情况下赠送了礼品，又在不知情的情况下删除了赠送记录。大功告成后，小谷购买了个广告机在各大论坛狂发....
>
> 一周之后，警察👮叔叔来敲门了，咚🕳🕳
>
> 上面小谷的攻击流程就是典型的 CSRF (Cross Site Request Forgery)攻击，中文名：跨站请求伪造。其原理是攻击者构造网站后台某个功能接口的请求地址，诱导用户去点击或者用特殊方法让该请求地址自动加载。用户在登录状态下这个请求被服务端接收后会被误以为是用户合法的操作。对于 GET 形式的接口地址可轻易被攻击，对于 POST 形式的接口地址也不是百分百安全，攻击者可诱导用户进入带 Form 表单可用POST方式提交参数的页面。
>
> 后续......
>
> xxxx视频网站不断接到用户举报，自己的礼品莫名丢失。经过排查发现有攻击者利用 CSRF 进行攻击，报警后赶紧让公司的安全部门的小饥来修复漏洞。
>
> 小饥梳理了一遍公司网站所有的接口，发现很多接口都存在这个问题。于是采用了anti-csrf-token的方案。 具体方案如下：
>
> 1. 服务端在收到路由请求时，生成一个随机数，在渲染请求页面时把随机数埋入页面（一般埋入 form 表单内，`<input type="hidden" name="_csrf_token" value="xxxx">`）
> 2. 服务端设置setCookie，把该随机数作为cookie或者session种入用户浏览器
> 3. 当用户发送 GET 或者 POST 请求时带上_csrf_token参数（对于 Form 表单直接提交即可，因为会自动把当前表单内所有的 input 提交给后台，包括_csrf_token）
> 4. 后台在接受到请求后解析请求的cookie获取_csrf_token的值，然后和用户请求提交的_csrf_token做个比较，如果相等表示请求是合法的。
>
> 
>
> ![img](https://ooo.0o0.ooo/2017/06/19/594788ec88c03.jpeg)
>
> 
>
> 
>
> ![img](https://ooo.0o0.ooo/2017/06/19/5947890316b95.jpeg)
>
> 
>
> （上图是某电商网站的真实设置，这里页面上设置的 token和session里设置的token 虽然不直接相等，但 md5('1474357164624') === '4bd4e512b0fbd9357150649adadedd4e'，后台还是很好计算的）
>
> 安全部的Leader 看了看小饥的方案，「方案出的很赞， 不过还有几点需要注意一下」：
>
> 1. Token 保存在 Session 中。假如 Token 保存在 Cookie 中，用户浏览器开了很多页面。在一些页面 Token 被使用消耗掉后新的Token 会被重新种入，但那些老的 Tab 页面对应的 HTML 里还是老 Token。这会让用户觉得为啥几分钟前打开的页面不能正常提交？
> 2. 尽量少用 GET。假如攻击者在我们的网站上传了一张图片，用户在加载图片的时候实际上是向攻击者的服务器发送了请求，这个请求会带有referer表示当前图片所在的页面的 url。 而如果使用 GET 方式接口的话这个 URL 就形如：
>    `https://xxxx.com/gift?giftId=aabbcc&amp;_csrf_token=xxxxx`
>
> ，那相当于攻击者就获取了_csrf_token，短时间内可以使用这个 token 来操作其他 GET 接口。
>
> 「这个项目，就由你来推动实施，晚上加加班争取这两天搞定~」

