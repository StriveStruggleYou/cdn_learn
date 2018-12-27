# cdn_learn
CDN_书籍阅读笔记

### 从零开始实现一个cdn

1. 智能dns服务器，一个可以根据客户端ip请求，转发到最近的服务器中。</br>
  1.1 dns服务器，根据dns 协议，实现一个dns 服务器。</br>
  1.2 ip到物理地址转换的实现。</br>
  1.3 保障dns服务器的高可用，udp负载均衡。</br>

2. web proxy cache,一个如果静态文件存在，就直接返回，不存在，就转发到实际原站。</br>
  2.1 openresty 进行proxy cache </br>
    2.1.1 为每个域名单独的cache 文件目录</br>
  	2.1.2 如何进行数据统计需要思考一下</br>
  2.2 拉取源站未缓存的文件。</br>
    2.2.1 对文件后缀需要做一些限制,尽量只缓存小文件信息。</br>
    2.2.2 对文件类型要加上缓存时间，和主动失效。</br>
    2.2.3 webmagic 用爬虫来进行文件下载。</br> 
  2.3 定期删除无效的cdn文件信息</br>