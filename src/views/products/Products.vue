<template>
    <div class="header">
        <!-- 头部组件 -->
        <CallBank></CallBank>
        <!--第一层下拉菜单 -->
    <van-dropdown-menu>
        <van-dropdown-item title="综合" >
        <van-switch-cell :title="item.title" v-for="item in list" :key="item.id"/>
        </van-dropdown-item>
        <van-dropdown-menu :overlay='false' active-color='#e93b3d' >
        <van-dropdown-item title="销量"></van-dropdown-item>
        <van-dropdown-item title="有货优先">
            <div class="checkbox" >
                <van-checkbox-group v-model="result" v-for="item in list" :key="item.id">
                    <van-checkbox :name="item.id">{{item.title}}</van-checkbox>
               </van-checkbox-group>
            </div>
        </van-dropdown-item>
        <van-dropdown-item title="筛选"></van-dropdown-item>
        </van-dropdown-menu>
    </van-dropdown-menu>

<van-card
  price="5999"
  desc="145996条评价 好评率97%"
  title="华为 HUAWEI Mate 30 Pro 5G 麒麟990 OLED环幕屏双4000万徕卡电影四摄8GB+256GB丹霞橙5G全网通手机"
  thumb="//img13.360buyimg.com/n2/s240x240_jfs/t1/90139/34/1379/180822/5dbe8875E02dc2e95/c78c80a4116ee57d.jpg!q70.jpg"
>
<div slot="tags">
    <van-tag plain type="danger">6.4英寸</van-tag>
    <van-tag plain type="danger">128G</van-tag>
    <van-tag plain type="danger">黑色</van-tag>
  </div>
  </van-card>
  <van-card
  price="5999"
  desc="145996条评价 好评率97%"
  title="华为 HUAWEI Mate 30 Pro 5G 麒麟990 OLED环幕屏双4000万徕卡电影四摄8GB+256GB丹霞橙5G全网通手机"
  thumb="https://img10.360buyimg.com/mobilecms/s316x316_jfs/t1/105914/2/5569/375378/5dee5263Eea787d18/9fa10292627688a7.jpg!q70.dpg.webp"
>
<div slot="tags">
    <van-tag plain type="danger">6.4英寸</van-tag>
    <van-tag plain type="danger">128G</van-tag>
    <van-tag plain type="danger">黑色</van-tag>
  </div>
  </van-card>
  <van-card
  price="2699"
  desc="145996条评价 好评率97%"
  title="华为 HUAWEI Mate 30 Pro 5G 麒麟990 OLED环幕屏双4000万徕卡电影四摄8GB+256GB丹霞橙5G全网通手机"
  thumb="https://img12.360buyimg.com/mobilecms/s316x316_jfs/t1/84947/8/5893/253152/5defcacaEc6653d63/c0cb236679f91e4e.jpg!q70.dpg.webp"
>
<div slot="tags">
    <van-tag plain type="danger">6.4英寸</van-tag>
    <van-tag plain type="danger">128G</van-tag>
    <van-tag plain type="danger">黑色</van-tag>
  </div>
  </van-card>
  <van-card
  price="5999"
  desc="145996条评价 好评率97%"
  title="华为 HUAWEI Mate 30 Pro 5G 麒麟990 OLED环幕屏双4000万徕卡电影四摄8GB+256GB丹霞橙5G全网通手机"
  thumb="https://img13.360buyimg.com/mobilecms/s316x316_jfs/t1/79596/30/11549/676613/5d901c88Ec7a97d29/d189e56d89d975b6.jpg!q70.dpg.webp"
>
<div slot="tags">
    <van-tag plain type="danger">6.4英寸</van-tag>
    <van-tag plain type="danger">128G</van-tag>
    <van-tag plain type="danger">黑色</van-tag>
  </div>
  </van-card>
  <van-card
  price="5999"
  desc="145996条评价 好评率97%"
  title="华为 HUAWEI Mate 30 Pro 5G 麒麟990 OLED环幕屏双4000万徕卡电影四摄8GB+256GB丹霞橙5G全网通手机"
  thumb="https://img14.360buyimg.com/mobilecms/s316x316_jfs/t1/51336/1/8104/201268/5d5b5213Ec0ea1a1d/ca1e456c486d6ed7.jpg!q70.dpg.webp"
>
<div slot="tags">
    <van-tag plain type="danger">6.4英寸</van-tag>
    <van-tag plain type="danger">128G</van-tag>
    <van-tag plain type="danger">黑色</van-tag>
  </div>
  </van-card>
</div>


</template>
<script>
import CallBank from '@/components/CallBank.vue'
export default {
    data(){
        return{

            list:[
                {
                    id:1,title:'综合'
                },
                {
                    id:2,title:'最新上架'
                },
                {
                    id:3,title:'价格最低'
                },
                {
                    id:4,title:'价格最高'
                },
                {
                    id:5,title:'评价最多'
                },
            ],
           result:[]
        }
    },
    components:{
        CallBank
    }
}
</script>
<style lang="scss">
.header{
    .van-dropdown-menu__item{
    width:100px;
}
.van-cell__value{
    display: none;
}
.van-overlay{
    background:#ccc;
}
.checkbox{
 .van-checkbox__label {
    margin-left: 8px;
    color: #323233;
    font-size: 18px;
    margin: 10px;
}
}
.mint-searchbar-cancel{
    display: none;
}
}
</style>
