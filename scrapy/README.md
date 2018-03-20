# 大数据时代
## 数据获取的方式
- 企业生产的用户数据：大型互联网公司有海量用户，所以他们积累数据有天然的优势
- 有数意识的中小型企业，也开始积累的数据

## 数据管理咨询公司
- 公司偶很庞大的数据采集团队，通过市场调研、问卷调查、固定的样本检测
- 各行各业公司进行合作、专家对话（数据积累很多年，最后得出科研结果）来采集数据

## 政府/机构提供的公开数据
- 通过各地政府统计上报的数据进行合并；机构都是权威的第三方网站


## 第三方数据平台购买数据
- 通过各个数据交易平台购买各行各业需要的数据

## 爬虫爬去数据
- 市场没有数据，价格太高
- 爬虫工程师，在互联网上定向采集数据


- index.baidu.com
- alizs.taobao.com
- data.weibo.com/index
- index.baidu.com

# 什么是爬虫
> 抓取网页数据的程序

# 爬虫是怎么抓取网页数据
## 网页三大特征
- 每个网页都有自己的**URL**（统一资源定位符）来进行定位
- 网页使用 **HTML** 来描述页面信息
- 网页使用**HTTP/HTTPS协议**来传输HTML数据

## 爬虫的设计思路
1. 确定 URL 地址
2. 通过 http/https 协议获取对应 html 页面
3. 提取 html 页面里有用的数据
	+ 如果需要的，就保存
	+ 页面里的其他 URL, 那就继续执行第二步

# 为什么选择 Python 做爬虫
- 可以做爬虫的语言很多：PHP、Java、C/C++、Python等等
- PHP 不擅长多线程、异步网络支持不够，并发处理能力弱
- 爬虫对速度和效率要求比较高
- Java 的网络爬虫生态圈也很完善，是 Python 爬虫对手，但是Java 语言本身很笨重，代码量很大，重构成本比较高，任何修改都会导致代码的大量变动，爬虫经常需要修改部分采集代码
- C/C++ 运行效率和性能几乎最强，但是学习成本很高，代码成型比较慢。
- Python 语法优美、代码简洁、开发效率高、支持的模块，相关的HTTP请求的模块和html的解析模块非常丰富。强大的Scrapy，以及成熟高效的 Scrpy redis 分布式策略。调用其它接口方便（胶水语言）


1. 抓取 HTML 页面：HTTP 请求的处理：urllib、urllib2、requests
2. 处理后的请求可以模拟浏览器发送请求，后去服务器响应的文件
3. 解析服务器响应的内容：re、xpath、BeautifulSoup4(bs4)、jsonpath、pyquery 等

4. 采集动态HTML、验证码的处理
通用的动态页面采集：**Selenium**, **PhantomJS(无界面)**模拟真实浏览器加载js、ajax等非静态的数据

- Tesseract：机器学习库，机器图像识别系统： 

- 打码平台

5. Scrapy 框架（Scrapy, Pyspider）
- 高定制性高性能（异步网络框架twisted），数据下载速度非常快，提供数据存储、数据下载、提取规则等组件。

6. 分布式策略
- Scrapy redis, 在Scrapy的基础上添加了一套以Redis 数据库为核心的一套组件。支持分布式的共能，主要在Redis里做请求指纹去重、请求分配、数据临时存储。

7. 爬虫、反爬虫、反反爬虫 之间的斗争
- 爬虫做到最后，最头疼的不是复杂的页面，而是与反爬虫运维工程师的斗争

- User Agent、代理、验证码、动态数据加载、加密数据
- 数据价值：是否值得去费劲做发爬虫

1.机器成本：人力成本、数据价值、就不反了，一般做到封IP就结束了
2.面子战争

- 爬虫与反爬虫之间的斗争，最后一定是爬虫获胜。为什么？只要是真实用户可以浏览到网页数据，爬虫就一定能爬下来



