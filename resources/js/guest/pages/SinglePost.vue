<template>
  <div>
      <h2>{{$route.params.slug}}</h2>
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
            console.log(response.data);
        })
    }
}
</script>

<style>

</style>