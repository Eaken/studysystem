因为本项目性质特殊，所以我不会将源码公开，以免不法分子窃取个人信息或随意提交参数篡改信息，有看源码需求或其它需求的可以联系我QQ：1063874640。

本项目教务系统的登录是模拟浏览器登录，使用okhttp3框架实现。以下简述模拟登录过程：   
    1.访问学校的“webvpn”网页，验证账号密码。   
    2.拿着验证完账号密码的正确cookie再去访问“webvpn”页面下的教务系统（一般cookie的存取是根据网址的域名（host）来的，这里我们要拿着域名     为“ http://webvpn.jxust.edu.cn ”的cookie去访问“ http://jw.webvpn.jxust.edu.cn ”，否则后者是没办法判断你是否验证了“webvpn”页面的）。   
    3.模拟登录的最后一步，就是提交账号密码给教务系统了。    
    4.以上所有步骤cookie都要随时更新。实际的参数提交远不止这么简单，各个页面还有隐藏参数需要提交，这些隐藏参数可以使用浏览器开发者工具进行查看。
  
登录完毕后，就是拿着cookie去访问教务系统的各种页面，用爬虫将数据爬取下来（有些页面的数据是教务系统动态访问服务端获取json数据再解析后得到的，这时你可以直接访问获取json数据的网址来拿数据），再进行安卓界面适配，一个属于自己的教务系统就有了。
