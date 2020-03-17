<template>
 <div>
     order
     <order-header></order-header>
     <router-view></router-view>
     <nav-footer></nav-footer>
 </div>
</template>
<style lang="stylus">

</style>
<script>
import OrderHeader from './../components/OrderHeader'
import NavFooter from './../components/NavFooter'

export default {
    name:"order",
    components:{
        OrderHeader,
        NavFooter
    }
}
</script>>