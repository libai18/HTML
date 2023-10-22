  **HTML基础速通**

- HTML 超文本标记语言——HyperText Markup Language。
- 注释 ：在 VS Code 中，添加 / 删除注释的快捷键：**Ctrl + / 。**	` <!--你好 世界-->`

- HTML 基本骨架：VS Code 快速生成骨架：**! + Enter / Tab 键**

- 标题标签：h1 ~ h6（双标签）   `  <h1>你好 世界</h1>`

- 段落标签：p（双标签）   ` <p>你好 世界</p>`

- 换行（单标签）：`<br>`

- 水平线（单标签）`<hr>`
- 文本格式化标签	 
	- ` <strong>你好 世界</strng>`	`  <b>b 加粗</b>`
	- `  <em>你好 世界</em>`                      `  <i>i 倾斜</i>`
	- ` <ins>你好 世界</ins>`	       `  <u>u 下划线</u>`
	- `  <del>你好 世界</del>`               `  <s>s 删除线</s>`


-  图像标签

	- 当图片无法显示时，alt 属性会显示一段文本来替代图片。     `<img src="./cat1.jpg" alt="这是一只猫">`
	- 鼠标悬停在图片上时显示一段文本。      `<img src="./dog.jpg" title="这是一只狗">`

	- 浏览器缩放图片，默认是等比例缩放。      `<img src="./cat.jpg" width="100">`或 `height="600"`

- **Windows 默认是 \ ，其他系统是 /，建议统一写为 /** 

- 路径分类
	- 相对路径：从当前文件位置出发查找目标文件。`<img src="./images/2.gif">`   `<img src="../3.jpg">`
	- 绝对路径：从盘符出发查找目标文件。


- 超链接        `<a href="https://www.baidu.com/">跳转到百度</a>`
	- 不确定跳转地址，则 href 属性值写为 #，表示空链接        `<a href="#">空链接</a>`
	- 超链接默认是在当前窗口跳转页面，添加 target="_blank" 实现新窗口打开页面。     `target="_blank"`

- 音频标签       `<audio src="./music.mp3" controls loop autoplay></audio>`

- **书写 HTML5 属性时，如果属性名和属性值相同，可以简写为一个单词**

- 视频标签       `<video src="./vue.mp4" controls loop muted autoplay></video>`

- 列表

	- ul 是无序列表	`  <ul>    <li>1</li> <li>2</li>    </ul>`

	- ol 是有序列表        `  <ol>    <li>1</li> <li>2</li>    </ol>`

	- dl 是定义列表，dt 是定义列表的标题，dd 是定义列表的描述 / 详情。

		`  <dl>	<dt>服务中心</dt>    <dd>申请售后</dd>	<dd>售后政策</dd>     </dl>`

- 表格`<table> <tr> <td>1</td> <td>1</td>  </tr> </table>`

	- 在网页中，表格默认没有边框线，使用 border 属性可以为表格添加边框线

		```html
		<table border="1">
		    <thead>
		      <tr>	<th>姓名</th><th>语文</th><th>数学</th>   <th>总分</th>	</tr>
		    </thead>
		    
		    <tbody>
		      <tr>	<td>张三</td><td>99 </td><td>90</td>	  <td>199</td>	</tr>
		      <tr>	<td>李四</td><td>98 </td><td>90</td>	  <td>198</td>	</tr>
		    </tbody>
		    
		    <tfoot>
		      <tr>	<td>总结</td><td>第一</td><td>第一</td>  <td>第一</td>	</tr>
		    </tfoot>
		</table>
		```

	- 表格结构标签

		thead表格头部–表格头部内容
		tbody表格主体–主要内容区域
		tfoot表格底部–汇总信息区域
		**表格结构标签可以省略**

	- 合并单元格

		- **rowspan跨行合并**   ` <td rowspan="2">90</td>`用于指定该单元格要跨越的行数为2。

		- **colspan跨列合并**    `<td colspan="3">第一</td>`指定了这个单元格要跨越3列的宽度。


- input 标签基本使用, type 属性值不同，则功能不同。

	- 文本框：`<input type="text">`，用于接收用户输入的文本。**输入什么就显示什么**

	- 密码框：`<input type="password">`，用于接收用户输入的密码，输入的内容会被隐藏。**以 点 的形式显示**。
		- **placeholder占位文本**：提示信息。`  文本框：<input type="text" placeholder="请输入用户名">`

	- 单选按钮：`<input type="radio">`，用于让用户在一组选项中选择一个选项。

		- checked单选按钮默认被选中。name 指定了这个单选按钮的名，进行分组。

			```html
			性别：<input type="radio" name="gender"> 男
			     <input type="radio" name="gender" checked> 女
			```

	- 复选框：`<input type="checkbox">`，用于让用户选择一个或多个选项。

		- ```html
			兴趣爱好：
			<input type="checkbox"> 敲代码
			<input type="checkbox" checked> 敲前端代码
			<input type="checkbox" checked> 敲前端 HTML 代码
			```

	- 提交按钮：`<input type="submit">`，用于提交表单数据到服务器进行处理。
	- 重置按钮：`<input type="reset">`，用于重置表单中的输入内容。

	- 文件上传：`<input type="file"  multipl>`，用于让用户选择上传文件。multiple 可以实现文件多选功能。

-  下拉菜单   

	- selected 默认选中功能

	`  <select> <option>深圳</option> <option selected>武汉</option>  </select>`

- 文本域,多行输入文本的表单控件 。`  <textarea>请输入评论</textarea>`

- 标签

	- 网页中，某个**标签的说明文本**

		```html
		    <label>姓名：</label><input type="text" placeholder="请输入真实姓名">
		    <label>密码：</label><input type="password" placeholder="请输入密码">
		    <label>确认密码：</label><input type="password" placeholder="请输入确认密码">
		    <label>性别：</label>
		    <label><input type="radio" name="gender"> 男</label>
		    <label><input type="radio" name="gender" checked> 女</label>
		```

	- 用 label 标签绑定文字和表单控件的关系，**增大表单控件的点击范围**。

		- 写法一

			label 标签只包裹内容，不包裹表单控件。设置 label 标签的 for 属性值 和表单控件的 id 属性值相同。

			```html
			性别：<input type="radio" name="gender" id="man"> <label for="man">男</label>
			```

		- 写法二

			使用 label 标签包裹文字和表单控件，不需要属性

			```html
				<label><input type="radio"> 女</label>
			```


- 按钮

	-  submit提交按钮，点击后可以提交数据到后台 (默认功能)

	- reset重置按钮，点击后将表单控件恢复默认值

	- button普通按钮，默认没有功能，一般配合JavaScript 使用

```html
  <form action="">
    用户名：<input type="text">
    密码：<input type="password">
    <!-- 如果省略 type 属性，功能是 提交 -->
    <button type="submit">提交</button>
    <button type="reset">重置</button>
    <button type="button">普通按钮</button>
  </form>
注意：按钮需配合 form 标签（表单区域）才能实现对应的功能。
```

- 布局标签

	- div：独占一行  	`<div>div 标签，独占一行</div>`

	- span：不换行 	 `<span>span 标签，不换行</span>`

- 字符实体

	- 空格`&nbsp;`

	- 小于号`&lt;`

	- 大于号`&gt;`

