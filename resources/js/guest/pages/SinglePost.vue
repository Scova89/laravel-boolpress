<template>
  <div>
      <h1>{{post.title}}</h1>
      <p>{{post.content}}</p>
  </div>
</template>

<script>
export default {
    name: "SinglePost",
    data(){
        return{
            post:{}
        }
    },
    created(){
       // console.log(this.$route.params.slug);
       axios.get(`/api/posts/${this.$route.params.slug}`)
        .then((response) => {
            this.post = response.data;
        })
    }
}
</script>

<style>

</style>