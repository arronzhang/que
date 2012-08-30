前端笔试题
==========

姓名_____________		电话______________

JavaScript
-----------------

###1. 写出下面代码执行结果

	function C1( name ) {
		if ( name ) this.name = name;
	}

	function C2( name ) {
		this.name = name;
	}

	function C3( name ) {
		this.name = name || 'John';
	}

	C1.prototype.name = 'Tom';
	C2.prototype.name = 'Tom';
	C3.prototype.name = 'Tom';

	alert( ( new C1() ).name + ( new C2() ).name + ( new C3() ).name );


###2. 写出下面代码执行结果

	window.number = 2;
	var obj = {
		'number': 4,
		'db1': ( function () {
			this.number *= 2;
			return function() {
				this.number *= 2;
			}
		} )()
	};

	var db1 = obj.db1;
	db1();
	obj.db1();
	alert( window.number + obj.number );

###3. 写一个函数，将给定字符串中出现的数字，替换为原数字与10的和

例：

Hello World, I Have __10__ big apples and __05__ pens.

->

Hello World, I Have __20__ big apples and __15__ pens.


综合
-----------------

###1. 请分析以下结构中，A标签字体颜色

	<style>
		a{ color: #ccc }
		#contact a{ color #333 }
		.safelink a{ color: #999 }
		h1 a{ color: #eee }
	</style>
	<div id="contact">
		<h1 class="safelink">
			<a href="http://3w.org">www</a>
		</h1>
	</div>

###2. label标签有什么用？




###3. IE下，mouseover与mouseenter事件有什么区别？



###4. 列举常见的JavaScript兼容性区别（4个）






###5. 列举你常用的开发与调试工具











解答
------------------------

1.1	TomundefinedJohn
1.2	16
1.3	str.replace(/\d+/g, function(a){ return 10 + parseInt(a) });

2.1	#333



