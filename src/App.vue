<template>
  <router-view />
  <navbar></navbar>
</template>

<script>
import navbar from "./components/navbar.vue"



export default{
  name:'app',
  componets:{
    'navbar' : navbar
  }
}
</script>
