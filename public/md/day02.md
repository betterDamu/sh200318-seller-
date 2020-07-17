### 移动端页面的画法
    1.  移动端的设计稿尺寸: 750*1334 (位图像素)
        iPhone6的物理像素: 750*1334
        只有1位图像素与1物理像素保持1:1的关系时;图片才可以完美清晰的展示

    2.  设计图上所有的尺寸都得除以2之后才可以使用


### 1. 引入reset.css
### 2. 画webapp 要引入viewport标签
         <meta name="viewport" content="width=device-width,initial-scale=1.0">
### 3. 引入stylus
        -- style标签上得加上lang属性来表明使用什么样的预处理器
            <style scoped lang="stylus"></style>
        -- 安装必要的解析工具
            npm i stylus stylus-loader -D
