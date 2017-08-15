<template lang="pug">
.about
  h1 about
  .data
    p(v-for="data in $store.state.pagedata.about") {{data}}
</template>

<script>
export default {
  layout:"appLayout"
}
</script>
