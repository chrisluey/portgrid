<script setup>
import { List, Menu, Plus, Edit } from '@element-plus/icons-vue'
</script>

<template>
<el-header class="placeholder_header"> 
    <el-container>
    <img src="@/assets/logo.png" alt="logo" style="width:100px;height:100px;">
    <nav>
      <navbar></navbar>
    </nav>
    </el-container>
    </el-header>
  <el-container class="main_container">
      
    
    <!-- <el-button type="primary"> Element UI </el-button> -->
    <el-aside class="left-panel">
        <el-scrollbar>
            <el-menu active-text-color="#dfdfe3">
                <el-menu-item index="1">
                    Work Projects
                </el-menu-item>
                <el-menu-item index="2">
                    School Projects
                </el-menu-item>
                <el-menu-item index="3">
                    Personal Projects
                </el-menu-item>
            </el-menu>
        </el-scrollbar>
    </el-aside>
    <el-main class="main-panel">
        <el-scrollbar >
            <el-container class="profile_container" direction="vertical">
                <el-header class="profile_accent">

                    </el-header>
                <h3>Generic Name </h3>
                <h5> Student<br>Vancouver, BC </h5>
                <h4>About Me </h4>
                <p>Some stuff bla a lot of stuff, student stuff, I love computer science wahoo</p>

            </el-container>
            <el-header class="project_header">
                <h3>Work Projects<el-icon :size="25" style="margin-left: 605px" color="#8f8e8c"><List />
                </el-icon><el-icon :size="25" style="margin-left: 5px" color="#DADADA"><Menu />
                </el-icon><el-icon :size="25" style="margin-left: 5px" color="#DADADA"><Plus /></el-icon>    </h3>                
            </el-header>
            
            <el-container class="project_container" direction="vertical">
                <el-container>
                    <el-aside class="project-image">
                    <img style="max-height:50px;max-width:50px" src="../data/images/startup-2561668-2140274.webp">
                    </el-aside>
                    <el-main class="project-body">
                        <h4>Sample Project</h4>
                        <p>Startup 456 <br> January 2022 - Present </p>
                    </el-main>
                    <el-aside class="project-status in_progress">
                        <h5 >In Progress</h5>
                    </el-aside>
                    <el-aside class="project-button">
                        <el-icon :size="25" style="margin-top:5px" color="#2617b0"><Edit /></el-icon>
                    </el-aside>
                </el-container>

                <el-container>
                    <el-aside class="project-image">
                    <img style="max-height:50px;max-width:50px" src="../data/images/startup-2561668-2140274.webp">
                    </el-aside>
                    <el-main class="project-body">
                        <h4>Sample Project 2</h4>
                        <p>Startup 678 <br> April 2019 - Sept 2019</p>
                    </el-main>
                    <el-aside class="project-status completed">
                        <h5>Completed</h5>
                    </el-aside>
                    <el-aside class="project-button">
                        <el-icon :size="25" style="margin-top:5px" color="#2617b0"><Edit /></el-icon>
                    </el-aside>
                </el-container>
            </el-container>

            <el-header class="project_header">
                <h3>School Projects<el-icon :size="25" style="margin-left: 590px" color="#8f8e8c"><List />
                </el-icon><el-icon :size="25" style="margin-left: 5px" color="#DADADA"><Menu />
                </el-icon><el-icon :size="25" style="margin-left: 5px" color="#DADADA"><Plus /></el-icon>    </h3>                
            </el-header>
            
            <el-container class="project_container" direction="vertical">
                <el-container>
                    <el-aside class="project-image">
                    <img style="max-height:50px;max-width:50px" src="../data/images/6FTSBrRaQBYjEL7KusQCy3d9zxT0tkNFfyq9ylhajhA.png">
                    </el-aside>
                    <el-main class="project-body">
                        <h4>Sample School Project</h4>
                        <p>CPSC 410 <br>January 2022 - Present</p>
                    </el-main>
                    <el-aside class="project-status in_progress">
                        <h5 >In Progress</h5>
                    </el-aside>
                    <el-aside class="project-button">
                        <el-icon :size="25" style="margin-top:5px" color="#2617b0"><Edit /></el-icon>
                    </el-aside>
                </el-container>

                <el-container>
                    <el-aside class="project-image">
                    <img style="max-height:50px;max-width:50px" src="../data/images/6FTSBrRaQBYjEL7KusQCy3d9zxT0tkNFfyq9ylhajhA.png">
                    </el-aside>
                    <el-main class="project-body">
                        <h4>Sample School Project 2</h4>
                        <p>CPSC 304 <br>April 2019 - Sept 2019</p>
                    </el-main>
                    <el-aside class="project-status completed">
                        <h5>Completed</h5>
                    </el-aside>
                    <el-aside class="project-button">
                        <el-icon :size="25" style="margin-top:5px" color="#2617b0"><Edit /></el-icon>
                    </el-aside>
                </el-container>
            </el-container>

            <el-header class="project_header">
                <h3>Personal Projects<el-icon :size="25" style="margin-left: 580px" color="#8f8e8c"><List />
                </el-icon><el-icon :size="25" style="margin-left: 5px" color="#DADADA"><Menu />
                </el-icon><el-icon :size="25" style="margin-left: 5px" color="#DADADA"><Plus /></el-icon>    </h3>                
            </el-header>
            
            <el-container class="project_container" direction="vertical">
                <el-container>
                    <el-aside class="project-image">
                    <img style="max-height:50px;max-width:50px" src="../data/images/256x256bb.jpg">
                    </el-aside>
                    <el-main class="project-body">
                        <h4>Sudoku Solver</h4>
                        <p> <br> January 2022 - Present</p>
                    </el-main>
                    <el-aside class="project-status in_progress">
                        <h5 >In Progress</h5>
                    </el-aside>
                    <el-aside class="project-button">
                        <el-icon :size="25" style="margin-top:5px" color="#2617b0"><Edit /></el-icon>
                    </el-aside>
                </el-container>

                <el-container>
                    <el-aside class="project-image">
                    <img style="max-height:50px;max-width:50px" src="../data/images/6FTSBrRaQBYjEL7KusQCy3d9zxT0tkNFfyq9ylhajhA.png">
                    </el-aside>
                    <el-main class="project-body">
                        <h4>UBC Course Planner</h4>
                        <p> <br>April 2019 - Sept 2019 </p>
                    </el-main>
                    <el-aside class="project-status completed">
                        <h5>Completed</h5>
                    </el-aside>
                    <el-aside class="project-button">
                        <el-icon :size="25" style="margin-top:5px" color="#2617b0"><Edit /></el-icon>
                    </el-aside>
                </el-container>
            </el-container>

        </el-scrollbar>
    </el-main>
    <el-aside class="aside_recs">
    </el-aside>
    </el-container>
  
