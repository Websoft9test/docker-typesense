## Typesense

[Typesense](https://typesense.org/)是一款开源搜索工具，是Algolia 或者大型搜索ElasticSearch 的替代方案

## 容器介绍

本项目涉及到两个容器typesense和typesense-scraper


## typesense容器

是数据容器，搜索的文件源，相当于数据服务器。
通过 URL 访问：http://IP:9001/health，如返回 OK 证明容器正常启动。

## typesense-scraper容器

typesense-scraper容器是一个搜集器（爬虫容器），将目标网站的数据搜集到typesenses数据服务器，即上文的typesense容器。它通过IP，端口以及API_KEY等连接下游server服务器;它连接用户网站是通过一个标准格式的json文件，目前我们是采用的https://developer.4d.com为范例，更多文件格式学习请参照[docsearch-configs](https://github.com/algolia/docsearch-configs)
