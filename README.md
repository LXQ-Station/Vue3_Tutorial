# Vue3_Tutorial

## 1 vue 基础

- vue是什么？

	vue是一套用于**构建用户界面**的**渐进式**JS框架：将得到的数据做成界面，自底向上逐层应用。

- vue的特点
	- 采用**组件化**模式，提高代码复用率，且让代码更好维护：Activity.vue文件中包括界面内指定组件所对应的HTML，CSS和JS代码，不同的页面单元被很好的分装；
	- **声明式**编码，让编码人员无需直接操作DOM(Document Object Model),提高开发效率；
	- 使用**虚拟DOM**+优秀的**Diff算法**，尽量复用DOM节点。

- Awesome Vue 中包含各种官方认可的第三方库。

- 1.1 vue 开发环境
	- <script>引入
		- 详见 **01_vue_debut/vue_import.html**

		- <script type="text/javascript" src="../vue.js"></script>

		- 在chrome中添加开发者工具：https://github.com/vuejs/vue-devtools

		- Vue.config 中有 production配置，将其设为false可以消除vue.js文件导致的production警告。详见文件中**script**。如果还有提示，将配置语句直接加在vue.js中：line 9282。

	- NPM 引入
- 1.2 初识 vue
	- 详见 **01_vue_debut/vue_import.html**。
	- 浏览器打开网页时，会默认去请求页签图标。
	- 创建 vue 实例。
		- const instance = new Vue({})
		- el：element用于指定当前vue实例为哪个容器服务，值通常为css内的id选择器字符串
		- data：插值语法来引用data内的值：{{ }}。双花括号内必须写成js内表达式，如Date.now()或其他定义的variable。
	- 想让vue工作，就必须创建一个vue实例，并且要传入一个配置对象。
	- root容器内的代码依然符合html规范，只不过混入一些特殊的vue语法。
	- root容器内的代码被称为**vue模板**。
	- vue实例与容器之间一一对应。
	- 一旦data中的数据发生改变，那么模板中用到该数据的地方也会改变。

- 1.3 模板语法
	- 详见 **01_vue_debut/vue_grammar.html**
	- 插值语法

## vue-cli

## vue-router

## vuex

## element-ui

## vue3
