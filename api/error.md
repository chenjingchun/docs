# 错误代码

响应是你从REST API返回的数据，响应可以返回所需的数据，也可以用来返回错误。

REST API使用响应代码（Response Code）来代表不同的状态，返回正确的响应代码为200，返回错误的响应代码及意义如下：

Code  | 类型  | 说明
------  | ------  | ------
400 | Bad request | 参数不正确或其他原因导致的请求错误。
401 | Unauthorized | 请求认证失败，可能是 Access Token 丢失、无效或没有权限。
404 | Not found | 未找到所请求的资源。如果URL完全无效(例如/api/v1/asdf)，或者它是一个可能有效的URL，但是引用了不存在的东西(例如/api/v1/site?siteId=12345)，则返回该响应。
429 | Too Many Requests | 如果为 Access Token 启用了速率限制，则此返回代码表示已到达速率限制，且未处理该请求。