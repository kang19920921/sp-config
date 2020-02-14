
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <link rel="canonical" href="https://blog.csdn.net/weixin_38305440/article/details/102810522"/>
    <meta http-equiv="content-type" content="text/html; charset=utf-8">
    <meta name="renderer" content="webkit"/>
    <meta name="force-rendering" content="webkit"/>
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1"/>
    <meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta name="apple-mobile-web-app-status-bar-style" content="black">
    <meta name="report" content='{"pid":"blog"}'>
    <meta name="referrer" content="always">
    <meta http-equiv="Cache-Control" content="no-siteapp" /><link rel="alternate" media="handheld" href="#" />
    <meta name="shenma-site-verification" content="5a59773ab8077d4a62bf469ab966a63b_1497598848">
        <meta name="csdn-baidu-search"  content='{"autorun":true,"install":true,"keyword":"RabbitMQ_大数据_weixin_38305440的博客-CSDN博客"}'>
    
    <link href="https://csdnimg.cn/public/favicon.ico" rel="SHORTCUT ICON">
    <title>RabbitMQ_大数据_weixin_38305440的博客-CSDN博客</title>
    <meta name="description" content="文章目录RabbitMQ 使用场景服务解耦流量削峰异步调用rabbitmq 基本概念Exchange大数据">
    <script src='//g.csdnimg.cn/tingyun/1.8.3/blog.js' type='text/javascript'></script>
        
                    <link rel="stylesheet" href="https://csdnimg.cn/release/phoenix/template/css/detail-afd5e40070.min.css">
                            <script type="application/ld+json">{"@context":"https:\/\/ziyuan.baidu.com\/contexts\/cambrian.jsonld","@id":"https:\/\/blog.csdn.net\/weixin_38305440\/article\/details\/102810522","appid":1638831770136827,"title":"RabbitMQ_\u5927\u6570\u636e_weixin_38305440\u7684\u535a\u5ba2-CSDN\u535a\u5ba2","pubDate":"2019-10-29T23:14:20","upDate":"2019-10-31T21:39:32"}</script>
    
            <link rel="stylesheet" href="https://csdnimg.cn/release/phoenix/themes/skin-sea/skin-sea-1da92177b4.min.css">
    
<!--    自定义皮肤样式-->
    
    <script type="text/javascript">
        var username = "weixin_38305440";
        var blog_address = "https://blog.csdn.net/weixin_38305440";
        var static_host = "https://csdnimg.cn/release/phoenix/";
        var currentUserName = "k826240369";
        var isShowAds = true;
        var isOwner = false;
        var loginUrl = "http://passport.csdn.net/account/login?from=https://blog.csdn.net/weixin_38305440/article/details/102810522"
        var blogUrl = "https://blog.csdn.net/";

        var curSkin = "skin-sea";
        // 收藏所需数据
        var articleTitle = "RabbitMQ";
        var articleDesc = "文章目录RabbitMQ 使用场景服务解耦流量削峰异步调用rabbitmq 基本概念Exchange大数据";

        var articleTitles = "RabbitMQ_大数据_weixin_38305440的博客-CSDN博客";
        
        var nickName = "Wanght6";
        var isCorporate = false;
        var subDomainBlogUrl = "https://blog.csdn.net/"
        var digg_base_url = "https://blog.csdn.net/weixin_38305440";
        var articleDetailUrl = "https://blog.csdn.net/weixin_38305440/article/details/102810522";
        var isShowThird = "0"
    </script>
    <script src="https://csdnimg.cn/public/common/libs/jquery/jquery-1.9.1.min.js" type="text/javascript"></script>
    <!--js引用-->
            <script src="//g.csdnimg.cn/??fixed-sidebar/1.1.6/fixed-sidebar.js,report/1.4.1/report.js" type="text/javascript"></script>
    <link rel="stylesheet" href="https://csdnimg.cn/public/sandalstrap/1.4/css/sandalstrap.min.css">
    <style>
        .MathJax, .MathJax_Message, .MathJax_Preview{
            display: none
        }
    </style>
</head>
<body class="nodata " > 
    <link rel="stylesheet" href="https://csdnimg.cn/public/common/toolbar/content_toolbar_css/content_toolbar.css">
    <script id="toolbar-tpl-scriptId" src="https://csdnimg.cn/public/common/toolbar/js/content_toolbar.js" type="text/javascript" domain="https://blog.csdn.net/"></script>
    <script>
    (function(){
        var bp = document.createElement('script');
        var curProtocol = window.location.protocol.split(':')[0];
        if (curProtocol === 'https') {
            bp.src = 'https://zz.bdstatic.com/linksubmit/push.js';
        }
        else {
            bp.src = 'http://push.zhanzhang.baidu.com/push.js';
        }
        var s = document.getElementsByTagName("script")[0];
        s.parentNode.insertBefore(bp, s);
    })();
</script>
<link rel="stylesheet" href="https://csdnimg.cn/release/phoenix/template/css/blog_code-c3a0c33d5c.css">
<link rel="stylesheet" href="https://csdnimg.cn/release/phoenix/vendor/pagination/paging-e040f0c7c8.css">

<script type="text/javascript">
	var NEWS_FEED = function(){}
</script>

<link rel="stylesheet" href="https://csdnimg.cn/release/phoenix/template/css/chart-3456820cac.css" />
<div class="main_father clearfix d-flex justify-content-center" style="height:100%;"> 
    <div class="container clearfix" id="mainBox">
        <div  class='space_container'></div>
        <main>
            <div class="blog-content-box">
    <div class="article-header-box">
        <div class="article-header">
            <div class="article-title-box">
                <h1 class="title-article">RabbitMQ</h1>
            </div>
            <div class="article-info-box">
                <div class="article-bar-top">
                    <!--文章类型-->
                    <span class="article-type type-1 float-left">原创</span>                                            <span class="c-gray">置顶</span>
                                                                                                                                            <a class="follow-nickName" href="https://me.csdn.net/weixin_38305440" target="_blank" rel="noopener">Wanght6</a>
                    <span class="time">最后发布于2019-10-31 21:39:32                    </span>
                    <span class="read-count">阅读数 8450</span>
                    <a id='blog_detail_zk_collection' data-report-click='{"mod":"popu_823"}'>
                        <svg class="icon">
                            <use xlink:href="#icon-csdnc-Collection-G" ></use>
                        </svg>
                        收藏
                    </a>
                </div>
                                <div class="up-time">发布于2019-10-29 23:14:20</div>
                <div class="slide-content-box">
                                                        <div class="tags-box artic-tag-box">
                           <span class="label">分类专栏：</span>
                                                                                             <a class="tag-link" target="_blank" rel="noopener"
                                      href="https://blog.csdn.net/weixin_38305440/category_9475453.html">
                                       RabbitMQ                                   </a>
                                                                                  </div>
                                                                                           <div class="tags-box artic-tag-box">
                                <span class="label">文章标签：</span>
                                                                <a data-report-click='{"mod":"popu_626","strategy":"RabbitMQ"}' data-report-view='{"mod":"popu_626","strategy":"RabbitMQ"}' class="tag-link" href="https://so.csdn.net/so/search/s.do?q=RabbitMQ&t=blog" target="_blank" rel="noopener">RabbitMQ                                                                    <a data-report-click='{"mod":"popu_626","strategy":"Rabbit"}' data-report-view='{"mod":"popu_626","strategy":"Rabbit"}' class="tag-link" href="https://so.csdn.net/so/search/s.do?q=Rabbit&t=blog" target="_blank" rel="noopener">Rabbit                                                                    <a data-report-click='{"mod":"popu_626","strategy":"MQ"}' data-report-view='{"mod":"popu_626","strategy":"MQ"}' class="tag-link" href="https://so.csdn.net/so/search/s.do?q=MQ&t=blog" target="_blank" rel="noopener">MQ                                                                    <a data-report-click='{"mod":"popu_626","strategy":"消息队列"}' data-report-view='{"mod":"popu_626","strategy":"消息队列"}' class="tag-link" href="https://so.csdn.net/so/search/s.do?q=消息队列&t=blog" target="_blank" rel="noopener">消息队列                                                                    <a data-report-click='{"mod":"popu_626","strategy":"流量削峰"}' data-report-view='{"mod":"popu_626","strategy":"流量削峰"}' class="tag-link" href="https://so.csdn.net/so/search/s.do?q=流量削峰&t=blog" target="_blank" rel="noopener">流量削峰                                                                    </a>
                            </div>
                                                                                                                <div class="article-copyright">
                        <span class="creativecommons">
                            <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"></a>
                            <span>
                                版权声明：本文为博主原创文章，遵循<a href="http://creativecommons.org/licenses/by-sa/4.0/" target="_blank" rel="noopener"> CC 4.0 BY-SA </a>版权协议，转载请附上原文出处链接和本声明。                            </span>
                            <div class="article-source-link2222">
                                本文链接：<a href="https://blog.csdn.net/weixin_38305440/article/details/102810522">https://blog.csdn.net/weixin_38305440/article/details/102810522</a>
                            </div>
                        </span> 
                        </div>
                                                                                </div>
                <div class="operating">
                                                                <a class="href-article-edit slide-toggle">展开</a>
                                    </div>
            </div>
        </div>
    </div>
    <article class="baidu_pl">
        <!--python安装手册开始-->
                <!--python安装手册结束-->
                <!--####专栏广告位图文切换开始-->
                                    <!--####专栏广告位图文切换结束-->
         <div id="article_content" class="article_content clearfix">
            <link rel="stylesheet" href="https://csdnimg.cn/release/phoenix/template/css/ck_htmledit_views-833878f763.css" />
                                        <div id="content_views" class="markdown_views prism-atom-one-dark">
                    <!-- flowchart 箭头图标 勿删 -->
                    <svg xmlns="http://www.w3.org/2000/svg" style="display: none;">
                        <path stroke-linecap="round" d="M5,0 0,2.5 5,5z" id="raphael-marker-block" style="-webkit-tap-highlight-color: rgba(0, 0, 0, 0);"></path>
                    </svg>
                                            <p></p><div class="toc"><h3>文章目录</h3><ul><li><a href="#RabbitMQ__1" rel="nofollow">RabbitMQ 使用场景</a></li><ul><li><a href="#_3" rel="nofollow">服务解耦</a></li><li><a href="#_19" rel="nofollow">流量削峰</a></li><li><a href="#_37" rel="nofollow">异步调用</a></li></ul><li><a href="#rabbitmq__57" rel="nofollow">rabbitmq 基本概念</a></li><ul><li><a href="#Exchange_64" rel="nofollow">Exchange</a></li><li><a href="#Message_Queue_70" rel="nofollow">Message Queue</a></li><li><a href="#Binding_Key_74" rel="nofollow">Binding Key</a></li><li><a href="#Routing_Key_78" rel="nofollow">Routing Key</a></li></ul><li><a href="#rabbitmq_82" rel="nofollow">rabbitmq安装</a></li><ul><li><a href="#erlang_86" rel="nofollow">安装erlang语言库</a></li><ul><li><a href="#rabbitmqErlang_90" rel="nofollow">rabbitmq官方精简的Erlang语言包</a></li><li><a href="#_99" rel="nofollow">下载和安装</a></li></ul><li><a href="#socat_109" rel="nofollow">安装socat依赖</a></li><ul><li><a href="#socat_111" rel="nofollow">socat依赖包</a></li><li><a href="#_121" rel="nofollow">下载和安装</a></li></ul><li><a href="#rabbitmq_131" rel="nofollow">安装rabbitmq</a></li><ul><li><a href="#rabbitmq_133" rel="nofollow">rabbitmq安装包</a></li><li><a href="#_139" rel="nofollow">下载和安装</a></li></ul><li><a href="#rabbitmq_150" rel="nofollow">rabbitmq启动和停止命令</a></li><li><a href="#rabbitmq_163" rel="nofollow">rabbitmq管理界面</a></li><ul><li><a href="#_165" rel="nofollow">启用管理界面</a></li><li><a href="#_176" rel="nofollow">访问</a></li></ul><li><a href="#_184" rel="nofollow">添加用户</a></li><ul><li><a href="#_186" rel="nofollow">添加用户</a></li><li><a href="#_196" rel="nofollow">设置访问权限</a></li></ul><li><a href="#_204" rel="nofollow">开放客户端连接端口</a></li></ul><li><a href="#rabbitmq_219" rel="nofollow">rabbitmq六种工作模式</a></li><ul><li><a href="#_221" rel="nofollow">简单模式</a></li><ul><li><a href="#pomxml_232" rel="nofollow">pom.xml</a></li><li><a href="#_279" rel="nofollow">生产者发送消息</a></li><li><a href="#_339" rel="nofollow">消费者接收消息</a></li></ul><li><a href="#_390" rel="nofollow">工作模式</a></li><ul><li><a href="#_400" rel="nofollow">生产者发送消息</a></li><li><a href="#_444" rel="nofollow">消费者接收消息</a></li><li><a href="#_502" rel="nofollow">运行测试</a></li><li><a href="#_515" rel="nofollow">消息确认</a></li><li><a href="#_618" rel="nofollow">消息持久化</a></li><li><a href="#_648" rel="nofollow">合理地分发</a></li><li><a href="#_658" rel="nofollow">生产者代码</a></li><li><a href="#_701" rel="nofollow">消费者代码</a></li></ul><li><a href="#_766" rel="nofollow">发布订阅模式</a></li><ul><li><a href="#Exchanges__778" rel="nofollow">Exchanges 交换机</a></li><li><a href="#_Bindings_800" rel="nofollow">绑定 Bindings</a></li><li><a href="#_818" rel="nofollow">完成的代码</a></li><ul><li><a href="#_822" rel="nofollow">生产者</a></li><li><a href="#_872" rel="nofollow">消费者</a></li></ul></ul><li><a href="#_933" rel="nofollow">路由模式</a></li><ul><li><a href="#_Bindings_941" rel="nofollow">绑定 Bindings</a></li><li><a href="#_Direct_exchange_958" rel="nofollow">直连交换机 Direct exchange</a></li><li><a href="#_Multiple_bindings_972" rel="nofollow">多重绑定 Multiple bindings</a></li><li><a href="#_978" rel="nofollow">发送日志</a></li><li><a href="#_1000" rel="nofollow">订阅</a></li><li><a href="#_1009" rel="nofollow">完整的代码</a></li><ul><li><a href="#_1013" rel="nofollow">生产者</a></li><li><a href="#_1068" rel="nofollow">消费者</a></li></ul></ul><li><a href="#_1133" rel="nofollow">主题模式</a></li><ul><li><a href="#_Topic_exchange_1145" rel="nofollow">主题交换机 Topic exchange</a></li><li><a href="#_1171" rel="nofollow">完成的代码</a></li><ul><li><a href="#_1173" rel="nofollow">生产者</a></li><li><a href="#_1224" rel="nofollow">消费者</a></li></ul></ul><li><a href="#RPC_1301" rel="nofollow">RPC模式</a></li><ul><li><a href="#_1307" rel="nofollow">客户端</a></li><li><a href="#_Callback_Queue_1317" rel="nofollow">回调队列 Callback Queue</a></li><li><a href="#id_correlationId_1347" rel="nofollow">关联id (correlationId)：</a></li><li><a href="#_1353" rel="nofollow">小结</a></li><li><a href="#_1364" rel="nofollow">完成的代码</a></li><ul><li><a href="#_1366" rel="nofollow">服务器端</a></li><li><a href="#_1459" rel="nofollow">客户端</a></li></ul></ul></ul><li><a href="#virtual_host_1548" rel="nofollow">virtual host</a></li><ul><li><a href="#virtual_host_pd_1552" rel="nofollow">创建virtual host: `/pd`</a></li><li><a href="#_1567" rel="nofollow">设置虚拟机的用户访问权限</a></li></ul><li><a href="#_rabbitmq_1573" rel="nofollow">拼多商城整合 rabbitmq</a></li><ul><li><a href="#_1583" rel="nofollow">订单存储的解耦</a></li><li><a href="#_1591" rel="nofollow">生产者-发送订单</a></li><ul><li><a href="#pomxml__1593" rel="nofollow">pom.xml 添加依赖</a></li><li><a href="#applicationyml_1604" rel="nofollow">application.yml</a></li><li><a href="#_RunPdAPP_1619" rel="nofollow">修改主程序 RunPdAPP</a></li><li><a href="#_OrderServiceImpl_1633" rel="nofollow">修改 OrderServiceImpl</a></li></ul><li><a href="#_1684" rel="nofollow">消费者-接收订单,并保存到数据库</a></li><ul><li><a href="#pdwebpdorderconsumer_1686" rel="nofollow">pd-web项目复制为pd-order-consumer</a></li><li><a href="#_applicationyml_1690" rel="nofollow">修改 application.yml</a></li><li><a href="#_1722" rel="nofollow">删除无关代码</a></li><li><a href="#_OrderConsumer_1730" rel="nofollow">新建 OrderConsumer</a></li><li><a href="#_OrderServiceImpl__saveOrder__1765" rel="nofollow">修改 OrderServiceImpl 的 saveOrder() 方法</a></li></ul><li><a href="#_1816" rel="nofollow">手动确认</a></li><ul><li><a href="#applicationyml_1818" rel="nofollow">application.yml</a></li><li><a href="#OrderConsumer_1828" rel="nofollow">OrderConsumer</a></li></ul></ul></ul></div><p></p>
<h1><a id="RabbitMQ__1"></a>RabbitMQ 使用场景</h1>
<h2><a id="_3"></a>服务解耦</h2>
<p>假设有这样一个场景, 服务A产生数据, 而服务B,C,D需要这些数据, 那么我们可以在A服务中直接调用B,C,D服务,把数据传递到下游服务即可</p>
<p>但是,随着我们的应用规模不断扩大,会有更多的服务需要A的数据,如果有几十甚至几百个下游服务,而且会不断变更,再加上还要考虑下游服务出错的情况,那么A服务中调用代码的维护会极为困难</p>
<p>这是由于服务之间耦合度过于紧密</p>
<p><img src="https://img-blog.csdnimg.cn/20191031160542204.png" alt="耦合"></p>
<p>再来考虑用RabbitMQ解耦的情况</p>
<p>A服务只需要向消息服务器发送消息,而不用考虑谁需要这些数据;下游服务如果需要数据,自行从消息服务器订阅消息,不再需要数据时则取消订阅即可</p>
<p><img src="https://img-blog.csdnimg.cn/201910311606241.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="解耦"></p>
<h2><a id="_19"></a>流量削峰</h2>
<p>假设我们有一个应用,平时访问量是每秒300请求,我们用一台服务器即可轻松应对</p>
<p><img src="https://img-blog.csdnimg.cn/20191031160702125.png" alt="低流量"></p>
<p>而在高峰期,访问量瞬间翻了十倍,达到每秒3000次请求,那么单台服务器肯定无法应对,这时我们可以考虑增加到10台服务器,来分散访问压力</p>
<p>但如果这种瞬时高峰的情况每天只出现一次,每次只有半小时,那么我们10台服务器在多数时间都只分担每秒几十次请求,这样就有点浪费资源了</p>
<p><img src="https://img-blog.csdnimg.cn/20191031160740317.png" alt="流量峰值"></p>
<p>这种情况,我们就可以使用RabbitMQ来进行流量削峰,高峰情况下,瞬间出现的大量请求数据,先发送到消息队列服务器,排队等待被处理,而我们的应用,可以慢慢的从消息队列接收请求数据进行处理,这样把数据处理时间拉长,以减轻瞬时压力</p>
<p>这是消息队列服务器非常典型的应用场景</p>
<p><img src="https://img-blog.csdnimg.cn/20191031160820872.png" alt="流量销峰"></p>
<h2><a id="_37"></a>异步调用</h2>
<p>考虑定外卖支付成功的情况</p>
<p>支付后要发送支付成功的通知,再寻找外卖小哥来进行配送,而寻找外卖小哥的过程非常耗时,尤其是高峰期,可能要等待几十秒甚至更长</p>
<p>这样就造成整条调用链路响应非常缓慢</p>
<p><img src="https://img-blog.csdnimg.cn/20191031160931221.png" alt="阻塞"></p>
<p>而如果我们引入RabbitMQ消息队列,订单数据可以发送到消息队列服务器,那么调用链路也就可以到此结束,订单系统则可以立即得到响应,整条链路的响应时间只有200毫秒左右</p>
<p>寻找外卖小哥的应用可以以异步的方式从消息队列接收订单消息,再执行耗时的寻找操作</p>
<p><img src="https://img-blog.csdnimg.cn/20191031161041367.png" alt="异步调用"></p>
<h1><a id="rabbitmq__57"></a>rabbitmq 基本概念</h1>
<p>RabbitMQ是一种消息中间件，用于处理来自客户端的异步消息。服务端将要发送的消息放入到队列池中。接收端可以根据RabbitMQ配置的转发机制接收服务端发来的消息。RabbitMQ依据指定的转发规则进行消息的转发、缓冲和持久化操作，主要用在多服务器间或单服务器的子系统间进行通信，是分布式系统标准的配置。</p>
<p><img src="https://img-blog.csdnimg.cn/2019103116113556.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="rabbitmq"></p>
<h2><a id="Exchange_64"></a>Exchange</h2>
<p>接受生产者发送的消息，并根据Binding规则将消息路由给服务器中的队列。ExchangeType决定了Exchange路由消息的行为。在RabbitMQ中，ExchangeType常用的有direct、Fanout和Topic三种。</p>
<p><img src="https://img-blog.csdnimg.cn/20191031164046114.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="exchange"></p>
<h2><a id="Message_Queue_70"></a>Message Queue</h2>
<p>消息队列。我们发送给RabbitMQ的消息最后都会到达各种queue，并且存储在其中(如果路由找不到相应的queue则数据会丢失)，等待消费者来取。</p>
<h2><a id="Binding_Key_74"></a>Binding Key</h2>
<p>它表示的是Exchange与Message Queue是通过binding key进行联系的，这个关系是固定。</p>
<h2><a id="Routing_Key_78"></a>Routing Key</h2>
<p>生产者在将消息发送给Exchange的时候，一般会指定一个routing key，来指定这个消息的路由规则。这个routing key需要与Exchange Type及binding key联合使用才能生，我们的生产者只需要通过指定routing key来决定消息流向哪里。</p>
<h1><a id="rabbitmq_82"></a>rabbitmq安装</h1>
<p>在centos7上安装rabbitmq</p>
<h2><a id="erlang_86"></a>安装erlang语言库</h2>
<p>RabbitMQ使用了Erlang开发语言，Erlang是为电话交换机开发的语言，天生自带高并发光环，和高可用特性</p>
<h3><a id="rabbitmqErlang_90"></a>rabbitmq官方精简的Erlang语言包</h3>
<ul>
<li>
<p>0依赖rpm安装包</p>
</li>
<li>
<p><a href="https://github.com/rabbitmq/erlang-rpm">https://github.com/rabbitmq/erlang-rpm</a></p>
</li>
</ul>
<p><img src="https://img-blog.csdnimg.cn/20191031164128494.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="erlang"></p>
<h3><a id="_99"></a>下载和安装</h3>
<pre><code class="prism language-shell"><span class="token comment"># 下载Erlang语言包</span>
<span class="token function">wget</span> https://github.com/rabbitmq/erlang-rpm/releases/download/v21.2.6/erlang-21.2.6-1.el7.x86_64.rpm

<span class="token comment"># 安装Erlang</span>
rpm -ivh erlang-21.2.6-1.el7.x86_64.rpm --force --nodeps
</code></pre>
<h2><a id="socat_109"></a>安装socat依赖</h2>
<h3><a id="socat_111"></a>socat依赖包</h3>
<ul>
<li><a href="https://pkgs.org/download/socat" rel="nofollow">https://pkgs.org/download/socat</a></li>
</ul>
<p><img src="https://img-blog.csdnimg.cn/2019103116422815.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="socat"></p>
<ul>
<li><a href="https://centos.pkgs.org/7/centos-x86_64/socat-1.7.3.2-2.el7.x86_64.rpm.html" rel="nofollow">https://centos.pkgs.org/7/centos-x86_64/socat-1.7.3.2-2.el7.x86_64.rpm.html</a></li>
</ul>
<p><img src="https://img-blog.csdnimg.cn/20191031164338710.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="socat"></p>
<h3><a id="_121"></a>下载和安装</h3>
<pre><code class="prism language-shell"><span class="token comment"># 下载 socat rpm</span>
<span class="token function">wget</span> http://mirror.centos.org/centos/7/os/x86_64/Packages/socat-1.7.3.2-2.el7.x86_64.rpm

<span class="token comment"># 安装 socat 依赖包</span>
rpm -ivh socat-1.7.3.2-2.el7.x86_64.rpm
</code></pre>
<h2><a id="rabbitmq_131"></a>安装rabbitmq</h2>
<h3><a id="rabbitmq_133"></a>rabbitmq安装包</h3>
<ul>
<li><a href="http://www.rabbitmq.com/install-rpm.html#downloads" rel="nofollow">http://www.rabbitmq.com/install-rpm.html#downloads</a></li>
</ul>
<p><img src="https://img-blog.csdnimg.cn/20191031164429219.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="rabbitmq"></p>
<h3><a id="_139"></a>下载和安装</h3>
<pre><code class="prism language-shell"><span class="token comment"># 下载 rpm 包</span>
<span class="token function">wget</span> https://github.com/rabbitmq/rabbitmq-server/releases/download/v3.7.13/rabbitmq-server-3.7.13-1.el7.noarch.rpm

<span class="token comment"># 安装 rpm 包</span>
rpm -ivh rabbitmq-server-3.7.13-1.el7.noarch.rpm
</code></pre>
<h2><a id="rabbitmq_150"></a>rabbitmq启动和停止命令</h2>
<pre><code class="prism language-shell"><span class="token comment"># 设置服务,开机自动启动</span>
<span class="token function">chkconfig</span> rabbitmq-server on

<span class="token comment"># 启动服务</span>
<span class="token function">service</span> rabbitmq-server start

<span class="token comment"># 停止服务</span>
<span class="token function">service</span> rabbitmq-server stop
</code></pre>
<h2><a id="rabbitmq_163"></a>rabbitmq管理界面</h2>
<h3><a id="_165"></a>启用管理界面</h3>
<pre><code class="prism language-shell"><span class="token comment"># 开启管理界面插件</span>
rabbitmq-plugins <span class="token function">enable</span> rabbitmq_management

<span class="token comment"># 防火墙打开 15672 管理端口</span>
firewall-cmd --zone<span class="token operator">=</span>public --add-port<span class="token operator">=</span>15672/tcp --permanent
firewall-cmd --reload
</code></pre>
<h3><a id="_176"></a>访问</h3>
<p>访问服务器的<code>15672</code>端口,例如:<br><br>
http://192.168.64.140:15672</p>
<h2><a id="_184"></a>添加用户</h2>
<h3><a id="_186"></a>添加用户</h3>
<pre><code class="prism language-shell"><span class="token comment"># 添加用户</span>
rabbitmqctl add_user admin admin

<span class="token comment"># 新用户设置用户为超级管理员</span>
rabbitmqctl set_user_tags admin administrator
</code></pre>
<h3><a id="_196"></a>设置访问权限</h3>
<p><img src="https://img-blog.csdnimg.cn/20191031164604441.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="访问权限"></p>
<ul>
<li>用户管理参考<br>
<a href="https://www.cnblogs.com/AloneSword/p/4200051.html" rel="nofollow">https://www.cnblogs.com/AloneSword/p/4200051.html</a></li>
</ul>
<h2><a id="_204"></a>开放客户端连接端口</h2>
<pre><code class="prism language-shell"><span class="token comment"># 打开客户端连接端口</span>
firewall-cmd --zone<span class="token operator">=</span>public --add-port<span class="token operator">=</span>5672/tcp --permanent
firewall-cmd --reload
</code></pre>
<ul>
<li>主要端口介绍
<ul>
<li>4369 – erlang发现口</li>
<li>5672 – client端通信口</li>
<li>15672 – 管理界面ui端口</li>
<li>25672 – server间内部通信口</li>
</ul>
</li>
</ul>
<h1><a id="rabbitmq_219"></a>rabbitmq六种工作模式</h1>
<h2><a id="_221"></a>简单模式</h2>
<p>RabbitMQ是一个消息中间件，你可以想象它是一个邮局。当你把信件放到邮箱里时，能够确信邮递员会正确地递送你的信件。RabbitMq就是一个邮箱、一个邮局和一个邮递员。</p>
<ul>
<li>发送消息的程序是<mark>生产者</mark></li>
<li><mark>队列</mark>就代表一个邮箱。虽然消息会流经RbbitMQ和你的应用程序，但消息只能被存储在队列里。队列存储空间只受服务器内存和磁盘限制，它本质上是一个大的消息缓冲区。多个生产者可以向同一个队列发送消息，多个消费者也可以从同一个队列接收消息.</li>
<li><mark>消费者</mark>等待从队列接收消息</li>
</ul>
<p><img src="https://img-blog.csdnimg.cn/20191031164725816.png" alt="简单模式"></p>
<h3><a id="pomxml_232"></a>pom.xml</h3>
<p>添加 slf4j 依赖, 和 rabbitmq amqp 依赖</p>
<pre><code class="prism language-xml"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>project</span> <span class="token attr-name">xmlns</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>http://maven.apache.org/POM/4.0.0<span class="token punctuation">"</span></span>
	<span class="token attr-name"><span class="token namespace">xmlns:</span>xsi</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>http://www.w3.org/2001/XMLSchema-instance<span class="token punctuation">"</span></span>
	<span class="token attr-name"><span class="token namespace">xsi:</span>schemaLocation</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>modelVersion</span><span class="token punctuation">&gt;</span></span>4.0.0<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>modelVersion</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>groupId</span><span class="token punctuation">&gt;</span></span>com.tedu<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>groupId</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>artifactId</span><span class="token punctuation">&gt;</span></span>rabbitmq<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>artifactId</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>version</span><span class="token punctuation">&gt;</span></span>0.0.1-SNAPSHOT<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>version</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>dependencies</span><span class="token punctuation">&gt;</span></span>
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>dependency</span><span class="token punctuation">&gt;</span></span>
			<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>groupId</span><span class="token punctuation">&gt;</span></span>com.rabbitmq<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>groupId</span><span class="token punctuation">&gt;</span></span>
			<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>artifactId</span><span class="token punctuation">&gt;</span></span>amqp-client<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>artifactId</span><span class="token punctuation">&gt;</span></span>
			<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>version</span><span class="token punctuation">&gt;</span></span>5.4.3<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>version</span><span class="token punctuation">&gt;</span></span>
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>dependency</span><span class="token punctuation">&gt;</span></span>
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>dependency</span><span class="token punctuation">&gt;</span></span>
			<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>groupId</span><span class="token punctuation">&gt;</span></span>org.slf4j<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>groupId</span><span class="token punctuation">&gt;</span></span>
			<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>artifactId</span><span class="token punctuation">&gt;</span></span>slf4j-api<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>artifactId</span><span class="token punctuation">&gt;</span></span>
			<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>version</span><span class="token punctuation">&gt;</span></span>1.8.0-alpha2<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>version</span><span class="token punctuation">&gt;</span></span>
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>dependency</span><span class="token punctuation">&gt;</span></span>
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>dependency</span><span class="token punctuation">&gt;</span></span>
			<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>groupId</span><span class="token punctuation">&gt;</span></span>org.slf4j<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>groupId</span><span class="token punctuation">&gt;</span></span>
			<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>artifactId</span><span class="token punctuation">&gt;</span></span>slf4j-log4j12<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>artifactId</span><span class="token punctuation">&gt;</span></span>
			<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>version</span><span class="token punctuation">&gt;</span></span>1.8.0-alpha2<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>version</span><span class="token punctuation">&gt;</span></span>
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>dependency</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>dependencies</span><span class="token punctuation">&gt;</span></span>

	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>build</span><span class="token punctuation">&gt;</span></span>
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>plugins</span><span class="token punctuation">&gt;</span></span>
			<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>plugin</span><span class="token punctuation">&gt;</span></span>
				<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>groupId</span><span class="token punctuation">&gt;</span></span>org.apache.maven.plugins<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>groupId</span><span class="token punctuation">&gt;</span></span>
				<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>artifactId</span><span class="token punctuation">&gt;</span></span>maven-compiler-plugin<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>artifactId</span><span class="token punctuation">&gt;</span></span>
				<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>version</span><span class="token punctuation">&gt;</span></span>3.8.0<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>version</span><span class="token punctuation">&gt;</span></span>
				<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>configuration</span><span class="token punctuation">&gt;</span></span>
					<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>source</span><span class="token punctuation">&gt;</span></span>1.8<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>source</span><span class="token punctuation">&gt;</span></span>
					<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>target</span><span class="token punctuation">&gt;</span></span>1.8<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>target</span><span class="token punctuation">&gt;</span></span>
				<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>configuration</span><span class="token punctuation">&gt;</span></span>
			<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>plugin</span><span class="token punctuation">&gt;</span></span>
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>plugins</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>build</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>project</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<h3><a id="_279"></a>生产者发送消息</h3>
<pre><code class="prism language-java"><span class="token keyword">package</span> rabbitmq<span class="token punctuation">.</span>simple<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Channel<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Connection<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>ConnectionFactory<span class="token punctuation">;</span>

