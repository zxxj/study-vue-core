<template>
	<!-- 
		思考: 在.vue文件template中写入的html元素是真实的html元素节点吗?
		答案: 不是的
		原因: 
			1.原因非常简单,如果在template中写入的是真实的html节点的话,对于v-if,v-bind,keep-alive这些东西,浏览器明显是不认识的,所以这些东西理应无法解析

			2.但现实可以发现这些vue中提供的指令或组件竟然被被浏览器解析了,并生成了真实的dom节点,所以vue不难猜出,一定是vue在中间做了什么,让假的html节点被渲染成了真实的html节点

			3.vue在中间做了什么?
				简单来说可以分为两件事:
					1.编译时: compiler
					2.运行时: runtime
					3.运行时 + 编译时: runtime + compilter
	 -->
	<div id="app">
		<div class="box" v-if="false">xin</div>
	</div>

</template>

<script>



</script>