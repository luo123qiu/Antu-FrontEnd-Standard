# 安途前端规范
1. 说明
	* 建立此文档旨在统一安途前端编码规范和风格，让所有代码都是有规可循的，并且能够得到沉淀，减少重复劳动。
	* 团队内所有人均可参与文档建设与维护
	* 此文档使用`Markdown`编写，[Markdown语法说明](http://wowubuntu.com/	markdown/)  
	  `Windows` [MarkdownPad](http://markdownpad.com/)、[MarkPad](http://code52.org/DownmarkerWPF/)  
	  `Mac` [Mou](http://mouapp.com/)  
	  `Linux` [ReText](http://sourceforge.net/p/retext/home/ReText/)
1. 开发规范
	* CSS
		* 使用[LESS](http://lesscss.net/)编写生产环境CSS代码
		* class使用`-`作为命名连接符，如：`.site-title`, `main-menu`
		* id使用`_`作为命名连接符，如：`site_wrapper`, `site_footer`
		* 所有CSS代码全部使用小写
		* 尽量避免类似`margin-23`，`padding-17`这样无意义且无法复用的命名
		* 使用统一`CSS Reset`
		* `CSS Hack`
		* 使用`:after`或`overflow`清除浮动，不要在html里增加多余的标签
		* 避免使用低效的选择器，参考文献：[高效地呈现CSS](http://www.lizhenwen.com/w3c/1034)
	* HTML
		* 使用`HTML5`标准格式编写HTML代码
		* 调用本地公共库或使用 [百度](http://developer.baidu.com/wiki/index.php?title=docs/cplat/libs) / [新浪](http://lib.sinaapp.com/) / [又拍](http://jscdn.upai.com/) 提供的CDN公共库
		* 框架级DOM使用`id`作为标记，其余全部使用`class`
		* 所有代码全部使用小写，DOM属性值使用双引号包裹
		* 交互型DOM添加以`data-`为前缀的属性，如`data-model="banner"`
		* `<img>`标签默认缺省格式：`<img src="xx.png" alt="缺省文字" />`
		* `<a>`标签默认缺省格式：`<a href="###" title="链接名称">链接文字</a>`
		* 统一标签结尾斜杠的书写形式：`<br />`, `<hr />` 注意空格
		* 避免使用过时的标签，如`<b>`, `<i>`而使用`<strong>`, `<em>`代替
		* 避免使用`style="xxx:xxx"`的内联样式表
		* `css`,`jQuery`及`Google Analytics`引用置于文档头部
		  `<head>`  
		  `……`  
		  `<link href="style.css" rel="stylesheet" />`  
		  `<script src="/jquery-1.9.1.min.js"></script>`  
		  `//放置Google Analytics代码`  
		  `</head>`
		* 其它js及统计代码置于文档底部  
		  `<body>`  
		  `……`  
		  `<script src="script.js"></script>`  
		  `//其他JS代码`  
		  `</body>`
		* css, js调用不添加`type="xxx"`
		* 特殊符号使用参考 [HTML ISO-8859-1 参考手册](http://www.w3school.com.cn/tags/html_ref_entities.html)
	* JS
		* 不在HTML文档中直接编写Javascript代码
		* 建议：jQuery变量首字符为`$`，私有变量首字符为`_`
		* 所有语句结束后必须使用`;`结束
		* 当需要通过JS来改变样式时，通过改变class名来完成，而不是直接设置元素style的值  
		  参考文献：[回流与重绘：css性能让javascript变慢？](http://www.zhangxinxu.com/wordpress/?p=600)  
		  英文原文：[Reflows & Repaints: CSS Performance making your JavaScript slow?](http://www.stubbornella.org/content/2009/03/27/reflows-repaints-css-performance-making-your-javascript-slow/)
		* JS调试使用`console.log()`进行，避免使用弹出框，线上版本需要注释所有调试代码
		* 编写更高效的jQuery代码：[jQuery最佳实践](http://www.ruanyifeng.com/blog/2011/08/jquery_best_practices.html)
