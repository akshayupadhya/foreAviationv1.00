<template lang="pug">
.button
    
    router-link( :to="item.link") 
       v-btn.button( dark  ) {{ item.title}}
                
</template>

<script>
export default {
  props: ['item'],
  data() {
    return {
    }
  },
 
}
</script>
<style lang="scss" scoped>
a {
  text-decoration: none;
}

.button:hover .button:active {
  box-shadow: 3px 3px 1px 0 #fff
}
</style>

