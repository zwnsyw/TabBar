<template>
    <TabBar>
        <TabBarItem path="/home" activeColor="deepping">
            <img slot="item-icon" src="../../assets/img/tabbar/home.svg" alt="">
            <img slot="item-icon-active" src="../../assets/img/tabbar/home_active.svg" alt="">
            <div slot="item-text">首页</div>
        </TabBarItem>

        <TabBarItem path="/category" activeColor="deepping">
            <img slot="item-icon" src="../../assets/img/tabbar/category.svg" alt="">
            <img slot="item-icon-active" src="../../assets/img/tabbar/category_active.svg" alt="">
            <div slot="item-text">分类</div>
        </TabBarItem>

        <TabBarItem path="/cart" activeColor="bule">
            <img slot="item-icon" src="../../assets/img/tabbar/shopcart.svg" alt="">
            <img slot="item-icon-active" src="../../assets/img/tabbar/shopcart_active.svg" alt="">
            <div slot="item-text">购物车</div>
        </TabBarItem>

        <TabBarItem path="/profile" activeColor="bule">
            <img slot="item-icon" src="../../assets/img/tabbar/profile.svg" alt="">
            <img slot="item-icon-active" src="../../assets/img/tabbar/profile_active.svg" alt="">
            <div slot="item-text">我的</div>
        </TabBarItem>

        <!-- 在这里插入项目需要的 TabBarItem，path，activeColor(默认deeppink)-->

    </TabBar>
</template>

<script>
import TabBar from "./TabBar"
import TabBarItem from "./TabBarItem"

export default {
    name: "MainTabBar",
    components:{
        TabBar,
        TabBarItem,
    }

}
</script>

<style scoped>

</style>