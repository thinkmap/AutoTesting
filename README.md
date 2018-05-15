# AutotestPlatform（自动化测试平台）
### 前言
    自动化测试平台，该项目于2017.10-2018.2北京深瞐科技公司在职时独立设计开发，组内测试成员使用2个月，使用现状接口规模300个/场景规模100个，UI自动化由于用例构建和维护成本过高，暂时废弃关闭入口。现已离开该公司，可提issue有时间会跟进，后续打算把接口自动化单独拿出来重构。

### 概述：
####        1、接口自动化测试模块：
            单接口录入/测试，多个接口组织场景，多个场景组成测试套，选择测试套进行任务执行和报告生成。
####         2、web界面自动化测试模块：
            通过selenium提供的api，以web页面元素的xpath来唯一定位每个对象，然后操作对象（点击，输入，移动，获取信息，校验，截屏等），来实现web界面测试自动化。为了应对前端界面的频繁变动，尽可能的减少用例的频繁修改，抽象出【页面-模板-数据】三层，动态组织用例。
        
        

### 使用指南：
<pre><code>
git clone https://github.com/qiangzhouf/AutotestPlatform.git

</pre></code>
<pre><code>
# python3.5, 安装下述三方库

pip install selenium
pip install flask
pip install flask_socketio
pip install requests
pip install uwsgi
pip install gevent

</code></pre>
<pre><code>
# 运行UI自动化测试服务

python3 server.py

</code></pre>
<pre><code>
# 启动web服务,启动时可自定义uwsgi.ini配置

cd AutotestPlatform/web
uwsgi -i uwsgi.ini

（启动成功后，即可访问自动化测试平台(admin/intedio),账户密码在wep.py里配置，暂无用户管理）
</code></pre>

### 示例：
#### 接口自动化测试模块
1、单个接口录入
![](https://github.com/qiangzhouf/AutotestPlatform/raw/master/doc/1.png)
![](https://github.com/qiangzhouf/AutotestPlatform/raw/master/doc/6.png)
![](https://github.com/qiangzhouf/AutotestPlatform/raw/master/doc/7.png)
2、多个接口组织场景
![](https://github.com/qiangzhouf/AutotestPlatform/raw/master/doc/2.png)
3、新建测试套，并添加场景
![](https://github.com/qiangzhouf/AutotestPlatform/raw/master/doc/3.png)
4、建立任务并执行
![](https://github.com/qiangzhouf/AutotestPlatform/raw/master/doc/4.png)
5、查看结果
![](https://github.com/qiangzhouf/AutotestPlatform/raw/master/doc/5.png)
#### web界面自动化测试模块
1、添加页面抽象
![](https://github.com/qiangzhouf/AutotestPlatform/raw/master/doc/11.png)
2、编写用例模板
![](https://github.com/qiangzhouf/AutotestPlatform/raw/master/doc/12.png)
3、组织用例集
![](https://github.com/qiangzhouf/AutotestPlatform/raw/master/doc/13.png)
4、建立任务并执行
![](https://github.com/qiangzhouf/AutotestPlatform/raw/master/doc/14.png)
5、查看结果
![](https://github.com/qiangzhouf/AutotestPlatform/raw/master/doc/15.png)

