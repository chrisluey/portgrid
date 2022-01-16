<template>
   
  <div class="common-layout">
    
    <el-header>
     <el-container>
      <img src="@/assets/logo.png" alt="logo" style="width:100px;height:100px;">
     <nav>
      <navbar></navbar>
    </nav>
      </el-container> 
   
    </el-header>
    <el-container>
        <el-aside width="200px">hello</el-aside>
        <el-main>
            <el-space direction="vertical">
                <el-card class="update-card">
                  <template #header>
                    <div class="input-header">
                      <User style="width: 40px; height: 40px; margin-right: 20px" />
                      <el-input v-model="input" placeholder="Please input" />
                    </div>
                    <el-container>
                      <el-button color="#2D2D2D" type="primary">
                        Picture/Video<el-icon class="el-icon--right"><Picture /></el-icon>
                      </el-button>
                      <el-dropdown>
                        <el-button color="#2D2D2D" type="primary">
                        Project<el-icon class="el-icon--right"><arrow-down /></el-icon>
                        </el-button>
                        <template #dropdown>
                        <el-dropdown-menu v-for="project in projects" :key="project"> 
                          <el-dropdown-item @click="handleProject(project.name)">{{project.name}}</el-dropdown-item>
                        </el-dropdown-menu>
                        </template>
                    </el-dropdown>
                      <el-button color="#2617b0" type="primary" style="margin-left: 250px" @click="handlePost">Post</el-button>
                    </el-container>
                  </template>
                </el-card>
                <el-card v-for="post in posts" :key="post" class="box-card">
                  <template #header>
                  <el-row>
                  <User style="width: 40px; height: 40px; margin-right: 20px" />
                  <div>
                  <span>{{ post.user }}</span>
                  <span class="project">{{post.project}}</span>
                  <div class="time">{{post.timestamp}}</div>
                  </div>
                  </el-row>
                  <div class="comments">{{ post.description }}</div>
                  <el-row class="mb-4" style="margin-top: 20px;">
                  <div class="comments">{{post.upvotes}}</div>
                  <el-button color="#2D2D2D" type="primary" @click="handleUpvote(post)">
                    <el-icon class="el-icon--left"><Top /></el-icon>
                  </el-button>
                  <el-button color="#2D2D2D" type="primary">
                    Comments<el-icon class="el-icon--right"><ChatDotSquare /></el-icon>
                  </el-button>
                  <el-button color="#2D2D2D" type="primary">
                    Share<el-icon class="el-icon--right"><Position /></el-icon>
                  </el-button>
                  </el-row>  
                </template>
                <div class="comments" v-for="comment in post.comments" :key="comment">{{comment}}</div>
                <div class="input-header" style="margin-top: 10px">
                <el-input v-model="post.comments[-1]" placeholder="Write a comment." />
                <el-button color="#2617b0" type="primary" style="margin-left: 15px;" @click="handleComment(post)">
                    Share<el-icon class="el-icon--right"><Position /></el-icon>
                  </el-button>
                </div>
                </el-card>
            </el-space>
            <el-space direction="vertical">
            <h1>Followers</h1>
            <el-card v-for="fan in fans" :key="fan" class="fan-card">
              <template #header>
                <User style="width: 20px; height: 20px; margin-right: 20px" />
                <span>{{ fan.user }}</span>
                
              </template>
            <span>{{ fan.description }}</span>
            </el-card>
          </el-space>
        </el-main>
       
  </el-container>

  <p>{{input}}</p>
</div>  
</template>

<script>
  import { Picture, User, ArrowDown, Top, ChatDotSquare, Position } from "@element-plus/icons-vue"
  import { ref } from 'vue'
  import allPosts from '@/data/posts.js'
  import allProjects from '@/data/projects.js'
  import allfans from '@/data/fans.js'
  import Navbar from "../components/navbar.vue"
  const input = ref('')
  var project = ''

  const shorten = (x) => {
    var result = ''
    var max = 100
    while(x.length > max) {
      result += x.slice(0, max) + '\n';
      x = x.slice(max);
    }
    return result += x
  }

  const getDate = () => {
    return new Date().toString().substring(0, 21);
  }

  export default {
    setup() {
      const posts = ref(allPosts)
      const projects = ref(allProjects)
      const fans = ref(allfans)
      return { posts, input, projects , fans}
    },
    components: {
      Picture,
      User,
      ArrowDown,
      Top,
      ChatDotSquare,
      Position,
      Navbar
    },
    methods: {
      handlePost: function () {
          ref(allPosts).value.unshift({
              user: "Christopher Luey",
              description: shorten(input.value),
              project: project,
              timestamp: getDate(),
              upvotes: 0,
              comments: []
          });
          input.value = ''
      }, 
      handleProject: function (name) {
        project = name
      },
      handleComment: function (post) {
        //alert(post.comments[-1])
        for (var x of ref(allPosts).value) {
            if (x == post) {
                post.comments.push(shorten(post.comments[-1]))
                post.comments[-1] = ""
            }
        }
      },
      handleUpvote: function (post) {
          for (var x of ref(allPosts).value) {
              if (x == post) {
                  post.upvotes += 1
              }
          }
      }
    }
  }
</script>

<style lang="scss">
.time {
    color: #979797;
    font-size: 75%;
    margin-bottom: 10px;
}
.project {
    margin-left: 15px;
    color: #2617b0
}
.input-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.common-layout {
  .card-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .comments {
    color: #979797;
  }
  .el-menu {
      height: 40px;
  }
  .el-dropdown-link {
      color: white;
      height: 40px;
      position: bottom;
  }
  .box-card {
    background-color: #2D2D2D;
    color: white;
    width: 600px;
  }
  .update-card {
    background-color: #2D2D2D;
    color: white;
    width: 600px;
    height: 100px;
    position: top;
  }
  .el-header {
    background-color: #2D2D2D;
    text-align: left;
    color: var(--el-text-color-primary);
    line-height: 60px;
    height: 100px;
  }
  body > .el-container {
    margin-bottom: 40px;
  }
  .el-main {
    background-color: black;
    padding: 50;
    color: var(--el-text-color-primary);
  }

  .el-aside {
    background-color: #2D2D2D;
    text-align: center;
    line-height: 5px;
    color: var(--el-text-color-primary);
    text-align: center;
  }
  .fan-card {
    background-color: #2D2D2D;
    color: white;
    width: 200px;
  }
  
}
</style>
