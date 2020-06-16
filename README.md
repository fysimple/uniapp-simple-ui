<!-- 项目描述 -->

## 使用uniapp框架，总结常规用到的样式，提取公用变量、样式、组件等
## 界面效果通过 npm 引用第三方组件

<!-- npm 引用方式 -->
## 1、进入项目目录：npm init -y
## 2、安装uni-ui：npm install @dcloudio/uni-ui
## 3、组件引用:
```import { uniBadge } from '@dcloudio/uni-ui';
<!-- 或 import uniBadge from '@dcloudio/uni-ui/lib/uni-badge/uni-badge.vue'; -->
```export default{
	components:{ uniBadge }
}