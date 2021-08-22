<template>
    <div>
        <LazyTheHeader v-if="isShow"/>
        <button @click="isShow = true">show header</button>
        <app-button>click</app-button>
        <h1>Home</h1>
        <img class="img" src="~/assets/images/nuxt-icon.png" alt="">
        <div class="block"></div>
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

<style lang="scss" scoped>
.nuxt-link-exact-active{
    background-color: $black;
    color: $white;
}

.nuxt-link-prefetched{
    text-decoration: none;
}

.img{
    width: 300px;
    height: 300px;
}

.block{
    width: 300px;
    height: 300px;
    background-image: url('~assets/images/nuxt-icon.png');
    background-size: contain;
}
</style>