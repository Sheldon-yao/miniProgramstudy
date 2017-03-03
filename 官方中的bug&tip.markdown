##官方中的bug&tip
###scroll-view
	1.tip: 请勿在 scroll-view 中使用 textarea、map、canvas、video 组件
	2.tip: scroll-into-view 的优先级高于 scroll-top
	3.tip: 在滚动 scroll-view 时会阻止页面回弹，所以在 scroll-view 中滚动，是无法触发 onPullDownRefresh
	4.tip: 若要使用下拉刷新，请使用页面的滚动，而不是 scroll-view ，这样也能通过点击顶部状态栏回到页面顶部
###input
	1.bug : 微信版本 6.3.30, focus 属性设置无效；
	2.bug : 微信版本 6.3.30, placeholder 在聚焦时出现重影问题；
	3.tip : input 组件是一个 native 组件，字体是系统字体，所以无法设置 font-family；
	4.tip : 在 input 聚焦期间，避免使用 css 动画；
###text
	tip: text 的长按复制功能尚未实现。
###textarea
	1.bug: 微信版本 6.3.30，textarea 在列表渲染时，新增加的 textarea 在自动聚焦时的位置计算错误。
	2.tip: textarea 的 blur 事件会晚于页面上的 	3.tap 事件，如果需要在 button 的点击事件获取 textarea，可以使用 form 的 bindsubmit。
	4.tip: 不建议在多行文本上对用户的输入进行修改，所以 textarea 的 bindinput 处理函数并不会将返回值反映到 textarea 上。
	5.tip: textarea 组件是由客户端创建的原生组件，它的层级是最高的。
	.tip: 请勿在 scroll-view 中使用 textarea 组件。
	7.tip: css 动画对 textarea 组件无效。
###video&map&canvas
	1.tip: video 组件是由客户端创建的原生组件，它的层级是最高的。
	2.tip: 请勿在 scroll-view 中使用 video 组件。
	3.tip: css 动画对 video/map/canvas 组件无效。
	4.tip:covers 属性即将移除，请使用 markers 替代。（video）