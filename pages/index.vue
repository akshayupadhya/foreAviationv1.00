<template lang="pug">
  .app
    .main-box
      .text1
        img(src="/AVITAION_HYDRABAD-02.png")
        //h2.name ForeAviation
      h5 {{$store.state.pagedata.home.welcome}}
    navList
    ul.iconfooter
      li(v-for="items in $store.state.pageComponents.linklist")
        micon(v-bind:item="items")
</template>

<style lang="scss" >
.app{
 // border: 1px solid white;
  height: 90vh;
  display: flex;
  flex-direction: column;
  justify-content:center;
  align-items: center;
  .main-box{
      .text1{
        display: flex;
        flex-direction: row;
        justify-content: center;
        img{
          transform: scaleX(2);
          //transform: scale(0.2);
          //border: 1px solid white;
        }
        
        .name{
          //border: 1px solid white;
          padding:0% 5% 0% 5%;
          color: whitesmoke;
          margin: 0 3%;
        }
      }
      h5 {
        color: whitesmoke;
        }
    }
  }

.iconfooter{
  //border: 1px solid wheat;
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: center;
  width: 100%;
    li{
      margin: 2% 5% ;
      list-style: none;
    }
  }
</style>
<script>
import micon from '../components/micon.vue'
import navList from '../components/navlist-home.vue'
export default {
  layout:"home",
  data(){
    return{
      
    }
  },components:{
    micon,
    navList
  }
}
</script>
