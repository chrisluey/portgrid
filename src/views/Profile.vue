<template>
  <div>
    <h1>Profile</h1>
    <nav>
      <el-button size="large" style="background-color:black"><navbar></navbar></el-button>
    </nav>
    <p>This page no longer exists or was moved to another location.</p>
    <el-button type="primary"> Element UI </el-button>
    <div class = "left-panel">
    </div>
    <div class = "profile-panel">

        </div>
  </div>
</template>

<style scoped>
.left-panel {
    width: 200px;
    position: fixed;
    background-color: #edebe8;
    height: 100%;
}
</style>

<script>
import navbar from "../components/navbar.vue"
import Navbar from "../components/navbar.vue"
export default{
    name: "Home",
    componets: {
        "navbar": navbar
    },
    components: { Navbar }
}
</script>