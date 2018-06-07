# <%= proName %>
<% if (description) { %>
> <%= description %>
<% } %>

![](https://biosan-saas.oss-cn-beijing.aliyuncs.com/FD/beeUi/github.jpg)

### ◆ 安装

1. 安装 bee-cli 命令行工具 `$ npm install -g @b1/bee-cli`;
2. Clone BeeUi 仓库到本地；
3. 安装依赖 `$ npm install`
4. 在 BeeUi 根目录下执行 `$ npm run dev`，生成 dist/ 目录；
5. 微信开发者工具 —— 新建一个小程序，目录指向生成的 dist/；

6. 开发自己的组件库时，删除项目的.git文件,并且remote add到你自己的git仓库中;

### ◆ 组件开发

- **新建组件**

``` bash
$ bee new *name
```

1. 该命令会在src/packages生成组件的npm库，同时生成指定模板的样例页面
2. 修改组件首页中的config.js
3. 组件开发时，注意在app.wpy中加入相应的页面

- **开发实时编译**

``` bash
$ npm run dev
```

- **发布组件**

``` bash
$ bee publish
```

1. 如果检测不到你的组件更新，使用git add 把新组件加入到索引中
2. 设置你npm publish 环境 https://blog.csdn.net/Thenightelfsnow/article/details/78573179
3. 该命令会给项目打上tag并提交，同时会publish你的组件到npm.org

### ◆ 组件使用安装

- **安装组件**

``` bash
$ npm install @b1/bee-code-input -S
```

### ◆ 使用组件

``` javascript
import wepy from 'wepy'
import BeeCodeInput from '@b1/bee-code-input'
export default class Index extends wepy.component {
  components = {
    BeeCodeInput
  }
  data = {}
  methods = {}
}
```
### ◆ 相关资源：
- [小程序开发文档](https://developers.weixin.qq.com/miniprogram/dev/)
- [wepy](https://tencent.github.io/wepy/)
- [min-cli](https://github.com/meili/min-cli)
- [minui](https://github.com/meili/minui)

### ◆ 开源协议

基于 [MIT](http://opensource.org/licenses/MIT) License，请自由的享受、参与开源。

### ◆ Contributing
1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
