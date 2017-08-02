<template lang="pug">
  .app
    .main-box
      .text
        h2.name ForeAviation
    navList
    ul.iconfooter
      li(v-for="items in linklist")
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
      .text{
        .name{
          padding:2% 5% ;
          color: whitesmoke;
          margin: 0 3%;
        }
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
import {linklist} from '../assets/js/list'
import micon from '../components/micon.vue'
import mcaption from '../components/caption.vue'
import navList from '../components/Navlist-home.vue'
export default {
  layout:"home",
  data(){
    return{
      linklist
    }
  },components:{
    "micon":micon,
    "mcaption":mcaption,
    navList
  }
}
</script>
