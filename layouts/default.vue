<template lang="pug">
  v-app( light)
    navigation
    v-container-fluid.container
        main
          nuxt
</template>

<script>
import navigation from '../components/navigation'
export default {
  components:{
    navigation
  }
}
</script>

<style lang="scss" scoped>
.container {
    display: flex;
}

main {
    //float: right;
    width: 94%;
    margin: 0 3%;
   
}
</style>
