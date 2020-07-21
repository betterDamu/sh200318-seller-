### 移动端页面的画法
    1.  移动端的设计稿尺寸: 750*1334 (位图像素)
        iPhone6的物理像素: 750*1334
        只有1位图像素与1物理像素保持1:1的关系时;图片才可以完美清晰的展示

    2.  设计图上所有的尺寸都得除以2之后才可以使用

    3. 像素比
           一个方向上 占满一块屏幕需要的物理像素的个数
                /
           一个方向上 占满一块屏幕需要的css像素的个数


### 1. 引入reset.css
### 2. 画webapp 要引入viewport标签
         <meta name="viewport" content="width=device-width,initial-scale=1.0">
### 3. 引入stylus
        -- style标签上得加上lang属性来表明使用什么样的预处理器
            <style scoped lang="stylus"></style>
        -- 安装必要的解析工具
            npm i stylus stylus-loader -D

### 编辑器
    vscode
    sublime
    atom

### 字体图标
    技术层面依赖于css3提供的自定义字体
        强依赖于阿里: iconfont
        自己制作字体图标:iconmoon


### css预处理器 & css后置处理器
    css预处理器: less  stylus
        css模块化语法 @import
        变量 @var $var
        嵌套 {}   缩进
        混合(当样式中存在变化的部分 那应该使用混合)
            .name(a,b){
                css声明
            }
            name(a,b)
                css声明
        继承(存静态的公共样式 那应该使用继承)
            selector{
                &:extend(类,all)
            }
            selector
                @extend(类)

    css后置处理器: postcss
        给我们的css文件做兼容性处理 参照的是can i use网站
