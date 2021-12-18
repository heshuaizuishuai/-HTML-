# a 标签的用法
1. href 超链接：
    
   
 三种输入形式https：// http://   // 会自动选择http或https，不会出错 

  路径表示方法： 可以/a/b/c 也可以 a/b/c 

 伪协议javascript:;  可以做空的伪协议，作用是做一个什么都不执行的a标签


mailto:邮箱 发邮箱


tel:手机号 自动跳转到拨号页面

1. target 控制在哪个界面打开链接
   
  -blank在空白页面打开 

  -top在最顶层页面打开

  -parent在上一层页面打开

  -self在本层打开

  -xxx用同一个窗口打开

2. rel=noopener
   
   与target="_blank"相同，只不过使用target="_blank"时，如果打开新页面时需要执行复杂的JS，那页面性能可能会收到影响，为了避免这种情况，就可以使用rel=noopener

3. download  
   
下载这个网页（很多浏览器不支持，特别是手机浏览器）

# img 标签的用法
img作用发出get请求展示一张图片
1. alt 用于图片加载失败后，备注内容来提示用户
2. src 图片地址
3. hight/width高度宽度
只写宽度，高度会自适应；只写高度，宽度会自适应如果同时写宽和高，要保持图片的比例，不能让图片变形
4. onload/onerror
图片加载成功/失败
~~~
验证加载成不成功的代码
<script>
onload=function()[
    console.log("加载成功")
];
onerror=function()[
    console.log("加载失败");
xxx.src="/图片地址;"
];
</script>
~~~
5. 图片固定，方便在各种设备查看
```
<style>
img[max-width:100%]
<style>
```
# table 标签的用法
table标签里只能有thead、tbody 、tfoot 这三个标签，其中thead和tfoot可以没有
1. thead表格列头的行（加粗）
   
   th 表格中的表头单元格

   tr表格中的行 

   td包含数据的表格单元格

   tbody表格的主体 

   tfoot表格中各列的汇总行（尾）

2. table-layout:
   
   auto自动算法，每个单元格宽度取决于包含的内容

   fixed等宽

3. border-collapse 合并表格  默认是不合并的）
   
   border-spacing:0px  控制border之间的距离，一般改为0

# from 标签 
发get或post请求，然后刷新页面

action 控制请求到某个页面        

method 控制是get还是post来请求

autocomplete  on自动填充的建议或off不自动填充

target 告诉浏览器要提交到哪个页面/哪个页面需要刷新

from标签里要放一个type=submit才能触发submit事件

# input标签 
让用户输入内容

type=

txt                        文本

color                      颜色
password                   不展示输入的内容（让用户更加安全的输入密码）

radio                      单选（比如性别）让它们的radio拥有同一个name

checkbox                   多选，用同一个name分为一组（比如四个选项都是兴趣爱好）

file                       上传文件，同时上传多个文件  加multiple

hidden                     看不见的行

textarea                   输入多行文字，默认右下角可以拖动，可以用style="resize:none;"固定

select                     提供选项菜单的控件例如
~~~
<select>
<option value=''>-请选择-</option>
<option value='1'>-星期一-</option>
<option value='2'>-星期二-</option>
<select>
~~~