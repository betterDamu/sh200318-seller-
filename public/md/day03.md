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