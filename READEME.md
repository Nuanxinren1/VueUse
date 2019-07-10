#####    Vue的安装及使用快速入门

###  一、安装vue

1、安装node.js，安装完node.js之后，npm也会自动安装

查询是否安装成功的命令：

node -v

npm -v

2、全局安装脚手架工具vue-cli，命令如下：

npm install --global vue-cli

3、vue项目初始化命令如下，若没有安装webpack，则先安装webpack

npm install -g webpack

vue init webpack myVue

注：安装过程 中有个选项（Use ESLint to line your code ?选择 No ）

4、进入到myVue目录下，使用npm install 安装package.json包中的依赖

命令如下：

cd myVue

npm install

5、运行项目：

npm run dev

在浏览器上输入：localhost:8080，将会出现下面的vue初始页面：

6、结束项目运行：

ctrl+v，选择Y即可停止项目的运行


####    二、vue项目目录说明

build：项目构建(webpack)相关代码

config：配置目录，包括端口号等

node_modules：npm加载的项目依赖块

src：这里是我们要开发的目录，基本上要做的事情都在这个目录里。里面包含了几个目录及文件：

assets: 放置一些图片，如logo等

components：该目录里存放的我们的开发文件组件，主要的开发文件都存放在这里了

App.vue：项目入口文件

main.js：项目的核心文件

router：路由配置目录

static：放置一些静态资源文件

test：初始测试目录，可删除

.xxxx文件：这些是一些配置文件，包括语法配置，git配置等

index.html：首页入口文件

package.json：项目配置文件

README.md：项目的说明文档，markdown 格式


####    三、项目启动流程

1、在执行npm run dev的时候，会去在当前文件夹下的项目中找package.json文件,启动开发服务器，默认端口是8080；

2、找到src的main.js文件，在该文件中new Vue的实例，要加载的模板内容App；

3、App是src目录下的App.vue结尾的文件；

4、在App.vue所对应的模板当中，有一个router-view在src目录下有一个router文件夹，该文件夹有个index.js文件，该文件是配置路由词典，指定了路由地址是空，加载HelloWorld组件

### 注：vue运行是基于node环境的,构建vue框架之前,需要确保node环境安装成功。



####    四、vue组件的使用

1、在components文件夹下创建.vue结尾的文件

例如在：src/components/public/目录下新建header.vue文件

2、在路由配置文件src/router/index.js中引入组件并配置组件路由

    2.1、引入组件

    import Header from '@/components/public/header'

    2.2、配置组件路由

    {  

    path: '/header',

    name: 'header',

    component: Header

    }

3、运行项目：npm run dev

4、在浏览器中输入：localhost:8080/header 












