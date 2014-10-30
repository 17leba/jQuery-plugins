jQuery-plugins
==============
// 参数默认为空，直接加到J_loading-1后面<br>
$(".J_loading-1").loading()<br>
<br>
// 参数为字符串类名，类名需要自定义<br>
$(".J_loading-2").loading("loading-img");<br>
<br>
// 参数为对象，设置自定义imgUrl，calssname，以及插入位置<br>
// 插入位置参数有三个可选：<br>
// 默认为insertAfter，插入到当前元素后面<br>
// appendTo：插入到设置元素的末尾<br>
// insertBefore：插入到设置元素前面<br>
// 三个参数不可同时设置，若同时设置，则优先级高低为：<br>
// appendTo > insertBefore > insertAfter <br>
<br>
// 默认为accord，插入到当前元素后面<br>
$(".J_loading-3").loading({
	imgUrl:"http://static.hiwifi.com/ued/images/icons/big_loading.gif",
	classWrap:"loading-3"
})<br>
// appendTo：插入到设置元素的末尾<br>
$(".J_loading-4").loading({
	imgUrl:"http://static.hiwifi.com/ued/images/icons/big_loading.gif",
	appendTo:$(".loading-box:eq(0)")
})<br>
// insertBefore：插入到设置元素前面<br>
$(".J_loading-5").loading({
	imgUrl:"http://static.hiwifi.com/ued/images/icons/big_loading.gif",
	insertBefore:$(".loading-box:eq(1)")
})<br>
<br>
// 参数为false时，删除添加的loading img<br>
var i = 0;
$(".J_loading-6").on("click",function(){
	if(i++ % 2 === 0){
		$(this).loading({
			imgUrl:"http://static.hiwifi.com/ued/images/icons/big_loading.gif",
			insertAfter:$(".loading-box:eq(2)")
		})
	}else{
		$(this).loading(false)
	}
})<br>
// 参数为字符串时<br>
// 当然也可以自己手动删除添加的classname，如<br>
// $(".J_loading-7").removeClass("loading-img")<br>
var j = 0;
$(".J_loading-7").on("click",function(){
	if(j++ % 2 === 0){
		$(this).loading("loading-img");
	}else{
		$(this).loading(false)
	}
})
