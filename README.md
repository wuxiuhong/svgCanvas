#SVG2Canvas Converter

#使用方式

##目录结构

```
src/
  --canvg-master/ -- canvg.js
  canvg2.js -- 修改生成的canvg.js
  insert.code.js -- 增加的扩展代码
  run.js -- node.js代码，使用 node run运行，生成canvg2.js
  run.sh -- 运行，生成canvg2.js
index.html -- SVG to Canvas 工具
```

##运行

请运行run.js或者run.sh，生成修改后的src/canvg21.js
```
cd src
node run
```
然后浏览器中访问index.html

### 使用生成的代码

将右侧文本框中的代码保存到js文件（比如SVGIcons.js），并在HTML中引入这个js，之后你就可以直接使用svg文件名作为节点图标了
<pre class="prettyprint">node.image = 'DataCenter.svg';
</pre>
示例代码
<pre class="prettyprint">&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;Hello Qunee for HTML5&lt;/title&gt;
&lt;meta charset="utf-8"&gt;
&lt;/head&gt;
&lt;body style="margin: 0px"&gt;
&lt;div style="position: absolute; width: 100%; top: 0px; bottom: 0px;" id="canvas"&gt;&lt;/div&gt;
&lt;script src="http://demo.qunee.com/lib/qunee-min.js"&gt;&lt;/script&gt;
&lt;script src="SVGIcons.js"&gt;&lt;/script&gt;
&lt;script&gt;
var graph = new Q.Graph('canvas');

var node = graph.createNode("SVG");
node.image = 'DataCenter.svg';

&lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
**运行效果**

![hello svg](http://blog.qunee.com/wp-content/uploads/2015/04/Screen-Shot-2015-04-30-at-5.35.31-PM.png)