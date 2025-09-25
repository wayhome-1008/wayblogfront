<template>
    <div class="grid grid-cols-2 h-screen">
        <div class="col-span-2 order-2 md:col-span-1 md:order-1 bg-black">
            <div class="flex justify-center items-center h-full">
                左边栏
            </div>
        </div>
        <div class="col-span-2 order-1 md:col-span-1 md:order-2 bg-white">
        	<!-- flex-col 用于指定子元素垂直排列 -->
            <div class="flex justify-center items-center h-full flex-col">
                <h1>欢迎回来</h1>
                <div>
                    账号密码登录
                </div>
                <!-- 引入 Element Plus 表单组件，移动端设置宽度为 5/6，PC 端设置为 2/5 -->
                <el-form class="w-5/6 md:w-2/5">
                    <el-form-item>
                    	<!-- 输入框组件 -->
                        <el-input size="large" placeholder="请输入用户名" :prefix-icon="User" clearable/>
                    </el-form-item>
                    <el-form-item>
	                    <!-- 密码框组件 -->
                        <el-input size="large" type="password" placeholder="请输入密码" :prefix-icon="Lock" clearable/>
                    </el-form-item>
                    <el-form-item>
                    	<!-- 登录按钮，宽度设置为 100% -->
                        <el-button class="w-full" size="large" type="primary">登录</el-button>
                    </el-form-item>
                </el-form>
                
            </div>
        </div>
    </div>
</template>

<script setup>
// 引入 Element Plus 中的用户、锁图标
import { User, Lock } from '@element-plus/icons-vue'
</script>
