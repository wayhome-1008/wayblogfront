<template>
    <!-- 外层容器 -->
    <el-container>
    
        <!-- 左边侧边栏 -->
        <el-aside>
             <AdminMenu></AdminMenu>
        </el-aside>
        
      <!-- 右边主内容区域 -->
        <el-container>
            <!-- 顶栏容器 -->
            <el-header>
                <AdminHeader></AdminHeader>
            </el-header>
            
            <el-main>
              <!-- 标签导航栏 -->
                <AdminTagList></AdminTagList>

                <!-- 主内容（根据路由动态展示不同页面） -->
                <router-view></router-view>
            </el-main>
            
            <!-- 底栏容器 -->
            <el-footer>
                <AdminFooter></AdminFooter>
            </el-footer>
        </el-container>
    </el-container>
</template>
<script setup>
// 引入组件
import AdminFooter from './components/AdminFooter.vue';
import AdminHeader from './components/AdminHeader.vue';
import AdminMenu from './components/AdminMenu.vue';
import AdminTagList from './components/AdminTagList.vue';
//初始化的骨架边距会有空白 Element Plus 组件样式导致的重写.el-header padding=0
</script>
<style scoped>
.el-header {
    padding: 0!important;
}
</style>