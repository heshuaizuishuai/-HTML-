# a 标签的用法
1. href 
* 超链接 三种输入形式https：// http:// // 
* 路径表示方法 可以/a/b/c 也可以 a/b/c 
* 三种伪协议javascript:; mailto:邮箱 tel:手机号
2. target
* -blank在空白页面打开 
* -top在最高级页面打开
* -parent在上一层页面打开
* -self在本层打开
* -xxx用同一个窗口打开
3. rel=noopener
# img 标签的用法
img作用发出get请求展示一张图片
1. alt 加载失败显示的图片
2. src 图片地址
   
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
3. 在手机上展示的代码
   
```
<style>
img[max-width:100%]
<style>
```
# table 标签的用法
1. thead顶行 th标头
tr一行 td数据
tbody内容 tfoot尾
2. table-layout:auto根据内容的宽度内容越长表格越长，fixed表格全部等宽
3. border-collapse 合并表格  
   border-spacing:0px  设置表格边距大小
其他感想
from标签里要放一个type=submit才能触发submit事件