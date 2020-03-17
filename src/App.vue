<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
// import storage from './storage'
export default {
  name: 'App',
  components: {
    
  },
  data(){
    return {
       res:{}
    }
  },
  mounted(){
    //  storage.setItem('a',1)
    //  storage.setItem('user',{b:1})
    // storage.setItem('abc',{a:1},'user')
    // storage.clear('b');
    // storage.clear('b','user');

     //本地加载请求静态json文件的形式
    // this.axios.get('/mock/user/login.json').then((res)=>{
    //   this.res=res;
    // })

   //通过easy-mock平台实现数据mock 弊端：easy-mock平台容易崩
  //  this.axios.get('/user/login').then((res)=>{
  //     this.res=res;
  //   })
  
  //本地集成mockjs实现数据mock
  //1.cnpm i mockjs --save-dev
  //2.src下新建mock文件夹，文件夹下新建api.js
  //3.mian.js中 require('./mock/api')
   this.axios.get('/user/login').then((res)=>{
      this.res=res;
    })

  },
  methods:{

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
