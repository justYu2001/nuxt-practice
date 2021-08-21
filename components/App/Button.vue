<template>
    <button class="btn">
        <slot></slot>
    </button>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
.btn{
    background-color: green;
    color: #fff;
    padding: 10px 20px;
    border-radius: 5px;
    border: 0;
}
</style>