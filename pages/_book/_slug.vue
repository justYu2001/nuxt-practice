<template>
    <div>
        <h1>book: {{ book }}</h1>
        <h1>slug: {{ slug }}</h1>
    </div>
</template>

<script>
import { useAsync, useContext } from '@nuxtjs/composition-api';

export default {
    setup() {
        const { params } = useContext();

        const book = useAsync(() => params.value.book);
        const slug = useAsync(() => params.value.slug);

        return {
            book,
            slug,
        }
    }
}
</script>