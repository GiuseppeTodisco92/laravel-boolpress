<template>
  <section>
    <div class="container">
        
    <ul class="row">
      <li class="col-4" v-for="post in posts" :key="post.slug">
        <base-card :title="post.title" :content="post.content" />
      </li>
    </ul>
    </div>
  </section>
</template>

<script>
import BaseCard from '../commons/BaseCard.vue';

export default {

    name:'PostsSection',

      components: { 
        BaseCard
         },
    data(){
      return{
        posts: []
      };
    },
    created(){
      axios.get('http://127.0.0.1:8000/api/posts')
      .then((res)=>{
        this.posts = res.data;

      })
      .catch((e) => {
        console.log(e);
      })
    },
}
</script>

<style lang="scss" scoped>
    ul{
        list-style: none;
    }
</style>