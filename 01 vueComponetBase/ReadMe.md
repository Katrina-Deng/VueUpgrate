# Vue 组件

### 自定义组件双绑

自定义组件支持 v-model 需要实现内部 input 的:value 和@input

v-model 默认转换是:value 和@input，如果想要修改这个行为，可以通过定义 model 选项

### 组件化的理解

#### Vue 组件化的理解

组件化是 Vue 的精髓，Vue 应用就是由一个个组件构成的。Vue 的组件化涉及到的内容非常多，当面试时被问到：谈一下你对 Vue 组件化的理解。这时候有可能无从下手，
可以从以下几点进行阐述：

- 定义：组件是可复用的 Vue 实例，准确讲它们是 VueComponent 的实例，继承自 Vue。
- 优点：从上面案例可以看出组件化可以增加代码的复用性、可维护性和可测试性。
- 使用场景：什么时候使用组件？以下分类可作为参考：
  - 通用组件：实现最基本的功能，具有通用性、复用性，例如按钮组件、输入框组件、布局组件等。
  - 业务组件：它们完成具体业务，具有一定的复用性，例如登录组件、轮播图组件。
  - 页面组件：组织应用各部分独立内容，需要时在不同页面组件间切换，例如列表页、详情页组件
- 如何使用组件
  - 定义：Vue.component()，components 选项，sfc
  - 分类：有状态组件，functional，abstract
        无状态组件可以实现更好的复用，利用父组件控制子组件的状态，而不是子组件自己控制自己控制自己的状态
  - 通信：props，$emit()/$on()，provide/inject，$children/$parent/$root/$attrs/$listeners
  - 内容分发：`<slot>，<template>，v-slot`
  - 使用及优化：is，keep-alive，异步组件
    组件的本质

vue 中的组件经历如下过程
组件配置 => VueComponent 实例 => render() => Virtual DOM=> DOM
所以组件的本质是产生虚拟 DOM
