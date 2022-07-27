<template>
  <div class="card">
    <h3> {{title}}</h3>
    <div class="card-content">
    {{content}}    
    </div>
    <a href="#">visualizza post</a>
  </div>
</template>

<script>
export default {
    name: 'BaseCard',
    props: {
        title:{
            type:String
        },
        content: {
            type:String
        },
    }
}
</script>

<style lang="scss" scoped>
.card{
    background-color: rgb(202, 199, 199);
    border-radius: 1.25rem;
    box-shadow: 0px 0px 2px 2px black;
    padding: .625rem;
    margin: .625rem;
}
</style>