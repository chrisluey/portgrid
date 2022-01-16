<template>
  <div>
    <h2></h2>
    <nav>
    <img src="@/assets/logo.png" alt="logo" style="width:100px;height:100px; margin-right: 605px">

    <router-link class="spacing" to="/"><el-icon size="20"><HomeFilled /></el-icon>Home</router-link>
                       
    <router-link class="spacing" to="/Profile"><el-icon size="20"><User /></el-icon>Profile</router-link>
    <router-link class="spacing" to=""><el-icon size="20"><Message /></el-icon>Message</router-link>
    <router-link class="spacing" to=""><el-icon size="20"><Folder /></el-icon>Projects</router-link>
    <router-link class="spacing" to=""><el-icon size="20"><Bell /></el-icon>Notifications</router-link>
    <router-link class="spacing" to=""><el-icon size="20"><Tools /></el-icon>Setting</router-link>
    </nav>
  </div>
</template>

<script setup>
import { HomeFilled } from '@element-plus/icons'
import { User } from '@element-plus/icons'
import { Message } from '@element-plus/icons'
import { Bell } from '@element-plus/icons'
import { Folder } from '@element-plus/icons'
import { Tools } from '@element-plus/icons'
</script>

<style>
.spacing {
    margin-left: 30px;
    color: darkgray;
    font-size: 20px;
   padding-left:30px;
   padding-right:30px;
}

</style>
