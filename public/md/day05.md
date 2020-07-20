### better-scroll最基本的使用
    官方文档: https://ustbhuangyi.github.io/better-scroll/doc/zh-hans/#better-scroll%20%E6%98%AF%E4%BB%80%E4%B9%88
    html结构
        <div id="wrap">  //滑屏区域
            <ul class="list">//滑屏元素
                ...
            </ul>
        </div>
    安装better-scroll : npm i better-scroll@1.15.0
    使用:
        import BScroll from "better-scroll";
        new BScroll(滑屏区域对应的dom节点)

### better-scroll API
    配置
        this.BScroll = new BScroll(dom,{
            probeType:3, //決定了scroll事件的派发时机
            click:ture //派发原生的click事件
        })
    方法
        this.BScroll.scrollTo(x, y, time, easing)
        this.BScroll.scrollToElement(el, time, offsetX, offsetY, easing)
    事件
        this.BScroll.on("scroll",({x,y})=>{//x,y代表元素滑动的实时距离})


### vm.$nextTick
    vue中数据产生改变时;改变的数据对应的界面的更新不是实时的!
        当我们需要进行dom操作时; 我们一定要在改变的数据完成后
        注册nextTick 在nextTick的回调中在进行dom操作(这个时候的dom操作是百分百安全的)


### goods布局
    三列布局 / 两列布局
### goods中的右侧列表 联动 左侧列表
    右侧列表 同步 左侧列表
    左侧列表 同步 右侧列表


