<template>
    <h1>Le categorie</h1>
</template>

<script>
export default {
    name: "Categories",
    data(){
        return{
            categories: []
        }
    },
    created(){
        axios.get("/api/categories")
            .then((response) => {
                this.categories = response.data;
            })
    }
}
</script>

<style>

</style>