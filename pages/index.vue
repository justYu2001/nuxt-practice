<template>
    <div>
        <h1>Home</h1>
        <nuxt-link to="/">Go to home</nuxt-link>
        <nuxt-link to="/about" no-prefetch>Go to About</nuxt-link>
    </div>
</template>

<style>
.nuxt-link-exact-active{
    background-color: #ccc;
}

.nuxt-link-prefetched{
    text-decoration: none;
}
</style>