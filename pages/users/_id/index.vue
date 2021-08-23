<template>
    <div>
        <p>ID:{{ user.id }}</p>
        <p>name: {{ user.name }}</p>
        <p>email: {{ user.email }}</p>
    </div>
</template>

<script>
export default {
    async asyncData({ params, error }) {
        try {
            const id = params.id;
            const url = `https://jsonplaceholder.typicode.com/users/${id}`;
            const res = await fetch(url);
            const userInfo = await res.json();
            return { user: userInfo };
        } catch (e) {
            error(e);
        }
    },
    validate({ params }){
        return /^\d+$/.test(params.id);
    },
}
</script>