<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">Test1</span> <span class="token punctuation">{</span>
	<span class="token keyword">public</span> <span class="token keyword">static</span> <span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span>String<span class="token punctuation">[</span><span class="token punctuation">]</span> args<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		<span class="token comment">//创建连接工厂,并设置连接信息</span>
		ConnectionFactory f <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ConnectionFactory</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setHost</span><span class="token punctuation">(</span><span class="token string">"192.168.64.140"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPort</span><span class="token punctuation">(</span><span class="token number">5672</span><span class="token punctuation">)</span><span class="token punctuation">;</span><span class="token comment">//可选,5672是默认端口</span>
		f<span class="token punctuation">.</span><span class="token function">setUsername</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPassword</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

		<span class="token comment">/*
		 * 与rabbitmq服务器建立连接,
		 * rabbitmq服务器端使用的是nio,会复用tcp连接,
		 * 并开辟多个信道与客户端通信
		 * 以减轻服务器端建立连接的开销
		 */</span>
		Connection c <span class="token operator">=</span> f<span class="token punctuation">.</span><span class="token function">newConnection</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token comment">//建立信道</span>
		Channel ch <span class="token operator">=</span> c<span class="token punctuation">.</span><span class="token function">createChannel</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

		<span class="token comment">/*
		 * 声明队列,会在rabbitmq中创建一个队列
		 * 如果已经创建过该队列，就不能再使用其他参数来创建
		 * 
		 * 参数含义:
		 *   -queue: 队列名称
		 *   -durable: 队列持久化,true表示RabbitMQ重启后队列仍存在
		 *   -exclusive: 排他,true表示限制仅当前连接可用
		 *   -autoDelete: 当最后一个消费者断开后,是否删除队列
		 *   -arguments: 其他参数
		 */</span>
		ch<span class="token punctuation">.</span><span class="token function">queueDeclare</span><span class="token punctuation">(</span><span class="token string">"helloworld"</span><span class="token punctuation">,</span> <span class="token boolean">false</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span>null<span class="token punctuation">)</span><span class="token punctuation">;</span>

		<span class="token comment">/*
		 * 发布消息
		 * 这里把消息向默认交换机发送.
		 * 默认交换机隐含与所有队列绑定,routing key即为队列名称
		 * 
		 * 参数含义:
		 * 	-exchange: 交换机名称,空串表示默认交换机"(AMQP default)",不能用 null 
		 * 	-routingKey: 对于默认交换机,路由键就是目标队列名称
		 * 	-props: 其他参数,例如头信息
		 * 	-body: 消息内容byte[]数组
		 */</span>
		ch<span class="token punctuation">.</span><span class="token function">basicPublish</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">"helloworld"</span><span class="token punctuation">,</span> null<span class="token punctuation">,</span> <span class="token string">"Hello world!"</span><span class="token punctuation">.</span><span class="token function">getBytes</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

		System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"消息已发送"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		c<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3><a id="_339"></a>消费者接收消息</h3>
<pre><code class="prism language-java"><span class="token keyword">package</span> rabbitmq<span class="token punctuation">.</span>simple<span class="token punctuation">;</span>

<span class="token keyword">import</span> java<span class="token punctuation">.</span>io<span class="token punctuation">.</span>IOException<span class="token punctuation">;</span>
<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>concurrent<span class="token punctuation">.</span>TimeoutException<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>CancelCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Channel<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Connection<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>ConnectionFactory<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>DeliverCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Delivery<span class="token punctuation">;</span>

<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">Test2</span> <span class="token punctuation">{</span>
	<span class="token keyword">public</span> <span class="token keyword">static</span> <span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span>String<span class="token punctuation">[</span><span class="token punctuation">]</span> args<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		<span class="token comment">//连接工厂</span>
		ConnectionFactory f <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ConnectionFactory</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setHost</span><span class="token punctuation">(</span><span class="token string">"192.168.64.140"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setUsername</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPassword</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token comment">//建立连接</span>
		Connection c <span class="token operator">=</span> f<span class="token punctuation">.</span><span class="token function">newConnection</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token comment">//建立信道</span>
		Channel ch <span class="token operator">=</span> c<span class="token punctuation">.</span><span class="token function">createChannel</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token comment">//声明队列,如果该队列已经创建过,则不会重复创建</span>
		ch<span class="token punctuation">.</span><span class="token function">queueDeclare</span><span class="token punctuation">(</span><span class="token string">"helloworld"</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span>null<span class="token punctuation">)</span><span class="token punctuation">;</span>
		System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"等待接收数据"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//收到消息后用来处理消息的回调对象</span>
		DeliverCallback callback <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">DeliverCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">,</span> Delivery message<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
				String msg <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">String</span><span class="token punctuation">(</span>message<span class="token punctuation">.</span><span class="token function">getBody</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token string">"UTF-8"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
				System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"收到: "</span><span class="token operator">+</span>msg<span class="token punctuation">)</span><span class="token punctuation">;</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		<span class="token comment">//消费者取消时的回调对象</span>
		CancelCallback cancel <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">CancelCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		ch<span class="token punctuation">.</span><span class="token function">basicConsume</span><span class="token punctuation">(</span><span class="token string">"helloworld"</span><span class="token punctuation">,</span> <span class="token boolean">true</span><span class="token punctuation">,</span> callback<span class="token punctuation">,</span> cancel<span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h2><a id="_390"></a>工作模式</h2>
<p><img src="https://img-blog.csdnimg.cn/20191031164808497.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="工作模式"></p>
<p>工作队列(即任务队列)背后的主要思想是避免立即执行资源密集型任务，并且必须等待它完成。相反，我们将任务安排在稍后完成。</p>
<p>我们将任务封装为消息并将其发送到队列。后台运行的工作进程将获取任务并最终执行任务。当运行多个消费者时，任务将在它们之间分发。</p>
<p>使用任务队列的一个优点是能够轻松地并行工作。如果我们正在积压工作任务，我们可以添加更多工作进程，这样就可以轻松扩展。</p>
<h3><a id="_400"></a>生产者发送消息</h3>
<p>这里模拟耗时任务,发送的消息中,每个点使工作进程暂停一秒钟,例如"Hello…"将花费3秒钟来处理</p>
<pre><code class="prism language-java"><span class="token keyword">package</span> rabbitmq<span class="token punctuation">.</span>workqueue<span class="token punctuation">;</span>

<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>Scanner<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Channel<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Connection<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>ConnectionFactory<span class="token punctuation">;</span>

<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">Test1</span> <span class="token punctuation">{</span>
	<span class="token keyword">public</span> <span class="token keyword">static</span> <span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span>String<span class="token punctuation">[</span><span class="token punctuation">]</span> args<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		ConnectionFactory f <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ConnectionFactory</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setHost</span><span class="token punctuation">(</span><span class="token string">"192.168.64.140"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPort</span><span class="token punctuation">(</span><span class="token number">5672</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setUsername</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPassword</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		Connection c <span class="token operator">=</span> f<span class="token punctuation">.</span><span class="token function">newConnection</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		Channel ch <span class="token operator">=</span> c<span class="token punctuation">.</span><span class="token function">createChannel</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token comment">//参数:queue,durable,exclusive,autoDelete,arguments</span>
		ch<span class="token punctuation">.</span><span class="token function">queueDeclare</span><span class="token punctuation">(</span><span class="token string">"helloworld"</span><span class="token punctuation">,</span> <span class="token boolean">false</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span>null<span class="token punctuation">)</span><span class="token punctuation">;</span>

		<span class="token keyword">while</span> <span class="token punctuation">(</span><span class="token boolean">true</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
		    <span class="token comment">//控制台输入的消息发送到rabbitmq</span>
			System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">print</span><span class="token punctuation">(</span><span class="token string">"输入消息: "</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			String msg <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Scanner</span><span class="token punctuation">(</span>System<span class="token punctuation">.</span>in<span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">nextLine</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			<span class="token comment">//如果输入的是"exit"则结束生产者进程</span>
			<span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token string">"exit"</span><span class="token punctuation">.</span><span class="token function">equals</span><span class="token punctuation">(</span>msg<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
				<span class="token keyword">break</span><span class="token punctuation">;</span>
			<span class="token punctuation">}</span>
			<span class="token comment">//参数:exchage,routingKey,props,body</span>
			ch<span class="token punctuation">.</span><span class="token function">basicPublish</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">"helloworld"</span><span class="token punctuation">,</span> null<span class="token punctuation">,</span> msg<span class="token punctuation">.</span><span class="token function">getBytes</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"消息已发送: "</span><span class="token operator">+</span>msg<span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token punctuation">}</span>

		c<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3><a id="_444"></a>消费者接收消息</h3>
<pre><code class="prism language-java"><span class="token keyword">package</span> rabbitmq<span class="token punctuation">.</span>workqueue<span class="token punctuation">;</span>

<span class="token keyword">import</span> java<span class="token punctuation">.</span>io<span class="token punctuation">.</span>IOException<span class="token punctuation">;</span>
<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>concurrent<span class="token punctuation">.</span>TimeoutException<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>CancelCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Channel<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Connection<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>ConnectionFactory<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>DeliverCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Delivery<span class="token punctuation">;</span>

<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">Test2</span> <span class="token punctuation">{</span>
	<span class="token keyword">public</span> <span class="token keyword">static</span> <span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span>String<span class="token punctuation">[</span><span class="token punctuation">]</span> args<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		ConnectionFactory f <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ConnectionFactory</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setHost</span><span class="token punctuation">(</span><span class="token string">"192.168.64.140"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setUsername</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPassword</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		Connection c <span class="token operator">=</span> f<span class="token punctuation">.</span><span class="token function">newConnection</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		Channel ch <span class="token operator">=</span> c<span class="token punctuation">.</span><span class="token function">createChannel</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		ch<span class="token punctuation">.</span><span class="token function">queueDeclare</span><span class="token punctuation">(</span><span class="token string">"helloworld"</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span>null<span class="token punctuation">)</span><span class="token punctuation">;</span>
		System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"等待接收数据"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//收到消息后用来处理消息的回调对象</span>
		DeliverCallback callback <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">DeliverCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">,</span> Delivery message<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
				String msg <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">String</span><span class="token punctuation">(</span>message<span class="token punctuation">.</span><span class="token function">getBody</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token string">"UTF-8"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
				System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"收到: "</span><span class="token operator">+</span>msg<span class="token punctuation">)</span><span class="token punctuation">;</span>

				<span class="token comment">//遍历字符串中的字符,每个点使进程暂停一秒</span>
				<span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">int</span> i <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> i <span class="token operator">&lt;</span> msg<span class="token punctuation">.</span><span class="token function">length</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> i<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
					<span class="token keyword">if</span> <span class="token punctuation">(</span>msg<span class="token punctuation">.</span><span class="token function">charAt</span><span class="token punctuation">(</span>i<span class="token punctuation">)</span><span class="token operator">==</span><span class="token string">'.'</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
						<span class="token keyword">try</span> <span class="token punctuation">{</span>
							Thread<span class="token punctuation">.</span><span class="token function">sleep</span><span class="token punctuation">(</span><span class="token number">1000</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
						<span class="token punctuation">}</span> <span class="token keyword">catch</span> <span class="token punctuation">(</span><span class="token class-name">InterruptedException</span> e<span class="token punctuation">)</span> <span class="token punctuation">{</span>
						<span class="token punctuation">}</span>
					<span class="token punctuation">}</span>
				<span class="token punctuation">}</span>
				System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"处理结束"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		<span class="token comment">//消费者取消时的回调对象</span>
		CancelCallback cancel <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">CancelCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		ch<span class="token punctuation">.</span><span class="token function">basicConsume</span><span class="token punctuation">(</span><span class="token string">"helloworld"</span><span class="token punctuation">,</span> <span class="token boolean">true</span><span class="token punctuation">,</span> callback<span class="token punctuation">,</span> cancel<span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3><a id="_502"></a>运行测试</h3>
<p>运行:</p>
<ul>
<li>一个生产者</li>
<li>两个消费者</li>
</ul>
<p>生产者发送多条消息,<br>
如: 1,2,3,4,5. 两个消费者分别收到:</p>
<ul>
<li>消费者一: 1,3,5</li>
<li>消费者二: 2,4</li>
</ul>
<p>rabbitmq在所有消费者中轮询分发消息,把消息均匀地发送给所有消费者</p>
<h3><a id="_515"></a>消息确认</h3>
<p>一个消费者接收消息后,在消息没有完全处理完时就挂掉了,那么这时会发生什么呢?</p>
<p>就现在的代码来说,rabbitmq把消息发送给消费者后,会立即删除消息,那么消费者挂掉后,它没来得及处理的消息就会丢失</p>
<blockquote>
<p>如果生产者发送以下消息: <br><br>
1…<br><br>
2<br><br>
3<br><br>
4<br><br>
5<br></p>
<p>两个消费者分别收到:</p>
<ul>
<li>消费者一: 1…, 3, 5</li>
<li>消费者二: 2, 4</li>
</ul>
<p>当消费者一收到所有消息后,要话费7秒时间来处理第一条消息,这期间如果关闭该消费者,那么1未处理完成,3,5则没有被处理</p>
</blockquote>
<p>我们并不想丢失任何消息, 如果一个消费者挂掉,我们想把它的任务消息派发给其他消费者</p>
<p>为了确保消息不会丢失，rabbitmq支持消息确认(回执)。当一个消息被消费者接收到并且执行完成后，消费者会发送一个ack (acknowledgment) 给rabbitmq服务器, 告诉他我已经执行完成了，你可以把这条消息删除了。</p>
<p>如果一个消费者没有返回消息确认就挂掉了（信道关闭，连接关闭或者TCP链接丢失），rabbitmq就会明白，这个消息没有被处理完成，rebbitmq就会把这条消息重新放入队列，如果在这时有其他的消费者在线，那么rabbitmq就会迅速的把这条消息传递给其他的消费者，这样就确保了没有消息会丢失。</p>
<p>这里不存在消息超时, rabbitmq只在消费者挂掉时重新分派消息, 即使消费者花非常久的时间来处理消息也可以</p>
<p>手动消息确认默认是开启的，前面的例子我们通过autoAck=ture把它关闭了。我们现在要把它设置为false，然后工作进程处理完意向任务时,发送一个消息确认(回执)。</p>
<pre><code class="prism language-java"><span class="token keyword">package</span> rabbitmq<span class="token punctuation">.</span>workqueue<span class="token punctuation">;</span>

<span class="token keyword">import</span> java<span class="token punctuation">.</span>io<span class="token punctuation">.</span>IOException<span class="token punctuation">;</span>
<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>concurrent<span class="token punctuation">.</span>TimeoutException<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>CancelCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Channel<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Connection<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>ConnectionFactory<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>DeliverCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Delivery<span class="token punctuation">;</span>

<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">Test2</span> <span class="token punctuation">{</span>
	<span class="token keyword">public</span> <span class="token keyword">static</span> <span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span>String<span class="token punctuation">[</span><span class="token punctuation">]</span> args<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		<span class="token comment">//连接工厂</span>
		ConnectionFactory f <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ConnectionFactory</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setHost</span><span class="token punctuation">(</span><span class="token string">"192.168.64.140"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setUsername</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPassword</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token comment">//建立连接</span>
		Connection c <span class="token operator">=</span> f<span class="token punctuation">.</span><span class="token function">newConnection</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token comment">//建立信道</span>
		Channel ch <span class="token operator">=</span> c<span class="token punctuation">.</span><span class="token function">createChannel</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token comment">//声明队列</span>
		ch<span class="token punctuation">.</span><span class="token function">queueDeclare</span><span class="token punctuation">(</span><span class="token string">"helloworld"</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span>null<span class="token punctuation">)</span><span class="token punctuation">;</span>
		System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"等待接收数据"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//收到消息后用来处理消息的回调对象</span>
		DeliverCallback callback <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">DeliverCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">,</span> Delivery message<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
				String msg <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">String</span><span class="token punctuation">(</span>message<span class="token punctuation">.</span><span class="token function">getBody</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token string">"UTF-8"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
				System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"收到: "</span><span class="token operator">+</span>msg<span class="token punctuation">)</span><span class="token punctuation">;</span>
				<span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">int</span> i <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> i <span class="token operator">&lt;</span> msg<span class="token punctuation">.</span><span class="token function">length</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> i<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
					<span class="token keyword">if</span> <span class="token punctuation">(</span>msg<span class="token punctuation">.</span><span class="token function">charAt</span><span class="token punctuation">(</span>i<span class="token punctuation">)</span><span class="token operator">==</span><span class="token string">'.'</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
						<span class="token keyword">try</span> <span class="token punctuation">{</span>
							Thread<span class="token punctuation">.</span><span class="token function">sleep</span><span class="token punctuation">(</span><span class="token number">1000</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
						<span class="token punctuation">}</span> <span class="token keyword">catch</span> <span class="token punctuation">(</span><span class="token class-name">InterruptedException</span> e<span class="token punctuation">)</span> <span class="token punctuation">{</span>
						<span class="token punctuation">}</span>
					<span class="token punctuation">}</span>
				<span class="token punctuation">}</span>
				System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"处理结束"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
				<span class="token comment">//发送回执</span>
				ch<span class="token punctuation">.</span><span class="token function">basicAck</span><span class="token punctuation">(</span>message<span class="token punctuation">.</span><span class="token function">getEnvelope</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getDeliveryTag</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token boolean">false</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		<span class="token comment">//消费者取消时的回调对象</span>
		CancelCallback cancel <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">CancelCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		<span class="token comment">//autoAck设置为false,则需要手动确认发送回执</span>
		ch<span class="token punctuation">.</span><span class="token function">basicConsume</span><span class="token punctuation">(</span><span class="token string">"helloworld"</span><span class="token punctuation">,</span> <span class="token boolean">false</span><span class="token punctuation">,</span> callback<span class="token punctuation">,</span> cancel<span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>

</code></pre>
<p>使用以上代码，就算杀掉一个正在处理消息的工作进程也不会丢失任何消息，工作进程挂掉之后，没有确认的消息就会被自动重新传递。</p>
<blockquote>
<p>忘记确认(ack)是一个常见的错误, 这样后果是很严重的, 由于未确认的消息不会被释放, rabbitmq会吃掉越来越多的内存</p>
<p>可以使用下面命令打印工作队列中未确认消息的数量</p>
<pre><code class="prism language-shell">rabbitmqctl list_queues name messages_ready messages_unacknowledged
</code></pre>
</blockquote>
<h3><a id="_618"></a>消息持久化</h3>
<p>当rabbitmq关闭时, 我们队列中的消息仍然会丢失, 除非明确要求它不要丢失数据</p>
<p>要求rabbitmq不丢失数据要做如下两点: 把队列和消息都设置为可持久化(durable)</p>
<p>队列设置为可持久化, 可以在定义队列时指定参数durable为true</p>
<pre><code class="prism language-java"><span class="token comment">//第二个参数是持久化参数durable</span>
ch<span class="token punctuation">.</span><span class="token function">queueDeclare</span><span class="token punctuation">(</span><span class="token string">"helloworld"</span><span class="token punctuation">,</span> <span class="token boolean">true</span><span class="token punctuation">,</span> <span class="token boolean">false</span><span class="token punctuation">,</span> <span class="token boolean">false</span><span class="token punctuation">,</span> null<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<p>由于之前我们已经定义过队列"hello"是不可持久化的, 对已存在的队列, rabbitmq不允许对其定义不同的参数, 否则会出错, 所以这里我们定义一个不同名字的队列"task_queue"</p>
<pre><code class="prism language-java"><span class="token comment">//定义一个新的队列,名为 task_queue</span>
<span class="token comment">//第二个参数是持久化参数 durable</span>
ch<span class="token punctuation">.</span><span class="token function">queueDeclare</span><span class="token punctuation">(</span><span class="token string">"task_queue"</span><span class="token punctuation">,</span> <span class="token boolean">true</span><span class="token punctuation">,</span> <span class="token boolean">false</span><span class="token punctuation">,</span> <span class="token boolean">false</span><span class="token punctuation">,</span> null<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<p>生产者和消费者代码都要修改</p>
<p>这样即使rabbitmq重新启动, 队列也不会丢失. 现在我们再设置队列中消息的持久化, 使用<code>MessageProperties.PERSISTENT_TEXT_PLAIN</code>参数</p>
<pre><code class="prism language-java"><span class="token comment">//第三个参数设置消息持久化</span>
ch<span class="token punctuation">.</span><span class="token function">basicPublish</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">"task_queue"</span><span class="token punctuation">,</span>
            MessageProperties<span class="token punctuation">.</span>PERSISTENT_TEXT_PLAIN<span class="token punctuation">,</span>
            msg<span class="token punctuation">.</span><span class="token function">getBytes</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h3><a id="_648"></a>合理地分发</h3>
<p>rabbitmq会一次把多个消息分发给消费者, 这样可能造成有的消费者非常繁忙, 而其它消费者空闲. 而rabbitmq对此一无所知, 仍然会均匀的分发消息</p>
<p>我们可以使用 <code>basicQos(1)</code> 方法, 这告诉rabbitmq一次只向消费者发送一条消息, 在返回确认回执前, 不要向消费者发送新消息. 而是把消息发给下一个空闲的消费者</p>
<p><img src="https://img-blog.csdnimg.cn/20191031164847900.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="合理分发"></p>
<p>下面是"工作模式"最终完成的生产者和消费者代码</p>
<h3><a id="_658"></a>生产者代码</h3>
<pre><code class="prism language-java"><span class="token keyword">package</span> rabbitmq<span class="token punctuation">.</span>workqueue<span class="token punctuation">;</span>

<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>Scanner<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Channel<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Connection<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>ConnectionFactory<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>MessageProperties<span class="token punctuation">;</span>

<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">Test3</span> <span class="token punctuation">{</span>
	<span class="token keyword">public</span> <span class="token keyword">static</span> <span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span>String<span class="token punctuation">[</span><span class="token punctuation">]</span> args<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		ConnectionFactory f <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ConnectionFactory</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setHost</span><span class="token punctuation">(</span><span class="token string">"192.168.64.140"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPort</span><span class="token punctuation">(</span><span class="token number">5672</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setUsername</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPassword</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		Connection c <span class="token operator">=</span> f<span class="token punctuation">.</span><span class="token function">newConnection</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		Channel ch <span class="token operator">=</span> c<span class="token punctuation">.</span><span class="token function">createChannel</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//第二个参数设置队列持久化</span>
		ch<span class="token punctuation">.</span><span class="token function">queueDeclare</span><span class="token punctuation">(</span><span class="token string">"task_queue"</span><span class="token punctuation">,</span> <span class="token boolean">true</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span>null<span class="token punctuation">)</span><span class="token punctuation">;</span>

		<span class="token keyword">while</span> <span class="token punctuation">(</span><span class="token boolean">true</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">print</span><span class="token punctuation">(</span><span class="token string">"输入消息: "</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			String msg <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Scanner</span><span class="token punctuation">(</span>System<span class="token punctuation">.</span>in<span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">nextLine</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			<span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token string">"exit"</span><span class="token punctuation">.</span><span class="token function">equals</span><span class="token punctuation">(</span>msg<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
				<span class="token keyword">break</span><span class="token punctuation">;</span>
			<span class="token punctuation">}</span>
			
			<span class="token comment">//第三个参数设置消息持久化</span>
			ch<span class="token punctuation">.</span><span class="token function">basicPublish</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">"task_queue"</span><span class="token punctuation">,</span> MessageProperties<span class="token punctuation">.</span>PERSISTENT_TEXT_PLAIN<span class="token punctuation">,</span> msg<span class="token punctuation">.</span><span class="token function">getBytes</span><span class="token punctuation">(</span><span class="token string">"UTF-8"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"消息已发送: "</span><span class="token operator">+</span>msg<span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token punctuation">}</span>

		c<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3><a id="_701"></a>消费者代码</h3>
<pre><code class="prism language-java"><span class="token keyword">package</span> rabbitmq<span class="token punctuation">.</span>workqueue<span class="token punctuation">;</span>

<span class="token keyword">import</span> java<span class="token punctuation">.</span>io<span class="token punctuation">.</span>IOException<span class="token punctuation">;</span>
<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>concurrent<span class="token punctuation">.</span>TimeoutException<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>CancelCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Channel<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Connection<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>ConnectionFactory<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>DeliverCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Delivery<span class="token punctuation">;</span>

<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">Test4</span> <span class="token punctuation">{</span>
	<span class="token keyword">public</span> <span class="token keyword">static</span> <span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span>String<span class="token punctuation">[</span><span class="token punctuation">]</span> args<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		ConnectionFactory f <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ConnectionFactory</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setHost</span><span class="token punctuation">(</span><span class="token string">"192.168.64.140"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setUsername</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPassword</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		Connection c <span class="token operator">=</span> f<span class="token punctuation">.</span><span class="token function">newConnection</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		Channel ch <span class="token operator">=</span> c<span class="token punctuation">.</span><span class="token function">createChannel</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//第二个参数设置队列持久化</span>
		ch<span class="token punctuation">.</span><span class="token function">queueDeclare</span><span class="token punctuation">(</span><span class="token string">"task_queue"</span><span class="token punctuation">,</span><span class="token boolean">true</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span>null<span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"等待接收数据"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		ch<span class="token punctuation">.</span><span class="token function">basicQos</span><span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">//一次只接收一条消息</span>
		
		<span class="token comment">//收到消息后用来处理消息的回调对象</span>
		DeliverCallback callback <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">DeliverCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">,</span> Delivery message<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
				String msg <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">String</span><span class="token punctuation">(</span>message<span class="token punctuation">.</span><span class="token function">getBody</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token string">"UTF-8"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
				System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"收到: "</span><span class="token operator">+</span>msg<span class="token punctuation">)</span><span class="token punctuation">;</span>
				<span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">int</span> i <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> i <span class="token operator">&lt;</span> msg<span class="token punctuation">.</span><span class="token function">length</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> i<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
					<span class="token keyword">if</span> <span class="token punctuation">(</span>msg<span class="token punctuation">.</span><span class="token function">charAt</span><span class="token punctuation">(</span>i<span class="token punctuation">)</span><span class="token operator">==</span><span class="token string">'.'</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
						<span class="token keyword">try</span> <span class="token punctuation">{</span>
							Thread<span class="token punctuation">.</span><span class="token function">sleep</span><span class="token punctuation">(</span><span class="token number">1000</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
						<span class="token punctuation">}</span> <span class="token keyword">catch</span> <span class="token punctuation">(</span><span class="token class-name">InterruptedException</span> e<span class="token punctuation">)</span> <span class="token punctuation">{</span>
						<span class="token punctuation">}</span>
					<span class="token punctuation">}</span>
				<span class="token punctuation">}</span>
				System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"处理结束"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
				<span class="token comment">//发送回执</span>
				ch<span class="token punctuation">.</span><span class="token function">basicAck</span><span class="token punctuation">(</span>message<span class="token punctuation">.</span><span class="token function">getEnvelope</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getDeliveryTag</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token boolean">false</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		<span class="token comment">//消费者取消时的回调对象</span>
		CancelCallback cancel <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">CancelCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		<span class="token comment">//autoAck设置为false,则需要手动确认发送回执</span>
		ch<span class="token punctuation">.</span><span class="token function">basicConsume</span><span class="token punctuation">(</span><span class="token string">"task_queue"</span><span class="token punctuation">,</span> <span class="token boolean">false</span><span class="token punctuation">,</span> callback<span class="token punctuation">,</span> cancel<span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>

</code></pre>
<h2><a id="_766"></a>发布订阅模式</h2>
<p><img src="https://img-blog.csdnimg.cn/20191031164929124.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="发布订阅"></p>
<p>在前面的例子中，我们任务消息只交付给一个工作进程。在这部分，我们将做一些完全不同的事情——我们将向多个消费者传递同一条消息。这种模式称为“发布/订阅”。</p>
<p>为了说明该模式，我们将构建一个简单的日志系统。它将由两个程序组成——第一个程序将发出日志消息，第二个程序接收它们。</p>
<p>在我们的日志系统中，接收程序的每个运行副本都将获得消息。这样，我们就可以运行一个消费者并将日志保存到磁盘; 同时我们可以运行另一个消费者在屏幕上打印日志。</p>
<p>最终, 消息会被广播到所有消息接受者</p>
<h3><a id="Exchanges__778"></a>Exchanges 交换机</h3>
<p>RabbitMQ消息传递模型的核心思想是，生产者永远不会将任何消息直接发送到队列。实际上，通常生产者甚至不知道消息是否会被传递到任何队列。</p>
<p>相反，生产者只能向交换机(Exchange)发送消息。交换机是一个非常简单的东西。一边接收来自生产者的消息，另一边将消息推送到队列。交换器必须确切地知道如何处理它接收到的消息。它应该被添加到一个特定的队列中吗?它应该添加到多个队列中吗?或者它应该被丢弃。这些规则由exchange的类型定义。</p>
<p>有几种可用的交换类型:direct、topic、header和fanout。我们将关注最后一个——fanout。让我们创建一个这种类型的交换机，并称之为 logs: <code>ch.exchangeDeclare("logs", "fanout");</code></p>
<p>fanout交换机非常简单。它只是将接收到的所有消息广播给它所知道的所有队列。这正是我们的日志系统所需要的。</p>
<p>我们前面使用的队列具有特定的名称(还记得hello和task_queue吗?)能够为队列命名对我们来说至关重要——我们需要将工作进程指向同一个队列,在生产者和消费者之间共享队列。</p>
<p>但日志记录案例不是这种情况。我们想要接收所有的日志消息，而不仅仅是其中的一部分。我们还只对当前的最新消息感兴趣，而不是旧消息。</p>
<p>要解决这个问题，我们需要两件事。首先，每当我们连接到Rabbitmq时，我们需要一个新的空队列。为此，我们可以创建一个具有随机名称的队列，或者，更好的方法是让服务器为我们选择一个随机队列名称。其次，一旦断开与使用者的连接，队列就会自动删除。在Java客户端中，当我们不向queueDeclare()提供任何参数时，会创建一个具有生成名称的、非持久的、独占的、自动删除队列</p>
<pre><code class="prism language-java"><span class="token comment">//自动生成队列名</span>
<span class="token comment">//非持久,独占,自动删除</span>
String queueName <span class="token operator">=</span> ch<span class="token punctuation">.</span><span class="token function">queueDeclare</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getQueue</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h3><a id="_Bindings_800"></a>绑定 Bindings</h3>
<p><img src="https://img-blog.csdnimg.cn/20191031164958127.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="绑定"></p>
<p>我们已经创建了一个fanout交换机和一个队列。现在我们需要告诉exchange向指定队列发送消息。exchange和队列之间的关系称为绑定。</p>
<pre><code class="prism language-java"><span class="token comment">//指定的队列,与指定的交换机关联起来</span>
<span class="token comment">//成为绑定 -- binding</span>
<span class="token comment">//第三个参数时 routingKey, 由于是fanout交换机, 这里忽略 routingKey</span>
ch<span class="token punctuation">.</span><span class="token function">queueBind</span><span class="token punctuation">(</span>queueName<span class="token punctuation">,</span> <span class="token string">"logs"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<p>现在, logs交换机将会向我们指定的队列添加消息</p>
<blockquote>
<p>列出绑定关系:<br><br>
rabbitmqctl list_bindings</p>
</blockquote>
<h3><a id="_818"></a>完成的代码</h3>
<p><img src="https://img-blog.csdnimg.cn/20191031165034604.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="完成代码"></p>
<h4><a id="_822"></a>生产者</h4>
<p>生产者发出日志消息，看起来与前一教程没有太大不同。最重要的更改是，我们现在希望将消息发布到logs交换机，而不是无名的日志交换机。我们需要在发送时提供一个routingKey，但是对于fanout交换机类型，该值会被忽略。</p>
<pre><code class="prism language-java"><span class="token keyword">package</span> rabbitmq<span class="token punctuation">.</span>publishsubscribe<span class="token punctuation">;</span>

<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>Scanner<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Channel<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Connection<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>ConnectionFactory<span class="token punctuation">;</span>

<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">Test1</span> <span class="token punctuation">{</span>
	<span class="token keyword">public</span> <span class="token keyword">static</span> <span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span>String<span class="token punctuation">[</span><span class="token punctuation">]</span> args<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		ConnectionFactory f <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ConnectionFactory</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setHost</span><span class="token punctuation">(</span><span class="token string">"192.168.64.140"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPort</span><span class="token punctuation">(</span><span class="token number">5672</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setUsername</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPassword</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		Connection c <span class="token operator">=</span> f<span class="token punctuation">.</span><span class="token function">newConnection</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		Channel ch <span class="token operator">=</span> c<span class="token punctuation">.</span><span class="token function">createChannel</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//定义名字为logs的交换机,交换机类型为fanout</span>
		<span class="token comment">//这一步是必须的，因为禁止发布到不存在的交换。</span>
		ch<span class="token punctuation">.</span><span class="token function">exchangeDeclare</span><span class="token punctuation">(</span><span class="token string">"logs"</span><span class="token punctuation">,</span> <span class="token string">"fanout"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token keyword">while</span> <span class="token punctuation">(</span><span class="token boolean">true</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">print</span><span class="token punctuation">(</span><span class="token string">"输入消息: "</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			String msg <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Scanner</span><span class="token punctuation">(</span>System<span class="token punctuation">.</span>in<span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">nextLine</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			<span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token string">"exit"</span><span class="token punctuation">.</span><span class="token function">equals</span><span class="token punctuation">(</span>msg<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
				<span class="token keyword">break</span><span class="token punctuation">;</span>
			<span class="token punctuation">}</span>
			
			<span class="token comment">//第一个参数,向指定的交换机发送消息</span>
			<span class="token comment">//第二个参数,不指定队列,由消费者向交换机绑定队列</span>
			<span class="token comment">//如果还没有队列绑定到交换器，消息就会丢失，</span>
			<span class="token comment">//但这对我们来说没有问题;即使没有消费者接收，我们也可以安全地丢弃这些信息。</span>
			ch<span class="token punctuation">.</span><span class="token function">basicPublish</span><span class="token punctuation">(</span><span class="token string">"logs"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">,</span> null<span class="token punctuation">,</span> msg<span class="token punctuation">.</span><span class="token function">getBytes</span><span class="token punctuation">(</span><span class="token string">"UTF-8"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"消息已发送: "</span><span class="token operator">+</span>msg<span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token punctuation">}</span>

		c<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h4><a id="_872"></a>消费者</h4>
<p>如果还没有队列绑定到交换器，消息就会丢失，但这对我们来说没有问题;如果还没有消费者在听，我们可以安全地丢弃这些信息。<br>
ReceiveLogs.java代码:</p>
<pre><code class="prism language-java"><span class="token keyword">package</span> rabbitmq<span class="token punctuation">.</span>publishsubscribe<span class="token punctuation">;</span>

<span class="token keyword">import</span> java<span class="token punctuation">.</span>io<span class="token punctuation">.</span>IOException<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>CancelCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Channel<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Connection<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>ConnectionFactory<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>DeliverCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Delivery<span class="token punctuation">;</span>

<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">Test2</span> <span class="token punctuation">{</span>
	<span class="token keyword">public</span> <span class="token keyword">static</span> <span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span>String<span class="token punctuation">[</span><span class="token punctuation">]</span> args<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		ConnectionFactory f <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ConnectionFactory</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setHost</span><span class="token punctuation">(</span><span class="token string">"192.168.64.140"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setUsername</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPassword</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		Connection c <span class="token operator">=</span> f<span class="token punctuation">.</span><span class="token function">newConnection</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		Channel ch <span class="token operator">=</span> c<span class="token punctuation">.</span><span class="token function">createChannel</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//定义名字为 logs 的交换机, 它的类型是 fanout</span>
		ch<span class="token punctuation">.</span><span class="token function">exchangeDeclare</span><span class="token punctuation">(</span><span class="token string">"logs"</span><span class="token punctuation">,</span> <span class="token string">"fanout"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//自动生成对列名,</span>
		<span class="token comment">//非持久,独占,自动删除</span>
		String queueName <span class="token operator">=</span> ch<span class="token punctuation">.</span><span class="token function">queueDeclare</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getQueue</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//把该队列,绑定到 logs 交换机</span>
		<span class="token comment">//对于 fanout 类型的交换机, routingKey会被忽略，不允许null值</span>
		ch<span class="token punctuation">.</span><span class="token function">queueBind</span><span class="token punctuation">(</span>queueName<span class="token punctuation">,</span> <span class="token string">"logs"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"等待接收数据"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//收到消息后用来处理消息的回调对象</span>
		DeliverCallback callback <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">DeliverCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">,</span> Delivery message<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
				String msg <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">String</span><span class="token punctuation">(</span>message<span class="token punctuation">.</span><span class="token function">getBody</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token string">"UTF-8"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
				System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"收到: "</span><span class="token operator">+</span>msg<span class="token punctuation">)</span><span class="token punctuation">;</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		<span class="token comment">//消费者取消时的回调对象</span>
		CancelCallback cancel <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">CancelCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		ch<span class="token punctuation">.</span><span class="token function">basicConsume</span><span class="token punctuation">(</span>queueName<span class="token punctuation">,</span> <span class="token boolean">true</span><span class="token punctuation">,</span> callback<span class="token punctuation">,</span> cancel<span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h2><a id="_933"></a>路由模式</h2>
<p><img src="https://img-blog.csdnimg.cn/20191031165104402.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="路由模式"></p>
<p>在上一小节，我们构建了一个简单的日志系统。我们能够向多个接收者广播日志消息。</p>
<p>在这一节，我们将向其添加一个特性—我们将只订阅所有消息中的一部分。例如，我们只接收关键错误消息并保存到日志文件(以节省磁盘空间)，同时仍然能够在控制台上打印所有日志消息。</p>
<h3><a id="_Bindings_941"></a>绑定 Bindings</h3>
<p>在上一节，我们已经创建了队列与交换机的绑定。使用下面这样的代码:</p>
<pre><code class="prism language-java">ch<span class="token punctuation">.</span><span class="token function">queueBind</span><span class="token punctuation">(</span>queueName<span class="token punctuation">,</span> <span class="token string">"logs"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<p>绑定是交换机和队列之间的关系。这可以简单地理解为:队列对来自此交换的消息感兴趣。</p>
<p>绑定可以使用额外的routingKey参数。为了避免与basic_publish参数混淆，我们将其称为bindingKey。这是我们如何创建一个键绑定:</p>
<pre><code class="prism language-java">ch<span class="token punctuation">.</span><span class="token function">queueBind</span><span class="token punctuation">(</span>queueName<span class="token punctuation">,</span> EXCHANGE_NAME<span class="token punctuation">,</span> <span class="token string">"black"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<p>bindingKey的含义取决于交换机类型。我们前面使用的fanout交换机完全忽略它。</p>
<h3><a id="_Direct_exchange_958"></a>直连交换机 Direct exchange</h3>
<p>上一节中的日志系统向所有消费者广播所有消息。我们希望扩展它，允许根据消息的严重性过滤消息。例如，我们希望将日志消息写入磁盘的程序只接收关键error，而不是在warning或info日志消息上浪费磁盘空间。</p>
<p>前面我们使用的是fanout交换机，这并没有给我们太多的灵活性——它只能进行简单的广播。</p>
<p>我们将用直连交换机(Direct exchange)代替。它背后的路由算法很简单——消息传递到bindingKey与routingKey完全匹配的队列。为了说明这一点，请考虑以下设置</p>
<p><img src="https://img-blog.csdnimg.cn/20191031165146499.png" alt="路由模式"></p>
<p>其中我们可以看到直连交换机<code>X</code>，它绑定了两个队列。第一个队列用绑定键<code>orange</code>绑定，第二个队列有两个绑定，一个绑定<code>black</code>，另一个绑定键<code>green</code>。</p>
<p>这样设置，使用路由键<code>orange</code>发布到交换器的消息将被路由到队列Q1。带有<code>black</code>或<code>green</code>路由键的消息将转到<code>Q2</code>。而所有其他消息都将被丢弃。</p>
<h3><a id="_Multiple_bindings_972"></a>多重绑定 Multiple bindings</h3>
<p><img src="https://img-blog.csdnimg.cn/20191031165228781.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="多重绑定"></p>
<p>使用相同的bindingKey绑定多个队列是完全允许的。如图所示，可以使用binding key black将X与Q1和Q2绑定。在这种情况下，直连交换机的行为类似于fanout，并将消息广播给所有匹配的队列。一条路由键为black的消息将同时发送到Q1和Q2。</p>
<h3><a id="_978"></a>发送日志</h3>
<p>我们将在日志系统中使用这个模型。我们把消息发送到一个Direct交换机，而不是fanout。我们将提供日志级别作为routingKey。这样，接收程序将能够选择它希望接收的级别。让我们首先来看发出日志。</p>
<p>和前面一样，我们首先需要创建一个exchange:</p>
<pre><code class="prism language-java"><span class="token comment">//参数1: 交换机名</span>
<span class="token comment">//参数2: 交换机类型</span>
ch<span class="token punctuation">.</span><span class="token function">exchangeDeclare</span><span class="token punctuation">(</span><span class="token string">"direct_logs"</span><span class="token punctuation">,</span> <span class="token string">"direct"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<p>接着来看发送消息的代码</p>
<pre><code class="prism language-java"><span class="token comment">//参数1: 交换机名</span>
<span class="token comment">//参数2: routingKey, 路由键,这里我们用日志级别,如"error","info","warning"</span>
<span class="token comment">//参数3: 其他配置属性</span>
<span class="token comment">//参数4: 发布的消息数据 </span>
ch<span class="token punctuation">.</span><span class="token function">basicPublish</span><span class="token punctuation">(</span><span class="token string">"direct_logs"</span><span class="token punctuation">,</span> <span class="token string">"error"</span><span class="token punctuation">,</span> null<span class="token punctuation">,</span> message<span class="token punctuation">.</span><span class="token function">getBytes</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h3><a id="_1000"></a>订阅</h3>
<p>接收消息的工作原理与前面章节一样，但有一个例外——我们将为感兴趣的每个日志级别创建一个新的绑定, 示例代码如下:</p>
<pre><code class="prism language-java">ch<span class="token punctuation">.</span><span class="token function">queueBind</span><span class="token punctuation">(</span>queueName<span class="token punctuation">,</span> <span class="token string">"logs"</span><span class="token punctuation">,</span> <span class="token string">"info"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
ch<span class="token punctuation">.</span><span class="token function">queueBind</span><span class="token punctuation">(</span>queueName<span class="token punctuation">,</span> <span class="token string">"logs"</span><span class="token punctuation">,</span> <span class="token string">"warning"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h3><a id="_1009"></a>完整的代码</h3>
<p><img src="https://img-blog.csdnimg.cn/20191031165307357.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="完整代码"></p>
<h4><a id="_1013"></a>生产者</h4>
<pre><code class="prism language-java"><span class="token keyword">package</span> rabbitmq<span class="token punctuation">.</span>routing<span class="token punctuation">;</span>

<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>Random<span class="token punctuation">;</span>
<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>Scanner<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>BuiltinExchangeType<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Channel<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Connection<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>ConnectionFactory<span class="token punctuation">;</span>

<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">Test1</span> <span class="token punctuation">{</span>
	<span class="token keyword">public</span> <span class="token keyword">static</span> <span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span>String<span class="token punctuation">[</span><span class="token punctuation">]</span> args<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		String<span class="token punctuation">[</span><span class="token punctuation">]</span> a <span class="token operator">=</span> <span class="token punctuation">{</span><span class="token string">"warning"</span><span class="token punctuation">,</span> <span class="token string">"info"</span><span class="token punctuation">,</span> <span class="token string">"error"</span><span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		ConnectionFactory f <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ConnectionFactory</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setHost</span><span class="token punctuation">(</span><span class="token string">"192.168.64.140"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPort</span><span class="token punctuation">(</span><span class="token number">5672</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setUsername</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPassword</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		Connection c <span class="token operator">=</span> f<span class="token punctuation">.</span><span class="token function">newConnection</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		Channel ch <span class="token operator">=</span> c<span class="token punctuation">.</span><span class="token function">createChannel</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//参数1: 交换机名</span>
		<span class="token comment">//参数2: 交换机类型</span>
		ch<span class="token punctuation">.</span><span class="token function">exchangeDeclare</span><span class="token punctuation">(</span><span class="token string">"direct_logs"</span><span class="token punctuation">,</span> BuiltinExchangeType<span class="token punctuation">.</span>DIRECT<span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token keyword">while</span> <span class="token punctuation">(</span><span class="token boolean">true</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">print</span><span class="token punctuation">(</span><span class="token string">"输入消息: "</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			String msg <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Scanner</span><span class="token punctuation">(</span>System<span class="token punctuation">.</span>in<span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">nextLine</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			<span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token string">"exit"</span><span class="token punctuation">.</span><span class="token function">equals</span><span class="token punctuation">(</span>msg<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
				<span class="token keyword">break</span><span class="token punctuation">;</span>
			<span class="token punctuation">}</span>
			
			<span class="token comment">//随机产生日志级别</span>
			String level <span class="token operator">=</span> a<span class="token punctuation">[</span><span class="token keyword">new</span> <span class="token class-name">Random</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">nextInt</span><span class="token punctuation">(</span>a<span class="token punctuation">.</span>length<span class="token punctuation">)</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
			
			<span class="token comment">//参数1: 交换机名</span>
			<span class="token comment">//参数2: routingKey, 路由键,这里我们用日志级别,如"error","info","warning"</span>
			<span class="token comment">//参数3: 其他配置属性</span>
			<span class="token comment">//参数4: 发布的消息数据 </span>
			ch<span class="token punctuation">.</span><span class="token function">basicPublish</span><span class="token punctuation">(</span><span class="token string">"direct_logs"</span><span class="token punctuation">,</span> level<span class="token punctuation">,</span> null<span class="token punctuation">,</span> msg<span class="token punctuation">.</span><span class="token function">getBytes</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"消息已发送: "</span><span class="token operator">+</span>level<span class="token operator">+</span><span class="token string">" - "</span><span class="token operator">+</span>msg<span class="token punctuation">)</span><span class="token punctuation">;</span>
			
		<span class="token punctuation">}</span>

		c<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>

</code></pre>
<h4><a id="_1068"></a>消费者</h4>
<pre><code class="prism language-java"><span class="token keyword">package</span> rabbitmq<span class="token punctuation">.</span>routing<span class="token punctuation">;</span>

<span class="token keyword">import</span> java<span class="token punctuation">.</span>io<span class="token punctuation">.</span>IOException<span class="token punctuation">;</span>
<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>Scanner<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>BuiltinExchangeType<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>CancelCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Channel<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Connection<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>ConnectionFactory<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>DeliverCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Delivery<span class="token punctuation">;</span>

<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">Test2</span> <span class="token punctuation">{</span>
	<span class="token keyword">public</span> <span class="token keyword">static</span> <span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span>String<span class="token punctuation">[</span><span class="token punctuation">]</span> args<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		ConnectionFactory f <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ConnectionFactory</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setHost</span><span class="token punctuation">(</span><span class="token string">"192.168.64.140"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setUsername</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPassword</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		Connection c <span class="token operator">=</span> f<span class="token punctuation">.</span><span class="token function">newConnection</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		Channel ch <span class="token operator">=</span> c<span class="token punctuation">.</span><span class="token function">createChannel</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//定义名字为 direct_logs 的交换机, 它的类型是 "direct"</span>
		ch<span class="token punctuation">.</span><span class="token function">exchangeDeclare</span><span class="token punctuation">(</span><span class="token string">"direct_logs"</span><span class="token punctuation">,</span> BuiltinExchangeType<span class="token punctuation">.</span>DIRECT<span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//自动生成对列名,</span>
		<span class="token comment">//非持久,独占,自动删除</span>
		String queueName <span class="token operator">=</span> ch<span class="token punctuation">.</span><span class="token function">queueDeclare</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getQueue</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"输入接收的日志级别,用空格隔开:"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		String<span class="token punctuation">[</span><span class="token punctuation">]</span> a <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Scanner</span><span class="token punctuation">(</span>System<span class="token punctuation">.</span>in<span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">nextLine</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">split</span><span class="token punctuation">(</span><span class="token string">"\\s"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//把该队列,绑定到 direct_logs 交换机</span>
		<span class="token comment">//允许使用多个 bindingKey</span>
		<span class="token keyword">for</span> <span class="token punctuation">(</span>String level <span class="token operator">:</span> a<span class="token punctuation">)</span> <span class="token punctuation">{</span>
			ch<span class="token punctuation">.</span><span class="token function">queueBind</span><span class="token punctuation">(</span>queueName<span class="token punctuation">,</span> <span class="token string">"direct_logs"</span><span class="token punctuation">,</span> level<span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token punctuation">}</span>
		
		System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"等待接收数据"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//收到消息后用来处理消息的回调对象</span>
		DeliverCallback callback <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">DeliverCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">,</span> Delivery message<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
				String msg <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">String</span><span class="token punctuation">(</span>message<span class="token punctuation">.</span><span class="token function">getBody</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token string">"UTF-8"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
				String routingKey <span class="token operator">=</span> message<span class="token punctuation">.</span><span class="token function">getEnvelope</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getRoutingKey</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
				System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"收到: "</span><span class="token operator">+</span>routingKey<span class="token operator">+</span><span class="token string">" - "</span><span class="token operator">+</span>msg<span class="token punctuation">)</span><span class="token punctuation">;</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		<span class="token comment">//消费者取消时的回调对象</span>
		CancelCallback cancel <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">CancelCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		ch<span class="token punctuation">.</span><span class="token function">basicConsume</span><span class="token punctuation">(</span>queueName<span class="token punctuation">,</span> <span class="token boolean">true</span><span class="token punctuation">,</span> callback<span class="token punctuation">,</span> cancel<span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h2><a id="_1133"></a>主题模式</h2>
<p>在上一小节，我们改进了日志系统。我们没有使用只能进行广播的fanout交换机，而是使用Direct交换机，从而可以选择性接收日志。</p>
<p>虽然使用Direct交换机改进了我们的系统，但它仍然有局限性——它不能基于多个标准进行路由。</p>
<p>在我们的日志系统中，我们可能不仅希望根据级别订阅日志，还希望根据发出日志的源订阅日志。</p>
<p>这将给我们带来很大的灵活性——我们可能只想接收来自“cron”的关键错误，但也要接收来自“kern”的所有日志。</p>
<p>要在日志系统中实现这一点，我们需要了解更复杂的Topic交换机。</p>
<h3><a id="_Topic_exchange_1145"></a>主题交换机 Topic exchange</h3>
<p>发送到Topic交换机的消息,它的的routingKey,必须是由点分隔的多个单词。单词可以是任何东西，但通常是与消息相关的一些特性。几个有效的routingKey示例:“stock.usd.nyse”、“nyse.vmw”、“quick.orange.rabbit”。routingKey可以有任意多的单词，最多255个字节。</p>
<p>bindingKey也必须采用相同的形式。Topic交换机的逻辑与直连交换机类似——使用特定routingKey发送的消息将被传递到所有使用匹配bindingKey绑定的队列。bindingKey有两个重要的特殊点:</p>
<ul>
<li><code>*</code> 可以通配单个单词。</li>
<li><code>#</code> 可以通配零个或多个单词。</li>
</ul>
<p>用一个例子来解释这个问题是最简单的</p>
<p><img src="https://img-blog.csdnimg.cn/20191031165351156.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="主题"></p>
<p>在本例中，我们将发送描述动物的消息。这些消息将使用由三个单词(两个点)组成的routingKey发送。routingKey中的第一个单词表示速度，第二个是颜色,第三个是物种:“<code>&lt;速度&gt;.&lt;颜色&gt;.&lt;物种&gt;</code>”。</p>
<p>我们创建三个绑定:Q1与bindingKey  “<code>*.orange.*</code>” 绑定。和Q2是 “<code>*.*.rabbit</code>” 和 “<code>lazy.#</code>” 。</p>
<p>这些绑定可概括为:</p>
<ul>
<li>Q1对所有橙色的动物感兴趣。</li>
<li>Q2想接收关于兔子和慢速动物的所有消息。</li>
</ul>
<p>将routingKey设置为"<code>quick.orange.rabbit</code>"的消息将被发送到两个队列。消息 "<code>lazy.orange.elephant</code>“也发送到它们两个。另外”<code>quick.orange.fox</code>“只会发到第一个队列，”<code>lazy.brown.fox</code>“只发给第二个。”<code>lazy.pink.rabbit</code>“将只被传递到第二个队列一次，即使它匹配两个绑定。”<code>quick.brown.fox</code>"不匹配任何绑定，因此将被丢弃。</p>
<p>如果我们违反约定，发送一个或四个单词的信息，比如"<code>orange</code>“或”<code>quick.orange.male.rabbit</code>"，会发生什么?这些消息将不匹配任何绑定，并将丢失。</p>
<p>另外，"<code>lazy.orange.male.rabbit</code>"，即使它有四个单词，也将匹配最后一个绑定，并将被传递到第二个队列。</p>
<h3><a id="_1171"></a>完成的代码</h3>
<h4><a id="_1173"></a>生产者</h4>
<pre><code class="prism language-java"><span class="token keyword">package</span> rabbitmq<span class="token punctuation">.</span>topic<span class="token punctuation">;</span>

<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>Random<span class="token punctuation">;</span>
<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>Scanner<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>BuiltinExchangeType<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Channel<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Connection<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>ConnectionFactory<span class="token punctuation">;</span>

<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">Test1</span> <span class="token punctuation">{</span>
	<span class="token keyword">public</span> <span class="token keyword">static</span> <span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span>String<span class="token punctuation">[</span><span class="token punctuation">]</span> args<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		ConnectionFactory f <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ConnectionFactory</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setHost</span><span class="token punctuation">(</span><span class="token string">"192.168.64.140"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPort</span><span class="token punctuation">(</span><span class="token number">5672</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setUsername</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPassword</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		Connection c <span class="token operator">=</span> f<span class="token punctuation">.</span><span class="token function">newConnection</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		Channel ch <span class="token operator">=</span> c<span class="token punctuation">.</span><span class="token function">createChannel</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//参数1: 交换机名</span>
		<span class="token comment">//参数2: 交换机类型</span>
		ch<span class="token punctuation">.</span><span class="token function">exchangeDeclare</span><span class="token punctuation">(</span><span class="token string">"topic_logs"</span><span class="token punctuation">,</span> BuiltinExchangeType<span class="token punctuation">.</span>TOPIC<span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token keyword">while</span> <span class="token punctuation">(</span><span class="token boolean">true</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">print</span><span class="token punctuation">(</span><span class="token string">"输入消息: "</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			String msg <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Scanner</span><span class="token punctuation">(</span>System<span class="token punctuation">.</span>in<span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">nextLine</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			<span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token string">"exit"</span><span class="token punctuation">.</span><span class="token function">contentEquals</span><span class="token punctuation">(</span>msg<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
				<span class="token keyword">break</span><span class="token punctuation">;</span>
			<span class="token punctuation">}</span>
			System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">print</span><span class="token punctuation">(</span><span class="token string">"输入routingKey: "</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			String routingKey <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Scanner</span><span class="token punctuation">(</span>System<span class="token punctuation">.</span>in<span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">nextLine</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			
			<span class="token comment">//参数1: 交换机名</span>
			<span class="token comment">//参数2: routingKey, 路由键,这里我们用日志级别,如"error","info","warning"</span>
			<span class="token comment">//参数3: 其他配置属性</span>
			<span class="token comment">//参数4: 发布的消息数据 </span>
			ch<span class="token punctuation">.</span><span class="token function">basicPublish</span><span class="token punctuation">(</span><span class="token string">"topic_logs"</span><span class="token punctuation">,</span> routingKey<span class="token punctuation">,</span> null<span class="token punctuation">,</span> msg<span class="token punctuation">.</span><span class="token function">getBytes</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			
			System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"消息已发送: "</span><span class="token operator">+</span>routingKey<span class="token operator">+</span><span class="token string">" - "</span><span class="token operator">+</span>msg<span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token punctuation">}</span>

		c<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h4><a id="_1224"></a>消费者</h4>
<pre><code class="prism language-java"><span class="token keyword">package</span> rabbitmq<span class="token punctuation">.</span>topic<span class="token punctuation">;</span>

<span class="token keyword">import</span> java<span class="token punctuation">.</span>io<span class="token punctuation">.</span>IOException<span class="token punctuation">;</span>
<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>Scanner<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>BuiltinExchangeType<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>CancelCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Channel<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Connection<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>ConnectionFactory<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>DeliverCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Delivery<span class="token punctuation">;</span>

<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">Test2</span> <span class="token punctuation">{</span>
	<span class="token keyword">public</span> <span class="token keyword">static</span> <span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span>String<span class="token punctuation">[</span><span class="token punctuation">]</span> args<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		ConnectionFactory f <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ConnectionFactory</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setHost</span><span class="token punctuation">(</span><span class="token string">"192.168.64.140"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setUsername</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPassword</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		Connection c <span class="token operator">=</span> f<span class="token punctuation">.</span><span class="token function">newConnection</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		Channel ch <span class="token operator">=</span> c<span class="token punctuation">.</span><span class="token function">createChannel</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		ch<span class="token punctuation">.</span><span class="token function">exchangeDeclare</span><span class="token punctuation">(</span><span class="token string">"topic_logs"</span><span class="token punctuation">,</span> BuiltinExchangeType<span class="token punctuation">.</span>TOPIC<span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//自动生成对列名,</span>
		<span class="token comment">//非持久,独占,自动删除</span>
		String queueName <span class="token operator">=</span> ch<span class="token punctuation">.</span><span class="token function">queueDeclare</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getQueue</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"输入bindingKey,用空格隔开:"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		String<span class="token punctuation">[</span><span class="token punctuation">]</span> a <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Scanner</span><span class="token punctuation">(</span>System<span class="token punctuation">.</span>in<span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">nextLine</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">split</span><span class="token punctuation">(</span><span class="token string">"\\s"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//把该队列,绑定到 topic_logs 交换机</span>
		<span class="token comment">//允许使用多个 bindingKey</span>
		<span class="token keyword">for</span> <span class="token punctuation">(</span>String bindingKey <span class="token operator">:</span> a<span class="token punctuation">)</span> <span class="token punctuation">{</span>
			ch<span class="token punctuation">.</span><span class="token function">queueBind</span><span class="token punctuation">(</span>queueName<span class="token punctuation">,</span> <span class="token string">"topic_logs"</span><span class="token punctuation">,</span> bindingKey<span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token punctuation">}</span>
		
		System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"等待接收数据"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//收到消息后用来处理消息的回调对象</span>
		DeliverCallback callback <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">DeliverCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">,</span> Delivery message<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
				String msg <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">String</span><span class="token punctuation">(</span>message<span class="token punctuation">.</span><span class="token function">getBody</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token string">"UTF-8"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
				String routingKey <span class="token operator">=</span> message<span class="token punctuation">.</span><span class="token function">getEnvelope</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getRoutingKey</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
				System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"收到: "</span><span class="token operator">+</span>routingKey<span class="token operator">+</span><span class="token string">" - "</span><span class="token operator">+</span>msg<span class="token punctuation">)</span><span class="token punctuation">;</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		<span class="token comment">//消费者取消时的回调对象</span>
		CancelCallback cancel <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">CancelCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		ch<span class="token punctuation">.</span><span class="token function">basicConsume</span><span class="token punctuation">(</span>queueName<span class="token punctuation">,</span> <span class="token boolean">true</span><span class="token punctuation">,</span> callback<span class="token punctuation">,</span> cancel<span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h2><a id="RPC_1301"></a>RPC模式</h2>
<p>如果我们需要在远程电脑上运行一个方法，并且还要等待一个返回结果该怎么办？这和前面的例子不太一样, 这种模式我们通常称为远程过程调用,即RPC.</p>
<p>在本节中，我们将会学习使用RabbitMQ去搭建一个RPC系统：一个客户端和一个可以升级(扩展)的RPC服务器。为了模拟一个耗时任务，我们将创建一个返回斐波那契数列的虚拟的RPC服务。</p>
<h3><a id="_1307"></a>客户端</h3>
<p>在客户端定义一个RPCClient类,并定义一个call()方法,这个方法发送一个RPC请求,并等待接收响应结果</p>
<pre><code class="prism language-java">RPCClient client <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">RPCClient</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
String result <span class="token operator">=</span> client<span class="token punctuation">.</span><span class="token function">call</span><span class="token punctuation">(</span><span class="token string">"4"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span> <span class="token string">"第四个斐波那契数是: "</span> <span class="token operator">+</span> result<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h3><a id="_Callback_Queue_1317"></a>回调队列 Callback Queue</h3>
<p>使用RabbitMQ去实现RPC很容易。一个客户端发送请求信息，并得到一个服务器端回复的响应信息。为了得到响应信息，我们需要在请求的时候发送一个“回调”队列地址。我们可以使用默认队列。下面是示例代码：</p>
<pre><code class="prism language-java"><span class="token comment">//定义回调队列,</span>
<span class="token comment">//自动生成对列名,非持久,独占,自动删除</span>
callbackQueueName <span class="token operator">=</span> ch<span class="token punctuation">.</span><span class="token function">queueDeclare</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getQueue</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token comment">//用来设置回调队列的参数对象</span>
BasicProperties props <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">BasicProperties</span>
                            <span class="token punctuation">.</span><span class="token function">Builder</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
                            <span class="token punctuation">.</span><span class="token function">replyTo</span><span class="token punctuation">(</span>callbackQueueName<span class="token punctuation">)</span>
                            <span class="token punctuation">.</span><span class="token function">build</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token comment">//发送调用消息</span>
ch<span class="token punctuation">.</span><span class="token function">basicPublish</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">"rpc_queue"</span><span class="token punctuation">,</span> props<span class="token punctuation">,</span> message<span class="token punctuation">.</span><span class="token function">getBytes</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<blockquote>
<p>消息属性 Message Properties<br><br>
AMQP 0-9-1协议定义了消息的14个属性。大部分属性很少使用，下面是比较常用的4个:</p>
<p><code>deliveryMode</code>:将消息标记为持久化(值为2)或非持久化(任何其他值)。</p>
<p><code>contentType</code>:用于描述mime类型。例如，对于经常使用的JSON格式，将此属性设置为:<code>application/json</code>。</p>
<p><code>replyTo</code>:通常用于指定回调队列。</p>
<p><code>correlationId</code>:将RPC响应与请求关联起来非常有用。</p>
</blockquote>
<h3><a id="id_correlationId_1347"></a>关联id (correlationId)：</h3>
<p>在上面的代码中，我们会为每个RPC请求创建一个回调队列。 这是非常低效的，这里还有一个更好的方法:让我们为每个客户端创建一个回调队列。</p>
<p>这就提出了一个新的问题，在队列中得到一个响应时，我们不清楚这个响应所对应的是哪一条请求。这时候就需要使用关联id（correlationId）。我们将为每一条请求设置唯一的的id值。稍后，当我们在回调队列里收到一条消息的时候，我们将查看它的id属性，这样我们就可以匹配对应的请求和响应。如果我们发现了一个未知的id值，我们可以安全的丢弃这条消息，因为它不属于我们的请求。</p>
<h3><a id="_1353"></a>小结</h3>
<p><img src="https://img-blog.csdnimg.cn/20191031165433922.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="rpc"></p>
<p>RPC的工作方式是这样的:</p>
<ul>
<li>对于RPC请求，客户端发送一条带有两个属性的消息:replyTo,设置为仅为请求创建的匿名独占队列,和correlationId,设置为每个请求的惟一id值。</li>
<li>请求被发送到rpc_queue队列。</li>
<li>RPC工作进程(即:服务器)在队列上等待请求。当一个请求出现时，它执行任务,并使用replyTo字段中的队列将结果发回客户机。</li>
<li>客户机在回应消息队列上等待数据。当消息出现时，它检查correlationId属性。如果匹配请求中的值，则向程序返回该响应数据。</li>
</ul>
<h3><a id="_1364"></a>完成的代码</h3>
<h4><a id="_1366"></a>服务器端</h4>
<pre><code class="prism language-java"><span class="token keyword">package</span> rabbitmq<span class="token punctuation">.</span>rpc<span class="token punctuation">;</span>

<span class="token keyword">import</span> java<span class="token punctuation">.</span>io<span class="token punctuation">.</span>IOException<span class="token punctuation">;</span>
<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>Random<span class="token punctuation">;</span>
<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>Scanner<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>AMQP<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>BuiltinExchangeType<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>CancelCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Channel<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Connection<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>ConnectionFactory<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>DeliverCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Delivery<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>AMQP<span class="token punctuation">.</span>BasicProperties<span class="token punctuation">;</span>

<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">RPCServer</span> <span class="token punctuation">{</span>
	<span class="token keyword">public</span> <span class="token keyword">static</span> <span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span>String<span class="token punctuation">[</span><span class="token punctuation">]</span> args<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		ConnectionFactory f <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ConnectionFactory</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setHost</span><span class="token punctuation">(</span><span class="token string">"192.168.64.140"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPort</span><span class="token punctuation">(</span><span class="token number">5672</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setUsername</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPassword</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		Connection c <span class="token operator">=</span> f<span class="token punctuation">.</span><span class="token function">newConnection</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		Channel ch <span class="token operator">=</span> c<span class="token punctuation">.</span><span class="token function">createChannel</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token comment">/*
		 * 定义队列 rpc_queue, 将从它接收请求信息
		 * 
		 * 参数:
		 * 1. queue, 对列名
		 * 2. durable, 持久化
		 * 3. exclusive, 排他
		 * 4. autoDelete, 自动删除
		 * 5. arguments, 其他参数属性
		 */</span>
		ch<span class="token punctuation">.</span><span class="token function">queueDeclare</span><span class="token punctuation">(</span><span class="token string">"rpc_queue"</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span><span class="token boolean">false</span><span class="token punctuation">,</span>null<span class="token punctuation">)</span><span class="token punctuation">;</span>
		ch<span class="token punctuation">.</span><span class="token function">queuePurge</span><span class="token punctuation">(</span><span class="token string">"rpc_queue"</span><span class="token punctuation">)</span><span class="token punctuation">;</span><span class="token comment">//清除队列中的内容</span>
		
		ch<span class="token punctuation">.</span><span class="token function">basicQos</span><span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">;</span><span class="token comment">//一次只接收一条消息</span>
		
		
		<span class="token comment">//收到请求消息后的回调对象</span>
		DeliverCallback deliverCallback <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">DeliverCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">,</span> Delivery message<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
				<span class="token comment">//处理收到的数据(要求第几个斐波那契数)</span>
				String msg <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">String</span><span class="token punctuation">(</span>message<span class="token punctuation">.</span><span class="token function">getBody</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token string">"UTF-8"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
				<span class="token keyword">int</span> n <span class="token operator">=</span> Integer<span class="token punctuation">.</span><span class="token function">parseInt</span><span class="token punctuation">(</span>msg<span class="token punctuation">)</span><span class="token punctuation">;</span>
				<span class="token comment">//求出第n个斐波那契数</span>
				<span class="token keyword">int</span> r <span class="token operator">=</span> <span class="token function">fbnq</span><span class="token punctuation">(</span>n<span class="token punctuation">)</span><span class="token punctuation">;</span>
				String response <span class="token operator">=</span> String<span class="token punctuation">.</span><span class="token function">valueOf</span><span class="token punctuation">(</span>r<span class="token punctuation">)</span><span class="token punctuation">;</span>
				
				<span class="token comment">//设置发回响应的id, 与请求id一致, 这样客户端可以把该响应与它的请求进行对应</span>
				BasicProperties replyProps <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">BasicProperties<span class="token punctuation">.</span>Builder</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
						<span class="token punctuation">.</span><span class="token function">correlationId</span><span class="token punctuation">(</span>message<span class="token punctuation">.</span><span class="token function">getProperties</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getCorrelationId</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
						<span class="token punctuation">.</span><span class="token function">build</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
				<span class="token comment">/*
				 * 发送响应消息
				 * 1. 默认交换机
				 * 2. 由客户端指定的,用来传递响应消息的队列名
				 * 3. 参数(关联id)
				 * 4. 发回的响应消息
				 */</span>
				ch<span class="token punctuation">.</span><span class="token function">basicPublish</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span>message<span class="token punctuation">.</span><span class="token function">getProperties</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getReplyTo</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">,</span> replyProps<span class="token punctuation">,</span> response<span class="token punctuation">.</span><span class="token function">getBytes</span><span class="token punctuation">(</span><span class="token string">"UTF-8"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
				<span class="token comment">//发送确认消息</span>
				ch<span class="token punctuation">.</span><span class="token function">basicAck</span><span class="token punctuation">(</span>message<span class="token punctuation">.</span><span class="token function">getEnvelope</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getDeliveryTag</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token boolean">false</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		<span class="token comment">//</span>
		CancelCallback cancelCallback <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">CancelCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		<span class="token comment">//消费者开始接收消息, 等待从 rpc_queue接收请求消息, 不自动确认</span>
		ch<span class="token punctuation">.</span><span class="token function">basicConsume</span><span class="token punctuation">(</span><span class="token string">"rpc_queue"</span><span class="token punctuation">,</span> <span class="token boolean">false</span><span class="token punctuation">,</span> deliverCallback<span class="token punctuation">,</span> cancelCallback<span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>

	<span class="token keyword">protected</span> <span class="token keyword">static</span> <span class="token keyword">int</span> <span class="token function">fbnq</span><span class="token punctuation">(</span><span class="token keyword">int</span> n<span class="token punctuation">)</span> <span class="token punctuation">{</span>
		<span class="token keyword">if</span><span class="token punctuation">(</span>n <span class="token operator">==</span> <span class="token number">1</span> <span class="token operator">||</span> n <span class="token operator">==</span> <span class="token number">2</span><span class="token punctuation">)</span> <span class="token keyword">return</span> <span class="token number">1</span><span class="token punctuation">;</span>
		
		<span class="token keyword">return</span> <span class="token function">fbnq</span><span class="token punctuation">(</span>n<span class="token operator">-</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token operator">+</span><span class="token function">fbnq</span><span class="token punctuation">(</span>n<span class="token operator">-</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>

</code></pre>
<h4><a id="_1459"></a>客户端</h4>
<pre><code class="prism language-java"><span class="token keyword">package</span> rabbitmq<span class="token punctuation">.</span>rpc<span class="token punctuation">;</span>

<span class="token keyword">import</span> java<span class="token punctuation">.</span>io<span class="token punctuation">.</span>IOException<span class="token punctuation">;</span>
<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>Scanner<span class="token punctuation">;</span>
<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>UUID<span class="token punctuation">;</span>
<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>concurrent<span class="token punctuation">.</span>ArrayBlockingQueue<span class="token punctuation">;</span>
<span class="token keyword">import</span> java<span class="token punctuation">.</span>util<span class="token punctuation">.</span>concurrent<span class="token punctuation">.</span>BlockingQueue<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>BuiltinExchangeType<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>CancelCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Channel<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Connection<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>ConnectionFactory<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>DeliverCallback<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Delivery<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>AMQP<span class="token punctuation">.</span>BasicProperties<span class="token punctuation">;</span>

<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">RPCClient</span> <span class="token punctuation">{</span>
	Connection con<span class="token punctuation">;</span>
	Channel ch<span class="token punctuation">;</span>
	
	<span class="token keyword">public</span> <span class="token function">RPCClient</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		ConnectionFactory f <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ConnectionFactory</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setHost</span><span class="token punctuation">(</span><span class="token string">"192.168.64.140"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setUsername</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		f<span class="token punctuation">.</span><span class="token function">setPassword</span><span class="token punctuation">(</span><span class="token string">"admin"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		con <span class="token operator">=</span> f<span class="token punctuation">.</span><span class="token function">newConnection</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		ch <span class="token operator">=</span> con<span class="token punctuation">.</span><span class="token function">createChannel</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
	
	<span class="token keyword">public</span> String <span class="token function">call</span><span class="token punctuation">(</span>String msg<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		<span class="token comment">//自动生成对列名,非持久,独占,自动删除</span>
		String replyQueueName <span class="token operator">=</span> ch<span class="token punctuation">.</span><span class="token function">queueDeclare</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getQueue</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token comment">//生成关联id</span>
		String corrId <span class="token operator">=</span> UUID<span class="token punctuation">.</span><span class="token function">randomUUID</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">toString</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//设置两个参数:</span>
		<span class="token comment">//1. 请求和响应的关联id</span>
		<span class="token comment">//2. 传递响应数据的queue</span>
		BasicProperties props <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">BasicProperties<span class="token punctuation">.</span>Builder</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
				<span class="token punctuation">.</span><span class="token function">correlationId</span><span class="token punctuation">(</span>corrId<span class="token punctuation">)</span>
				<span class="token punctuation">.</span><span class="token function">replyTo</span><span class="token punctuation">(</span>replyQueueName<span class="token punctuation">)</span>
				<span class="token punctuation">.</span><span class="token function">build</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token comment">//向 rpc_queue 队列发送请求数据, 请求第n个斐波那契数</span>
		ch<span class="token punctuation">.</span><span class="token function">basicPublish</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">"rpc_queue"</span><span class="token punctuation">,</span> props<span class="token punctuation">,</span> msg<span class="token punctuation">.</span><span class="token function">getBytes</span><span class="token punctuation">(</span><span class="token string">"UTF-8"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//用来保存结果的阻塞集合,取数据时,没有数据会暂停等待</span>
		BlockingQueue<span class="token generics function"><span class="token punctuation">&lt;</span>String<span class="token punctuation">&gt;</span></span> response <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ArrayBlockingQueue</span><span class="token generics function"><span class="token punctuation">&lt;</span>String<span class="token punctuation">&gt;</span></span><span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		
		<span class="token comment">//接收响应数据的回调对象</span>
		DeliverCallback deliverCallback <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">DeliverCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">,</span> Delivery message<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
				<span class="token comment">//如果响应消息的关联id,与请求的关联id相同,我们来处理这个响应数据</span>
				<span class="token keyword">if</span> <span class="token punctuation">(</span>message<span class="token punctuation">.</span><span class="token function">getProperties</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getCorrelationId</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">contentEquals</span><span class="token punctuation">(</span>corrId<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
					<span class="token comment">//把收到的响应数据,放入阻塞集合</span>
					response<span class="token punctuation">.</span><span class="token function">offer</span><span class="token punctuation">(</span><span class="token keyword">new</span> <span class="token class-name">String</span><span class="token punctuation">(</span>message<span class="token punctuation">.</span><span class="token function">getBody</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token string">"UTF-8"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
				<span class="token punctuation">}</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>

		CancelCallback cancelCallback <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">CancelCallback</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			<span class="token annotation punctuation">@Override</span>
			<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">handle</span><span class="token punctuation">(</span>String consumerTag<span class="token punctuation">)</span> <span class="token keyword">throws</span> IOException <span class="token punctuation">{</span>
			<span class="token punctuation">}</span>
		<span class="token punctuation">}</span><span class="token punctuation">;</span>
		
		<span class="token comment">//开始从队列接收响应数据</span>
		ch<span class="token punctuation">.</span><span class="token function">basicConsume</span><span class="token punctuation">(</span>replyQueueName<span class="token punctuation">,</span> <span class="token boolean">true</span><span class="token punctuation">,</span> deliverCallback<span class="token punctuation">,</span> cancelCallback<span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token comment">//返回保存在集合中的响应数据</span>
		<span class="token keyword">return</span> response<span class="token punctuation">.</span><span class="token function">take</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
	
	<span class="token keyword">public</span> <span class="token keyword">static</span> <span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span>String<span class="token punctuation">[</span><span class="token punctuation">]</span> args<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		RPCClient client <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">RPCClient</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token keyword">while</span> <span class="token punctuation">(</span><span class="token boolean">true</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">print</span><span class="token punctuation">(</span><span class="token string">"求第几个斐波那契数:"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			<span class="token keyword">int</span> n <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Scanner</span><span class="token punctuation">(</span>System<span class="token punctuation">.</span>in<span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">nextInt</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			String r <span class="token operator">=</span> client<span class="token punctuation">.</span><span class="token function">call</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token operator">+</span>n<span class="token punctuation">)</span><span class="token punctuation">;</span>
			System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span>r<span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token punctuation">}</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>

</code></pre>
<h1><a id="virtual_host_1548"></a>virtual host</h1>
<p>在RabbitMQ中叫做虚拟消息服务器VirtualHost，每个VirtualHost相当于一个相对独立的RabbitMQ服务器，每个VirtualHost之间是相互隔离的。exchange、queue、message不能互通</p>
<h2><a id="virtual_host_pd_1552"></a>创建virtual host: <code>/pd</code></h2>
<ul>
<li>进入虚拟机管理界面</li>
</ul>
<p><img src="https://img-blog.csdnimg.cn/20191031165520956.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="虚拟主机"></p>
<ul>
<li>添加新的虚拟机’/pd’,名称必须以"/"开头</li>
</ul>
<p><img src="https://img-blog.csdnimg.cn/20191031213231475.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="虚拟主机"></p>
<ul>
<li>查看添加的结果</li>
</ul>
<p><img src="https://img-blog.csdnimg.cn/20191031213346166.png" alt="结果"></p>
<h2><a id="_1567"></a>设置虚拟机的用户访问权限</h2>
<p>点击 /pd 虚拟主机, 设置用户 admin 对它的访问权限</p>
<p><img src="https://img-blog.csdnimg.cn/20191031213443737.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="权限"></p>
<h1><a id="_rabbitmq_1573"></a>拼多商城整合 rabbitmq</h1>
<p>当用户下订单时,我们的业务系统直接与数据库通信,把订单保存到数据库中</p>
<p>当系统流量突然激增,大量的订单压力,会拖慢业务系统和数据库系统</p>
<p>我们需要应对流量峰值,让流量曲线变得平缓,如下图</p>
<p><img src="https://img-blog.csdnimg.cn/20191031213522745.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="削峰"></p>
<h2><a id="_1583"></a>订单存储的解耦</h2>
<p>为了进行流量削峰,我们引入 rabbitmq 消息队列,当购物系统产生订单后,可以把订单数据发送到消息队列;而订单消费者应用从消息队列接收订单消息,并把订单保存到数据库</p>
<p><img src="https://img-blog.csdnimg.cn/20191031213656661.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl8zODMwNTQ0MA==,size_16,color_FFFFFF,t_70" alt="订单"></p>
<p>这样,当流量激增时,大量订单会暂存在rabbitmq中,而订单消费者可以从容地从消息队列慢慢接收订单,向数据库保存</p>
<h2><a id="_1591"></a>生产者-发送订单</h2>
<h3><a id="pomxml__1593"></a>pom.xml 添加依赖</h3>
<p>spring提供了更方便的消息队列访问接口,它对RabbitMQ的客户端API进行了封装,使用起来更加方便</p>
<pre><code class="prism language-xml"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>dependency</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>groupId</span><span class="token punctuation">&gt;</span></span>org.springframework.boot<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>groupId</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>artifactId</span><span class="token punctuation">&gt;</span></span>spring-boot-starter-amqp<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>artifactId</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>dependency</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<h3><a id="applicationyml_1604"></a>application.yml</h3>
<p>添加RabbitMQ的连接信息</p>
<pre><code class="prism language-yml"><span class="token key atrule">spring</span><span class="token punctuation">:</span>
  <span class="token key atrule">rabbitmq</span><span class="token punctuation">:</span>
    <span class="token key atrule">host</span><span class="token punctuation">:</span> 192.168.64.140
    <span class="token key atrule">port</span><span class="token punctuation">:</span> <span class="token number">5672</span>
    <span class="token key atrule">virtualHost</span><span class="token punctuation">:</span> /pd
    <span class="token key atrule">username</span><span class="token punctuation">:</span> admin
    <span class="token key atrule">password</span><span class="token punctuation">:</span> admin

</code></pre>
<h3><a id="_RunPdAPP_1619"></a>修改主程序 RunPdAPP</h3>
<p>在主程序中添加下面的方法创建Queue实例</p>
<p>当创建RabbitMQ连接和信道后,Spring的RabbitMQ工具会自动在服务器中创建队列,代码在<code>RabbitAdmin.declareQueues()</code>方法中</p>
<pre><code class="prism language-java">	<span class="token annotation punctuation">@Bean</span>
	<span class="token keyword">public</span> Queue <span class="token function">getQueue</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
		Queue q <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Queue</span><span class="token punctuation">(</span><span class="token string">"orderQueue"</span><span class="token punctuation">,</span> <span class="token boolean">true</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token keyword">return</span> q<span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
</code></pre>
<h3><a id="_OrderServiceImpl_1633"></a>修改 OrderServiceImpl</h3>
<pre><code class="prism language-java">	<span class="token comment">//RabbitAutoConfiguration中创建了AmpqTemplate实例</span>
	<span class="token annotation punctuation">@Autowired</span>
	AmqpTemplate amqpTemplate<span class="token punctuation">;</span>

    <span class="token comment">//saveOrder原来的数据库访问代码全部注释,添加rabbitmq消息发送代码</span>
	<span class="token keyword">public</span> String <span class="token function">saveOrder</span><span class="token punctuation">(</span>PdOrder pdOrder<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		String orderId <span class="token operator">=</span> <span class="token function">generateId</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		pdOrder<span class="token punctuation">.</span><span class="token function">setOrderId</span><span class="token punctuation">(</span>orderId<span class="token punctuation">)</span><span class="token punctuation">;</span>

		amqpTemplate<span class="token punctuation">.</span><span class="token function">convertAndSend</span><span class="token punctuation">(</span><span class="token string">"orderQueue"</span><span class="token punctuation">,</span> pdOrder<span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token keyword">return</span> orderId<span class="token punctuation">;</span>

		
		<span class="token comment">//		String orderId = generateId();</span>
		<span class="token comment">//		pdOrder.setOrderId(orderId);</span>
		<span class="token comment">//</span>
		<span class="token comment">//		</span>
		<span class="token comment">//		PdShipping pdShipping = pdShippingMapper.selectByPrimaryKey(pdOrder.getAddId());</span>
		<span class="token comment">//		pdOrder.setShippingName(pdShipping.getReceiverName());</span>
		<span class="token comment">//		pdOrder.setShippingCode(pdShipping.getReceiverAddress());</span>
		<span class="token comment">//		pdOrder.setStatus(1);// </span>
		<span class="token comment">//		pdOrder.setPaymentType(1);</span>
		<span class="token comment">//		pdOrder.setPostFee(10D);</span>
		<span class="token comment">//		pdOrder.setCreateTime(new Date());</span>
		<span class="token comment">//</span>
		<span class="token comment">//		double payment = 0;</span>
		<span class="token comment">//		List&lt;ItemVO&gt; itemVOs = selectCartItemByUseridAndItemIds(pdOrder.getUserId(), pdOrder.getItemIdList());</span>
		<span class="token comment">//		for (ItemVO itemVO : itemVOs) {</span>
		<span class="token comment">//			PdOrderItem pdOrderItem = new PdOrderItem();</span>
		<span class="token comment">//			String id = generateId();</span>
		<span class="token comment">//			//String id="2";</span>
		<span class="token comment">//			pdOrderItem.setId(id);</span>
		<span class="token comment">//			pdOrderItem.setOrderId(orderId);</span>
		<span class="token comment">//			pdOrderItem.setItemId("" + itemVO.getPdItem().getId());</span>
		<span class="token comment">//			pdOrderItem.setTitle(itemVO.getPdItem().getTitle());</span>
		<span class="token comment">//			pdOrderItem.setPrice(itemVO.getPdItem().getPrice());</span>
		<span class="token comment">//			pdOrderItem.setNum(itemVO.getPdCartItem().getNum());</span>
		<span class="token comment">//</span>
		<span class="token comment">//			payment = payment + itemVO.getPdCartItem().getNum() * itemVO.getPdItem().getPrice();</span>
		<span class="token comment">//			pdOrderItemMapper.insert(pdOrderItem);</span>
		<span class="token comment">//		}</span>
		<span class="token comment">//		pdOrder.setPayment(payment);</span>
		<span class="token comment">//		pdOrderMapper.insert(pdOrder);</span>
		<span class="token comment">//		return orderId;</span>
	<span class="token punctuation">}</span>

</code></pre>
<h2><a id="_1684"></a>消费者-接收订单,并保存到数据库</h2>
<h3><a id="pdwebpdorderconsumer_1686"></a>pd-web项目复制为pd-order-consumer</h3>
<p><img src="https://img-blog.csdnimg.cn/2019103121375010.png" alt="复制项目"></p>
<h3><a id="_applicationyml_1690"></a>修改 application.yml</h3>
<p>把端口修改成 81</p>
<pre><code class="prism language-yml"><span class="token key atrule">server</span><span class="token punctuation">:</span>
  <span class="token key atrule">port</span><span class="token punctuation">:</span> <span class="token number">81</span>

<span class="token key atrule">spring</span><span class="token punctuation">:</span>
  <span class="token key atrule">datasource</span><span class="token punctuation">:</span>
    <span class="token key atrule">type</span><span class="token punctuation">:</span> com.alibaba.druid.pool.DruidDataSource
    <span class="token key atrule">driver-class-name</span><span class="token punctuation">:</span> com.mysql.jdbc.Driver
    <span class="token key atrule">url</span><span class="token punctuation">:</span> jdbc<span class="token punctuation">:</span>mysql<span class="token punctuation">:</span>//localhost<span class="token punctuation">:</span>3306/pd_store<span class="token punctuation">?</span>useUnicode=true<span class="token important">&amp;characterEncoding</span>=utf8
    <span class="token key atrule">username</span><span class="token punctuation">:</span> root
    <span class="token key atrule">password</span><span class="token punctuation">:</span> root

  <span class="token key atrule">rabbitmq</span><span class="token punctuation">:</span>
    <span class="token key atrule">host</span><span class="token punctuation">:</span> 192.168.64.140
    <span class="token key atrule">port</span><span class="token punctuation">:</span> <span class="token number">5672</span>
    <span class="token key atrule">virtualHost</span><span class="token punctuation">:</span> /pd
    <span class="token key atrule">username</span><span class="token punctuation">:</span> admin
    <span class="token key atrule">password</span><span class="token punctuation">:</span> admin

<span class="token key atrule">mybatis</span><span class="token punctuation">:</span>
  <span class="token comment">#typeAliasesPackage: cn.tedu.ssm.pojo</span>
  <span class="token key atrule">mapperLocations</span><span class="token punctuation">:</span> classpath<span class="token punctuation">:</span>com.pd.mapper/*.xml

<span class="token key atrule">logging</span><span class="token punctuation">:</span>
  <span class="token key atrule">level</span><span class="token punctuation">:</span> 
    <span class="token key atrule">cn.tedu.ssm.mapper</span><span class="token punctuation">:</span> debug
</code></pre>
<h3><a id="_1722"></a>删除无关代码</h3>
<p>pd-order-consumer项目只需要从 RabbitMQ 接收订单数据, 再保存到数据库即可, 所以项目中只需要保留这部分代码</p>
<ul>
<li>删除 com.pd.controller 包</li>
<li>删除 com.pd.payment.utils 包</li>
<li>删除无关的 Service,只保留 OrderService 和 OrderServiceImpl</li>
</ul>
<h3><a id="_OrderConsumer_1730"></a>新建 OrderConsumer</h3>
<pre><code class="prism language-java"><span class="token keyword">package</span> com<span class="token punctuation">.</span>pd<span class="token punctuation">;</span>

<span class="token keyword">import</span> org<span class="token punctuation">.</span>springframework<span class="token punctuation">.</span>amqp<span class="token punctuation">.</span>rabbit<span class="token punctuation">.</span>annotation<span class="token punctuation">.</span>RabbitListener<span class="token punctuation">;</span>
<span class="token keyword">import</span> org<span class="token punctuation">.</span>springframework<span class="token punctuation">.</span>beans<span class="token punctuation">.</span>factory<span class="token punctuation">.</span>annotation<span class="token punctuation">.</span>Autowired<span class="token punctuation">;</span>
<span class="token keyword">import</span> org<span class="token punctuation">.</span>springframework<span class="token punctuation">.</span>stereotype<span class="token punctuation">.</span>Component<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>pd<span class="token punctuation">.</span>pojo<span class="token punctuation">.</span>PdOrder<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>pd<span class="token punctuation">.</span>service<span class="token punctuation">.</span>OrderService<span class="token punctuation">;</span>

<span class="token annotation punctuation">@Component</span>
<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">OrderConsumer</span> <span class="token punctuation">{</span>
    <span class="token comment">//收到订单数据后,会调用订单的业务代码,把订单保存到数据库</span>
	<span class="token annotation punctuation">@Autowired</span>
	<span class="token keyword">private</span> OrderService orderService<span class="token punctuation">;</span>

    <span class="token comment">//添加该注解后,会从指定的orderQueue接收消息,</span>
    <span class="token comment">//并把数据转为 PdOrder 实例传递到此方法</span>
	<span class="token annotation punctuation">@RabbitListener</span><span class="token punctuation">(</span>queues<span class="token operator">=</span><span class="token string">"orderQueue"</span><span class="token punctuation">)</span>
	<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">save</span><span class="token punctuation">(</span>PdOrder pdOrder<span class="token punctuation">)</span>
	<span class="token punctuation">{</span>
		System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"消费者"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span>pdOrder<span class="token punctuation">.</span><span class="token function">toString</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token keyword">try</span> <span class="token punctuation">{</span>
			orderService<span class="token punctuation">.</span><span class="token function">saveOrder</span><span class="token punctuation">(</span>pdOrder<span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token punctuation">}</span> <span class="token keyword">catch</span> <span class="token punctuation">(</span><span class="token class-name">Exception</span> e<span class="token punctuation">)</span> <span class="token punctuation">{</span>
			e<span class="token punctuation">.</span><span class="token function">printStackTrace</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token punctuation">}</span>
	<span class="token punctuation">}</span>

<span class="token punctuation">}</span>
</code></pre>
<h3><a id="_OrderServiceImpl__saveOrder__1765"></a>修改 OrderServiceImpl 的 saveOrder() 方法</h3>
<pre><code class="prism language-java">	<span class="token keyword">public</span> String <span class="token function">saveOrder</span><span class="token punctuation">(</span>PdOrder pdOrder<span class="token punctuation">)</span> <span class="token keyword">throws</span> Exception <span class="token punctuation">{</span>
		<span class="token comment">//		String orderId = generateId();</span>
		<span class="token comment">//		pdOrder.setOrderId(orderId);</span>
		<span class="token comment">//</span>
		<span class="token comment">//		amqpTemplate.convertAndSend("orderQueue", pdOrder);</span>
		<span class="token comment">//		return orderId;</span>
		<span class="token comment">//</span>
		<span class="token comment">//		</span>
		<span class="token comment">//		</span>
		<span class="token comment">//		String orderId = generateId();</span>
		<span class="token comment">//		pdOrder.setOrderId(orderId);</span>
		
		<span class="token comment">//从RabbitMQ接收的订单数据,</span>
		<span class="token comment">//已经在上游订单业务中生成过id,这里不再重新生成id</span>
		<span class="token comment">//直接获取该订单的id</span>
		String orderId <span class="token operator">=</span> pdOrder<span class="token punctuation">.</span><span class="token function">getOrderId</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

		
		PdShipping pdShipping <span class="token operator">=</span> pdShippingMapper<span class="token punctuation">.</span><span class="token function">selectByPrimaryKey</span><span class="token punctuation">(</span>pdOrder<span class="token punctuation">.</span><span class="token function">getAddId</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		pdOrder<span class="token punctuation">.</span><span class="token function">setShippingName</span><span class="token punctuation">(</span>pdShipping<span class="token punctuation">.</span><span class="token function">getReceiverName</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		pdOrder<span class="token punctuation">.</span><span class="token function">setShippingCode</span><span class="token punctuation">(</span>pdShipping<span class="token punctuation">.</span><span class="token function">getReceiverAddress</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		pdOrder<span class="token punctuation">.</span><span class="token function">setStatus</span><span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">;</span><span class="token comment">// </span>
		pdOrder<span class="token punctuation">.</span><span class="token function">setPaymentType</span><span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		pdOrder<span class="token punctuation">.</span><span class="token function">setPostFee</span><span class="token punctuation">(</span><span class="token number">10D</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		pdOrder<span class="token punctuation">.</span><span class="token function">setCreateTime</span><span class="token punctuation">(</span><span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

		<span class="token keyword">double</span> payment <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
		List<span class="token generics function"><span class="token punctuation">&lt;</span>ItemVO<span class="token punctuation">&gt;</span></span> itemVOs <span class="token operator">=</span> <span class="token function">selectCartItemByUseridAndItemIds</span><span class="token punctuation">(</span>pdOrder<span class="token punctuation">.</span><span class="token function">getUserId</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">,</span> pdOrder<span class="token punctuation">.</span><span class="token function">getItemIdList</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token keyword">for</span> <span class="token punctuation">(</span>ItemVO itemVO <span class="token operator">:</span> itemVOs<span class="token punctuation">)</span> <span class="token punctuation">{</span>
			PdOrderItem pdOrderItem <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">PdOrderItem</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			String id <span class="token operator">=</span> <span class="token function">generateId</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			<span class="token comment">//String id="2";</span>
			pdOrderItem<span class="token punctuation">.</span><span class="token function">setId</span><span class="token punctuation">(</span>id<span class="token punctuation">)</span><span class="token punctuation">;</span>
			pdOrderItem<span class="token punctuation">.</span><span class="token function">setOrderId</span><span class="token punctuation">(</span>orderId<span class="token punctuation">)</span><span class="token punctuation">;</span>
			pdOrderItem<span class="token punctuation">.</span><span class="token function">setItemId</span><span class="token punctuation">(</span><span class="token string">""</span> <span class="token operator">+</span> itemVO<span class="token punctuation">.</span><span class="token function">getPdItem</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getId</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			pdOrderItem<span class="token punctuation">.</span><span class="token function">setTitle</span><span class="token punctuation">(</span>itemVO<span class="token punctuation">.</span><span class="token function">getPdItem</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getTitle</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			pdOrderItem<span class="token punctuation">.</span><span class="token function">setPrice</span><span class="token punctuation">(</span>itemVO<span class="token punctuation">.</span><span class="token function">getPdItem</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getPrice</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			pdOrderItem<span class="token punctuation">.</span><span class="token function">setNum</span><span class="token punctuation">(</span>itemVO<span class="token punctuation">.</span><span class="token function">getPdCartItem</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getNum</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

			payment <span class="token operator">=</span> payment <span class="token operator">+</span> itemVO<span class="token punctuation">.</span><span class="token function">getPdCartItem</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getNum</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">*</span> itemVO<span class="token punctuation">.</span><span class="token function">getPdItem</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getPrice</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
			pdOrderItemMapper<span class="token punctuation">.</span><span class="token function">insert</span><span class="token punctuation">(</span>pdOrderItem<span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token punctuation">}</span>
		pdOrder<span class="token punctuation">.</span><span class="token function">setPayment</span><span class="token punctuation">(</span>payment<span class="token punctuation">)</span><span class="token punctuation">;</span>
		pdOrderMapper<span class="token punctuation">.</span><span class="token function">insert</span><span class="token punctuation">(</span>pdOrder<span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token keyword">return</span> orderId<span class="token punctuation">;</span>
	<span class="token punctuation">}</span>   
</code></pre>
<h2><a id="_1816"></a>手动确认</h2>
<h3><a id="applicationyml_1818"></a>application.yml</h3>
<pre><code class="prism language-yml"><span class="token key atrule">spring</span><span class="token punctuation">:</span>
  <span class="token key atrule">rabbitmq</span><span class="token punctuation">:</span>
    <span class="token key atrule">listener</span><span class="token punctuation">:</span>
      <span class="token key atrule">simple</span><span class="token punctuation">:</span>
        <span class="token key atrule">acknowledge-mode</span><span class="token punctuation">:</span> manual
</code></pre>
<h3><a id="OrderConsumer_1828"></a>OrderConsumer</h3>
<pre><code class="prism language-java"><span class="token keyword">package</span> com<span class="token punctuation">.</span>pd<span class="token punctuation">;</span>

<span class="token keyword">import</span> org<span class="token punctuation">.</span>springframework<span class="token punctuation">.</span>amqp<span class="token punctuation">.</span>core<span class="token punctuation">.</span>Message<span class="token punctuation">;</span>
<span class="token keyword">import</span> org<span class="token punctuation">.</span>springframework<span class="token punctuation">.</span>amqp<span class="token punctuation">.</span>rabbit<span class="token punctuation">.</span>annotation<span class="token punctuation">.</span>RabbitListener<span class="token punctuation">;</span>
<span class="token keyword">import</span> org<span class="token punctuation">.</span>springframework<span class="token punctuation">.</span>beans<span class="token punctuation">.</span>factory<span class="token punctuation">.</span>annotation<span class="token punctuation">.</span>Autowired<span class="token punctuation">;</span>
<span class="token keyword">import</span> org<span class="token punctuation">.</span>springframework<span class="token punctuation">.</span>stereotype<span class="token punctuation">.</span>Component<span class="token punctuation">;</span>

<span class="token keyword">import</span> com<span class="token punctuation">.</span>pd<span class="token punctuation">.</span>pojo<span class="token punctuation">.</span>PdOrder<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>pd<span class="token punctuation">.</span>service<span class="token punctuation">.</span>OrderService<span class="token punctuation">;</span>
<span class="token keyword">import</span> com<span class="token punctuation">.</span>rabbitmq<span class="token punctuation">.</span>client<span class="token punctuation">.</span>Channel<span class="token punctuation">;</span>

<span class="token annotation punctuation">@Component</span>
<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">OrderConsumer</span> <span class="token punctuation">{</span>
    <span class="token comment">//收到订单数据后,会调用订单的业务代码,把订单保存到数据库</span>
	<span class="token annotation punctuation">@Autowired</span>
	<span class="token keyword">private</span> OrderService orderService<span class="token punctuation">;</span>

    <span class="token comment">//添加该注解后,会从指定的orderQueue接收消息,</span>
    <span class="token comment">//并把数据转为 PdOrder 实例传递到此方法</span>
	<span class="token annotation punctuation">@RabbitListener</span><span class="token punctuation">(</span>queues<span class="token operator">=</span><span class="token string">"orderQueue"</span><span class="token punctuation">)</span>
	<span class="token keyword">public</span> <span class="token keyword">void</span> <span class="token function">save</span><span class="token punctuation">(</span>PdOrder pdOrder<span class="token punctuation">,</span> Channel channel<span class="token punctuation">,</span> Message message<span class="token punctuation">)</span>
	<span class="token punctuation">{</span>
		System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"消费者"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span>pdOrder<span class="token punctuation">.</span><span class="token function">toString</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token keyword">try</span> <span class="token punctuation">{</span>
			orderService<span class="token punctuation">.</span><span class="token function">saveOrder</span><span class="token punctuation">(</span>pdOrder<span class="token punctuation">)</span><span class="token punctuation">;</span>
			channel<span class="token punctuation">.</span><span class="token function">basicAck</span><span class="token punctuation">(</span>message<span class="token punctuation">.</span><span class="token function">getMessageProperties</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getDeliveryTag</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token boolean">false</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token punctuation">}</span> <span class="token keyword">catch</span> <span class="token punctuation">(</span><span class="token class-name">Exception</span> e<span class="token punctuation">)</span> <span class="token punctuation">{</span>
			e<span class="token punctuation">.</span><span class="token function">printStackTrace</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
		<span class="token punctuation">}</span> 
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

                                    </div>
                <link href="https://csdnimg.cn/release/phoenix/mdeditor/markdown_views-b6c3c6d139.css" rel="stylesheet">
                                                <div class="more-toolbox">
                <div class="left-toolbox">
                    <ul class="toolbox-list">
                        
                        <li class="tool-item tool-active is-like "><a href="javascript:;"><svg class="icon" aria-hidden="true">
                            <use xlink:href="#csdnc-thumbsup"></use>
                        </svg><span class="name">点赞</span>
                        <span class="count">75</span>
                        </a></li>
                        <li class="tool-item tool-active is-collection "><a href="javascript:;" data-report-click='{"mod":"popu_824"}'><svg class="icon" aria-hidden="true">
                            <use xlink:href="#icon-csdnc-Collection-G" ></use>
                        </svg><span class="name">收藏</span></a></li>
                        <li class="tool-item tool-active is-share"><a href="javascript:;"><svg class="icon" aria-hidden="true">
                            <use xlink:href="#icon-csdnc-fenxiang"></use>
                        </svg>分享</a></li>
                        <!--打赏开始-->
                                                <!--打赏结束-->
                                                <li class="tool-item tool-more">
                            <a>
                            <svg t="1575545411852" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="5717" xmlns:xlink="http://www.w3.org/1999/xlink" width="200" height="200"><defs><style type="text/css"></style></defs><path d="M179.176 499.222m-113.245 0a113.245 113.245 0 1 0 226.49 0 113.245 113.245 0 1 0-226.49 0Z" p-id="5718"></path><path d="M509.684 499.222m-113.245 0a113.245 113.245 0 1 0 226.49 0 113.245 113.245 0 1 0-226.49 0Z" p-id="5719"></path><path d="M846.175 499.222m-113.245 0a113.245 113.245 0 1 0 226.49 0 113.245 113.245 0 1 0-226.49 0Z" p-id="5720"></path></svg>
                            </a>
                            <ul class="more-box">
                                <li class="item"><a class="article-report">文章举报</a></li>
                            </ul>
                        </li>
                                            </ul>
                </div>
                            </div>
            <div class="person-messagebox">
                <div class="left-message"><a href="https://blog.csdn.net/weixin_38305440">
                    <img src="https://profile.csdnimg.cn/7/4/5/3_weixin_38305440" class="avatar_pic" username='weixin_38305440'>
                                            <img src="https://g.csdnimg.cn/static/user-reg-year/1x/3.png" class="user-years">
                                    </a></div>
                <div class="middle-message">
                                        <div class="title"><span class="tit"><a href="https://blog.csdn.net/weixin_38305440" data-report-click='{"mod":"popu_379"}' target="_blank">Wanght6</a></span>
                                            </div>
                    <div class="text"><span>发布了11 篇原创文章</span> · <span>获赞 619</span> · <span>访问量 7万+</span></div>
                </div>
                                <div class="right-message">
                                            <a href=https://im.csdn.net/im/main.html?userName=weixin_38305440 target="_blank" 
                            class="btn btn-sm btn-red-hollow bt-button personal-letter">私信
                        </a>
                                                            <a class="btn btn-sm attented bt-button personal-watch" data-report-click='{"mod":"popu_379"}'>已关注</a>
                                    </div>
                            </div>
                    </div>
    </article>
    
</div>


                        <div class="hide-article-box hide-article-pos text-center">
                <a class="btn-readmore" data-report-view='{"mod":"popu_376","dest":"https://blog.csdn.net/weixin_38305440/article/details/102810522","strategy":"fans-readmore"}' data-report-click='{"mod":"popu_376","dest":"https://blog.csdn.net/weixin_38305440/article/details/102810522","strategy":"fans-readmore"}'>
                    关注博主即可阅读全文
                    <svg class="icon chevrondown" aria-hidden="true">
                        <use xlink:href="#csdnc-chevrondown"></use>
                    </svg>
                </a>
            </div>
            <script>
    $("#blog_detail_zk_collection").click(function(){
        window.csdn.articleCollection()
    })
</script>

            <div class="recommend-box"><div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/kebi007/article/details/104164570","strategy":"BlogCommendFromMachineLearnPai2","index":"0"}'>
	<div class="content">
		<a href="https://blog.csdn.net/kebi007/article/details/104164570" target="_blank"  rel="noopener" title="为什么说程序员做外包没前途？">
		<h4 class="text-truncate oneline">
				为什么说程序员做外包没前途？		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-03</span>
				<span class="read-num hover-hide">
					阅读数 
					2万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/kebi007/article/details/104164570" target="_blank" rel="noopener" title="为什么说程序员做外包没前途？">
				<span class="desc oneline">之前做过不到3个月的外包，2020的第一天就被释放了，2019年还剩1天，我从外包公司离职了。我就谈谈我个人的看法吧。首先我们定义一下什么是有前途	稳定的工作环境			不错的收入			能够在项目中不断...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/kebi007">来自：	<span class="blog_title"> dotNet全栈开发</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
</div>            
            <a id="commentBox" name="commentBox"></a>
<div class="comment-box">
	<div class="comment-edit-box d-flex">
		<a id="commentsedit"></a>
		<div class="user-img">
			<a href="//me.csdn.net/k826240369" target="_blank" rel="noopener">
				<img class="" src="https://profile.csdnimg.cn/B/B/2/3_k826240369">
			</a>
		</div>
		<form id="commentform">
			<input type="hidden" id="comment_replyId">
			<textarea class="comment-content" name="comment_content" id="comment_content" placeholder="想对作者说点什么" maxlength="1000"></textarea>
			<div class="opt-box"> <!-- d-flex -->
				<div id="ubbtools" class="add_code">
					<a href="#insertcode" code="code" target="_self"><i class="icon iconfont icon-daima"></i></a>
				</div>
				<input type="hidden" id="comment_replyId" name="comment_replyId">
				<input type="hidden" id="article_id" name="article_id" value="102810522">
				<input type="hidden" id="comment_userId" name="comment_userId" value="">
				<input type="hidden" id="commentId" name="commentId" value="">
				<div style="display: none;" class="csdn-tracking-statistics tracking-click" data-report-click='{"mod":"popu_384","dest":""}'><a href="#" target="_blank" class="comment_area_btn" rel="noopener">发表评论</a></div>
				<div class="dropdown" id="myDrap">
					<a class="dropdown-face d-flex align-items-center" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">
					<div class="txt-selected text-truncate">添加代码片</div>
					<svg class="icon d-block" aria-hidden="true">
						<use xlink:href="#csdnc-triangledown"></use>
					</svg>
					</a>
					<ul class="dropdown-menu" id="commentCode" aria-labelledby="drop4">
						<li><a data-code="html">HTML/XML</a></li>
						<li><a data-code="objc">objective-c</a></li>
						<li><a data-code="ruby">Ruby</a></li>
						<li><a data-code="php">PHP</a></li>
						<li><a data-code="csharp">C</a></li>
						<li><a data-code="cpp">C++</a></li>
						<li><a data-code="javascript">JavaScript</a></li>
						<li><a data-code="python">Python</a></li>
						<li><a data-code="java">Java</a></li>
						<li><a data-code="css">CSS</a></li>
						<li><a data-code="sql">SQL</a></li>
						<li><a data-code="plain">其它</a></li>
					</ul>
				</div>  
				<div class="right-box">
                                            <span class="tip">评论将由博主筛选后显示，对所有人可见 |</span>
                                        <span id="tip_comment" class="tip">还能输入<em>1000</em>个字符</span>
					<input type="button" class="btn btn-sm btn-cancel d-none" value="取消回复">
					<input type="submit" class="btn btn-sm btn-red btn-comment" value="发表评论">
				</div>
			</div>
		</form>
	</div>

	<div class="comment-list-container">
		<a id="comments"></a>
		<div class="comment-list-box">
		</div>
		<div id="commentPage" class="pagination-box d-none"></div>
		<div class="opt-box text-center">
			<div class="btn btn-sm btn-link-blue" id="btnMoreComment"></div>
		</div>
	</div>
</div>
            <div class="recommend-box">
                                    <div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_33701617/article/details/91738017","strategy":"BlogCommendFromMachineLearnPai2","index":"1"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_33701617/article/details/91738017" target="_blank"  rel="noopener" title="RabbitMQ：从零开始">
		<h4 class="text-truncate oneline">
				<em>RabbitMQ</em>：从零开始		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">04-24</span>
				<span class="read-num hover-hide">
					阅读数 
					47</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_33701617/article/details/91738017" target="_blank" rel="noopener" title="RabbitMQ：从零开始">
				<span class="desc oneline">为什么80%的码农都做不了架构师？&gt;&gt;&gt;                                                         ......</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_33701617">来自：	<span class="blog_title"> weixin_33701617的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/hustspy1990/article/details/102989305","strategy":"BlogCommendFromMachineLearnPai2","index":"2"}'>
	<div class="content">
		<a href="https://blog.csdn.net/hustspy1990/article/details/102989305" target="_blank"  rel="noopener" title="Nginx 原理和架构">
		<h4 class="text-truncate oneline">
				Nginx 原理和架构		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">11-09</span>
				<span class="read-num hover-hide">
					阅读数 
					4万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/hustspy1990/article/details/102989305" target="_blank" rel="noopener" title="Nginx 原理和架构">
				<span class="desc oneline">Nginx 是一个免费的，开源的，高性能的 HTTP 服务器和反向代理，以及 IMAP / POP3 代理服务器。Nginx 以其高性能，稳定性，丰富的功能，简单的配置和低资源消耗而闻名。Nginx ...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/hustspy1990">来自：	<span class="blog_title"> albon arith</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_41674620/article/details/81356703","strategy":"BlogCommendFromMachineLearnPai2","index":"3"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_41674620/article/details/81356703" target="_blank"  rel="noopener" title="十分钟看懂RabbitMQ">
		<h4 class="text-truncate oneline">
				十分钟看懂<em>RabbitMQ</em>		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">08-02</span>
				<span class="read-num hover-hide">
					阅读数 
					229</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_41674620/article/details/81356703" target="_blank" rel="noopener" title="十分钟看懂RabbitMQ">
				<span class="desc oneline">一、什么是RabbitMQ： rabbitmq是一种遵循AMQP协议，由Erlang语言开发的，消息传递的消息队列系统。二、简单理解 　学过websocket的来理解rabbitMQ应该是非常简单的了...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_41674620">来自：	<span class="blog_title"> weixin_41674620的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	<div class="recommend-item-box recommend-recommend-box"><div id="kp_box_59" data-pid="59"><script type="text/javascript">
    (function() {
        var s = "_" + Math.random().toString(36).slice(2);
        document.write('<div style="" id="' + s + '"></div>');
        (window.slotbydup = window.slotbydup || []).push({
            id: "u3491668",
            container:  s
        });
    })();
</script>
<!-- 多条广告如下脚本只需引入一次 -->
<script type="text/javascript" src="//cpro.baidustatic.com/cpro/ui/c.js" async="async" defer="defer" ></script><img class="pre-img-lasy" data-src="https://kunyu.csdn.net/1.png?p=59&a=78&c=0&k=&d=1&t=3&u=a5d6a509ede540eebe2dfdf34b484ca7"></div></div>
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/csdnnews/article/details/102548475","strategy":"BlogCommendFromMachineLearnPai2","index":"4"}'>
	<div class="content">
		<a href="https://blog.csdn.net/csdnnews/article/details/102548475" target="_blank"  rel="noopener" title="为什么程序员在学习编程的时候什么都记不住？">
		<h4 class="text-truncate oneline">
				为什么程序员在学习编程的时候什么都记不住？		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">10-12</span>
				<span class="read-num hover-hide">
					阅读数 
					5万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/csdnnews/article/details/102548475" target="_blank" rel="noopener" title="为什么程序员在学习编程的时候什么都记不住？">
				<span class="desc oneline">在程序员的职业生涯中，记住所有你接触过的代码是一件不可能的事情！那么我们该如何解决这一问题？作者 |Dylan Mestyanek译者 | 弯月，责编 | 屠敏出品 | CSDN（ID：CSDNnew...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/csdnnews">来自：	<span class="blog_title"> CSDN资讯</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/xianaoshi/article/details/103248846","strategy":"BlogCommendFromMachineLearnPai2","index":"5"}'>
	<div class="content">
		<a href="https://blog.csdn.net/xianaoshi/article/details/103248846" target="_blank"  rel="noopener" title="互联网公司的裁员，能玩出多少种花样？">
		<h4 class="text-truncate oneline">
				互联网公司的裁员，能玩出多少种花样？		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">11-25</span>
				<span class="read-num hover-hide">
					阅读数 
					3万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/xianaoshi/article/details/103248846" target="_blank" rel="noopener" title="互联网公司的裁员，能玩出多少种花样？">
				<span class="desc oneline">裁员，也是一门学问，可谓博大精深！以下，是互联网公司的裁员的多种方法：-正文开始-135岁+不予续签的理由：千禧一代网感更强。95后不予通过试用期的理由：已婚已育员工更有责任心。2通知接下来要过苦日子...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/xianaoshi">来自：	<span class="blog_title"> 吓脑湿</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/yuanziok/article/details/103198266","strategy":"BlogCommendFromMachineLearnPai2","index":"6"}'>
	<div class="content">
		<a href="https://blog.csdn.net/yuanziok/article/details/103198266" target="_blank"  rel="noopener" title="腾讯架构师，为了家庭去小厂，一个月后主动离职：不做中台就是等死">
		<h4 class="text-truncate oneline">
				腾讯架构师，为了家庭去小厂，一个月后主动离职：不做中台就是等死		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">11-22</span>
				<span class="read-num hover-hide">
					阅读数 
					2万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/yuanziok/article/details/103198266" target="_blank" rel="noopener" title="腾讯架构师，为了家庭去小厂，一个月后主动离职：不做中台就是等死">
				<span class="desc oneline">今天咱们第一课，来讲讲大家一直很关注的数据中台。其实，数据中台也是企业数据管理的一部分，甚至可以说是很重要的一部分。一、什么是中台？这其实是一个老生常谈的概念了，中台，顾名思义，就是在起中间作用的东西...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/yuanziok">来自：	<span class="blog_title"> Leo的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/qq_40630246/article/details/102643196","strategy":"BlogCommendFromMachineLearnPai2","index":"7"}'>
	<div class="content">
		<a href="https://blog.csdn.net/qq_40630246/article/details/102643196" target="_blank"  rel="noopener" title="c++制作的植物大战僵尸，开源，一代二代结合游戏">
		<h4 class="text-truncate oneline">
				c++制作的植物大战僵尸，开源，一代二代结合游戏		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">01-10</span>
				<span class="read-num hover-hide">
					阅读数 
					2万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/qq_40630246/article/details/102643196" target="_blank" rel="noopener" title="c++制作的植物大战僵尸，开源，一代二代结合游戏">
				<span class="desc oneline">此游戏全部由本人自己制作完成。游戏大部分的素材来源于原版游戏素材，少部分搜集于网络，以及自己制作。 此游戏为同人游戏而且仅供学习交流使用，任何人未经授权，不得对本游戏进行更改、盗用等，否则后果自负。目...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/qq_40630246">来自：	<span class="blog_title"> 尔灵尔亿的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/shawn210/article/details/80968805","strategy":"BlogCommendFromMachineLearnPai2","index":"8"}'>
	<div class="content">
		<a href="https://blog.csdn.net/shawn210/article/details/80968805" target="_blank"  rel="noopener" title="RabbitMQ安装">
		<h4 class="text-truncate oneline">
				<em>RabbitMQ</em>安装		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">07-09</span>
				<span class="read-num hover-hide">
					阅读数 
					1067</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/shawn210/article/details/80968805" target="_blank" rel="noopener" title="RabbitMQ安装">
				<span class="desc oneline">RabbitMQRabbitMQ官方网站：传送门RabbitMQ下载网站：下载传送门  系统  centos7  RabbitMQ  3.7.7  Erlang  19.3+安装RabbitMQ需要e...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/shawn210">来自：	<span class="blog_title"> ZYXW的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	<div class="recommend-item-box recommend-recommend-box"><div id="kp_box_60" data-pid="60"><script type="text/javascript">
        (function() {
            var s = "_" + Math.random().toString(36).slice(2);
            document.write('<div style="" id="' + s + '"></div>');
            (window.slotbydup = window.slotbydup || []).push({
                id: "u3502456",
                container: s
            });
        })();
</script>
<!-- 多条广告如下脚本只需引入一次 -->
<script type="text/javascript" src="//cpro.baidustatic.com/cpro/ui/c.js" async="async" defer="defer" >
</script><img class="pre-img-lasy" data-src="https://kunyu.csdn.net/1.png?p=60&a=763&c=0&k=&d=1&t=3&u=2902262e229b4e6b93d755177e677e2d"></div></div>
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_43493955/article/details/83304768","strategy":"BlogCommendFromMachineLearnPai2","index":"9"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_43493955/article/details/83304768" target="_blank"  rel="noopener" title="安装RabbitMQ各种踩坑详细教程">
		<h4 class="text-truncate oneline">
				安装<em>RabbitMQ</em>各种踩坑详细教程		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">10-23</span>
				<span class="read-num hover-hide">
					阅读数 
					2035</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_43493955/article/details/83304768" target="_blank" rel="noopener" title="安装RabbitMQ各种踩坑详细教程">
				<span class="desc oneline">第一步：安装RabbitMQ，首先要安装Erlang  我下载的版本是 OTP21.1官网地址：[Erlang地址]    (http://www.erlang.org/downloads)下载之后是...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_43493955">来自：	<span class="blog_title"> weixin_43493955的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_30666401/article/details/95735293","strategy":"BlogCommendFromMachineLearnPai2","index":"10"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_30666401/article/details/95735293" target="_blank"  rel="noopener" title="RabbitMQ-官方指南－RabbitMQ配置">
		<h4 class="text-truncate oneline">
				<em>RabbitMQ</em>-官方指南－<em>RabbitMQ</em>配置		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">08-04</span>
				<span class="read-num hover-hide">
					阅读数 
					64</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_30666401/article/details/95735293" target="_blank" rel="noopener" title="RabbitMQ-官方指南－RabbitMQ配置">
				<span class="desc oneline">原文：http://www.rabbitmq.com/configure.htmlRabbitMQ 提供了三种方式来定制服务器:环境变量定义端口，文件位置和名称(接受shell输入,或者在环境配置文件...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_30666401">来自：	<span class="blog_title"> weixin_30666401的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
			<div class="recommend-item-box blog-expert-recommend-box">
			<div class="d-flex">
				<div class="blog-expert-recommend">
					<div class="blog-expert">
						<div class="blog-expert-flexbox"></div>
					</div>
				</div>
			</div>
		</div>
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_43189126/article/details/89446386","strategy":"BlogCommendFromMachineLearnPai2","index":"11"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_43189126/article/details/89446386" target="_blank"  rel="noopener" title="RabbitMQ采坑笔记">
		<h4 class="text-truncate oneline">
				<em>RabbitMQ</em>采坑笔记		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">04-24</span>
				<span class="read-num hover-hide">
					阅读数 
					382</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_43189126/article/details/89446386" target="_blank" rel="noopener" title="RabbitMQ采坑笔记">
				<span class="desc oneline">QueueingConsumer过时QueueingConsumer在Rabbitmq客户端3.x版本中用的如火如荼，但是在4.x版本开初就被标记为@Deprecated。Consumer的消费模式有...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_43189126">来自：	<span class="blog_title"> weixin_43189126的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_44564365/article/details/87097367","strategy":"BlogCommendFromMachineLearnPai2","index":"12"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_44564365/article/details/87097367" target="_blank"  rel="noopener" title="RabbitMQ的用法整合">
		<h4 class="text-truncate oneline">
				<em>RabbitMQ</em>的用法整合		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-12</span>
				<span class="read-num hover-hide">
					阅读数 
					104</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_44564365/article/details/87097367" target="_blank" rel="noopener" title="RabbitMQ的用法整合">
				<span class="desc oneline">MQ的作用：解耦：在项目启动之初是很难预测未来会遇到什么困难的，消息中间件在处理过程中插入了一个隐含的，基于数据的接口层，两边都实现这个接口，这样就允许独立的修改或者扩展两边的处理过程，只要两边遵守相...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_44564365">来自：	<span class="blog_title"> weixin_44564365的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_42763504/article/details/81604600","strategy":"BlogCommendFromMachineLearnPai2","index":"13"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_42763504/article/details/81604600" target="_blank"  rel="noopener" title="RabbitMQ高级特性">
		<h4 class="text-truncate oneline">
				<em>RabbitMQ</em>高级特性		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">08-12</span>
				<span class="read-num hover-hide">
					阅读数 
					1136</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_42763504/article/details/81604600" target="_blank" rel="noopener" title="RabbitMQ高级特性">
				<span class="desc oneline">一.消息如何保证100%的投递成功1. 生产端的可靠性投递(1)保障消息的成功发出(2)保障MQ节点的成功接收(3)发送端收到MQ节点确认应答(4)完善的消息进行补偿机制2. 解决方案(1)消息落库，...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_42763504">来自：	<span class="blog_title"> weixin_42763504的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	<div class="recommend-item-box recommend-recommend-box"><div id="kp_box_61" data-pid="61"><script type="text/javascript">
        (function() {
            var s = "_" + Math.random().toString(36).slice(2);
            document.write('<div style="" id="' + s + '"></div>');
            (window.slotbydup = window.slotbydup || []).push({
                id: "u3565309",
                container: s
            });
        })();
</script>
<!-- 多条广告如下脚本只需引入一次 -->
<script type="text/javascript" src="//cpro.baidustatic.com/cpro/ui/c.js" async="async" defer="defer" >
</script><img class="pre-img-lasy" data-src="https://kunyu.csdn.net/1.png?p=61&a=622&c=0&k=&d=1&t=3&u=c74d14e1e81b4706b1d1f712028f4f1c"></div></div>
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/yulianlin/article/details/102784772","strategy":"BlogCommendFromMachineLearnPai2","index":"14"}'>
	<div class="content">
		<a href="https://blog.csdn.net/yulianlin/article/details/102784772" target="_blank"  rel="noopener" title="管理程序员的第三年，给大家的一些建议">
		<h4 class="text-truncate oneline">
				管理程序员的第三年，给大家的一些建议		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">10-28</span>
				<span class="read-num hover-hide">
					阅读数 
					1万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/yulianlin/article/details/102784772" target="_blank" rel="noopener" title="管理程序员的第三年，给大家的一些建议">
				<span class="desc oneline">我是三年前从一名普通程序员转型成为部门负责人。11024是2的10次方，今年的10月24日也是网上公认的第五个程序员节日，前几天还专门组织了部门员工庆祝了程序员节日，和我们部门的程序员讲了下自己的心得...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/yulianlin">来自：	<span class="blog_title"> 于连林520wcf的专栏</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/wangnan9279/article/details/54694976","strategy":"BlogCommendFromMachineLearnPai2","index":"15"}'>
	<div class="content">
		<a href="https://blog.csdn.net/wangnan9279/article/details/54694976" target="_blank"  rel="noopener" title="rabbitMQ 命令">
		<h4 class="text-truncate oneline">
				<em>rabbitMQ</em> 命令		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">01-23</span>
				<span class="read-num hover-hide">
					阅读数 
					1382</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/wangnan9279/article/details/54694976" target="_blank" rel="noopener" title="rabbitMQ 命令">
				<span class="desc oneline">启动RabbitMQ Server/etc/init.d/rabbitmq-serverstart  或  service rabbitmq-service start  Rabbitmq服务器的主要...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/wangnan9279">来自：	<span class="blog_title"> Ghost Stories</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/PanJianlei1990/article/details/102416858","strategy":"BlogCommendFromMachineLearnPai2","index":"16"}'>
	<div class="content">
		<a href="https://blog.csdn.net/PanJianlei1990/article/details/102416858" target="_blank"  rel="noopener" title="2019年10月中国编程语言排行榜">
		<h4 class="text-truncate oneline">
				2019年10月中国编程语言排行榜		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">10-08</span>
				<span class="read-num hover-hide">
					阅读数 
					1万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/PanJianlei1990/article/details/102416858" target="_blank" rel="noopener" title="2019年10月中国编程语言排行榜">
				<span class="desc oneline">2019年10月2日，我统计了某招聘网站，获得有效程序员招聘数据9万条。针对招聘信息，提取编程语言关键字，并统计如下：编程语言比例rankpl_percentage1java33.54%2cpp16....</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/PanJianlei1990">来自：	<span class="blog_title"> 毛毛虫</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_30478923/article/details/95208312","strategy":"BlogCommendFromMachineLearnPai2","index":"17"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_30478923/article/details/95208312" target="_blank"  rel="noopener" title="MQ使用:apollo和rabbitmq">
		<h4 class="text-truncate oneline">
				MQ使用:apollo和<em>rabbitmq</em>		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">03-14</span>
				<span class="read-num hover-hide">
					阅读数 
					117</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_30478923/article/details/95208312" target="_blank" rel="noopener" title="MQ使用:apollo和rabbitmq">
				<span class="desc oneline">apolloapollo 是一个更快、更可靠、更容易维护的消息代理，它是由最初的ActiveMQ的基础构建的。它使用一个完全不同的线程和消息调度架构来实现这一点。与ActiveMQ一样，apollo ...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_30478923">来自：	<span class="blog_title"> weixin_30478923的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_34068198/article/details/91367759","strategy":"BlogCommendFromMachineLearnPai2","index":"18"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_34068198/article/details/91367759" target="_blank"  rel="noopener" title="关于RabbitMq你必须深入理解的内容">
		<h4 class="text-truncate oneline">
				关于<em>RabbitMq</em>你必须深入理解的内容		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">03-23</span>
				<span class="read-num hover-hide">
					阅读数 
					333</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_34068198/article/details/91367759" target="_blank" rel="noopener" title="关于RabbitMq你必须深入理解的内容">
				<span class="desc oneline">关于RabbitMq你必须深入理解的内容前言这里主要想整理关于消息队列rabbitmq可能遇到问题，躺一躺其中的坑，然后在团队沉淀下来，最终变为整个团队的技术能力，然后写着写着发现，官方文档写的都比较...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_34068198">来自：	<span class="blog_title"> weixin_34068198的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	<div class="recommend-item-box recommend-recommend-box"><div id="kp_box_62" data-pid="62"><script type="text/javascript">
        (function() {
            var s = "_" + Math.random().toString(36).slice(2);
            document.write('<div style="" id="' + s + '"></div>');
            (window.slotbydup = window.slotbydup || []).push({
                id: "u3565311",
                container: s
            });
        })();
</script>
<!-- 多条广告如下脚本只需引入一次 -->
<script type="text/javascript" src="//cpro.baidustatic.com/cpro/ui/c.js" async="async" defer="defer" >
</script><img class="pre-img-lasy" data-src="https://kunyu.csdn.net/1.png?p=62&a=623&c=0&k=&d=1&t=3&u=a32842d4606a4cb39c7dce059f5c4f04"></div></div>
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/huster1446/article/details/101542085","strategy":"BlogCommendFromMachineLearnPai2","index":"19"}'>
	<div class="content">
		<a href="https://blog.csdn.net/huster1446/article/details/101542085" target="_blank"  rel="noopener" title="字节跳动视频编解码面经">
		<h4 class="text-truncate oneline">
				字节跳动视频编解码面经		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">11-20</span>
				<span class="read-num hover-hide">
					阅读数 
					11万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/huster1446/article/details/101542085" target="_blank" rel="noopener" title="字节跳动视频编解码面经">
				<span class="desc oneline">三四月份投了字节跳动的实习（图形图像岗位），然后hr打电话过来问了一下会不会opengl，c++，shador，当时只会一点c++，其他两个都不会，也就直接被拒了。七月初内推了字节跳动的提前批，因为内...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/huster1446">来自：	<span class="blog_title"> ljh_shuai的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_30889885/article/details/96469978","strategy":"BlogCommendFromMachineLearnPai2","index":"20"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_30889885/article/details/96469978" target="_blank"  rel="noopener" title="RabbitMQ的五种工作方式详细">
		<h4 class="text-truncate oneline">
				<em>RabbitMQ</em>的五种工作方式详细		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">07-13</span>
				<span class="read-num hover-hide">
					阅读数 
					88</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_30889885/article/details/96469978" target="_blank" rel="noopener" title="RabbitMQ的五种工作方式详细">
				<span class="desc oneline">在了解之前得先有个RabbitMQ客户端.官网： https://www.rabbitmq.com/getstarted.htmlconnections：无论生产者还是消费者，都需要与RabbitMQ...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_30889885">来自：	<span class="blog_title"> weixin_30889885的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/lantian_123/article/details/103172069","strategy":"BlogCommendFromMachineLearnPai2","index":"21"}'>
	<div class="content">
		<a href="https://blog.csdn.net/lantian_123/article/details/103172069" target="_blank"  rel="noopener" title="so easy！ 10行代码写个&quot;狗屁不通&quot;文章生成器">
		<h4 class="text-truncate oneline">
				so easy！ 10行代码写个&quot;狗屁不通&quot;文章生成器		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">11-20</span>
				<span class="read-num hover-hide">
					阅读数 
					9万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/lantian_123/article/details/103172069" target="_blank" rel="noopener" title="so easy！ 10行代码写个&quot;狗屁不通&quot;文章生成器">
				<span class="desc oneline">前几天，GitHub 有个开源项目特别火，只要输入标题就可以生成一篇长长的文章。背后实现代码一定很复杂吧，里面一定有很多高深莫测的机器学习等复杂算法不过，当我看了源代码之后这程序不到50行尽管我有多年...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/lantian_123">来自：	<span class="blog_title"> Python之禅的专栏</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_34348805/article/details/93638207","strategy":"BlogCommendFromMachineLearnPai2","index":"22"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_34348805/article/details/93638207" target="_blank"  rel="noopener" title="RabbitMQ后台管理界面">
		<h4 class="text-truncate oneline">
				<em>RabbitMQ</em>后台管理界面		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">05-10</span>
				<span class="read-num hover-hide">
					阅读数 
					433</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_34348805/article/details/93638207" target="_blank" rel="noopener" title="RabbitMQ后台管理界面">
				<span class="desc oneline">　　打开后台界面：http://localhost:15672/#/ 右上角可以设置页面&quot;刷新时间&quot;。以及选择监听的&quot;虚拟主机&quot;。界面有&quot;概要&quot;、&quot;连接&quot;、&quot;通道&quot;、&quot;分发器&quot;、&quot;队列&quot;、&quot;用户&quot;等几...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_34348805">来自：	<span class="blog_title"> weixin_34348805的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_42763504/article/details/81608237","strategy":"BlogCommendFromMachineLearnPai2","index":"23"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_42763504/article/details/81608237" target="_blank"  rel="noopener" title="RabbitMQ高级整合应用">
		<h4 class="text-truncate oneline">
				<em>RabbitMQ</em>高级整合应用		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">08-13</span>
				<span class="read-num hover-hide">
					阅读数 
					2544</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_42763504/article/details/81608237" target="_blank" rel="noopener" title="RabbitMQ高级整合应用">
				<span class="desc oneline">一.RabbitMQ整合Spring AMQP1.RabbitAdmin(1)RabbitAdmin类可以很好的操作RabbitMQ，在Spring中直接进行注入即可(2)autoStartup必须设...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_42763504">来自：	<span class="blog_title"> weixin_42763504的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	<div class="recommend-item-box recommend-recommend-box"><div id="kp_box_63" data-pid="63"><div id="three_ad23" class="mediav_ad" ></div>
<script type="text/javascript" src="//static.mediav.com/js/mvf_news_feed.js"></script>
<script>
                                               NEWS_FEED({
                w: 852,
                h : 60,
                showid : 'GNKXx7',
                placeholderId: "three_ad23",
                inject : 'define',
                define : {
                    imagePosition : 'left',
                    imageBorderRadius : 3,
                    imageWidth: 90,
                    imageHeight: 60,
                    imageFill : 'clip',
                    displayImage : true,
                    displayTitle : true,
                    titleFontSize: 18,
                    titleFontColor: '#000',
                    titleFontFamily : 'Lato,-apple-system,SF UI Text,Arial,PingFang SC,Hiragino Sans GB,Microsoft YaHei,WenQuanYi Micro Hei,sans-serif',
                    titleFontWeight: 'bold',
                    titlePaddingTop : 0,
                    titlePaddingRight : 0,
                    titlePaddingBottom : 5,
                    titlePaddingLeft : 16,
                    displayDesc : true,
                    descFontSize: 14,
                    descFontColor: '#8e959a',
                    descFontFamily : 'Microsoft Yahei',
                    paddingTop : 0,
                    paddingRight : 0,
                    paddingBottom : 0,
                    paddingLeft : 0,
                    backgroundColor: '#fff',
                    hoverColor: '#000'
                      }
                  })
                                        </script><img class="pre-img-lasy" data-src="https://kunyu.csdn.net/1.png?p=63&a=555&c=0&k=&d=1&t=3&u=fa1fbe3729be4510b4ded9e8edd0ecca"></div></div>
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/aoreng9439/article/details/101815981","strategy":"BlogCommendFromMachineLearnPai2","index":"24"}'>
	<div class="content">
		<a href="https://blog.csdn.net/aoreng9439/article/details/101815981" target="_blank"  rel="noopener" title="RabbitMQ封装实战">
		<h4 class="text-truncate oneline">
				<em>RabbitMQ</em>封装实战		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">04-01</span>
				<span class="read-num hover-hide">
					阅读数 
					17</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/aoreng9439/article/details/101815981" target="_blank" rel="noopener" title="RabbitMQ封装实战">
				<span class="desc oneline">先说下背景：上周开始给项目添加曾经没有过的消息中间件。虽然说，一路到头非常容易，直接google，万事不愁~可是生活远不仅是眼前的“苟且”。首先是想使用其他项目使用过的一套对mq封装的框架，融合进来。...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/aoreng9439">来自：	<span class="blog_title"> aoreng9439的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/qq_40693171/article/details/100716766","strategy":"BlogCommendFromMachineLearnPai2","index":"25"}'>
	<div class="content">
		<a href="https://blog.csdn.net/qq_40693171/article/details/100716766" target="_blank"  rel="noopener" title="我花了一夜用数据结构给女朋友写个H5走迷宫游戏">
		<h4 class="text-truncate oneline">
				我花了一夜用数据结构给女朋友写个H5走迷宫游戏		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">09-21</span>
				<span class="read-num hover-hide">
					阅读数 
					37万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/qq_40693171/article/details/100716766" target="_blank" rel="noopener" title="我花了一夜用数据结构给女朋友写个H5走迷宫游戏">
				<span class="desc oneline">起因又到深夜了，我按照以往在csdn和公众号写着数据结构！这占用了我大量的时间！我的超越妹妹严重缺乏陪伴而 怨气满满！而女朋友时常埋怨，认为数据结构这么抽象难懂的东西没啥作用，常会问道：天天写这玩意，...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/qq_40693171">来自：	<span class="blog_title"> bigsai</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_33690367/article/details/91685935","strategy":"BlogCommendFromMachineLearnPai2","index":"26"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_33690367/article/details/91685935" target="_blank"  rel="noopener" title="重磅发布-RabbitMQ实战系列完整视频教程">
		<h4 class="text-truncate oneline">
				重磅发布-<em>RabbitMQ</em>实战系列完整视频教程		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">09-04</span>
				<span class="read-num hover-hide">
					阅读数 
					28</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_33690367/article/details/91685935" target="_blank" rel="noopener" title="重磅发布-RabbitMQ实战系列完整视频教程">
				<span class="desc oneline">概要介绍：历经一个多月的时间，我录制的RabbitMQ实战系列完整视频教程终于出世了！在本课程中，我将带领大家一窥消息中间件RabbitMQ的容貌，并将学到的知识要点实战到实际的应用场景中。本课程将分...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_33690367">来自：	<span class="blog_title"> weixin_33690367的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_33716941/article/details/90324587","strategy":"BlogCommendFromMachineLearnPai2","index":"27"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_33716941/article/details/90324587" target="_blank"  rel="noopener" title="学会查看 RabbitMQ日志">
		<h4 class="text-truncate oneline">
				学会查看 <em>RabbitMQ</em>日志		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">07-09</span>
				<span class="read-num hover-hide">
					阅读数 
					330</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_33716941/article/details/90324587" target="_blank" rel="noopener" title="学会查看 RabbitMQ日志">
				<span class="desc oneline">如果在使用RabbitMQ的过程中出现了异常情况，通过翻阅RabbitMQ的服务日志可以让你在处理异常的过程中事半功倍。RabbitMQ日志中会有明确的事件日期、事件内容以及事件等级等。RabbitM...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_33716941">来自：	<span class="blog_title"> weixin_33716941的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_33860528/article/details/91529777","strategy":"BlogCommendFromMachineLearnPai2","index":"28"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_33860528/article/details/91529777" target="_blank"  rel="noopener" title="RabbitMQ 6种业务场景">
		<h4 class="text-truncate oneline">
				<em>RabbitMQ</em> 6种业务场景		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">05-22</span>
				<span class="read-num hover-hide">
					阅读数 
					298</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_33860528/article/details/91529777" target="_blank" rel="noopener" title="RabbitMQ 6种业务场景">
				<span class="desc oneline">应用场景1-“Hello Word”一个P向queue发送一个message，一个C从该queue接收message并打印。producer，连接至RabbitMQ Server，声明队列，发送mes...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_33860528">来自：	<span class="blog_title"> weixin_33860528的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	<div class="recommend-item-box recommend-recommend-box"><div id="kp_box_64" data-pid="64"><div id="three_ad23" class="mediav_ad" ></div>
<script type="text/javascript" src="//static.mediav.com/js/mvf_news_feed.js"></script>
<script>
                                               NEWS_FEED({
                w: 852,
                h : 60,
                showid : 'GNKXx7',
                placeholderId: "three_ad23",
                inject : 'define',
                define : {
                    imagePosition : 'left',
                    imageBorderRadius : 3,
                    imageWidth: 90,
                    imageHeight: 60,
                    imageFill : 'clip',
                    displayImage : true,
                    displayTitle : true,
                    titleFontSize: 18,
                    titleFontColor: '#000',
                    titleFontFamily : 'Lato,-apple-system,SF UI Text,Arial,PingFang SC,Hiragino Sans GB,Microsoft YaHei,WenQuanYi Micro Hei,sans-serif',
                    titleFontWeight: 'bold',
                    titlePaddingTop : 0,
                    titlePaddingRight : 0,
                    titlePaddingBottom : 5,
                    titlePaddingLeft : 16,
                    displayDesc : true,
                    descFontSize: 14,
                    descFontColor: '#8e959a',
                    descFontFamily : 'Microsoft Yahei',
                    paddingTop : 0,
                    paddingRight : 0,
                    paddingBottom : 0,
                    paddingLeft : 0,
                    backgroundColor: '#fff',
                    hoverColor: '#000'
                      }
                  })
                                        </script><img class="pre-img-lasy" data-src="https://kunyu.csdn.net/1.png?p=64&a=555&c=0&k=&d=1&t=3&u=fa1501fbafe343738d8c5caa68c8b458"></div></div>
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/qq_43901693/article/details/100606828","strategy":"BlogCommendFromMachineLearnPai2","index":"29"}'>
	<div class="content">
		<a href="https://blog.csdn.net/qq_43901693/article/details/100606828" target="_blank"  rel="noopener" title="130 个相见恨晚的超实用网站，一次性分享出来">
		<h4 class="text-truncate oneline">
				130 个相见恨晚的超实用网站，一次性分享出来		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">01-06</span>
				<span class="read-num hover-hide">
					阅读数 
					18万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/qq_43901693/article/details/100606828" target="_blank" rel="noopener" title="130 个相见恨晚的超实用网站，一次性分享出来">
				<span class="desc oneline">相见恨晚的超实用网站持续更新中。。。</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/qq_43901693">来自：	<span class="blog_title"> 藏冰的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_43562234/article/details/102792355","strategy":"BlogCommendFromMachineLearnPai2","index":"30"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_43562234/article/details/102792355" target="_blank"  rel="noopener" title="RabbitMQ高可用">
		<h4 class="text-truncate oneline">
				<em>RabbitMQ</em>高可用		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">10-29</span>
				<span class="read-num hover-hide">
					阅读数 
					96</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_43562234/article/details/102792355" target="_blank" rel="noopener" title="RabbitMQ高可用">
				<span class="desc oneline">rabbitMQ highly avilable基础环境系统： ubuntu19.10节点：node1,node2,node3修改服务hostname文件和hosts文件sudo vim /etc/h...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_43562234">来自：	<span class="blog_title"> weixin_43562234的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_39910040/article/details/80193782","strategy":"BlogCommendFromMachineLearnPai2","index":"31"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_39910040/article/details/80193782" target="_blank"  rel="noopener" title="安装RabbitMQ">
		<h4 class="text-truncate oneline">
				安装<em>RabbitMQ</em>		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">05-04</span>
				<span class="read-num hover-hide">
					阅读数 
					205</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_39910040/article/details/80193782" target="_blank" rel="noopener" title="安装RabbitMQ">
				<span class="desc oneline">1.erlang下载地址  http://www.erlang.org/downloads打开网址后，如果是win10是64位的，则选择64位的版本，下载后的文件名如下:  otp_win64_20....</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_39910040">来自：	<span class="blog_title"> weixin_39910040的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/yusimiao/article/details/102951152","strategy":"BlogCommendFromMachineLearnPai2","index":"32"}'>
	<div class="content">
		<a href="https://blog.csdn.net/yusimiao/article/details/102951152" target="_blank"  rel="noopener" title="JDK12 Collectors.teeing 你真的需要了解一下">
		<h4 class="text-truncate oneline">
				JDK12 Collectors.teeing 你真的需要了解一下		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">11-07</span>
				<span class="read-num hover-hide">
					阅读数 
					8371</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/yusimiao/article/details/102951152" target="_blank" rel="noopener" title="JDK12 Collectors.teeing 你真的需要了解一下">
				<span class="desc oneline">前言在 Java 12 里面有个非常好用但在官方 JEP 没有公布的功能，因为它只是 Collector 中的一个小改动，它的作用是 merge 两个 collector 的结果，这句话显得很抽象，老...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/yusimiao">来自：	<span class="blog_title"> 日拱一兵</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_30577801/article/details/99770610","strategy":"BlogCommendFromMachineLearnPai2","index":"33"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_30577801/article/details/99770610" target="_blank"  rel="noopener" title="Rabbitmq - 配置">
		<h4 class="text-truncate oneline">
				<em>Rabbitmq</em> - 配置		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">05-28</span>
				<span class="read-num hover-hide">
					阅读数 
					38</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_30577801/article/details/99770610" target="_blank" rel="noopener" title="Rabbitmq - 配置">
				<span class="desc oneline">目录                    RabbitMQ 配置        简介        环境变量        配置文件        运行时参数和策略                 ...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_30577801">来自：	<span class="blog_title"> weixin_30577801的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	<div class="recommend-item-box recommend-recommend-box"><div id="kp_box_65" data-pid="65"><script type="text/javascript">
        (function() {
            var s = "_" + Math.random().toString(36).slice(2);
            document.write('<div style="" id="' + s + '"></div>');
            (window.slotbydup = window.slotbydup || []).push({
                id: "u4221803",
                container: s
            });
        })();
</script>
<!-- 多条广告如下脚本只需引入一次 -->
<script type="text/javascript" src="//cpro.baidustatic.com/cpro/ui/c.js" async="async" defer="defer" >
</script><img class="pre-img-lasy" data-src="https://kunyu.csdn.net/1.png?p=65&a=1378&c=0&k=&d=1&t=3&u=1079ba475ec64721971969324bf56327"></div></div>
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_41656377/article/details/91490169","strategy":"BlogCommendFromMachineLearnPai2","index":"34"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_41656377/article/details/91490169" target="_blank"  rel="noopener" title="rabbitmq官方文档">
		<h4 class="text-truncate oneline">
				<em>rabbitmq</em>官方文档		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">06-12</span>
				<span class="read-num hover-hide">
					阅读数 
					291</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_41656377/article/details/91490169" target="_blank" rel="noopener" title="rabbitmq官方文档">
				<span class="desc oneline">https://www.rabbitmq.com/</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_41656377">来自：	<span class="blog_title"> weixin_41656377的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_33951761/article/details/94543002","strategy":"BlogCommendFromMachineLearnPai2","index":"35"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_33951761/article/details/94543002" target="_blank"  rel="noopener" title="登录RabbitMQ的方法">
		<h4 class="text-truncate oneline">
				登录<em>RabbitMQ</em>的方法		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">04-03</span>
				<span class="read-num hover-hide">
					阅读数 
					271</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_33951761/article/details/94543002" target="_blank" rel="noopener" title="登录RabbitMQ的方法">
				<span class="desc oneline">一：(运行RabbitMQ之前需要先打开docker 容器)打开相应的路径，在windows Powershell 管理员下打开,启动docker容器，一并打开了Server,Api,Workbenc...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_33951761">来自：	<span class="blog_title"> weixin_33951761的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/youku1327/article/details/102979381","strategy":"BlogCommendFromMachineLearnPai2","index":"36"}'>
	<div class="content">
		<a href="https://blog.csdn.net/youku1327/article/details/102979381" target="_blank"  rel="noopener" title="SQL-小白最佳入门sql查询一">
		<h4 class="text-truncate oneline">
				SQL-小白最佳入门sql查询一		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">11-10</span>
				<span class="read-num hover-hide">
					阅读数 
					5万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/youku1327/article/details/102979381" target="_blank" rel="noopener" title="SQL-小白最佳入门sql查询一">
				<span class="desc oneline">不要偷偷的查询我的个人资料，即使你再喜欢我，也不要这样，真的不好；</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/youku1327">来自：	<span class="blog_title"> 知识追寻者(Inheriting the spirit of open source, Spreading java knowledge;)</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_43163359/article/details/98776913","strategy":"BlogCommendFromMachineLearnPai2","index":"37"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_43163359/article/details/98776913" target="_blank"  rel="noopener" title="rabbitMQ">
		<h4 class="text-truncate oneline">
				<em>rabbitMQ</em>		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">08-07</span>
				<span class="read-num hover-hide">
					阅读数 
					61</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_43163359/article/details/98776913" target="_blank" rel="noopener" title="rabbitMQ">
				<span class="desc oneline">rabbitmq页面解析5种消息模型基本消息模型页面解析http://localhost:15672/#/账号: guest密码: guest5种消息模型RabbitMQ提供了6种消息模型，但是第6种...</span>
			</a>
			<span class="blog_title_box oneline ">
									<span class="type-show type-show-blog type-show-after">博文</span>
											<a target="_blank" rel="noopener" href="https://blog.csdn.net/weixin_43163359">来自：	<span class="blog_title"> weixin_43163359的博客</span></a>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/zzti_erlie/article/details/101060892","strategy":"BlogCommendFromMachineLearnPai2","index":"38"}'>
	<div class="content">
		<a href="https://blog.csdn.net/zzti_erlie/article/details/101060892" target="_blank"  rel="noopener" title="花了20分钟，给女朋友们写了一个web版群聊程序">
		<h4 class="text-truncate oneline">
				花了20分钟，给女朋友们写了一个web版群聊程序		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">11-28</span>
				<span class="read-num hover-hide">
					阅读数 
					27万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/zzti_erlie/article/details/101060892" target="_blank" rel="noopener" title="花了20分钟，给女朋友们写了一个web版群聊程序">
				<span class="desc oneline">参考博客[1]https://www.byteslounge.com/tutorials/java-ee-html5-websocket-example</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	<div class="recommend-item-box recommend-recommend-box"><div id="kp_box_66" data-pid="66"><script type="text/javascript">
        (function() {
            var s = "_" + Math.random().toString(36).slice(2);
            document.write('<div style="" id="' + s + '"></div>');
            (window.slotbydup = window.slotbydup || []).push({
                id: "u4623747",
                container: s
            });
        })();
</script>
<!-- 多条广告如下脚本只需引入一次 -->
<script type="text/javascript" src="//cpro.baidustatic.com/cpro/ui/c.js" async="async" defer="defer" >
</script><img class="pre-img-lasy" data-src="https://kunyu.csdn.net/1.png?p=66&a=1755&c=0&k=&d=1&t=3&u=18cd295d04804eba88e5322fe79455fd"></div></div>
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_45081575/article/details/102886718","strategy":"BlogCommendHotData","index":"0"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_45081575/article/details/102886718" target="_blank"  rel="noopener" title="《奇巧淫技》系列-python！！每天早上八点自动发送天气预报邮件到QQ邮箱">
		<h4 class="text-truncate oneline">
				《奇巧淫技》系列-python！！每天早上八点自动发送天气预报邮件到QQ邮箱		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">01-19</span>
				<span class="read-num hover-hide">
					阅读数 
					6万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_45081575/article/details/102886718" target="_blank" rel="noopener" title="《奇巧淫技》系列-python！！每天早上八点自动发送天气预报邮件到QQ邮箱">
				<span class="desc oneline">将代码部署服务器，每日早上定时获取到天气数据，并发送到邮箱。
也可以说是一个小人工智障。
思路可以运用在不同地方，主要介绍的是思路。...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/qq_41453285/article/details/103001772","strategy":"BlogCommendHotData","index":"1"}'>
	<div class="content">
		<a href="https://blog.csdn.net/qq_41453285/article/details/103001772" target="_blank"  rel="noopener" title="Linux(服务器编程):15---两种高效的事件处理模式（reactor模式、proactor模式）">
		<h4 class="text-truncate oneline">
				Linux(服务器编程):15---两种高效的事件处理模式（reactor模式、proactor模式）		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">11-17</span>
				<span class="read-num hover-hide">
					阅读数 
					3408</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/qq_41453285/article/details/103001772" target="_blank" rel="noopener" title="Linux(服务器编程):15---两种高效的事件处理模式（reactor模式、proactor模式）">
				<span class="desc oneline">前言

同步I/O模型通常用于实现Reactor模式
	异步I/O模型则用于实现Proactor模式
	最后我们会使用同步I/O方式模拟出Proactor模式
一、Reactor模式


Reacto...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/qq_14996421/article/details/103135914","strategy":"BlogCommendHotData","index":"2"}'>
	<div class="content">
		<a href="https://blog.csdn.net/qq_14996421/article/details/103135914" target="_blank"  rel="noopener" title="为什么要学数据结构？">
		<h4 class="text-truncate oneline">
				为什么要学数据结构？		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">11-19</span>
				<span class="read-num hover-hide">
					阅读数 
					2万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/qq_14996421/article/details/103135914" target="_blank" rel="noopener" title="为什么要学数据结构？">
				<span class="desc oneline">一、前言
在可视化化程序设计的今天，借助于集成开发环境可以很快地生成程序，程序设计不再是计算机专业人员的专利。很多人认为，只要掌握几种开发工具就可以成为编程高手，其实，这是一种误解。要想成为一个专业的...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/qq_41505957/article/details/103138305","strategy":"BlogCommendHotData","index":"3"}'>
	<div class="content">
		<a href="https://blog.csdn.net/qq_41505957/article/details/103138305" target="_blank"  rel="noopener" title="C语言魔塔游戏">
		<h4 class="text-truncate oneline">
				C语言魔塔游戏		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-08</span>
				<span class="read-num hover-hide">
					阅读数 
					2万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/qq_41505957/article/details/103138305" target="_blank" rel="noopener" title="C语言魔塔游戏">
				<span class="desc oneline">很早就很想写这个，今天终于写完了。

游戏截图：







编译环境: VS2017

游戏需要一些图片，如果有想要的或者对游戏有什么看法的可以加我的QQ 2985486630 讨论，如果暂时没有...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/qq_34666857/article/details/103162132","strategy":"BlogCommendHotData","index":"4"}'>
	<div class="content">
		<a href="https://blog.csdn.net/qq_34666857/article/details/103162132" target="_blank"  rel="noopener" title="进程通信方式总结与盘点">
		<h4 class="text-truncate oneline">
				进程通信方式总结与盘点		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">11-20</span>
				<span class="read-num hover-hide">
					阅读数 
					781</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/qq_34666857/article/details/103162132" target="_blank" rel="noopener" title="进程通信方式总结与盘点">
				<span class="desc oneline">​	进程通信是指进程之间的信息交换。这里需要和进程同步做一下区分，进程同步控制多个进程按一定顺序执行，进程通信是一种手段，而进程同步是目标。从某方面来讲，进程通信可以解决进程同步问题。
​	首先回顾下...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	<div class="recommend-item-box recommend-recommend-box"><script type="text/javascript" src="//rabc1.iteye.com/production/res/rxjg.js?pkcgstj=jm"></script></div>
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/qq_45036710/article/details/103226451","strategy":"BlogCommendHotData","index":"5"}'>
	<div class="content">
		<a href="https://blog.csdn.net/qq_45036710/article/details/103226451" target="_blank"  rel="noopener" title="究竟你适不适合买Mac？">
		<h4 class="text-truncate oneline">
				究竟你适不适合买Mac？		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">11-24</span>
				<span class="read-num hover-hide">
					阅读数 
					6万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/qq_45036710/article/details/103226451" target="_blank" rel="noopener" title="究竟你适不适合买Mac？">
				<span class="desc oneline">我清晰的记得，刚买的macbook pro回到家，开机后第一件事情，就是上了淘宝网，花了500元钱，找了一个上门维修电脑的师傅，上门给我装了一个windows系统。。。。。。
表砍我。。。
当时买ma...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/yunqiinsight/article/details/103235032","strategy":"BlogCommendHotData","index":"6"}'>
	<div class="content">
		<a href="https://blog.csdn.net/yunqiinsight/article/details/103235032" target="_blank"  rel="noopener" title="听说了吗？阿里双11作战室竟1根网线都没有">
		<h4 class="text-truncate oneline">
				听说了吗？阿里双11作战室竟1根网线都没有		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">11-25</span>
				<span class="read-num hover-hide">
					阅读数 
					1万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/yunqiinsight/article/details/103235032" target="_blank" rel="noopener" title="听说了吗？阿里双11作战室竟1根网线都没有">
				<span class="desc oneline">双11不光是购物狂欢节，更是对技术的一次“大考”，对于阿里巴巴企业内部运营的基础保障技术而言，亦是如此。

回溯双11历史，这背后也经历过“小米加步枪”的阶段：作战室从随处是网线，交换机放地上的“一地...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/yunqiinsight/article/details/103252083","strategy":"BlogCommendHotData","index":"7"}'>
	<div class="content">
		<a href="https://blog.csdn.net/yunqiinsight/article/details/103252083" target="_blank"  rel="noopener" title="在阿里，40岁的奋斗姿势">
		<h4 class="text-truncate oneline">
				在阿里，40岁的奋斗姿势		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">11-26</span>
				<span class="read-num hover-hide">
					阅读数 
					3万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/yunqiinsight/article/details/103252083" target="_blank" rel="noopener" title="在阿里，40岁的奋斗姿势">
				<span class="desc oneline">在阿里，40岁的奋斗姿势

在阿里，什么样的年纪可以称为老呢？35岁？
在云网络，有这样一群人，他们的平均年龄接近40，却刚刚开辟职业生涯的第二战场。
他们的奋斗姿势是什么样的呢？

洛神赋

“翩若...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/huver2007/article/details/103260847","strategy":"BlogCommendHotData","index":"8"}'>
	<div class="content">
		<a href="https://blog.csdn.net/huver2007/article/details/103260847" target="_blank"  rel="noopener" title="关于研发效能提升的思考">
		<h4 class="text-truncate oneline">
				关于研发效能提升的思考		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">11-26</span>
				<span class="read-num hover-hide">
					阅读数 
					1984</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/huver2007/article/details/103260847" target="_blank" rel="noopener" title="关于研发效能提升的思考">
				<span class="desc oneline">研发效能提升是最近比较热门的一个话题，本人根据这几年的工作心得，做了一些思考总结，由于个人深度有限，暂且抛转引入。
	
	三要素
	
任何生产力的提升都离不开这三个因素：人、流程和工具，少了其中任何一...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/qq_43764365/article/details/103539728","strategy":"BlogCommendHotData","index":"9"}'>
	<div class="content">
		<a href="https://blog.csdn.net/qq_43764365/article/details/103539728" target="_blank"  rel="noopener" title="Python爬虫爬取淘宝，京东商品信息">
		<h4 class="text-truncate oneline">
				Python爬虫爬取淘宝，京东商品信息		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-09</span>
				<span class="read-num hover-hide">
					阅读数 
					9351</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/qq_43764365/article/details/103539728" target="_blank" rel="noopener" title="Python爬虫爬取淘宝，京东商品信息">
				<span class="desc oneline">小编是一个理科生，不善长说一些废话。简单介绍下原理然后直接上代码。

使用的工具（Python+pycharm2019.3+selenium+xpath+chromedriver）其中要使用pycha...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	<div class="recommend-item-box recommend-recommend-box"><script type="text/javascript" src="//rabc1.iteye.com/production/res/rxjg.js?pkcgstj=jm"></script></div>
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/qq_35190492/article/details/103965492","strategy":"BlogCommendHotData","index":"10"}'>
	<div class="content">
		<a href="https://blog.csdn.net/qq_35190492/article/details/103965492" target="_blank"  rel="noopener" title="阿里程序员写了一个新手都写不出的低级bug，被骂惨了。">
		<h4 class="text-truncate oneline">
				阿里程序员写了一个新手都写不出的低级bug，被骂惨了。		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">01-13</span>
				<span class="read-num hover-hide">
					阅读数 
					1万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/qq_35190492/article/details/103965492" target="_blank" rel="noopener" title="阿里程序员写了一个新手都写不出的低级bug，被骂惨了。">
				<span class="desc oneline">这种新手都不会范的错，居然被一个工作好几年的小伙子写出来，差点被当场开除了。...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/HarderXin/article/details/103971493","strategy":"BlogCommendHotData","index":"11"}'>
	<div class="content">
		<a href="https://blog.csdn.net/HarderXin/article/details/103971493" target="_blank"  rel="noopener" title="Java工作4年来应聘要16K最后没要,细节如下。。。">
		<h4 class="text-truncate oneline">
				Java工作4年来应聘要16K最后没要,细节如下。。。		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">01-14</span>
				<span class="read-num hover-hide">
					阅读数 
					2万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/HarderXin/article/details/103971493" target="_blank" rel="noopener" title="Java工作4年来应聘要16K最后没要,细节如下。。。">
				<span class="desc oneline">前奏：
今天2B哥和大家分享一位前几天面试的一位应聘者，工作4年26岁，统招本科。
以下就是他的简历和面试情况。

基本情况：


专业技能：
1、&nbsp;熟悉Sping了解SpringMVC、S...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/yellowzf3/article/details/103982287","strategy":"BlogCommendHotData","index":"12"}'>
	<div class="content">
		<a href="https://blog.csdn.net/yellowzf3/article/details/103982287" target="_blank"  rel="noopener" title="2020年，冯唐49岁：我给20、30岁IT职场年轻人的建议">
		<h4 class="text-truncate oneline">
				2020年，冯唐49岁：我给20、30岁IT职场年轻人的建议		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-07</span>
				<span class="read-num hover-hide">
					阅读数 
					1万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/yellowzf3/article/details/103982287" target="_blank" rel="noopener" title="2020年，冯唐49岁：我给20、30岁IT职场年轻人的建议">
				<span class="desc oneline">
点击“技术领导力”关注∆  每天早上8:30推送

作者| Mr.K   编辑| Emma

来源| 技术领导力(ID：jishulingdaoli)

前天的推文《冯唐：职场人35岁以后，方法论比...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_44735475/article/details/104037265","strategy":"BlogCommendHotData","index":"13"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_44735475/article/details/104037265" target="_blank"  rel="noopener" title="程序员该看的几部电影">
		<h4 class="text-truncate oneline">
				程序员该看的几部电影		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-08</span>
				<span class="read-num hover-hide">
					阅读数 
					8891</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_44735475/article/details/104037265" target="_blank" rel="noopener" title="程序员该看的几部电影">
				<span class="desc oneline">##1、骇客帝国(1999) 概念：在线/离线，递归，循环，矩阵等

剧情简介：
不久的将来，网络黑客尼奥对这个看似正常的现实世界产生了怀疑。
他结识了黑客崔妮蒂，并见到了黑客组织的首领墨菲斯。
墨菲...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/alitech2017/article/details/104037639","strategy":"BlogCommendHotData","index":"14"}'>
	<div class="content">
		<a href="https://blog.csdn.net/alitech2017/article/details/104037639" target="_blank"  rel="noopener" title="入职阿里5年，他如何破解“技术债”？">
		<h4 class="text-truncate oneline">
				入职阿里5年，他如何破解“技术债”？		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">01-19</span>
				<span class="read-num hover-hide">
					阅读数 
					2048</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/alitech2017/article/details/104037639" target="_blank" rel="noopener" title="入职阿里5年，他如何破解“技术债”？">
				<span class="desc oneline">简介： 作者 | 都铎



作为一名技术人，你常常会听到这样的话：

“先快速上线”
“没时间改”
“再缓一缓吧”
“以后再解决”
“先用临时方案处理”
……

当你埋下的坑越来越多，不知道哪天哪位...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/qq_34409973/article/details/104048903","strategy":"BlogCommendHotData","index":"15"}'>
	<div class="content">
		<a href="https://blog.csdn.net/qq_34409973/article/details/104048903" target="_blank"  rel="noopener" title="Python绘图，圣诞树，花，爱心  |  Turtle篇">
		<h4 class="text-truncate oneline">
				Python绘图，圣诞树，花，爱心  |  Turtle篇		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">01-20</span>
				<span class="read-num hover-hide">
					阅读数 
					2284</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/qq_34409973/article/details/104048903" target="_blank" rel="noopener" title="Python绘图，圣诞树，花，爱心  |  Turtle篇">
				<span class="desc oneline">每周每日，分享Python实战代码，入门资料，进阶资料，基础语法，爬虫，数据分析，web网站，机器学习，深度学习等等。

公众号回复【进群】沟通交流吧，QQ扫码进群学习吧

微信群 QQ群 



1...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/sinat_33921105/article/details/104066631","strategy":"BlogCommendHotData","index":"16"}'>
	<div class="content">
		<a href="https://blog.csdn.net/sinat_33921105/article/details/104066631" target="_blank"  rel="noopener" title="作为一个程序员，CPU的这些硬核知识你必须会！">
		<h4 class="text-truncate oneline">
				作为一个程序员，CPU的这些硬核知识你必须会！		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">01-21</span>
				<span class="read-num hover-hide">
					阅读数 
					2万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/sinat_33921105/article/details/104066631" target="_blank" rel="noopener" title="作为一个程序员，CPU的这些硬核知识你必须会！">
				<span class="desc oneline">CPU对每个程序员来说，是个既熟悉又陌生的东西？
如果你只知道CPU是中央处理器的话，那可能对你并没有什么用，那么作为程序员的我们，必须要搞懂的就是CPU这家伙是如何运行的，尤其要搞懂它里面的寄存器是...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/u014044812/article/details/104076639","strategy":"BlogCommendHotData","index":"17"}'>
	<div class="content">
		<a href="https://blog.csdn.net/u014044812/article/details/104076639" target="_blank"  rel="noopener" title="破14亿，Python分析我国存在哪些人口危机！">
		<h4 class="text-truncate oneline">
				破14亿，Python分析我国存在哪些人口危机！		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-04</span>
				<span class="read-num hover-hide">
					阅读数 
					1万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/u014044812/article/details/104076639" target="_blank" rel="noopener" title="破14亿，Python分析我国存在哪些人口危机！">
				<span class="desc oneline">2020年1月17日，国家统计局发布了2019年国民经济报告，报告中指出我国人口突破14亿。
猪哥的朋友圈被14亿人口刷屏，但是很多人并没有看到我国复杂的人口问题：老龄化、男女比例失衡、生育率下降、人...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/csdnnews/article/details/104137953","strategy":"BlogCommendHotData","index":"18"}'>
	<div class="content">
		<a href="https://blog.csdn.net/csdnnews/article/details/104137953" target="_blank"  rel="noopener" title="在家远程办公效率低？那你一定要收好这个「在家办公」神器！">
		<h4 class="text-truncate oneline">
				在家远程办公效率低？那你一定要收好这个「在家办公」神器！		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-01</span>
				<span class="read-num hover-hide">
					阅读数 
					1万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/csdnnews/article/details/104137953" target="_blank" rel="noopener" title="在家远程办公效率低？那你一定要收好这个「在家办公」神器！">
				<span class="desc oneline">相信大家都已经收到国务院延长春节假期的消息，接下来，在家远程办公可能将会持续一段时间。

但是问题来了。远程办公不是人在电脑前就当坐班了，相反，对于沟通效率，文件协作，以及信息安全都有着极高的要求。有...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/sinat_33921105/article/details/104142623","strategy":"BlogCommendHotData","index":"19"}'>
	<div class="content">
		<a href="https://blog.csdn.net/sinat_33921105/article/details/104142623" target="_blank"  rel="noopener" title="作为一个程序员，内存和磁盘的这些事情，你不得不知道啊！！！">
		<h4 class="text-truncate oneline">
				作为一个程序员，内存和磁盘的这些事情，你不得不知道啊！！！		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-02</span>
				<span class="read-num hover-hide">
					阅读数 
					2万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/sinat_33921105/article/details/104142623" target="_blank" rel="noopener" title="作为一个程序员，内存和磁盘的这些事情，你不得不知道啊！！！">
				<span class="desc oneline">截止目前，我已经分享了如下几篇文章：
一个程序在计算机中是如何运行的？超级干货！！！
作为一个程序员，CPU的这些硬核知识你必须会！
作为一个程序员，内存的这些硬核知识你必须懂！
这些知识可以说是我们...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/x763795151/article/details/104149557","strategy":"BlogCommendHotData","index":"20"}'>
	<div class="content">
		<a href="https://blog.csdn.net/x763795151/article/details/104149557" target="_blank"  rel="noopener" title="2020年的1月，我辞掉了我的第一份工作">
		<h4 class="text-truncate oneline">
				2020年的1月，我辞掉了我的第一份工作		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-11</span>
				<span class="read-num hover-hide">
					阅读数 
					1884</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/x763795151/article/details/104149557" target="_blank" rel="noopener" title="2020年的1月，我辞掉了我的第一份工作">
				<span class="desc oneline">其实，这篇文章，我应该早点写的，毕竟现在已经2月份了。不过一些其它原因，或者是我的惰性、还有一些迷茫的念头，让自己迟迟没有试着写一点东西，记录下，或者说是总结下自己前3年的工作上的经历、学习的过程。
...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/leelight/article/details/104151487","strategy":"BlogCommendHotData","index":"21"}'>
	<div class="content">
		<a href="https://blog.csdn.net/leelight/article/details/104151487" target="_blank"  rel="noopener" title="别低估自己的直觉，也别高估自己的智商">
		<h4 class="text-truncate oneline">
				别低估自己的直觉，也别高估自己的智商		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-02</span>
				<span class="read-num hover-hide">
					阅读数 
					3225</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/leelight/article/details/104151487" target="_blank" rel="noopener" title="别低估自己的直觉，也别高估自己的智商">
				<span class="desc oneline">所有群全部吵翻天，朋友圈全部沦陷，公众号疯狂转发。这两周没怎么发原创，只发新闻，可能有人注意到了。我不是懒，是文章写了却没发，因为大家的关注力始终在这次的疫情上面，发了也没人看。当然，我......</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/renfufei/article/details/104163518","strategy":"BlogCommendHotData","index":"22"}'>
	<div class="content">
		<a href="https://blog.csdn.net/renfufei/article/details/104163518" target="_blank"  rel="noopener" title="Java坑人面试题系列: 包装类（中级难度）">
		<h4 class="text-truncate oneline">
				Java坑人面试题系列: 包装类（中级难度）		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-03</span>
				<span class="read-num hover-hide">
					阅读数 
					1万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/renfufei/article/details/104163518" target="_blank" rel="noopener" title="Java坑人面试题系列: 包装类（中级难度）">
				<span class="desc oneline">Java Magazine上面有一个专门坑人的面试题系列: https://blogs.oracle.com/javamagazine/quiz-2。
这些问题的设计宗旨，主要是测试面试者对Java语...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/TeFuirnever/article/details/104174480","strategy":"BlogCommendHotData","index":"23"}'>
	<div class="content">
		<a href="https://blog.csdn.net/TeFuirnever/article/details/104174480" target="_blank"  rel="noopener" title="深度学习入门笔记（十八）：卷积神经网络（一）">
		<h4 class="text-truncate oneline">
				深度学习入门笔记（十八）：卷积神经网络（一）		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-12</span>
				<span class="read-num hover-hide">
					阅读数 
					375</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/TeFuirnever/article/details/104174480" target="_blank" rel="noopener" title="深度学习入门笔记（十八）：卷积神经网络（一）">
				<span class="desc oneline">欢迎关注WX公众号：【程序员管小亮】
专栏——深度学习入门笔记
声明
1）该文章整理自网上的大牛和机器学习专家无私奉献的资料，具体引用的资料请看参考文献。
2）本文仅供学术交流，非商用。所以每一部分具...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/harvic880925/article/details/104176042","strategy":"BlogCommendHotData","index":"24"}'>
	<div class="content">
		<a href="https://blog.csdn.net/harvic880925/article/details/104176042" target="_blank"  rel="noopener" title="这个世界上人真的分三六九等，你信吗？">
		<h4 class="text-truncate oneline">
				这个世界上人真的分三六九等，你信吗？		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-13</span>
				<span class="read-num hover-hide">
					阅读数 
					1万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/harvic880925/article/details/104176042" target="_blank" rel="noopener" title="这个世界上人真的分三六九等，你信吗？">
				<span class="desc oneline">偶然间，在知乎上看到一个问题



一时间，勾起了我深深的回忆。

以前在厂里打过两次工，做过家教，干过辅导班，做过中介。零下几度的晚上，贴过广告，满脸、满手地长冻疮。



再回首那段岁月，虽然苦，...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/HyperAI/article/details/104177715","strategy":"BlogCommendHotData","index":"25"}'>
	<div class="content">
		<a href="https://blog.csdn.net/HyperAI/article/details/104177715" target="_blank"  rel="noopener" title="节后首个工作日，企业们集体开晨会让钉钉挂了">
		<h4 class="text-truncate oneline">
				节后首个工作日，企业们集体开晨会让钉钉挂了		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-04</span>
				<span class="read-num hover-hide">
					阅读数 
					2374</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/HyperAI/article/details/104177715" target="_blank" rel="noopener" title="节后首个工作日，企业们集体开晨会让钉钉挂了">
				<span class="desc oneline">By 超神经场景描述：昨天 2 月 3 日，是大部分城市号召远程工作的第一天，全国有接近 2 亿人在家开始远程办公，钉钉上也有超过 1000 万家企业活跃起来。关键词：十一出行 人脸......</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/m0_46245938/article/details/104179209","strategy":"BlogCommendHotData","index":"26"}'>
	<div class="content">
		<a href="https://blog.csdn.net/m0_46245938/article/details/104179209" target="_blank"  rel="noopener" title="Java基础知识点梳理">
		<h4 class="text-truncate oneline">
				Java基础知识点梳理		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-09</span>
				<span class="read-num hover-hide">
					阅读数 
					3772</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/m0_46245938/article/details/104179209" target="_blank" rel="noopener" title="Java基础知识点梳理">
				<span class="desc oneline">Java基础知识点梳理
摘要：
虽然已经在实际工作中经常与java打交道，但是一直没系统地对java这门语言进行梳理和总结，掌握的知识也比较零散。恰好利用这段时间重新认识下java，并对一些常见的语法...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/itcast_cn/article/details/104196535","strategy":"BlogCommendHotData","index":"27"}'>
	<div class="content">
		<a href="https://blog.csdn.net/itcast_cn/article/details/104196535" target="_blank"  rel="noopener" title="2020年全新Java学习路线图，含配套视频，学完即为中级Java程序员！！">
		<h4 class="text-truncate oneline">
				2020年全新Java学习路线图，含配套视频，学完即为中级Java程序员！！		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-06</span>
				<span class="read-num hover-hide">
					阅读数 
					7246</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/itcast_cn/article/details/104196535" target="_blank" rel="noopener" title="2020年全新Java学习路线图，含配套视频，学完即为中级Java程序员！！">
				<span class="desc oneline">新的一年来临，突如其来的疫情打破了平静的生活！

在家的你是否很无聊，如果无聊就来学习吧！

世上只有一种投资只赚不赔，那就是学习！！！

传智播客于2020年升级了Java学习线路图，硬核升级，免费...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/JiuZhang_ninechapter/article/details/104197117","strategy":"BlogCommendHotData","index":"28"}'>
	<div class="content">
		<a href="https://blog.csdn.net/JiuZhang_ninechapter/article/details/104197117" target="_blank"  rel="noopener" title="B 站上有哪些很好的学习资源?">
		<h4 class="text-truncate oneline">
				B 站上有哪些很好的学习资源?		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-06</span>
				<span class="read-num hover-hide">
					阅读数 
					2万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/JiuZhang_ninechapter/article/details/104197117" target="_blank" rel="noopener" title="B 站上有哪些很好的学习资源?">
				<span class="desc oneline">哇说起B站，在小九眼里就是宝藏般的存在，放年假宅在家时一天刷6、7个小时不在话下，更别提今年的跨年晚会，我简直是跪着看完的！！
最早大家聚在在B站是为了追番，再后来我在上面刷欧美新歌和漂亮小姐姐的舞蹈...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_44613063/article/details/104203736","strategy":"BlogCommendHotData","index":"29"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_44613063/article/details/104203736" target="_blank"  rel="noopener" title="你也能看懂的：蒙特卡罗方法">
		<h4 class="text-truncate oneline">
				你也能看懂的：蒙特卡罗方法		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-12</span>
				<span class="read-num hover-hide">
					阅读数 
					283</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_44613063/article/details/104203736" target="_blank" rel="noopener" title="你也能看懂的：蒙特卡罗方法">
				<span class="desc oneline">蒙特卡罗方法，也称统计模拟方法，是1940年代中期由于科学技术的发展和电子计算机的发明，而提出的一种以概率统计理论为指导的数值计算方法。是指使用随机数（或更常见的伪随机数）来解决很多计算问题的方法
蒙...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/qing_gee/article/details/104206866","strategy":"BlogCommendHotData","index":"30"}'>
	<div class="content">
		<a href="https://blog.csdn.net/qing_gee/article/details/104206866" target="_blank"  rel="noopener" title="如何优雅地打印一个Java对象？">
		<h4 class="text-truncate oneline">
				如何优雅地打印一个Java对象？		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-07</span>
				<span class="read-num hover-hide">
					阅读数 
					1万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/qing_gee/article/details/104206866" target="_blank" rel="noopener" title="如何优雅地打印一个Java对象？">
				<span class="desc oneline">你好呀，我是沉默王二，一个和黄家驹一样身高，和刘德华一样颜值的程序员。虽然已经写了十多年的 Java 代码，但仍然觉得自己是个菜鸟（请允许我惭愧一下）。
在一个月黑风高的夜晚，我思前想后，觉得再也不能...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/jdcdev_/article/details/104208023","strategy":"BlogCommendHotData","index":"31"}'>
	<div class="content">
		<a href="https://blog.csdn.net/jdcdev_/article/details/104208023" target="_blank"  rel="noopener" title="雷火神山直播超两亿，Web播放器事件监听是怎么实现的？">
		<h4 class="text-truncate oneline">
				雷火神山直播超两亿，Web播放器事件监听是怎么实现的？		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-07</span>
				<span class="read-num hover-hide">
					阅读数 
					1677</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/jdcdev_/article/details/104208023" target="_blank" rel="noopener" title="雷火神山直播超两亿，Web播放器事件监听是怎么实现的？">
				<span class="desc oneline">Web播放器解决了在手机浏览器和PC浏览器上播放音视频数据的问题，让视音频内容可以不依赖用户安装App，就能进行播放以及在社交平台进行传播。在视频业务大数据平台中，播放数据的统计分析非常重要，所以We...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_43766298/article/details/104208049","strategy":"BlogCommendHotData","index":"32"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_43766298/article/details/104208049" target="_blank"  rel="noopener" title="JAVA后端面试《Spring》">
		<h4 class="text-truncate oneline">
				JAVA后端面试《Spring》		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-07</span>
				<span class="read-num hover-hide">
					阅读数 
					6660</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_43766298/article/details/104208049" target="_blank" rel="noopener" title="JAVA后端面试《Spring》">
				<span class="desc oneline">Spring1.Spring是什么？有什么好处？2.IOC是什么？有什么好处？具体过程？3.DI是什么？4.IOC和DI的关系？5.bean标签的属性有哪些？6.IOC创建对象有哪几种方式？7.Spr...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/csdnnews/article/details/104218194","strategy":"BlogCommendHotData","index":"33"}'>
	<div class="content">
		<a href="https://blog.csdn.net/csdnnews/article/details/104218194" target="_blank"  rel="noopener" title="AI 医生“战疫”在前线">
		<h4 class="text-truncate oneline">
				AI 医生“战疫”在前线		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-07</span>
				<span class="read-num hover-hide">
					阅读数 
					3991</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/csdnnews/article/details/104218194" target="_blank" rel="noopener" title="AI 医生“战疫”在前线">
				<span class="desc oneline">作者| Just出品|CSDN（CSDNnews）紧急驰援疫区，AI医生也出动了。截止到2月6日，随着新冠病毒肺炎疫情的不断发展，全国累计已有31161例确诊病例，26359例疑......</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/xinzhifu1/article/details/104228470","strategy":"BlogCommendHotData","index":"34"}'>
	<div class="content">
		<a href="https://blog.csdn.net/xinzhifu1/article/details/104228470" target="_blank"  rel="noopener" title="3万字总结，Mysql优化之精髓">
		<h4 class="text-truncate oneline">
				3万字总结，Mysql优化之精髓		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-08</span>
				<span class="read-num hover-hide">
					阅读数 
					4590</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/xinzhifu1/article/details/104228470" target="_blank" rel="noopener" title="3万字总结，Mysql优化之精髓">
				<span class="desc oneline">本文知识点较多，篇幅较长，请耐心学习

MySQL已经成为时下关系型数据库产品的中坚力量，备受互联网大厂的青睐，出门面试想进BAT，想拿高工资，不会点MySQL优化知识，拿offer的成功率会大大下降...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/shineych/article/details/104231072","strategy":"BlogCommendHotData","index":"35"}'>
	<div class="content">
		<a href="https://blog.csdn.net/shineych/article/details/104231072" target="_blank"  rel="noopener" title="用Python爬取新型冠状病毒肺炎实时数据，pyecharts v1.x绘制省市区疫情地图">
		<h4 class="text-truncate oneline">
				用Python爬取新型冠状病毒肺炎实时数据，pyecharts v1.x绘制省市区疫情地图		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-09</span>
				<span class="read-num hover-hide">
					阅读数 
					4121</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/shineych/article/details/104231072" target="_blank" rel="noopener" title="用Python爬取新型冠状病毒肺炎实时数据，pyecharts v1.x绘制省市区疫情地图">
				<span class="desc oneline">文章目录运行结果（2020-2-8数据）基本方案数据格式全国疫情地图实现福建省疫情地图实现福州市疫情地图实现其他
运行结果（2020-2-8数据）



基本方案

web请求用requests
网页...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/nightLetme/article/details/104231968","strategy":"BlogCommendHotData","index":"36"}'>
	<div class="content">
		<a href="https://blog.csdn.net/nightLetme/article/details/104231968" target="_blank"  rel="noopener" title="MySQL基础笔记">
		<h4 class="text-truncate oneline">
				MySQL基础笔记		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-11</span>
				<span class="read-num hover-hide">
					阅读数 
					2002</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/nightLetme/article/details/104231968" target="_blank" rel="noopener" title="MySQL基础笔记">
				<span class="desc oneline">如有错误，恳请告知。非常感谢！

环境(相关下载、配置)：
phpstudy7.0.9
Apache2.4.39
MySQL5.7.26
phpMyAdmin4.8.5
此文在Windows10下实验...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/weixin_43853097/article/details/104240158","strategy":"BlogCommendHotData","index":"37"}'>
	<div class="content">
		<a href="https://blog.csdn.net/weixin_43853097/article/details/104240158" target="_blank"  rel="noopener" title="HTML5适合的情人节礼物有纪念日期功能">
		<h4 class="text-truncate oneline">
				HTML5适合的情人节礼物有纪念日期功能		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-09</span>
				<span class="read-num hover-hide">
					阅读数 
					1万+</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/weixin_43853097/article/details/104240158" target="_blank" rel="noopener" title="HTML5适合的情人节礼物有纪念日期功能">
				<span class="desc oneline">前言
利用HTML5，css，js实现爱心树 以及 纪念日期的功能 网页有播放音乐功能 以及打字倾诉感情的画面，非常适合情人节送给女朋友
具体的HTML代码
具体只要修改代码里面的男某某和女某某 文字...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/zhanglong_4444/article/details/104242276","strategy":"BlogCommendHotData","index":"38"}'>
	<div class="content">
		<a href="https://blog.csdn.net/zhanglong_4444/article/details/104242276" target="_blank"  rel="noopener" title="JVM 调优命令&amp;工具使用">
		<h4 class="text-truncate oneline">
				JVM 调优命令&amp;工具使用		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-10</span>
				<span class="read-num hover-hide">
					阅读数 
					981</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/zhanglong_4444/article/details/104242276" target="_blank" rel="noopener" title="JVM 调优命令&amp;工具使用">
				<span class="desc oneline">top命令查看进程占用资源情况

jps 命令 查看 java进程

jstack 命令 关注WATTING 查看死锁问题

jstat -gc pid 查看 GC 情况

jinfo pid 查看 ...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
<div class="recommend-item-box type_blog clearfix"  data-report-click='{"mod":"popu_614","dest":"https://blog.csdn.net/zhou_heaven/article/details/104246114","strategy":"BlogCommendHotData","index":"39"}'>
	<div class="content">
		<a href="https://blog.csdn.net/zhou_heaven/article/details/104246114" target="_blank"  rel="noopener" title="Python基础知识入门（二）">
		<h4 class="text-truncate oneline">
				Python基础知识入门（二）		</h4>
		<div class="info-box d-flex align-content-center">
			<p class="date-and-readNum oneline">
				<span class="date hover-show">02-10</span>
				<span class="read-num hover-hide">
					阅读数 
					1134</span>
				</p>
			</div>
		</a>
		<p class="content">
			<a href="https://blog.csdn.net/zhou_heaven/article/details/104246114" target="_blank" rel="noopener" title="Python基础知识入门（二）">
				<span class="desc oneline">4 容器类型
容器深层含义自己不知道，但是就表面意思。我自己理解的容器就是容器。他就是一个可以装“东西”的罐子啥的。不同的“罐子”可以装的“东西”不同，就像酒杯装酒，茶杯装茶，水缸装水。酒杯、茶杯、水...</span>
			</a>
			<span class="blog_title_box oneline no-title">
									<span class="type-show type-show-blog type-show-after">博文</span>
												</span>
		</p>
	</div>
	</div>

	
	
                    <div class="recommend-item-box type_hot_word">
                    <div class="content clearfix">
                        <div class="float-left">
                                                                                <span>
                                <a href="https://blog.csdn.net/yilovexing/article/details/80577510" target="_blank">
                                python</a>
                            </span>
                                                        <span>
                                <a href="https://blog.csdn.net/slwbcsdn/article/details/53458352" target="_blank">
                                json</a>
                            </span>
                                                        <span>
                                <a href="https://blog.csdn.net/csdnnews/article/details/83753246" target="_blank">
                                java</a>
                            </span>
                                                        <span>
                                <a href="https://blog.csdn.net/qq_35077512/article/details/88952519" target="_blank">
                                mysql</a>
                            </span>
                                                        <span>
                                <a href="https://blog.csdn.net/pdcfighting/article/details/80297499" target="_blank">
                                pycharm</a>
                            </span>
                                                        <span>
                                <a href="https://blog.csdn.net/sinyu890807/article/details/97142065" target="_blank">
                                android</a>
                            </span>
                                                        <span>
                                <a href="https://blog.csdn.net/gexiaoyizhimei/article/details/100122368" target="_blank">
                                linux</a>
                            </span>
                                                        <span>
                                <a href="https://download.csdn.net/download/xhg_gszs/10978826" target="_blank">
                                json格式</a>
                            </span>
                                                    
                                                                                <span>
                                <a href="https://www.csdn.net/gather_2b/MtzaQg0sLWJsb2cO0O0O.html" target="_blank">
                                c# implicit</a>
                            </span>
                                                        <span>
                                <a href="https://www.csdn.net/gather_1d/MtzaQg1sLWRvd25sb2Fk.html" target="_blank">
                                c#怎么保留3个小数点</a>
                            </span>
                                                        <span>
                                <a href="https://www.csdn.net/gather_11/MtzaQg2sLWRvd25sb2Fk.html" target="_blank">
                                c# 串口通信、</a>
                            </span>
                                                        <span>
                                <a href="https://www.csdn.net/gather_1c/MtzaQg3sLWRvd25sb2Fk.html" target="_blank">
                                网络调试助手c#</a>
                            </span>
                                                        <span>
                                <a href="https://www.csdn.net/gather_10/MtzaQg4sLWRvd25sb2Fk.html" target="_blank">
                                c# 泛型比较大小</a>
                            </span>
                                                        <span>
                                <a href="https://www.csdn.net/gather_10/MtzaQg5sLWRvd25sb2Fk.html" target="_blank">
                                c#解压分卷问题</a>
                            </span>
                                                        <span>
                                <a href="https://www.csdn.net/gather_19/MtzaUgwsLWRvd25sb2Fk.html" target="_blank">
                                c#启动居中</a>
                            </span>
                                                        <span>
                                <a href="https://www.csdn.net/gather_1e/MtzaUgxsLWRvd25sb2Fk.html" target="_blank">
                                c# 逻辑或运算符</a>
                            </span>
                                                        <span>
                                <a href="https://www.csdn.net/gather_13/MtzaUgysLWRvd25sb2Fk.html" target="_blank">
                                c# 全局检测鼠标位置</a>
                            </span>
                                                        <span>
                                <a href="https://www.csdn.net/gather_11/MtzaUgzsLWRvd25sb2Fk.html" target="_blank">
                                c# js popup</a>
                            </span>
                                                                            </div>
                    </div>
                    </div>
                                    <div class="recommend-loading-box">
                    <img src='https://csdnimg.cn/release/phoenix/images/feedLoading.gif'>
                </div>
                <div class="recommend-end-box">
                    <p class="text-center">没有更多推荐了，<a href="https://blog.csdn.net/" class="c-blue c-blue-hover c-blue-focus">返回首页</a></p>
                </div>
            </div>
                            <div class="template-box">
                    <span>©️2019 CSDN</span><span class="point"></span>
                <span>皮肤主题: 深蓝海洋</span>
                <span> 设计师:
                                            CSDN官方博客                                    </span>
                </div>
                    </main>
        <aside class="blog_container_aside">
	<!--主页引入-->

    <div id="asideProfile" class="aside-box">
    <!-- <h3 class="aside-title">个人资料</h3> -->
    <div class="profile-intro d-flex">
        <div class="avatar-box d-flex justify-content-center flex-column">
            <a href="https://blog.csdn.net/weixin_38305440"  data-report-click='{"mod":"popu_379","dest":"https://blog.csdn.net/weixin_38305440"}'>
                <img src="https://profile.csdnimg.cn/7/4/5/3_weixin_38305440" class="avatar_pic" username='weixin_38305440'>
                                    <img src="https://g.csdnimg.cn/static/user-reg-year/1x/3.png" class="user-years">
                            </a>
                    </div>
        <div class="user-info d-flex flex-column profile-intro-name-box">
            <div>
                                <span class="name csdn-tracking-statistics tracking-click "   data-report-click='{"mod":"popu_379","dest":"https://blog.csdn.net/weixin_38305440"}' username='weixin_38305440'>
                    <a href="https://blog.csdn.net/weixin_38305440" class="" id="uid" title='Wanght6'>
                    Wanght6                    </a>
                </span>
            </div>
            <div class="profile-intro-name-boxFooter">
                                                <span class="personal-home-page" style='right:-96px;'><a target="_blank" href="https://me.csdn.net/weixin_38305440">TA的个人主页 ></a></span>
                            </div>
        </div>
    </div>
    <div class="data-info d-flex item-tiling">
                <dl class="text-center" title="11">
                            <dt><a href="https://blog.csdn.net/weixin_38305440" data-report-query="t=1">原创</a></dt>
                <dd><a href="https://blog.csdn.net/weixin_38305440" data-report-query="t=1"><span class="count">11</span></a></dd>
                    </dl>
        <dl class="text-center" id="fanBox" title="3158">
            <dt>粉丝</dt>
            <dd><span class="count" id="fan">3158</span></dd>
        </dl>
        <dl class="text-center" title="619">
            <dt>获赞</dt>
            <dd><span class="count">619</span></dd>
        </dl>
        <dl class="text-center" title="14">
            <dt>评论</dt>
            <dd><span class="count">14</span></dd>
        </dl>
        <dl class="text-center" title="78818">
            <dt>访问</dt>
            <dd><span class="count">7万+</span></dd>
        </dl>
    </div>
    <div class="grade-box clearfix">
        <dl class="aside-box-footerClassify">
            <dt>等级:</dt>
            <dd>
                <a href="https://blog.csdn.net/home/help.html#level" title="4级,点击查看等级说明" target="_blank">
                    <svg class="icon icon-level" aria-hidden="true">
                        <use xlink:href="#csdnc-bloglevel-4"></use>
                    </svg>
                </a>
            </dd>
        </dl>
        <dl title="22653">
            <dt>周排名:</dt>
            <dd>
                <a class="grade-box-rankA" href="https://blog.csdn.net/rank/writing_rank" target="_blank">
                    2万+                </a>
            </dd>
        </dl>
        <dl>
            <dt>积分:</dt>
            <dd title="1259">
                1259            </dd>
        </dl>
        <dl title="51189">
            <dt>总排名:</dt>
            <dd>
                <a class="grade-box-rankA" href="https://blog.csdn.net/rank/writing_rank_total" target="_blank">
                    5万+                </a>
            </dd>
        </dl>
    </div>
    <div class="aside-box-footer">
                    <div class="badge-box d-flex">
                <div class="profile-medal">勋章:</div>
                <div class="badge d-flex">
                                                                                                        <div class="icon-badge" title="持之以恒">
                                    <div class="mouse-box">
                                        <img src="https://g.csdnimg.cn/static/user-medal/chizhiyiheng.png" alt="">
                                        <div class="icon-arrow"></div>
                                    </div>
                                    <div class="grade-detail-box">
                                        <div class="pos-box">
                                            <div class="left-box d-flex justify-content-center align-items-center flex-column">
                                                <img src="https://g.csdnimg.cn/static/user-medal/chizhiyiheng.png" alt="">
                                                <p>持之以恒</p>
                                            </div>
                                            <div class="right-box">
                                                授予每个自然月内发布4篇或4篇以上原创或翻译IT博文的用户。不积跬步无以至千里，不积小流无以成江海，程序人生的精彩需要坚持不懈地积累！                                            </div>
                                        </div>
                                    </div>
                                </div>
                                                                                                                <div class="icon-badge" title="勤写标兵Lv2">
                                    <div class="mouse-box">
                                        <img src="https://g.csdnimg.cn/static/user-medal/qixiebiaobing-2.png" alt="">
                                        <div class="icon-arrow"></div>
                                    </div>
                                    <div class="grade-detail-box">
                                        <div class="pos-box">
                                            <div class="left-box d-flex justify-content-center align-items-center flex-column">
                                                <img src="https://g.csdnimg.cn/static/user-medal/qixiebiaobing-2.png" alt="">
                                                <p>勤写标兵Lv2</p>
                                            </div>
                                            <div class="right-box">
                                                授予每个自然周发布4篇到6篇原创IT博文的用户。本勋章将于次周周三上午根据用户上周的博文发布情况由系统自动颁发。                                            </div>
                                        </div>
                                    </div>
                                </div>
                                                                                        </div>
                <script>
                    (function($) {
                        setTimeout(function() {
                            $('div.icon-badge.show-moment').removeClass('show-moment');
                        }, 5000);
                    })(window.jQuery)
                </script>
            </div>
                
    </div>
        <div class="profile-intro-name-boxOpration">
        <div class="opt-letter-watch-box">
                            <a class="attented personal-watch bt-button" id="btnAttent" data-report-click='{"mod":"popu_379"}'>已关注</a>
                    </div>
        <div class='opt-letter-watch-box'>
            <a class="bt-button btn-red-hollow personal-letter" href=https://im.csdn.net/im/main.html?userName=weixin_38305440 target="_blank" rel="noopener">私信</a>
        </div>
    </div>
    </div>
<script>
    function watchBtnChange(flag, username) {
        $('span.blog-expert-button-follow').each(function(index) {
            if (flag) {
                if ($(this).attr("data-name") == username) {
                    $(this).html('<span class="hover-hide">已关注</span><span class="hover-show">取消</span>').removeClass('btn-red-follow').addClass('btn-gray-follow attented');
                }
            } else {
                if ($(this).attr("data-name") == username) {
                    $(this).html("关注").addClass('btn-red-follow').removeClass('btn-gray-follow attented');
                }
            }
        })
        if (username == $('p.csdn-tracking-statistics').attr("username")) {
            if (flag) {
                $('#btnAttent').addClass("attented").text("已关注").removeClass('btn-red-hollow').addClass('btn-gray-hollow');
                changeFans(1)
            } else {
                $('#btnAttent').text("关注").addClass('btn-red-hollow').removeClass('btn-gray-hollow attented');
                changeFans(-1)
            }
        }

    }

    function changeFans(num) {
        if ($('#fan').text().indexOf('+') < 0) {
            $('#fan').text(parseInt($('#fan').text()) + num);
        } else {
            $('#fanBox').attr('title', parseInt($('#fanBox').attr('title')) + num);
        }
    }
    window.csdn = window.csdn ? window.csdn : {};
    window.csdn.watchBtnChange = watchBtnChange;
</script><div id="asideNewArticle" class="aside-box">
    <h3 class="aside-title">最新文章</h3>
    <div class="aside-content">
        <ul class="inf_list clearfix">
                        <li class="clearfix">
                <a data-report-click='{"mod":"popu_382","dest":"https://blog.csdn.net/weixin_38305440/article/details/103965462"}' href="https://blog.csdn.net/weixin_38305440/article/details/103965462" target="_blank" >
                                        k8s部署Spring Cloud应用                </a>
            </li>
                        <li class="clearfix">
                <a data-report-click='{"mod":"popu_382","dest":"https://blog.csdn.net/weixin_38305440/article/details/103709712"}' href="https://blog.csdn.net/weixin_38305440/article/details/103709712" target="_blank" >
                                        Maven配置 - settings.xml                </a>
            </li>
                        <li class="clearfix">
                <a data-report-click='{"mod":"popu_382","dest":"https://blog.csdn.net/weixin_38305440/article/details/103709420"}' href="https://blog.csdn.net/weixin_38305440/article/details/103709420" target="_blank" >
                                        Lombok插件安装                </a>
            </li>
                        <li class="clearfix">
                <a data-report-click='{"mod":"popu_382","dest":"https://blog.csdn.net/weixin_38305440/article/details/103709067"}' href="https://blog.csdn.net/weixin_38305440/article/details/103709067" target="_blank" >
                                        STS 安装                </a>
            </li>
                        <li class="clearfix">
                <a data-report-click='{"mod":"popu_382","dest":"https://blog.csdn.net/weixin_38305440/article/details/103377854"}' href="https://blog.csdn.net/weixin_38305440/article/details/103377854" target="_blank" >
                                        Spring Cloud入门操作手册(Greenwich)                </a>
            </li>
                    </ul>
    </div>
</div>
    <div id="asideCategory" class="aside-box flexible-box"
         style="display:block!important;">
    <h3 class="aside-title">分类专栏</h3>
    <div class="aside-content">
        <ul>
                            <li class="">
                                        <a class="clearfix" 
                                                    data-report-click='{"mod":"popu_537","strategy":"","dest":"https://blog.csdn.net/weixin_38305440/category_9463504.html"}'
                            data-report-view='{"mod":"popu_537","strategy":"","dest":"https://blog.csdn.net/weixin_38305440/category_9463504.html"}'
                                               href="https://blog.csdn.net/weixin_38305440/category_9463504.html">
                                                    <img src="https://img-blog.csdnimg.cn/20190918140037908.png" alt="">
                                                <!--####是否付费-->
                        <span class="title oneline"><span class="text">Spring Cloud</span>
                                                    </span>
                        <!--####是否付费-->
                                                    <span class="count float-right">3篇</span>
                                            </a>
                </li>
                            <li class="">
                                        <a class="clearfix" 
                                                    data-report-click='{"mod":"popu_537","strategy":"","dest":"https://blog.csdn.net/weixin_38305440/category_9476658.html"}'
                            data-report-view='{"mod":"popu_537","strategy":"","dest":"https://blog.csdn.net/weixin_38305440/category_9476658.html"}'
                                               href="https://blog.csdn.net/weixin_38305440/category_9476658.html">
                                                    <img src="https://img-blog.csdnimg.cn/20190927151132530.png" alt="">
                                                <!--####是否付费-->
                        <span class="title oneline"><span class="text">Kubernetes</span>
                                                    </span>
                        <!--####是否付费-->
                                                    <span class="count float-right">2篇</span>
                                            </a>
                </li>
                            <li class="">
                                        <a class="clearfix" 
                                                    data-report-click='{"mod":"popu_537","strategy":"","dest":"https://blog.csdn.net/weixin_38305440/category_9621775.html"}'
                            data-report-view='{"mod":"popu_537","strategy":"","dest":"https://blog.csdn.net/weixin_38305440/category_9621775.html"}'
                                               href="https://blog.csdn.net/weixin_38305440/category_9621775.html">
                                                    <img src="https://img-blog.csdnimg.cn/20190918140158853.png" alt="">
                                                <!--####是否付费-->
                        <span class="title oneline"><span class="text">开发工具</span>
                                                    </span>
                        <!--####是否付费-->
                                            </a>
                </li>
                            <li class="">
                                        <a class="clearfix" 
                                                    data-report-click='{"mod":"popu_537","strategy":"","dest":"https://blog.csdn.net/weixin_38305440/category_9621788.html"}'
                            data-report-view='{"mod":"popu_537","strategy":"","dest":"https://blog.csdn.net/weixin_38305440/category_9621788.html"}'
                                               href="https://blog.csdn.net/weixin_38305440/category_9621788.html">
                                                    <img src="https://img-blog.csdnimg.cn/20190918135101160.png" alt="">
                                                <!--####是否付费-->
                        <span class="title oneline"><span class="text">Maven</span>
                                                    </span>
                        <!--####是否付费-->
                                                    <span class="count float-right">1篇</span>
                                            </a>
                </li>
                            <li class="">
                                        <a class="clearfix" 
                                                    data-report-click='{"mod":"popu_537","strategy":"","dest":"https://blog.csdn.net/weixin_38305440/category_9621727.html"}'
                            data-report-view='{"mod":"popu_537","strategy":"","dest":"https://blog.csdn.net/weixin_38305440/category_9621727.html"}'
                                               href="https://blog.csdn.net/weixin_38305440/category_9621727.html">
                                                    <img src="https://img-blog.csdnimg.cn/20190918140158853.png" alt="">
                                                <!--####是否付费-->
                        <span class="title oneline"><span class="text">Spring Boot</span>
                                                    </span>
                        <!--####是否付费-->
                                                    <span class="count float-right">1篇</span>
                                            </a>
                </li>
                            <li class="">
                                        <a class="clearfix" 
                                                    data-report-click='{"mod":"popu_537","strategy":"","dest":"https://blog.csdn.net/weixin_38305440/category_9476424.html"}'
                            data-report-view='{"mod":"popu_537","strategy":"","dest":"https://blog.csdn.net/weixin_38305440/category_9476424.html"}'
                                               href="https://blog.csdn.net/weixin_38305440/category_9476424.html">
                                                    <img src="https://img-blog.csdnimg.cn/20190927151124774.png" alt="">
                                                <!--####是否付费-->
                        <span class="title oneline"><span class="text">Docker</span>
                                                    </span>
                        <!--####是否付费-->
                                                    <span class="count float-right">2篇</span>
                                            </a>
                </li>
                            <li class="">
                                        <a class="clearfix" 
                                                    data-report-click='{"mod":"popu_537","strategy":"","dest":"https://blog.csdn.net/weixin_38305440/category_9475661.html"}'
                            data-report-view='{"mod":"popu_537","strategy":"","dest":"https://blog.csdn.net/weixin_38305440/category_9475661.html"}'
                                               href="https://blog.csdn.net/weixin_38305440/category_9475661.html">
                                                    <img src="https://img-blog.csdnimg.cn/20190918140012416.png" alt="">
                                                <!--####是否付费-->
                        <span class="title oneline"><span class="text">全文检索</span>
                                                    </span>
                        <!--####是否付费-->
                                                    <span class="count float-right">1篇</span>
                                            </a>
                </li>
                            <li class="">
                                        <a class="clearfix" 
                                                    data-report-click='{"mod":"popu_537","strategy":"","dest":"https://blog.csdn.net/weixin_38305440/category_9475453.html"}'
                            data-report-view='{"mod":"popu_537","strategy":"","dest":"https://blog.csdn.net/weixin_38305440/category_9475453.html"}'
                                               href="https://blog.csdn.net/weixin_38305440/category_9475453.html">
                                                    <img src="https://img-blog.csdnimg.cn/20190918140012416.png" alt="">
                                                <!--####是否付费-->
                        <span class="title oneline"><span class="text">RabbitMQ</span>
                                                    </span>
                        <!--####是否付费-->
                                                    <span class="count float-right">1篇</span>
                                            </a>
                </li>
                    </ul>
    </div>
        <p class="text-center">
        <a class="btn btn-link-blue flexible-btn" data-fbox="aside-archive">展开</a>
    </p>
    </div>
<div id="asideArchive" class="aside-box">
    <h3 class="aside-title">归档</h3>
    <div class="aside-content">
        <ul class="archive-list">
                        <!--归档统计-->
            <li>
                <a href="https://blog.csdn.net/weixin_38305440/article/month/2020/01" data-report-click='{"mod":"popu_538","dest":"https://blog.csdn.net/weixin_38305440/article/month/2020/01"}'>
                    2020年1月                    <span class="count float-right">1篇</span>
                </a>
            </li>
                        <!--归档统计-->
            <li>
                <a href="https://blog.csdn.net/weixin_38305440/article/month/2019/12" data-report-click='{"mod":"popu_538","dest":"https://blog.csdn.net/weixin_38305440/article/month/2019/12"}'>
                    2019年12月                    <span class="count float-right">4篇</span>
                </a>
            </li>
                        <!--归档统计-->
            <li>
                <a href="https://blog.csdn.net/weixin_38305440/article/month/2019/11" data-report-click='{"mod":"popu_538","dest":"https://blog.csdn.net/weixin_38305440/article/month/2019/11"}'>
                    2019年11月                    <span class="count float-right">3篇</span>
                </a>
            </li>
                        <!--归档统计-->
            <li>
                <a href="https://blog.csdn.net/weixin_38305440/article/month/2019/10" data-report-click='{"mod":"popu_538","dest":"https://blog.csdn.net/weixin_38305440/article/month/2019/10"}'>
                    2019年10月                    <span class="count float-right">3篇</span>
                </a>
            </li>
                    </ul>
    </div>
    </div>
<div id="asideHotArticle" class="aside-box">
	<h3 class="aside-title">热门文章</h3>
	<div class="aside-content">
		<ul class="hotArticle-list">
							<li>

                    <a
                    data-report-click='{"mod":"popu_541","dest":"https://blog.csdn.net/weixin_38305440/article/details/102775484"}' 
                     href="https://blog.csdn.net/weixin_38305440/article/details/102775484" >
                                                Spring Cloud入门操作手册(Hoxton)                    </a>
					<p class="read">阅读数 <span>41533</span></p>
				</li>
							<li>

                    <a
                    data-report-click='{"mod":"popu_541","dest":"https://blog.csdn.net/weixin_38305440/article/details/102810522"}' 
                     href="https://blog.csdn.net/weixin_38305440/article/details/102810522" >
                                                RabbitMQ                    </a>
					<p class="read">阅读数 <span>8075</span></p>
				</li>
							<li>

                    <a
                    data-report-click='{"mod":"popu_541","dest":"https://blog.csdn.net/weixin_38305440/article/details/102810509"}' 
                     href="https://blog.csdn.net/weixin_38305440/article/details/102810509" >
                                                Lucene Solr 811                    </a>
					<p class="read">阅读数 <span>5343</span></p>
				</li>
							<li>

                    <a
                    data-report-click='{"mod":"popu_541","dest":"https://blog.csdn.net/weixin_38305440/article/details/102810532"}' 
                     href="https://blog.csdn.net/weixin_38305440/article/details/102810532" >
                                                Docker                    </a>
					<p class="read">阅读数 <span>4374</span></p>
				</li>
							<li>

                    <a
                    data-report-click='{"mod":"popu_541","dest":"https://blog.csdn.net/weixin_38305440/article/details/102810548"}' 
                     href="https://blog.csdn.net/weixin_38305440/article/details/102810548" >
                                                Kubernetes                    </a>
					<p class="read">阅读数 <span>3916</span></p>
				</li>
					</ul>
	</div>
</div>
	<div id="asideFooter">
			
		<div class="aside-box">
			<div id="kp_box_57" data-pid="57"><script async src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<!-- 博客内页左下视窗-20181130 -->
<ins class="adsbygoogle"
     style="display:inline-block;width:300px;height:250px"
     data-ad-client="ca-pub-1076724771190722"
     data-ad-slot="1894159733"></ins>
<script>
(adsbygoogle = window.adsbygoogle || []).push({});
</script><img class="pre-img-lasy" data-src="https://kunyu.csdn.net/1.png?p=57&a=707&c=0&k=&d=1&t=3&u=29de51d8a8a746d38cb2355288244f4d"></div>		</div>
				<div class="aside-box">
			<div class="persion_article">
			</div>
		</div>
	</div>
</aside>
<script src="https://csdnimg.cn/pubfooter/js/publib_footer-1.0.3.js" data-isfootertrack="false" type="text/javascript"></script>
<script>
	$("a.flexible-btn").click(function(){
		$(this).parents('div.aside-box').removeClass('flexible-box');
		$(this).parents("p.text-center").remove();
	})
</script>
<script src="https://g.csdnimg.cn/user-tooltip/1.9/user-tooltip.js"  type="text/javascript"></script>
    </div>
                 <div class="recommend-right  align-items-stretch clearfix" data-type="recommend" style="display: none">
        <aside class="recommend-right_aside">
            <div id="recommend-right" style="height:100%;">
                <ul class="recommend-fixed-box">
                    
                </ul>
            </div>    
        </aside>    
    </div> 

    </div>

<div class="mask-dark"></div>
<div class="tool-box vertical">
	<ul class="meau-list">
		<li class="btn-like-box long-width">
			<button class=" long-height hover-box btn-like " title="点赞">
				<svg class="icon active hover-hide" aria-hidden="true">
					<use xlink:href="#csdnc-thumbsup-ok"></use>
				</svg>
				<svg class="icon no-active hover-hide" aria-hidden="true">
					<use xlink:href="#csdnc-thumbsup"></use>
				</svg>
				<span class="hover-show text-box text">
					<span class="no-active">点赞</span>
					<span class="active">取消点赞</span>
				</span>
				<p id="supportCount">75</p>	
			</button>
		</li>
		<li class="to-commentBox" id = 'sharePost' data-report-click='{"mod":"popu_794","dest":"https://blog.csdn.net/weixin_38305440/article/details/102810522"}'>
			<a class="btn-comments low-height hover-box" >
				<svg class="icon hover-hide" aria-hidden="true" style="padding-top: 3px;">
					<use xlink:href="#icon-csdnc-fenxiang"></use>
				</svg>
				<span class="hover-show text">海报</span>
				<p class="">
				</p>
			</a>
		</li>
		<li class="to-commentBox">
						<a class="btn-comments low-height hover-box" title="写评论" href="#commentBox">
				<svg class="icon hover-hide" aria-hidden="true">
					<use xlink:href="#csdnc-comments"></use>
				</svg>
				<span class="hover-show text">评论</span>
				<p class="">
										</p>
			</a>
		</li>
		<li class="toc-container-box" id="liTocBox">
			<a class="btn-toc low-height hover-box btn-comments" title="目录">
				<svg class="icon hover-hide" aria-hidden="true">
					<use xlink:href="#csdnc-contents"></use>
				</svg>
				<span class="hover-show text">目录</span>
			</a>
			<div class="toc-container">
				<div class="pos-box">
					<div class="icon-arrow"></div>
					<div class="scroll-box">
						<div class="toc-box"></div>
					</div>
				</div>
				<div class="opt-box">
					<button class="btn-opt prev nomore" title="向上">
						<svg class="icon" aria-hidden="true">
							<use xlink:href="#csdnc-chevronup"></use>
						</svg>
					</button>
					<button class="btn-opt next">
						<svg class="icon" aria-hidden="true">
							<use xlink:href="#csdnc-chevrondown"></use>
						</svg>
					</button>
				</div>
			</div>

		</li>
		<li>
			<a class="btn-bookmark low-height hover-box btn-comments"  data-report-click='{"mod":"popu_824"}' title="收藏">
				<svg class="icon active hover-hide" aria-hidden="true" style="padding-top: 2px;">
					<use xlink:href="#icon-shoucangjia"></use>
				</svg>
				<svg class="icon no-active hover-hide" aria-hidden="true" style="padding-top: 2px;">
					<use xlink:href="#icon-csdnc-Collection-G" ></use>
				</svg>
					<span class="hover-show text">收藏</span>
				<!-- <span class="hover-show text-box text">
					<span class="no-active">收藏</span>
					<span class="active">取消收藏</span>
				</span> -->
			</a>
		</li>
		<li class="bdsharebuttonbox">
			<div class="weixin-qr btn-comments low-height hover-box" >
				<a id="btnQrShare" class="bds_weixin clear-share-style" data-report-click='{"mod":"popu_831","dest":""}'  title="手机看"></a>
				<svg class="icon hover-hide" aria-hidden="true">
					<use xlink:href="#csdnc-usephone"></use>
				</svg>
				<span class="hover-show text text3">
					手机看
				</span>
			</div>
		</li>
							<li class="widescreen-hide">
				<a class="prev btn-comments low-height hover-box" href="https://blog.csdn.net/weixin_38305440/article/details/102810509" title="Lucene Solr 811">
					<svg class="icon hover-hide" aria-hidden="true">
						<use xlink:href="#csdnc-chevronleft"></use>
					</svg>
					<span class="hover-show text text3">上一篇</span>
				</a>
			</li>
								<li class="widescreen-hide">
			<a class="next btn-comments hover-box low-height" href="https://blog.csdn.net/weixin_38305440/article/details/102810532" title="Docker">
				<svg class="icon hover-hide" aria-hidden="true">
					<use xlink:href="#csdnc-chevronright"></use>
				</svg>
				<span class="hover-show text text3">下一篇</span>
			</a>
		</li>
						<!-- 宽屏更多按钮 -->
		<li class="widescreen-more">
			<a class="btn-comments chat-ask-button low-height hover-box" title="快问" href="#chatqa">
				<svg class="icon hover-hide" aria-hidden="true">
					<use xlink:href="#csdnc-more"></use>
				</svg>
				<span class="hover-show text">更多</span>
				
			</a>
			<ul class="widescreen-more-box">
													<li class="widescreen-more">
						<a class="btn-comments low-height hover-box" href="https://blog.csdn.net/weixin_38305440/article/details/102810509" title="Lucene Solr 811">
							<svg class="icon hover-hide" aria-hidden="true">
								<use xlink:href="#csdnc-chevronleft"></use>
							</svg>
							<span class="hover-show text text3">上一篇</span>
						</a>
					</li>
																<li class="widescreen-more">
					<a class="btn-comments hover-box low-height" href="https://blog.csdn.net/weixin_38305440/article/details/102810532" title="Docker">
						<svg class="icon hover-hide" aria-hidden="true">
							<use xlink:href="#csdnc-chevronright"></use>
						</svg>
						<span class="hover-show text text3">下一篇</span>
					</a>
				</li>
							</ul>
		</li>
        		<li class="to-commentBox to-reward">
			<a class="btn-comments low-height hover-box" data-report-click='{"mod":"popu_830" "dest":""}'  title="打赏">
				<svg class="hover-hide" width="24px" height="24px" viewBox="0 0 24 24" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
					<g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
						<g transform="translate(-1398.000000, -486.000000)" fill-rule="nonzero">
							<g transform="translate(1398.000000, 486.000000)">
								<path d="M0,12 C0,16.287187 2.287187,20.2487113 6,22.3923048 C9.7128129,24.5358984 14.2871871,24.5358984 18,22.3923048 C21.712813,20.2487113 24,16.287187 24,12 C24,5.37258296 18.627417,0 12,0 C5.372583,0 0,5.37258296 0,12 Z" id="路径" fill-opacity="0.3" fill="#FF5A52"></path>
								<path d="M2.09340659,11.9505494 C2.09340659,15.4721673 3.97216734,18.7262766 7.02197798,20.4870856 C10.0717886,22.2478946 13.8293103,22.2478946 16.8791209,20.4870856 C19.9289316,18.7262766 21.8076923,15.4721673 21.8076923,11.9505494 C21.8076923,6.50659974 17.3944991,2.09340659 11.9505495,2.09340659 C6.50659977,2.09340659 2.09340659,6.50659974 2.09340659,11.9505494 Z" id="路径" fill="#F63D47"></path>
								<path d="M11.3005025,5.28638434 L12.7115578,5.28638434 L12.7115578,6.87854416 L14.1105528,6.87854416 C14.4,6.39607148 14.6592965,5.89550609 14.8884422,5.37081705 L16.1849246,5.82313519 C15.99799,6.23926787 15.7929648,6.58906055 15.5758794,6.88457507 L18,6.88457507 L18,9.84575109 L16.6733668,9.84575109 L16.6733668,8.03647857 L7.33869347,8.03647857 L7.33869347,9.85781291 L6,9.85781291 L6,6.87854416 L8.51457286,6.87854416 C8.31557789,6.52875147 8.08040201,6.1910206 7.80904523,5.86535155 L9.08140703,5.4009716 C9.39497488,5.80504246 9.67236181,6.29957695 9.92562814,6.88457507 L11.3065327,6.88457507 L11.3065327,5.28638434 L11.3005025,5.28638434 Z M12.8571429,13.9657994 C12.6552823,15.5675992 12.2332101,16.6234672 11.5848095,17.1394027 C10.8813559,17.8053195 9.1991844,18.2312662 6.54441188,18.4292415 L6,17.2233922 C8.22046642,17.1394027 9.68854339,16.8454395 10.3919969,16.3415024 C11.0098127,15.8735609 11.3768319,15.0456644 11.4930547,13.8578129 L12.8571429,13.9657994 Z M16.8571429,12.1435272 L16.8571429,15.9892245 L15.5161905,15.9892245 L15.5161905,13.3067319 L9.05523809,13.3067319 L9.05523809,16.1435272 L7.71428571,16.1435272 L7.71428571,12.1435272 L16.8571429,12.1435272 L16.8571429,12.1435272 Z M8.28571429,8.71495577 L15.7142857,8.71495577 L15.7142857,11.5720986 L8.28571429,11.5720986 L8.28571429,8.71495577 L8.28571429,8.71495577 Z M14.5714286,10.4292415 L14.5714286,9.28638434 L10,9.28638434 L10,10.4292415 L14.5714286,10.4292415 Z M12.9579832,16.1435272 C14.8187275,16.4853162 16.4993998,16.9018717 18,17.3931934 L17.2436975,18.4292415 C15.635054,17.8311106 13.9783914,17.3664911 12.2857143,17.0407235 L12.9579832,16.1435272 L12.9579832,16.1435272 Z" id="形状" fill="#FFFFFF"></path>
							</g>
						</g>
					</g>
				</svg>
				<span class="hover-show text">打赏</span>
			</a>
							<div id="reward" class="reward-box">
	<p class="rewad-title">打赏<span class="reward-close"><svg t="1567152543821" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="10924" xmlns:xlink="http://www.w3.org/1999/xlink" width="12" height="12"><defs><style type="text/css"></style></defs><path d="M512 438.378667L806.506667 143.893333a52.032 52.032 0 1 1 73.6 73.621334L585.621333 512l294.485334 294.485333a52.074667 52.074667 0 0 1-73.6 73.642667L512 585.621333 217.514667 880.128a52.053333 52.053333 0 1 1-73.621334-73.642667L438.378667 512 143.893333 217.514667a52.053333 52.053333 0 1 1 73.621334-73.621334L512 438.378667z" fill="" p-id="10925"></path></svg></span></p>
	<dl>
		<dd><a href="javascript:;"><img src="https://profile.csdnimg.cn/7/4/5/3_weixin_38305440" alt=""></a></dd>
		<dt>
			<p class="blog-name">Wanght6</p>
			<p class="blog-discript">“你的鼓励将是我创作的最大动力”</p>
		</dt>
	</dl>
	<div class="money-box">
        			            	<span class="choosed choose_money" data-id="5">5C币</span>
			        							<span class="choose_money" data-id="10">10C币</span>
			        							<span class="choose_money" data-id="20">20C币</span>
			        							<span class="choose_money" data-id="50">50C币</span>
			        							<span class="choose_money" data-id="100">100C币</span>
			        							<span class="choose_money" data-id="200">200C币</span>
			        	</div>
	<div class="sure-box">
		<p class="is-have-money"><a class="reward-sure">确定</a></p>
	</div>
</div>

					</li>
        	</ul>
</div>
<div id = 'tool-post-common'>
	<div class = 'tool_post_box'>
		<img class = 'tool_post_img' src="https://csdnimg.cn/release/phoenix/write/assets/postShareBack.png" alt="">
		<div id = 'shareCode'></div>
	</div>
</div>
<div id="share-bg-shadow">
<div id="share-qrcode-box">
    <h3>分享到微信朋友圈</h3>
    <div class='qrcode-img-box'>
        <a class="btn-close">×</a>
        <div id='shareQrCode'></div>
	</div>
    <p>扫一扫，手机浏览</p>
</div>
</div>
<script>
		var imgReal = new Image();
		imgReal.src = "https://csdnimg.cn/release/phoenix/write/assets/postShareBack.png"
</script>
<script type=text/javascript crossorigin src="https://csdnimg.cn/release/phoenix/production/qrcode-7c90a92189.min.js"></script>
<script type=text/javascript crossorigin src="https://csdnimg.cn/release/phoenix/production/icon-1349369f06.js"></script>
<script src="//g.csdnimg.cn/??sharewx/1.2.1/sharewx.js" type="text/javascript"></script>
<script type="text/javascript" crossorigin src="https://g.csdnimg.cn/collection-box/1.1.7/collection-box.js"></script><script>
    var recommendCount = 78;
    recommendCount = recommendCount > 1 ? (recommendCount + (recommendCount>6 ? 2 : 1)) : recommendCount;
    var ChannelId = 0;
    var articleId = "102810522";
    var commentscount = 0;
    var islock = true;
    var curentUrl = "https://blog.csdn.net/weixin_38305440/article/details/102810522";
    var myUrl = "https://my.csdn.net/";
    //1禁止评论，2正常
    var commentAuth = 1;
    //百度搜索
    var baiduKey = "RabbitMQ_大数据_weixin_38305440的博客-CSDN博客";
    var needInsertBaidu = true;
    // 代码段样式
    var codeStyle = '';
	var highlight = ["RabbitMQ"];//高亮数组

    var share_card_url = 'https://blog.csdn.net/weixin_38305440/article/shareArticleCardPage?article_id=102810522'
    var RecommendBlogExpertList = [{"user_name":"kebi007","nick_name":"dotnet\u5168\u6808\u5f00\u53d1","avatar":"https:\/\/profile.csdnimg.cn\/3\/4\/1\/3_kebi007","is_expert":true,"article_count":140,"rank":"1000+"},{"user_name":"weixin_33701617","nick_name":"weixin_33701617","avatar":"https:\/\/profile.csdnimg.cn\/D\/2\/C\/3_weixin_33701617","is_expert":false,"article_count":4548,"rank":"\u5343\u91cc\u4e4b\u5916"},{"user_name":"hustspy1990","nick_name":"albon_arith","avatar":"https:\/\/profile.csdnimg.cn\/3\/F\/1\/3_hustspy1990","is_expert":true,"article_count":239,"rank":"2000+"},{"user_name":"weixin_41674620","nick_name":"weixin_41674620","avatar":"https:\/\/profile.csdnimg.cn\/F\/8\/F\/3_weixin_41674620","is_expert":false,"article_count":2,"rank":"\u5343\u91cc\u4e4b\u5916"},{"user_name":"csdnnews","nick_name":"CSDN\u8d44\u8baf","avatar":"https:\/\/profile.csdnimg.cn\/C\/3\/E\/3_csdnnews","is_expert":true,"article_count":5933,"rank":"\u5343\u91cc\u4e4b\u5916"},{"user_name":"xianaoshi","nick_name":"\u5413\u8111\u6e7f","avatar":"https:\/\/profile.csdnimg.cn\/B\/6\/3\/3_xianaoshi","is_expert":false,"article_count":25,"rank":"\u5343\u91cc\u4e4b\u5916"},{"user_name":"yuanziok","nick_name":"Leo.yuan","avatar":"https:\/\/profile.csdnimg.cn\/C\/E\/4\/3_yuanziok","is_expert":true,"article_count":439,"rank":"1000+"},{"user_name":"qq_40630246","nick_name":"\u5c14\u7075\u5c14\u4ebf","avatar":"https:\/\/profile.csdnimg.cn\/8\/0\/B\/3_qq_40630246","is_expert":false,"article_count":20,"rank":"\u5343\u91cc\u4e4b\u5916"},{"user_name":"shawn210","nick_name":"\u91d1\u94a9\u676f\u513f","avatar":"https:\/\/profile.csdnimg.cn\/F\/F\/1\/3_shawn210","is_expert":false,"article_count":34,"rank":"\u5343\u91cc\u4e4b\u5916"},{"user_name":"weixin_43493955","nick_name":"\u6052\u9759\u65e0\u8a00ty","avatar":"https:\/\/profile.csdnimg.cn\/6\/5\/7\/3_weixin_43493955","is_expert":false,"article_count":23,"rank":"\u5343\u91cc\u4e4b\u5916"}];
	var articleType = 1;
	var CopyrightContent = '';
</script>
<script src="https://csdnimg.cn/public/sandalstrap/1.4/js/sandalstrap.min.js"></script>
<script src="https://csdnimg.cn/release/phoenix/vendor/pagination/paging-3d3b805766.js"></script>
<div class="skin-boxshadow"></div>
<div style="display:none;">
	<img src="" onerror='setTimeout(function(){if(!/(csdn.net|iteye.com|baiducontent.com|googleusercontent.com|360webcache.com|sogoucdn.com|bingj.com|baidu.com)$/.test(window.location.hostname)){window.location.href="\x68\x74\x74\x70\x73\x3a\x2f\x2f\x77\x77\x77\x2e\x63\x73\x64\x6e\x2e\x6e\x65\x74"}},3000);'>
</div>
</body>
<script type="text/javascript" src="https://csdnimg.cn/release/phoenix/production/pc_wap_common-f91259fb12.js"></script>
<link rel="stylesheet" href="https://csdnimg.cn/release/blog_editor_html/release1.6.0/ckeditor/plugins/codesnippet/lib/highlight/styles/atom-one-light.css">
<script>
 // 全局声明
 if (window.csdn === undefined) {
      window.csdn = {};
    }
    window.csdn.sideToolbar = {
        options: {
            report:{
                isShow: true,
            },
            qr: {
                isShow: false,
            }
        }
    }
    $(function(){
        $(document).on('click',"a.option-box[data-type='report']",function() {
            window.csdn.userLogin.loadAjax(function(res){
                showReport(false,articleTitles);
            })
        });
    })
</script>
<script src="https://csdnimg.cn/release/phoenix/vendor/iconfont/csdnc-c439e66521.js"></script>
<script src="https://csdnimg.cn/release/phoenix/template/js/common-da450fe83c.min.js"></script>
<script src="https://csdnimg.cn/release/phoenix/template/js/detail-eccaa49577.min.js"></script>
	<script src="https://csdnimg.cn/release/phoenix/themes/skin-yellow/skin-yellow-e2b6be7b58.min.js"></script>
<script src="https://g.csdnimg.cn/copyright/1.0.3/copyright.js" type="text/javascript"></script>
<script type="text/javascript"  src="https://g.csdnimg.cn/??login-box/1.1.1/30/login-box.js,login-box/1.1.1/30/login-auto.js"></script>
<script>
    $(".MathJax").remove();
    if ($('div.markdown_views pre.prettyprint code.hljs').length > 0) {
        $('div.markdown_views')[0].className = 'markdown_views';
    }
</script>
<script type="text/javascript" src="https://csdnimg.cn/release/blog_mathjax/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
<script type="text/x-mathjax-config">
    MathJax.Hub.Config({
            "HTML-CSS": {
                    linebreaks: { automatic: true, width: "94%container" },
                    imageFont: null
            },
            tex2jax: {
                preview: "none"
            },
            mml2jax: {
                preview: 'none'
            }
    });
</script>
    <script src="//g.csdnimg.cn/baidu-search/1.0.2/baidu-search.js"  type="text/javascript"></script>
<script type="text/javascript" crossorigin src="https://g.csdnimg.cn/user-login/2.2.4/user-login.js"></script>
</html>

