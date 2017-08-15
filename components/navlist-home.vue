<template lang="pug">
  .linklist
    ul
        li(v-for="(item,i) in $store.state.pageComponents.list" v-if="i!=0") 
            router-link(:to="item.link") 
                 v-btn(dark) {{item.title}}
</template>
<style lang="scss" scoped>
.linklist{
    //border: 1px solid whitesmoke;
    width: 120%;

}
    ul{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        a{
            text-decoration: none;
        }
        li{
            display: inline-block
        }
    }
</style>