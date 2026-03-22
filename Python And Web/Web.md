# Web基本技术要素

* HTML  --> 定义网页结构与信息

* CSS   --> 定义网页样式

* JaveScript --> 定义用户与网页的交互逻辑

---

# **HTML**

[点此查看代码示例](<test case/Html_test.html>)

* *一个最简单的html如下*
     ```html
    <!DOCTYPE HTML>  //告知浏览器文件类型为html
    <html>           //起始标签，表示开始，是文档的根
        <body>            //表示文档的主题内容
        <h1>这是一个标题</h1>     //h1表示1级标题，是body的子元素
        <p>这是一段文字</p>       //p表示文本段落，是body的子元素
    </html>          //闭合标签，表示结束，两个标签连同中间的所有内容视作一个html元素
    ```
    ## 常用标签
  
    1. **标题标签** ```<h数字> </h数字>```  ，数字越小，标题层级越大
        ```html
        <h1>一级标题</h1>
        <h2>二级标题</h2>
        ......
        ```
    
    2. **文本标签** ```<p> </p>``` 
    
       **换行标签** ```<br>```      

       **粗体标签** ```<b> </b>``` 

       **斜体标签** ```<i> </i>``` 

       **下划线标签** ```<u> </u>``` 

        ```html
        <p>第一行文本内容</p>
        <p> 第二行文本内容<br>第三行文本内容</p>
        <p><b>粗体</b><i>斜体</i><u>加下划线</u></p>
        ```

    3.  **图片标签** ```<img  属性1=""  属性2=""  ...>``` 

        * 必要属性： ```<img src="图片路径">``` 指定图片来源的链接或路径

        * 其他属性： ```width=""``` ```height=""``` 等

    4. **链接标签** ```<a  href="链接"  target="..."> <\a>``` 

        * ```herf``` 属性：必要属性，值为目标要跳转的URL地址

        * ```target``` 属性：可填可不填，默认为```target="_self"```直接在当前窗口跳转链接，也可设置为```target="_blank"```在新窗口打开

    5.  **容器标签**

        ```<div> </div>     //块级元素独占一块，每行最多一个```

        ```<span> </span>   //内联元素，一行可以有多个 ```

        本身不包含内容，可将其他元素包含在两个标签中，作为子元素，再对容器进行统一的操作（如更换颜色） 

        ```html
        <a href="https://baidu.com">
            一个带有<span style="background-color:red;">红字</span>和<span style="background-color:blue;">蓝字</span>的链接
        </a>
        ```
        ```html
        <a href="https://baidu.com">
            一个带有<div style="background-color:red;">红字且独占一行</div>和<div style="background-color:blue;">蓝字且独占一行</div>的链接
        </a>
        ```

    6.  **列表标签** 

        ```<ol> </ol>``` **有序列表标签** (Ordered List)

        ```<ul> </ul>``` **无序列表标签** (Unordered List)
        
        * ```<li></li>``` **列表元素标签** (List Item) 列表里的每项元素都要加上该标签
    
        ```html
        <ol>
            <li>第一项</li> //1.第一项
            <li>第二项</li> //2.第二项
            <li>第三项</li> //3.第三项
        </ol>
        ```

    7. **表格标签**

        ```<table> </table>``` 用于定义表格，内部嵌套表格相关元素 ( 可加入```border=""```属性来实现表格边框)

          * ```<thead> </thead>``` 表示表格头部

          * ```<tbody> <tbody>``` 表示表格主体

            * ```<tr> </tr>``` 定义表格行(table row)
        
                * ```<td> </td>``` 表示每项数据(table data)
    
        ```html
        <table border="1">
            <thead>
                <tr>
                    <td>表头1</td>
                    <td>表头2</td>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>第一行第一个</td>
                    <td>第一行第二个</td>
                </tr>
                <tr>
                    <td>第二行第一个</td>
                    <td>第二行第二个</td>
                </tr>
            </tbody>
        </table>
        ``` 

    8. **类属性** ```<标签 class="">``` 
    
        可运用于所有元素上，定义元素的类的名称，从而帮助分组

        ```html
        <p class="context">文章1</p>
        <p class="context">文章2</p>
        <p class="review">评论1</p>
        ```
