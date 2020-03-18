<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<style>
@import './assets/scss/reset.scss';


</style>

<script>
// import storage from './storage'
export default {
  name: 'App',
  components: {
    
  },
  data(){
    return {

    }
  },
  mounted(){
    //  storage.setItem('a',1)
    //  storage.setItem('user',{b:1})
    // storage.setItem('abc',{a:1},'user')
    // storage.clear('b');
    // storage.clear('b','user');
  },
  methods:{

  }
}
</script>

