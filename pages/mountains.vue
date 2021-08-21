<template>
    <p v-if="$fetchState.pending">Fetch mountains...</p>
    <p v-else-if="$fetchState.error">Error</p>
    <div v-else>
        <h1>Mountains</h1>
        <ul>
            <li v-for="mountain in mountains">{{ mountain.title }}</li>
        </ul>
        <button @click="$fetch">Refresh</button>
    </div>
</template>

<script>
export default {
    head() {
        return {
            title: this.title,
            meta: [
                { hid: 'description', name: 'description', content: 'mountaions page' },
            ],
            script: [
                {
                    src: 'https://cdnjs.cloudflare.com/ajax/libs/jquery/3.1.1/jquery.min.js',
                    body: true,
                }
            ],
        }
    },
    data() {
        return {
            mountains: [],
            title: "mountains",
        }
    },
    watch: {
        "$route.query": "$fetch",
    },
    async fetch(){
        console.log("query", this.$route.query.id);
        const url = "https://api.nuxtjs.dev/mountains";
        const res = await fetch(url);
        this.mountains = await res.json();
    },
}
</script>