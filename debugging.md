#Lua——调试（Debugging）  

Lua 提供一个调试库，这个库中提供了创建自己的调试器所需的所有原语函数。虽然，Lua 没有内置调试器，但是开发者们为 Lua 开发了许多的开源调试器。  
Lua 调试库包括的函数如下表所示。  
<table>
	<tr>
		<th>S.N.</th>
		<th>方法和描述</th>
	</tr>
	<tr>
		<td>1</td>
		<td>debug():进入交互式调试模式，在此模式下用户可以用其它函数查看变量的值。</td>
	</tr>
		<tr>
		<td>2</td>
		<td>getfenv(object):返回对象的环境。</td>
	</tr>
		<tr>
		<td>3</td>
		<td>gethook(optional thread)：返回线程当前的钩子设置，总共三个值：当前钩子函数、当前的钩子掩码与当前的钩子计数。</td>
	</tr>
		<tr>
		<td>4</td>
		<td>getinfo(optional thread,function or stack leve,optional flag)：返回保存函数信息的一个表。你也可以直接给指定函数，或者你也</td>
	</tr>

</table>
