<template lang="pug">
.nav
    v-navigation-drawer(v-model="drawer" persistent=true)
        v-toolbar( flat class="transparent")
            v-list( class="pa-0")
                router-link(to="/") 
                    v-list-tile( tag="ul") fA
        v-divider
        v-list( dense class="pt-0")
                v-list-tile( v-for="(item,$index) in $store.state.pageComponents.list" ripple  v-bind:to="item.link" :key="$index")
                    v-list-tile-title {{ item.title}}
    v-toolbar( dark )
        v-toolbar-side-icon(@click.native.stop="drawer = !drawer")
        v-toolbar-title(class="white--text") 
            //v-btn( icon)
                v-icon arrow_back
            router-link(to="/" ) 
                v-btn( icon)
                    v-icon home
</template>
<style lang="scss" scoped>
    a{
        text-decoration: none;
    }
</style>

<script>
export default {
    data(){
        return{
            drawer: false,
             }
    }
}
</script>
