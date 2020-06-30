# mini-app : [小程序](http://gitlab.shomop.com/shomop/doc/-/wikis/front-end/mini-app)

---

> [淘宝开放平台](https://console.open.taobao.com/?spm=a219a.7386653.0.0.6fcd669aS0EO8h#/index)

> [小程序开发说明](https://miniapp.open.taobao.com/docV3.htm?spm=a1z3lu.12103192.0.0.642328b3nUA5GB&docId=117766&docType=1)

> [官方 demo 下载](https://wirelsee-weex-tasp-public-oss.oss-cn-hangzhou.aliyuncs.com/demo.zip?spm=a1z3lu.12103192.0.0.642328b3nUA5GB&file=demo.zip)

> 开发工具 [下载](https://miniapp.open.taobao.com/docV3.htm?spm=a1z3lu.12103192.0.0.642328b3nUA5GB&docId=117780&docType=1)

> 开发工具 [使用](https://miniapp.open.taobao.com/docV3.htm?spm=a1z3lu.12103192.0.0.642328b3nUA5GB&docId=117770&docType=1)

> [多端发布](https://opendocs.alipay.com/mini/multi-platform)

> [商家应用模板](https://miniapp.open.taobao.com/doc.htm?docId=117783&docType=1)： 商家应用模板由独立于主体商家应用的第三方进行开发并发布，商家购买后实例化该模板即可作为主体商家应用使用，为用户提供完整功能，无需任何开发。

> [**开发消费者端模板**](https://miniapp.open.taobao.com/docV3.htm?docId=118455&docType=1&treeId=635)

> [各端通用组件和 API](https://opendocs.alipay.com/mini/multi-platform/common)

> [**小程序框架**](https://opendocs.alipay.com/mini/framework/overview)

> [小程序调试](https://opendocs.alipay.com/mini/ide/debug)

> **<span style="color: red;">技术栈选择</span>** - [uni-app](https://uniapp.dcloud.io/)： 开发多端小程序教程

> [uni-app 快速上手](https://uniapp.dcloud.io/quickstart)

---

## **<span style="color: red;">技术栈选择</span>** [uni-app](https://uniapp.dcloud.io/)： 开发多端小程序教程

- 工具一 [小程序开发者工具](https://help.aliyun.com/document_detail/130777.htm)

  ![打开小程序开发者工具，选择跨平台小程序 > uni-app](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/zh-CN/6859135851/p55998.png)

  uni-app 项目创建成功后，就可以开发 uni-app 跨端工程了。主要项目目录如下：

  - src/：uni-app 工程的源码目录。详细信息，请参见[uni-app 工程目录结构](<[#开发规范](https://uniapp.dcloud.io/frame?id=%E7%9B%AE%E5%BD%95%E7%BB%93%E6%9E%84)>)。
  - dist/：小程序构建的文件：
    - dev/mp-alipay：支付宝小程序结构文件。
    - dev/mp-weixin：微信小程序结构文件，需要结合 uni-app 插件使用。详细使用说明，请参见 uni-app 跨平台开发扩展使用教程。

- 工具二 [HBuilderX](https://uniapp.dcloud.io/quickstart)

  1. [创建 uni-app](https://uniapp.dcloud.io/quickstart?id=%e5%88%9b%e5%bb%bauni-app): 日常开发推荐使用 uni ui 项目模板，已内置大量常用组件
  2. [运行 uni-app](https://uniapp.dcloud.io/quickstart?id=%e8%bf%90%e8%a1%8cuni-app)

     ![在支付宝小程序开发者工具里运行：进入hello-uniapp项目，点击工具栏的运行 -> 运行到小程序模拟器 -> 支付宝小程序开发者工具，即可在支付宝小程序开发者工具里面体验uni-app。](https://img-cdn-qiniu.dcloud.net.cn/uniapp/doc/uni20190222-3.png)

- 工具三 [通过 vue-cli 命令行](https://uniapp.dcloud.io/quickstart?id=_2-%e9%80%9a%e8%bf%87vue-cli%e5%91%bd%e4%bb%a4%e8%a1%8c)

  ```
  npm install -g @vue/cli

  vue create -p dcloudio/uni-preset-vue my-project

  npm run dev:%PLATFORM%
  npm run build:%PLATFORM%
  ```

  ![项目模板](https://img.cdn.aliyun.dcloud.net.cn/guide/uniapp/h5-cli-01.png)

  - [Vue CLI - 插件和 Preset #插件](https://cli.vuejs.org/zh/guide/plugins-and-presets.html)
    `vue add eslint`

### [组件](https://uniapp.dcloud.io/component/README)

- [基础组件](https://uniapp.dcloud.io/component/README?id=%e5%9f%ba%e7%a1%80%e7%bb%84%e4%bb%b6)
- [扩展组件：uni-ui](https://uniapp.dcloud.io/component/README?id=uniui)：支持 HBuilderX 直接新建项目模板、npm 安装和单独导入个别组件等多种使用方式

### [<span style="color: red;">开发规范</span>](https://uniapp.dcloud.io/frame)

### [目录结构](https://uniapp.dcloud.io/frame?id=%E7%9B%AE%E5%BD%95%E7%BB%93%E6%9E%84)

```
┌─components            uni-app组件目录
│  └─comp-a.vue         可复用的a组件
├─hybrid                存放本地网页的目录，[详见](https://uniapp.dcloud.io/component/web-view)
├─platforms             存放各平台专用页面的目录，[详见](https://uniapp.dcloud.io/platform?id=%E6%95%B4%E4%BD%93%E7%9B%AE%E5%BD%95%E6%9D%A1%E4%BB%B6%E7%BC%96%E8%AF%91)
├─pages                 业务页面文件存放的目录
│  ├─index
│  │  └─index.vue       index页面
│  └─list
│     └─list.vue        list页面
├─static                存放应用引用静态资源（如图片、视频等）的目录，<b>注意：</b>静态资源只能存放于此
├─mycomponents          存放小程序组件的目录，[详见](https://uniapp.dcloud.io/frame?id=%E5%B0%8F%E7%A8%8B%E5%BA%8F%E7%BB%84%E4%BB%B6%E6%94%AF%E6%8C%81)
├─main.js               Vue初始化入口文件
├─App.vue               应用配置，用来配置App全局样式以及监听 [应用生命周期](https://uniapp.dcloud.io/frame?id=%E5%BA%94%E7%94%A8%E7%94%9F%E5%91%BD%E5%91%A8%E6%9C%9F)
├─manifest.json         配置应用名称、appid、logo、版本等打包信息，[详见](https://uniapp.dcloud.io/collocation/manifest)
└─pages.json            配置页面路由、导航条、选项卡等页面类信息，[详见](https://uniapp.dcloud.io/collocation/pages)

```

---

## build & run

```
# lint
npm run lint

# alibuild:mp-alipay
npm run alibuild:mp-alipay

# alidev:mp-alipay
npm run alidev:mp-alipay


# dev:mp-alipay
npm run dev:mp-alipay
```