</template>

<style scoped>

.el-aside {
    /* position: fixed; */
    background-color: #2d2d2d;
    border: 5px #2d2d2d;
    border-radius: 5px;
    /* filter: drop-shadow(0 0 0.5rem #c7c5c3); */
    /* margin-top: 10px; */
}

.left-panel {
    width: 300px;
    height: 80%;
}

.project-image {
    width: 70px;
    height: 70px;
    margin-top: 10px;
}
.project-button {
    margin-top: 22px;
    width: 50px;
    height: 40px;
    background-color: #ffffff;
    text-align: center;
}

.project-status {
    margin-top: 20px;
    width: 100px;
    height: 40px;
    margin-right: 10px;
}

.completed {
    background-color: #2617b0;
}

.in_progress {
    background-color: #4bb543;
}

.project-status h5 {
    color: #ffffff;
    font-weight: 500;
    margin-top: 11px;
    font-size: 15px;
    text-align: center;
}

.aside_recs {
    margin-top: 35px;
    width: 300px;
}

.el-menu {
    background-color: #2d2d2d;
    margin-top: 20px;
    margin-left: 20px;
    margin-bottom: 20px;
    margin-right: 20px;    
}

/* .main_scroll {
    background-color: #000000;
} */

.profile_container {
    background-color: #2d2d2d;
    height: 50%;
    width: 100%;
    padding: 20px;
    border: 5px #2d2d2d;
    border-radius: 5px;
    margin-bottom: 5px;
    margin-top: 5px;
}

.profile_container h3 {
    color: #ffffff;
    font-size: 20px;
    font-weight: 600;
}

.profile_container p {
    color: #979797;
    font-size: 12px;
}

.profile_container h4 {
    color: #979797;
    font-size: 16px;
    font-weight: 600;
}

.profile_container h5 {
    color: #979797;
    font-size: 16px;

}

.project_header {
    margin-left: -5px;
    margin-top: 10px;
    height: 100%;
    width: 100%;
    float: "right";
}

.project_header h3 {
    color: #ffffff;
    font-size: 16px;
    font-weight: 600;
    margin-left: -15px;
    float: "right";
    margin-bottom: 5px;
}

.project_container {
    background-color: #2d2d2d;
    height: 50%;
    width: 100%;
    padding: 20px;
    border: 5px #2d2d2d;
    border-radius: 5px;
    margin-bottom: 5px;
    margin-top: 5px;
}

.project-body {
    height: 50%;
    width: 100px;
    padding: 0px;
    margin-bottom: 5px;
    margin-top: 5px;
    margin-left: 50px;
}

.project-body h4 {
    color: #ffffff;
    font-weight: 600;
    font-size: 16px;
}

.project-body p {
    color: #979797;
    font-size: 14px;
}

.project-class {
    width: 100px;
}



.main_container {
    background-color: #000000;
    height: 100%;
    position: fixed;
    width: 100%;
    font-family: Helvetica;
}

.placeholder_header {
    height: 100px;
    background-color: #2d2d2d;
    /* padding-top: 5px; */
    line-height: 60px;
}

.profile_accent {
    height: 100px;
    width: 100%;
    background-color: #ccc9c4;
    border: 5px #ccc9c4;
    border-radius: 5px;

    /* margin-bottom: 10px;  */
}

.main-panel {
    height: 80%;
    background-color: #000000;
    margin-left: 35px;
    margin-right: 35px;
    margin-top: 35px;
    border: 5px #000000;
    border-radius: 5px;
    width: 50%;

}


.el-submenu {
    /* display: block; */
}
.el-menu-item {
    color: #979797;
    font-size: 18px;
    margin-top: 10px;
    margin-bottom: 10px;
}

.el-menu-item:hover {
    background-color: #2617b0;
}

/* .el-scrollbar {
    background-color: #;
} */

</style>

<script>

import Navbar from "../components/navbar.vue"
export default{
    name: "Home",
    
    components: { Navbar }
}
</script>
