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
	- script引入
		- 详见 **01_vue_debut/vue_import.html**。
		- <script type="text/javascript" src="../vue.js"></script>。
		-  在chrome中添加开发者工具：https://github.com/vuejs/vue-devtools
		- Vue.config 中有 production配置，将其设为false可以消除vue.js文件导致的production警告。详见文件中**script**。如果还有提示，将配置语句直接加在vue.js中：line 9282。
	- NPM 引入

- 1.2 初识 vue
	- 详见 **01_vue_debut/vue_import.html**。
	- 浏览器打开网页时，会默认去请求页签图标。
	- 创建 vue 实例。
		- const instance = new Vue({})
		- el：element用于指定当前vue实例为哪个容器服务，值通常为css内的id选择器字符串。可以直接绑定，也可以用实例的.$mount来挂载。
		- data：插值语法来引用data内的值：{{ }}。双花括号内必须写成js内表达式，如Date.now()或其他定义的variable。有**对象式**和**函数式**两种写法。
	- 想让vue工作，就必须创建一个vue实例，并且要传入一个配置对象。
	- root容器内的代码依然符合html规范，只不过混入一些特殊的vue语法。
	- root容器内的代码被称为**vue模板**。
	- vue实例与容器之间一一对应。
	- 一旦data中的数据发生改变，那么模板中用到该数据的地方也会改变。

- 1.3 模板语法
	- 详见 **01_vue_debut/vue_grammar.html**
	- 插值语法：{{}}
	- 指令语法：比如v-bind:href="url"，v-bind后执行js表达式。v-bind可简写为:。

- 1.4 数据绑定
	- 详见 **01_vue_debut/vue_data_bind.html**
	- 单向数据绑定 v-bind； data向页面单向绑定
	- 双向数据绑定 v-model： data和页面双向绑定

- 1.5 MVVM模型
	- Model-View-ViewModel
	- Model： 对应data中的数据
	- View： 模板
	- ViewModel： Vue实例对象。经常用vm来代表Vue实例。

## 数据代理 
- 2.1 Object.defineproperty方法
	- Object.defineProperty(object, 'age',{value:18})
	- 添加的属性是不能被枚举的（不参与遍历），如果想要遍历，将enumerable改为true
	- 添加的属性是不能被更改的，如果想要更改，将writable改为true
	- 添加的属性是不能被删除的，如果想删除，将configurable改为true
	- get函数会在每次读取age时返回值，所以当我们改变number时，age的值也可以跟着变
	- set函数会在每次修改age时返回值

- 2.2 什么是数据代理
	- 数据代理：通过一个对象代理对另一个对象中了属性的操作（读/写）
	```
		<script type="text/javascript">
            let obj1 = {x:100}
            let obj2 = {y:200}

            Object.defineProperty(obj2,'x',{
                get(){
                    return obj1.x
                },
                set(value){
                    obj1.x = value
                }
            })
        </script>
	```

## vue-cli

## vue-router

## vuex

## element-ui

## vue3
