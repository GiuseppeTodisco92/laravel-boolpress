<template>
  <main>
    <posts-section/>
  </main>
</template>

<script>
import PostsSection from '../section/PostsSection.vue'
export default {
  
    name:'BaseMain',
    components: { 
      PostsSection
       },
}
</script>

<style>

</style>