<template>
    <div>
        <h1 v-if="error.statusCode === 404">Not found</h1>
        <nuxt-link to="/">Home</nuxt-link>
    </div>
</template>

<script>
export default {
    props: ["error"],
}
</script>