# 工单系统接口列表 
----------
 
## 注册接口

 - 地址：[/interface](/interface "注册接口")
 - 方式：POST 或 GET
 - 返回数据类型：json or jsonp
 - 描述：注册新用户
 - 传入参数： <table>
				<thead>
					<tr>
						<th>参数</th>
						<th>必填</th>
						<th>说明</th>
					</tr>
				</thead>
				<tbody>
					<tr>
						<td>act</td>
						<td>是</td>
						<td>regist</td>
					</tr>
					<tr>
						<td>name</td>
						<td>是</td>
						<td>用户名。用户名只能是字母数字下划线和小数点！</td>
					</tr>
					<tr>
						<td>p1</td>
						<td>是</td>
						<td>密码。密码长度在6~11之间，只能包含字符、数字和下划线</td>
					</tr>
					<tr>
						<td>nick</td>
						<td>是</td>
						<td>真实姓名。只能填写中文姓名</td>
					</tr>
					<tr>
						<td>phone</td>
						<td>是</td>
						<td>手机电话必须11位。</td>
					</tr>
					<tr>
						<td>mail</td>
						<td>是</td>
						<td>公司邮箱</td>
					</tr>
					<tr>
						<td>team</td>
						<td>是</td>
						<td>1:交互组，2：设计组，3：前端组，5：多app组</td>
					</tr>
					<tr>
						<td>sendMail</td>
						<td>是</td>
						<td>是否需要邮件提醒功能。0：不需要；1：需要</td>
					</tr>
					<tr>
						<td>ts</td>
						<td>是</td>
						<td>时间戳。传值+new Date()即可</td>
					</tr>
					<tr>
						<td>callback</td>
						<td>否</td>
						<td>jsonp</td>
					</tr>
				</tbody>
			</table>
 - 返回数据：<table>
				<thead>
					<tr>
						<th>参数</th>
						<th>说明</th>
					</tr>
				</thead>
				<tbody>
					<tr>
						<td>status</td>
						<td>0为失败，1为成功</td>
					</tr>
					<tr>
						<td>message</td>
						<td>错误提示</td>
					</tr>
				</tbody>
			</table>

## 登录接口
 - 地址：[/interface](/interface "注册接口")
 - 方式：POST 或 GET
 - 返回数据类型：json or jsonp
 - 描述：用户登录
 - 传入参数： <table>
				<thead>
					<tr>
						<th>参数</th>
						<th>必填</th>
						<th>说明</th>
					</tr>
				</thead>
				<tbody>
					<tr>
						<td>act</td>
						<td>是</td>
						<td>login</td>
					</tr>
					<tr>
						<td>username</td>
						<td>是</td>
						<td>用户名。</td>
					</tr>
					<tr>
						<td>password</td>
						<td>是</td>
						<td>密码。</td>
					</tr>
					<tr>
						<td>remark</td>
						<td>否</td>
						<td>是否需要记录登录状态。值为1则保存登录cookie，为0则不保存。</td>
					</tr>
					<tr>
						<td>ts</td>
						<td>是</td>
						<td>时间戳。传值+new Date()即可</td>
					</tr>
					<tr>
						<td>callback</td>
						<td>否</td>
						<td>jsonp</td>
					</tr>
				</tbody>
			</table>
 - 返回数据：<table>
				<thead>
					<tr>
						<th>参数</th>
						<th>说明</th>
					</tr>
				</thead>
				<tbody>
					<tr>
						<td>status</td>
						<td>0为失败，1为成功</td>
					</tr>
					<tr>
						<td>message</td>
						<td>错误提示</td>
					</tr>
				</tbody>
			</table>

## 登出接口

 - 地址：[/interface](/interface "注册接口")
 - 方式：POST 或 GET
 - 返回数据类型：json or jsonp
 - 描述：用户退出登录状态
 - 传入参数： <table>
				<thead>
					<tr>
						<th>参数</th>
						<th>必填</th>
						<th>说明</th>
					</tr>
				</thead>
				<tbody>
					<tr>
						<td>act</td>
						<td>是</td>
						<td>logout</td>
					</tr>
					<tr>
						<td>ts</td>
						<td>是</td>
						<td>时间戳。传值+new Date()即可</td>
					</tr>
					<tr>
						<td>callback</td>
						<td>否</td>
						<td>jsonp</td>
					</tr>
				</tbody>
			</table>
 - 返回数据：<table>
				<thead>
					<tr>
						<th>参数</th>
						<th>说明</th>
					</tr>
				</thead>
				<tbody>
					<tr>
						<td>status</td>
						<td>0为失败，1为成功</td>
					</tr>
					<tr>
						<td>message</td>
						<td>提示</td>
					</tr>
				</tbody>
			</table>

## 获取用户信息