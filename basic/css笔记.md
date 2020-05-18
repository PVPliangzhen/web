1.css格式：
	选择器{属性名称:属性值; 属性名称2:属性值2}
	width，height，background-color
	像素px和%用来表示大小，%根据父容器来决定。
2.css样式的引入方式：
	1）内联样式（行内、行间样式）（在标签中使用style）
	2）内部样式（写在head中的stytle，可以复用且可以让样式可结构分开处理）
	3）外部样式（引入一个单独的css文件）
		1.<link>标签：引入外部资源，rel属性指定资源跟页面的关系，href属性指定资源的地址
		2.通过@import方式引入外部样式表（这种方式有很多问题，不建议使用）
3.颜色表示法：
	单词表示法，16进制表示法，rgb表示法
4.背景样式：
	background-color，background-image，background-repeat（repeat, repeat-x, repeat-y, no-repeat），
	background-position：（1.x:number, y:number坐标值或者百分比%；2.x:left,right,top.bottom,center等，y...）
	background-attachment：背景图随滚动条移动的方式（scroll（默认值，背景位置按照元素进行偏移），fixed（背景位置按照浏览器进行偏移））
	(详情参考视觉差文件夹)
5.边框样式：
	border-style（solid，dashed（虚线），dotted（点线）），border-width，border-color，
	border-right-style，border-right-color（只针对某一条边进行设置，left，right，top，bottom）......
6.文字样式：
	1.font-family:字体类型：中文字体（中英文都支持）和英文字体（不支持中文），默认为微软雅黑
	2.衬线体（端点有棱角：宋体）和非衬线体（端点没棱角：微软雅黑）
	3.设置多字体的方式：
		1.用逗号隔开（电脑不识别那么会自动向后继续识别，即备选方案（计算机内的字体，控制面板里面字体的种类））
		2.***当字体的中间有空格需要加引号，没有空格的话不需要加引号***
	4.font-size：默认16px，
		1.设置具体像素数值（规范用偶数）
		2.属性取值（xx-small，x-small，small，medium（16px）， large， x-large，xx-large）（单词表示法不建议使用，因为不够具体）
	5.font-weight：normal，bold（加粗），或者数值（100px-900px成百的整数，100-500都是normal，600-900都是bold，实际上也是只有两种类型）
	6.font-style: normal, italic(斜体), oblique（也是斜体，不推荐使用，因为人家不想支持非得强迫人家支持倾斜属性会很奇怪）
		（1.italic所有带有倾斜属性的字体才可以设置倾斜属性， 2.oblique没有倾斜属性的字体也可以设置倾斜属性）
	7.color：字体颜色
7.段落样式：
	1.text-decoration：下划线underline，删除线linethrough，上划线overline，不添加修饰none等（可用空格隔开，同时添加多可文本修饰）
	2.text-transform：英文文本的大小写（lowercase，uppercase，capitalize（只针对首字母大写，其他字母大小写不管））
	3.text-indent：文本缩进（eg.20px，或者取两个文字像素的写法（默认一个字16px，那么两个字就是32px），可以写成2em（根据文字大小动态变化）；中英文混排无法对齐）
	4.text-align：文本对齐方式（left，right，center，justify（两端点对其））
	5.line-height：两种取值方式（默认16px情况下）：
		1.特定像素：20px
		2.比例值：1（则为16px），2（则为32px）
	6.letter-spacing：字的间距
	7.word-spacing：词的间距（针对英文）
	8.英文折行：（默认情况下在某个特定区域，数字和英文很长的话不会自动折行）
		1.word-break：break-all（非常强烈的折行）
		2.word-wrap：break-word（不是很强烈，会产生一些空白区域）
9.css复合样式：通过空格来分割：(有的不需要关心顺序问题（background、border），有的需要关心顺序问题（font）)
	1.background:red url() repeat 0 0; eg.background:red url("") no-repeat center center;
	2.border:1px red solid
		border-right:......
	3.font：最少要有两个值（先size后family，size和family顺序不能变，其他属性可以不关心顺序问题，不过size和family要放在最后）
		eg.weight style size family
			style weight size family
			weight style size/line-height family
			(以上都是正确的写法，color不能写，因为color不属于font的)
	***单一样式和符合样式尽量不要混写，如果非要混写，那么先写复合再写单一（复合会把单一覆盖掉）***
10.选择器：
	1.id选择器：#
		1.在一个页面中，id取值必须唯一（出现多次不报错但是不符合规范）
		2.字母，_（下划线），-（中划线），数字来命名（数字不能开头）
		3.驼峰式，下划线式，短线（中划线）式
	2.class选择器：.
		1.class一个页面可以重复，提高复用
		2.可以添加多个class样式，用空格分开（class="style1 style2"）
		3.多个样式时，由css的顺序决定，而不是class的里面多样式的顺序
		4.标签+类的写法（标签.class--->p.style1）
	3.标签选择器：（TAG选择器、元素选择器）
		1.去掉某些标签的默认样式
		2.复杂的选择器中（比如：层级选择器）
	4.群组选择器：（分组选择器）(用逗号分隔)
		div,p,.class,#id{......}
	5.通配选择器：
		*{}（所有标签），尽量避免使用通配选择器
		1.去掉所有标签的默认样式
	6.层次选择器：
		1.后代：M N
		2.父子：M > N
		3.兄弟：M ~ N M下面的所有N标签，上面的不生效
		4.相邻：M + N M下面相邻的N标签，上面的不生效
	7.属性选择器：
		（=完全匹配，*=部分匹配，^=起始匹配，$=结束匹配，[][]多个[]进行组合匹配）
		详情参考css10.属性选择器.html
	8.伪类选择器：
		:link访问前的样式, （只能给a标签）
		:visited访问后的样式, （只能给a标签）
		:hover鼠标移入时的样式, （可以添加给所有标签）
		:active鼠标按下时的样式,（可以添加给所有标签）
		eg.div:hover{}
		注：
			1.如果给a标签添加四种样式需要顺序：L V H A
			2.一般网站只设置a{} 和 a:hover{}
		:after, :before, 通过伪类的方式给元素添加一段文本内容，使用content属性
		eg.div:after{content="..."}
		:checked, :disabled, :focus（获取光标的时候）, 针对表单元素
		
	9.结构性伪类选择器：
		1.nth-of-type(index)和nth-child(index)（两个选择器效果几乎完全一样）:（角标从1开始, n表示从0到无穷大, 2n表示偶数，2n+1表示奇数）
		2.first-of-type和first-child:index = 1
		3.last-of-type和last-child:index = 最后
		4.only-of-type和only-child: 唯一的时候才会生效
		eg.ul嵌套5个li：(li:nth-of-type(2n+1){...}或者child(2n+1){...}则选中了奇数的)
		区别：
		nth-of-type(index)：类型
		nth-child(index)：孩子
		详情参考css10.结构性伪类选择器.html
11.css的继承：（文字相关的样式可以被继承，但是布局相关的样式不能被继承）
		
	
			
		
	

