# TabBar
封装Vue的TabBar公共组件

一、实现简单思路
        1. 在页面底部有一个单独的TabBar组件
            1.1自定义TabBar组件，在APP中使用
            1.2让TabBar出于底部，并且设置相关的样式
            
        2.TabBar中显示的内容由外界决定
            2.1定义插槽
            2.2flex布局平分TabBar
            
        3.自定义TabBarItem，可以传入 图片和文字
            3.1定义TabBarItem，并且定义两个插槽：图片、文字。
            3.2给两个插槽外层包装div，用于设置样式。
            3.3填充插槽，实现底部TabBar的效果
            
        4.传入 高亮图片
            4.1定义另外一个插槽，插入active-icon的数据
            4.2定义一个变量isActive，通过v-show来决定是否显示对应的icon
            
        5.TabBarItem绑定路由数据
            5.1安装路由：npm install vue-router —save
            5.2完成router/index.js的内容，以及创建对应的组件
            5.3main.js中注册router
            5.4APP中加入<router-view>组件
            
        6.点击item跳转到对应路由，并且动态决定isActive
            6.1监听item的点击，通过this.$router.replace()替换路由路径
            6.2通过this.$route.path.indexOf(this.link) !== -1来判断是否是active
            
        7.动态计算active样式
            7.1封装新的计算属性：this.isActive ? {'color': 'red'} : {}
            
二、使用
            1. App.vue里面导入MainTabBar，在<template><div> <main-tab-bar></main-tab-bar>  </div></template>
            1.1在MainTabBar里面填充插槽
                例如：
                          <TabBarItem path="/home" activeColor="deepping">
                              <img slot="item-icon" src="~assets/img/tabbar/home.svg" alt="">
                              <img slot="item-icon-active" src="~assets/img/tabbar/home_active.svg" alt="">
                              <div slot="item-text">首页</div>
                          </TabBarItem>
                          
三、效果预览
                <img src="https://img2018.cnblogs.com/common/1585478/202002/1585478-20200216150525236-1898652490.gif" width = "200" height = "320" div align=left />





            
