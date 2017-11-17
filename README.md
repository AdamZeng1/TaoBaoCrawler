# TaoBaoCrawler
这是一个关于淘宝的爬虫程序。

现测试是可以使用的，非对单个信息进行爬取，而是只要是搜索框中输入的内容可以自主选择，在config.py文件中，更改KEYWORD中的内容到你想要爬取的词条就可以了。default为'美食'。

![image](http://oxufz8asv.bkt.clouddn.com/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-11-17%20%E4%B8%8B%E5%8D%883.26.46.png)

此次使用的Python发行版为anaconda，因为无法使用解析json的方式进行爬取，所以使用了Phamton(不可视浏览器)对内容进行渲染之后再爬取内容。如果对于Phamton不熟悉，可以换为Chrome，毕竟Phamton的文档阅读也是需要一定的时间成本的。

```python
spider.py

browser = webdriver.PhantomJS(service_args=SERVICE_ARGS)
#这是使用的Phamton的代码，下面更改为使用Chrome的代码

browser=wewebdriver.Chrome()
```

```python
config.py

SERVICE_ARGS=['--load-images=false','--disk-cache=true']
#该代码仍然可以保留
```



使用的工具有Selenium，Pymongo，pyquery。安装方式为命令行安装。