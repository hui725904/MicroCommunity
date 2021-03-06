

**1\. 刷新缓存**
###### 接口功能
> 开发人员通过手工调用接口 刷新缓存

###### URL
> [http://api.java110.com:8008/api/flush.center.cache](http://api.java110.com:8008/api/flush.center.cache)

###### 支持格式
> JSON

###### HTTP请求方式
> GET

###### 请求参数(header部分)
|参数名称|约束|类型|长度|描述|取值说明|
| :-: | :-: | :-: | :-: | :-: | :-:|
|app_id|1|String|30|应用ID|Api服务分配                      |
|transaction_id|1|String|30|请求流水号|不能重复 1000000000+YYYYMMDDhhmmss+6位序列 |
|sign|1|String|-|签名|请参考签名说明|
|req_time|1|String|-|请求时间|YYYYMMDDhhmmss|

###### 请求参数
|参数名称|约束|类型|长度|描述|取值说明|
| :-: | :-: | :-: | :-: | :-: | :-: |
|cache|1|String|4|缓存类型|ALL代表所有|

###### 返回协议

当http返回状态不为200 时请求处理失败 body内容为失败的原因

当http返回状态为200时请求处理成功，body内容为返回内容，

刷新缓存成功


###### 举例
> 地址：[http://api.java110.com:8008/api/flush.center.cache?cache=All](http://api.java110.com:8008/api/flush.center.cache?cache=All)

``` javascript
请求头信息：
Content-Type:application/json
USER_ID:1234
APP_ID:8000418002
TRANSACTION_ID:10029082726
REQ_TIME:20181113225612
SIGN:aabdncdhdbd878sbdudn898
请求报文：

无

返回报文：
刷新缓存成功

```
