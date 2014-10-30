jQuery-plugins-mask
==============
### 示例HTML
```html
<a href="javascript:void(0)" class="J_mask-btn">mask</a>
<a href="javascript:void(0)" class="J_mask-btn-close">mask close</a>
<script>
$(function(){
	$(".J_mask-btn").on("click",function(){
		$.mask()
	})
	$(".J_mask-btn-close").on("click",function(){
		$.mask(false)
	})
})
</script>
```
### Live Demo
[View Demo](http://17leba.github.io/demo/jQuery-mask/)
### 参数默认为空，直接加入透明度为50的黑色背景
```html
$.mask()
```
### 参数为fasle，删除mask
```html
$.mask(false)
```
### 参数默认值为：
```html
"position":"absolute",
"width":"100%",
"height":"100%",
"background-color":"#000",
"filter":"alpha(opacity=50)",
"opacity":.5,
"z-index":999,
```
###可以自定义设置参数对象
```html
$.mask({
	"background-color":"#fff",
	"z-index":1000
})