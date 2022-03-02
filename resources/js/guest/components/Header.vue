<template>
    <header>
        <h2>Header</h2>
        <a href="/admin/home">Area riservata</a>

        <nav>
            <li>
                <router-link :to="{ name: 'home' }">Home</router-link>
            </li>
            <li>
                <router-link :to="{ name: 'about' }">Chi Siamo</router-link>
            </li>
            <li>
                <router-link :to="{ name: 'categories' }">Categorie</router-link>
            </li>
        </nav>
    </header>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style>

</style>