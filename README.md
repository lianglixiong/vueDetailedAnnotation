
## 总体框架
> 一个vue-cli的项目结构如下，其中src文件夹是需要掌握的，所以本文也重点讲解其中的文件，至于其他相关文件，了解一下即可。

<img src="https://upload-images.jianshu.io/upload_images/5700710-cebf33ac17019737.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/650" alt="">

## 文件结构细分

### 1.build——[webpack配置]
>build文件主要是webpack的配置，主要启动文件是dev-server.js，当我们输入npm run dev首先启动的就是dev-server.js，它会去检查node及npm版本，加载配置文件，启动服务。

<img src="https://upload-images.jianshu.io/upload_images/5700710-a10682f111510b07.png?imageMogr2/auto-orient/" alt="">

###### 2.config——[vue项目配置]
>config文件主要是项目相关配置，我们常用的就是当端口冲突时配置监听端口，打包输出路径及命名等

<img src="https://upload-images.jianshu.io/upload_images/5700710-81ac9bc6b912d0fc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/490" alt="">

######3.node_modules——[依赖包]
>node_modules里面是项目依赖包，其中包括很多基础依赖，自己也可以根据需要安装其他依赖。安装方法为打开cmd，进入项目目录，输入npm install [依赖包名称],回车。

在两种情况下我们会自己去安装依赖：

（1）项目运行缺少该依赖包：例如项目加载外部css会用到的css-loader，路由跳转vue-loader等（安装方法示例：npm install css-loader）

（2）安装插件：如vux（基于WEUI的移动端组件库），vue-swiper（轮播插件）

注：有时会安装指定依赖版本，需在依赖包名称后加上版本号信息，如安装11.1.4版本的vue-loader，输入npm install vue-loader@11.1.4

######4.src——[项目核心文件]

>项目核心文件前面已经进行了简单的说明，接下来重点讲解main.js，App.vue,及router的index.js

######4.1 index.html——[主页]
>index.html如其他html一样，但一般只定义一个空的根节点，在main.js里面定义的实例将挂载在根节点下，内容都通过vue组件来填充

<img src="https://upload-images.jianshu.io/upload_images/5700710-61ec47ad54f1a3cf.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/415" alt="">

######4.2 App.vue——[根组件]
>一个vue页面通常由三部分组成:模板(template)、js(script)、样式(style)

<img src="https://upload-images.jianshu.io/upload_images/5700710-6b6087ca3510a257.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/546" alt="">

#######【template】