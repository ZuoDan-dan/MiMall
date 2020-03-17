<template>
    <div>
        
        <order-header></order-header>
        cart
        <nav-footer></nav-footer>
    </div>
</template>
<style lang="stylus">

</style>
<script>
import OrderHeader from './../components/OrderHeader'
import NavFooter from './../components/NavFooter'
export default {
    name:"cart",
     components:{
        OrderHeader,
        NavFooter
    }
}
</script>>