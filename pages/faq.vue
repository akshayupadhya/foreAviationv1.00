<template lang="pug">
.faq
  h1 FAQ
  .data(v-for="(data,i) in $store.state.pagedata.faq")
    h3 {{(i+1)+") "+Object.keys(data)}}
    p {{"Answer: "+Object.values(data)}}
</template>
