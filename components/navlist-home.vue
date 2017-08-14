<template lang="pug">
  .linklist
    ul
        li(v-for="item in $store.state.pageComponents.list" ) 
            router-link(:to="item.link") 
                 v-btn(dark) {{item.title}}
</template>
<style lang="scss" scoped>
.linklist{
    //border: 1px solid whitesmoke;
    width: 100%;

}
    ul{
        display: flex;
        justify-content: space-between;
        a{
            text-decoration: none;
        }
        li{
            display: inline-block
        }
    }
</style>