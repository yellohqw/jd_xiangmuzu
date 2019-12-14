<template>
<div class="callBank">
 <mt-header>
  <router-link to="/cate" slot="left">
    <mt-button icon="back"></mt-button>
   </router-link>
  <mt-button icon="more" slot="right" @click="ball"></mt-button>
</mt-header>
 <mt-search placeholder="搜索你想要的东西"></mt-search>
</div>
</template>
<script>
export default {
data(){
    return{
    //  ishow:true
    }
},
methods:{
ball(){
    this.ishow=false
    console.log(11)
}
}
}
</script>
<style lang='scss' >
.callBank{
 position: relative;
.mint-header {
        background:#fff;
    }
.mint-header-button{
    color: #252525
}
.mint-search{
    height:0px;
}
.mint-searchbar {
    position: absolute;
    left: 40px;
    top:6px;
    height: 30px;
    width: 300px;
    border-radius: 15px;
    background:#fff;
    .mint-searchbar-inner{
        height: 20px;
        background: #f7f7f7;
        border-radius: 15px;
        .mint-searchbar-core{
            background: #f7f7f7;
            font-size:14px;
            margin-left:.133333rem;
        }
    }
}
}

</style>

