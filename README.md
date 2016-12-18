# 高匿代理池 ProxyPool


**待做：**
- 实现Web页面交互、以及REST API交互
- 将Web服务器开/关选项添加到CUI交互界面上
- CUI交互界面上实现代理验证线程数设置
- 填写工具说明
- 开发更多代理爬虫，以实现类似Unit Testing的效果
- 多步网络连接测试，仅一次连接失败就删除的实现较不妥
- 检测X-Forwarded-For的HTTP头
- 数据库在同步操作的时候会上锁，影响效率，应想办法优化

**12月18日**
- 开发了信息池模块交互文字框架并使用MSVCRT模块进行命令行交互
- 在命令行界面添加了LOGO
- 修复了线程共享变量的Bug
- 

**12月17日**
- 将爬虫模块整合为多线程，一发制动全部
- 修复了requests代理全部失败的Bug（大小写）
- 增加并优化了验证代理时的各类异常捕捉机制
- 实现爬虫与验证程序的一体化方式(直接通过信息池模块启动)。
- 新增信息池模块，负责启动代理&爬虫模块，以及实时获取各模块状态并提供命令行交互
- 优化了等待时间以提高验证效率


**12月16日**
- 将数据库记录定义为ip、端口、协议，必须满足全部三项才可指定（比如删除）一条记录
- 实现了代理验证的多线程特性
- 优化了代理模块的部分逻辑关系
- 设计了爬虫管理模块的运行模式：单文件多函数，每个函数为一个爬虫，运行时进行多线程爬取

**（中间的这段时间我去折腾机器学习了。。。）**

**12月3日**
- 重新设计了整个高匿代理池项目的组成模块。
- 完成数据库模块的Add功能，改进Sqlite命令的去重
- 完成数据库模块的Delete及Fetch_all功能
- 完成代理库模块的check功能，暂时先使用icanhazip进行匿名检测，去除了多余的异常处理。
- 待学习：模块之间沟通的具体代码实现，是直接在模块内调用其他模块的代码还是在主程序中为各模块进行交互？

