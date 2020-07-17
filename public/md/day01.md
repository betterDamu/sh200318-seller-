## day01
### @vue/cli的使用
    1. 安装 : npm i @vue/cli (如果安装过其他版本的脚手架 先要卸载他们)
    2. 初始化项目: vue create project-name
    3. vue.config.js
        是vue4.0官方脚手架的配置 (有别于webpack的配置)
        module.exports={
            lintOnSave:false,
            devServer:{
                port:8080,
                open:true
            },
            configureWebpack:{//webpack的原生配置}
        }

### mock
    1.静态mock
        devServer:
             before(app){
                app.get('/api/seller', function(req, res) {
                    res.json({
                        code:200,
                        data:data.seller
                    });
                });
                app.get('/api/goods', function(req, res) {
                    res.json({
                        code:200,
                        data:data.goods
                    });
                });
                app.get('/api/ratings', function(req, res) {
                    res.json({
                        code:200,
                        data:data.ratings
                    });
                });
             }
    2.动态mock
        DTD: 一套规则
        DPD: 占位符@
        Mock.mock(url,{
            key|DTD:"1",
            city:DPD
        })

### 搭项目环境
    路由
    数据仓库
    ajax请求
    mock