<template>
    <div>
        <LazyTheHeader v-if="isShow"/>
        <button @click="isShow = true">show header</button>
        <app-button>click</app-button>
        <h1>Home</h1>
        <nuxt-link to="/">Go to home</nuxt-link>
        <nuxt-link to="/about" no-prefetch>Go to About</nuxt-link>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isShow: false,
        }
    },
}
</script>

<style>
.nuxt-link-exact-active{
    background-color: #ccc;
}

.nuxt-link-prefetched{
    text-decoration: none;
}
</style>