<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<style lang='scss'>
@import './assets/scss/reset.scss';
@import './assets/scss/config.scss';
@import './assets/scss/button.scss';
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
    if(this.$cookie.get('userId')){
      this.getUser();
      this.getCartCount();
    }
    //  storage.setItem('a',1)
    //  storage.setItem('user',{b:1})
    // storage.setItem('abc',{a:1},'user')
    // storage.clear('b');
    // storage.clear('b','user');
  },
  methods:{
      getUser(){
        this.axios.get('/user').then(
          (res={})=>{
            this.$store.dispatch('saveUserName',res.username);
          }
        )
      },
      getCartCount(){
        this.axios.get('/carts/products/sum').then((res=0)=>{
            this.$store.dispatch('saveCartCount',res);
        })
      }
  }
}
</script>

