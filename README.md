1、ABCD
2、D

简单题1、
触发prepatch钩子函数
触发update钩子函数
新节点如果有text属性&&不等于旧节点的text属性
	如果老节点中有子节点
		移除老节点child对应的COM元素
	否则
		设置新节点的对应DOM元素的textContext
新老节点都有child，且不相等
	调用updateChildren（）
	对比子节点，并且更新子节点的差异
只有新节点有child属性
	如果老节点有text属性
		清空这个textContent
	添加所有的子节点
只有老节点有child
	移除所有的老节点
只有老节点有text属性
	清空dom元素对应的textContent
出发postpatch钩子函数