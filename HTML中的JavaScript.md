# src属性

要包含外部的JavaScript文件，需要在src属性中设置包含文件的URL，文件可以跟网页在同一台服务器上，也可以在不同的域，也就是说`<script></script>`标签可以跨域。
```javascript
<script src="example.js"></script>
```

# 执行顺序

所有的`script`标签都将按顺序执行，在不使用`defer`和`async`属性的情况下。

# 代码中的位置

按照顺序执行的逻辑，如果将`script`标签放在`body`标签前面，javascript的执行将会阻塞页面的渲染，所以通常将它放在页面的末尾。

# defer && async

defer属性会将JavaScript推迟到文档加载完毕后开始执行。如果有多个`script`脚本，原则上会按照顺序执行。
async属性是异步的意思，既不会阻塞文档的渲染，也不会影响其他的脚本加载，所以各个脚本不会顺序执行

# noscript

使用`<noscript>`标签，将在浏览器不支持脚本时渲染，展示其中的内容，即备胎，如果浏览器支持，则不显示。