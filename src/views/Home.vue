<template>
  <div>
    <h1>Welcome</h1>
    <nav>
      <el-button style="background-color:black;"><navbar></navbar></el-button>
    </nav>
    <p>This page no longer exists or was moved to another location.</p>
  </div>
</template>



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