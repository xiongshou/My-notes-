# 创建表单

```html
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>sss</title> 
</head>
<body>
	<form method=post>
 		<fieldset>
	 		<legend>Personalia:</legend>
  			Name: <input type="text" maxlength="10" required="true" size="10" value="sss" pattern=""><br/>
  			Email: <input type="text"><br/>
  			Date of birth: <input type="text"><br/>
			<!-- 下拉菜单-->
			<select name="shiuo">
				<option selected>sds<option>
				<option>sas<option>
				<option>sds<option>
	 		</select>
	 		<br/>
	 		<!-- 单选框-->
	 		<input name="dan1" type="radio">first
	 		<input name="dan1" type="radio">second
	 		<input name="dan1" type="radio">third
	 		<br/>
	  		邮箱<input type="Email">
			<br/>
			<!-- 复选框-->
			<input name="fu" type="checkbox" value="">first
			<input name="fu" type="checkbox" value="">secong
			<input name="fu" type="checkbox" value="">third
 		</fieldset>
	<!-- 提交、重写-->
	<input type="submit" value="提交">
	<input type="reset" value="重写">
</form>

</body>
</html>
```

![image-20201217000805646](https://tva1.sinaimg.cn/large/0081Kckwly1glq5bbiqmgj30xs0fogms.jpg)



# 日期对象

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
</head>
<body>
<script>
	function output(){
		var date1=new Date();
		var year=date1.getFullYear();
		alert(year);
	}
</script>
<input type="button" onclick="output()" value="获取日期"/>
</body>
</html>
```



# 列表

```html
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
</head> 
<body>

<h4>无序列表:</h4>
<ol start=4 type="i">
  <li>Coffee</li>
	<ul>
		<li> ds</li>
		<li> ds</li>
	</ul>
  <li>Tea</li>
  <li>Milk</li>
</ul>

</body>
</html>
```

# 表格

边框属性

frame外边框属性

* above显示上边框
* below显示下边框
* hsides显示上下边框
* vside显示左右边框
* lhs显示左边框
* rhs显示右边框
* border显示上下左右边框
* void不显示边框

rules内边框属性

* all显示所有内部框线
* none不显示内部框线
* rows就显示行边框
* cols就显示列边框
* grops和none差不多



# CSS

* color文本颜色
* Font-family文本的字体
* font-style字体的样式（斜体、正常、倾斜）
* font-variant小型大写字母
* font-weight字体的粗细
* font-size文本的大小
* line-height文本的行高
* font一次设置多种属性

---

* line-height行间距
* letter-spacing字符间距
* word-spacing字间距
* text-align水平对齐
* vertical-align垂直对齐
* text-indent缩进文本
* text-transform字符转换
* text-decoration文本修饰

![image-20201217104625233](https://tva1.sinaimg.cn/large/0081Kckwly1glqnrgll9hj31360tkqsh.jpg)



---

web标准：结构（html）、行为（css)、表现（JavaScript)



---

![image-20201217111006718](/Users/xiongshou/markdown/课程/image-20201217111006718.png)

![image-20201217111656630](https://tva1.sinaimg.cn/large/0081Kckwly1glqonk1trvj30ym0ea11h.jpg)

![image-20201217111847370](https://tva1.sinaimg.cn/large/0081Kckwly1glqop472sbj312409qn4f.jpg)

![image-20201217111923445](/Users/xiongshou/markdown/课程/image-20201217111923445.png)

![image-20201217112041289](https://tva1.sinaimg.cn/large/0081Kckwly1glqor2yj45j311808sq6d.jpg)

![image-20201217112117682](https://tva1.sinaimg.cn/large/0081Kckwly1glqorth6vvj31400nktog.jpg)****

![image-20201217112226369](/Users/xiongshou/markdown/课程/image-20201217112226369.png)

![image-20201217112405929](https://tva1.sinaimg.cn/large/0081Kckwly1glqoun8asjj311k0qan84.jpg)

![image-20201217112607646](/Users/xiongshou/markdown/课程/image-20201217112607646.png)