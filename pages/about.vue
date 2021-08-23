<template>
    <div>
        <h1>About</h1>
        <nuxt-link to="/">Go to Home</nuxt-link>
        <nuxt-link to="/about">Go to About</nuxt-link>
    </div>
</template>

<script>
import { useMeta, defineComponent } from '@nuxtjs/composition-api';

export default defineComponent({
    head: {},
    setup() {
        useMeta({ 
            title: "About",
            meta: [
                { hid: 'description', name: 'description', content: 'about page' },
            ]
        });
    }
})
</script>