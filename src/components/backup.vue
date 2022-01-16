<template>

<div>
<h2></h2>
<nav>
     <router-link class="spacing" v-for="routes in links" ``
      v-bind:key="routes.id"
      :to="`${routes.page}`">{{routes.text}}</router-link>
</nav>

</div>

</template>


<script>



export default {
    name:'navbar',
    data(){
        return{
        links:[
            {
                id:1,
                text:'Home',
                page: '/'
                
            },
            {
                id:2.,
                text:'Profile',
                page: '/Profile'
            }
        ]
    }
    }
}
</script>

<style>
.spacing {
    margin-left: 30px;
    margin-right: 30px;
    color: darkgray;
    font-size: 20px;
}

</style>