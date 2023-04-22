<template>
  <body class="bg">
    <div class="cards-and-title">
      <div class="title">
        <h2 class="title-h2">Designed for business teams like yours</h2>
        <p class="title-p">
          Here at Flowbite we focus on markets where technology, innovation, and capital can unlock long-term value and drive economic growth.
        </p>
      </div>
      <el-row  :gutter="5" class="cards">
        <el-col
          v-for="(o, index1) in 3"
          :key="o"
          :span="8"
        >
          <el-card class="card">
            <template #header>
              <div>
                <h3 class="card-h3" >{{t[index1][0]}}</h3>
                <p card-p>{{t[index1][1]}}</p>
              </div>
              <div class="card-spans">
                <span class="card-price">{{t[index1][2]}}</span>
                <span class="card-month">/month</span>
              </div>
            </template>
            <ul role="list" class="card-ulist">
              <li v-for="(x,index2) in 4" class="card-list">
                <el-icon class="icon"><Check /></el-icon>
                <span>{{ t[index1][index2+3] }}</span>
              </li >
            </ul>
            <a href="https://www.youtube.com/" class="btn">Get started</a>
          </el-card>
        </el-col>
      </el-row>
    </div>  
  </body>
</template>
<script setup>
  import {Check} from '@element-plus/icons-vue'
  const t=[
    ['Starter','Best option for personal use & for your next project.','$29',
    'Individual configuration','No setup, or hidden fees','Team size: 1 developer','Premium support: 6 months','Free updates: 6 months'],
    ['Company','Relevant for multiple users, extended & premium support.','$99',
    'Individual configuration','No setup, or hidden fees','Team size: 10 developers','Premium support: 24 months','Free updates: 24 months'],
    ['Enterprise','Best for large scale uses and extended redistribution rights.','$499',
    'Individual configuration','No setup, or hidden fees','Team size: 100+ developers','Premium support: 36 months','Free updates: 36 months']
    ];
</script>
<style scoped>
.bg{
  background-color: rgb(17 24 39);
  height: 100%;
  font-family: Arial, Helvetica, sans-serif;
}
.cards-and-title{
  padding-left: 1rem;
  padding-right: 1rem;
  padding-top: 2rem;
  padding-bottom: 2rem;
  margin-left: auto;
  margin-right: auto;
  max-width: 1280px;
}
.title{
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 2rem;
  text-align: center;
  max-width: 768px;
}
.title-h2{
  margin-bottom: 1rem;
  font-size: 2.25rem;
  line-height: 2.5rem;
  font-weight: 800;
  letter-spacing: -0.025em;
  color: #ffffff;
}

.title-p{
  margin-bottom: 1.25rem;
  color: #9ca3af;
  font-weight: 300;
}

.cards{
  margin-top: 2rem;
}
.card{
  padding: 1.5rem;
  margin-left: auto;
  margin-right: auto;
  background-color: #1F2937;
  color: #ffffff;
  text-align: center;
  max-width: 32rem;
  border-radius: 0.5rem;
  border-width: 1px;
  border-color: #4b5563;
  box-shadow: 0 1px 3px rgba(0,0,0,0.1), 0 1px 2px rgba(0,0,0,0.06);
}
.card-h3{
  margin-bottom: 1rem;
  font-size: 1.5rem;
  line-height: 2rem;
  font-weight: 600;
}
.card-p{
  color: #9ca3af;
  font-weight: 300;
}
.card-spans{
  display: flex;
  margin-top: 2rem;
  margin-bottom: 2rem;
  justify-content: center;
  align-items: baseline;
}
.card-price{
  margin-right: 0.5rem;
  font-size: 3rem;
  font-weight: 800;
}
.card-month{
  color: #9ca3af;
}

.card-ulist{
  margin-bottom: 2rem;
  margin-top: 1rem;
  text-align: left;
}

.icon{
  margin-right: 1rem;
  color: cadetblue;
}

.card-list{
  display: flex;
  margin-left: 0.75rem; 
  margin-top: 0.875rem;
  align-items: center;
}
.btn{
  padding-top: 0.625rem;
  padding-bottom: 0.625rem;
  padding-left: 1.25rem;
  padding-right: 1.25rem;
  color: #ffffff;
  font-size: 0.875rem;
  line-height: 1.25rem;
  font-weight: 500;
  text-align: center;
  border-radius: 0.5rem;
  background-color: #425876;
  text-decoration: none;
}
.btn:hover{
  color: black;
  background-color: #d2dae5;
}
</style>