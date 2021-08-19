<template>
    <h1>ID:{{ id }}</h1>
</template>

<script>
import { useRoute } from '@nuxtjs/composition-api';

export default {
    setup() {
        const route = useRoute().value;

        return {
            id: route.params.id,
        }
    }
}
</script>