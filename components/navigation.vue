<template lang="pug">
.nav
    v-navigation-drawer(v-model="drawer" )
        v-toolbar( flat class="transparent")
            v-list( class="pa-0")
                router-link(to="/") 
                    v-list-tile( tag="ul") fA
        v-divider
        v-list( dense class="pt-0")
            v-list-tile( v-for="(item,$index) in list" :key="$index")
                nuxt-link( :to="item.link") 
                    v-list-tile-title( dark  ) {{ item.title}}
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
import {list} from '../assets/js/list.js'
export default {
    data(){
        return{
            drawer: false,
            list
        }
    }
}
</script>
