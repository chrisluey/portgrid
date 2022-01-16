<template>
  <div class = "test">
    <h2></h2>
    <nav class="test2">
    <router-link class="spacing" to="/"><el-icon size="30"><HomeFilled /></el-icon>Home</router-link>
                       
    <router-link class="spacing" to="/Profile"><el-icon size="30"><User /></el-icon>Profile</router-link>
    <router-link class="spacing" to=""><el-icon size="30"><Message /></el-icon>Message</router-link>
    <router-link class="spacing" to=""><el-icon size="30"><Folder /></el-icon>Projects</router-link>
    <router-link class="spacing" to=""><el-icon size="30"><Upload /></el-icon>Uploads</router-link>
    <router-link class="spacing" to=""><el-icon size="30"><Bell /></el-icon>Notifications</router-link>
    
    </nav>
  </div>
</template>

<script setup>
import { HomeFilled } from '@element-plus/icons'
import { User } from '@element-plus/icons'
import { Message } from '@element-plus/icons'
import { Bell } from '@element-plus/icons'
import { Folder } from '@element-plus/icons'
import { Upload } from '@element-plus/icons'

</script>

<style>
.spacing {
    margin-left: 20px;
    margin-right: 20px;
    color: #9593a0;
    font-size: 20px;
   padding-left:10px;
   padding-right:10px;
}
.test {
  background-color: #2d2d2d;
}
.test2 {
  margin-left: 20vw;
  margin-top: 20px;
}

</style>
