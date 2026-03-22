# <span style="color:red;">爬虫</span>
```import requests```

 [***点此查看代码示例文件***](<test case/Scrape.py>)
    
1.  **使用```requests.get("链接")```返回得到该链接URL的参数**
    
    ```python
    response=requests.get("...")    //将该链接的参数存在该类的实例中
    ``` 

2. **使用 ```print(response)``` 或 ```print(response.status_code)``` 获得状态码**

    **使用 ```response.ok``` 来判断请求是否成功，成功则返回 ```true```**

    *关于http响应状态码详情请看 [这里](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Reference/Status)*

3. **使用 ```response.text``` 获得网页源码**

4. **通过对 ```requests.get()``` 传入```headers``` 参数更改传入信息**
    ```py
    head={"User-Agent":"用户参数"}
    response=requests.get("链接",headers=head)
    ```
