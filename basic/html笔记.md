1.标题与段落：
	标题：h1-h6
	段落：p
2.文本的修饰标签：
	强调：strong，加粗
	强调：em，斜体
	sup：上标
	sub：下标
	del：删除，样式为：中间被横线划掉
	ins：插入，样式为：添加下划线
3.图片标签：
	img：单标签
		src：图片的地址
		alt：当图片加载出现问题的时候，添加一段有好的提示文字
		title：几乎所有标签共有的属性，鼠标放在标签上，显示该提示信息
		width，height
4.相对路径绝对路径：
	.表示当前文件夹
	./表示当前文件夹下的文件
	..表示上一级文件夹
5.链接标签：
	a: 双标签 <a></a>
		href:链接地址
		target：可以改变链接打开的方式，默认在当前页面打开（_self），若在新页面打开（_blank）
		
	base:单标签：改变链接默认行为的。写在head标签中，<base target="_blank">
6.跳转锚点：
	实现方式一：#和id
	实现方式二：#和name（name属性加给a标签）
	（详情参考6.跳转锚点.html）
7.特殊符号：
	具体内容百度html特殊符号代码
8.列表标签：
	ul li：无序列表；样式：type：
							disc：默认，实心圆
							circle：空心圆
							square：实心方块
	ol li：有序列表；（type能够标识顺序，eg：123等，无序列表则是实心圆等这些）
				样式：type：
						1，a, A, i, I(i和I为罗马数字)
	dl，dt，dd：定义列表：列表项需要添加标题和对标题进行描述的内容；（详情参考8.列表标签.html）
9.表格标签：
	table：表格的最外层容器
	tr：表格行
	th：表头
	td：表格单元
	caption：表格标题
	语义化标签：
	tHead
	tBody
	tFoot
	eg.
		table-caption-thead开始-thead里面包th-多个tbody开始-里面包tr-tr里面包td-最后tfoot
	表格的属性：
	border：边框
	cellpadding：单元格内的空间
	cdllspacing：单元格之间的边距
	rowspan：合并行
	clospan：合并列
	align：左右对齐方式
	valign：上下对齐方式
10.表单标签：
	form标签：表单的最外层容器
	input标签：单标签；type：（text（placeholder就是android中的hint属性）、password、checkbox（checked表示默认选中）、
							radio（通过name属性来标识是不是一组，才会有是否互斥的效果），file、submit、reset）
						disable：表示禁止使用
	textarea标签：多行文本框；cols，rows通过行列调整大小
	select+option标签：下拉标签：select（size=2的话会出现两项可选择的选项，multiple可以进行多选（多选属性其他例子：比如file标签添加multiple属性就可以一次选择多个文件）），
							option（selected表示默认被选中，disable不能被选择）
	label标签：辅助标签
	（详情参考10.表单标签.html）
11.div和span
	div是块；span是修饰文字的，内联
	